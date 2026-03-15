<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SYS://RECON — Linux Recon Files</title>
<link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Orbitron:wght@400;700;900&display=swap" rel="stylesheet">
<style>
  :root {
    --green: #00ff41;
    --green-dim: #00c832;
    --green-dark: #003b00;
    --green-glow: rgba(0,255,65,0.15);
    --bg: #000000;
    --card-bg: rgba(0, 15, 0, 0.85);
    --border: rgba(0,255,65,0.3);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--green);
    font-family: 'Share Tech Mono', monospace;
    min-height: 100vh;
    overflow-x: hidden;
    cursor: crosshair;
  }

  /* MATRIX RAIN CANVAS */
  #matrix-canvas {
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    z-index: 0;
    opacity: 0.18;
    pointer-events: none;
  }

  /* SCANLINES */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background: repeating-linear-gradient(
      0deg,
      transparent,
      transparent 2px,
      rgba(0,255,65,0.03) 2px,
      rgba(0,255,65,0.03) 4px
    );
    z-index: 1;
    pointer-events: none;
  }

  /* FLICKER */
  body::after {
    content: '';
    position: fixed;
    inset: 0;
    background: radial-gradient(ellipse at center, transparent 60%, rgba(0,0,0,0.7) 100%);
    z-index: 1;
    pointer-events: none;
    animation: flicker 8s infinite;
  }

  @keyframes flicker {
    0%,95%,100% { opacity: 1; }
    96% { opacity: 0.85; }
    97% { opacity: 1; }
    98% { opacity: 0.9; }
  }

  .wrapper {
    position: relative;
    z-index: 2;
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 24px 80px;
  }

  /* HEADER */
  header {
    padding: 48px 0 32px;
    text-align: center;
    border-bottom: 1px solid var(--border);
    margin-bottom: 60px;
    position: relative;
  }

  .sys-label {
    font-family: 'Share Tech Mono', monospace;
    font-size: 11px;
    letter-spacing: 4px;
    color: var(--green-dim);
    margin-bottom: 12px;
    animation: blink-text 3s infinite;
  }

  @keyframes blink-text {
    0%,49%,51%,100% { opacity: 1; }
    50% { opacity: 0; }
  }

  h1 {
    font-family: 'Orbitron', monospace;
    font-size: clamp(28px, 6vw, 64px);
    font-weight: 900;
    letter-spacing: 6px;
    text-transform: uppercase;
    color: var(--green);
    text-shadow:
      0 0 10px var(--green),
      0 0 30px var(--green),
      0 0 60px rgba(0,255,65,0.4);
    animation: glitch 6s infinite;
  }

  @keyframes glitch {
    0%,90%,100% { text-shadow: 0 0 10px var(--green), 0 0 30px var(--green), 0 0 60px rgba(0,255,65,0.4); transform: none; }
    91% { text-shadow: -3px 0 #ff0040, 3px 0 #00ffff; transform: skewX(-1deg); }
    92% { text-shadow: 3px 0 #ff0040, -3px 0 #00ffff; transform: skewX(1deg); }
    93% { text-shadow: 0 0 10px var(--green), 0 0 30px var(--green); transform: none; }
  }

  .subtitle {
    margin-top: 16px;
    font-size: 12px;
    letter-spacing: 3px;
    color: rgba(0,255,65,0.5);
  }

  .typing-cursor::after {
    content: '_';
    animation: blink-text 0.8s infinite;
  }

  /* STATUS BAR */
  .status-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 10px;
    letter-spacing: 2px;
    color: rgba(0,255,65,0.4);
    margin-bottom: 48px;
    padding-bottom: 12px;
    border-bottom: 1px solid rgba(0,255,65,0.1);
    flex-wrap: wrap;
    gap: 8px;
  }

  .status-bar span { color: var(--green); }

  /* SECTION TITLE */
  .section-title {
    font-family: 'Orbitron', monospace;
    font-size: 11px;
    letter-spacing: 5px;
    color: rgba(0,255,65,0.4);
    text-transform: uppercase;
    margin-bottom: 32px;
    display: flex;
    align-items: center;
    gap: 16px;
  }

  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(to right, var(--border), transparent);
  }

  /* CARDS GRID */
  .cards-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 20px;
  }

  .card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    padding: 28px 24px;
    position: relative;
    cursor: pointer;
    transition: all 0.2s ease;
    overflow: hidden;
    backdrop-filter: blur(4px);
  }

  .card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px;
    height: 100%;
    background: var(--green);
    box-shadow: 0 0 12px var(--green);
    opacity: 0;
    transition: opacity 0.2s;
  }

  .card::after {
    content: '';
    position: absolute;
    inset: 0;
    background: var(--green-glow);
    opacity: 0;
    transition: opacity 0.2s;
  }

  .card:hover {
    border-color: var(--green);
    transform: translateY(-2px);
    box-shadow: 0 0 20px rgba(0,255,65,0.2), inset 0 0 30px rgba(0,255,65,0.03);
  }

  .card:hover::before { opacity: 1; }
  .card:hover::after { opacity: 1; }

  .card-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 20px;
    position: relative;
    z-index: 1;
  }

  .card-path {
    font-family: 'Orbitron', monospace;
    font-size: 13px;
    font-weight: 700;
    color: var(--green);
    text-shadow: 0 0 8px rgba(0,255,65,0.5);
    letter-spacing: 1px;
    word-break: break-all;
  }

  .card-badge {
    font-size: 9px;
    letter-spacing: 2px;
    padding: 3px 8px;
    border: 1px solid currentColor;
    white-space: nowrap;
    margin-left: 12px;
    flex-shrink: 0;
  }

  .badge-crit { color: #ff3c3c; border-color: rgba(255,60,60,0.4); }
  .badge-high { color: #ff9f00; border-color: rgba(255,159,0,0.4); }
  .badge-med  { color: var(--green-dim); border-color: var(--border); }

  .card-icon {
    font-size: 32px;
    margin-bottom: 16px;
    display: block;
    filter: drop-shadow(0 0 6px rgba(0,255,65,0.4));
    position: relative;
    z-index: 1;
  }

  .card-body {
    position: relative;
    z-index: 1;
  }

  .card-desc {
    font-size: 12px;
    line-height: 1.8;
    color: rgba(0,255,65,0.7);
    margin-bottom: 16px;
  }

  .card-tag {
    display: inline-block;
    font-size: 9px;
    letter-spacing: 2px;
    color: rgba(0,255,65,0.4);
    border: 1px solid rgba(0,255,65,0.15);
    padding: 2px 8px;
    margin: 2px;
  }

  .card-tag.active {
    color: var(--green);
    border-color: rgba(0,255,65,0.4);
    box-shadow: 0 0 6px rgba(0,255,65,0.15);
  }

  .card-footer {
    margin-top: 20px;
    padding-top: 16px;
    border-top: 1px solid rgba(0,255,65,0.1);
    display: flex;
    justify-content: space-between;
    font-size: 9px;
    letter-spacing: 2px;
    color: rgba(0,255,65,0.3);
    position: relative;
    z-index: 1;
  }

  .card-footer .access { color: var(--green-dim); }

  /* TERMINAL LINE */
  .terminal-line {
    font-size: 11px;
    color: rgba(0,255,65,0.35);
    margin-bottom: 6px;
    letter-spacing: 1px;
  }

  .terminal-line .prompt { color: var(--green-dim); }
  .terminal-line .cmd { color: var(--green); }

  /* BOTTOM */
  .bottom-bar {
    margin-top: 64px;
    padding-top: 24px;
    border-top: 1px solid var(--border);
    text-align: center;
    font-size: 10px;
    letter-spacing: 3px;
    color: rgba(0,255,65,0.25);
  }

  .bottom-bar span { color: rgba(0,255,65,0.5); }

  /* CORNER DECORATIONS */
  .card .corner {
    position: absolute;
    width: 8px; height: 8px;
    border-color: var(--green);
    opacity: 0;
    transition: opacity 0.2s;
    z-index: 2;
  }
  .card:hover .corner { opacity: 0.6; }
  .corner.tl { top: 6px; left: 6px; border-top: 1px solid; border-left: 1px solid; }
  .corner.tr { top: 6px; right: 6px; border-top: 1px solid; border-right: 1px solid; }
  .corner.bl { bottom: 6px; left: 6px; border-bottom: 1px solid; border-left: 1px solid; }
  .corner.br { bottom: 6px; right: 6px; border-bottom: 1px solid; border-right: 1px solid; }

  /* ENTRY ANIMATION */
  .card {
    opacity: 0;
    transform: translateY(20px);
    animation: card-in 0.5s forwards;
  }
  .card:nth-child(1) { animation-delay: 0.1s; }
  .card:nth-child(2) { animation-delay: 0.2s; }
  .card:nth-child(3) { animation-delay: 0.3s; }
  .card:nth-child(4) { animation-delay: 0.4s; }
  .card:nth-child(5) { animation-delay: 0.5s; }
  .card:nth-child(6) { animation-delay: 0.6s; }

  @keyframes card-in {
    to { opacity: 1; transform: translateY(0); }
  }

  /* HEADER ANIMATION */
  header { animation: fade-down 0.8s ease forwards; }
  @keyframes fade-down {
    from { opacity: 0; transform: translateY(-20px); }
    to { opacity: 1; transform: translateY(0); }
  }
</style>
</head>
<body>

<canvas id="matrix-canvas"></canvas>

<div class="wrapper">

  <header>
    <div class="sys-label">// SISTEMA OPERATIVO: LINUX — MODO RECONOCIMIENTO ACTIVO</div>
    <h1>SYS://RECON</h1>
    <div class="subtitle">ARCHIVOS CRÍTICOS DEL SISTEMA <span class="typing-cursor"></span></div>
  </header>

  <div class="status-bar">
    <div>SESIÓN: <span>ROOT@DARKNET</span></div>
    <div>HOST: <span>192.168.0.1</span></div>
    <div>KERNEL: <span>6.1.0-kali</span></div>
    <div>ESTADO: <span>● COMPROMETIDO</span></div>
    <div id="clock">TIEMPO: <span>00:00:00</span></div>
  </div>

  <div class="section-title">/// VECTORES DE RECONOCIMIENTO IDENTIFICADOS</div>

  <div class="cards-grid">

    <!-- CARD 1 -->
    <div class="card">
      <div class="corner tl"></div><div class="corner tr"></div>
      <div class="corner bl"></div><div class="corner br"></div>
      <div class="card-header">
        <div class="card-path">$ /etc/shadow</div>
        <div class="card-badge badge-crit">CRÍTICO</div>
      </div>
      <span class="card-icon">🔐</span>
      <div class="card-body">
        <p class="card-desc">Contiene los hashes de contraseñas de todos los usuarios del sistema. Solo accesible por root. Objetivo primario para cracking offline y escalación de privilegios.</p>
        <div>
          <span class="card-tag active">OFFLINE CRACK</span>
          <span class="card-tag active">PRIV ESC</span>
          <span class="card-tag">HASH DUMP</span>
        </div>
      </div>
      <div class="card-footer">
        <span>PERMS: rw-r-----</span>
        <span class="access">ACCESO: ROOT</span>
      </div>
    </div>

    <!-- CARD 2 -->
    <div class="card">
      <div class="corner tl"></div><div class="corner tr"></div>
      <div class="corner bl"></div><div class="corner br"></div>
      <div class="card-header">
        <div class="card-path">$ /var/log/auth.log</div>
        <div class="card-badge badge-high">ALTO</div>
      </div>
      <span class="card-icon">📋</span>
      <div class="card-body">
        <p class="card-desc">Registro completo de intentos de autenticación. Muestra rutas de acceso fallidas y exitosas. Permite mapear patrones de login y detectar vectores de entrada utilizados.</p>
        <div>
          <span class="card-tag active">LOGIN HISTORY</span>
          <span class="card-tag active">FORENSICS</span>
          <span class="card-tag">SSH AUDIT</span>
        </div>
      </div>
      <div class="card-footer">
        <span>PERMS: rw-r-----</span>
        <span class="access">ACCESO: ADLOG</span>
      </div>
    </div>

    <!-- CARD 3 -->
    <div class="card">
      <div class="corner tl"></div><div class="corner tr"></div>
      <div class="corner bl"></div><div class="corner br"></div>
      <div class="card-header">
        <div class="card-path">$ ~/.bash_history</div>
        <div class="card-badge badge-high">ALTO</div>
      </div>
      <span class="card-icon">💻</span>
      <div class="card-body">
        <p class="card-desc">Historial de comandos ejecutados por el usuario. Revela hábitos del administrador, credenciales en texto plano, herramientas internas y rutas sensibles del sistema.</p>
        <div>
          <span class="card-tag active">CRED LEAK</span>
          <span class="card-tag active">OSINT</span>
          <span class="card-tag">ENUM</span>
        </div>
      </div>
      <div class="card-footer">
        <span>PERMS: rw-------</span>
        <span class="access">ACCESO: USER</span>
      </div>
    </div>

    <!-- CARD 4 -->
    <div class="card">
      <div class="corner tl"></div><div class="corner tr"></div>
      <div class="corner bl"></div><div class="corner br"></div>
      <div class="card-header">
        <div class="card-path">$ /etc/sudoers</div>
        <div class="card-badge badge-crit">CRÍTICO</div>
      </div>
      <span class="card-icon">⚡</span>
      <div class="card-body">
        <p class="card-desc">Define qué usuarios pueden ejecutar comandos como root. Configuraciones mal hardened permiten escalación de privilegios inmediata sin necesidad de contraseña.</p>
        <div>
          <span class="card-tag active">PRIV ESC</span>
          <span class="card-tag active">ROOT ACCESS</span>
          <span class="card-tag">MISCONFIG</span>
        </div>
      </div>
      <div class="card-footer">
        <span>PERMS: r--r-----</span>
        <span class="access">ACCESO: ROOT</span>
      </div>
    </div>

    <!-- CARD 5 -->
    <div class="card">
      <div class="corner tl"></div><div class="corner tr"></div>
      <div class="corner bl"></div><div class="corner br"></div>
      <div class="card-header">
        <div class="card-path">$ /etc/hosts</div>
        <div class="card-badge badge-med">MEDIO</div>
      </div>
      <span class="card-icon">🌐</span>
      <div class="card-body">
        <p class="card-desc">Mapeos internos de red no visibles externamente. Expone servicios ocultos, dominios internos, infraestructura privada y arquitectura de red de la organización objetivo.</p>
        <div>
          <span class="card-tag active">NETWORK MAP</span>
          <span class="card-tag active">RECON</span>
          <span class="card-tag">LATERAL</span>
        </div>
      </div>
      <div class="card-footer">
        <span>PERMS: rw-r--r--</span>
        <span class="access">ACCESO: ALL</span>
      </div>
    </div>

    <!-- CARD 6 -->
    <div class="card">
      <div class="corner tl"></div><div class="corner tr"></div>
      <div class="corner bl"></div><div class="corner br"></div>
      <div class="card-header">
        <div class="card-path">$ ~/.ssh/authorized_keys</div>
        <div class="card-badge badge-crit">CRÍTICO</div>
      </div>
      <span class="card-icon">🗝️</span>
      <div class="card-body">
        <p class="card-desc">Mecanismo de persistencia principal en Linux. Inyectar una clave pública aquí otorga acceso SSH permanente sin contraseña, sobreviviendo reinicios y rotación de credenciales.</p>
        <div>
          <span class="card-tag active">PERSISTENCE</span>
          <span class="card-tag active">BACKDOOR</span>
          <span class="card-tag">SSH KEY</span>
        </div>
      </div>
      <div class="card-footer">
        <span>PERMS: rw-------</span>
        <span class="access">ACCESO: USER</span>
      </div>
    </div>

  </div>

  <!-- TERMINAL LINES -->
  <div style="margin-top:48px; padding:20px; border:1px solid rgba(0,255,65,0.1); background:rgba(0,10,0,0.6);">
    <div class="terminal-line"><span class="prompt">root@kali:~# </span><span class="cmd">cat /etc/shadow | grep -v '!' | grep -v '*'</span></div>
    <div class="terminal-line"><span class="prompt">root@kali:~# </span><span class="cmd">sudo -l 2>/dev/null | grep NOPASSWD</span></div>
    <div class="terminal-line"><span class="prompt">root@kali:~# </span><span class="cmd">find / -name "authorized_keys" 2>/dev/null</span></div>
    <div class="terminal-line" style="color:rgba(0,255,65,0.2)">// EJECUTAR SOLO EN ENTORNOS AUTORIZADOS — USO EDUCATIVO Y CTF</div>
  </div>

  <div class="bottom-bar">
    <div>SYS://RECON v2.6 — <span>WOLVES TI</span> — KALETH CORCHO</div>
    <div style="margin-top:8px;">USO EXCLUSIVO EN ENTORNOS AUTORIZADOS · ETHICAL HACKING · CTF</div>
  </div>

</div>

<script>
// MATRIX RAIN
const canvas = document.getElementById('matrix-canvas');
const ctx = canvas.getContext('2d');

function resize() {
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
}
resize();
window.addEventListener('resize', resize);

const chars = 'アイウエオカキクケコサシスセソタチツテトナニヌネノ0123456789ABCDEF$#@!>/\\|{}[]';
const fontSize = 14;
let columns = Math.floor(canvas.width / fontSize);
let drops = Array(columns).fill(1);

function drawMatrix() {
  ctx.fillStyle = 'rgba(0,0,0,0.05)';
  ctx.fillRect(0, 0, canvas.width, canvas.height);
  ctx.fillStyle = '#00ff41';
  ctx.font = fontSize + 'px Share Tech Mono';
  for (let i = 0; i < drops.length; i++) {
    const char = chars[Math.floor(Math.random() * chars.length)];
    ctx.fillStyle = drops[i] * fontSize < 60 ? '#ffffff' : '#00ff41';
    ctx.fillText(char, i * fontSize, drops[i] * fontSize);
    if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) drops[i] = 0;
    drops[i]++;
  }
}

setInterval(drawMatrix, 40);

// CLOCK
function updateClock() {
  const now = new Date();
  const t = [now.getHours(), now.getMinutes(), now.getSeconds()]
    .map(n => String(n).padStart(2,'0')).join(':');
  document.querySelector('#clock span').textContent = t;
}
setInterval(updateClock, 1000);
updateClock();
</script>
</body>
</html>
