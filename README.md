
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dubai Abaya Fashion</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Arial, sans-serif; }
    body { background-color: #f4f4f9; padding: 15px; color: #333; }
    .container { max-width: 500px; margin: 0 auto; background: #fff; padding: 20px; border-radius: 10px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }
    h1 { text-align: center; font-size: 22px; margin-bottom: 15px; }
    
    /* Product Display */
    .media-box { width: 100%; border-radius: 8px; margin-bottom: 15px; overflow: hidden; }
    .media-box img, .media-box video { width: 100%; display: block; border-radius: 8px; }
    
    .section-title { font-weight: bold; margin: 15px 0 8px; font-size: 14px; }
    .options-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 8px; }
    .btn { padding: 10px; border: 1px solid #ccc; background: #fff; border-radius: 6px; cursor: pointer; text-align: center; font-size: 13px; }
    .btn.selected { border-color: #007bff; background: #e6f0ff; color: #007bff; font-weight: bold; }
    
    /* Interaction Section */
    .interaction-bar { display: flex; align-items: center; justify-content: space-between; margin: 15px 0; padding: 10px 0; border-top: 1px solid #eee; border-bottom: 1px solid #eee; }
    .like-btn { background: #f0f2f5; border: none; padding: 8px 15px; border-radius: 20px; cursor: pointer; font-weight: bold; }
    .like-btn.liked { background: #ffe6e6; color: #e74c3c; }
    
    .whatsapp-btn { display: block; width: 100%; padding: 14px; background: #25D366; color: white; text-align: center; font-weight: bold; text-decoration: none; border-radius: 6px; margin-top: 15px; font-size: 16px; }
    
    .comment-section { margin-top: 20px; }
    .comment-box { width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 6px; margin-bottom: 8px; resize: none; }
    .comment-list { margin-top: 10px; font-size: 13px; max-height: 150px; overflow-y: auto; }
    .comment-item { background: #f9f9f9; padding: 8px; border-radius: 5px; margin-bottom: 5px; border-left: 3px solid #007bff; }
  </style>
</head>
<body>

<div class="container">
  <h1>DUBAI ABAYA FASHION</h1>
  
  <!-- Main Display Media -->
  <div class="media-box" id="media-container">
    <img id="main-image" src="https://srasafayt.github.io/image1.jpg" alt="Dubai Abaya">
  </div>

  <!-- Like Button -->
  <div class="interaction-bar">
    <button class="like-btn" id="like-btn" onclick="toggleLike()">❤️ Like <span id="like-count">0</span></button>
    <span style="font-size: 12px; color: #777;">Dubai Abaya Collection</span>
  </div>

  <!-- Size Selection -->
  <div class="section-title">Select Size:</div>
  <div class="options-grid" id="size-options">
    <button class="btn" onclick="selectOpt('size', this, '52')">52</button>
    <button class="btn" onclick="selectOpt('size', this, '54')">54</button>
    <button class="btn" onclick="selectOpt('size', this, '56')">56</button>
    <button class="btn" onclick="selectOpt('size', this, '58')">58</button>
    <button class="btn" onclick="selectOpt('size', this, '60')">60</button>
    <button class="btn" onclick="selectOpt('size', this, '62')">62</button>
  </div>

  <!-- Color Selection -->
  <div class="section-title">Select Color:</div>
  <div class="options-grid" id="color-options">
    <button class="btn" onclick="selectOpt('color', this, 'Black')">Black</button>
    <button class="btn" onclick="selectOpt('color', this, 'Maroon')">Maroon</button>
    <button class="btn" onclick="selectOpt('color', this, 'Navy Blue')">Navy Blue</button>
    <button class="btn" onclick="selectOpt('color', this, 'Beige')">Beige</button>
    <button class="btn" onclick="selectOpt('color', this, 'Olive Green')">Olive Green</button>
    <button class="btn" onclick="selectOpt('color', this, 'Grey')">Grey</button>
  </div>

  <!-- Order WhatsApp Link -->
  <a id="whatsapp-link" href="#" target="_blank" class="whatsapp-btn" onclick="sendWhatsApp(event)">Order via WhatsApp</a>

  <!-- Comment Section -->
  <div class="comment-section">
    <div class="section-title">Leave a Comment:</div>
    <textarea id="comment-input" class="comment-box" rows="2" placeholder="Write your comment here..."></textarea>
    <button class="btn" style="width: 100%; background: #333; color: white;" onclick="addComment()">Submit Comment</button>
    
    <div class="comment-list" id="comment-list"></div>
  </div>
</div>

<script>
  let selectedSize = '';
  let selectedColor = '';
  let likeCount = 0;
  let isLiked = false;
  const phoneNumber = '971567439129';

  function selectOpt(type, element, value) {
    const buttons = element.parentElement.getElementsByClassName('btn');
    for (let btn of buttons) btn.classList.remove('selected');
    element.classList.add('selected');
    if (type === 'size') selectedSize = value;
    if (type === 'color') selectedColor = value;
  }

  function toggleLike() {
    const likeBtn = document.getElementById('like-btn');
    const likeCountSpan = document.getElementById('like-count');
    if (!isLiked) {
      likeCount++;
      isLiked = true;
      likeBtn.classList.add('liked');
    } else {
      likeCount--;
      isLiked = false;
      likeBtn.classList.remove('liked');
    }
    likeCountSpan.innerText = likeCount;
  }

  function sendWhatsApp(e) {
    if (!selectedSize || !selectedColor) {
      alert('Please select both Size and Color.');
      e.preventDefault();
      return;
    }
    const msg = encodeURIComponent(`Hello Dubai Abaya Fashion,\nI want to order:\nSize: ${selectedSize}\nColor: ${selectedColor}`);
    document.getElementById('whatsapp-link').href = `https://wa.me/${phoneNumber}?text=${msg}`;
  }

  function addComment() {
    const input = document.getElementById('comment-input');
    const text = input.value.trim();
    if (text === '') return;
    
    const commentList = document.getElementById('comment-list');
    const newComment = document.createElement('div');
    newComment.className = 'comment-item';
    newComment.innerText = text;
    commentList.prepend(newComment);
    
    input.value = '';
  }
</script>

</body>
</html>
