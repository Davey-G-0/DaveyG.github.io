<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Davey G. | Links</title>
  <style>
    :root {
      --bg: #c8ff00;
      --ink: #050505;
      --panel: #061a31;
      --panel-2: #0b2a4d;
      --line: rgba(5, 5, 5, 0.14);
      --muted: rgba(5, 5, 5, 0.7);
      --glow: rgba(90, 235, 255, 0.65);
      --card: rgba(255, 255, 255, 0.06);
      --card-border: rgba(255, 255, 255, 0.14);
      --white: #f4f7fb;
    }

    * {
      box-sizing: border-box;
    }

    html, body {
      margin: 0;
      min-height: 100%;
      background: var(--bg);
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
      grid-template-columns: 52% 48%;
      position: relative;
      isolation: isolate;
    }

    .left {
      position: relative;
      padding: 3vw 4vw 2.5vw;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      background: var(--bg);
    }

    .right {
      position: relative;
      min-height: 100vh;
      background:
        linear-gradient(180deg, rgba(4, 16, 34, 0.1), rgba(4, 16, 34, 0.65)),
        radial-gradient(circle at 50% 18%, rgba(180, 240, 255, 0.45), transparent 26%),
        linear-gradient(180deg, #3cb5ff 0%, #07264a 52%, #06111f 100%);
      overflow: hidden;
    }

    .right::before {
      content: "";
      position: absolute;
      inset: 0;
      background:
        linear-gradient(transparent 70%, rgba(0, 0, 0, 0.15) 100%),
        repeating-linear-gradient(
          to bottom,
          transparent 0 11%,
          rgba(255,255,255,0.03) 11.2% 11.5%
        );
      pointer-events: none;
      mix-blend-mode: screen;
    }

    .video-wrap {
      position: absolute;
      inset: 0;
      overflow: hidden;
    }

    .video-wrap video,
    .video-wrap img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
      filter: saturate(1.1) contrast(1.05);
    }

    .video-overlay {
      position: absolute;
      inset: 0;
      background:
        radial-gradient(circle at 55% 20%, rgba(200, 240, 255, 0.45), transparent 28%),
        linear-gradient(180deg, rgba(8, 18, 40, 0.15), rgba(4, 9, 18, 0.58)),
        repeating-linear-gradient(
          to bottom,
          transparent 0 16%,
          rgba(130, 220, 255, 0.12) 16.4% 17.2%
        );
      pointer-events: none;
    }

    .logo {
      font-size: clamp(4.5rem, 10vw, 9rem);
      line-height: 0.9;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      max-width: 6ch;
      margin: 0;
    }

    .logo span {
      display: inline-block;
      position: relative;
    }

    .logo span::after {
      content: "°";
      position: absolute;
      top: 0.06em;
      right: -0.45em;
      font-size: 0.28em;
      line-height: 1;
    }

    .plus,
    .ring,
    .scanline,
    .corner {
      position: absolute;
      pointer-events: none;
    }

    .plus {
      font-family: Arial, sans-serif;
      font-weight: 400;
      color: rgba(5, 5, 5, 0.66);
      font-size: clamp(1.5rem, 2.6vw, 2.4rem);
    }

    .plus.a { top: 12%; left: 6%; }
    .plus.b { top: 12%; left: 56%; }
    .plus.c { top: 45%; left: 48%; font-size: clamp(2rem, 3vw, 3rem); }
    .plus.d { top: 45%; right: -2.2rem; color: rgba(200, 255, 60, 0.8); }

    .ring {
      width: clamp(70px, 8vw, 110px);
      height: clamp(70px, 8vw, 110px);
      border: 10px solid var(--ink);
      border-right-color: transparent;
      border-bottom-color: transparent;
      border-radius: 50%;
      left: calc(100% - 3.2rem);
      top: 49%;
      transform: translate(-50%, -50%) rotate(-45deg);
      z-index: 4;
    }

    .left::after {
      content: "";
      position: absolute;
      top: 0;
      right: -64px;
      width: 170px;
      height: 58%;
      background: var(--bg);
      clip-path: polygon(0 0, 100% 0, 100% 72%, 62% 72%, 62% 100%, 0 100%);
      z-index: 2;
    }

    .hud {
      position: relative;
      z-index: 3;
      max-width: 680px;
    }

    .prompt {
      margin-top: 2rem;
      font-family: Arial, Helvetica, sans-serif;
      font-weight: 900;
      text-transform: uppercase;
      letter-spacing: 0.02em;
      font-size: clamp(1.4rem, 2.6vw, 3rem);
      color: rgba(5, 5, 5, 0.35);
    }

    .prompt .mouse {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 0.6em;
      height: 0.95em;
      border: 0.08em solid currentColor;
      border-radius: 0.4em;
      vertical-align: -0.08em;
      margin: 0 0.12em;
      position: relative;
    }

    .prompt .mouse::before {
      content: "";
      position: absolute;
      top: 0.13em;
      width: 0.08em;
      height: 0.18em;
      background: currentColor;
      border-radius: 999px;
    }

    .id-line,
    .exit {
      margin-top: 1rem;
      font-family: "Courier New", Courier, monospace;
      text-transform: uppercase;
      letter-spacing: 0.06em;
      color: rgba(5, 5, 5, 0.88);
    }

    .id-line {
      font-size: clamp(0.95rem, 1.45vw, 1.65rem);
    }

    .exit {
      font-size: clamp(0.9rem, 1vw, 1.1rem);
      color: rgba(5, 5, 5, 0.78);
    }

    .esc {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 0.12rem 0.33rem;
      border: 1px solid rgba(5, 5, 5, 0.35);
      border-radius: 0.22rem;
      margin-right: 0.55rem;
      font-size: 0.8em;
      background: rgba(255,255,255,0.28);
    }

    .links-panel {
      position: absolute;
      left: clamp(2rem, 4vw, 4rem);
      bottom: clamp(2rem, 4vw, 4rem);
      width: min(420px, calc(100% - 4rem));
      z-index: 5;
    }

    .link-list {
      display: grid;
      gap: 0.9rem;
      margin-top: 1.2rem;
    }

    .link-btn {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1rem;
      text-decoration: none;
      color: var(--white);
      padding: 1rem 1.1rem;
      background: linear-gradient(180deg, rgba(6, 26, 49, 0.78), rgba(8, 34, 63, 0.88));
      border: 1px solid var(--card-border);
      backdrop-filter: blur(6px);
      text-transform: uppercase;
      letter-spacing: 0.08em;
      font-family: Arial, Helvetica, sans-serif;
      font-weight: 800;
      position: relative;
      overflow: hidden;
      transition: transform 0.18s ease, border-color 0.18s ease, box-shadow 0.18s ease;
      box-shadow: 0 0 0 1px rgba(255,255,255,0.03), 0 14px 34px rgba(0,0,0,0.2);
    }

    .link-btn::before {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.09), transparent);
      transform: translateX(-100%);
      transition: transform 0.45s ease;
    }

    .link-btn:hover,
    .link-btn:focus-visible {
      transform: translateY(-2px);
      border-color: rgba(140, 235, 255, 0.55);
      box-shadow: 0 0 0 1px rgba(130, 220, 255, 0.2), 0 0 26px rgba(90, 235, 255, 0.18), 0 18px 40px rgba(0,0,0,0.3);
      outline: none;
    }

    .link-btn:hover::before,
    .link-btn:focus-visible::before {
      transform: translateX(100%);
    }

    .label {
      display: flex;
      align-items: center;
      gap: 0.75rem;
    }

    .index {
      color: rgba(200, 255, 0, 0.85);
      font-family: "Courier New", Courier, monospace;
      font-weight: 700;
      font-size: 0.92rem;
      min-width: 2.2rem;
    }

    .arrow {
      font-size: 1rem;
      color: rgba(255,255,255,0.85);
    }

    .small-meta {
      position: absolute;
      top: 2rem;
      right: 2rem;
      z-index: 5;
      color: rgba(255,255,255,0.78);
      font: 700 0.78rem/1.2 "Courier New", monospace;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      text-align: right;
      text-shadow: 0 0 10px rgba(0,0,0,0.35);
    }

    .small-meta span {
      display: block;
      opacity: 0.75;
    }

    @media (max-width: 980px) {
      .screen {
        grid-template-columns: 1fr;
      }

      .right {
        min-height: 38vh;
        order: -1;
      }

      .left {
        min-height: auto;
        padding-top: 2rem;
      }

      .left::after,
      .ring,
      .plus.d {
        display: none;
      }

      .links-panel {
        position: static;
        width: 100%;
        margin-top: 2.5rem;
      }

      .hud {
        max-width: 100%;
      }

      .logo {
        max-width: none;
      }
    }

    @media (max-width: 640px) {
      .left {
        padding: 1.25rem 1.25rem 2rem;
      }

      .small-meta {
        top: 1rem;
        right: 1rem;
        font-size: 0.68rem;
      }

      .link-btn {
        padding: 0.95rem 0.9rem;
        font-size: 0.92rem;
      }

      .prompt {
        margin-top: 1rem;
      }

      .id-line {
        font-size: 0.95rem;
      }
    }
  </style>
</head>
<body>
  <main class="screen">
    <section class="left">
      <div class="plus a">+</div>
      <div class="plus b">+</div>
      <div class="plus c">+</div>
      <div class="ring"></div>

      <div class="hud">
        <h1 class="logo"><span>Marathon</span></h1>

        <div class="prompt">Press <span class="mouse"></span> to continue</div>
        <div class="id-line">|||||||||| × ⌬ 2893 ▬</div>
        <div class="exit"><span class="esc">Esc</span> Exit to desktop</div>
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
      <div class="small-meta">
        Davey G.
        <span>Link Terminal</span>
      </div>

      <div class="video-wrap">
        <!-- Replace splash.mp4 with your own looping video file -->
        <video autoplay muted loop playsinline poster="">
          <source src="splash.mp4" type="video/mp4" />
        </video>

        <!-- Fallback if you do not want video yet: uncomment and use an image -->
        <!-- <img src="right-panel.jpg" alt="Background panel art" /> -->
      </div>

      <div class="video-overlay"></div>
      <div class="plus d">+</div>
    </section>
  </main>
</body>
</html>

