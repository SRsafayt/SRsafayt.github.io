
from PIL import Image

from pathlib import Path

import shutil, zipfile, re

base = Path("/mnt/data/dubai_abaya_fashion")

assets = base / "assets"

assets.mkdir(exist_ok=True)

# The generated catalog image is a 4x2 grid. Crop each product into its own image.

sheet = Image.open("/mnt/data/a_clean_catalog_like_composite_image_a_grid_coll.png").convert("RGB")

boxes = [

    (14, 12, 326, 514), (345, 12, 658, 514),

    (678, 12, 991, 514), (1011, 12, 1323, 514),

    (14, 568, 326, 1069), (345, 568, 658, 1069),

    (678, 568, 991, 1069), (1011, 568, 1323, 1069),

]

names = [

    "abaya-green-flower.jpg", "abaya-red-lace.jpg",

    "abaya-black-stones.jpg", "abaya-olive-embroid.jpg",

    "abaya-lavender-fleur.jpg", "abaya-purple-embroid.jpg",

    "abaya-navy-lace.jpg", "abaya-black-wave.jpg",

]

for box, name in zip(boxes, names):

    crop = sheet.crop(box)

    # Keep the image clean and consistent for the website.

    crop.thumbnail((900, 1200), Image.Resampling.LANCZOS)

    crop.save(assets / name, quality=94, optimize=True)

html_path = base / "index.html"

html = html_path.read_text(encoding="utf-8")

# Fix the existing product object separator if needed.

html = html.replace(

    'desc:"A statement black design with premium-looking embroidery and a graceful silhouette."}\n\n7:',

    'desc:"A statement black design with premium-looking embroidery and a graceful silhouette."},\n7:'

)

# Add products 15-22 immediately before the existing closing "};".

products_end = html.find("};", html.find("const products="))

new_products = r'''

15:{title:"Pastel Green Flower Abaya",code:"DAF-015",img:"assets/abaya-green-flower.jpg",color:"Pastel Green",design:"Long floral front embroidery",fabric:"Flowing premium fabric",embroidery:"Pink & mint floral embroidery",category:"Abaya",availability:"Available",delivery:"UAE delivery available",sizes:["S","M","L","XL","XXL"],desc:"A soft pastel-green abaya with a beautiful floral embroidered front and matching cuff details."},

16:{title:"Ruby Red Lace Abaya",code:"DAF-016",img:"assets/abaya-red-lace.jpg",color:"Ruby Red",design:"Full front lace trim",fabric:"Smooth flowing fabric",embroidery:"Tone-on-tone floral lace",category:"Abaya",availability:"Available",delivery:"UAE delivery available",sizes:["S","M","L","XL","XXL"],desc:"A rich red abaya with elegant lace running along the front and sleeves."},

17:{title:"Black Crystal Abaya",code:"DAF-017",img:"assets/abaya-black-stones.jpg",color:"Black",design:"Crystal leaf embellishment",fabric:"Smooth flowing fabric",embroidery:"Sparkling crystal leaf details",category:"Abaya",availability:"Available",delivery:"UAE delivery available",sizes:["S","M","L","XL","XXL"],desc:"A dramatic black design with subtle sparkling embellishment across the upper body and sleeves."},

18:{title:"Olive Green Embroidered Abaya",code:"DAF-018",img:"assets/abaya-olive-embroid.jpg",color:"Olive Green",design:"Wide-sleeve embroidered style",fabric:"Flowing premium fabric",embroidery:"Fine floral embroidery",category:"Abaya",availability:"Available",delivery:"UAE delivery available",sizes:["S","M","L","XL","XXL"],desc:"An elegant olive-green abaya with a flowing silhouette and detailed embroidery."},

19:{title:"Lavender Fleur Abaya",code:"DAF-019",img:"assets/abaya-lavender-fleur.jpg",color:"Lavender Pink",design:"Fleur motif front design",fabric:"Lightweight flowing fabric",embroidery:"Delicate floral motifs",category:"Abaya",availability:"Available",delivery:"UAE delivery available",sizes:["S","M","L","XL","XXL"],desc:"A graceful lavender abaya with soft decorative motifs and a wide modest silhouette."},

20:{title:"Royal Purple Embroidered Abaya",code:"DAF-020",img:"assets/abaya-purple-embroid.jpg",color:"Royal Purple",design:"All-over luxury embroidery",fabric:"Premium flowing fabric",embroidery:"Rich floral embroidery",category:"Abaya",availability:"Available",delivery:"UAE delivery available",sizes:["S","M","L","XL","XXL"],desc:"A luxurious purple abaya with rich embroidery and an elegant occasion-ready finish."},

21:{title:"Navy Blue Lace Abaya",code:"DAF-021",img:"assets/abaya-navy-lace.jpg",color:"Navy Blue",design:"Long lace-panel design",fabric:"Smooth flowing fabric",embroidery:"Decorative lace edging",category:"Abaya",availability:"Available",delivery:"UAE delivery available",sizes:["S","M","L","XL","XXL"],desc:"A classic navy design with long decorative panels and refined lace-style edging."},

22:{title:"Black Wave Abaya",code:"DAF-022",img:"assets/abaya-black-wave.jpg",color:"Black",design:"Flowing wave-sleeve silhouette",fabric:"Smooth flowing fabric",embroidery:"Fine front and sleeve detailing",category:"Abaya",availability:"Available",delivery:"UAE delivery available",sizes:["S","M","L","XL","XXL"],desc:"A sophisticated black abaya with a dramatic flowing silhouette and refined detailing."},

'''

