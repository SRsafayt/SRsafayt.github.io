<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dubai Abaya Fashion</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f4f4f9;
            color: #333;
        }

        /* Header Navigation */
        header {
            background-color: #131921;
            color: white;
            padding: 15px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            color: #f3a847;
            letter-spacing: 1px;
        }

        .contact-top {
            font-size: 15px;
            font-weight: 500;
        }

        /* Hero Banner */
        .banner {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://via.placeholder.com/1200x400?text=Dubai+Abaya+Collection');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 80px 20px;
        }

        .banner h1 {
            font-size: 38px;
            margin-bottom: 10px;
        }

        .banner p {
            font-size: 18px;
            margin-bottom: 20px;
        }

        .banner-btn {
            background-color: #25D366;
            color: white;
            padding: 12px 25px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 5px;
            display: inline-block;
        }

        /* Product Section Grid */
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 30px;
            font-size: 28px;
            color: #111;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
        }

        .product-card {
            background: white;
            border: 1px solid #e2e2e2;
            border-radius: 8px;
            overflow: hidden;
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .product-card img {
            width: 100%;
            height: 320px;
            object-fit: cover;
        }

        .product-info {
            padding: 15px;
        }

        .product-title {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 8px;
        }

        .product-details {
            font-size: 14px;
            color: #555;
            margin-bottom: 12px;
            line-height: 1.5;
        }

        .whatsapp-btn {
            display: block;
            width: 100%;
            background-color: #25D366;
            color: white;
            text-align: center;
            padding: 10px 0;
            text-decoration: none;
            font-weight: bold;
            border-radius: 4px;
        }

        .whatsapp-btn:hover {
            background-color: #1eb854;
        }

        /* Footer */
        footer {
            background-color: #131921;
            color: white;
            text-align: center;
            padding: 20px;
            margin-top: 50px;
            font-size: 14px;
        }
    </style>
</head>
<body>

    <!-- Navigation Header -->
    <header>
        <div class="logo">DUBAI ABAYA COLLECTION</div>
        <div class="contact-top">WhatsApp: +971 567 439129</div>
    </header>

    <!-- Hero Banner -->
    <section class="banner">
        <h1>এক্সক্লুসিভ দুবাই আবায়া কালেকশন</h1>
        <p>সেরা ডিজাইন ও প্রিমিয়াম ফেব্রিকস | আপনার সাইজ অনুযায়ী অর্ডার করুন</p>
        <a href="https://wa.me/971567439129" class="banner-btn" target="_blank">কথা বলুন WhatsApp-এ (+971 567 439129)</a>
    </section>

    <!-- Products Grid -->
    <div class="container">
        <h2 class="section-title">আমাদের আবায়া কালেকশন</h2>
        <div class="product-grid">

            <!-- Product 1 -->
            <div class="product-card">
                <img src="https://via.placeholder.com/300x400?text=Abaya+1" alt="Abaya 1">
                <div class="product-info">
                    <div class="product-title">ক্লাসিক ব্ল্যাক আবায়া</div>
                    <div class="product-details">
                        <strong>কালার:</strong> কালো<br>
                        <strong>বুকের সাইজ (Bust):</strong> 38", 40", 42", 44"<br>
                        <strong>ফিটিং:</strong> রিল্যাক্সড ফিট
                    </div>
                    <a href="https://wa.me/971567439129?text=I%20want%20to%20know%20the%20price%20for%20Classic%20Black%20Abaya" class="whatsapp-btn" target="_blank">দাম জানতে WhatsApp করুন</a>
                </div>
            </div>

            <!-- Product 2 -->
            <div class="product-card">
                <img src="https://via.placeholder.com/300x400?text=Abaya+2" alt="Abaya 2">
                <div class="product-info">
                    <div class="product-title">রয়েল নেভি ব্লু আবায়া</div>
                    <div class="product-details">
                        <strong>কালার:</strong> নেভি ব্লু<br>
                        <strong>বুকের সাইজ (Bust):</strong> 36", 38", 40", 42"<br>
                        <strong>ফিটিং:</strong> রেগুলার ফিট
                    </div>
                    <a href="https://wa.me/971567439129?text=I%20want%20to%20know%20the%20price%20for%20Royal%20Navy%20Abaya" class="whatsapp-btn" target="_blank">দাম জানতে WhatsApp করুন</a>
                </div>
            </div>

            <!-- Product 3 -->
            <div class="product-card">
                <img src="https://via.placeholder.com/300x400?text=Abaya+3" alt="Abaya 3">
                <div class="product-info">
                    <div class="product-title">মেরুন এমব্রয়ডারি আবায়া</div>
                    <div class="product-details">
                        <strong>কালার:</strong> ডার্ক মেরুন<br>
                        <strong>বুকের সাইজ (Bust):</strong> 40", 42", 44", 46"<br>
                        <strong>ফিটিং:</strong> কমফোর্ট ফিট
                    </div>
                    <a href="https://wa.me/971567439129?text=I%20want%20to%20know%20the%20price%20for%20Maroon%20Abaya" class="whatsapp-btn" target="_blank">দাম জানতে WhatsApp করুন</a>
                </div>
            </div>

            <!-- Product 4 -->
            <div class="product-card">
                <img src="https://via.placeholder.com/300x400?text=Abaya+4" alt="Abaya 4">
                <div class="product-info">
                    <div class="product-title">দুর্লভ অলিভ গ্রিন আবায়া</div>
                    <div class="product-details">
                        <strong>কালার:</strong> অলিভ গ্রিন<br>
                        <strong>বুকের সাইজ (Bust):</strong> 38", 40", 42"<br>
                        <strong>ফিটিং:</strong> স্লিম ফিট
                    </div>
                    <a href="https://wa.me/971567439129?text=I%20want%20to%20know%20the%20price%20for%20Olive%20Green%20Abaya" class="whatsapp-btn" target="_blank">দাম জানতে WhatsApp করুন</a>
                </div>
            </div>

            <!-- Product 5 -->
            <div class="product-card">
                <img src="https://via.placeholder.com/300x400?text=Abaya+5" alt="Abaya 5">
                <div class="product-info">
                    <div class="product-title">প্রিমিয়াম শ্যাম্পেন বেইজ আবায়া</div>
                    <div class="product-details">
                        <strong>কালার:</strong> বেইজ / ক্রিম<br>
                        <strong>বুকের সাইজ (Bust):</strong> 36", 38", 40", 44"<br>
                        <strong>ফিটিং:</strong> ফ্রি সাইজ
                    </div>
                    <a href="https://wa.me/971567439129?text=I%20want%20to%20know%20the%20price%20for%20Beige%20Abaya" class="whatsapp-btn" target="_blank">দাম জানতে WhatsApp করুন</a>
                </div>
            </div>

            <!-- Product 6 -->
            <div class="product-card">
                <img src="https://via.placeholder.com/300x400?text=Abaya+6" alt="Abaya 6">
                <div class="product-info">
                    <div class="product-title">সিম্পল ক্যাজুয়াল আবায়া</div>
                    <div class="product-details">
                        <strong>কালার:</strong> গ্রে (ধূসর)<br>
                        <strong>বুকের সাইজ (Bust):</strong> 38", 40", 42", 44"<br>
                        <strong>ফিটিং:</strong> রেগুলার ফিট
                    </div>
                    <a href="https://wa.me/971567439129?text=I%20want%20to%20know%20the%20price%20for%20Grey%20Abaya" class="whatsapp-btn" target="_blank">দাম জানতে WhatsApp করুন</a>
                </div>
            </div>

        </div>
    </div>

    <!-- Footer Section -->
    <footer>
        <p>&copy; 2026 Dubai Abaya Collection | All Rights Reserved.</p>
        <p>অর্ডারের জন্য যোগাযোগ করুন: +971 567 439129</p>
    </footer>

</body>
</html>
