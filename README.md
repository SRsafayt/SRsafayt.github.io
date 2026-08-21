
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dubai Abaya Fashion</title>
  <style>
    :root {
      --primary: #0a0a0a;
      --accent: #d4af37;
      --bg: #f9f8f6;
      --card-bg: #ffffff;
      --text: #222222;
      --text-muted: #666666;
      --border: #e8e8e8;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background-color: var(--bg);
      color: var(--text);
    }

    /* Top Bar */
    .top-bar {
      background: var(--primary);
      color: #ccc;
      font-size: 0.8rem;
      padding: 0.5rem 1rem;
      text-align: center;
      letter-spacing: 0.5px;
    }

    /* Header & Navigation */
    header {
      background-color: #111111;
      color: #ffffff;
      padding: 1.2rem 1.5rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }

    .logo {
      font-size: 1.4rem;
      font-weight: bold;
      color: var(--accent);
      letter-spacing: 1px;
    }

    .nav-links {
      display: flex;
      gap: 1.2rem;
      list-style: none;
    }

    .nav-links a {
      color: #fff;
      text-decoration: none;
      font-size: 0.85rem;
      text-transform: uppercase;
    }

    /* Hero Title */
    .hero-title {
      text-align: center;
      padding: 2.5rem 1rem 1rem;
    }

    .hero-title h1 {
      font-size: 2rem;
      color: var(--primary);
      margin-bottom: 0.5rem;
    }

    .hero-title p {
      color: var(--text-muted);
      font-size: 0.95rem;
    }

    /* Container & Grid */
    .container {
      max-width: 1200px;
      margin: 1.5rem auto 3rem;
      padding: 0 1rem;
    }

    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 1.8rem;
    }

    /* Product Card */
    .product-card {
      background: var(--card-bg);
      border-radius: 12px;
      overflow: hidden;
      border: 1px solid var(--border);
      box-shadow: 0 4px 15px rgba(0,0,0,0.03);
      display: flex;
      flex-direction: column;
      position: relative;
    }

    .product-image-container {
      position: relative;
      width: 100%;
      height: 380px;
      background-color: #f2f2f2;
      overflow: hidden;
    }

    .product-image {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .like-btn {
      position: absolute;
      top: 12px;
      right: 12px;
      background: rgba(255, 255, 255, 0.85);
      border: none;
      border-radius: 50%;
      width: 36px;
      height: 36px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.1rem;
      color: #888;
      transition: all 0.2s;
    }

    .like-btn.active {
      color: #e74c3c;
      background: #ffffff;
    }

    .product-info {
      padding: 1.2rem;
      display: flex;
      flex-direction: column;
      flex-grow: 1;
      text-align: center;
    }

    .product-title {
      font-size: 1.1rem;
      font-weight: 600;
      margin-bottom: 0.4rem;
    }

    .price-hidden-tag {
      font-size: 0.85rem;
      color: var(--text-muted);
      margin-bottom: 1rem;
    }

    .size-option {
      margin-bottom: 1rem;
      text-align: left;
    }

    .size-option label {
      font-size: 0.8rem;
      color: var(--text-muted);
      display: block;
      margin-bottom: 0.3rem;
    }

    .size-select {
      width: 100%;
      padding: 0.5rem;
      border: 1px solid var(--border);
      border-radius: 6px;
      outline: none;
      background-color: #fff;
    }

    /* Buttons */
    .btn-group {
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
      margin-top: auto;
    }

    .btn-whatsapp {
      background-color: #000000;
      color: #ffffff;
      text-decoration: none;
      padding: 0.75rem;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.9rem;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
    }

    .btn-contact {
      background-color: #f2f2f2;
      color: var(--text);
      text-decoration: none;
      padding: 0.6rem;
      border-radius: 6px;
      font-size: 0.85rem;
      font-weight: 500;
      border: 1px solid var(--border);
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.4rem;
    }

    /* Sticky Bottom Banner */
    .bottom-banner {
      background: #0d0d0d;
      color: #fff;
      padding: 1.2rem 1rem;
      text-align: center;
      margin-top: 3rem;
      border-top: 2px solid var(--accent);
    }

    .bottom-banner h3 {
      font-size: 1.1rem;
      margin-bottom: 0.5rem;
      font-weight: 500;
    }

    .banner-wa-btn {
      display: inline-flex;
      align-items: center;
      gap: 0.6rem;
      background: #d4af37;
      color: #000;
      padding: 0.7rem 1.5rem;
      border-radius: 30px;
      text-decoration: none;
      font-weight: bold;
      font-size: 1.1rem;
      margin-top: 0.5rem;
    }

    @media (max-width: 600px) {
      .nav-links { display: none; }
      .hero-title h1 { font-size: 1.5rem; }
    }
  </style>
</head>
<body>

  <div class="top-bar">
    FREE SHIPPING ACROSS UAE | PREMIUM QUALITY | SECURE PACKAGING
  </div>

  <header>
    <div class="logo">DUBAI ABAYA FASHION</div>
    <ul class="nav-links">
      <li><a href="#">Home</a></li>
      <li><a href="#">Abayas</a></li>
      <li><a href="#">Burqas</a></li>
      <li><a href="#">Contact Us</a></li>
    </ul>
  </header>

  <div class="hero-title">
    <h1>Dubai Abaya Fashion Collection</h1>
    <p>Contact us directly via WhatsApp for pricing and product details</p>
  </div>

  <div class="container">
    <img width="533" height="711" alt="image" src="https://github.com/user-attachments/assets/539d7427-4a17-4534-a0cc-e950328e7731" />

    <div class="product-grid">

      <!-- Item 1 -->
      <div class="product-card">
        <div class="product-image-container">
          <img src="assets/image1.png" alt="Premium Black Abaya" class="product-image" onerror="imageFallback(this)">
          <button class="like-btn" onclick="toggleLike(this)">♥</button>
        </div>
        <div class="product-info">
          <div class="product-title">Premium Black Abaya</div>
          <div class="price-hidden-tag">Contact via WhatsApp to know price</div>
          <div class="size-option">
            <label>Select Size:</label>
            <select id="size-1" class="size-select">
              <option value="52">52</option>
              <option value="54">54</option>
              <option value="56">56</option>
            </select>
          </div>
          <div class="btn-group">
            <a href="#" onclick="orderWhatsApp('Premium Black Abaya', 'size-1')" class="btn-whatsapp">
              WhatsApp Order
            </a>
            <a href="#" onclick="orderWhatsApp('Premium Black Abaya (Price Query)', 'size-1')" class="btn-contact">
              📞 Contact (Price)
            </a>
          </div>
        </div>
      </div>

      <!-- Item 2 -->
      <div class="product-card">
        <div class="product-image-container">
          <img src="assets/image2.png" alt="Premium Sea-Green Abaya" class="product-image" onerror="imageFallback(this)">
          <button class="like-btn" onclick="toggleLike(this)">♥</button>
        </div>
        <div class="product-info">
          <div class="product-title">Premium Sea-Green Abaya</div>
          <div class="price-hidden-tag">Contact via WhatsApp to know price</div>
          <div class="size-option">
            <label>Select Size:</label>
            <select id="size-2" class="size-select">
              <option value="52">52</option>
              <option value="54">54</option>
              <option value="56">56</option>
            </select>
          </div>
          <div class="btn-group">
            <a href="#" onclick="orderWhatsApp('Premium Sea-Green Abaya', 'size-2')" class="btn-whatsapp">
              WhatsApp Order
            </a>
            <a href="#" onclick="orderWhatsApp('Premium Sea-Green Abaya (Price Query)', 'size-2')" class="btn-contact">
              📞 Contact (Price)
            </a>
          </div>
        </div>
      </div>

      <!-- Item 3 -->
      <div class="product-card">
        <div class="product-image-container">
          <img src="assets/image3.png" alt="Premium Brown Abaya" class="product-image" onerror="imageFallback(this)">
          <button class="like-btn" onclick="toggleLike(this)">♥</button>
        </div>
        <div class="product-info">
          <div class="product-title">Premium Brown Abaya</div>
          <div class="price-hidden-tag">Contact via WhatsApp to know price</div>
          <div class="size-option">
            <label>Select Size:</label>
            <select id="size-3" class="size-select">
              <option value="52">52</option>
              <option value="54">54</option>
              <option value="56">56</option>
            </select>
          </div>
          <div class="btn-group">
            <a href="#" onclick="orderWhatsApp('Premium Brown Abaya', 'size-3')" class="btn-whatsapp">
              WhatsApp Order
            </a>
            <a href="#" onclick="orderWhatsApp('Premium Brown Abaya (Price Query)', 'size-3')" class="btn-contact">
              📞 Contact (Price)
            </a>
          </div>
        </div>
      </div>

      <!-- Item 4 -->
      <div class="product-card">
        <div class="product-image-container">
          <img src="assets/image4.png" alt="Premium Mauve Abaya" class="product-image" onerror="imageFallback(this)">
          <button class="like-btn" onclick="toggleLike(this)">♥</button>
        </div>
        <div class="product-info">
          <div class="product-title">Premium Mauve Abaya</div>
          <div class="price-hidden-tag">Contact via WhatsApp to know price</div>
          <div class="size-option">
            <label>Select Size:</label>
            <select id="size-4" class="size-select">
              <option value="52">52</option>
              <option value="54">54</option>
              <option value="56">56</option>
            </select>
          </div>
          <div class="btn-group">
            <a href="#" onclick="orderWhatsApp('Premium Mauve Abaya', 'size-4')" class="btn-whatsapp">
              WhatsApp Order
            </a>
            <a href="#" onclick="orderWhatsApp('Premium Mauve Abaya (Price Query)', 'size-4')" class="btn-contact">
              📞 Contact (Price)
            </a>
          </div>
        </div>
      </div>

      <!-- Item 5 -->
      <div class="product-card">
        <div class="product-image-container">
          <img src="assets/image5.png" alt="Deep Green Lace Abaya" class="product-image" onerror="imageFallback(this)">
          <button class="like-btn" onclick="toggleLike(this)">♥</button>
        </div>
        <div class="product-info">
          <div class="product-title">Deep Green Lace Abaya</div>
          <div class="price-hidden-tag">Contact via WhatsApp to know price</div>
          <div class="size-option">
            <label>Select Size:</label>
            <select id="size-5" class="size-select">
              <option value="52">52</option>
              <option value="54">54</option>
              <option value="56">56</option>
            </select>
          </div>
          <div class="btn-group">
            <a href="#" onclick="orderWhatsApp('Deep Green Lace Abaya', 'size-5')" class="btn-whatsapp">
              WhatsApp Order
            </a>
            <a href="#" onclick="orderWhatsApp('Deep Green Lace Abaya (Price Query)', 'size-5')" class="btn-contact">
              📞 Contact (Price)
            </a>
          </div>
        </div>
      </div>

      <!-- Item 6 -->
      <div class="product-card">
        <div class="product-image-container">
          <img src="assets/image6.png" alt="Lilac Purple Abaya" class="product-image" onerror="imageFallback(this)">
          <button class="like-btn" onclick="toggleLike(this)">♥</button>
        </div>
        <div class="product-info">
          <div class="product-title">Lilac Purple Abaya</div>
          <div class="price-hidden-tag">Contact via WhatsApp to know price</div>
          <div class="size-option">
            <label>Select Size:</label>
            <select id="size-6" class="size-select">
              <option value="52">52</option>
              <option value="54">54</option>
              <option value="56">56</option>
            </select>
          </div>
          <div class="btn-group">
            <a href="#" onclick="orderWhatsApp('Lilac Purple Abaya', 'size-6')" class="btn-whatsapp">
              WhatsApp Order
            </a>
            <a href="#" onclick="orderWhatsApp('Lilac Purple Abaya (Price Query)', 'size-6')" class="btn-contact">
              📞 Contact (Price)
            </a>
          </div>
        </div>
      </div>

      <!-- Item 7 -->
      <div class="product-card">
        <div class="product-image-container">
          <img src="assets/image7.png" alt="Mocha Brown Embroidery" class="product-image" onerror="imageFallback(this)">
          <button class="like-btn" onclick="toggleLike(this)">♥</button>
        </div>
        <div class="product-info">
          <div class="product-title">Mocha Brown Embroidery</div>
          <div class="price-hidden-tag">Contact via WhatsApp to know price</div>
          <div class="size-option">
            <label>Select Size:</label>
            <select id="size-7" class="size-select">
              <option value="52">52</option>
              <option value="54">54</option>
              <option value="56">56</option>
            </select>
          </div>
          <div class="btn-group">
            <a href="#" onclick="orderWhatsApp('Mocha Brown Embroidery', 'size-7')" class="btn-whatsapp">
              WhatsApp Order
            </a>
            <a href="#" onclick="orderWhatsApp('Mocha Brown Embroidery (Price Query)', 'size-7')" class="btn-contact">
              📞 Contact (Price)
            </a>
          </div>
        </div>
      </div>

      <!-- Item 8 -->
      <div class="product-card">
        <div class="product-image-container">
          <img src="assets/image8.png" alt="Designer Look Abaya" class="product-image" onerror="imageFallback(this)">
          <button class="like-btn" onclick="toggleLike(this)">♥</button>
        </div>
        <div class="product-info">
          <div class="product-title">Designer Look Abaya</div>
          <div class="price-hidden-tag">Contact via WhatsApp to know price</div>
          <div class="size-option">
            <label>Select Size:</label>
            <select id="size-8" class="size-select">
              <option value="52">52</option>
              <option value="54">54</option>
              <option value="56">56</option>
            </select>
          </div>
          <div class="btn-group">
            <a href="#" onclick="orderWhatsApp('Designer Look Abaya', 'size-8')" class="btn-whatsapp">
              WhatsApp Order
            </a>
            <a href="#" onclick="orderWhatsApp('Designer Look Abaya (Price Query)', 'size-8')" class="btn-contact">
              📞 Contact (Price)
            </a>
          </div>
        </div>
      </div>

      <!-- Item 9 -->
      <div class="product-card">
        <div class="product-image-container">
          <img src="assets/image9.png" alt="Royal Red Abaya" class="product-image" onerror="imageFallback(this)">
          <button class="like-btn" onclick="toggleLike(this)">♥</button>
        </div>
        <div class="product-info">
          <div class="product-title">Royal Red Abaya</div>
          <div class="price-hidden-tag">Contact via WhatsApp to know price</div>
          <div class="size-option">
            <label>Select Size:</label>
            <select id="size-9" class="size-select">
              <option value="52">52</option>
              <option value="54">54</option>
              <option value="56">56</option>
            </select>
          </div>
          <div class="btn-group">
            <a href="#" onclick="orderWhatsApp('Royal Red Abaya', 'size-9')" class="btn-whatsapp">
              WhatsApp Order
            </a>
            <a href="#" onclick="orderWhatsApp('Royal Red Abaya (Price Query)', 'size-9')" class="btn-contact">
              📞 Contact (Price)
            </a>
          </div>
        </div>
      </div>

    </div>
  </div>

  <div class="bottom-banner">
    <h3>Have questions or want to place an order?</h3>
    <a href="https://wa.me/971567439129" target="_blank" class="banner-wa-btn">
      💬 +971 567 43 9129
    </a>
  </div>

  <script>
    function toggleLike(btn) {
      btn.classList.toggle('active');
    }

    function imageFallback(img) {
      if (img.dataset.fallbackApplied) return;
      img.dataset.fallbackApplied = "1";
      img.src = "assets/image1.png";
    }

    function orderWhatsApp(productName, sizeSelectId) {
      var size = document.getElementById(sizeSelectId).value;
      var phoneNumber = "971567439129";
      var message = "Hello, I would like to inquire/order this item:\n\n" +
                    "Product: " + productName + "\n" +
                    "Size: " + size;
      
      var whatsappUrl = "https://wa.me/" + phoneNumber + "?text=" + encodeURIComponent(message);
      window.open(whatsappUrl, '_blank');
    }
  </script>

</body>
</html>
