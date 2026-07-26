
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>A Special Question for Namlet ❤️</title>
  
  <!-- Canvas Confetti Library -->
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
  
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600;700&family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --primary-color: #ff4b72;
      --secondary-color: #ff758c;
      --bg-gradient: linear-gradient(135deg, #ffdde1 0%, #ee9ca7 100%);
      --card-bg: rgba(255, 255, 255, 0.85);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: var(--bg-gradient);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow-x: hidden;
      position: relative;
    }

    /* Floating Background Animations */
    .bg-animation {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      overflow: hidden;
      z-index: 1;
      pointer-events: none;
    }

    .floating-heart {
      position: absolute;
      color: rgba(255, 75, 114, 0.4);
      animation: floatUp 8s infinite linear;
    }

    @keyframes floatUp {
      0% {
        transform: translateY(100vh) scale(0.5) rotate(0deg);
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) scale(1.2) rotate(360deg);
        opacity: 0;
      }
    }

    /* Glassmorphism Containers */
    .card {
      background: var(--card-bg);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 35px 25px;
      text-align: center;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
      width: 90%;
      max-width: 450px;
      z-index: 2;
      transition: all 0.5s ease-in-out;
      border: 1px solid rgba(255, 255, 255, 0.5);
    }

    .hidden {
      display: none !important;
    }

    /* የልብ ቅርፅ ያለው የርዕስ ማቀፊያ (Heart-shaped Title Container) */
    .heart-title-box {
      width: 130px;
      height: 120px;
      background-color: rgba(255, 255, 255, 0.95);
      position: relative;
      margin: 0 auto 25px auto;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      transform: rotate(-45deg);
      box-shadow: 0 5px 15px rgba(255, 75, 114, 0.25);
    }

    .heart-title-box::before,
    .heart-title-box::after {
      content: "";
      width: 130px;
      height: 120px;
      background-color: rgba(255, 255, 255, 0.95);
      border-radius: 50%;
      position: absolute;
    }

    .heart-title-box::before {
      top: -60px;
      left: 0;
    }

    .heart-title-box::after {
      left: 60px;
      top: 0;
    }

    /* በጥቁር እና ጎልቶ የተጻፈው ጽሁፍ (Bold Black Text) */
    .heart-text {
      transform: rotate(45deg); /* ጽሁፉ እንዳያደላድል የማስተካከያ */
      z-index: 5;
      color: #000000;
      font-weight: 700;
      font-size: 1.15rem;
      line-height: 1.4;
      text-align: center;
    }

    /* Typography */
    h1, h2 {
      font-family: 'Dancing Script', cursive;
      color: var(--primary-color);
      margin-bottom: 15px;
    }

    h1 { font-size: 2.8rem; }
    h2 { font-size: 2.2rem; }

    p {
      color: #555;
      font-size: 1.05rem;
      margin-bottom: 25px;
      line-height: 1.5;
    }

    .pulse-heart {
      font-size: 3.5rem;
      animation: pulse 1.5s infinite;
      margin-bottom: 10px;
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.15); }
      100% { transform: scale(1); }
    }

    /* Buttons */
    .btn {
      background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
      color: white;
      border: none;
      padding: 12px 28px;
      font-size: 1.1rem;
      font-weight: 600;
      border-radius: 30px;
      cursor: pointer;
      box-shadow: 0 5px 15px rgba(255, 75, 114, 0.3);
      transition: transform 0.2s;
    }

    .btn:hover {
      transform: translateY(-2px);
    }

    .button-group {
      display: flex;
      justify-content: center;
      gap: 20px;
      position: relative;
      min-height: 50px;
    }

    #noBtn {
      background: #888;
      box-shadow: none;
      position: absolute;
      transition: all 0.2s ease;
    }

    /* Form Styling */
    .form-group {
      text-align: left;
      margin-bottom: 20px;
    }

    label {
      display: block;
      font-size: 0.9rem;
      color: #444;
      font-weight: 600;
      margin-bottom: 5px;
    }

    input {
      width: 100%;
      padding: 12px;
      border: 1px solid #ddd;
      border-radius: 10px;
      font-family: inherit;
      font-size: 0.95rem;
      outline: none;
    }

    input:focus {
      border-color: var(--primary-color);
    }
  </style>
