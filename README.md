# Mi-niña-hermosa
Mi amoy```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Jardín del Amor</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg-1: #fff4f7;
      --bg-2: #ffe4ec;
      --bg-3: #f8e8ff;
      --rose: #d94f74;
      --rose-dark: #7f2d47;
      --rose-soft: #ffc7d9;
      --gold: #ffd166;
      --white: rgba(255,255,255,0.75);
      --text: #4f2c38;
      --muted: #7b5866;
      --line: rgba(217, 79, 116, 0.22);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: "Poppins", sans-serif;
      color: var(--text);
      background:
        radial-gradient(circle at top left, rgba(255,170,196,0.35), transparent 28%),
        radial-gradient(circle at bottom right, rgba(187,138,255,0.25), transparent 28%),
        linear-gradient(135deg, var(--bg-1), var(--bg-2), var(--bg-3));
      min-height: 100vh;
      overflow-x: hidden;
      position: relative;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      background-image:
        radial-gradient(circle at 20% 20%, rgba(255,105,180,0.06) 0 2px, transparent 3px),
        radial-gradient(circle at 70% 30%, rgba(255,105,180,0.08) 0 2px, transparent 3px),
        radial-gradient(circle at 50% 80%, rgba(255,105,180,0.06) 0 2px, transparent 3px);
      background-size: 140px 140px;
      pointer-events: none;
      z-index: 0;
    }

    .container {
      position: relative;
      z-index: 1;
      width: min(1100px, 92vw);
      margin: 0 auto;
      padding: 30px 0 60px;
    }

    header {
      text-align: center;
      padding: 30px 0 16px;
    }

    .badge {
      width: 78px;
      height: 78px;
      margin: 0 auto 18px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      background: linear-gradient(135deg, #ff9bb9, #f94f82);
      box-shadow: 0 16px 30px rgba(217, 79, 116, 0.25);
      color: white;
      font-size: 2.1rem;
      animation: heartbeat 1.6s infinite ease-in-out;
    }

    @keyframes heartbeat {
      0%, 100% { transform: scale(1); }
      25% { transform: scale(1.08); }
      50% { transform: scale(1.18); }
      75% { transform: scale(1.08); }
    }

    h1 {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(3rem, 7vw, 5.4rem);
      color: var(--rose-dark);
      line-height: 0.92;
      letter-spacing: 0.02em;
      margin-bottom: 12px;
    }

    .subtitle {
      max-width: 760px;
      margin: 0 auto;
      font-size: clamp(1.05rem, 2vw, 1.35rem);
      color: var(--muted);
      line-height: 1.6;
      font-style: italic;
    }

    .intro {
      margin: 40px auto;
      padding: 30px 26px;
      background: var(--white);
      border: 1px solid rgba(255,255,255,0.7);
      border-radius: 26px;
      box-shadow: 0 18px 40px rgba(99, 48, 68, 0.08);
      max-width: 820px;
      text-align: center;
    }

    .intro p {
      font-size: clamp(1.05rem, 2vw, 1.3rem);
      line-height: 1.9;
      color: var(--text);
      margin-bottom: 14px;
    }

    .intro p:last-child {
      margin-bottom: 0;
    }

    .signature {
      margin-top: 18px;
      text-align: right;
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(2rem, 3vw, 2.8rem);
      color: var(--rose-dark);
      font-weight: 600;
    }

    .garden {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 26px;
      margin-top: 46px;
    }

    .flower-card {
      background: rgba(255,255,255,0.78);
      border: 1px solid var(--line);
      border-radius: 22px;
      padding: 22px 18px 20px;
      box-shadow: 0 18px 32px rgba(99,48,68,0.08);
      position: relative;
      overflow: hidden;
      transition: transform 0.25s ease, box-shadow 0.25s ease;
    }

    .flower-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 24px 38px rgba(99,48,68,0.12);
    }

    .flower-card::before {
      content: "";
      position: absolute;
      left: 12%;
      right: 12%;
      top: 0;
      height: 5px;
      border-radius: 0 0 12px 12px;
      background: linear-gradient(90deg, #ffb5cb, #ffd166, #ffc2d1);
    }

    .flower-title {
      text-align: center;
      font-family: "Cormorant Garamond", serif;
      font-size: 2.1rem;
      color: var(--rose-dark);
      margin-bottom: 16px;
    }

    .flower-stage {
      position: relative;
      height: 190px;
      display: grid;
      place-items: center;
      margin-bottom: 16px;
    }

    .flower-info {
      text-align: center;
      line-height: 1.7;
      color: var(--muted);
      font-size: 0.98rem;
    }

    .btn {
      display: inline-block;
      margin-top: 16px;
      background: linear-gradient(135deg, #ff95bb, #f76c9e);
      color: #fff;
      border: none;
      border-radius: 999px;
      padding: 11px 20px;
      font-weight: 600;
      cursor: pointer;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
      box-shadow: 0 10px 18px rgba(217,79,116,0.25);
    }

    .btn:hover {
      transform: translateY(-2px) scale(1.01);
      box-shadow: 0 12px 22px rgba(217,79,116,0.32);
    }

    .rose-wrap {
      position: relative;
      width: 150px;
      height: 150px;
    }

    .rose-wrap .petal {
      position: absolute;
      width: 56px;
      height: 78px;
      background: linear-gradient(180deg, #ffafc8, #ff7fa0);
      border-radius: 50%;
      left: 47px;
      top: 20px;
      box-shadow: inset 0 -10px 15px rgba(255,255,255,0.2);
    }

    .rose-wrap .centre {
      position: absolute;
      width: 34px;
      height: 34px;
      background: var(--gold);
      border-radius: 50%;
      left: 58px;
      top: 76px;
      box-shadow: 0 0 14px rgba(255,209,102,0.5);
      z-index: 2;
    }

    .rose-wrap .stem {
      position: absolute;
      width: 8px;
      height: 90px;
      background: linear-gradient(180deg, #97d6a2, #5aaf7a);
      left: 71px;
      top: 108px;
      border-radius: 999px;
    }

    .rose-wrap .leaf {
      position: absolute;
      width: 26px;
      height: 48px;
      background: linear-gradient(180deg, #a5e0ae, #74bf84);
      border-radius: 100% 0 100% 0;
      top: 120px;
      left: 44px;
      transform: rotate(-30deg);
      box-shadow: inset -2px -2px 6px rgba(0,0,0,0.08);
    }

    .rose-wrap .leaf.right {
      left: 80px;
      transform: rotate(30deg);
      border-radius: 0 100% 0 100%;
    }

    .tulip {
      position: relative;
      width: 140px;
      height: 150px;
    }

    .tulip .petal {
      position: absolute;
      width: 48px;
      height: 88px;
      background: linear-gradient(180deg, #ff9dab, #ff6f8a);
      border-radius: 50% 50% 40% 40%;
      top: 28px;
      left: 46px;
      transform-origin: center bottom;
      box-shadow: inset 0 -10px 16px rgba(255,255,255,0.15);
    }

    .tulip .petal:nth-child(1) { left: 18px; transform: rotate(-18deg); }
    .tulip .petal:nth-child(2) { left: 72px; transform: rotate(18deg); }
    .tulip .stam {
      position: absolute;
      width: 8px;
      height: 92px;
      background: linear-gradient(180deg, #9dd7b0, #60b883);
      left: 66px;
      top: 92px;
      border-radius: 999px;
    }

    .tulip .leaf {
      position: absolute;
      width: 30px;
      height: 62px;
      background: linear-gradient(180deg, #a9e2b1, #6abf7b);
      border-radius: 50% 50% 0 100%;
      top: 120px;
      left: 22px;
      transform: rotate(-18deg);
    }

    .tulip .leaf.right {
      left: 88px;
      transform: scaleX(-1) rotate(-18deg);
    }

    .sunflower {
      position: relative;
      width: 170px;
      height: 170px;
    }

    .sunflower .center {
      position: absolute;
      width: 62px;
      height: 62px;
      border-radius: 50%;
      background: radial-gradient(circle at 40% 35%, #ffdb68, #d09a00);
      left: 54px;
      top: 54px;
      box-shadow: 0 0 16px rgba(255,209,102,0.5);
      z-index: 2;
    }

    .sunflower .petal {
      position: absolute;
      width: 20px;
      height: 74px;
      background: linear-gradient(180deg, #ffe28a, #f7c242);
      border-radius: 20px;
      left: 75px;
      top: 18px;
      transform-origin: center 100px;
      z-index: 1;
    }

    .sunflower .stem {
      position: absolute;
      width: 8px;
      height: 100px;
      background: linear-gradient(180deg, #9fe4b0, #5eaf7b);
      left: 81px;
      top: 108px;
      border-radius: 999px;
    }

    .sunflower .leaf {
      position: absolute;
      width: 30px;
      height: 52px;
      background: linear-gradient(180deg, #aeeab0, #6dbb7f);
      border-radius: 100% 0 100% 0;
      top: 126px;
      left: 50px;
      transform: rotate(-25deg);
    }

    .sunflower .leaf.right {
      left: 90px;
      transform: scaleX(-1) rotate(-25deg);
    }

    .orchid {
      position: relative;
      width: 150px;
      height: 150px;
    }

    .orchid .petal {
      position: absolute;
      width: 48px;
      height: 74px;
      background: linear-gradient(135deg, #db9ca8, #f7bca0);
      border-radius: 60% 40% 50% 50%;
      top: 42px;
      left: 52px;
      transform: rotate(45deg);
      box-shadow: inset 0 -8px 12px rgba(255,255,255,0.18);
    }

    .orchid .petal:nth-child(1) { left: 32px; transform: rotate(25deg); }
    .orchid .petal:nth-child(2) { left: 72px; transform: rotate(70deg); }
    .orchid .petal:nth-child(3) { left: 48px; top: 62px; transform: rotate(130deg); }
    .orchid .center {
      position: absolute;
      width: 22px;
      height: 32px;
      background: linear-gradient(180deg, #ffd86e, #d9a700);
      border-radius: 50%;
      left: 64px;
      top: 72px;
      z-index: 2;
    }

    .orchid .stem {
      position: absolute;
      width: 8px;
      height: 84px;
      background: linear-gradient(180deg, #9dddb0, #5ab57d);
      left: 72px;
      top: 98px;
      border-radius: 999px;
    }

    .orchid .leaf {
      position: absolute;
      width: 30px;
      height: 50px;
      background: linear-gradient(180deg, #abdca9, #68b57f);
      border-radius: 50% 0 50% 0;
      top: 122px;
      left: 36px;
      transform: rotate(-18deg);
    }

    .orchid .leaf.right {
      left: 88px;
      transform: scaleX(-1) rotate(-18deg);
    }

    .love-section {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
      gap: 24px;
      margin-top: 46px;
    }

    .love-item {
      background: rgba(255,255,255,0.8);
      border: 1px solid var(--line);
      border-radius: 20px;
      padding: 22px 18px;
      text-align: center;
      box-shadow: 0 18px 28px rgba(99,48,68,0.06);
    }

    .love-item i {
      font-size: 2.2rem;
      color: var(--rose);
      margin-bottom: 12px;
      display: inline-block;
      animation: floatIcon 3s ease-in-out infinite;
    }

    @keyframes floatIcon {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-6px); }
    }

    .love-item h3 {
      font-size: 1.5rem;
      color: var(--rose-dark);
      font-family: "Cormorant Garamond", serif;
      margin-bottom: 10px;
    }

    .love-item p {
      color: var(--muted);
      line-height: 1.7;
      font-size: 0.96rem;
    }

    .quote {
      margin: 46px auto 0;
      max-width: 850px;
      background: rgba(255,255,255,0.7);
      border-left: 4px solid var(--rose);
      border-radius: 14px;
      padding: 18px 22px;
      text-align: center;
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(1.6rem, 3vw, 2.2rem);
      color: var(--rose-dark);
      line-height: 1.3;
    }

    footer {
      text-align: center;
      margin-top: 40px;
      padding: 30px 0 10px;
      color: var(--rose-dark);
      font-weight: 500;
      line-height: 1.8;
    }

    .floating-hearts {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 0;
      overflow: hidden;
    }

    .floating-hearts span {
      position: absolute;
      bottom: -40px;
      left: var(--left);
      color: var(--color);
      font-size: var(--size);
      opacity: 0;
      animation: rise var(--duration) linear infinite;
      animation-delay: var(--delay);
    }

    @keyframes rise {
      0% {
        opacity: 0;
        transform: translate3d(0, 0, 0) scale(0.75);
      }
      20% {
        opacity: 0.8;
      }
      100% {
        opacity: 0;
        transform: translate3d(var(--drift), -120vh, 0) scale(1.2);
      }
    }

    @media (max-width: 700px) {
      .intro {
        padding: 24px 18px;
      }

      .signature {
        text-align: center;
      }
    }
  </style>
</head>
<body>
  <div class="floating-hearts" id="floatingHearts"></div>

  <div class="container">
    <header>
      <div class="badge">❤</div>
      <h1>Para Mi Amor</h1>
      <p class="subtitle">
        Cada flor en este jardín representa un pedacito de todo lo que siento por ti
      </p>
    </header>

    <section class="intro">
      <p>
        Desde que entraste en mi vida, todo cobró un nuevo brillo. Tu sonrisa ilumina mis días,
        tu presencia calma mis tormentas y tu amor hace que cada momento se vuelva más hermoso.
      </p>
      <p>
        Este jardín es una pequeña forma de decirte lo mucho que te amo. Cada flor simboliza
        un recuerdo, un sentimiento y una promesa: seguir creciendo juntos, cuidándonos y
        regalándonos una historia llena de amor.
      </p>
      <p class="signature">Con todo mi amor,<br>Para siempre tuyo</p>
    </section>

    <div class="garden">
      <article class="flower-card">
        <h2 class="flower-title">Rosa</h2>
        <div class="flower-stage">
          <div class="rose-wrap">
            <div class="petal" style="transform: rotate(0deg);"></div>
            <div class="petal" style="transform: rotate(30deg);"></div>
            <div class="petal" style="transform: rotate(60deg);"></div>
            <div class="petal" style="transform: rotate(90deg);"></div>
            <div class="petal" style="transform: rotate(120deg);"></div>
            <div class="petal" style="transform: rotate(150deg);"></div>
            <div class="centre"></div>
            <div class="stem"></div>
            <div class="leaf"></div>
            <div class="leaf right"></div>
          </div>
        </div>
        <p class="flower-info">
          Como la rosa, nuestro amor es delicado y hermoso, y cada día florece más con ternura.
        </p>
        <button class="btn" type="button">Enviar beso</button>
      </article>

      <article class="flower-card">
        <h2 class="flower-title">Tulipán</h2>
        <div class="flower-stage">
          <div class="tulip">
            <div class="petal"></div>
            <div class="petal"></div>
            <div class="stam"></div>
            <div class="leaf"></div>
            <div class="leaf right"></div>
          </div>
        </div>
        <p class="flower-info">
          Un tulipán que representa la pasión, la alegría y la vida que tú me has regalado.
        </p>
        <button class="btn" type="button">Enviar beso</button>
      </article>

      <article class="flower-card">
        <h2 class="flower-title">Girasol</h2>
        <div class="flower-stage">
          <div class="sunflower">
            <div class="petal" style="transform: rotate(0deg);"></div>
            <div class="petal" style="transform: rotate(18deg);"></div>
            <div class="petal" style="transform: rotate(36deg);"></div>
            <div class="petal" style="transform: rotate(54deg);"></div>
            <div class="petal" style="transform: rotate(72deg);"></div>
            <div class="petal" style="transform: rotate(90deg);"></div>
            <div class="petal" style="transform: rotate(108deg);"></div>
            <div class="petal" style="transform: rotate(126deg);"></div>
            <div class="petal" style="transform: rotate(144deg);"></div>
            <div class="petal" style="transform: rotate(162deg);"></div>
            <div class="center"></div>
            <div class="stem"></div>
            <div class="leaf"></div>
            <div class="leaf right"></div>
          </div>
        </div>
        <p class="flower-info">
          Como el girasol, yo siempre seguiré orientado hacia ti, porque eres mi luz y mi hogar.
        </p>
        <button class="btn" type="button">Enviar beso</button>
      </article>

      <article class="flower-card">
        <h2 class="flower-title">Orquídea</h2>
        <div class="flower-stage">
          <div class="orchid">
            <div class="petal"></div>
            <div class="petal"></div>
            <div class="petal"></div>
            <div class="petal"></div>
            <div class="center"></div>
            <div class="stem"></div>
            <div class="leaf"></div>
            <div class="leaf right"></div>
          </div>
        </div>
        <p class="flower-info">
          Eres única, especial y hermosa por dentro y por fuera, igual que esta flor tan delicada.
        </p>
        <button class="btn" type="button">Enviar beso</button>
      </article>
    </div>

    <div class="quote">
      “Te amo no solo por lo que eres, sino por todo lo que me haces sentir.”
    </div>

    <div class="love-section">
      <div class="love-item">
        <i class="fa-solid fa-heart"></i>
        <h3>Razón de mi alegría</h3>
        <p>Tu presencia en mi vida hace que todo se vea más bonito y más lleno de sentido.</p>
      </div>

      <div class="love-item">
        <i class="fa-solid fa-star"></i>
        <h3>Mi estrella</h3>
        <p>En la oscuridad, tú eres la luz que guía mi camino y el brillo que me acompaña.</p>
      </div>

      <div class="love-item">
        <i class="fa-solid fa-infinity"></i>
        <h3>Amor eterno</h3>
        <p>Mi amor por ti no tiene fin; crece, se fortalece y sigue floreciendo cada día.</p>
      </div>
    </div>

    <footer>
      <p>Este jardín fue creado con todo mi amor para ti.</p>
      <p>Porque cada día contigo es un nuevo motivo para sonreír.</p>
    </footer>
  </div>

  <script>
    const floatingHearts = document.getElementById("floatingHearts");
    const colors = ["#ff7aa2", "#ff9ab4", "#ff5e8a", "#d976b5", "#ffb6c8"];

    for (let i = 0; i < 24; i++) {
      const heart = document.createElement("span");
      heart.textContent = "❤";
      heart.style.setProperty("--left", `${Math.random() * 100}%`);
      heart.style.setProperty("--size", `${16 + Math.random() * 18}px`);
      heart.style.setProperty("--duration", `${9 + Math.random() * 8}s`);
      heart.style.setProperty("--delay", `${-Math.random() * 12}s`);
      heart.style.setProperty("--drift", `${(Math.random() - 0.5) * 140}px`);
      heart.style.setProperty("--color", colors[Math.floor(Math.random() * colors.length)]);
      floatingHearts.appendChild(heart);
    }

    document.querySelectorAll(".btn").forEach(button => {
      button.addEventListener("click", () => {
        button.textContent = "💖 Enviado";
        button.disabled = true;
        setTimeout(() => {
          button.textContent = "Enviar beso";
          button.disabled = false;
        }, 1200);
      });
    });
  </script>
</body>
</html>
```