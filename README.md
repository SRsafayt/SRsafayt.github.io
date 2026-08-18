from pathlib import Path

import shutil, zipfile

src = Path("/mnt/data/B9AB6F58-F258-4DE5-A2C0-96259021484F.jpeg")

root = Path("/mnt/data/dubai-abaya-final")

root.mkdir(exist_ok=True)

shutil.copy2(src, root / "hero-design.jpeg")

html = r'''<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Dubai Abaya Fashion</title>

<meta name="description" content="Dubai Abaya Fashion — premium abayas and burqas.">

<style>

*{box-sizing:border-box;margin:0;padding:0}

html{scroll-behavior:smooth}

body{font-family:Arial,Helvetica,sans-serif;background:#f7f1e8;color:#17130e}

a{text-decoration:none;color:inherit}

.top{height:36px;background:#080808;color:#fff;display:flex;justify-content:center;align-items:center;gap:55px;font-size:12px;border-bottom:1px solid #8d6a29}

.top span{color:#e0b85d}

.nav{height:82px;background:#050505;color:#fff;display:flex;align-items:center;padding:0 4%;gap:30px;border-bottom:1px solid #9b7630;position:sticky;top:0;z-index:10}

.logo{display:flex;align-items:center;gap:10px;min-width:290px}

.logoMark{width:54px;height:54px;border:2px solid #d9ad52;border-radius:50%;display:grid;place-items:center;color:#d9ad52;font-family:Georgia,serif;font-size:19px}

.logoText{font-family:Georgia,serif;color:#e2b85d;font-size:27px;line-height:.8;letter-spacing:2px}

.logoText small{display:block;font-family:Arial;font-size:8px;color:#ddd;letter-spacing:2px;margin-top:8px}

.links{display:flex;align-items:center;justify-content:center;gap:24px;flex:1;font-size:12px;font-weight:bold;text-transform:uppercase}

.links a{padding:31px 0;border-bottom:2px solid transparent}

.links a:hover,.links a.active{color:#e0b85d;border-bottom-color:#e0b85d}

.whatsappTop{border:1px solid #d9ad52;color:#e0b85d;padding:12px 17px;border-radius:8px;font-weight:bold;font-size:11px;white-space:nowrap}

.hero{position:relative;min-height:520px;overflow:hidden;background:#080808}

.hero img{width:100%;height:520px;object-fit:cover;display:block}

.heroOverlay{position:absolute;inset:0;background:linear-gradient(90deg,rgba(0,0,0,.72),rgba(0,0,0,.30) 48%,rgba(0,0,0,.05))}

.heroContent{position:absolute;left:8%;top:50%;transform:translateY(-50%);color:#fff;max-width:530px}

.kicker{color:#e1b65b;letter-spacing:4px;font-size:13px;font-weight:bold}

.hero h1{font-family:Georgia,serif;font-size:clamp(48px,6vw,78px);line-height:.9;margin:18px 0}

.hero h1 span{display:block}

.hero p{font-size:15px;line-height:1.7;max-width:450px;color:#eee}

.buttons{display:flex;gap:13px;margin-top:25px}

.btn{display:inline-block;padding:14px 24px;border-radius:4px;border:1px solid #d9ad52;font-size:11px;font-weight:bold;text-transform:uppercase;letter-spacing:.7px}

.btnGold{background:linear-gradient(135deg,#c99738,#ebc96f);color:#111}

.btnDark{background:#080808c9;color:#fff}

.features{display:grid;grid-template-columns:repeat(4,1fr);background:#111;color:#fff;border-bottom:1px solid #806024}

.feature{text-align:center;padding:22px 12px;border-right:1px solid #493819}

.feature:last-child{border:0}

.feature strong{display:block;color:#e2b85d;font-size:12px;text-transform:uppercase}

.feature small{display:block;color:#bbb;margin-top:5px;font-size:10px}

.section{max-width:1400px;margin:auto;padding:55px 5%}

.sectionTitle{text-align:center;margin-bottom:30px}

.eyebrow{color:#9b762d;font-size:11px;letter-spacing:3px;text-transform:uppercase;font-weight:bold}

.sectionTitle h2{font-family:Georgia,serif;font-size:43px;margin:8px 0}

.sectionTitle p{color:#777;font-size:12px}

.layout{display:grid;grid-template-columns:205px 1fr;gap:30px}

.sidebar{background:#fff;border:1px solid #ded5c8;padding:18px;height:max-content}

.sidebar h3{font-family:Georgia,serif;margin-bottom:14px}

.filter{display:block;width:100%;text-align:left;border:0;border-bottom:1px solid #e4ddd3;background:#fff;padding:14px 5px;cursor:pointer;font-size:12px}

.filter.active,.filter:hover{color:#9a742c;font-weight:bold}

.grid{display:grid;grid-template-columns:repeat(4,1fr);gap:15px}

.card{background:#fff;border:1px solid #dfd6ca;overflow:hidden;transition:.2s}

.card:hover{transform:translateY(-5px);box-shadow:0 15px 35px #0002}

.productImage{height:270px;background:linear-gradient(145deg,#e9dece,#bba891);display:flex;align-items:flex-end;justify-content:center;position:relative}

.dress{height:87%;width:61%;border-radius:45% 45% 6% 6%;background:linear-gradient(90deg,#050505,#2c251c,#050505)}

.card:nth-child(2) .dress{background:linear-gradient(90deg,#07152c,#29446d,#071329)}

.card:nth-child(3) .dress{background:linear-gradient(90deg,#321a0e,#704022,#291308)}

.card:nth-child(4) .dress{background:linear-gradient(90deg,#08261d,#20583e,#061b14)}

.card:nth-child(5) .dress{background:linear-gradient(90deg,#37101c,#76283c,#2a0b14)}

.card:nth-child(6) .dress{background:linear-gradient(90deg,#30343a,#747b83,#292d32)}

.heart{position:absolute;right:10px;top:10px;width:31px;height:31px;border-radius:50%;background:white;display:grid;place-items:center}

.cardBody{text-align:center;padding:14px}

.tag{font-size:8px;color:#9b762d;letter-spacing:1.5px;text-transform:uppercase}

.card h3{font-family:Georgia,serif;font-size:20px;margin:6px 0}

.card p{font-size:9px;color:#888}

.ask{margin-top:12px;width:100%;border:0;background:#080808;color:#e2b85d;padding:11px;cursor:pointer;font-weight:bold;font-size:9px;text-transform:uppercase}

.order{margin:0 5% 55px;background:#080808;color:#fff;border:1px solid #a47c2d;padding:24px 4%;display:flex;align-items:center;justify-content:space-between;gap:20px}

.order h3{font-family:Georgia,serif;font-size:27px;margin-bottom:5px}

.order p{font-size:10px;color:#aaa}

.phone{font-size:25px;color:#e2b85d;font-weight:bold;white-space:nowrap}

.footer{background:#080808;color:#aaa;padding:45px 5% 15px;border-top:1px solid #9b762d}

.footerGrid{max-width:1400px;margin:auto;display:grid;grid-template-columns:2fr 1fr 1fr 1.3fr;gap:35px}

.footer h3{font-family:Georgia,serif;color:#e2b85d;font-size:23px;margin-bottom:10px}

.footer a,.footer p{font-size:10px;line-height:2;display:block;color:#999}

.copy{text-align:center;border-top:1px solid #282828;margin-top:28px;padding-top:14px;font-size:8px;color:#666}

.float{position:fixed;right:20px;bottom:20px;width:58px;height:58px;border-radius:50%;background:#25d366;color:white;display:grid;place-items:center;font-size:25px;z-index:20;box-shadow:0 5px 20px #0005}

@media(max-width:1050px){.links{display:none}.grid{grid-template-columns:repeat(2,1fr)}.layout{grid-template-columns:160px 1fr}}

@media(max-width:700px){.top{gap:10px;font-size:8px}.nav{height:70px}.logo{min-width:0}.logoText{font-size:20px}.logoMark{width:43px;height:43px}.whatsappTop{display:none}.hero img{height:500px;object-position:center}.heroContent{left:6%;right:6%}.hero h1{font-size:52px}.features{grid-template-columns:repeat(2,1fr)}.feature{border-bottom:1px solid #493819}.layout{grid-template-columns:1fr}.sidebar{display:flex;overflow:auto;gap:5px}.filter{min-width:120px;border:1px solid #ddd}.grid{gap:9px}.productImage{height:220px}.order{margin:0 4% 40px;flex-direction:column;align-items:flex-start}.phone{font-size:21px}.footerGrid{grid-template-columns:1fr 1fr}}

@media(max-width:450px){.hero{min-height:480px}.hero img{height:480px}.heroContent{top:48%}.hero p{font-size:12px}.buttons{flex-direction:column}.btn{text-align:center}.grid{grid-template-columns:1fr 1fr}.card h3{font-size:17px}.productImage{height:200px}.footerGrid{grid-template-columns:1fr}}

</style>

</head>

<body>

<div class="top"><span>🚚 FREE SHIPPING ACROSS UAE</span><span>◇ PREMIUM QUALITY</span><span>♜ SECURE PAYMENT</span><span>♧ CUSTOMER SUPPORT</span></div>

<nav class="nav">

<a class="logo" href="#home"><span class="logoMark">DA</span><span class="logoText">DUBAI<br>ABAYA FASHION<small>MODESTY · ELEGANCE · LUXURY</small></span></a>

<div class="links"><a class="active" href="#home">Home</a><a href="#collection">Abayas</a><a href="#collection">Burqas</a><a href="#collection">New Arrivals</a><a href="#collection">Best Sellers</a><a href="#about">About Us</a><a href="#contact">Contact Us</a></div>

<a class="whatsappTop" target="_blank" href="https://wa.me/971567439129">◉ WHATSAPP US</a>

</nav>

<header class="hero" id="home">

<img src="hero-design.jpeg" alt="Dubai Abaya Fashion luxury collection">

<div class="heroOverlay"></div>

<div class="heroContent">

<div class="kicker">Welcome to</div>

<h1>Dubai Abaya<br><span>Fashion</span></h1>

<p>Premium abayas & burqas crafted for elegance, comfort and timeless modest fashion.</p>

<div class="buttons"><a class="btn btnGold" href="#collection">Explore Collection →</a><a class="btn btnDark" href="#collection">View New Arrivals</a></div>

</div>

</header>

<section class="features">

<div class="feature"><strong>♕ Premium Quality</strong><small>Finest Fabrics & Stitching</small></div>

<div class="feature"><strong>◎ Worldwide Shipping</strong><small>Fast & Reliable Delivery</small></div>

<div class="feature"><strong>◇ Secure Service</strong><small>Safe & Trusted Shopping</small></div>

<div class="feature"><strong>♧ 24/7 Customer Support</strong><small>We Are Always Here To Help</small></div>

</section>

<section class="section" id="collection">

<div class="sectionTitle"><div class="eyebrow">Our Exclusive Collection</div><h2>Premium Abayas & Burqas</h2><p>Discover elegant modest fashion designs.</p></div>

<div class="layout">

<aside class="sidebar"><h3>Shop by Category</h3><button class="filter active" onclick="filterProducts('all',this)">▦ All Collections</button><button class="filter" onclick="filterProducts('Abaya',this)">♧ Abayas</button><button class="filter" onclick="filterProducts('Burqa',this)">♧ Burqas</button><button class="filter" onclick="filterProducts('New',this)">☆ New Arrivals</button><button class="filter" onclick="filterProducts('Best',this)">♕ Best Sellers</button></aside>

<div class="grid" id="products"></div>

</div>

</section>

<section class="order" id="contact">

<div><div class="eyebrow">Have a Question or Want to Place an Order?</div><h3>Chat With Us on WhatsApp</h3><p>Ask about size, color, availability and delivery details.</p></div>

<div class="phone">+971 56 743 9129</div>

<a class="btn btnGold" target="_blank" href="https://wa.me/971567439129">◉ Chat on WhatsApp</a>

</section>

<footer class="footer" id="about">

<div class="footerGrid">

<div><h3>Dubai Abaya Fashion</h3><p>Modesty is the new luxury. Premium abayas & burqas designed for every beautiful moment.</p></div>

<div><h3>Quick Links</h3><a href="#home">Home</a><a href="#collection">Abayas</a><a href="#collection">Burqas</a><a href="#collection">New Arrivals</a><a href="#collection">Best Sellers</a></div>

<div><h3>Customer Service</h3><a href="#about">About Us</a><a href="#contact">Contact Us</a><a href="#contact">Shipping & Delivery</a><a href="#contact">Privacy Policy</a><a href="#contact">Terms & Conditions</a></div>

<div><h3>Contact Us</h3><p>WhatsApp: +971 56 743 9129</p><p>Dubai, United Arab Emirates</p><p>info@dubaiabayafashion.com</p></div>

</div>

<div class="copy">© 2026 Dubai Abaya Fashion. All Rights Reserved.</div>

</footer>

<a class="float" target="_blank" href="https://wa.me/971567439129">◉</a>

<script>

const products=[

["Black Royal Abaya","Abaya","New Collection","black"],

["Navy Blue Abaya","Abaya","New Collection","blue"],

["Mocha Brown Abaya","Abaya","New Collection","brown"],

["Emerald Green Abaya","Abaya","New Collection","green"],

["Burgundy Designer Abaya","New","New Arrival","burgundy"],

["Silver Grey Abaya","Abaya","New Collection","grey"],

["Beige Abaya","Best","Best Seller","beige"],

["Designer Black Abaya","Burqa","New Collection","black"]

];

function render(list=products){

document.getElementById("products").innerHTML=list.map(p=>`

<article class="card"><div class="productImage ${p[3]}"><div class="dress"></div><div class="heart">♡</div></div>

<div class="cardBody"><div class="tag">${p[2]}</div><h3>${p[0]}</h3><p>No price shown • Contact for details</p>

<button class="ask" onclick="ask('${p[0]}')">Ask on WhatsApp →</button></div></article>`).join("");

}

function filterProducts(type,btn){

document.querySelectorAll(".filter").forEach(x=>x.classList.remove("active"));btn.classList.add("active");

render(type==="all"?products:products.filter(p=>p[1]===type));

}

function ask(name){

location.href="https://wa.me/971567439129?text="+encodeURIComponent("Hello Dubai Abaya Fashion, I am interested in "+name+". Please share the available details.");

}

render();

</script>

</body>

</html>'''

