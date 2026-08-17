
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dubai Abaya & Burqa Collection</title>
  <style>
    /* Reset & General Styles */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background-color: #f8f9fa;
      color: #333;
    }

    /* Header Section */
    header {
      background-color: #111;
      color: #fff;
      padding: 20px;
      text-align: center;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    /* Main Container */
    .container {
      max-width: 1200px;
      margin: 30px auto;
      padding: 0 15px;
    }

    /* Gallery Grid Structure */
    .abaya-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 25px;
    }

    /* Product Card Style */
    .abaya-card {
      background: #ffffff;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .abaya-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
    }

    /* Image Wrapper & Settings */
    .img-box {
      width: 100%;
      height: 380px;
      overflow: hidden;
      background-color: #eee;
    }

    .img-box img {
      width: 100%;
      height: 100%;
      object-fit: cover; /* এটি ছবি না কেটে সুন্দরভাবে ফিট করবে */
      display: block;
      transition: transform 0.5s ease;
    }

    .abaya-card:hover .img-box img {
      transform: scale(1.05); /* হোভার করলে ছবি জুমিং ইফেক্ট দেবে */
    }

    /* Title Details */
    .abaya-info {
      padding: 15px;
      text-align: center;
    }

    .abaya-info h3 {
      font-size: 16px;
      font-weight: 600;
      color: #222;
      letter-spacing: 0.5px;
      text-transform: uppercase;
    }
  </style>
</head>
<body>

  <header>
    <h1>LUXURY ABAYA COLLECTION</h1>
  </header>

  <div class="container">
    <div class="abaya-grid">

      <!-- Card 1 -->
      <div class="abaya-card">
        <div class="img-box">
          <img src="https://images.unsplash.com/photo-1583391733956-3750e0ff4e8b?auto=format&fit=crop&w=600&q=80" alt="Embroidered Abaya">
        </div>
        <div class="abaya-info">
          <h3>Embroidered Black Abaya</h3>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="abaya-card">
        <div class="img-box">
          <img src="https://images.unsplash.com/photo-1563178406-4cdc2923acbc?auto=format&fit=crop&w=600&q=80" alt="Stylish Mauve Abaya">
        </div>
        <div class="abaya-info">
          <h3>Stylish Mauve Abaya</h3>
        </div>
      </div>

      <!-- Card 3 -->
      <div class="abaya-card">
        <div class="img-box">
          <img src="https://images.unsplash.com/photo-1583391733975-299f242588a4?auto=format&fit=crop&w=600&q=80" alt="Brown Designer Abaya">
        </div>
        <div class="abaya-info">
          <h3>Brown Designer Abaya</h3>
        </div>
      </div>

      <!-- Card 4 -->
      <div class="abaya-card">
        <div class="img-box">
          <img src="https://images.unsplash.com/photo-1567401893414-76b7b1e5a7a5?auto=format&fit=crop&w=600&q=80" alt="Navy Blue Lace Abaya">
        </div>
        <div class="abaya-info">
          <h3>Navy Blue Lace Abaya</h3>
        </div>
      </div>

    </div>
  </div>

</body>
</html>
