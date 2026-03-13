<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Davey G. | Links</title>
<style>
:root{
  --acid:#c8ff00;
  --ink:#020202;
  --blue:#0b2a4d;
  --white:#f3f7fb;
  --panel-border:rgba(170,240,255,.25);
  --glow:rgba(125,230,255,.28);
  --hud:rgba(255,255,255,.08);
  --hud-bright:rgba(170,240,255,.45);
}

*{box-sizing:border-box}
html,body{
  margin:0;
  min-height:100%;
  background:var(--acid);
  color:var(--ink);
  font-family:Impact,Haettenschweiler,"Arial Narrow Bold",sans-serif;
  overflow-x:hidden;
}
body{position:relative}

.app{
  min-height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
  padding:2rem;
  position:relative;
}

/* INTRO OVERLAY */
.intro{
  position:fixed;
  inset:0;
  z-index:50;
  display:flex;
  align-items:center;
  justify-content:center;
  background:
    radial-gradient(circle at 50% 20%, rgba(120,210,255,.08), transparent 25%),
    linear-gradient(180deg, rgba(2,8,14,.88), rgba(2,8,14,.96));
  color:var(--white);
  transition:opacity .5s ease, visibility .5s ease;
}

.intro.hidden{
  opacity:0;
  visibility:hidden;
  pointer-events:none;
}

.intro::before{
  content:"";
  position:absolute;
  inset:0;
  background:repeating-linear-gradient(to bottom, transparent 0 3px, rgba(255,255,255,.03) 3px 4px);
  opacity:.45;
  pointer-events:none;
}

.intro-panel{
  position:relative;
  z-index:2;
  width:min(92vw,760px);
  padding:2rem 1.5rem;
  text-align:center;
}

.intro-title{
  margin:0;
  color:var(--acid);
  font-size:clamp(3rem,8vw,6rem);
  text-transform:uppercase;
  letter-spacing:.04em;
  line-height:.9;
}

.intro-sub{
  margin:.7rem 0 1.6rem;
  font:800 clamp(.9rem,1.4vw,1rem)/1.4 Arial,Helvetica,sans-serif;
  letter-spacing:.18em;
  text-transform:uppercase;
  color:rgba(255,255,255,.7);
}

.intro-prompt{
  display:inline-block;
  padding:.9rem 1.25rem;
  border:1px solid rgba(170,240,255,.28);
  background:rgba(255,255,255,.03);
  font:900 clamp(.9rem,1.5vw,1.1rem)/1.2 Arial,Helvetica,sans-serif;
  letter-spacing:.14em;
  text-transform:uppercase;
  color:var(--white);
  animation:pulsePrompt 1.4s ease-in-out infinite;
}

@keyframes pulsePrompt{
  0%,100%{opacity:.55;box-shadow:0 0 0 rgba(170,240,255,0)}
  50%{opacity:1;box-shadow:0 0 24px rgba(170,240,255,.16)}
}

/* DESKTOP */
.screen{
  width:min(96vw,1600px);
  aspect-ratio:16/9;
  min-height:720px;
  max-height:92vh;
  display:grid;
  grid-template-columns:50% 50%;
  background:var(--acid);
  position:relative;
  overflow:hidden;
  box-shadow:0 30px 80px rgba(0,0,0,.25);
}

.left{
  padding:3vw 4vw;
  position:relative;
  display:flex;
  flex-direction:column;
  justify-content:space-between;
}

