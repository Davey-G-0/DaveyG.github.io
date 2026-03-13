<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Links | Links</title>
  <style>
    :root {
      --acid: #c8ff00;
      --acid-deep: #9fcd00;
      --ink: #020202;
      --blue-0: #04101f;
      --blue-1: #0a2746;
      --blue-2: #0f57a7;
      --blue-3: #68d8ff;
      --white: #f3f7fb;
      --line-dark: rgba(0, 0, 0, 0.16);F
      --line-light: rgba(255, 255, 255, 0.12);
      --panel: rgba(5, 18, 33, 0.72);
      --panel-border: rgba(170, 240, 255, 0.26);
      --glow: rgba(125, 230, 255, 0.28);
    }

    * { box-sizing: border-box; }

    html, body {
      margin: 0;
      min-height: 100%;
      background: var(--acid);
      color: var(--ink);
      font-family: Impact, Haettenschweiler, "Arial Narrow Bold", sans-serif;
      overflow-x: hidden;
    }

    body {
      position: relative;
    }

    .screen {
      min-height: 100vh;
      display: grid;
      grid-template-columns: 49.5% 50.5%;
      position: relative;
      isolation: isolate;
      background: var(--acid);
    }

    .left {
      position: relative;
      background: var(--acid);
      padding: 3vw 4vw 2.6vw;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      overflow: hidden;
    }

    .right {
      position: relative;
      min-height: 100vh;
      overflow: hidden;
      background: linear-gradient(180deg, #18406b 0%, #0d2e58 18%, #0a1d35 60%, #06111e 100%);
    }

    .right::after {
      content: "";
      position: absolute;
      inset: 0;
      background:
        linear-gradient(180deg, rgba(2, 12, 23, 0.08), rgba(2, 10, 18, 0.5)),
        repeating-linear-gradient(to bottom, transparent 0 16%, rgba(255,255,255,0.025) 16.15% 16.5%),
        radial-gradient(circle at 50% 15%, rgba(210, 245, 255, 0.22), transparent 24%);
      pointer-events: none;
      mix-blend-mode: screen;
      z-index: 4;
    }

    .logo {
      margin: 0;
      font-size: clamp(4rem, 9vw, 8.4rem);
      line-height: 0.86;
      text-transform: uppercase;
      letter-spacing: 0.03em;
      max-width: 6ch;
      position: relative;
      z-index: 3;
    }

    .logo .mark {
      position: relative;
      display: inline-block;
    }

    .logo .mark::after {
      content: "°";
      position: absolute;
      top: 0.05em;
      right: -0.43em;
      font-size: 0.28em;
      line-height: 1;
    }

    .plus,
    .ring,
    .split-block,
    .center-notch,
    .hud-cross {
      position: absolute;
      pointer-events: none;
      z-index: 3;
    }

    .plus {
      font-family: Arial, Helvetica, sans-serif;
      font-size: clamp(1.2rem, 2.1vw, 2.1rem);
      color: rgba(0, 0, 0, 0.58);
      line-height: 1;
    }

    .plus.p1 { top: 10%; left: 7%; }
    .plus.p2 { top: 11%; left: 55%; }
    .plus.p3 { top: 45%; left: 46%; font-size: clamp(2rem, 3vw, 2.8rem); }
    .plus.p4 { top: 45%; right: 6%; color: rgba(200, 255, 0, 0.88); }

    .hud-cross {
      width: 52px;
      height: 52px;
      left: 48%;
      top: 45%;
      transform: translate(-50%, -50%);
      opacity: 0.34;
    }

    .hud-cross::before,
    .hud-cross::after {
      content: "";
      position: absolute;
      background: rgba(0, 0, 0, 0.42);
    }

    .hud-cross::before {
      width: 2px;
      height: 100%;
      left: 50%;
      top: 0;
      transform: translateX(-50%);
    }

    .hud-cross::after {
      width: 100%;
      height: 2px;
      top: 50%;
      left: 0;
      transform: translateY(-50%);
    }

    .ring {
      width: clamp(72px, 8vw, 108px);
      height: clamp(72px, 8vw, 108px);
      border: 10px solid var(--ink);
      border-right-color: transparent;
      border-bottom-color: transparent;
      border-radius: 50%;
      left: calc(100% - 3.5rem);
      top: 49.2%;
      transform: translate(-50%, -50%) rotate(-45deg);
    }

    .left::before {
      content: "";
      position: absolute;
      inset: 0;
      background:
        linear-gradient(transparent, transparent),
        repeating-linear-gradient(to right, transparent 0 99.7%, rgba(0,0,0,0.03) 99.7% 100%),
        repeating-linear-gradient(to bottom, transparent 0 99.7%, rgba(0,0,0,0.03) 99.7% 100%);
      opacity: 0.26;
      pointer-events: none;
    }

    .split-block {
      top: 0;
      right: -66px;
      width: 170px;
      height: 57%;
      background: var(--acid);
      clip-path: polygon(0 0, 100% 0, 100% 72%, 62% 72%, 62% 100%, 0 100%);
    }

    .center-notch {
      width: 66px;
      height: 24%;
      left: calc(100% - 1px);
      top: 50%;
      transform: translate(-100%, -50%);
      background: var(--acid);
      clip-path: polygon(0 0, 100% 0, 100% 34%, 42% 34%, 42% 66%, 100% 66%, 100% 100%, 0 100%);
      z-index: 3;
    }

    .top-ui {
      position: relative;
      z-index: 3;
    }

    .prompt-wrap {
      position: relative;
      z-index: 3;
      margin-top: auto;
      max-width: 760px;
      padding-bottom: 8.8rem;
    }

    .prompt {
      margin: 0 0 0.55rem;
      font-family: Arial, Helvetica, sans-serif;
      font-size: clamp(1.4rem, 2.5vw, 2.95rem);
      font-weight: 900;
      letter-spacing: 0.01em;
      text-transform: uppercase;
      color: rgba(0, 0, 0, 0.36);
    }

    .mouse {
      display: inline-flex;
      width: 0.6em;
      height: 0.94em;
      border: 0.09em solid currentColor;
      border-radius: 0.45em;
      vertical-align: -0.1em;
      margin: 0 0.13em;
      position: relative;
    }

    .mouse::before {
      content: "";
      position: absolute;
      width: 0.08em;
      height: 0.18em;
      border-radius: 999px;
      background: currentColor;
      left: 50%;
      top: 0.12em;
      transform: translateX(-50%);
    }

    .meta-line,
    .exit-line {
      font-family: "Courier New", Courier, monospace;
      text-transform: uppercase;
      letter-spacing: 0.06em;
      color: rgba(0, 0, 0, 0.84);
    }

    .meta-line {
      font-size: clamp(0.95rem, 1.45vw, 1.6rem);
      margin-bottom: 0.8rem;
    }

    .exit-line {
      font-size: clamp(0.82rem, 1vw, 1.05rem);
      color: rgba(0, 0, 0, 0.7);
    }

    .esc {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-width: 1.5rem;
      padding: 0.15rem 0.32rem;
      margin-right: 0.5rem;
      border: 1px solid rgba(0, 0, 0, 0.28);
      border-radius: 0.16rem;
      background: rgba(255,255,255,0.2);
      font-size: 0.84em;
    }

    .links-panel {
      position: absolute;
      left: clamp(1.4rem, 3.2vw, 3rem);
      bottom: clamp(1.4rem, 2.8vw, 2.4rem);
      width: min(470px, calc(100% - 2.8rem));
      z-index: 5;
    }

    .link-list {
      display: grid;
      gap: 0.72rem;
    }

    .link-btn {
      position: relative;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1rem;
      text-decoration: none;
      color: var(--white);
      background: linear-gradient(180deg, rgba(7, 26, 46, 0.8), rgba(7, 24, 40, 0.92));
      border: 1px solid var(--panel-border);
      padding: 0.96rem 1rem;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      font-family: Arial, Helvetica, sans-serif;
      font-weight: 900;
      overflow: hidden;
      box-shadow: 0 0 0 1px rgba(255,255,255,0.03), 0 10px 26px rgba(0,0,0,0.24);
      backdrop-filter: blur(4px);
      transition: transform 0.18s ease, box-shadow 0.18s ease, border-color 0.18s ease;
    }

    .link-btn::before {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.08), transparent);
      transform: translateX(-120%);
      transition: transform 0.45s ease;
    }

    .link-btn:hover,
    .link-btn:focus-visible {
      transform: translateY(-2px);
      border-color: rgba(186, 245, 255, 0.5);
      box-shadow: 0 0 0 1px rgba(130, 220, 255, 0.18), 0 0 24px var(--glow), 0 18px 38px rgba(0,0,0,0.34);
      outline: none;
    }

    .link-btn:hover::before,
    .link-btn:focus-visible::before {
      transform: translateX(120%);
    }

    .label {
      display: flex;
      align-items: center;
      gap: 0.78rem;
    }

    .index {
      color: rgba(200, 255, 0, 0.9);
      font-family: "Courier New", Courier, monospace;
      font-weight: 700;
      min-width: 2.2rem;
      font-size: 0.92rem;
    }

    .arrow {
      color: rgba(255, 255, 255, 0.86);
      font-size: 1rem;
    }

    .right-media {
      position: absolute;
      inset: 0;
      overflow: hidden;
      background:
        radial-gradient(circle at 50% 15%, rgba(205, 245, 255, 0.3), transparent 21%),
        linear-gradient(180deg, rgba(12, 63, 121, 0.28), rgba(5, 13, 24, 0.48));
    }

    .frame {
      position: absolute;
      inset: 0;
      opacity: 0;
      animation: cycleFrames 24s infinite;
    }

    .frame img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
      filter: saturate(1.12) contrast(1.06) brightness(0.92);
    }

    .frame.f1 { animation-delay: 0s; }
    .frame.f2 { animation-delay: 6s; }
    .frame.f3 { animation-delay: 12s; }
    .frame.f4 { animation-delay: 18s; }

    @keyframes cycleFrames {
      0% { opacity: 0; transform: scale(1.04); }
      4% { opacity: 1; }
      21% { opacity: 1; transform: scale(1.01); }
      25% { opacity: 0; transform: scale(1); }
      100% { opacity: 0; }
    }

    .fallback-bg {
      position: absolute;
      inset: 0;
      background:
        radial-gradient(circle at 50% 17%, rgba(210, 245, 255, 0.42), transparent 22%),
        linear-gradient(180deg, rgba(60, 180, 255, 0.9) 0%, rgba(19, 87, 167, 0.82) 38%, rgba(8, 37, 72, 0.92) 68%, rgba(4, 17, 32, 1) 100%);
      z-index: 0;
    }

    .moon {
      position: absolute;
      width: min(92vw, 900px);
      aspect-ratio: 1;
      border-radius: 50%;
      top: -13%;
      left: 50%;
      transform: translateX(-20%);
      background:
        radial-gradient(circle at 38% 35%, rgba(255,255,255,0.28), rgba(160,215,255,0.14) 34%, rgba(90, 160, 220, 0.08) 54%, rgba(0,0,0,0) 70%),
        radial-gradient(circle at 60% 60%, rgba(255,255,255,0.05), transparent 55%),
        radial-gradient(circle at 50% 50%, rgba(220,240,255,0.1), rgba(140,210,255,0.02) 58%, transparent 66%);
      box-shadow: 0 0 120px rgba(170, 230, 255, 0.24);
      opacity: 0.55;
      z-index: 1;
    }

    .city {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 32%;
      height: 18%;
      z-index: 2;
      opacity: 0.78;
      background:
        linear-gradient(180deg, rgba(0,0,0,0), rgba(0,0,0,0.18)),
        linear-gradient(to right,
          transparent 0 6%,
          rgba(8,16,28,0.92) 6% 12%,
          transparent 12% 15%,
          rgba(8,16,28,0.92) 15% 19%,
          transparent 19% 24%,
          rgba(8,16,28,0.92) 24% 30%,
          transparent 30% 35%,
          rgba(8,16,28,0.92) 35% 45%,
          transparent 45% 51%,
          rgba(8,16,28,0.92) 51% 62%,
          transparent 62% 67%,
          rgba(8,16,28,0.92) 67% 77%,
          transparent 77% 84%,
          rgba(8,16,28,0.92) 84% 93%,
          transparent 93% 100%);
      clip-path: polygon(0 100%, 0 48%, 7% 48%, 7% 26%, 11% 26%, 11% 44%, 18% 44%, 18% 14%, 24% 14%, 24% 38%, 32% 38%, 32% 8%, 39% 8%, 39% 42%, 49% 42%, 49% 18%, 58% 18%, 58% 46%, 69% 46%, 69% 12%, 76% 12%, 76% 40%, 85% 40%, 85% 24%, 92% 24%, 92% 48%, 100% 48%, 100% 100%);
    }

    .light-bars {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 18%;
      height: 24%;
      z-index: 3;
      pointer-events: none;
    }

    .light-bars span {
      display: block;
      height: 18%;
      margin-bottom: 10%;
      width: 100%;
      background: linear-gradient(90deg, rgba(40,160,255,0.06), rgba(173, 240, 255, 0.92) 28%, rgba(173, 240, 255, 0.92) 78%, rgba(40,160,255,0.1));
      box-shadow: 0 0 20px rgba(145, 230, 255, 0.45), 0 0 40px rgba(80, 200, 255, 0.2);
      opacity: 0.94;
    }

    .scan-ui {
      position: absolute;
      inset: 0;
      z-index: 4;
      pointer-events: none;
      background:
        linear-gradient(180deg, transparent 0 72%, rgba(0,0,0,0.08) 100%),
        radial-gradient(circle at 87% 86%, rgba(0, 255, 170, 0.1), transparent 16%);
    }

    .tiny-meta {
      position: absolute;
      top: 2rem;
      right: 2rem;
      z-index: 5;
      text-align: right;
      color: rgba(255,255,255,0.82);
      font: 700 0.78rem/1.24 "Courier New", monospace;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      text-shadow: 0 0 14px rgba(0,0,0,0.28);
    }

    .tiny-meta span {
      display: block;
      opacity: 0.72;
      margin-top: 0.25rem;
    }

    .usage-note {
      position: absolute;
      left: 1.2rem;
      top: 1.2rem;
      z-index: 6;
      font: 700 0.72rem/1.35 "Courier New", monospace;
      color: rgba(255,255,255,0.55);
      text-transform: uppercase;
      letter-spacing: 0.08em;
      max-width: 18rem;
      background: rgba(0,0,0,0.18);
      border: 1px solid rgba(255,255,255,0.08);
      padding: 0.6rem 0.7rem;
      backdrop-filter: blur(4px);
    }

    @media (max-width: 980px) {
      .screen { grid-template-columns: 1fr; }
      .right { min-height: 40vh; order: -1; }
      .left { padding: 1.6rem 1.25rem 2rem; }
      .split-block, .center-notch, .ring, .plus.p4, .hud-cross { display: none; }
      .prompt-wrap { padding-bottom: 0; margin-top: 2rem; }
      .links-panel {
        position: static;
        width: 100%;
        margin-top: 2rem;
      }
      .logo { max-width: none; font-size: clamp(3.3rem, 16vw, 6rem); }
    }

    @media (max-width: 640px) {
      .tiny-meta {
        top: 1rem;
        right: 1rem;
        font-size: 0.65rem;
      }
      .usage-note {
        left: 0.75rem;
        top: 0.75rem;
        max-width: 14rem;
        font-size: 0.62rem;
      }
      .link-btn {
        padding: 0.92rem 0.9rem;
        font-size: 0.92rem;
      }
      .prompt {
        font-size: 1.5rem;
      }
      .meta-line {
        font-size: 0.92rem;
      }
    }
  </style>