html = html[:products_end] + new_products + html[products_end:]

# Add the eight new cards before the existing empty-state marker.

card_anchor = '      <div class="empty" id="empty">No matching designs found.</div>'

new_cards = r'''

      <article class="card" data-name="Pastel Green Flower Abaya" data-type="abaya new" data-id="15">

        <div class="photo"><img src="assets/abaya-green-flower.jpg" alt="Pastel Green Flower Abaya"><button class="like" onclick="likeProduct(event,15)">♡</button><span class="tag">NEW ARRIVAL</span></div>

        <div class="card-info"><h3>Pastel Green Flower Abaya</h3><div class="meta">Pastel Green • Floral • Abaya</div><div class="card-bottom"><button class="details" onclick="openDetails(15)">VIEW DETAILS</button><button class="ask" onclick="ask(15)">ASK PRICE</button></div></div>

      </article>

      <article class="card" data-name="Ruby Red Lace Abaya" data-type="abaya new best" data-id="16">

        <div class="photo"><img src="assets/abaya-red-lace.jpg" alt="Ruby Red Lace Abaya"><button class="like" onclick="likeProduct(event,16)">♡</button><span class="tag">BEST SELLER</span></div>

        <div class="card-info"><h3>Ruby Red Lace Abaya</h3><div class="meta">Ruby Red • Lace • Abaya</div><div class="card-bottom"><button class="details" onclick="openDetails(16)">VIEW DETAILS</button><button class="ask" onclick="ask(16)">ASK PRICE</button></div></div>

      </article>

      <article class="card" data-name="Black Crystal Abaya" data-type="abaya best" data-id="17">

        <div class="photo"><img src="assets/abaya-black-stones.jpg" alt="Black Crystal Abaya"><button class="like" onclick="likeProduct(event,17)">♡</button><span class="tag">BEST SELLER</span></div>

        <div class="card-info"><h3>Black Crystal Abaya</h3><div class="meta">Black • Crystal • Abaya</div><div class="card-bottom"><button class="details" onclick="openDetails(17)">VIEW DETAILS</button><button class="ask" onclick="ask(17)">ASK PRICE</button></div></div>

      </article>

      <article class="card" data-name="Olive Green Embroidered Abaya" data-type="abaya new" data-id="18">

        <div class="photo"><img src="assets/abaya-olive-embroid.jpg" alt="Olive Green Embroidered Abaya"><button class="like" onclick="likeProduct(event,18)">♡</button><span class="tag">NEW ARRIVAL</span></div>

        <div class="card-info"><h3>Olive Green Embroidered Abaya</h3><div class="meta">Olive Green • Embroidery • Abaya</div><div class="card-bottom"><button class="details" onclick="openDetails(18)">VIEW DETAILS</button><button class="ask" onclick="ask(18)">ASK PRICE</button></div></div>

      </article>

      <article class="card" data-name="Lavender Fleur Abaya" data-type="abaya new" data-id="19">

        <div class="photo"><img src="assets/abaya-lavender-fleur.jpg" alt="Lavender Fleur Abaya"><button class="like" onclick="likeProduct(event,19)">♡</button><span class="tag">NEW ARRIVAL</span></div>

        <div class="card-info"><h3>Lavender Fleur Abaya</h3><div class="meta">Lavender • Fleur • Abaya</div><div class="card-bottom"><button class="details" onclick="openDetails(19)">VIEW DETAILS</button><button class="ask" onclick="ask(19)">ASK PRICE</button></div></div>

      </article>

      <article class="card" data-name="Royal Purple Embroidered Abaya" data-type="abaya best" data-id="20">

        <div class="photo"><img src="assets/abaya-purple-embroid.jpg" alt="Royal Purple Embroidered Abaya"><button class="like" onclick="likeProduct(event,20)">♡</button><span class="tag">BEST SELLER</span></div>

        <div class="card-info"><h3>Royal Purple Embroidered Abaya</h3><div class="meta">Royal Purple • Embroidery • Abaya</div><div class="card-bottom"><button class="details" onclick="openDetails(20)">VIEW DETAILS</button><button class="ask" onclick="ask(20)">ASK PRICE</button></div></div>

      </article>

      <article class="card" data-name="Navy Blue Lace Abaya" data-type="abaya new" data-id="21">

        <div class="photo"><img src="assets/abaya-navy-lace.jpg" alt="Navy Blue Lace Abaya"><button class="like" onclick="likeProduct(event,21)">♡</button><span class="tag">NEW ARRIVAL</span></div>

        <div class="card-info"><h3>Navy Blue Lace Abaya</h3><div class="meta">Navy Blue • Lace • Abaya</div><div class="card-bottom"><button class="details" onclick="openDetails(21)">VIEW DETAILS</button><button class="ask" onclick="ask(21)">ASK PRICE</button></div></div>

      </article>

      <article class="card" data-name="Black Wave Abaya" data-type="abaya best" data-id="22">

        <div class="photo"><img src="assets/abaya-black-wave.jpg" alt="Black Wave Abaya"><button class="like" onclick="likeProduct(event,22)">♡</button><span class="tag">BEST SELLER</span></div>

        <div class="card-info"><h3>Black Wave Abaya</h3><div class="meta">Black • Wave Sleeve • Abaya</div><div class="card-bottom"><button class="details" onclick="openDetails(22)">VIEW DETAILS</button><button class="ask" onclick="ask(22)">ASK PRICE</button></div></div>

      </article>

'''

if card_anchor in html:

    html = html.replace(card_anchor, new_cards + card_anchor, 1)

html_path.write_text(html, encoding="utf-8")

# Create a ZIP with the complete website.

zip_path = Path("/mnt/data/Dubai_Abaya_Fashion_22_Products_Updated.zip")

with zipfile.ZipFile(zip_path, "w", zipfile.ZIP_DEFLATED) as z:

    for path in base.rglob("*"):

        if path.is_file():

            z.write(path, path.relative_to(base.parent))

# Also provide the eight individual images in a separate ZIP.

images_zip = Path("/mnt/data/Dubai_Abaya_Fashion_8_Individual_Product_Images.zip")

with zipfile.ZipFile(images_zip, "w", zipfile.ZIP_DEFLATED) as z:

    for name in names:

        z.write(assets / name, name)

print("Done.")

print(f"Website ZIP: {zip_path}")

print(f"Individual images ZIP: {images_zip}")
