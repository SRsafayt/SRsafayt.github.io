
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SRSafayt - Dubai Abaya Fashion</title>
    <!-- FontAwesome for Facebook Like & Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Arial, sans-serif;
        }

        body {
            background-color: #0f0f0f;
            color: #ffffff;
        }

        /* Top Header & Logo */
        .header {
            background-color: #000;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 2px solid #d4af37;
        }

        .logo {
            font-size: 22px;
            font-weight: bold;
            color: #d4af37;
            text-decoration: none;
            letter-spacing: 1px;
        }

        /* Hero Cover Banner */
        .hero-banner {
            text-align: center;
            padding: 40px 15px;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.9)), url('https://images.unsplash.com/photo-1542838132-92c53300491e?auto=format&fit=crop&w=800&q=80') center/cover;
            border-bottom: 2px solid #d4af37;
        }

        .hero-banner h3 {
            color: #d4af37;
            font-size: 13px;
            letter-spacing: 2px;
        }

        .hero-banner h1 {
            font-size: 24px;
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
            padding: 10px 18px;
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

        /* Main Container */
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px 10px;
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

        /* Layout Grid */
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
            color: #000;
        }

        .sidebar ul {
            list-style: none;
        }

        .sidebar ul li {
            padding: 8px 0;
            border-bottom: 1px solid #eee;
            font-size: 13px;
            color: #555;
            cursor: pointer;
        }

        /* Product Cards Options */
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
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
            border: 1px solid #e0e0e0;
            position: relative;
        }

        .product-card img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            border-radius: 6px;
            background-color: #e0e0e0;
        }

        .product-card h3 {
            font-size: 13px;
            margin-top: 10px;
            color: #222;
        }

        .product-card p {
            font-size: 11px;
            color: #777;
            margin-bottom: 10px;
        }

        /* Like & Action Buttons */
        .card-actions {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-top: 8px;
            border-top: 1px solid #eee;
        }

        .like-btn {
            background: #f0f2f5;
            border: none;
            color: #1877f2;
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 12px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 5px;
            font-weight: bold;
        }

        .like-btn:hover {
            background: #e4e6eb;
        }

        .order-btn {
            background-color: #25d366;
            color: #fff;
            padding: 6px 10px;
            border-radius: 4px;
            text-decoration: none;
            font-size: 11px;
            font-weight: bold;
        }

        /* WhatsApp Contact Banner */
        .whatsapp-banner {
            background-color: #000;
            color: #fff;
            padding: 15px;
            border-radius: 8px;
            margin-top: 25px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border: 1px solid #d4af37;
        }

        .whatsapp-btn {
            background-color: #25d366;
            color: #fff;
            padding: 10px 15px;
            border-radius: 5px;
            font-weight: bold;
            text-decoration: none;
            font-size: 13px;
        }

        /* Mobile Optimization */
        @media (max-width: 768px) {
            .main-layout {
                flex-direction: column;
            }

            .sidebar {
                width: 100%;
            }

            .product-grid {
                grid-template-columns: repeat(2, 1fr);
                gap: 10px;
            }

            .product-card img {
                height: 170px;
            }

            .whatsapp-banner {
                flex-direction: column;
                gap: 12px;
                text-align: center;
            }
        }
    </style>