</head>
<body>
  <main class="screen">
    <section class="left">
      <div class="plus p1">+</div>
      <div class="plus p2">+</div>
      <div class="plus p3">+</div>
      <div class="hud-cross"></div>
      <div class="ring"></div>
      <div class="split-block"></div>
      <div class="center-notch"></div>

      <div class="top-ui">
        <h1 class="logo"><span class="mark">Davey G.
        <span>Link terminal</span></span></h1>
      </div>

      <div class="prompt-wrap">
        <p class="prompt">Press <span class="mouse"></span> to continue</p>
        <div class="meta-line">|||||||||| × ⌬ 2893 ▬</div>
        <div class="exit-line"><span class="esc">Esc</span> Exit to desktop</div>
      </div>

      <div class="links-panel">
        <div class="link-list">
          <a class="link-btn" href="https://youtube.com" target="_blank" rel="noopener noreferrer">
            <span class="label"><span class="index">01</span> YouTube</span>
            <span class="arrow">↗</span>
          </a>
          <a class="link-btn" href="https://tiktok.com" target="_blank" rel="noopener noreferrer">
            <span class="label"><span class="index">02</span> TikTok</span>
            <span class="arrow">↗</span>
          </a>
          <a class="link-btn" href="https://instagram.com" target="_blank" rel="noopener noreferrer">
            <span class="label"><span class="index">03</span> Instagram</span>
            <span class="arrow">↗</span>
          </a>
          <a class="link-btn" href="#" target="_blank" rel="noopener noreferrer">
            <span class="label"><span class="index">04</span> Hardware Ranked</span>
            <span class="arrow">↗</span>
          </a>
        </div>
      </div>
    </section>

    <section class="right">
      <div class="usage-note">
        Drop in jpg or webp files instead of video.<br>
        Replace frame-1.jpg to frame-4.jpg.
      </div>

      <div class="tiny-meta">
        
      </div>

      <div class="right-media">
        <div class="fallback-bg"></div>
        <div class="moon"></div>
        <div class="city"></div>

        <!-- Replace these with your own compressed stills. Using 4 webp images usually stays far below 25 MB total. -->
        <div class="frame f1"><img src="frame-1.jpg" alt="Background frame 1" /></div>
        <div class="frame f2"><img src="frame-2.jpg" alt="Background frame 2" /></div>
        <div class="frame f3"><img src="frame-3.jpg" alt="Background frame 3" /></div>
        <div class="frame f4"><img src="frame-4.jpg" alt="Background frame 4" /></div>

        <div class="light-bars">
          <span></span>
          <span></span>
          <span></span>
        </div>
        <div class="scan-ui"></div>
      </div>

      <div class="plus p4">+</div>
    </section>
  </main>
</body>
</html>
