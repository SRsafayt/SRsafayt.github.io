

from pathlib import Path

import zipfile, textwrap, os

root = Path("/mnt/data/dubai-abaya-fashion")

root.mkdir(parents=True, exist_ok=True)

html = r'''<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<meta name="description" content="Dubai Abaya Fashion - Premium Abaya, Burqa and Kurta Collection">

<title>Dubai Abaya Fashion</title>

<style>

:root{

  --bg:#f5f3ef; --card:#fff; --dark:#111827; --gold:#d79a25;

  --green:#20c968; --muted:#6b7280; --line:#e5e7eb;

}

*{box-sizing:border-box}

html{scroll-behavior:smooth}

body{margin:0;font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Arial,sans-serif;background:var(--bg);color:#171717}

header{position:sticky;top:0;z-index:20;background:#111827;color:#fff;box-shadow:0 2px 12px #0002}

.nav{max-width:900px;margin:auto;padding:15px 18px;display:flex;align-items:center;justify-content:space-between;gap:12px}

.brand{font-weight:900;letter-spacing:.4px;color:#f4b84b;font-size:20px}

.nav a{color:#fff;text-decoration:none;margin-left:15px;font-size:14px}

.hero{max-width:900px;margin:auto;padding:28px 16px 18px}

.hero-box{border-radius:22px;padding:36px 22px;text-align:center;background:

linear-gradient(135deg,#111827,#30343b 55%,#151a20);color:#fff;box-shadow:0 14px 35px #0002}

.badge{display:inline-block;color:#111827;background:#f4b84b;border-radius:999px;padding:7px 13px;font-size:12px;font-weight:800}

h1{font-size:34px;line-height:1.12;margin:15px 0 10px}

.hero p{margin:0 auto 20px;color:#d7d9dd;max-width:580px}

.btn{display:inline-block;background:var(--green);color:#fff;text-decoration:none;border:0;border-radius:9px;padding:12px 20px;font-weight:800;cursor:pointer}

.controls{max-width:900px;margin:10px auto 4px;padding:0 16px}

.controls-row{display:flex;gap:8px;overflow:auto;padding-bottom:6px}

.filter{border:1px solid #d1d5db;background:#fff;padding:10px 15px;border-radius:999px;font-weight:700;white-space:nowrap;cursor:pointer}

.filter.active{background:#111827;color:#fff;border-color:#111827}

.section{max-width:900px;margin:0 auto;padding:22px 16px 50px}

.section-title{display:flex;justify-content:space-between;align-items:center;gap:10px;margin:5px 0 18px}

.section-title h2{margin:0;font-size:24px}

.refresh{background:#fff;border:1px solid #d1d5db;border-radius:9px;padding:10px 13px;font-weight:800;cursor:pointer}

.products{display:grid;grid-template-columns:1fr;gap:18px}

.card{background:var(--card);border:1px solid var(--line);border-radius:15px;overflow:hidden;box-shadow:0 5px 18px #0000000d}

.photo-wrap{position:relative;background:#e9e5df;aspect-ratio:4/3;overflow:hidden}

.photo-wrap img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .35s}

.card:hover img{transform:scale(1.03)}

.tag{position:absolute;top:12px;left:12px;background:#111827;color:#fff;padding:6px 9px;border-radius:999px;font-size:11px;font-weight:800}

.info{padding:16px}

.info h3{margin:0 0 9px;font-size:19px}

.meta{font-size:13px;color:#555;line-height:1.65;margin-bottom:14px}

.meta b{color:#222}

.whatsapp{display:block;text-align:center;background:var(--green);color:#fff;text-decoration:none;padding:12px;border-radius:9px;font-weight:800}

footer{background:#111827;color:#d7d9dd;text-align:center;padding:28px 16px}

footer strong{color:#f4b84b}

.lightbox{position:fixed;inset:0;background:#000d;display:none;align-items:center;justify-content:center;z-index:50;padding:18px}

.lightbox.show{display:flex}

.lightbox img{max-width:96%;max-height:90vh;border-radius:12px}

.close{position:absolute;right:18px;top:18px;color:#fff;font-size:30px;cursor:pointer}

@media(min-width:700px){

  .products{grid-template-columns:repeat(2,1fr)}

  h1{font-size:44px}

}

</style>

</head>

<body>

<header>

  <div class="nav">

    <div class="brand">DUBAI ABAYA FASHION</div>

    <nav>

      <a href="#products">Collection</a>

      <a href="#contact">Contact</a>

    </nav>

  </div>

</header>

<section class="hero">

  <div class="hero-box">

    <span class="badge">PREMIUM DUBAI COLLECTION</span>

    <h1>Elegant Abaya, Burqa & Kurta Collection</h1>

    <p>Premium designs, beautiful colours and custom sizes. Prices are available on WhatsApp.</p>

    <a class="btn" href="https://wa.me/971567439129?text=Hello%20Dubai%20Abaya%20Fashion%2C%20I%20would%20like%20to%20see%20your%20collection." target="_blank">Contact on WhatsApp</a>

  </div>

</section>

<div class="controls">

  <div class="controls-row">

    <button class="filter active" data-cat="All">All</button>

    <button class="filter" data-cat="Abaya">Abaya</button>

    <button class="filter" data-cat="Burqa">Burqa</button>

    <button class="filter" data-cat="Kurta">Kurta</button>

  </div>

</div>

<section class="section" id="products">

  <div class="section-title">

    <h2>Featured Collection</h2>

    <button class="refresh" id="refresh">↻ New Designs</button>

  </div>

  <div class="products" id="productsGrid"></div>

</section>

<footer id="contact">

  <p><strong>Dubai Abaya Fashion</strong></p>

  <p>Premium Quality • Custom Sizes Available</p>

  <p>WhatsApp: +971 56 743 9129</p>

</footer>

<div class="lightbox" id="lightbox">

  <span class="close" id="close">×</span>

  <img id="lightboxImg" alt="Product preview">

</div>

<script>

const WHATSAPP = "971567439129";

const products = [

  {cat:"Abaya", name:"Black Premium Nida Abaya", color:"Jet Black", sizes:"50, 52, 54, 56, 58, 60, 62", fit:"Standard Loose Fit",

   img:"https://images.unsplash.com/photo-1594633312681-425c7b97ccd1?auto=format&fit=crop&w=1200&q=85"},

  {cat:"Abaya", name:"Royal Navy Blue Abaya", color:"Navy Blue", sizes:"50, 52, 54, 56, 58, 60", fit:"Elegant Fit",

   img:"https://images.unsplash.com/photo-1591369822096-ffd140ec948f?auto=format&fit=crop&w=1200&q=85"},

  {cat:"Abaya", name:"Maroon Lace Work Abaya", color:"Deep Maroon", sizes:"52, 54, 56, 58, 60, 62", fit:"Relaxed Fit",

   img:"https://images.unsplash.com/photo-1583391733956-6c78276477e2?auto=format&fit=crop&w=1200&q=85"},

  {cat:"Abaya", name:"Olive Green Dubai Style", color:"Olive Green", sizes:"50, 52, 54, 56, 58", fit:"Modern Fit",

   img:"https://images.unsplash.com/photo-1551488831-00ddcb6c6bd3?auto=format&fit=crop&w=1200&q=85"},

  {cat:"Abaya", name:"Beige Champagne Abaya", color:"Soft Beige", sizes:"52, 54, 56, 58, 60, 62", fit:"Comfort Fit",

   img:"https://images.unsplash.com/photo-1551028719-00167b16eac5?auto=format&fit=crop&w=1200&q=85"},

  {cat:"Abaya", name:"Casual Charcoal Grey Abaya", color:"Charcoal Grey", sizes:"50, 52, 54, 56, 58, 60", fit:"Regular Fit",

   img:"https://images.unsplash.com/photo-1490481651871-ab68de25d43d?auto=format&fit=crop&w=1200&q=85"},

  {cat:"Burqa", name:"Classic Black Burqa", color:"Black", sizes:"Free Size / Custom", fit:"Full Coverage",

   img:"https://images.unsplash.com/photo-1539109136881-3be0616acf4b?auto=format&fit=crop&w=1200&q=85"},

  {cat:"Burqa", name:"Dubai Premium Burqa", color:"Black & Gold", sizes:"Custom Sizes", fit:"Premium Fit",

   img:"https://images.unsplash.com/photo-1483985988355-763728e1935b?auto=format&fit=crop&w=1200&q=85"},

  {cat:"Burqa", name:"Elegant Embroidered Burqa", color:"Black", sizes:"Custom Sizes", fit:"Elegant Fit",

   img:"https://images.unsplash.com/photo-1485230895905-ec40ba36b9bc?auto=format&fit=crop&w=1200&q=85"},

  {cat:"Kurta", name:"White Premium Kurta", color:"Pearl White", sizes:"S, M, L, XL, XXL", fit:"Regular Fit",

   img:"https://images.unsplash.com/photo-1622445275576-721325763afe?auto=format&fit=crop&w=1200&q=85"},

  {cat:"Kurta", name:"Black Classic Kurta", color:"Jet Black", sizes:"S, M, L, XL, XXL", fit:"Comfort Fit",

   img:"https://images.unsplash.com/photo-1596755094514-f87e34085b2c?auto=format&fit=crop&w=1200&q=85"},

  {cat:"Kurta", name:"Sand Beige Premium Kurta", color:"Sand Beige", sizes:"S, M, L, XL, XXL", fit:"Modern Fit",

   img:"https://images.unsplash.com/photo-1610652492500-ded49ceeb378?auto=format&fit=crop&w=1200&q=85"}

];

let currentCat = "All";

function shuffle(arr){

  const a=[...arr];

  for(let i=a.length-1;i>0;i--){const j=Math.floor(Math.random()*(i+1));[a[i],a[j]]=[a[j],a[i]];}

  return a;

}

function render(){

  const grid=document.getElementById("productsGrid");

  let list=products.filter(p=>currentCat==="All" || p.cat===currentCat);

  list=shuffle(list);

  grid.innerHTML=list.map((p,i)=>{

    const msg=encodeURIComponent(`Hello Dubai Abaya Fashion, I am interested in "${p.name}" (${p.color}). Please send me the price and details.`);

    return `

      <article class="card">

        <div class="photo-wrap">

          <span class="tag">${p.cat}</span>

          <img src="${p.img}" alt="${p.name}" loading="${i<2?'eager':'lazy'}"

               onerror="this.onerror=null;this.src='https://placehold.co/1200x900/222/fff?text=Dubai+Abaya+Fashion';">

        </div>

        <div class="info">

          <h3>${p.name}</h3>

          <div class="meta">

            <b>Color:</b> ${p.color}<br>

            <b>Available Sizes:</b> ${p.sizes}<br>

            <b>Fitting:</b> ${p.fit}

          </div>

          <a class="whatsapp" href="https://wa.me/${WHATSAPP}?text=${msg}" target="_blank">Inquire Price on WhatsApp</a>

        </div>

      </article>`;

  }).join("");

  document.querySelectorAll(".photo-wrap img").forEach(img=>{

    img.addEventListener("click",()=>{document.getElementById("lightboxImg").src=img.src;document.getElementById("lightbox").classList.add("show");});

  });

}

document.querySelectorAll(".filter").forEach(btn=>{

  btn.addEventListener("click",()=>{

    document.querySelectorAll(".filter").forEach(b=>b.classList.remove("active"));

    btn.classList.add("active"); currentCat=btn.dataset.cat; render();

  });

});

document.getElementById("refresh").addEventListener("click",render);

document.getElementById("close").addEventListener("click",()=>document.getElementById("lightbox").classList.remove("show"));

document.getElementById("lightbox").addEventListener("click",e=>{if(e.target.id==="lightbox")e.currentTarget.classList.remove("show")});

render();

</script>

</body>

</html>

'''

