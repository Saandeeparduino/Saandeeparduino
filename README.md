<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Sadu Sai Saandeep — GitHub Profile</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg:       #0d1117;
    --surface1: #161b22;
    --surface2: #21262d;
    --surface3: #30363d;
    --border:   #30363d;
    --text:     #e6edf3;
    --muted:    #8b949e;
    --accent:   #00c8ff;
    --green:    #3fb950;
    --orange:   #f78166;
    --purple:   #bc8cff;
    --yellow:   #d29922;
    --teal:     #39d353;
    --mono:     'JetBrains Mono', monospace;
    --sans:     'Space Grotesk', sans-serif;
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--sans);
    font-size: 15px;
    line-height: 1.6;
    padding: 0;
    min-height: 100vh;
  }

  /* ───── HERO ───── */
  .hero {
    position: relative;
    overflow: hidden;
    padding: 64px 40px 48px;
    background: var(--surface1);
    border-bottom: 1px solid var(--border);
  }
  .hero-grid {
    max-width: 900px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 40px;
    align-items: center;
  }
  .hero-tag {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-family: var(--mono);
    font-size: 12px;
    color: var(--accent);
    border: 1px solid var(--accent);
    border-radius: 4px;
    padding: 3px 10px;
    margin-bottom: 18px;
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }
  .hero-tag span { width: 6px; height: 6px; background: var(--accent); border-radius: 50%; animation: blink 1.4s ease-in-out infinite; }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:.2} }

  .hero h1 {
    font-size: clamp(26px, 4vw, 40px);
    font-weight: 700;
    line-height: 1.15;
    color: var(--text);
    margin-bottom: 10px;
    letter-spacing: -0.5px;
  }
  .hero h1 em {
    font-style: normal;
    color: var(--accent);
  }
  .hero-sub {
    font-family: var(--mono);
    font-size: 13px;
    color: var(--muted);
    margin-bottom: 22px;
    letter-spacing: 0.02em;
  }
  .hero-quote {
    font-size: 14px;
    color: var(--green);
    border-left: 2px solid var(--green);
    padding-left: 14px;
    font-style: italic;
    margin-bottom: 28px;
    line-height: 1.5;
  }
  .hero-btns { display: flex; gap: 12px; flex-wrap: wrap; }
  .btn {
    font-family: var(--mono);
    font-size: 12px;
    letter-spacing: 0.06em;
    padding: 8px 18px;
    border-radius: 6px;
    text-decoration: none;
    font-weight: 500;
    transition: all 0.18s;
  }
  .btn-primary { background: var(--accent); color: #0d1117; }
  .btn-primary:hover { background: #33d6ff; }
  .btn-ghost { border: 1px solid var(--border); color: var(--muted); background: transparent; }
  .btn-ghost:hover { border-color: var(--accent); color: var(--accent); }

  /* Avatar / chip cluster */
  .hero-avatar-wrap { text-align: center; }
  .avatar {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent) 0%, var(--purple) 100%);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 40px;
    font-weight: 700;
    color: #0d1117;
    letter-spacing: -1px;
    margin: 0 auto 14px;
    box-shadow: 0 0 0 3px var(--surface1), 0 0 0 4px var(--border);
  }
  .status-pill {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-family: var(--mono);
    font-size: 11px;
    color: var(--green);
    background: rgba(63,185,80,.12);
    border: 1px solid rgba(63,185,80,.3);
    border-radius: 20px;
    padding: 4px 12px;
  }
  .status-pill span { width: 6px; height: 6px; background: var(--green); border-radius: 50%; }

  /* Circuit decoration */
  .hero-circuit {
    position: absolute;
    right: 0; top: 0; bottom: 0;
    width: 340px;
    opacity: 0.04;
    pointer-events: none;
  }

  /* ───── LAYOUT ───── */
  .wrapper {
    max-width: 900px;
    margin: 0 auto;
    padding: 40px 40px 60px;
  }

  /* ───── SECTION TITLES ───── */
  .sec-label {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--accent);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 18px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .sec-label::after { content:''; flex: 1; height: 1px; background: var(--border); }

  /* ───── STATS ROW ───── */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
    gap: 14px;
    margin-bottom: 40px;
  }
  .stat-card {
    background: var(--surface1);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 18px 20px;
    transition: border-color 0.18s;
  }
  .stat-card:hover { border-color: var(--accent); }
  .stat-num {
    font-family: var(--mono);
    font-size: 26px;
    font-weight: 700;
    color: var(--accent);
    line-height: 1;
    margin-bottom: 4px;
  }
  .stat-label { font-size: 12px; color: var(--muted); }

  /* ───── CHIP CLOUDS ───── */
  .chip-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 28px;
    margin-bottom: 40px;
  }
  @media(max-width:620px){ .chip-grid { grid-template-columns:1fr; } }

  .chip-group { }
  .chip-group-title {
    font-family: var(--mono);
    font-size: 12px;
    color: var(--muted);
    margin-bottom: 10px;
    letter-spacing: 0.05em;
  }
  .chips { display: flex; flex-wrap: wrap; gap: 8px; }
  .chip {
    font-family: var(--mono);
    font-size: 11.5px;
    padding: 4px 12px;
    border-radius: 5px;
    border: 1px solid;
    letter-spacing: 0.03em;
    transition: all 0.15s;
    white-space: nowrap;
  }
  .chip:hover { filter: brightness(1.2); }
  .chip-blue  { color: var(--accent); border-color: rgba(0,200,255,.25); background: rgba(0,200,255,.07); }
  .chip-green { color: var(--green);  border-color: rgba(63,185,80,.25); background: rgba(63,185,80,.07); }
  .chip-purple{ color: var(--purple); border-color: rgba(188,140,255,.25); background: rgba(188,140,255,.07); }
  .chip-orange{ color: var(--orange); border-color: rgba(247,129,102,.25); background: rgba(247,129,102,.07); }
  .chip-yellow{ color: var(--yellow); border-color: rgba(210,153,34,.25); background: rgba(210,153,34,.07); }

  /* ───── FOCUS AREAS ───── */
  .focus-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 16px;
    margin-bottom: 40px;
  }
  .focus-card {
    background: var(--surface1);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 20px;
    transition: border-color 0.18s, transform 0.18s;
  }
  .focus-card:hover { border-color: var(--accent); transform: translateY(-2px); }
  .focus-icon {
    font-size: 22px;
    margin-bottom: 10px;
    line-height: 1;
  }
  .focus-title {
    font-size: 13px;
    font-weight: 600;
    color: var(--text);
    margin-bottom: 6px;
  }
  .focus-desc {
    font-size: 12px;
    color: var(--muted);
    line-height: 1.5;
  }

  /* ───── TOOLS SECTION ───── */
  .tools-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 12px;
    margin-bottom: 40px;
  }
  .tool-item {
    display: flex;
    align-items: center;
    gap: 10px;
    background: var(--surface1);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 12px 14px;
    font-size: 12.5px;
    font-family: var(--mono);
    color: var(--muted);
    transition: all 0.16s;
  }
  .tool-item:hover { border-color: var(--accent); color: var(--text); }
  .tool-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }

  /* ───── CONTRIBUTION GRAPH FAKE ───── */
  .contrib-wrap {
    background: var(--surface1);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 24px;
    margin-bottom: 40px;
    overflow-x: auto;
  }
  .contrib-title {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--muted);
    margin-bottom: 14px;
    letter-spacing: 0.06em;
    text-transform: uppercase;
  }
  .contrib-grid {
    display: flex;
    gap: 3px;
  }
  .contrib-col { display: flex; flex-direction: column; gap: 3px; }
  .contrib-cell {
    width: 11px;
    height: 11px;
    border-radius: 2px;
    background: var(--surface2);
  }

  /* ───── CONNECT ───── */
  .connect-row {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-bottom: 40px;
  }
  .connect-card {
    display: flex;
    align-items: center;
    gap: 10px;
    background: var(--surface1);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 12px 18px;
    text-decoration: none;
    transition: border-color 0.18s;
  }
  .connect-card:hover { border-color: var(--accent); }
  .connect-icon { font-size: 20px; }
  .connect-info { }
  .connect-platform { font-size: 11px; color: var(--muted); font-family: var(--mono); }
  .connect-handle { font-size: 13px; color: var(--text); font-weight: 500; }

  /* ───── FOOTER ───── */
  .footer {
    border-top: 1px solid var(--border);
    padding: 20px 40px;
    max-width: 900px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 12px;
  }
  .footer-text { font-family: var(--mono); font-size: 11px; color: var(--muted); }
  .footer-text a { color: var(--accent); text-decoration: none; }

  /* ───── CONTRIBUTION CELL COLORS ───── */
  .l0 { background: var(--surface2); }
  .l1 { background: rgba(57,211,83,.18); }
  .l2 { background: rgba(57,211,83,.38); }
  .l3 { background: rgba(57,211,83,.62); }
  .l4 { background: rgba(57,211,83,.88); }
