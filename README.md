# for-jana
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Jana 🌹</title>
<link href="https://fonts.googleapis.com/css2?family=Amiri:ital,wght@0,400;0,700;1,400&family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Great+Vibes&display=swap" rel="stylesheet">
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    min-height: 100vh;
    background: linear-gradient(135deg, #ffd6e7 0%, #ffb3d1 20%, #ff8fb1 40%, #ffadc7 60%, #ffc8da 80%, #ffe0ec 100%);
    font-family: 'Amiri', serif;
    overflow-x: hidden;
    position: relative;
  }

  /* ===== GIANT REALISTIC SVG ROSES ===== */
  .giant-rose-wrap {
    position: fixed;
    z-index: 0;
    pointer-events: none;
  }
  .giant-rose-wrap.rose-left {
    width: 105vw;
    height: 105vw;
    bottom: -30vw;
    left: -30vw;
    animation: spinCW 18s linear infinite;
  }
  .giant-rose-wrap.rose-right {
    width: 105vw;
    height: 105vw;
    top: -30vw;
    right: -30vw;
    animation: spinCCW 22s linear infinite;
  }
  @keyframes spinCW  { from { transform: rotate(0deg); }   to { transform: rotate(360deg); } }
  @keyframes spinCCW { from { transform: rotate(0deg); }   to { transform: rotate(-360deg); } }

  /* Falling roses from sides */
  .falling-rose {
    position: fixed;
    font-size: 28px;
    top: -60px;
    animation: fallRose linear infinite;
    z-index: 3;
    pointer-events: none;
    opacity: 0.9;
  }
  @keyframes fallRose {
    0%   { top: -60px; opacity: 1; transform: translateX(0) rotate(0deg); }
    100% { top: 110vh; opacity: 0.3; transform: translateX(40px) rotate(360deg); }
  }

  /* Balloon hearts */
  .balloon {
    position: fixed;
    bottom: -80px;
    font-size: 36px;
    animation: floatUp linear infinite;
    z-index: 3;
    pointer-events: none;
  }
  @keyframes floatUp {
    0%   { bottom: -80px; opacity: 1; transform: translateX(0) scale(1); }
    50%  { opacity: 0.9; transform: translateX(20px) scale(1.05); }
    100% { bottom: 110vh; opacity: 0; transform: translateX(-10px) scale(0.8); }
  }

  /* Main card */
  .card {
    position: relative;
    z-index: 10;
    max-width: 700px;
    margin: 0 auto;
    padding: 20px 16px 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .header-roses {
    font-size: 42px;
    letter-spacing: 8px;
    animation: pulse 2s ease-in-out infinite;
    margin-bottom: 4px;
  }
  @keyframes pulse {
    0%,100% { transform: scale(1); }
    50%      { transform: scale(1.12); }
  }

  .title {
    font-family: 'Great Vibes', cursive;
    font-size: clamp(52px, 12vw, 88px);
    color: #6b0020;
    text-shadow: 0 0 20px #ff6fa044, 0 2px 0 #fff, 2px 4px 12px #c0003360;
    line-height: 1.1;
    text-align: center;
    margin-bottom: 2px;
    animation: titleGlow 3s ease-in-out infinite;
  }
  @keyframes titleGlow {
    0%,100% { text-shadow: 0 0 20px #ff6fa044, 0 2px 0 #fff, 2px 4px 12px #c0003360; }
    50%      { text-shadow: 0 0 50px #ff6fa0aa, 0 2px 0 #fff, 2px 4px 30px #c00033cc; }
  }

  .subtitle {
    font-family: 'Great Vibes', cursive;
    font-size: clamp(26px, 6vw, 40px);
    color: #9b0040;
    margin-bottom: 18px;
    text-align: center;
  }

  .message-box {
    background: linear-gradient(145deg, rgba(255,255,255,0.78), rgba(255,200,220,0.62));
    border: 2px solid rgba(192,0,51,0.18);
    border-radius: 28px;
    padding: 28px 30px;
    box-shadow: 0 8px 40px rgba(192,0,51,0.15), inset 0 1px 0 rgba(255,255,255,0.9);
    backdrop-filter: blur(14px);
    width: 100%;
    margin-bottom: 22px;
  }

  .arabic-text {
    font-family: 'Amiri', serif;
    font-size: clamp(18px, 4.5vw, 24px);
    line-height: 2.1;
    color: #4a0018;
    text-align: center;
    direction: rtl;
  }

  .divider {
    font-size: 30px;
    text-align: center;
    margin: 18px 0;
    letter-spacing: 6px;
    opacity: 0.7;
  }

  .english-text {
    font-family: 'Playfair Display', serif;
    font-size: clamp(14px, 3.5vw, 18px);
    line-height: 2;
    color: #5a0020;
    text-align: center;
    direction: ltr;
    font-style: italic;
  }

  .proposal-section {
    margin-top: 30px;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 18px;
  }

  .proposal-divider {
    font-size: 28px;
    letter-spacing: 10px;
    animation: pulse 1.5s ease-in-out infinite;
  }

  .proposal-box {
    background: linear-gradient(135deg, #6b0020, #a0003a, #6b0020);
    border-radius: 24px;
    padding: 30px 28px;
    box-shadow: 0 12px 50px rgba(107,0,32,0.5), 0 0 0 4px rgba(255,255,255,0.3), inset 0 1px 0 rgba(255,255,255,0.2);
    width: 100%;
    text-align: center;
    position: relative;
    overflow: hidden;
    animation: proposalGlow 3s ease-in-out infinite;
  }
  @keyframes proposalGlow {
    0%,100% { box-shadow: 0 12px 50px rgba(107,0,32,0.5), 0 0 0 4px rgba(255,255,255,0.3); }
    50%      { box-shadow: 0 16px 80px rgba(107,0,32,0.75), 0 0 0 4px rgba(255,255,255,0.5), 0 0 70px #ff6fa060; }
  }
  .proposal-box::before {
    content: '';
    position: absolute;
    top: -50%; left: -50%;
    width: 200%; height: 200%;
    background: radial-gradient(circle, rgba(255,255,255,0.07) 0%, transparent 60%);
    animation: shimmer 4s linear infinite;
  }
  @keyframes shimmer { from { transform: rotate(0deg); } to { transform: rotate(360deg); } }

  .ring-emoji { font-size: 48px; animation: ringBounce 1.5s ease-in-out infinite; display: block; margin-bottom: 10px; }
  @keyframes ringBounce {
    0%,100% { transform: translateY(0) rotate(-10deg); }
    50%      { transform: translateY(-10px) rotate(10deg); }
  }

  .proposal-text {
    font-family: 'Playfair Display', serif;
    font-size: clamp(18px, 5vw, 26px);
    color: #fff;
    line-height: 1.6;
    font-weight: 700;
    text-shadow: 0 2px 8px rgba(0,0,0,0.4);
    position: relative;
    z-index: 1;
  }
  .proposal-name {
    font-family: 'Great Vibes', cursive;
    font-size: clamp(24px, 6vw, 36px);
    color: #ffd6e7;
    display: block;
    margin-top: 8px;
    text-shadow: 0 0 20px rgba(255,214,231,0.9);
  }

  .signature {
    margin-top: 28px;
    font-family: 'Great Vibes', cursive;
    font-size: clamp(22px, 5vw, 32px);
    color: #7a0028;
    text-align: center;
    text-shadow: 0 0 15px rgba(122,0,40,0.3);
  }
</style>
</head>
<body>

<!-- ===== GIANT REALISTIC ROSE LEFT (bottom-left, spins CW) ===== -->
<div class="giant-rose-wrap rose-left">
<svg viewBox="0 0 500 500" xmlns="http://www.w3.org/2000/svg" width="100%" height="100%">
  <defs>
    <radialGradient id="rg1" cx="50%" cy="50%" r="50%">
      <stop offset="0%"   stop-color="#ff1a4a"/>
      <stop offset="40%"  stop-color="#cc0030"/>
      <stop offset="75%"  stop-color="#8b0020"/>
      <stop offset="100%" stop-color="#4a0010"/>
    </radialGradient>
    <radialGradient id="rg2" cx="40%" cy="35%" r="55%">
      <stop offset="0%"   stop-color="#ff4060"/>
      <stop offset="50%"  stop-color="#b8002a"/>
      <stop offset="100%" stop-color="#5a0015"/>
    </radialGradient>
    <radialGradient id="rg3" cx="60%" cy="40%" r="50%">
      <stop offset="0%"   stop-color="#ff3355"/>
      <stop offset="50%"  stop-color="#aa0025"/>
      <stop offset="100%" stop-color="#600018"/>
    </radialGradient>
    <radialGradient id="rg4" cx="50%" cy="60%" r="50%">
      <stop offset="0%"   stop-color="#ff2244"/>
      <stop offset="60%"  stop-color="#990020"/>
      <stop offset="100%" stop-color="#500012"/>
    </radialGradient>
    <filter id="softBlur">
      <feGaussianBlur stdDeviation="1.2"/>
    </filter>
    <filter id="petalShad">
      <feDropShadow dx="2" dy="4" stdDeviation="4" flood-color="#3a000a" flood-opacity="0.45"/>
    </filter>
  </defs>

  <!-- Outer petals layer 1 -->
  <ellipse cx="250" cy="130" rx="54" ry="90"  fill="url(#rg2)" opacity="0.92" transform="rotate(0   250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="130" rx="54" ry="90"  fill="url(#rg3)" opacity="0.85" transform="rotate(45  250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="130" rx="54" ry="90"  fill="url(#rg2)" opacity="0.90" transform="rotate(90  250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="130" rx="54" ry="90"  fill="url(#rg4)" opacity="0.88" transform="rotate(135 250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="130" rx="54" ry="90"  fill="url(#rg3)" opacity="0.92" transform="rotate(180 250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="130" rx="54" ry="90"  fill="url(#rg2)" opacity="0.87" transform="rotate(225 250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="130" rx="54" ry="90"  fill="url(#rg4)" opacity="0.90" transform="rotate(270 250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="130" rx="54" ry="90"  fill="url(#rg3)" opacity="0.85" transform="rotate(315 250 250)" filter="url(#petalShad)"/>

  <!-- Mid petals layer 2 -->
  <ellipse cx="250" cy="165" rx="40" ry="72"  fill="url(#rg1)" opacity="0.95" transform="rotate(22  250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="165" rx="40" ry="72"  fill="url(#rg2)" opacity="0.93" transform="rotate(82  250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="165" rx="40" ry="72"  fill="url(#rg3)" opacity="0.95" transform="rotate(142 250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="165" rx="40" ry="72"  fill="url(#rg1)" opacity="0.92" transform="rotate(202 250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="165" rx="40" ry="72"  fill="url(#rg4)" opacity="0.94" transform="rotate(262 250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="165" rx="40" ry="72"  fill="url(#rg2)" opacity="0.93" transform="rotate(322 250 250)" filter="url(#petalShad)"/>

  <!-- Inner petals layer 3 -->
  <ellipse cx="250" cy="195" rx="28" ry="52"  fill="url(#rg1)" opacity="0.97" transform="rotate(10  250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="195" rx="28" ry="52"  fill="url(#rg2)" opacity="0.96" transform="rotate(82  250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="195" rx="28" ry="52"  fill="url(#rg3)" opacity="0.97" transform="rotate(154 250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="195" rx="28" ry="52"  fill="url(#rg1)" opacity="0.96" transform="rotate(226 250 250)" filter="url(#petalShad)"/>
  <ellipse cx="250" cy="195" rx="28" ry="52"  fill="url(#rg4)" opacity="0.97" transform="rotate(298 250 250)" filter="url(#petalShad)"/>

  <!-- Core -->
  <circle cx="250" cy="250" r="46" fill="url(#rg1)" filter="url(#petalShad)"/>
  <circle cx="250" cy="250" r="30" fill="#7a0018" opacity="0.9"/>
  <circle cx="250" cy="250" r="16" fill="#4a000e" opacity="0.95"/>
  <circle cx="242" cy="242" r="5"  fill="#ff6070" opacity="0.5" filter="url(#softBlur)"/>
</svg>
</div>

<!-- ===== GIANT REALISTIC ROSE RIGHT (top-right, spins CCW) ===== -->
<div class="giant-rose-wrap rose-right">
<svg viewBox="0 0 500 500" xmlns="http://www.w3.org/2000/svg" width="100%" height="100%">
  <defs>
    <radialGradient id="rr1" cx="50%" cy="50%" r="50%">
      <stop offset="0%"   stop-color="#ff1a4a"/>
      <stop offset="40%"  stop-color="#cc0030"/>
      <stop offset="75%"  stop-color="#8b0020"/>
      <stop offset="100%" stop-color="#4a0010"/>
    </radialGradient>
    <radialGradient id="rr2" cx="40%" cy="35%" r="55%">
      <stop offset="0%"   stop-color="#ff4060"/>
      <stop offset="50%"  stop-color="#b8002a"/>
      <stop offset="100%" stop-color="#5a0015"/>
    </radialGradient>
    <radialGradient id="rr3" cx="60%" cy="40%" r="50%">
      <stop offset="0%"   stop-color="#e02040"/>
      <stop offset="50%"  stop-color="#960020"/>
      <stop offset="100%" stop-color="#4e0014"/>
    </radialGradient>
    <radialGradient id="rr4" cx="50%" cy="65%" r="50%">
      <stop offset="0%"   stop-color="#ff2244"/>
      <stop offset="60%"  stop-color="#880018"/>
      <stop offset="100%" stop-color="#3e000e"/>
    </radialGradient>
    <filter id="ps2">
      <feDropShadow dx="-2" dy="4" stdDeviation="4" flood-color="#3a000a" flood-opacity="0.4"/>
    </filter>
  </defs>

  <ellipse cx="250" cy="130" rx="56" ry="92"  fill="url(#rr3)" opacity="0.92" transform="rotate(20  250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="130" rx="56" ry="92"  fill="url(#rr2)" opacity="0.88" transform="rotate(65  250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="130" rx="56" ry="92"  fill="url(#rr4)" opacity="0.91" transform="rotate(110 250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="130" rx="56" ry="92"  fill="url(#rr3)" opacity="0.89" transform="rotate(155 250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="130" rx="56" ry="92"  fill="url(#rr2)" opacity="0.92" transform="rotate(200 250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="130" rx="56" ry="92"  fill="url(#rr4)" opacity="0.88" transform="rotate(245 250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="130" rx="56" ry="92"  fill="url(#rr3)" opacity="0.91" transform="rotate(290 250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="130" rx="56" ry="92"  fill="url(#rr2)" opacity="0.90" transform="rotate(335 250 250)" filter="url(#ps2)"/>

  <ellipse cx="250" cy="168" rx="42" ry="70"  fill="url(#rr1)" opacity="0.95" transform="rotate(35  250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="168" rx="42" ry="70"  fill="url(#rr3)" opacity="0.93" transform="rotate(95  250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="168" rx="42" ry="70"  fill="url(#rr2)" opacity="0.95" transform="rotate(155 250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="168" rx="42" ry="70"  fill="url(#rr4)" opacity="0.93" transform="rotate(215 250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="168" rx="42" ry="70"  fill="url(#rr1)" opacity="0.94" transform="rotate(275 250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="168" rx="42" ry="70"  fill="url(#rr3)" opacity="0.93" transform="rotate(335 250 250)" filter="url(#ps2)"/>

  <ellipse cx="250" cy="198" rx="29" ry="50"  fill="url(#rr1)" opacity="0.97" transform="rotate(18  250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="198" rx="29" ry="50"  fill="url(#rr2)" opacity="0.96" transform="rotate(90  250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="198" rx="29" ry="50"  fill="url(#rr3)" opacity="0.97" transform="rotate(162 250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="198" rx="29" ry="50"  fill="url(#rr1)" opacity="0.96" transform="rotate(234 250 250)" filter="url(#ps2)"/>
  <ellipse cx="250" cy="198" rx="29" ry="50"  fill="url(#rr4)" opacity="0.97" transform="rotate(306 250 250)" filter="url(#ps2)"/>

  <circle cx="250" cy="250" r="48" fill="url(#rr1)" filter="url(#ps2)"/>
  <circle cx="250" cy="250" r="31" fill="#7a0018" opacity="0.9"/>
  <circle cx="250" cy="250" r="17" fill="#4a000e" opacity="0.95"/>
  <circle cx="243" cy="243" r="5"  fill="#ff5060" opacity="0.45"/>
</svg>
</div>

<!-- Falling roses -->
<div class="falling-rose" style="left:5%;  animation-duration:5s;  animation-delay:0s;   font-size:26px;">🌹</div>
<div class="falling-rose" style="left:12%; animation-duration:7s;  animation-delay:1s;   font-size:22px;">🥀</div>
<div class="falling-rose" style="left:3%;  animation-duration:6s;  animation-delay:2.5s; font-size:28px;">🌹</div>
<div class="falling-rose" style="left:19%; animation-duration:8s;  animation-delay:0.5s; font-size:20px;">🌸</div>
<div class="falling-rose" style="right:5%;  animation-duration:6s;  animation-delay:1.2s; font-size:24px;">🌹</div>
<div class="falling-rose" style="right:12%; animation-duration:5.5s;animation-delay:3s;   font-size:28px;">🥀</div>
<div class="falling-rose" style="right:3%;  animation-duration:7.5s;animation-delay:0.8s; font-size:22px;">🌹</div>
<div class="falling-rose" style="right:20%; animation-duration:9s;  animation-delay:2s;   font-size:20px;">🌸</div>

<!-- Balloons -->
<div class="balloon" style="left:8%;  animation-duration:7s;  animation-delay:0s;">🩷</div>
<div class="balloon" style="left:22%; animation-duration:9s;  animation-delay:1s;">❤️</div>
<div class="balloon" style="left:38%; animation-duration:6s;  animation-delay:2s;">🩷</div>
<div class="balloon" style="left:55%; animation-duration:8s;  animation-delay:0.5s;">💗</div>
<div class="balloon" style="left:70%; animation-duration:10s; animation-delay:1.5s;">❤️</div>
<div class="balloon" style="left:85%; animation-duration:7.5s;animation-delay:3s;">🩷</div>
<div class="balloon" style="left:50%; animation-duration:11s; animation-delay:4s;">💖</div>
<div class="balloon" style="left:15%; animation-duration:8.5s;animation-delay:2.5s;">💗</div>

<!-- CARD -->
<div class="card">
  <div class="header-roses">🌹🥀🌹🥀🌹</div>
  <div class="title">Happy Birthday</div>
  <div class="title" style="margin-top:-20px;">Jana</div>
  <div class="subtitle">✨ يوم ميلادك الأجمل ✨</div>

  <div class="message-box">
    <p class="arabic-text">
      كل سنه وانتي طيبة يا حبيبة قلبي ونور عيني 🌹<br>
      ربنا يخليكي ليا يا روحي، وربنا — حمدلله — رزقني بيكي 💗<br>
      عقبال ما يرزقنا بعيالنا ويرزقني بفلوس أدلعك<br>
      وأحقق كل اللي نفسك فيه يا قلبي 🎀<br>
      ربنا يكرمك ويبارك فيكي وتبقي دكتورتي اللي قد الدنيا 👩‍⚕️✨<br>
      أنتي كل حاجة حلوة في حياتي يا جنا<br>
      ومش قادر أتخيل يوم من غيرك 🥀<br>
      ربنا يديمك عليا وعلى قلبي دايمًا 💖
    </p>
    <div class="divider">🌹 ✦ 🌹 ✦ 🌹</div>
    <p class="english-text">
      Every year may you bloom more beautiful, my love 🌹<br>
      You are the reason my heart beats with joy and peace 💗<br>
      God blessed me the day He brought you into my life<br>
      And I pray He blesses us with a future full of love 🎀<br>
      May all your dreams come true, my dearest Jana<br>
      May your path be filled with light and happiness ✨<br>
      I wish you success in every step of your journey, Doctor Jana 👩‍⚕️<br>
      You deserve the whole world and so much more, my heart 💖<br>
      With every breath I take, I am grateful you are mine 🥀<br>
      May God keep you safe, happy, and always by my side 🌸<br>
      No words can ever describe how much you mean to me, love 💗<br>
      Happy Birthday, my soul — today and every day 🎂🌹
    </p>
  </div>

  <div class="proposal-section">
    <div class="proposal-divider">💍 🌹 💍 🌹 💍</div>
    <div class="proposal-box">
      <span class="ring-emoji">💍</span>
      <p class="proposal-text">
        Jana, my love, my heart, my everything...<br><br>
        Will you marry me? 🌹<br><br>
        <span class="proposal-name">— Mohannad Mohamed Haroon 🤍</span>
      </p>
    </div>
    <div class="signature">
      🌹 With all my love, forever yours 🌹
    </div>
  </div>
</div>

</body>
</html>