(root/"index.html").write_text(html, encoding="utf-8")

(root/"README.txt").write_text(

"""DUBAI ABAYA FASHION

====================

1. Upload index.html to your GitHub Pages repository.

2. Make sure GitHub Pages is enabled for the repository.

3. Open your GitHub Pages website.

Features:

- One product per row on mobile.

- Abaya, Burqa and Kurta categories.

- Product photos with fallback if an image fails.

- New Designs button shuffles products every refresh/click.

- WhatsApp inquiry buttons.

- No product prices displayed.

- Mobile-friendly responsive design.

- Tap a product photo to view it larger.

WhatsApp number configured:

+971 56 743 9129

NOTE:

The sample product photos are loaded from public Unsplash image URLs. For a permanent shop,

replace the image URLs in index.html with your own product photos (preferably uploaded into

an /images folder in the same GitHub repository). This avoids dependency on third-party image URLs.

""", encoding="utf-8")

zip_path = Path("/mnt/data/Dubai-Abaya-Fashion-Website.zip")

with zipfile.ZipFile(zip_path, "w", zipfile.ZIP_DEFLATED) as z:

    z.write(root/"index.html", "index.html")

    z.write(root/"README.txt", "README.txt")

print(f"Created: {zip_path}")

print("The ZIP contains index.html and README.txt. The site is mobile-friendly, one product per row on mobile, has Abaya/Burqa/Kurta filters, randomized designs on refresh, WhatsApp buttons, and image fallbacks.")
