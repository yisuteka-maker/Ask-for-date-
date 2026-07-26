
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>A Special Question for Namlet ❤️</title>
  
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600;700&family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --primary-color: #ff4b72;
      --secondary-color: #ff758c;
      --bg-gradient: linear-gradient(135deg, #ffdde1 0%, #ee9ca7 100%);
      --card-bg: rgba(255, 255, 255, 0.92);
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      font-family: 'Poppins', sans-serif;
      background: var(--bg-gradient);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow-x: hidden;
      position: relative;
      padding: 15px;
    }

    .bg-animation {
      position: fixed;
      top: 0; left: 0; width: 100%; height: 100%;
      overflow: hidden; z-index: 1; pointer-events: none;
    }

    .floating-heart {
      position: absolute;
      color: rgba(255, 75, 114, 0.4);
      animation: floatUp 8s infinite linear;
    }

    @keyframes floatUp {
      0% { transform: translateY(100vh) scale(0.5) rotate(0deg); opacity: 1; }
      100% { transform: translateY(-10vh) scale(1.2) rotate(360deg); opacity: 0; }
    }

    .card {
      background: var(--card-bg);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 35px 25px;
      text-align: center;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
      width: 100%;
      max-width: 400px;
      z-index: 2;
      transition: all 0.3s ease-in-out;
      border: 1px solid rgba(255, 255, 255, 0.6);
      margin: auto;
    }

    .hidden { display: none !important; }

    /* የልብ ቅርፅ ያለው የርዕስ ማቀፊያ */
    .heart-title-box {
      width: 120px;
      height: 110px;
      background-color: #ffffff;
      position: relative;
      margin: 25px auto 35px auto;
      display: flex;
      justify-content: center;
      align-items: center;
      transform: rotate(-45deg);
      box-shadow: 0 6px 15px rgba(255, 75, 114, 0.3);
    }

    .heart-title-box::before,
    .heart-title-box::after {
      content: "";
      width: 120px;
      height: 110px;
      background-color: #ffffff;
      border-radius: 50%;
      position: absolute;
    }

    .heart-title-box::before { top: -55px; left: 0; }
    .heart-title-box::after { left: 55px; top: 0; }

    .heart-text {
      transform: rotate(45deg);
      z-index: 5;
      color: #000000;
      font-weight: 800;
      font-size: 1.1rem;
      line-height: 1.4;
      text-align: center;
    }

    h1, h2 {
      font-family: 'Dancing Script', cursive;
      color: var(--primary-color);
      margin-bottom: 15px;
    }

    h1 { font-size: 2.6rem; }
    h2 { font-size: 2.1rem; }

    p { color: #444; font-size: 1rem; margin-bottom: 25px; line-height: 1.5; }

    .pulse-heart {
      font-size: 3.5rem;
      animation: pulse 1.5s infinite;
      margin-bottom: 10px;
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.12); }
      100% { transform: scale(1); }
    }

    .btn {
      background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
      color: white; border: none; padding: 12px 28px;
      font-size: 1.05rem; font-weight: 600; border-radius: 30px;
      cursor: pointer; box-shadow: 0 5px 15px rgba(255, 75, 114, 0.3);
      transition: transform 0.2s, background 0.2s;
    }

    .btn:active { transform: scale(0.95); }

    /* አዝራሮች ጎን ለጎን እንዲቀመጡ አስተካክለነዋል */
    .button-group {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 15px;
      position: relative;
      min-height: 60px;
      width: 100%;
    }

    #noBtn {
      background: #777;
      box-shadow: none;
      z-index: 10;
      position: relative;
    }

    .form-group { text-align: left; margin-bottom: 20px; }
    label { display: block; font-size: 0.88rem; color: #333; font-weight: 600; margin-bottom: 6px; }
    input {
      width: 100%; padding: 12px; border: 1px solid #ccc;
      border-radius: 10px; font-family: inherit; font-size: 0.95rem; outline: none;
    }
    input:focus { border-color: var(--primary-color); }
  </style>
</head>
<body>

  <div class="bg-animation" id="bgAnimation"></div>

  <!-- STEP 1 -->
  <div class="card" id="step1">
    <div class="heart-title-box">
      <div class="heart-text">
        from yisu<br>to namlet
      </div>
    </div>
    <div class="pulse-heart">❤️</div>
    <h1>Hey...</h1>
    <p>I have something special for you.</p>
    <button class="btn" onclick="goToStep(2)">I Have a Question</button>
  </div>

  <!-- STEP 2 -->
  <div class="card hidden" id="step2">
    <div style="font-size: 1.8rem; margin-bottom: 10px;">🌹✨🌹</div>
    <h2>Will you go on a date with me?</h2>
    <p>I'd love to spend some quality time together. ❤️</p>
    <div class="button-group">
      <button class="btn" id="yesBtn" onclick="acceptInvitation()">YES!</button>
      <button class="btn" id="noBtn">No</button>
    </div>
  </div>

  <!-- STEP 3 -->
  <div class="card hidden" id="step3">
    <h2>You just made my day! 🥰</h2>
    <p>I can't wait to spend time with you. Choose our date details below:</p>
    
    <!-- Formspree Submit Form -->
    <form action="https://formspree.io/f/yisuteka@gmail.com" method="POST">
      <div class="form-group">
        <label for="date">Select a Date 📅</label>
        <input type="date" id="date" name="Date" required>
      </div>

      <div class="form-group">
        <label for="time">Select a Time ⏰</label>
        <input type="time" id="time" name="Time" required>
      </div>

      <div class="form-group">
        <label for="location">Preferred Meeting Place 📍</label>
        <input type="text" id="location" name="Location" placeholder="e.g. Cafe, Restaurant" required>
      </div>

      <button type="submit" class="btn" style="width: 100%;">Confirm Our Date ✨</button>
    </form>
  </div>

  <script>
    // Background Hearts
    const container = document.getElementById('bgAnimation');
    for (let i = 0; i < 20; i++) {
      const heart = document.createElement('div');
      heart.classList.add('floating-heart');
      heart.innerHTML = '❤️';
      heart.style.left = `${Math.random() * 100}%`;
      heart.style.animationDuration = `${5 + Math.random() * 5}s`;
      heart.style.animationDelay = `${Math.random() * 5}s`;
      heart.style.fontSize = `${12 + Math.random() * 18}px`;
      container.appendChild(heart);
    }

    function goToStep(stepNumber) {
      document.querySelectorAll('.card').forEach(card => card.classList.add('hidden'));
      document.getElementById(`step${stepNumber}`).classList.remove('hidden');
    }

    // "NO" button behavior
    const noBtn = document.getElementById('noBtn');
    function moveNoButton() {
      const x = Math.random() * (window.innerWidth - noBtn.offsetWidth - 40) + 20;
      const y = Math.random() * (window.innerHeight - noBtn.offsetHeight - 40) + 20;
      noBtn.style.position = 'fixed';
      noBtn.style.left = `${x}px`;
      noBtn.style.top = `${y}px`;
    }

    noBtn.addEventListener('mouseover', moveNoButton);
    noBtn.addEventListener('touchstart', (e) => {
      e.preventDefault();
      moveNoButton();
    });

    function acceptInvitation() {
      confetti({ particleCount: 100, spread: 70, origin: { y: 0.6 } });
      const today = new Date().toISOString().split('T')[0];
      document.getElementById('date').setAttribute('min', today);
      goToStep(3);
    }
  </script>
</body>
</html>