</style>
</head>
<body>

<!-- ══════════ HERO ══════════ -->
<section class="hero">
  <svg class="hero-circuit" viewBox="0 0 340 500" fill="none" xmlns="http://www.w3.org/2000/svg">
    <line x1="40" y1="0" x2="40" y2="500" stroke="#fff" stroke-width="1"/>
    <line x1="120" y1="0" x2="120" y2="500" stroke="#fff" stroke-width="1"/>
    <line x1="200" y1="0" x2="200" y2="500" stroke="#fff" stroke-width="1"/>
    <line x1="280" y1="0" x2="280" y2="500" stroke="#fff" stroke-width="1"/>
    <line x1="0" y1="80" x2="340" y2="80" stroke="#fff" stroke-width="1"/>
    <line x1="0" y1="180" x2="340" y2="180" stroke="#fff" stroke-width="1"/>
    <line x1="0" y1="280" x2="340" y2="280" stroke="#fff" stroke-width="1"/>
    <line x1="0" y1="380" x2="340" y2="380" stroke="#fff" stroke-width="1"/>
    <circle cx="40" cy="80" r="4" fill="#fff"/>
    <circle cx="120" cy="80" r="4" fill="#fff"/>
    <circle cx="200" cy="80" r="4" fill="#fff"/>
    <circle cx="40" cy="180" r="4" fill="#fff"/>
    <circle cx="200" cy="280" r="4" fill="#fff"/>
    <circle cx="280" cy="180" r="4" fill="#fff"/>
    <circle cx="120" cy="380" r="4" fill="#fff"/>
    <circle cx="280" cy="380" r="4" fill="#fff"/>
    <rect x="28" y="168" width="24" height="24" rx="3" fill="none" stroke="#fff" stroke-width="1"/>
    <rect x="188" y="268" width="24" height="24" rx="3" fill="none" stroke="#fff" stroke-width="1"/>
    <rect x="108" y="68" width="24" height="24" rx="3" fill="none" stroke="#fff" stroke-width="1"/>
  </svg>

  <div class="hero-grid">
    <div>
      <div class="hero-tag">
        <span></span>
        Open for collaboration
      </div>
      <h1>Sadu Sai <em>Saandeep</em></h1>
      <p class="hero-sub">// Managing Director &nbsp;·&nbsp; Embedded Systems Engineer &nbsp;·&nbsp; Open Hardware</p>
      <p class="hero-quote">"Innovation grows when knowledge is shared."</p>
      <div class="hero-btns">
        <a href="#connect" class="btn btn-primary">Connect with me</a>
        <a href="https://vishishtainnovators.com" class="btn btn-ghost">Vishishta Innovators →</a>
      </div>
    </div>
    <div class="hero-avatar-wrap">
      <div class="avatar">SS</div>
      <div class="status-pill"><span></span>Building hardware</div>
    </div>
  </div>
