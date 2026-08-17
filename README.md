<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dubai Abaya Collection</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Arial, sans-serif;
        }

        body {
            background-color: #f8f9fa;
            color: #333;
        }

        /* Header Navigation */
        header {
            background-color: #131921;
            color: white;
            padding: 12px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            flex-wrap: wrap;
            gap: 10px;
        }

        .logo {
            font-size: 20px;
            font-weight: bold;
            color: #f3a847;
            letter-spacing: 1px;
        }

        .contact-top {
            font-size: 14px;
            color: #25D366;
            font-weight: 600;
        }

        /* Hero Banner */
        .banner {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1583391733956-3750e0ff4e8b?auto=format&fit=crop&w=1200&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 50px 15px;
        }

        .banner h1 {
            font-size: 26px;
            margin-bottom: 10px;
        }

        .banner p {
            font-size: 15px;
            margin-bottom: 20px;
            color: #ddd;
        }

        .banner-btn {
            background-color: #25D366;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 5px;
            display: inline-block;
            font-size: 14px;
        }

        /* Product Section Grid */
        .container {
            max-width: 1200px;
            margin: 30px auto;
            padding: 0 15px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 25px;
            font-size: 24px;
            color: #111;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 20px;
        }

        .product-card {
            background: white;
            border: 1px solid #e0e0e0;
            border-radius: 8px;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }

        .product-card img {
            width: 100%;
            height: 350px;
            object-fit: cover;
        }

        .product-info {
            padding: 15px;
        }

        .product-title {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 8px;
            color: #222;
        }

        .product-details {
            font-size: 14px;
            color: #555;
            margin-bottom: 15px;
            line-height: 1.6;
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
            font-size: 14px;
        }

        /* Footer */
        footer {
            background-color: #131921;
            color: white;
            text-align: center;
            padding: 20px 15px;
            margin-top: 40px;
            font-size: 13px;
            line-height: 1.6;
        }
    </style>
</head>
<body>

    <!-- Header Navigation -->
    <header>
        <div class="logo">DUBAI ABAYA COLLECTION</div>
        <div class="contact-top">WhatsApp: +971 567 439129</div>
    </header>

    <!-- Hero Banner -->
    <section class="banner">
        <h1>Exclusive Dubai Abaya Collection</h1>
        <p>Premium Fabrics & Elegant Designs | Order Your Preferred Size</p>
        <a href="https://wa.me/971567439129" class="banner-btn" target="_blank">Chat on WhatsApp</a>
    </section>

    <!-- Products Grid -->
    <div class="container">
        <h2 class="section-title">Our Featured Collection</h2>
        <div class="product-grid">

            <!-- Product 1 -->
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1583391733956-3750e0ff4e8b?auto=format&fit=crop&w=600&q=80" alt="Abaya 1">
                <div class="product-info">
                    <div class="product-title">Classic Black Abaya</div>
                    <div class="product-details">
                        <strong>Color:</strong> Black<br>
                        <strong>Bust Size:</strong> 38", 40", 42", 44"<br>
                        <strong>Fitting:</strong> Relaxed Fit
                    </div>
                    <a href="https://wa.me/971567439129?text=I%20want%20to%20know%20the%20price%20for%20Classic%20Black%20Abaya" class="whatsapp-btn" target="_blank">Ask Price on WhatsApp</a>
                </div>
            </div>

            <!-- Product 2 -->
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1583391733956-3750e0ff4e8b?auto=format&fit=crop&w=600&q=80" alt="Abaya 2">
                <div class="product-info">
                    <div class="product-title">Royal Navy Blue Abaya</div>
                    <div class="product-details">
                        <strong>Color:</strong> Navy Blue<br>
                        <strong>Bust Size:</strong> 36", 38", 40", 42"<br>
                        <strong>Fitting:</strong> Regular Fit
                    </div>
                    <a href="https://wa.me/971567439129?text=I%20want%20to%20know%20the%20price%20for%20Royal%20Navy%20Abaya" class="whatsapp-btn" target="_blank">Ask Price on WhatsApp</a>
                </div>
            </div>

            <!-- Product 3 -->
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1583391733956-3750e0ff4e8b?auto=format&fit=crop&w=600&q=80" alt="Abaya 3">
                <div class="product-info">
                    <div class="product-title">Maroon Embroidery Abaya</div>
                    <div class="product-details">
                        <strong>Color:</strong> Dark Maroon<br>
                        <strong>Bust Size:</strong> 40", 42", 44", 46"<br>
                        <strong>Fitting:</strong> Comfort Fit
                    </div>
                    <a href="https://wa.me/971567439129?text=I%20want%20to%20know%20the%20price%20for%20Maroon%20Abaya" class="whatsapp-btn" target="_blank">Ask Price on WhatsApp</a>
                </div>
            </div>

            <!-- Product 4 -->
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1583391733956-3750e0ff4e8b?auto=format&fit=crop&w=600&q=80" alt="Abaya 4">
                <div class="product-info">
                    <div class="product-title">Elegant Olive Green Abaya</div>
                    <div class="product-details">
                        <strong>Color:</strong> Olive Green<br>
                        <strong>Bust Size:</strong> 38", 40", 42"<br>
                        <strong>Fitting:</strong> Slim Fit
                    </div>
                    <a href="https://wa.me/971567439129?text=I%20want%20to%20know%20the%20price%20for%20Olive%20Green%20Abaya" class="whatsapp-btn" target="_blank">Ask Price on WhatsApp</a>
                </div>
            </div>

            <!-- Product 5 -->
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1583391733956-3750e0ff4e8b?auto=format&fit=crop&w=600&q=80" alt="Abaya 5">
                <div class="product-info">
                    <div class="product-title">Premium Champagne Beige Abaya</div>
                    <div class="product-details">
                        <strong>Color:</strong> Beige / Cream<br>
                        <strong>Bust Size:</strong> 36", 38", 40", 44"<br>
                        <strong>Fitting:</strong> Free Size
                    </div>
                    <a href="https://wa.me/971567439129?text=I%20want%20to%20know%20the%20price%20for%20Beige%20Abaya" class="whatsapp-btn" target="_blank">Ask Price on WhatsApp</a>
                </div>
            </div>

            <!-- Product 6 -->
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1583391733956-3750e0ff4e8b?auto=format&fit=crop&w=600&q=80" alt="Abaya 6">
                <div class="product-info">
                    <div class="product-title">Simple Casual Grey Abaya</div>
                    <div class="product-details">
                        <strong>Color:</strong> Grey<br>
                        <strong>Bust Size:</strong> 38", 40", 42", 44"<br>
                        <strong>Fitting:</strong> Regular Fit
                    </div>
                    <a href="https://wa.me/971567439129?text=I%20want%20to%20know%20the%20price%20for%20Grey%20Abaya" class="whatsapp-btn" target="_blank">Ask Price on WhatsApp</a>
                </div>
            </div>

        </div>
    </div>

    <!-- Footer Section -->
    <footer>
        <p>&copy; 2026 Dubai Abaya Collection | All Rights Reserved.</p>
        <p>For Orders Contact: +971 567 439129</p>
    </footer>

</body>
</html>
