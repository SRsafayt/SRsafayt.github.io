
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dubai Abaya Fashion</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Arial, sans-serif; }
    body { background-color: #f4f4f9; padding: 15px; color: #333; }
    .catalog-container { max-width: 600px; margin: 0 auto; }
    h1 { text-align: center; font-size: 24px; margin-bottom: 20px; color: #111; }
    
    .product-card { background: #fff; border-radius: 12px; padding: 18px; margin-bottom: 30px; box-shadow: 0 4px 12px rgba(0,0,0,0.1); }
    .product-img { width: 100%; border-radius: 8px; display: block; margin-bottom: 12px; }
    
    .interaction-bar { display: flex; align-items: center; justify-content: space-between; padding: 10px 0; border-top: 1px solid #eee; border-bottom: 1px solid #eee; margin-bottom: 15px; }
    .like-btn { background: #f0f2f5; border: none; padding: 8px 16px; border-radius: 20px; cursor: pointer; font-weight: bold; }
    .like-btn.liked { background: #ffe6e6; color: #e74c3c; }

    .section-title { font-weight: bold; margin: 15px 0 8px; font-size: 14px; color: #222; border-left: 3px solid #007bff; padding-left: 8px; }
    
    /* Grid Selection with Quantity */
    .selection-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 10px; margin-bottom: 10px; }
    .selection-item { border: 1px solid #e0e0e0; border-radius: 8px; padding: 8px; background: #fafafa; display: flex; align-items: center; justify-content: space-between; }
    .selection-item.active { border-color: #007bff; background: #e6f0ff; }
    .item-label { font-size: 13px; font-weight: 600; }
    
    .qty-controls { display: flex; align-items: center; gap: 5px; }
    .qty-btn { width: 26px; height: 26px; font-size: 14px; font-weight: bold; background: #fff; border: 1px solid #ccc; border-radius: 4px; cursor: pointer; }
    .qty-input { width: 32px; height: 26px; text-align: center; font-size: 13px; font-weight: bold; border: 1px solid #ccc; border-radius: 4px; background: #fff; }

    .whatsapp-btn { display: block; width: 100%; padding: 14px; background: #25D366; color: white; text-align: center; font-weight: bold; text-decoration: none; border-radius: 8px; margin-top: 20px; font-size: 16px; }

    .comment-section { margin-top: 20px; }
    .comment-box { width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 6px; margin-bottom: 8px; resize: none; font-size: 13px; }
    .submit-btn { width: 100%; padding: 8px; background: #333; color: white; border: none; border-radius: 6px; cursor: pointer; font-weight: bold; }
    .comment-list { margin-top: 10px; font-size: 12px; max-height: 120px; overflow-y: auto; }
    .comment-item { background: #f9f9f9; padding: 8px; border-radius: 5px; margin-bottom: 5px; border-left: 3px solid #007bff; }
  </style>
</head>
<body>

<div class="catalog-container">
  <h1>DUBAI ABAYA FASHION</h1>

  <!-- Product Card 1 -->
  <div class="product-card" id="product-1">
    <img src="https://srasafayt.github.io/image1.jpg" alt="Abaya Design 1" class="product-img">

    <div class="interaction-bar">
      <button class="like-btn" onclick="toggleLike(this)">❤️ Like <span class="like-count">0</span></button>
      <span style="font-size: 12px; color: #666;">Design #1</span>
    </div>

    <!-- Color Breakdown Selection -->
    <div class="section-title">Select Color & Quantity:</div>
    <div class="selection-grid color-grid">
      <div class="selection-item">
        <span class="item-label">Black</span>
        <div class="qty-controls">
          <button class="qty-btn" onclick="adjustQty(this, -1)">-</button>
          <input type="number" class="qty-input" value="0" min="0" readonly>
          <button class="qty-btn" onclick="adjustQty(this, 1)">+</button>
        </div>
      </div>
      <div class="selection-item">
        <span class="item-label">Off White</span>
        <div class="qty-controls">
          <button class="qty-btn" onclick="adjustQty(this, -1)">-</button>
          <input type="number" class="qty-input" value="0" min="0" readonly>
          <button class="qty-btn" onclick="adjustQty(this, 1)">+</button>
        </div>
      </div>
      <div class="selection-item">
        <span class="item-label">Navy Blue</span>
        <div class="qty-controls">
          <button class="qty-btn" onclick="adjustQty(this, -1)">-</button>
          <input type="number" class="qty-input" value="0" min="0" readonly>
          <button class="qty-btn" onclick="adjustQty(this, 1)">+</button>
        </div>
      </div>
      <div class="selection-item">
        <span class="item-label">Maroon</span>
        <div class="qty-controls">
          <button class="qty-btn" onclick="adjustQty(this, -1)">-</button>
          <input type="number" class="qty-input" value="0" min="0" readonly>
          <button class="qty-btn" onclick="adjustQty(this, 1)">+</button>
        </div>
      </div>
    </div>

    <!-- Size Breakdown Selection -->
    <div class="section-title">Select Size & Quantity:</div>
    <div class="selection-grid size-grid">
      <div class="selection-item">
        <span class="item-label">Size 52</span>
        <div class="qty-controls">
          <button class="qty-btn" onclick="adjustQty(this, -1)">-</button>
          <input type="number" class="qty-input" value="0" min="0" readonly>
          <button class="qty-btn" onclick="adjustQty(this, 1)">+</button>
        </div>
      </div>
      <div class="selection-item">
        <span class="item-label">Size 54</span>
        <div class="qty-controls">
          <button class="qty-btn" onclick="adjustQty(this, -1)">-</button>
          <input type="number" class="qty-input" value="0" min="0" readonly>
          <button class="qty-btn" onclick="adjustQty(this, 1)">+</button>
        </div>
      </div>
      <div class="selection-item">
        <span class="item-label">Size 56</span>
        <div class="qty-controls">
          <button class="qty-btn" onclick="adjustQty(this, -1)">-</button>
          <input type="number" class="qty-input" value="0" min="0" readonly>
          <button class="qty-btn" onclick="adjustQty(this, 1)">+</button>
        </div>
      </div>
      <div class="selection-item">
        <span class="item-label">Size 58</span>
        <div class="qty-controls">
          <button class="qty-btn" onclick="adjustQty(this, -1)">-</button>
          <input type="number" class="qty-input" value="0" min="0" readonly>
          <button class="qty-btn" onclick="adjustQty(this, 1)">+</button>
        </div>
      </div>
      <div class="selection-item">
        <span class="item-label">Size 60</span>
        <div class="qty-controls">
          <button class="qty-btn" onclick="adjustQty(this, -1)">-</button>
          <input type="number" class="qty-input" value="0" min="0" readonly>
          <button class="qty-btn" onclick="adjustQty(this, 1)">+</button>
        </div>
      </div>
      <div class="selection-item">
        <span class="item-label">Size 62</span>
        <div class="qty-controls">
          <button class="qty-btn" onclick="adjustQty(this, -1)">-</button>
          <input type="number" class="qty-input" value="0" min="0" readonly>
          <button class="qty-btn" onclick="adjustQty(this, 1)">+</button>
        </div>
      </div>
    </div>

    <!-- WhatsApp Order Link -->
    <a href="#" target="_blank" class="whatsapp-btn" onclick="sendWhatsAppOrder(event, 'product-1', 'Design 1')">Order via WhatsApp</a>

    <!-- Comments -->
    <div class="comment-section">
      <div class="section-title">Leave a Comment:</div>
      <textarea class="comment-box" rows="2" placeholder="Write a comment about this design..."></textarea>
      <button class="submit-btn" onclick="addComment(this)">Submit Comment</button>
      <div class="comment-list"></div>
    </div>
  </div>

</div>

<script>
  const phoneNumber = '971567439129';

  function adjustQty(button, change) {
    const container = button.parentElement;
    const input = container.querySelector('.qty-input');
    const wrapper = container.closest('.selection-item');
    let val = parseInt(input.value) || 0;
    val = Math.max(0, val + change);
    input.value = val;

    if (val > 0) {
      wrapper.classList.add('active');
    } else {
      wrapper.classList.remove('active');
    }
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

  function sendWhatsAppOrder(event, cardId, designName) {
    const card = document.getElementById(cardId);
    
    // Collect Colors
    let colorDetails = [];
    card.querySelectorAll('.color-grid .selection-item').forEach(item => {
      const label = item.querySelector('.item-label').innerText;
      const qty = parseInt(item.querySelector('.qty-input').value) || 0;
      if (qty > 0) {
        colorDetails.push(`${label}: ${qty} Pcs`);
      }
    });

    // Collect Sizes
    let sizeDetails = [];
    card.querySelectorAll('.size-grid .selection-item').forEach(item => {
      const label = item.querySelector('.item-label').innerText;
      const qty = parseInt(item.querySelector('.qty-input').value) || 0;
      if (qty > 0) {
        sizeDetails.push(`${label}: ${qty} Pcs`);
      }
    });

    if (colorDetails.length === 0 || sizeDetails.length === 0) {
      alert('Please select at least one Color quantity and one Size quantity!');
      event.preventDefault();
      return;
    }

    let messageText = `Hello Dubai Abaya Fashion,\nI want to place an order for *${designName}*:\n\n*Colors Ordered:*\n- ${colorDetails.join('\n- ')}\n\n*Sizes Ordered:*\n- ${sizeDetails.join('\n- ')}`;

    event.target.href = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(messageText)}`;
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