</section>

<!-- ══════════ BODY ══════════ -->
<div class="wrapper">

  <!-- Stats -->
  <div class="stats-row">
    <div class="stat-card">
      <div class="stat-num">10+</div>
      <div class="stat-label">Years in embedded</div>
    </div>
    <div class="stat-card">
      <div class="stat-num">50+</div>
      <div class="stat-label">PCB designs</div>
    </div>
    <div class="stat-card">
      <div class="stat-num">200+</div>
      <div class="stat-label">Students mentored</div>
    </div>
    <div class="stat-card">
      <div class="stat-num">15+</div>
      <div class="stat-label">Open-source projects</div>
    </div>
    <div class="stat-card">
      <div class="stat-num">∞</div>
      <div class="stat-label">Cups of chai ☕</div>
    </div>
  </div>

  <!-- Microcontrollers & Protocols -->
  <div class="sec-label">Microcontrollers &amp; Protocols</div>
  <div class="chip-grid">
    <div class="chip-group">
      <div class="chip-group-title">// silicon</div>
      <div class="chips">
        <span class="chip chip-blue">STM32</span>
        <span class="chip chip-blue">CH32 RISC-V</span>
        <span class="chip chip-blue">ESP32</span>
        <span class="chip chip-blue">ESP8266</span>
        <span class="chip chip-blue">AVR ATtiny</span>
        <span class="chip chip-blue">ARM Cortex-M</span>
        <span class="chip chip-blue">Py32 M0+</span>
        <span class="chip chip-blue">Arduino</span>
      </div>
    </div>
    <div class="chip-group">
      <div class="chip-group-title">// protocols &amp; comms</div>
      <div class="chips">
        <span class="chip chip-purple">BLE</span>
        <span class="chip chip-purple">LoRa</span>
        <span class="chip chip-purple">CAN Bus</span>
        <span class="chip chip-purple">UART</span>
        <span class="chip chip-purple">SPI</span>
        <span class="chip chip-purple">I2C</span>
        <span class="chip chip-purple">MQTT</span>
        <span class="chip chip-purple">Wi-Fi</span>
      </div>
    </div>
    <div class="chip-group">
      <div class="chip-group-title">// languages</div>
      <div class="chips">
        <span class="chip chip-green">C</span>
        <span class="chip chip-green">C++</span>
        <span class="chip chip-green">Embedded C</span>
        <span class="chip chip-green">Arduino</span>
        <span class="chip chip-green">Python</span>
        <span class="chip chip-green">MicroPython</span>
      </div>
    </div>
    <div class="chip-group">
      <div class="chip-group-title">// domains</div>
      <div class="chips">
        <span class="chip chip-orange">IoT</span>
        <span class="chip chip-orange">PCB Design</span>
        <span class="chip chip-orange">Industrial Auto</span>
        <span class="chip chip-orange">Robotics</span>
        <span class="chip chip-orange">Embedded AI</span>
        <span class="chip chip-orange">Open Hardware</span>
      </div>
    </div>
  </div>

  <!-- Current Focus -->
  <div class="sec-label">Current Focus Areas</div>
  <div class="focus-grid">
    <div class="focus-card">
      <div class="focus-icon">🔩</div>
      <div class="focus-title">Low-cost Dev Boards</div>
      <div class="focus-desc">Designing affordable microcontroller boards to empower students and makers globally.</div>
    </div>
    <div class="focus-card">
      <div class="focus-icon">🦾</div>
      <div class="focus-title">WCH RISC-V MCUs</div>
      <div class="focus-desc">Porting Arduino cores and building toolchains for CH32 RISC-V family of microcontrollers.</div>
    </div>
    <div class="focus-card">
      <div class="focus-icon">🧠</div>
      <div class="focus-title">Embedded AI</div>
      <div class="focus-desc">Bringing TinyML and edge inference to resource-constrained microcontrollers and dev kits.</div>
    </div>
    <div class="focus-card">
      <div class="focus-icon">📐</div>
      <div class="focus-title">Open Hardware Designs</div>
      <div class="focus-desc">Publishing fully open PCB designs, schematics, and firmware under permissive licences.</div>
    </div>
    <div class="focus-card">
      <div class="focus-icon">📚</div>
      <div class="focus-title">Education Kits</div>
      <div class="focus-desc">Building hands-on electronics kits paired with bilingual curriculum for engineering students.</div>
    </div>
    <div class="focus-card">
      <div class="focus-icon">🏭</div>
      <div class="focus-title">ERDL — R&amp;D Lab</div>
      <div class="focus-desc">Leading the Electronics Research &amp; Development Laboratory at Vishishta Innovators Pvt. Ltd.</div>
    </div>
  </div>

  <!-- Tools -->
  <div class="sec-label">Tools &amp; Software</div>
  <div class="tools-grid">
    <div class="tool-item"><span class="tool-dot" style="background:#00c8ff"></span>Arduino IDE</div>
    <div class="tool-item"><span class="tool-dot" style="background:#bc8cff"></span>MounRiver Studio</div>
    <div class="tool-item"><span class="tool-dot" style="background:#f78166"></span>STM32CubeIDE</div>
    <div class="tool-item"><span class="tool-dot" style="background:#3fb950"></span>KiCad</div>
    <div class="tool-item"><span class="tool-dot" style="background:#3fb950"></span>EasyEDA</div>
    <div class="tool-item"><span class="tool-dot" style="background:#d29922"></span>Altium Designer</div>
    <div class="tool-item"><span class="tool-dot" style="background:#00c8ff"></span>VS Code</div>
    <div class="tool-item"><span class="tool-dot" style="background:#8b949e"></span>Git &amp; GitHub</div>
  </div>

  <!-- Contribution graph -->
  <div class="sec-label">Contribution Activity</div>
  <div class="contrib-wrap">
    <div class="contrib-title">// last 365 days of hardware-making &amp; open-source commits</div>
    <div class="contrib-grid" id="cgraph"></div>
  </div>

  <!-- Connect -->
  <div class="sec-label" id="connect">Get in Touch</div>
  <div class="connect-row">
    <a class="connect-card" href="https://github.com">
      <span class="connect-icon">🐙</span>
      <div class="connect-info">
        <div class="connect-platform">GitHub</div>
        <div class="connect-handle">@YourGitHubUsername</div>
      </div>
    </a>
    <a class="connect-card" href="https://linkedin.com">
      <span class="connect-icon">💼</span>
      <div class="connect-info">
        <div class="connect-platform">LinkedIn</div>
        <div class="connect-handle">Sadu Sai Saandeep</div>
      </div>
    </a>
    <a class="connect-card" href="https://vishishtainnovators.com">
      <span class="connect-icon">🏢</span>
      <div class="connect-info">
        <div class="connect-platform">Company</div>
        <div class="connect-handle">Vishishta Innovators Pvt. Ltd.</div>
      </div>
    </a>
  </div>