(root/"index.html").write_text(html,encoding="utf-8")

(root/"README.txt").write_text(

"""DUBAI ABAYA FASHION — FINAL HTML

=================================

Files:

- index.html

- hero-design.jpeg

IMPORTANT:

Keep hero-design.jpeg in the same folder as index.html.

The HTML uses the uploaded design image as the main hero section.

WhatsApp:

+971 56 743 9129

Prices are intentionally hidden.

To run:

1. Put both files in the same folder.

2. Open index.html in a browser.

3. For a public website, upload the folder to Netlify, GitHub Pages, or another static hosting service.

""",encoding="utf-8")

zip_path=Path("/mnt/data/Dubai-Abaya-Fashion-FINAL-HTML.zip")

with zipfile.ZipFile(zip_path,"w",zipfile.ZIP_DEFLATED) as z:

    for p in root.iterdir(): z.write(p,p.name)

print(zip_path)

<img width="720" height="867" alt="image" src="https://github.com/user-attachments/assets/e4043d0e-8fdd-4756-aa03-a2ac0d292d5e" />
<img width="736" height="942" alt="image" src="https://github.com/user-attachments/assets/2bdbdf56-e7db-459d-8c65-22c057d367ef" />

</body>
</html>

<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">

<title>Dubai Abaya Fashion | Premium Abaya & Burqa Collection</title>