</head>
<body>

    <!-- Header Section with Your Logo -->
    <header class="header">
        <a href="#" class="logo"><i class="fa-solid fa-gem"></i> SRSafayt</a>
        <a href="https://wa.me/971567439129" style="color: #25d366; font-size: 20px;"><i class="fa-brands fa-whatsapp"></i></a>
    </header>

    <!-- Hero Islamic Banner -->
    <section class="hero-banner">
        <h3>WELCOME TO</h3>
        <h1>DUBAI ABAYA FASHION</h1>
        <p>MODESTY IS THE NEW LUXURY<br>PREMIUM ABAYAS & BURQAS</p>
        <div class="btn-container">
            <a href="#" class="btn btn-gold">EXPLORE COLLECTION &rarr;</a>
            <a href="#" class="btn btn-outline">NEW ARRIVALS</a>
        </div>
    </section>

    <!-- Main Container -->
    <main class="container">
        <div class="section-title">
            <h2>OUR EXCLUSIVE COLLECTION</h2>
            <p style="font-size: 12px; color: #666;">Premium Abayas & Burqas</p>
        </div>

        <div class="main-layout">
            <!-- Sidebar Navigation -->
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

            <!-- Product Grid Options -->
            <section class="product-grid" id="productContainer">
                <!-- Javascript দিয়ে ছবি লোড হবে -->
            </section>
        </div>

        <!-- WhatsApp Banner -->
        <div class="whatsapp-banner">
            <div>
                <p style="font-size: 12px;">HAVE A QUESTION OR WANT TO PLACE AN ORDER?</p>
                <h3 style="color: #d4af37; font-size: 18px; margin-top: 3px;">+971 56 743 9129</h3>
            </div>
            <a href="https://wa.me/971567439129" class="whatsapp-btn"><i class="fa-brands fa-whatsapp"></i> CHAT ON WHATSAPP</a>
        </div>
    </main>

    <!-- Auto Load Reliable Abaya Images & Like Feature -->
    <script>
        // সরাসরি কাজ করবে এমন টেস্টেড ইসলামিক আবায়া ছবিসমূহ
        const abayaImages = [
            "https://images.unsplash.com/photo-1583391733956-3750e0ff4e8b?auto=format&fit=crop&w=500&q=80",
            "https://images.unsplash.com/photo-1567401893414-76b7b1e5a7a5?auto=format&fit=crop&w=500&q=80",
            "https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?auto=format&fit=crop&w=500&q=80",
            "https://images.unsplash.com/photo-1490481651871-ab68de25d43d?auto=format&fit=crop&w=500&q=80",
            "https://images.unsplash.com/photo-1509631179647-0177331693ae?auto=format&fit=crop&w=500&q=80",
            "https://images.unsplash.com/photo-1483985988355-763728e1935b?auto=format&fit=crop&w=500&q=80"
        ];

        const products = [
            { name: "BLACK ROYAL ABAYA", category: "New Collection" },
            { name: "NAVY BLUE ABAYA", category: "New Collection" },
            { name: "MOCHA BROWN ABAYA", category: "New Collection" },
            { name: "EMERALD GREEN ABAYA", category: "New Collection" },
            { name: "BEIGE ELEGANT ABAYA", category: "New Collection" },
            { name: "DESIGNER BLACK BURQA", category: "New Collection" }
        ];

        const container = document.getElementById('productContainer');

        products.forEach((product, index) => {
            // র্যান্ডম পেজ রিফ্রেশ ছবি নেওয়ার নিয়ম
            const imgIndex = (index + Math.floor(Math.random() * abayaImages.length)) % abayaImages.length;
            const imageUrl = abayaImages[imgIndex];

            const cardHtml = `
                <div class="product-card">
                    <img src="${imageUrl}" alt="${product.name}">
                    <h3>${product.name}</h3>
                    <p>${product.category}</p>
                    <div class="card-actions">
                        <button class="like-btn" onclick="toggleLike(this)">
                            <i class="fa-regular fa-thumbs-up"></i> Like <span class="like-count">${Math.floor(Math.random() * 20) + 5}</span>
                        </button>
                        <a href="https://wa.me/971567439129?text=I%20want%20to%20buy%20${encodeURIComponent(product.name)}" class="order-btn">Order</a>
                    </div>
                </div>
            `;
            container.innerHTML += cardHtml;
        });

        // ফেসবুক লাইক টগল ফাংশন
        function toggleLike(btn) {
            const icon = btn.querySelector('i');
            const countSpan = btn.querySelector('.like-count');
            let count = parseInt(countSpan.innerText);

            if (icon.classList.contains('fa-regular')) {
                icon.classList.remove('fa-regular');
                icon.classList.add('fa-solid');
                btn.style.color = '#1877f2';
                countSpan.innerText = count + 1;
            } else {
                icon.classList.remove('fa-solid');
                icon.classList.add('fa-regular');
                countSpan.innerText = count - 1;
            }
        }
    </script>
</body>
</html>
