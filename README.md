<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Dharshini! 🎀</title>
<link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Pacifico&family=Nunito:wght@400;600;700&display=swap" rel="stylesheet">
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --pink-light: #fff0f5;
    --pink-mid: #ffb6d9;
    --pink-hot: #ff69b4;
    --pink-deep: #e91e8c;
    --purple: #c084fc;
    --gold: #ffd700;
    --text-dark: #5c1a4a;
  }

  body {
    font-family: 'Nunito', sans-serif;
    background: var(--pink-light);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ===== FLOATING HEARTS BG ===== */
  .hearts-bg {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    pointer-events: none; z-index: 0; overflow: hidden;
  }
  .heart-float {
    position: absolute;
    font-size: 1.2rem;
    animation: floatUp linear infinite;
    opacity: 0.15;
  }
  @keyframes floatUp {
    0% { transform: translateY(110vh) rotate(0deg); opacity: 0.15; }
    100% { transform: translateY(-10vh) rotate(360deg); opacity: 0; }
  }

  /* ===== SCREENS ===== */
  .screen {
    display: none;
    position: relative;
    z-index: 1;
    min-height: 100vh;
    width: 100%;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 30px 20px;
    animation: fadeIn 0.8s ease;
  }
  .screen.active { display: flex; }
  @keyframes fadeIn {
    from { opacity: 0; transform: scale(0.95); }
    to { opacity: 1; transform: scale(1); }
  }

  /* ===== SCREEN 1 - LOADER ===== */
  #screen1 {
    background: linear-gradient(135deg, #fff0f5 0%, #ffe4f0 100%);
  }
  .loader-ring {
    width: 70px; height: 70px;
    border: 5px solid var(--pink-mid);
    border-top-color: var(--pink-deep);
    border-radius: 50%;
    animation: spin 1s linear infinite;
    margin-bottom: 20px;
  }
  @keyframes spin { to { transform: rotate(360deg); } }
  .loader-text {
    font-family: 'Dancing Script', cursive;
    font-size: 1.6rem;
    color: var(--pink-deep);
    text-align: center;
  }
  .kitty-img { width: 80px; margin-bottom: 10px; }

  /* ===== SCREEN 2 - INTRO ===== */
  #screen2 {
    background: linear-gradient(160deg, #fff0f5 0%, #fce4f3 100%);
    text-align: center;
  }
  .intro-kitty { font-size: 5rem; margin-bottom: 10px; animation: bounce 1.2s ease infinite; }
  @keyframes bounce {
    0%,100% { transform: translateY(0); }
    50% { transform: translateY(-12px); }
  }
  .intro-title {
    font-family: 'Pacifico', cursive;
    font-size: 1.9rem;
    color: var(--pink-deep);
    margin-bottom: 8px;
    line-height: 1.3;
  }
  .intro-sub {
    font-family: 'Dancing Script', cursive;
    font-size: 1.1rem;
    color: #a0547e;
    margin-bottom: 25px;
  }
  .btn-pink {
    background: linear-gradient(135deg, var(--pink-hot), var(--pink-deep));
    color: white;
    border: none;
    padding: 14px 35px;
    border-radius: 50px;
    font-size: 1rem;
    font-family: 'Nunito', sans-serif;
    font-weight: 700;
    cursor: pointer;
    box-shadow: 0 6px 20px rgba(233,30,140,0.35);
    transition: transform 0.2s, box-shadow 0.2s;
    display: flex; align-items: center; gap: 8px;
  }
  .btn-pink:hover { transform: scale(1.05); box-shadow: 0 8px 25px rgba(233,30,140,0.5); }

  /* ===== SCREEN 3 - CAKE ===== */
  #screen3 {
    background: linear-gradient(160deg, #fff0f5, #fce4f3);
    text-align: center;
  }
  .cake-emoji { font-size: 5rem; animation: wiggle 1s ease infinite; }
  @keyframes wiggle {
    0%,100% { transform: rotate(-5deg); }
    50% { transform: rotate(5deg); }
  }
  .cake-text {
    font-family: 'Dancing Script', cursive;
    font-size: 1.5rem;
    color: var(--pink-deep);
    margin: 15px 0 5px;
  }
  .cake-sub { color: #a0547e; font-size: 0.9rem; margin-bottom: 20px; }
  .swipe-area {
    width: 260px; height: 260px;
    background: linear-gradient(135deg, #ffb6d9, #ff85c0);
    border-radius: 20px;
    display: flex; align-items: center; justify-content: center;
    font-size: 4rem;
    cursor: pointer;
    box-shadow: 0 10px 30px rgba(255,105,180,0.4);
    transition: transform 0.1s;
    user-select: none;
    position: relative; overflow: hidden;
    border: 3px solid white;
  }
  .swipe-area:active { transform: scale(0.97); }
  .cut-line {
    position: absolute; top: 0; height: 100%; width: 3px;
    background: rgba(255,255,255,0.9);
    left: -10px; pointer-events: none;
    transition: left 0.1s;
  }
  .candles { position: absolute; top: 10px; font-size: 1.8rem; }

  /* ===== SCREEN 4 - PHOTOS ===== */
  #screen4 {
    background: linear-gradient(160deg, #fff0f5, #fce4f3);
    text-align: center;
  }
  .photos-title {
    font-family: 'Dancing Script', cursive;
    font-size: 1.8rem;
    color: var(--pink-deep);
    margin-bottom: 20px;
  }
  .photo-carousel {
    width: 280px; height: 320px;
    position: relative; margin-bottom: 25px;
  }
  .photo-card {
    position: absolute; top: 0; left: 0;
    width: 100%; height: 100%;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 10px 30px rgba(233,30,140,0.25);
    transition: opacity 0.6s, transform 0.6s;
    background: linear-gradient(135deg, #ffb6d9, #e991c8);
    display: flex; align-items: center; justify-content: center;
    font-size: 6rem;
    border: 4px solid white;
  }
  .photo-card.hidden { opacity: 0; transform: scale(0.9); }

  /* ===== SCREEN 5 - MESSAGE ===== */
  #screen5 {
    background: linear-gradient(160deg, #fff0f5, #fce4f3);
    text-align: center;
  }
  .msg-title {
    font-family: 'Pacifico', cursive;
    font-size: 1.5rem;
    color: var(--pink-deep);
    margin-bottom: 20px;
  }
  .msg-card {
    background: white;
    border-radius: 20px;
    padding: 25px 20px;
    max-width: 360px;
    box-shadow: 0 10px 30px rgba(233,30,140,0.15);
    border: 2px solid var(--pink-mid);
    font-family: 'Dancing Script', cursive;
    font-size: 1.15rem;
    color: var(--text-dark);
    line-height: 1.8;
    position: relative;
  }
  .msg-card::before {
    content: '💌';
    font-size: 2rem;
    display: block;
    margin-bottom: 10px;
  }

  /* ===== SCREEN 6 - FINAL ===== */
  #screen6 {
    background: linear-gradient(160deg, #fff0f5, #fce4f3);
    text-align: center;
  }
  .final-title {
    font-family: 'Pacifico', cursive;
    font-size: 2.2rem;
    color: var(--pink-deep);
    margin-bottom: 5px;
    animation: pulse 1.5s ease infinite;
  }
  @keyframes pulse {
    0%,100% { transform: scale(1); }
    50% { transform: scale(1.04); }
  }
  .confetti-emoji { font-size: 3rem; margin: 10px 0; }
  .final-sub {
    font-family: 'Dancing Script', cursive;
    font-size: 1.3rem;
    color: #a0547e;
    margin-bottom: 25px;
  }
  .balloons { font-size: 3rem; animation: float 2s ease-in-out infinite; }
  @keyframes float {
    0%,100% { transform: translateY(0); }
    50% { transform: translateY(-15px); }
  }
  .fireworks {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    pointer-events: none; z-index: 999;
  }
  .spark {
    position: absolute;
    width: 8px; height: 8px;
    border-radius: 50%;
    animation: burst 1.2s ease-out forwards;
  }
  @keyframes burst {
    0% { transform: translate(0,0) scale(1); opacity: 1; }
    100% { transform: translate(var(--dx), var(--dy)) scale(0); opacity: 0; }
  }

  /* ===== PROGRESS DOTS ===== */
  .dots {
    display: flex; gap: 8px; margin-top: 30px;
  }
  .dot {
    width: 10px; height: 10px; border-radius: 50%;
    background: var(--pink-mid); transition: background 0.3s, transform 0.3s;
  }
  .dot.active { background: var(--pink-deep); transform: scale(1.3); }

  /* SPARKLES */
  .sparkle {
    display: inline-block;
    animation: sparkleAnim 1.5s ease-in-out infinite;
  }
  @keyframes sparkleAnim {
    0%,100% { transform: rotate(0deg) scale(1); }
    50% { transform: rotate(20deg) scale(1.2); }
  }
</style>
</head>
<body>

<!-- Floating hearts background -->
<div class="hearts-bg" id="heartsbg"></div>

<!-- SCREEN 1: Loader -->
<div class="screen active" id="screen1">
  <div style="text-align:center">
    <div style="font-size:4rem; margin-bottom:10px;">🎀</div>
    <div class="loader-ring"></div>
    <div class="loader-text">Loading your birthday surprise...</div>
    <div style="margin-top:10px; color:#c084fc; font-size:0.85rem;">Just for you, Dharshini 💕</div>
  </div>
</div>

<!-- SCREEN 2: Intro -->
<div class="screen" id="screen2">
  <div class="intro-kitty">🎂</div>
  <div class="intro-title">My girl was born<br>18 years ago today!</div>
  <div class="intro-sub">Yes, it's YOU! ✨ A little surprise awaits...</div>
  <button class="btn-pink" onclick="goTo(3)">🎁 Start the Surprise</button>
  <div class="dots">
    <div class="dot active"></div>
    <div class="dot"></div>
    <div class="dot"></div>
    <div class="dot"></div>
    <div class="dot"></div>
  </div>
</div>

<!-- SCREEN 3: Cut the Cake -->
<div class="screen" id="screen3">
  <div class="cake-text">Swipe anywhere</div>
  <div style="font-family:'Dancing Script',cursive; color:var(--pink-deep); font-size:1.3rem; margin-bottom:5px;">to cut the cake!</div>
  <div style="color:#a0547e; font-size:0.85rem; margin-bottom:20px;">Dharshini's special birthday cake 🎂</div>
  <div class="swipe-area" id="cakeArea" onmousedown="startCut(event)" ontouchstart="startCut(event)">
    <span class="candles">🕯️🕯️</span>
    🎂
    <div class="cut-line" id="cutLine"></div>
  </div>
  <div style="margin-top:15px; color:#a0547e; font-size:0.85rem;">Drag across the cake ✂️</div>
  <div class="dots">
    <div class="dot"></div>
    <div class="dot active"></div>
    <div class="dot"></div>
    <div class="dot"></div>
    <div class="dot"></div>
  </div>
</div>

<!-- SCREEN 4: Sweet Moments / Photos -->
<div class="screen" id="screen4">
  <div class="photos-title">💕 Some Sweet Moments</div>
  <div class="photo-carousel">
    <div class="photo-card" id="card0">🌸</div>
    <div class="photo-card hidden" id="card1">🌷</div>
    <div class="photo-card hidden" id="card2">🦋</div>
    <div class="photo-card hidden" id="card3">✨</div>
  </div>
  <div style="color:#a0547e; font-size:0.85rem; margin-bottom:15px;">Tap to flip through moments 💖</div>
  <button class="btn-pink" onclick="goTo(5)">💌 Open My Message</button>
  <div class="dots">
    <div class="dot"></div>
    <div class="dot"></div>
    <div class="dot active"></div>
    <div class="dot"></div>
    <div class="dot"></div>
  </div>
</div>

<!-- SCREEN 5: Message -->
<div class="screen" id="screen5">
  <div class="msg-title">A Special Message 💌</div>
  <div class="msg-card">
    Happy Birthday, My Dharshini! 🎀<br><br>
    You deserve all the happiness, love, and smiles in the world today and always. The way you make people around you feel is truly one of a kind. Your smile lights up everything 🌟<br><br>
    You're officially 18 now — the world better be ready for you! 🌸<br><br>
    Keep being the amazing girl you are. Wishing you endless joy, laughter, and all the sweet things life has to offer. 💕<br><br>
    — Always yours 🎂
  </div>
  <button class="btn-pink" style="margin-top:25px;" onclick="goTo(6)">🎉 See the Finale!</button>
  <div class="dots">
    <div class="dot"></div>
    <div class="dot"></div>
    <div class="dot"></div>
    <div class="dot active"></div>
    <div class="dot"></div>
  </div>
</div>

<!-- SCREEN 6: Final -->
<div class="screen" id="screen6">
  <div class="balloons">🎈🎈🎈</div>
  <div class="confetti-emoji">🎊✨🎊</div>
  <div class="final-title">Happy Birthday<br>Dharshini! 🎀</div>
  <div class="final-sub">18 & absolutely wonderful 💖</div>
  <div style="font-size:3rem; margin:10px 0;">🌸🦋🌷</div>
  <div style="color:#a0547e; font-family:'Dancing Script',cursive; font-size:1.1rem; max-width:300px;">
    May this year bring you everything your heart desires 💕
  </div>
  <button class="btn-pink" style="margin-top:25px;" onclick="launchFireworks()">🎆 Launch Fireworks!</button>
  <div class="dots">
    <div class="dot"></div>
    <div class="dot"></div>
    <div class="dot"></div>
    <div class="dot"></div>
    <div class="dot active"></div>
  </div>
</div>

<!-- Fireworks container -->
<div class="fireworks" id="fireworks"></div>

<script>
// ===== FLOATING HEARTS =====
const heartsContainer = document.getElementById('heartsbg');
const emojis = ['💕','🌸','✨','🎀','💖','🌷','🦋','⭐','💗'];
for (let i = 0; i < 18; i++) {
  const h = document.createElement('div');
  h.className = 'heart-float';
  h.textContent = emojis[Math.floor(Math.random() * emojis.length)];
  h.style.left = Math.random() * 100 + 'vw';
  h.style.animationDuration = (6 + Math.random() * 8) + 's';
  h.style.animationDelay = (Math.random() * 8) + 's';
  h.style.fontSize = (0.8 + Math.random() * 1.2) + 'rem';
  heartsContainer.appendChild(h);
}

// ===== SCREEN NAV =====
let currentScreen = 1;
function goTo(n) {
  document.getElementById('screen'+currentScreen).classList.remove('active');
  currentScreen = n;
  document.getElementById('screen'+n).classList.add('active');
}

// ===== AUTO LOADER =====
setTimeout(() => goTo(2), 2500);

// ===== CAKE CUT =====
let cutting = false;
let cakeProgress = 0;
function startCut(e) {
  cutting = true;
  moveCut(e);
}
function moveCut(e) {
  if (!cutting) return;
  const area = document.getElementById('cakeArea');
  const rect = area.getBoundingClientRect();
  const clientX = e.touches ? e.touches[0].clientX : e.clientX;
  const x = clientX - rect.left;
  const pct = Math.max(0, Math.min(100, (x / rect.width) * 100));
  document.getElementById('cutLine').style.left = pct + '%';
  cakeProgress = pct;
  if (pct > 70) {
    setTimeout(() => goTo(4), 500);
    cutting = false;
  }
}
function stopCut() { cutting = false; }
document.addEventListener('mousemove', moveCut);
document.addEventListener('mouseup', stopCut);
document.addEventListener('touchmove', moveCut);
document.addEventListener('touchend', stopCut);

// ===== PHOTO CAROUSEL =====
let currentCard = 0;
document.addEventListener('click', function(e) {
  if (currentScreen === 4) {
    const cards = document.querySelectorAll('.photo-card');
    cards[currentCard].classList.add('hidden');
    currentCard = (currentCard + 1) % cards.length;
    cards[currentCard].classList.remove('hidden');
  }
});

// ===== FIREWORKS =====
function launchFireworks() {
  const fw = document.getElementById('fireworks');
  const colors = ['#ff69b4','#ffb6d9','#c084fc','#ffd700','#ff1493','#87ceeb'];
  for (let i = 0; i < 8; i++) {
    setTimeout(() => {
      const cx = 10 + Math.random() * 80;
      const cy = 10 + Math.random() * 60;
      for (let j = 0; j < 14; j++) {
        const spark = document.createElement('div');
        spark.className = 'spark';
        spark.style.left = cx + 'vw';
        spark.style.top = cy + 'vh';
        spark.style.background = colors[Math.floor(Math.random() * colors.length)];
        const angle = (j / 14) * Math.PI * 2;
        const dist = 60 + Math.random() * 80;
        spark.style.setProperty('--dx', Math.cos(angle)*dist + 'px');
        spark.style.setProperty('--dy', Math.sin(angle)*dist + 'px');
        spark.style.animationDelay = Math.random()*0.3 + 's';
        fw.appendChild(spark);
        setTimeout(() => spark.remove(), 1800);
      }
    }, i * 300);
  }
}
</script>
</body>
</html>