<style>
*{box-sizing:border-box}

html{scroll-behavior:smooth}

body{
  margin:0;
  background:#f6f3ee;
  color:#171717;
  font-family:Arial,Helvetica,sans-serif;
}

header{
  position:sticky;
  top:0;
  z-index:100;
  background:#101722;
  color:#fff;
  box-shadow:0 3px 18px #0002;
}

.nav{
  max-width:1100px;
  margin:auto;
  padding:15px 18px;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:15px;
}

.logo{
  color:#e9b95b;
  font-weight:900;
  font-size:17px;
  letter-spacing:.5px;
}

.nav a{
  color:#fff;
  text-decoration:none;
  margin-left:18px;
  font-size:14px;
  font-weight:700;
}

.hero{
  max-width:1100px;
  margin:auto;
  padding:25px 15px;
}

.heroBox{
  min-height:390px;
  border-radius:26px;
  padding:60px 22px;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  text-align:center;
  color:#fff;
  background:
    radial-gradient(circle at 20% 20%,#ffffff18,transparent 30%),
    linear-gradient(135deg,#101722,#3c4149);
  box-shadow:0 15px 45px #0002;
}

.heroSmall{
  color:#e9b95b;
  font-weight:900;
  letter-spacing:2px;
  font-size:13px;
}

.hero h1{
  font-family:Georgia,serif;
  font-size:45px;
  margin:15px 0 12px;
  max-width:750px;
}

.hero p{
  color:#ddd;
  max-width:650px;
  line-height:1.7;
  margin:0 0 25px;
}

.wa{
  display:inline-block;
  background:#20c968;
  color:#fff;
  text-decoration:none;
  padding:14px 24px;
  border-radius:10px;
  font-weight:900;
  box-shadow:0 8px 20px #0003;
}

.wrap{
  max-width:1100px;
  margin:auto;
  padding:0 15px 65px;
}

.search{
  width:100%;
  padding:15px 18px;
  border:1px solid #ddd;
  border-radius:12px;
  background:#fff;
  font-size:15px;
  outline:none;
  margin-bottom:14px;
}

.search:focus{
  border-color:#c79b4b;
}

.filters{
  display:flex;
  gap:8px;
  overflow-x:auto;
  padding:5px 0 22px;
}

.filter{
  white-space:nowrap;
  border:1px solid #d7d2ca;
  background:#fff;
  color:#222;
  border-radius:50px;
  padding:10px 16px;
  font-weight:800;
  cursor:pointer;
}

.filter.active{
  background:#101722;
  color:#fff;
  border-color:#101722;
}

.title{
  display:flex;
  justify-content:space-between;
  align-items:center;
  margin-bottom:18px;
}

.title h2{
  font-family:Georgia,serif;
  font-size:28px;
  margin:0;
}

.grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:22px;
}

.card{
  background:#fff;
  border-radius:18px;
  overflow:hidden;
  box-shadow:0 7px 28px #00000012;
  transition:.25s ease;
}

.card:hover{
  transform:translateY(-4px);
  box-shadow:0 12px 35px #0002;
}

.pic{
  position:relative;
  aspect-ratio:4/3;
  background:#eee;
  overflow:hidden;
  cursor:zoom-in;
}

.pic img{
  width:100%;
  height:100%;
  object-fit:cover;
  display:block;
  transition:.35s ease;
}

.card:hover .pic img{
  transform:scale(1.035);
}

.tag{
  position:absolute;
  top:12px;
  left:12px;
  z-index:2;
  background:#101722;
  color:#fff;
  padding:7px 11px;
  border-radius:30px;
  font-size:11px;
  font-weight:900;
}

.zoom{
  position:absolute;
  right:12px;
  bottom:12px;
  background:#fff;
  color:#111;
  width:40px;
  height:40px;
  border-radius:50%;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:19px;
  box-shadow:0 4px 15px #0003;
}

.info{
  padding:18px;
}

.info h3{
  margin:0 0 10px;
  font-family:Georgia,serif;
  font-size:20px;
}

.meta{
  color:#666;
  font-size:13px;
  line-height:1.8;
  margin-bottom:15px;
}

.meta b{
  color:#222;
}

.wa2{
  display:block;
  text-align:center;
  background:#20c968;
  color:#fff;
  text-decoration:none;
  padding:12px;
  border-radius:10px;
  font-weight:900;
}

.about{
  margin-top:60px;
  padding:35px 25px;
  border-radius:20px;
  background:#101722;
  color:#fff;
  text-align:center;
}

.about h2{
  color:#e9b95b;
  font-family:Georgia,serif;
  margin-top:0;
}

.about p{
  max-width:750px;
  margin:auto;
  color:#ddd;
  line-height:1.8;
}

footer{
  background:#101722;
  color:#bbb;
  text-align:center;
  padding:30px 15px;
  line-height:1.8;
}

footer b{
  color:#e9b95b;
}

/* LIGHTBOX */

.lightbox{
  position:fixed;
  inset:0;
  z-index:9999;
  background:#000e;
  display:none;
  align-items:center;
  justify-content:center;
  padding:25px;
}

.lightbox.show{
  display:flex;
}

.lightbox img{
  max-width:92vw;
  max-height:86vh;
  object-fit:contain;
  border-radius:12px;
  box-shadow:0 15px 60px #000;
}

.close{
  position:absolute;
  top:18px;
  right:22px;
  width:48px;
  height:48px;
  border:0;
  border-radius:50%;
  background:#fff;
  color:#111;
  font-size:30px;
  cursor:pointer;
}

.prev,
.next{
  position:absolute;
  top:50%;
  transform:translateY(-50%);
  width:48px;
  height:48px;
  border:0;
  border-radius:50%;
  background:#fff;
  color:#111;
  font-size:28px;
  cursor:pointer;
}

.prev{left:18px}
.next{right:18px}

@media(max-width:699px){

  .nav{
    padding:13px 12px;
  }

  .logo{
    font-size:13px;
  }

  .nav a{
    margin-left:8px;
    font-size:12px;
  }

  .hero{
    padding:14px 10px;
  }

  .heroBox{
    min-height:340px;
    padding:45px 18px;
    border-radius:20px;
  }

  .hero h1{
    font-size:34px;
  }

  .grid{
    grid-template-columns:1fr;
    gap:18px;
  }

  .title h2{
    font-size:24px;
  }

  .lightbox{
    padding:12px;
  }

  .prev,
  .next{
    width:42px;
    height:42px;
    font-size:22px;
  }

  .prev{left:8px}
  .next{right:8px}
}
</style>
</head>

<body>

<header>
  <div class="nav">
    <div class="logo">DUBAI ABAYA FASHION</div>

    <div>
      <a href="#collection">Collection</a>
      <a href="#about">About</a>
      <a href="#contact">WhatsApp</a>
    </div>
  </div>
</header>


<section class="hero">

  <div class="heroBox">

    <div class="heroSmall">PREMIUM ISLAMIC WEAR</div>

    <h1>Elegant Abaya & Burqa Collection</h1>

    <p>
      Discover elegant Dubai-inspired abayas, burqas,
      embroidered abayas, niqabs and shaylas.
      Custom sizes available.
    </p>

    <a
      class="wa"
      href="https://wa.me/971567439129?text=Hello%20Dubai%20Abaya%20Fashion%2C%20I%20want%20to%20ask%20about%20your%20collection."
      target="_blank"
    >
      WhatsApp Inquiry
    </a>

  </div>

</section>


<main class="wrap" id="collection">

  <input
    class="search"
    id="search"
    type="search"
    placeholder="Search abaya, burqa, embroidered..."
  >

  <div class="filters">

    <button class="filter active" data-cat="All">All</button>

    <button class="filter" data-cat="Abaya">Abaya</button>

    <button class="filter" data-cat="Burqa">Burqa</button>

    <button class="filter" data-cat="Embroidered">
      Embroidered Abaya
    </button>

    <button class="filter" data-cat="Niqab">Niqab</button>

    <button class="filter" data-cat="Shayla">Shayla</button>

  </div>


  <div class="title">
    <h2>Our Designs</h2>
  </div>


  <div class="grid" id="grid"></div>


  <section class="about" id="about">

    <h2>About Dubai Abaya Fashion</h2>

    <p>
      Dubai Abaya Fashion brings elegant Dubai-inspired Islamic wear
      with a focus on beautiful designs, quality finishing and
      comfortable custom sizing. Explore our abayas, burqas,
      embroidered abayas, niqabs and shaylas and contact us directly
      on WhatsApp for details and orders.
    </p>

  </section>

</main>


<footer id="contact">

  <b>Dubai Abaya Fashion</b><br>

  Custom Orders Available<br>
<img width="739" height="1600" alt="image" src="https://github.com/user-attachments/assets/8398b48f-7811-472b-b204-29b6d62f4bc6" />

  WhatsApp: +971 56 743 9129

</footer>


<!-- LIGHTBOX -->

<div class="lightbox" id="lightbox">

  <button class="close" id="close">×</button>

  <button class="prev" id="prev">‹</button>

  <img id="lightboxImg" src="" alt="Abaya Design">

  <button class="next" id="next">›</button>

</div>


<script>

const number = "971567439129";

const products = [

  {
    cat:"Abaya",
    name:"Original Abaya Design 01",
    color:"Black",
    size:"Custom size",
    img:"images/design-1.jpeg"
  },

  {
    cat:"Embroidered",
    name:"Embroidered Abaya Design 02",
    color:"Black / Embroidery",
    size:"Custom size",
    img:"images/design-2.jpeg"
  },

  {
    cat:"Abaya",
    name:"Elegant Abaya Design 03",
    color:"Light Tone",
    size:"Custom size",
    img:"images/design-3.jpeg"
  },

  {
    cat:"Embroidered",
    name:"Embroidered Abaya Design 04",
    color:"Blue / Embroidery",
    size:"Custom size",
    img:"images/design-4.jpeg"
  },

  {
    cat:"Abaya",
    name:"Elegant Abaya Design 05",
    color:"Custom Colour",
    size:"Custom size",
    img:"images/design-5.jpeg"
  },

  {
    cat:"Burqa",
    name:"Burqa Design 06",
    color:"Black",
    size:"Custom size",
    img:"images/design-6.jpeg"
  },

  {
    cat:"Abaya",
    name:"Abaya Design 07",
    color:"Custom Colour",
    size:"Custom size",
    img:"images/design-7.jpeg"
  },

  {
    cat:"Embroidered",
    name:"Embroidered Design 08",
    color:"Custom Colour",
    size:"Custom size",
    img:"images/design-8.jpeg"
  }

];


let current = "All";
let searchText = "";
let lightIndex = 0;


/* PRODUCTS */

function getProducts(){

  return products.filter(p => {

    const categoryMatch =
      current === "All" || p.cat === current;

    const text =
      (p.name + " " + p.cat + " " + p.color).toLowerCase();

    const searchMatch =
      text.includes(searchText.toLowerCase());

    return categoryMatch && searchMatch;

  });

}


function render(){

  const list = getProducts();

  const grid = document.getElementById("grid");

  if(!list.length){

    grid.innerHTML = `
      <div style="
        grid-column:1/-1;
        background:#fff;
        padding:35px;
        text-align:center;
        border-radius:15px;
      ">
        No design found.
      </div>
    `;

    return;
  }


  grid.innerHTML = list.map((p) => {

    const realIndex = products.indexOf(p);

    const msg = encodeURIComponent(
      "Hello Dubai Abaya Fashion, I am interested in " +
      p.name +
      ". Please send me details and price."
    );

    return `

      <article class="card">

        <div
          class="pic"
          onclick="openLightbox(${realIndex})"
        >

          <span class="tag">${p.cat}</span>

          <img
            src="${p.img}"
            alt="${p.name}"
            loading="lazy"
          >

          <span class="zoom">⌕</span>

        </div>


        <div class="info">

          <h3>${p.name}</h3>

          <div class="meta">

            <b>Colour:</b> ${p.color}<br>

            <b>Size:</b> ${p.size}<br>

            <b>Price:</b> Contact on WhatsApp

          </div>


          <a
            class="wa2"
            href="https://wa.me/${number}?text=${msg}"
            target="_blank"
          >
            Ask Price on WhatsApp
          </a>

        </div>

      </article>

    `;

  }).join("");

}


/* CATEGORY */

document.querySelectorAll(".filter").forEach(button => {

  button.addEventListener("click", () => {

    document
      .querySelectorAll(".filter")
      .forEach(x => x.classList.remove("active"));

    button.classList.add("active");

    current = button.dataset.cat;

    render();

  });

});


/* SEARCH */

document
  .getElementById("search")
  .addEventListener("input", e => {

    searchText = e.target.value;

    render();

  });


/* LIGHTBOX */

const lightbox =
  document.getElementById("lightbox");

const lightboxImg =
  document.getElementById("lightboxImg");


function openLightbox(index){

  lightIndex = index;

  lightboxImg.src = products[index].img;

  lightboxImg.alt = products[index].name;

  lightbox.classList.add("show");

  document.body.style.overflow = "hidden";

}


function closeLightbox(){

  lightbox.classList.remove("show");

  document.body.style.overflow = "";

}


function nextImage(){

  lightIndex =
    (lightIndex + 1) % products.length;

  lightboxImg.src =
    products[lightIndex].img;

  lightboxImg.alt =
    products[lightIndex].name;

}


function prevImage(){

  lightIndex =
    (lightIndex - 1 + products.length)
    % products.length;

  lightboxImg.src =
    products[lightIndex].img;

  lightboxImg.alt =
    products[lightIndex].name;

}


document
  .getElementById("close")
  .onclick = closeLightbox;

document
  .getElementById("next")
  .onclick = nextImage;

document
  .getElementById("prev")
  .onclick = prevImage;


lightbox.addEventListener("click", e => {

  if(e.target === lightbox){

    closeLightbox();

  }

});


document.addEventListener("keydown", e => {

  if(!lightbox.classList.contains("show")) return;

  if(e.key === "Escape") closeLightbox();

  if(e.key === "ArrowRight") nextImage();

  if(e.key === "ArrowLeft") prevImage();

});


/* START */

render();

</script>

</body>
</html>
