
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dubai Abaya Fashion Catalog</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Arial, sans-serif; }
    body { background-color: #f4f4f9; padding: 15px; color: #333; }
    .catalog-container { max-width: 600px; margin: 0 auto; }
    h1 { text-align: center; font-size: 24px; margin-bottom: 20px; color: #222; }
    
    /* Product Card */
    .product-card { background: #fff; border-radius: 10px; padding: 15px; margin-bottom: 25px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }
    .product-img { width: 100%; border-radius: 8px; display: block; margin-bottom: 12px; }
    
    /* Interaction Bar */
    .interaction-bar { display: flex; align-items: center; justify-content: space-between; padding: 8px 0; border-top: 1px solid #eee; border-bottom: 1px solid #eee; margin-bottom: 12px; }
    .like-btn { background: #f0f2f5; border: none; padding: 8px 15px; border-radius: 20px; cursor: pointer; font-weight: bold; }
    .like-btn.liked { background: #ffe6e6; color: #e74c3c; }

    /* Selection Fields */
    .section-title { font-weight: bold; margin: 10px 0 5px; font-size: 13px; color: #555; }
    .options-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 6px; }
    .btn { padding: 8px; border: 1px solid #ccc; background: #fff; border-radius: 6px; cursor: pointer; text-align: center; font-size: 13px; }
    .btn.selected { border-color: #007bff; background: #e6f0ff; color: #007bff; font-weight: bold; }

    /* Quantity Input */
    .qty-container { display: flex; align-items: center; gap: 8px; margin-top: 5px; }
    .qty-btn { width: 35px; height: 35px; font-size: 16px; font-weight: bold; background: #f0f2f5; border: 1px solid #ccc; border-radius: 6px; cursor: pointer; }
    .qty-input { width: 50px; height: 35px; text-align: center; font-size: 15px; font-weight: bold; border: 1px solid #ccc; border-radius: 6px; }

    /* WhatsApp Button */
    .whatsapp-btn { display: block; width: 100%; padding: 12px; background: #25D366; color: white; text-align: center; font-weight: bold; text-decoration: none; border-radius: 6px; margin-top: 15px; font-size: 15px; }

    /* Comment Section */
    .comment-section { margin-top: 15px; }
    .comment-box { width: 100%; padding: 8px; border: 1px solid #ccc; border-radius: 6px; margin-bottom: 6px; resize: none; font-size: 13px; }
    .comment-list { margin-top: 8px; font-size: 12px; max-height: 120px; overflow-y: auto; }
    .comment-item { background: #f9f9f9; padding: 6px 10px; border-radius: 5px; margin-bottom: 4px; border-left: 3px solid #007bff; }
  </style>
</head>
<body>

<div class="catalog-container">
  <h1>DUBAI ABAYA FASHION</h1>

  <!-- Product 1 -->
  <div class="product-card" id="product-1">
    <img src="https://srasafayt.github.io/image1.jpg" alt="Dubai Abaya Design 1" class="product-img">

    <!-- Like Button -->
    <div class="interaction-bar">
      <button class="like-btn" onclick="toggleLike(this)">❤️ Like <span class="like-count">0</span></button>
      <span style="font-size: 12px; color: #777;">Design #1</span>
    </div>

    <!-- Size Selection (52 to 62) -->
    <div class="section-title">Which Size:</div>
    <div class="options-grid size-options">
      <button class="btn" onclick="selectOpt(this, 'size')">52</button>
      <button class="btn" onclick="selectOpt(this, 'size')">54</button>
      <button class="btn" onclick="selectOpt(this, 'size')">56</button>
      <button class="btn" onclick="selectOpt(this, 'size')">58</button>
      <button class="btn" onclick="selectOpt(this, 'size')">60</button>
      <button class="btn" onclick="selectOpt(this, 'size')">62</button>
    </div>

    <!-- Color Selection -->
    <div class="section-title">Which Color:</div>
    <div class="options-grid color-options">
      <button class="btn" onclick="selectOpt(this, 'color')">Black</button>
      <button class="btn" onclick="selectOpt(this, 'color')">Maroon</button>
      <button class="btn" onclick="selectOpt(this, 'color')">Navy Blue</button>
      <button class="btn" onclick="selectOpt(this, 'color')">Beige</button>
      <button class="btn" onclick="selectOpt(this, 'color')">Olive Green</button>
      <button class="btn" onclick="selectOpt(this, 'color')">Grey</button>
    </div>

    <!-- How Many Pieces (Quantity) -->
    <div class="section-title">How Many Pieces:</div>
    <div class="qty-container">
      <button class="qty-btn" onclick="updateQty(this, -1)">-</button>
      <input type="number" class="qty-input" value="1" min="1" readonly>
      <button class="qty-btn" onclick="updateQty(this, 1)">+</button>
    </div>

    <!-- Order via WhatsApp -->
    <a href="#" target="_blank" class="whatsapp-btn" onclick="sendWhatsApp(event, 'product-1', 'Design 1')">Order via WhatsApp</a>

    <!-- Comments -->
    <div class="comment-section">
      <div class="section-title">Leave a Comment:</div>
      <textarea class="comment-box" rows="2" placeholder="Write a comment about this design..."></textarea>
      <button class="btn" style="width: 100%; background: #333; color: white;" onclick="addComment(this)">Submit Comment</button>
      <div class="comment-list"></div>
    </div>
  </div>

</div>

<script>
  const phoneNumber = '971567439129';

  function selectOpt(element, type) {
    const parent = element.parentElement;
    const buttons = parent.getElementsByClassName('btn');
    for (let btn of buttons) btn.classList.remove('selected');
    element.classList.add('selected');
  }

  function updateQty(element, change) {
    const container = element.parentElement;
    const input = container.querySelector('.qty-input');
    let currentQty = parseInt(input.value) || 1;
    currentQty = Math.max(1, currentQty + change);
    input.value = currentQty;
  }

  function toggleLike(btn) {
    const countSpan = btn.querySelector('.like-count');
    let count = parseInt(countSpan.innerText) || 0;
    if (btn.classList.contains('liked')) {
      btn.classList.remove('liked');
      countSpan.innerText = count - 1;
    } else {
      btn.classList.add('liked');
      countSpan.innerText = count + 1;
    }
  }

  function sendWhatsApp(event, cardId, designName) {
    const card = document.getElementById(cardId);
    const selectedSizeBtn = card.querySelector('.size-options .btn.selected');
    const selectedColorBtn = card.querySelector('.color-options .btn.selected');
    const qty = card.querySelector('.qty-input').value;

    if (!selectedSizeBtn || !selectedColorBtn) {
      alert('Please select both Size and Color before ordering!');
      event.preventDefault();
      return;
    }

    const size = selectedSizeBtn.innerText;
    const color = selectedColorBtn.innerText;

    const message = encodeURIComponent(`Hello Dubai Abaya Fashion,\nI want to order:\n- Item: ${designName}\n- Size: ${size}\n- Color: ${color}\n- Quantity: ${qty} Pcs`);
    event.target.href = `https://wa.me/${phoneNumber}?text=${message}`;
  }

  function addComment(btn) {
    const section = btn.parentElement;
    const input = section.querySelector('.comment-box');
    const text = input.value.trim();
    if (text === '') return;

    const commentList = section.querySelector('.comment-list');
    const newComment = document.createElement('div');
    newComment.className = 'comment-item';
    newComment.innerText = text;
    commentList.prepend(newComment);

    input.value = '';
  }
</script>

</body>
</html>
