from pathlib import Path

import zipfile, shutil

srcs = [

"/mnt/data/52F84C82-60D4-4AE4-822A-3F312DDED140.jpeg",

"/mnt/data/789EBFE4-25EE-4929-AFE3-B8ECEA976606.jpeg",

"/mnt/data/CA18EA4B-7AD4-4320-ABDA-B77D3963133D.jpeg",

"/mnt/data/9348536C-BD28-44C2-AE9D-BAD2F54985E3.jpeg",

"/mnt/data/8BC5E8E5-38AB-451E-8D3D-A1A57D99F249.jpeg",

"/mnt/data/ABDFFE8E-B142-4EAC-AE17-9FB1C02231FC.jpeg",

"/mnt/data/43A8F148-C5DD-41E1-A4B5-C82B3B55BFC9.jpeg",

"/mnt/data/0E62C523-DBD1-4FD5-B915-F708BE49CFD5.jpeg",

]

root=Path("/mnt/data/Dubai-Abaya-Fashion-8-Photos")

imgdir=root/"images"

imgdir.mkdir(parents=True,exist_ok=True)

for i,s in enumerate(srcs,1):

    shutil.copy2(s,imgdir/f"design-{i}.jpeg")

html='''<!doctype html><html lang="en"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1"><title>Dubai Abaya Fashion</title><style>

*{box-sizing:border-box}body{margin:0;background:#f7f5f1;color:#151515;font-family:Arial,sans-serif}header{background:#111827;color:#fff;padding:16px;position:sticky;top:0;z-index:5}.nav{max-width:900px;margin:auto;display:flex;justify-content:space-between;align-items:center}.logo{font-weight:900;color:#f2b94b}.nav a{color:#fff;text-decoration:none;margin-left:14px;font-size:14px}.hero{max-width:900px;margin:auto;padding:22px 14px}.heroBox{padding:42px 20px;border-radius:22px;text-align:center;background:linear-gradient(135deg,#111827,#3b3f45);color:#fff}.hero h1{font-size:34px;margin:12px 0}.hero p{color:#ddd}.wa{display:inline-block;background:#20c968;color:#fff;text-decoration:none;padding:12px 20px;border-radius:9px;font-weight:800}.wrap{max-width:900px;margin:auto;padding:0 14px 50px}.filters{display:flex;gap:8px;overflow:auto;padding:8px 0 18px}.filter{white-space:nowrap;border:1px solid #ccc;background:#fff;border-radius:99px;padding:10px 15px;font-weight:700}.filter.active{background:#111827;color:#fff}.title{display:flex;justify-content:space-between;align-items:center}.title h2{font-size:24px}.refresh{border:1px solid #ccc;background:#fff;border-radius:9px;padding:10px;font-weight:700}.grid{display:grid;grid-template-columns:1fr;gap:18px}.card{background:#fff;border-radius:15px;overflow:hidden;box-shadow:0 5px 20px #0001}.pic{position:relative;aspect-ratio:4/3;background:#eee}.pic img{width:100%;height:100%;object-fit:cover;display:block}.tag{position:absolute;top:10px;left:10px;background:#111827;color:#fff;padding:6px 9px;border-radius:20px;font-size:11px;font-weight:800}.info{padding:15px}.info h3{margin:0 0 8px}.meta{font-size:13px;color:#555;line-height:1.7;margin-bottom:13px}.wa2{display:block;text-align:center;background:#20c968;color:#fff;text-decoration:none;padding:12px;border-radius:9px;font-weight:800}footer{background:#111827;color:#ddd;text-align:center;padding:25px 15px}footer b{color:#f2b94b}@media(min-width:700px){.grid{grid-template-columns:repeat(2,1fr)}.hero h1{font-size:44px}}</style></head><body>

<header><div class="nav"><div class="logo">DUBAI ABAYA FASHION</div><div><a href="#collection">Collection</a><a href="#contact">WhatsApp</a></div></div></header>

<section class="hero"><div class="heroBox"><div>PREMIUM ISLAMIC WEAR</div><h1>Burqa & Abaya Collection</h1><p>Original designs • Embroidery • Custom sizes • No prices shown</p><a class="wa" href="https://wa.me/971567439129?text=Hello%20Dubai%20Abaya%20Fashion%2C%20I%20want%20to%20ask%20about%20a%20design." target="_blank">WhatsApp Inquiry</a></div></section>

<main class="wrap" id="collection"><div class="filters"><button class="filter active" data-cat="All">All</button><button class="filter" data-cat="Abaya">Abaya</button><button class="filter" data-cat="Burqa">Burqa</button><button class="filter" data-cat="Embroidered">Embroidered Abaya</button><button class="filter" data-cat="Niqab">Niqab</button><button class="filter" data-cat="Shayla">Shayla</button></div><div class="title"><h2>Our Designs</h2><button class="refresh" onclick="render()">↻ New Design</button></div><div class="grid" id="grid"></div></main>

<footer id="contact"><b>Dubai Abaya Fashion</b><br>Custom orders available<br>WhatsApp: +971 56 743 9129</footer>

<script>

const number="971567439129";const products=[

{cat:"Abaya",name:"Original Abaya Design 01",color:"Black",size:"Custom size",img:"images/design-1.jpeg"},

{cat:"Embroidered",name:"Embroidered Abaya Design 02",color:"Black / Embroidery",size:"Custom size",img:"images/design-2.jpeg"},

{cat:"Abaya",name:"Elegant Abaya Design 03",color:"Light Tone",size:"Custom size",img:"images/design-3.jpeg"},

{cat:"Embroidered",name:"Embroidered Abaya Design 04",color:"Blue / Embroidery",size:"Custom size",img:"images/design-4.jpeg"},

{cat:"Abaya",name:"Elegant Abaya Design 05",color:"Custom colour",size:"Custom size",img:"images/design-5.jpeg"},

{cat:"Burqa",name:"Burqa Design 06",color:"Black",size:"Custom size",img:"images/design-6.jpeg"},

{cat:"Abaya",name:"Abaya Design 07",color:"Custom colour",size:"Custom size",img:"images/design-7.jpeg"},

{cat:"Embroidered",name:"Embroidered Design 08",color:"Custom colour",size:"Custom size",img:"images/design-8.jpeg"}];

let current="All";function shuffle(a){a=[...a];for(let i=a.length-1;i;i--){let j=Math.floor(Math.random()*(i+1));[a[i],a[j]]=[a[j],a[i]]}return a}

function render(){let list=shuffle(products.filter(p=>current==="All"||p.cat===current));document.getElementById("grid").innerHTML=list.map(p=>{let msg=encodeURIComponent("Hello Dubai Abaya Fashion, I am interested in "+p.name+". Please send me details and price.");return '<article class="card"><div class="pic"><span class="tag">'+p.cat+'</span><img src="'+p.img+'" alt="'+p.name+'"></div><div class="info"><h3>'+p.name+'</h3><div class="meta"><b>Colour:</b> '+p.color+'<br><b>Size:</b> '+p.size+'<br><b>Price:</b> Contact on WhatsApp</div><a class="wa2" href="https://wa.me/'+number+'?text='+msg+'" target="_blank">Ask Price on WhatsApp</a></div></article>'}).join("")}

document.querySelectorAll(".filter").forEach(b=>b.onclick=()=>{document.querySelectorAll(".filter").forEach(x=>x.classList.remove("active"));b.classList.add("active");current=b.dataset.cat;render()});render();

</script></body></html>'''

(root/"index.html").write_text(html,encoding="utf-8")

(root/"README.txt").write_text("Open index.html. The eight uploaded photos are in the images folder. Upload the whole folder to hosting/GitHub Pages. Only Abaya, Burqa, Embroidered Abaya, Niqab and Shayla categories are included. No fixed prices. WhatsApp: +971 56 743 9129.",encoding="utf-8")

zip_path=Path("/mnt/data/Dubai-Abaya-Fashion-8-Photos.zip")

with zipfile.ZipFile(zip_path,"w",zipfile.ZIP_DEFLATED) as z:

    for p in root.rglob("*"):

        if p.is_file(): z.write(p,p.relative_to(root))

print(zip_path)