</div><!-- /wrapper -->

<footer style="border-top:1px solid var(--border); padding:18px 40px; max-width:900px; margin:0 auto; display:flex; justify-content:space-between; flex-wrap:wrap; gap:10px; align-items:center;">
  <span class="footer-text">Designed for <a href="https://github.com">GitHub Profile README</a> &nbsp;·&nbsp; Vishishta Innovators Pvt. Ltd.</span>
  <span class="footer-text">Built with ❤️ from Andhra Pradesh, India 🇮🇳</span>
</footer>

<script>
/* ── Contribution graph generator ── */
(function(){
  const graph = document.getElementById('cgraph');
  const levels = [0,1,2,3,4];
  const weights = [0.38, 0.22, 0.18, 0.14, 0.08];

  function pick(){
    const r = Math.random();
    let acc = 0;
    for(let i=0;i<weights.length;i++){
      acc += weights[i];
      if(r<acc) return levels[i];
    }
    return 0;
  }

  const cols = 52;
  const rows = 7;
  const frag = document.createDocumentFragment();

  for(let c=0;c<cols;c++){
    const col = document.createElement('div');
    col.className = 'contrib-col';
    for(let r=0;r<rows;r++){
      const cell = document.createElement('div');
      cell.className = 'contrib-cell l' + pick();
      col.appendChild(cell);
    }
    frag.appendChild(col);
  }
  graph.appendChild(frag);
})();
</script>
</body>
</html>