.right{
  position:relative;
  background:linear-gradient(180deg,#18406b 0%,#0d2e58 18%,#0a1d35 60%,#06111e 100%);
  overflow:hidden;
}

.left:before{
  content:"";
  position:absolute;
  inset:0;
  background:
    repeating-linear-gradient(to right,transparent 0 99.7%,rgba(0,0,0,.03) 99.7% 100%),
    repeating-linear-gradient(to bottom,transparent 0 99.7%,rgba(0,0,0,.03) 99.7% 100%);
  opacity:.25;
  pointer-events:none;
}

.brand{
  font-size:clamp(3.8rem,8vw,7rem);
  letter-spacing:.03em;
  line-height:.9;
  text-transform:uppercase;
}

.brand small{
  display:block;
  font-family:Arial,Helvetica,sans-serif;
  font-weight:900;
  font-size:.28em;
  letter-spacing:.15em;
  margin-top:.3rem;
}

.prompt{
  font-family:Arial,Helvetica,sans-serif;
  font-weight:900;
  font-size:clamp(1.3rem,2vw,2.4rem);
  text-transform:uppercase;
  color:rgba(0,0,0,.35);
  margin-top:2rem;
}

.meta{
  font-family:"Courier New",monospace;
  font-size:clamp(.8rem,1vw,1.2rem);
  letter-spacing:.06em;
  margin-top:.5rem;
}

.links-panel{
  position:absolute;
  bottom:2rem;
  left:2rem;
  width:min(420px,calc(100% - 4rem));
}

.link-list{display:grid;gap:.6rem}

.link-btn{
  text-decoration:none;
  color:var(--white);
  background:linear-gradient(180deg,rgba(7,26,46,.8),rgba(7,24,40,.92));
  border:1px solid var(--panel-border);
  padding:.9rem 1rem;
  display:flex;
  justify-content:space-between;
  align-items:center;
  text-transform:uppercase;
  letter-spacing:.08em;
  font-family:Arial,Helvetica,sans-serif;
  font-weight:900;
  transition:transform .18s ease, box-shadow .18s ease, border-color .18s ease, background .18s ease;
  box-shadow:0 10px 26px rgba(0,0,0,.25);
  position:relative;
  overflow:hidden;
}

.link-btn::before{
  content:"";
  position:absolute;
  inset:0;
  background:linear-gradient(90deg, transparent, rgba(255,255,255,.12), transparent);
  transform:translateX(-120%);
  transition:transform .45s ease;
}

.link-btn:hover,
.link-btn:focus-visible{
  transform:translateY(-2px);
  border-color:rgba(186,245,255,.5);
  background:linear-gradient(180deg,rgba(9,34,59,.88),rgba(7,24,40,.96));
  box-shadow:0 0 20px var(--glow),0 16px 38px rgba(0,0,0,.35);
  outline:none;
}

.link-btn:hover::before,
.link-btn:focus-visible::before{
  transform:translateX(120%);
}

.index{
  font-family:"Courier New",monospace;
  color:rgba(200,255,0,.9);
  margin-right:.6rem;
}

.right-media{
  position:absolute;
  inset:0;
}

.frame{
  position:absolute;
  inset:0;
  opacity:0;
  animation:cycle 24s infinite;
}

.frame img{
  width:100%;
  height:100%;
  object-fit:cover;
  filter:saturate(1.08) contrast(1.02) brightness(.94);
}

.frame.f1{animation-delay:0s}
.frame.f2{animation-delay:6s}
.frame.f3{animation-delay:12s}
.frame.f4{animation-delay:18s}

@keyframes cycle{
  0%{opacity:0;transform:scale(1.04)}
  4%{opacity:1}
  21%{opacity:1;transform:scale(1.01)}
  25%{opacity:0;transform:scale(1)}
  100%{opacity:0}
}

/* HUD / scanlines */
.hud-overlay,
.hud-overlay::before,
.hud-overlay::after{
  position:absolute;
  inset:0;
  pointer-events:none;
}

.hud-overlay{
  z-index:6;
  background:
    linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,0) 18%),
    radial-gradient(circle at 82% 18%, rgba(170,240,255,.14), transparent 20%),
    radial-gradient(circle at 15% 80%, rgba(200,255,0,.08), transparent 18%);
}

.hud-overlay::before{
  content:"";
  background:repeating-linear-gradient(to bottom, transparent 0 3px, rgba(255,255,255,.03) 3px 4px);
  opacity:.35;
  animation:scanFlicker 4s linear infinite;
}

.hud-overlay::after{
  content:"";
  background:linear-gradient(180deg, transparent 0%, rgba(170,240,255,.08) 48%, transparent 100%);
  transform:translateY(-100%);
  animation:scanSweep 5.5s linear infinite;
  opacity:.55;
}

@keyframes scanSweep{
  0%{transform:translateY(-100%)}
  100%{transform:translateY(100%)}
}

