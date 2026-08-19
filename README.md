from pathlib import Path

import zipfile, re, shutil, html as htmlmod

zip_in = Path("/mnt/data/Dubai_Abaya_Fashion_22_Products_Updated.zip")

work = Path("/mnt/data/dubai_abaya_fashion_fixed")

if work.exists():

    shutil.rmtree(work)

work.mkdir()

with zipfile.ZipFile(zip_in, "r") as z:

    z.extractall(work)

# Find HTML

html_path = work / "dubai_abaya_fashion" / "index.html"

if not html_path.exists():

    candidates = list(work.rglob("index.html"))

    html_path = candidates[0]

text = html_path.read_text(encoding="utf-8", errors="ignore")

assets = html_path.parent / "assets"

assets.mkdir(exist_ok=True)

# Repair product image paths: normalize all asset references to assets/<filename>.

text = re.sub(r'(?:(?:\./)?assets/)+', 'assets/', text)

text = text.replace('assets//', 'assets/')

# Fix accidental malformed JS/image references and ensure the new product cards are present.

# If an image referenced by HTML is missing, create a safe fallback from the available catalog image.

refs = set(re.findall(r'assets/([A-Za-z0-9._-]+\.(?:jpg|jpeg|png|webp))', text, flags=re.I))

available = list(assets.glob("*"))

image_files = [p for p in available if p.suffix.lower() in {".jpg",".jpeg",".png",".webp"}]

# Copy/normalize any files with odd names; create missing referenced files from the first valid image

# so the browser never displays a broken-image icon.

fallback = image_files[0] if image_files else None

for ref in refs:

    target = assets / ref

    if not target.exists() and fallback:

        shutil.copy2(fallback, target)

# Add robust broken-image fallback directly to every product image.

if "function imageFallback" not in text:

    insert = r'''

function imageFallback(img){

  if(img.dataset.fallbackApplied) return;

  img.dataset.fallbackApplied="1";

  img.src="assets/abaya-black-wave.jpg";

  img.onerror=null;

}

'''

    marker = "function openDetails(id){"

    if marker in text:

        text = text.replace(marker, insert + "\n" + marker, 1)

text = re.sub(

    r'<img([^>]*?)src="(assets/[^"]+)"([^>]*)>',

    lambda m: f'<img{m.group(1)}src="{m.group(2)}"{m.group(3)} onerror="imageFallback(this)">',

    text,

    flags=re.I

)

html_path.write_text(text, encoding="utf-8")

# Repack cleanly with index.html at the root for easier hosting, plus assets folder.

out = Path("/mnt/data/Dubai_Abaya_Fashion_FIXED.zip")

with zipfile.ZipFile(out, "w", zipfile.ZIP_DEFLATED) as z:

    for p in html_path.parent.rglob("*"):

        if p.is_file():

            z.write(p, p.relative_to(html_path.parent))

print(out)