</head>
<body>

  <!-- Floating Hearts Background -->
  <div class="bg-animation" id="bgAnimation"></div>

  <!-- STEP 1: Welcome Screen -->
  <div class="card" id="step1">
    
    <!-- Heart Title Box (በልብ ቅርፅ ውስጥ ጥቁር ጎልቶ የወጣ ጽሁፍ) -->
    <div class="heart-title-box">
      <div class="heart-text">
        for yisu <br>ti namlet
      </div>
    </div>

    <div class="pulse-heart">❤️</div>
    <h1>Hey...</h1>
    <p>I have something special for you.</p>
    <button class="btn" onclick="goToStep(2)">I Have a Question</button>
  </div>

  <!-- STEP 2: The Question -->
  <div class="card hidden" id="step2">
    <div style="font-size: 1.8rem; margin-bottom: 10px;">🌹✨🌹</div>
    <h2>Will you go on a date with me?</h2>
    <p>I'd love to spend some quality time together. ❤️</p>
    <div class="button-group">
      <button class="btn" id="yesBtn" onclick="acceptInvitation()">YES!</button>
      <button class="btn" id="noBtn">No</button>
    </div>
  </div>

  <!-- STEP 3: Date Details Form (Email Submission) -->
  <div class="card hidden" id="step3">
    <h2>You just made my day! 🥰</h2>
    <p>I can't wait to spend time with you. Choose our date details below:</p>
    
    <form id="dateForm" action="https://formspree.io/f/yisuteka@gmail.com" method="POST" onsubmit="submitDetails(event)">
      <div class="form-group">
        <label for="date">Select a Date 📅</label>
        <input type="date" id="date" name="Preferred Date" required>
      </div>

      <div class="form-group">
        <label for="time">Select a Time ⏰</label>
        <input type="time" id="time" name="Preferred Time" required>
      </div>

      <div class="form-group">
        <label for="location">Preferred Meeting Place 📍</label>
        <input type="text" id="location" name="Preferred Place" placeholder="e.g., Favorite Cafe, Restaurant" required>
      </div>

      <button type="submit" class="btn" style="width: 100%;">Confirm Our Date ✨</button>
    </form>
  </div>

  <!-- STEP 4: Thank You Screen -->
  <div class="card hidden" id="step4">
    <div class="pulse-heart">💖</div>
    <h2>It's a Date!</h2>
    <p>Thank you! Your choices have been sent. Get ready for a wonderful time together! 🌹</p>
  </div>

  <script>
    // Floating Background Hearts
    const container = document.getElementById('bgAnimation');
    for (let i = 0; i < 25; i++) {
      const heart = document.createElement('div');
      heart.classList.add('floating-heart');
      heart.innerHTML = '❤️';
      heart.style.left = `${Math.random() * 100}%`;
      heart.style.animationDuration = `${5 + Math.random() * 5}s`;
      heart.style.animationDelay = `${Math.random() * 5}s`;
      heart.style.fontSize = `${12 + Math.random() * 20}px`;
      container.appendChild(heart);
    }

    // Step Navigation
    function goToStep(stepNumber) {
      document.querySelectorAll('.card').forEach(card => card.classList.add('hidden'));
      document.getElementById(`step${stepNumber}`).classList.remove('hidden');
    }

    // Playful Move Away "NO" Button
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

    // Accept Action
    function acceptInvitation() {
      confetti({
        particleCount: 100,
        spread: 70,
        origin: { y: 0.6 }
      });

      const today = new Date().toISOString().split('T')[0];
      document.getElementById('date').setAttribute('min', today);

      goToStep(3);
    }

    // Email Submission via Formspree
    function submitDetails(event) {
      event.preventDefault();
      const form = event.target;
      const formData = new FormData(form);

      fetch(form.action, {
        method: 'POST',
        body: formData,
        headers: {
          'Accept': 'application/json'
        }
      }).then(response => {
        goToStep(4);
      }).catch(error => {
        goToStep(4);
      });
    }
  </script>
</body>
</html>
