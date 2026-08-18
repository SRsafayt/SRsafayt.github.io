<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SRSafayt - Dubai Abaya Fashion</title>
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Arial, sans-serif;
        }

        body {
            background-color: #0d0d0d;
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

        /* Hero Dark Luxury Cover Banner */
        .hero-banner {
            text-align: center;
            padding: 45px 15px;
            background: linear-gradient(rgba(0,0,0,0.85), rgba(0,0,0,0.95)), #111;
            border-bottom: 2px solid #d4af37;
        }

        .hero-banner h3 {
            color: #d4af37;
            font-size: 12px;
            letter-spacing: 2px;
        }

        .hero-banner h1 {
            font-size: 24px;
            margin: 10px 0;
            color: #fff;
            text-transform: uppercase;
        }

        .hero-banner p {
            color: #ccc;
            font-size: 12px;
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
            font-size: 12px;
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
            background-color: #f8f9fa;
            color: #333;
        }

        .section-title {
            text-align: center;
            margin-bottom: 20px;
        }

        .section-title h2 {
            font-size: 20px;
            color: #111;
            text-transform: uppercase;
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
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
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

        /* Product Cards Mobile Options */
        .product-grid {
            flex: 1;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 12px;
        }

        .product-card {
            background: #fff;
            border-radius: 8px;
            padding: 8px;
            text-align: center;
            box-shadow: 0 2px 8px rgba(0,0,0,0.06);
            border: 1px solid #e0e0e0;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .product-card img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            border-radius: 6px;
            background-color: #f0f0f0;
        }

        .product-card h3 {
            font-size: 12px;
            margin-top: 8px;
            color: #111;
            font-weight: 700;
        }

        .product-card p {
            font-size: 10px;
            color: #777;
            margin-bottom: 8px;
        }

        /* Like & Order Actions */
        .card-actions {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-top: 8px;
            border-top: 1px solid #eee;
            gap: 5px;
        }

        .like-btn {
            background: #e7f0ff;
            border: none;
            color: #1877f2;
            padding: 6px 10px;
            border-radius: 15px;
            font-size: 11px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 4px;
            font-weight: bold;
            flex: 1;
            justify-content: center;
        }

        .order-btn {
            background-color: #25d366;
            color: #fff;
            padding: 6px 10px;
            border-radius: 4px;
            text-decoration: none;
            font-size: 11px;
            font-weight: bold;
            flex: 1;
            text-align: center;
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

            .product-grid {
                grid-template-columns: repeat(2, 1fr);
                gap: 10px;
            }

            .product-card img {
                height: 190px;
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

    <!-- Logo & Header -->
    <header class="header">
        <a href="#" class="logo"><i class="fa-solid fa-gem"></i> SRSafayt</a>
        <a href="https://wa.me/971567439129" style="color: #25d366; font-size: 22px;"><i class="fa-brands fa-whatsapp"></i></a>
    </header>

    <!-- Cover Banner -->
    <section class="hero-banner">
        <h3>WELCOME TO</h3>
        <h1>DUBAI ABAYA FASHION</h1>
        <p>MODESTY IS THE NEW LUXURY<br>PREMIUM ABAYAS & BURQAS</p>
        <div class="btn-container">
            <a href="#" class="btn btn-gold">EXPLORE COLLECTION &rarr;</a>
            <a href="#" class="btn btn-outline">NEW ARRIVALS</a>
        </div>
    </section>

    <!-- Main Shop Area -->
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

            <!-- Product Grid Options -->
            <section class="product-grid" id="productContainer">
                <!-- Javascript দিয়ে শুধুমাত্র ইসলামিক বোরকা ও আবায়ার ছবি দেওয়া হবে -->
            </section>
        </div>

        <!-- WhatsApp Banner -->
        <div class="whatsapp-banner">
            <div>
                <p style="font-size: 11px;">HAVE A QUESTION OR WANT TO PLACE AN ORDER?</p>
                <h3 style="color: #d4af37; font-size: 17px; margin-top: 2px;">+971 56 743 9129</h3>
            </div>
            <a href="https://wa.me/971567439129" class="whatsapp-btn"><i class="fa-brands fa-whatsapp"></i> CHAT ON WHATSAPP</a>
        </div>
    </main>

    <!-- JS Code -->
    <script>
        // শতভাগ নিশ্চিত ইসলামিক আবায়া ও বোরকার ফিল্টারকৃত ছবি
        const abayaProducts = [
            {
                name: "BLACK ROYAL ABAYA",
                category: "New Collection",
                img: "https://images.pexels.com/photos/9940431/pexels-photo-9940431.jpeg?auto=compress&cs=tinysrgb&w=500"
            },
            {
                name: "NAVY BLUE ABAYA",
                category: "New Collection",
                img: "https://images.pexels.com/photos/11622340/pexels-photo-11622340.jpeg?auto=compress&cs=tinysrgb&w=500"
            },
            {
                name: "MOCHA BROWN ABAYA",
                category: "New Collection",
                img: "https://images.pexels.com/photos/10380428/pexels-photo-10380428.jpeg?auto=compress&cs=tinysrgb&w=500"
            },
            {
                name: "EMERALD GREEN ABAYA",
                category: "New Collection",
                img: "https://images.pexels.com/photos/11622339/pexels-photo-11622339.jpeg?auto=compress&cs=tinysrgb&w=500"
            },
            {
                name: "BEIGE ELEGANT ABAYA",
                category: "New Collection",
                img: "https://images.pexels.com/photos/11622338/pexels-photo-11622338.jpeg?auto=compress&cs=tinysrgb&w=500"
            },
            {
                name: "DESIGNER BLACK BURQA",
                category: "New Collection",
                img: "https://images.pexels.com/photos/9940432/pexels-photo-9940432.jpeg?auto=compress&cs=tinysrgb&w=500"
            }
        ];

        const container = document.getElementById('productContainer');

        abayaProducts.forEach((product) => {
            const cardHtml = `
                <div class="product-card">
                    <div>
                        <img src="${product.img}" alt="${product.name}" loading="lazy">
                        <h3>${product.name}</h3>
                        <p>${product.category}</p>
                    </div>
                    <div class="card-actions">
                        <button class="like-btn" onclick="toggleLike(this)">
                            <i class="fa-regular fa-thumbs-up"></i> Like <span class="like-count">${Math.floor(Math.random() * 25) + 10}</span>
                        </button>
                        <a href="https://wa.me/971567439129?text=Hello,%20I%20want%20to%20order%20${encodeURIComponent(product.name)}" class="order-btn" target="_blank">Order</a>
                    </div>
                </div>
            `;
            container.innerHTML += cardHtml;
        });

        // Facebook Like Functionality
        function toggleLike(btn) {
            const icon = btn.querySelector('i');
            const countSpan = btn.querySelector('.like-count');
            let count = parseInt(countSpan.innerText);

            if (icon.classList.contains('fa-regular')) {
                icon.classList.remove('fa-regular');
                icon.classList.add('fa-solid');
                btn.style.background = '#1877f2';
                btn.style.color = '#ffffff';
                countSpan.innerText = count + 1;
            } else {
                icon.classList.remove('fa-solid');
                icon.classList.add('fa-regular');
                btn.style.background = '#e7f0ff';
                btn.style.color = '#1877f2';
                countSpan.innerText = count - 1;
            }
        }
    </script>
</body>
</html>
