<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>For Pookieeee 🎀</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: 'Poppins', 'Segoe UI', sans-serif;
      background: radial-gradient(circle at top, #ffe6f0, #ffd1dc, #ffb6c1);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }

    .container {
      background: rgba(255,255,255,0.95);
      width: 92%;
      max-width: 420px;
      padding: 36px 28px;
      border-radius: 24px;
      text-align: center;
      box-shadow: 0 30px 60px rgba(0,0,0,0.18);
      animation: popIn 1.2s ease;
      position: relative;
    }

    h1 {
      color: #ff5e8a;
      margin-bottom: 8px;
      font-size: 26px;
    }

    .subtitle {
      color: #777;
      font-size: 14px;
      margin-bottom: 20px;
    }

    .heart {
      font-size: 48px;
      animation: heartbeat 1.2s infinite;
      margin: 14px 0 18px;
    }

    p {
      color: #444;
      font-size: 15.5px;
      line-height: 1.7;
      margin: 10px 0;
    }

    .soft {
      font-style: italic;
      color: #666;
      margin-top: 14px;
    }

    .buttons {
      margin-top: 26px;
      display: flex;
      flex-direction: column;
      gap: 14px;
    }

    button {
      padding: 13px 22px;
      border: none;
      border-radius: 999px;
      font-size: 15px;
      cursor: pointer;
      transition: all 0.25s ease;
    }

    .btn-main {
      background: linear-gradient(135deg, #ff6b9a, #ff3d6e);
      color: #fff;
      box-shadow: 0 10px 20px rgba(255,61,110,0.35);
    }

    .btn-main:hover {
      transform: translateY(-2px) scale(1.03);
    }

    .btn-wa {
      background: #25D366;
      color: #fff;
      box-shadow: 0 10px 20px rgba(37,211,102,0.35);
    }

    .btn-wa:hover {
      transform: translateY(-2px) scale(1.03);
    }

    .from {
      margin-top: 18px;
      font-weight: 600;
      color: #ff5e8a;
    }

    .floating {
      position: absolute;
      inset: 0;
      pointer-events: none;
      overflow: hidden;
    }

    .bubble {
      position: absolute;
      bottom: -40px;
      font-size: 22px;
      animation: floatUp linear infinite;
      opacity: 0.8;
    }

    @keyframes popIn {
      from { opacity: 0; transform: scale(0.9) translateY(20px); }
      to { opacity: 1; transform: scale(1) translateY(0); }
    }

    @keyframes heartbeat {
      0%,100% { transform: scale(1); }
      50% { transform: scale(1.25); }
    }

    @keyframes floatUp {
      from { transform: translateY(0); opacity: 0; }
      10% { opacity: 0.8; }
      to { transform: translateY(-110vh); opacity: 0; }
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Hey Pookieeee 🎀</h1>
    <div class="subtitle">I made this just for you</div>

    <div class="heart">💗</div>

    <p>
      I know you’re upset… and honestly, I get why.
      I messed up, and I’m really sorry for hurting you.
    </p>

    <p>
      Your silence hits harder than any argument.
      I just want a chance to make things right.
    </p>

    <p class="soft">
      Even if you’re still mad… just say hi? 🥹
    </p>

    <div class="buttons">
      <button class="btn-main" onclick="gentleMsg()">Tap if you forgive me a little 💛</button>

      <a href="https://wa.me/?text=Hey%20Karthiiii…%20I%20saw%20your%20page" target="_blank" style="text-decoration:none;">
        <button class="btn-wa">Reply to Karthiiii on WhatsApp 💬</button>
      </a>
    </div>

    <div class="from">— Karthiiii 💛</div>
  </div>

  <div class="floating" id="floating"></div>

  <script>
    function gentleMsg() {
      alert("Thank you for tapping this 💛\nWhenever you’re ready, I’m here.");
    }

    const emojis = ['💗','🎀','✨','💛','🌸'];
    const floating = document.getElementById('floating');

    function createBubble() {
      const span = document.createElement('span');
      span.className = 'bubble';
      span.innerText = emojis[Math.floor(Math.random() * emojis.length)];
      span.style.left = Math.random() * 100 + 'vw';
      span.style.animationDuration = (6 + Math.random() * 6) + 's';
      floating.appendChild(span);

      setTimeout(() => span.remove(), 12000);
    }

    setInterval(createBubble, 600);
      // background music (soft & optional)
    const audio = new Audio('https://cdn.pixabay.com/download/audio/2022/10/03/audio_8b7c7c0d2b.mp3?filename=gentle-piano-ambient-114998.mp3');
    audio.loop = true;
    audio.volume = 0.15;

    function toggleMusic(btn) {
      if (audio.paused) {
        audio.play();
        btn.innerText = 'Pause music 🎵';
      } else {
        audio.pause();
        btn.innerText = 'Play soft music 🎵';
      }
    }
  </script>
</body>
</html>
