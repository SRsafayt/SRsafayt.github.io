
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dubai Abaya Fashion</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #0f0f0f;
            color: #ffffff;
        }

        /* Hero Banner */
        .hero-banner {
            text-align: center;
            padding: 40px 15px;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.9)), url('https://source.unsplash.com/1600x900/?islamic,architecture') center/cover;
            border-bottom: 2px solid #d4af37;
        }

        .hero-banner h3 {
            color: #d4af37;
            font-size: 13px;
            letter-spacing: 2px;
        }

        .hero-banner h1 {
            font-size: 26px;
            margin: 10px 0;
            color: #fff;
        }

        .hero-banner p {
            color: #ccc;
            font-size: 13px;
            margin-bottom: 20px;
        }

        .btn-container {
            display: flex;
            gap: 10px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 10px 20px;
            border-radius: 5px;
            font-size: 13px;
            font-weight: bold;
            text-decoration: none;
        }

        .btn-gold {
            background-color: #d4af37;
            color: #000;
        }

        .btn-outline {
            border: 1px solid #fff;
            color: #fff;
        }

        /* Container */
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 20px 15px;
            background-color: #f4f4f4;
            color: #333;
        }

        .section-title {
            text-align: center;
            margin-bottom: 20px;
        }

        .section-title h2 {
            font-size: 20px;
            color: #111;
        }

        /* Grid Layout */
        .main-layout {
            display: flex;
            gap: 20px;
        }

        .sidebar {
            width: 220px;
            background: #fff;
            padding: 15px;
            border-radius: 8px;
            height: fit-content;
        }

        .sidebar h4 {
            margin-bottom: 10px;
            font-size: 14px;
            border-bottom: 2px solid #d4af37;
            padding-bottom: 5px;
        }

        .sidebar ul {
            list-style: none;
        }

        .sidebar ul li {
            padding: 8px 0;
            border-bottom: 1px solid #eee;
            font-size: 13px;
        }

        /* Product Grid Options */
        .product-grid {
            flex: 1;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
        }

        .product-card {
            background: #fff;
            border-radius: 8px;
            padding: 10px;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            border: 1px solid #e5e5e5;
        }

        .product-card img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 6px;
            background-color: #eee;
        }

        .product-card h3 {
            font-size: 13px;
            margin-top: 10px;
            color: #222;
        }

        .product-card p {
            font-size: 11px;
            color: #777;
        }

        /* WhatsApp Section */
        .whatsapp-banner {
            background-color: #000;
            color: #fff;
            padding: 15px;
            border-radius: 8px;
            margin-top: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .whatsapp-btn {
            background-color: #d4af37;
            color: #000;
            padding: 10px 15px;
            border-radius: 5px;
            font-weight: bold;
            text-decoration: none;
            font-size: 12px;
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .main-layout {
                flex-direction: column;
            }

            .sidebar {
                width: 100%;
            }

            /* মোবাইলে সুন্দর ২ কলামের গ্রিড অপশন */
            .product-grid {
                grid-template-columns: repeat(2, 1fr);
                gap: 10px;
            }

            .product-card img {
                height: 180px;
            }

            .whatsapp-banner {
                flex-direction: column;
                gap: 10px;
                text-align: center;
            }
        }
    </style>
</head>
<body>

    <!-- Hero Banner -->
    <section class="hero-banner">
        <h3>WELCOME TO</h3>
        <h1>DUBAI ABAYA FASHION</h1>
        <p>MODESTY IS THE NEW LUXURY<br>PREMIUM ABAYAS & BURQAS</p>
        <div class="btn-container">
            <a href="#" class="btn btn-gold">EXPLORE COLLECTION &rarr;</a>
            <a href="#" class="btn btn-outline">VIEW NEW ARRIVALS</a>
        </div>
    </section>

    <!-- Main Section -->
    <main class="container">
        <div class="section-title">
            <h2>OUR EXCLUSIVE COLLECTION</h2>
            <p style="font-size: 12px; color: #666;">Premium Abayas & Burqas</p>
        </div>

        <div class="main-layout">
            <!-- Sidebar -->
            <aside class="sidebar">
                <h4>SHOP BY CATEGORY</h4>
                <ul>
                    <li>All Collections &rsaquo;</li>
                    <li>Abayas &rsaquo;</li>
                    <li>Burqas &rsaquo;</li>
                    <li>New Arrivals &rsaquo;</li>
                    <li>Best Sellers &rsaquo;</li>
                </ul>
            </aside>

            <!-- Dynamic Product Grid -->
            <section class="product-grid" id="productContainer">
                <!-- JavaScript এর মাধ্যমে অটোমেটিক ছবি আসবে -->
            </section>
        </div>

        <!-- WhatsApp Banner -->
        <div class="whatsapp-banner">
            <div>
                <p style="font-size: 11px;">HAVE A QUESTION OR WANT TO PLACE AN ORDER?</p>
                <h3 style="color: #d4af37; font-size: 16px;">+971 56 743 9129</h3>
            </div>
            <a href="https://wa.me/971567439129" class="whatsapp-btn">CHAT ON WHATSAPP</a>
        </div>
    </main>

    <!-- JavaScript code for Auto-Refreshing Images -->
    <script>
        const products = [
            { name: "BLACK ROYAL ABAYA", category: "New Collection" },
            { name: "NAVY BLUE ABAYA", category: "New Collection" },
            { name: "MOCHA BROWN ABAYA", category: "New Collection" },
            { name: "EMERALD GREEN ABAYA", category: "New Collection" },
            { name: "BEIGE ELEGANT ABAYA", category: "New Collection" },
            { name: "DESIGNER BLACK BURQA", category: "New Collection" }
        ];

        const container = document.getElementById('productContainer');

        // অটোমেটিক আবায়া ও ইসলামিক ফ্যাশনের ছবি লোড করার ফাংশন
        products.forEach((product, index) => {
            const randomNum = Math.floor(Math.random() * 1000); // পেজ রিফ্রেশ করলে নতুন ছবি পাওয়ার জন্য
            const imageUrl = `https://source.unsplash.com/400x500/?abaya,hijab,dubai-fashion,islamic-fashion&sig=${randomNum + index}`;

            const cardHtml = `
                <div class="product-card">
                    <img src="${imageUrl}" alt="${product.name}" loading="lazy">
                    <h3>${product.name}</h3>
                    <p>${product.category}</p>
                </div>
            `;
            container.innerHTML += cardHtml;
        });
    </script>
</body>
</html>
