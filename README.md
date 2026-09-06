# altair-vega
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>Altair &amp; Vega</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
  html { scroll-behavior: smooth; }
  body {
    background: #05060f;
    color: #e8e8f0;
    font-family: Georgia, 'Times New Roman', serif;
    overflow-x: hidden;
    -webkit-font-smoothing: antialiased;
  }
  #stars {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    z-index: 0; pointer-events: none;
  }
  #sky {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    z-index: 1; pointer-events: none;
    background: radial-gradient(ellipse at 50% 30
    <!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>Altair &amp; Vega</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
  html { scroll-behavior: smooth; }
  body {
    background: #05060f;
    color: #e8e8f0;
    font-family: Georgia, 'Times New Roman', serif;
    overflow-x: hidden;
    -webkit-font-smoothing: antialiased;
  }
  #stars {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    z-index: 0; pointer-events: none;
  }
  #sky {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    z-index: 1; pointer-events: none;
    background: radial-gradient(ellipse at 50% 30%, rgba(40,30,80,0.35), transparent 60%);
  }
  #scene {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    z-index: 2; pointer-events: none;
  }
  .panel {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 8vh 8vw;
    text-align: center;
    position: relative;
    z-index: 3;
  }
  .panel p {
    font-size: clamp(18px, 5.2vw, 26px);
    line-height: 1.7;
    max-width: 34ch;
    opacity: 0;
    transform: translateY(18px);
    transition: opacity 1.1s ease, transform 1.1s ease;
    text-shadow: 0 0 18px rgba(0,0,0,0.85);
  }
  .panel p.show { opacity: 1; transform: translateY(0); }
  .panel .title {
    font-size: clamp(30px, 9vw, 46px);
    letter-spacing: 0.04em;
    font-style: italic;
  }
  .panel .sub {
    font-size: clamp(14px, 4vw, 18px);
    opacity: 0.7;
    margin-top: 1.2em;
  }
  .hint {
    position: fixed; bottom: 5vh; left: 0; width: 100%;
    text-align: center; z-index: 4;
    font-size: 14px; letter-spacing: 0.2em; text-transform: uppercase;
    opacity: 0.5; animation: pulse 2s infinite;
  }
  @keyframes pulse { 0%,100% { opacity: 0.25; } 50% { opacity: 0.6; } }
  .river {
    position: absolute; left: 0; width: 100%; height: 2px;
    background: linear-gradient(90deg, transparent, rgba(120,160,220,0.7), transparent);
    box-shadow: 0 0 12px rgba(120,160,220,0.5);
    opacity: 0; transition: opacity 1.5s ease;
  }
  .silhouette {
    position: absolute; bottom: 38vh; width: 46px; height: 70px;
    opacity: 0; transition: opacity 1.5s ease;
    background: radial-gradient(ellipse at 50% 30%, #1a1a2e, transparent 70%);
    filter: blur(0.5px);
  }
  .silhouette.left { left: 22%; }
  .silhouette.right { right: 22%; }
  .bridge {
    position: absolute; left: 22%; right: 22%; bottom: 38vh; height: 70px;
    opacity: 0; transition: opacity 2s ease;
  }
  .bridge span {
    position: absolute; top: 50%; width: 6px; height: 6px; border-radius: 50%;
    background: #ffd27a; box-shadow: 0 0 8px #ffd27a;
    transform: translate(-50%, -50%);
  }
  .final p { font-style: italic; }
</style>
</head>
<body>
<canvas id="stars"></canvas>
<div id="sky"></div>
<div id="scene">
  <div class="river" id="river"></div>
  <div class="silhouette left" id="silLeft"></div>
  <div class="silhouette right" id="silRight"></div>
  <div class="bridge" id="bridge"></div>
</div>

<section class="panel" data-text="0">
  <div>
    <p class="title show">Altair &amp; Vega</p>
    <p class="sub show">a story about two stars, and a river that never ends</p>
  </div>
</section>

<section class="panel"><p>Once, the sky was one unbroken light.</p></section>
<section class="panel"><p>Then something broke it apart and scattered the pieces across the dark.</p></section>
<section class="panel"><p>Most of them gave up and just shone where they landed.</p></section>
<section class="panel"><p>But two of them never stopped trying to find their way back to each other.</p></section>

<section class="panel"><p>They called her Vega. She wove light into cloth for the gods, and her loom never went quiet.</p></section>
<section class="panel"><p>They called him Altair. He tended the herds at the edge of the sky, quiet and steady, always watching the horizon.</p></section>
<section class="panel"><p>They lived on opposite sides of a river that had no beginning and no end.</p></section>

<section class="panel"><p>One night the river thinned. Just for a moment.</p></section>
<section class="panel"><p>And they saw each other across it.</p></section>
<section class="panel"><p>They did not speak. They did not need to.</p></section>
<section class="panel"><p>They just stood on their own banks, looking at the light on the other side — and both of them knew, without a word, that this was the person they had been waiting for.</p></section>

<section class="panel"><p>But the river came back. It always does.</p></section>
<section class="panel"><p>So they went back to their lives. She to her loom. He to his cattle.</p></section>
<section class="panel"><p>And every night they looked across, and the distance never got smaller, and neither of them ever stopped looking.</p></section>

<section class="panel"><p>The story says that once a year, on the seventh night of the seventh month, the magpies build a bridge across the river with their wings.</p></section>
<section class="panel"><p>And the two stars finally meet.</p></section>
<section class="panel"><p>But here is the part nobody tells you.</p></section>
<section class="panel"><p>The bridge is not the point.</p></section>
<section class="panel"><p>The point is that they kept looking. Every single night, for years, across a river that never moved.</p></section>

<section class="panel final">
  <p>I am on one side of a river right now.<br>You are on the other.<br><br>I do not know when the bridge gets built.<br>But I know I am still looking.<br><br>This story is between us.</p>
</section>

<div class="hint" id="hint">scroll ↓</div>

<script>
  // Starfield
  const canvas = document.getElementById('stars');
  const ctx = canvas.getContext('2d');
  let stars = [];
  function resize() {
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
    stars = [];
    const count = Math.floor((canvas.width * canvas.height) / 9000);
    for (let i = 0; i < count; i++) {
      stars.push({
        x: Math.random() * canvas.width,
        y: Math.random() * canvas.height,
        r: Math.random() * 1.4 + 0.2,
        a: Math.random(),
        s: Math.random() * 0.02 + 0.005
      });
    }
  }
  resize();
  window.addEventListener('resize', resize);
  function drawStars() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    for (const st of stars) {
      st.a += st.s;
      const tw = 0.4 + 0.6 * Math.abs(Math.sin(st.a));
      ctx.beginPath();
      ctx.arc(st.x, st.y, st.r, 0, Math.PI * 2);
      ctx.fillStyle = 'rgba(230,230,255,' + tw + ')';
      ctx.fill();
    }
    requestAnimationFrame(drawStars);
  }
  drawStars();

  // Sound (Web Audio, no files)
  let audioCtx = null;
  let soundReady = false;
  function unlockAudio() {
    if (soundReady) return;
    try {
      audioCtx = new (window.AudioContext || window.webkitAudioContext)();
      soundReady = true;
    } catch (e)
  }
  document.addEventListener('touchstart', unlockAudio, { once: true });
  document.addEventListener('click', unlockAudio, { once: true });

  function playChime() {
    if (!audioCtx) return;
    const now = audioCtx.currentTime;
    [523.25, 659.25, 783.99].forEach((freq, i) => {
      const osc = audioCtx.createOscillator();
      const gain = audioCtx.createGain();
      osc.type = 'sine';
      osc.frequency.value = freq;
      gain.gain.setValueAtTime(0, now + i * 0.12);
      gain.gain.linearRampToValueAtTime(0.18, now + i * 0.12 + 0.05);
      gain.gain.exponentialRampToValueAtTime(0.001, now + i * 0.12 + 1.4);
      osc.connect(gain);
      gain.connect(audioCtx.destination);
      osc.start(now + i * 0.12);
      osc.stop(now + i * 0.12 + 1.5);
    });
  }

  // Bridge dots
  const bridge = document.getElementById('bridge');
  for (let i = 0; i < 9; i++) {
    const s = document.createElement('span');
    s.style.left = (i * 12.5) + '%';
    s.style.transitionDelay = (i * 0.15) + 's';
    bridge.appendChild(s);
  }

  // Scroll reveal
  const panels = document.querySelectorAll('.panel');
  const river = document.getElementById('river');
  const silL = document.getElementById('silLeft');
  const silR = document.getElementById('silRight');
  const hint = document.getElementById('hint');
  let bridgePlayed = false;

  const io = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.querySelectorAll('p').forEach(p => p.classList.add('show'));
      }
    });
  }, { threshold: 0.4 });
  panels.forEach(p => io.observe(p));

  function onScroll() {
    const scrollY = window.scrollY;
    const vh = window.innerHeight;
    const docH = document.documentElement.scrollHeight - vh;
    const prog = Math.min(1, scrollY / docH);

    if (prog > 0.02) hint.style.opacity = '0'; else hint.style.opacity = '0.5';

    // River appears around 55%
    if (prog > 0.55) {
      river.style.opacity = Math.min(1, (prog - 0.55) * 4);
      river.style.top = '62vh';
    } else {
      river.style.opacity = 0;
    }

    // Silhouettes around 60%
    if (prog > 0.60) {
      const o = Math.min(1, (prog - 0.60) * 5);
      silL.style.opacity = o;
      silR.style.opacity = o;
    } else {
      silL.style.opacity = 0;
      silR.style.opacity = 0;
    }

    // Bridge around 78%
    if (prog > 0.78) {
      bridge.style.opacity = Math.min(1, (prog - 0.78) * 6);
      if (!bridgePlayed && soundReady) {
        bridgePlayed = true;
        playChime();
      }
    } else {
      bridge.style.opacity = 0;
    }
  }
  window.addEventListener('scroll', onScroll, { passive: true });
  onScroll();
</script>
</body>
</html>