@keyframes scanFlicker{
  0%,100%{opacity:.28}
  50%{opacity:.38}
}

.corner-lines{
  position:absolute;
  inset:1rem;
  z-index:7;
  pointer-events:none;
  border:1px solid rgba(255,255,255,.05);
}

.corner-lines::before,
.corner-lines::after{
  content:"";
  position:absolute;
  width:120px;
  height:120px;
  border-color:var(--hud-bright);
  opacity:.35;
}

.corner-lines::before{
  top:0;
  left:0;
  border-top:2px solid;
  border-left:2px solid;
}

.corner-lines::after{
  right:0;
  bottom:0;
  border-right:2px solid;
  border-bottom:2px solid;
}

/* MOBILE */
@media (orientation:portrait),(max-width:820px){
  .app{padding:0}
  .screen{
    width:100%;
    aspect-ratio:auto;
    min-height:100vh;
    display:block;
    box-shadow:none;
  }
  .right{display:none}
  .left{padding:1.5rem 1rem}
  .brand{font-size:clamp(2.8rem,16vw,4.5rem)}
  .prompt{font-size:1rem;margin-top:.5rem}
  .links-panel{position:static;margin-top:1.5rem;width:100%}
  .link-btn{padding:.85rem .9rem;font-size:.9rem}
  .intro-title{font-size:clamp(2.4rem,14vw,4rem)}
  .intro-sub{font-size:.8rem;letter-spacing:.12em}
  .intro-prompt{font-size:.8rem;padding:.8rem 1rem}
}
</style>
</head>
<body>
<div class="intro" id="intro">
  <div class="intro-panel">
    <h1 class="intro-title">Davey G</h1>
    <div class="intro-sub">Creator Hub // Enter Terminal</div>
    <div class="intro-prompt">Press any key or tap to continue</div>
  </div>
</div>

<main class="app">
  <div class="screen">
    <section class="left">
      <div>
        <div class="brand">
          Davey G
          <small>Creator Hub</small>
        </div>
        <div class="prompt">Social + Content Links</div>
        <div class="meta">||||||||| × digital terminal ▬</div>
      </div>

      <div class="links-panel">
        <div class="link-list">
          <a class="link-btn" href="https://www.youtube.com/@DaveyG" target="_blank" rel="noopener noreferrer">
            <span><span class="index">01</span>YouTube</span>
            <span>↗</span>
          </a>
          <a class="link-btn" href="https://www.instagram.com/_daveyg._/reels/" target="_blank" rel="noopener noreferrer">
            <span><span class="index">02</span>Instagram</span>
            <span>↗</span>
          </a>
          <a class="link-btn" href="https://www.tiktok.com/@daveyg920?is_from_webapp=1&sender_device=pc" target="_blank" rel="noopener noreferrer">
            <span><span class="index">03</span>TikTok</span>
            <span>↗</span>
          </a>
          <a class="link-btn" href="https://hardwareranked.com/" target="_blank" rel="noopener noreferrer">
            <span><span class="index">04</span>Hardware Ranked</span>
            <span>↗</span>
          </a>
        </div>
      </div>
    </section>

    <section class="right">
      <div class="right-media">
        <div class="frame f1"><img src="frame-1.jpg" alt="Background frame 1"></div>
        <div class="frame f2"><img src="frame-2.jpg" alt="Background frame 2"></div>
        <div class="frame f3"><img src="frame-3.jpg" alt="Background frame 3"></div>
        <div class="frame f4"><img src="frame-4.jpg" alt="Background frame 4"></div>
      </div>
      <div class="hud-overlay"></div>
      <div class="corner-lines"></div>
    </section>
  </div>
</main>

<script>
(function(){
  const intro = document.getElementById('intro');
  if (!intro) return;

  const dismiss = () => {
    intro.classList.add('hidden');
    window.removeEventListener('keydown', dismiss);
    window.removeEventListener('pointerdown', dismiss);
  };

  window.addEventListener('keydown', dismiss, { once: true });
  window.addEventListener('pointerdown', dismiss, { once: true });

  setTimeout(() => {
    if (!intro.classList.contains('hidden')) dismiss();
  }, 2800);
})();
</script>
</body>
</html>
