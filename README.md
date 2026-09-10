<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>SutureMaster PRO | Surgical Suturing Masterclass</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --navy-900: #0a1f33;
      --navy-800: #0e2b45;
      --navy-700: #123a5c;
      --green-800: #083f2f;
      --green-700: #0b5d47;
      --green-600: #0e7a5f;
      --teal: #14b8a6;
      --mint: #34d399;
      --bg: #f3f8f6;
      --card: #ffffff;
      --ink: #12212e;
      --mut: #5b6b78;
      --line: #e1ebe8;
      --soft: #eef6f3;
      --warn-bg: #fff7ed;
      --warn-line: #fed7aa;
      --gold: #d4af37;
      --gold-deep: #a67c1e;
      --gold-soft: #f9ecc4;
      --radius: 16px;
    }
    
    * { box-sizing: border-box; }
    
    /* Strict Mobile Responsiveness Resets */
    html, body { 
      scroll-behavior: smooth; 
      overflow-x: hidden; 
      width: 100%;
      max-width: 100vw;
      margin: 0;
      padding: 0;
      -webkit-text-size-adjust: 100%; 
    }
    
    body {
      background: var(--bg);
      font-family: 'Inter', 'Segoe UI', Tahoma, sans-serif;
      color: var(--ink);
      line-height: 1.6;
      text-align: left;
    }

    img, iframe, video { 
      max-width: 100%; 
      height: auto;
    }

    /* ---------- Top bar ---------- */
    .topbar {
      position: sticky;
      top: 0;
      z-index: 500;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 15px;
      padding: 12px 28px;
      background: rgba(10, 31, 51, 0.95);
      backdrop-filter: blur(8px);
      border-bottom: 1px solid rgba(255,255,255,0.08);
      width: 100%;
    }
    .brand { display: flex; align-items: center; gap: 8px; color: #fff; flex-shrink: 0; }
    .brand-mark { font-size: 22px; }
    .brand-name { font-weight: 800; font-size: clamp(14px, 2vw, 18px); letter-spacing: 0.3px; }
    .brand-name span { color: var(--mint); }
    .brand-pro {
      background: linear-gradient(90deg, var(--mint), var(--teal));
      color: var(--navy-900);
      font-size: 9px;
      font-weight: 800;
      padding: 2px 6px;
      border-radius: 20px;
      letter-spacing: 1px;
      margin-left: 4px;
    }
    .topnav { display: flex; gap: 4px; flex: 1; justify-content: center; overflow-x: auto; scrollbar-width: none; }
    .topnav::-webkit-scrollbar { display: none; }
    .topnav a {
      color: #c3d2df;
      text-decoration: none;
      font-size: 13.5px;
      font-weight: 600;
      padding: 7px 12px;
      border-radius: 8px;
      transition: background 0.25s, color 0.25s;
      white-space: nowrap;
    }
    .topnav a:hover { background: rgba(255,255,255,0.08); color: #fff; }
    
    .prof-mini {
      display: flex;
      align-items: center;
      gap: 10px;
      padding: 4px 12px 4px 5px;
      border-radius: 40px;
      background: rgba(255,255,255,0.07);
      border: 1px solid rgba(212,175,55,0.35);
      flex-shrink: 0;
    }
    .avatar {
      width: 36px; height: 36px;
      flex-shrink: 0;
      border-radius: 50%;
      display: grid;
      place-items: center;
      font-size: 12.5px;
      font-weight: 800;
      color: var(--navy-900);
      background: radial-gradient(circle at 30% 30%, #f7e6b0, var(--gold) 58%, var(--gold-deep));
    }
    .prof-id b { display: block; color: #fff; font-size: 13px; font-weight: 800; line-height: 1.3; }
    .prof-id span { display: block; font-size: 10px; color: var(--gold); font-weight: 700; text-transform: uppercase; }

    .ai-btn {
      background: linear-gradient(90deg, var(--green-600), var(--teal));
      color: #fff;
      border: none;
      padding: 10px 16px;
      border-radius: 10px;
      font-weight: 700;
      font-size: 13.5px;
      cursor: pointer;
      flex-shrink: 0;
      white-space: nowrap;
      box-shadow: 0 4px 14px rgba(14, 122, 95, 0.35);
    }

    /* ---------- Hero ---------- */
    .hero {
      background:
        radial-gradient(900px 380px at 85% -10%, rgba(20,184,166,0.35), transparent 60%),
        linear-gradient(160deg, var(--navy-900), var(--navy-800) 60%, var(--green-800));
      color: #fff;
      text-align: center;
      padding: clamp(40px, 8vw, 64px) 20px;
      border-bottom: 4px solid var(--mint);
      width: 100%;
    }
    .hero-badge {
      display: inline-block;
      background: rgba(52, 211, 153, 0.14);
      border: 1px solid rgba(52, 211, 153, 0.35);
      color: var(--mint);
      font-size: 12px;
      font-weight: 700;
      padding: 6px 14px;
      border-radius: 30px;
      margin-bottom: 18px;
    }
    .hero h1 { margin: 0 0 12px; font-size: clamp(28px, 6vw, 48px); font-weight: 800; line-height: 1.2; }
    .hero h1 .grad { background: linear-gradient(90deg, var(--mint), var(--teal)); -webkit-background-clip: text; color: transparent; }
    .hero p { max-width: 740px; margin: 0 auto 28px; color: #c9d8e4; font-size: clamp(14px, 3vw, 16px); padding: 0 10px; }
    
    .hero-faculty {
      display: inline-flex;
      align-items: center;
      gap: 13px;
      margin: 0 auto 30px;
      padding: 8px 20px 8px 9px;
      border-radius: 60px;
      text-align: left;
      background: linear-gradient(90deg, rgba(212,175,55,0.16), rgba(255,255,255,0.06));
      border: 1px solid rgba(212,175,55,0.4);
      max-width: 100%;
    }
    .avatar-lg { width: 46px; height: 46px; font-size: 16px; }
    .hf-kicker { display: block; font-size: 9px; font-weight: 800; text-transform: uppercase; color: var(--gold); }
    .hf-name { display: block; font-size: clamp(14px, 3vw, 16.5px); font-weight: 800; color: #fff; }

    .hero-stats { display: flex; justify-content: center; gap: 10px; flex-wrap: wrap; }
    .stat {
      background: rgba(255,255,255,0.06);
      border: 1px solid rgba(255,255,255,0.12);
      border-radius: 14px;
      padding: 12px 18px;
      flex: 1 1 120px;
      max-width: 200px;
    }
    .stat b { display: block; font-size: 20px; color: var(--mint); }
    .stat span { font-size: 11px; color: #b6c7d4; }

    /* ---------- Main / Layout ---------- */
    .main, .pathway, .faculty {
      width: 100%;
      max-width: 1240px;
      margin: 0 auto;
      padding: clamp(20px, 5vw, 44px) 20px;
    }

    .faculty-inner {
      background: #fff;
      border: 1px solid var(--line);
      border-radius: 20px;
      padding: clamp(20px, 5vw, 30px);
      display: flex;
      align-items: center;
      gap: 20px;
      box-shadow: 0 18px 40px rgba(10, 45, 60, 0.08);
      flex-wrap: wrap;
    }
    .faculty-seal {
      width: 80px; height: 80px;
      flex-shrink: 0;
      border-radius: 50%;
      display: grid;
      place-items: center;
      font-size: 24px;
      font-weight: 800;
      background: radial-gradient(circle at 30% 30%, #f7e6b0, var(--gold) 58%, var(--gold-deep));
      box-shadow: 0 0 0 6px #faf5e3, 0 10px 24px rgba(166, 124, 30, 0.35);
    }
    .faculty-body { flex: 1; min-width: 280px; }

    /* Fluid Grids - This makes cards responsive automatically */
    .grid { 
      display: grid; 
      grid-template-columns: repeat(auto-fit, minmax(min(100%, 280px), 1fr)); 
      gap: 20px; 
    }
    
    .acc-grid { 
      display: grid; 
      grid-template-columns: repeat(auto-fit, minmax(min(100%, 250px), 1fr)); 
      gap: 14px; 
    }

    .category h2 { font-size: clamp(20px, 4vw, 24px); display: flex; align-items: center; gap: 10px; }
    .cat-no { background: linear-gradient(135deg, var(--green-600), var(--teal)); color: #fff; padding: 4px 11px; border-radius: 8px; font-size: 13px; font-weight: 800;}
    .cat-sub { margin-left: 0; margin-bottom: 20px; color: var(--mut); font-size: 14px;}

    /* ---------- Cards ---------- */
    .card {
      background: var(--card);
      border: 1px solid var(--line);
      border-radius: var(--radius);
      padding: 20px;
      transition: transform 0.25s, box-shadow 0.25s;
      display: flex;
      flex-direction: column;
    }
    .card-top { display: flex; justify-content: space-between; align-items: center; margin-bottom: 15px;}
    .card-icon { width: 46px; height: 46px; background: var(--soft); border-radius: 12px; display: grid; place-items: center; font-size: 22px; }
    .card h3 { font-size: 17px; margin: 0 0 8px; color: var(--navy-800); }
    .card p { font-size: 13.5px; color: var(--mut); margin: 0 0 15px; flex-grow: 1;}
    .tags { display: flex; flex-wrap: wrap; gap: 6px; }
    .tags span { background: var(--soft); color: var(--green-700); font-size: 11px; padding: 4px 10px; border-radius: 20px; font-weight: 700;}

    /* ---------- Modal & Video fixes ---------- */
    .modal-backdrop {
      position: fixed;
      inset: 0;
      z-index: 1000;
      background: rgba(8, 20, 32, 0.6);
      backdrop-filter: blur(5px);
      display: grid;
      place-items: center;
      padding: 15px;
      opacity: 0;
      visibility: hidden;
      pointer-events: none;
      transition: opacity 0.3s;
    }
    .modal-backdrop.open { 
      opacity: 1; 
      visibility: visible; 
      pointer-events: auto; 
    }
    .modal {
      width: 100%;
      max-width: 940px;
      max-height: 90vh;
      overflow-y: auto;
      background: #fff;
      border-radius: 20px;
      transform: translateY(20px);
      transition: transform 0.3s;
    }
    .modal-backdrop.open .modal { transform: none; }
    
    .modal-head {
      position: sticky;
      top: 0;
      z-index: 10;
      background: linear-gradient(135deg, var(--navy-800), var(--green-800));
      padding: 20px;
      color: #fff;
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      border-radius: 20px 20px 0 0;
    }
    .modal-body { padding: 20px; }

    /* Fluid Video Containers */
    .video-wrap { width: 100%; margin-bottom: 20px; }
    .video-frame, .video-frame-sm {
      position: relative;
      width: 100%;
      aspect-ratio: 16 / 9;
      background: #000;
      border-radius: 12px;
      overflow: hidden;
    }
    .video-frame iframe, .video-frame-sm iframe {
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      border: 0;
    }

    .two-col, .comp-grid { 
      display: grid; 
      grid-template-columns: repeat(auto-fit, minmax(min(100%, 300px), 1fr)); 
      gap: 15px; 
    }
    .spec .row { display: grid; grid-template-columns: 120px 1fr; border-bottom: 1px solid var(--line); }
    .spec .k, .spec .v { padding: 10px; font-size: 13px; }
    .spec .k { background: var(--soft); font-weight: bold; color: var(--green-700); }

    /* ---------- Accordion ---------- */
    .acc-btn { width: 100%; text-align: left; padding: 15px; border: none; background: #fff; border-bottom: 1px solid var(--line); display: flex; align-items: center; gap: 15px; cursor: pointer;}
    .acc-panel { max-height: 0; overflow: hidden; transition: max-height 0.4s ease; padding: 0 15px; }
    .acc-item.open .acc-panel { max-height: 5000px; padding: 15px; }

    /* ---------- Drawer ---------- */
    .drawer {
      position: fixed; right: 0; top: 0; bottom: 0;
      width: 100%; max-width: 400px;
      background: #fff; z-index: 1001;
      transform: translateX(100%);
      transition: transform 0.3s;
      display: flex; flex-direction: column;
    }
    .drawer.open { transform: translateX(0); }

    .fab {
      position: fixed; bottom: 20px; left: 20px;
      width: 55px; height: 55px;
      border-radius: 50%; border: none;
      background: linear-gradient(135deg, var(--green-600), var(--teal));
      color: #fff; font-size: 24px; cursor: pointer;
      box-shadow: 0 10px 25px rgba(14, 122, 95, 0.4);
      z-index: 900;
    }

    /* ---------- Mobile Overrides ---------- */
    @media (max-width: 768px) {
      .topnav, .prof-id { display: none; }
      .brand-name { font-size: 16px; }
      .prof-mini { padding: 4px; }
      .ai-btn { font-size: 12px; padding: 8px 12px; }
      
      .faculty-inner { flex-direction: column; text-align: center; }
      .faculty-badges, .faculty-meta { justify-content: center; }
      
      .modal { border-radius: 12px; max-height: 95vh; }
      .modal-head { border-radius: 12px 12px 0 0; flex-direction: column; gap: 10px; }
      .modal-close { position: absolute; top: 15px; right: 15px; }
      
      .spec .row { grid-template-columns: 1fr; }
      .spec .k { border-bottom: 1px solid var(--line); }
      
      .footer-contact { flex-direction: column; }
      .contact-dot { display: none; }
    }
  </style>
</head>
<body>

  <div class="topbar">
    <div class="brand">
      <span class="brand-mark">🧵</span>
      <span class="brand-name">Suture<span>Master</span><span class="brand-pro">PRO</span></span>
    </div>
    <nav class="topnav">
      <a href="#pathway">Clinical Pathway</a>
      <a href="#cat-basic">Basic Closure</a>
      <a href="#cat-advanced">Hemostasis &amp; Advanced</a>
      <a href="#cat-ortho">Tendon Repair</a>
    </nav>
    <div class="prof-mini" aria-label="Dr. Mohanad Hamad — Medical Doctor">
      <span class="avatar">MH</span>
      <div class="prof-id">
        <b>Dr. Mohanad Hamad</b>
        <span>Medical Doctor</span>
      </div>
    </div>
    <button class="ai-btn" id="aiToggle">🧑‍⚕️ Ask Prof. Surgeon</button>
  </div>

  <header class="hero">
    <div class="hero-badge">✓ Evidence-based · Surgeon-reviewed</div>
    <h1>Surgical Suturing <span class="grad">Masterclass</span></h1>
    <p>Interactive modules covering thread selection, step-by-step technique, complication management, high-quality video demonstrations, and an interactive step walkthrough of every movement.</p>
    <div class="hero-faculty">
      <span class="avatar avatar-lg">MH</span>
      <div>
        <span class="hf-kicker">Course Director · Chief Medical Educator</span>
        <span class="hf-name">Dr. Mohanad Hamad</span>
      </div>
    </div>
    <div class="hero-stats">
      <div class="stat"><b>9</b><span>Suture modules</span></div>
      <div class="stat"><b>5</b><span>Visual steps each</span></div>
      <div class="stat"><b>USP</b><span>Size-by-site guidance</span></div>
    </div>
  </header>

  <section class="faculty" id="faculty">
    <div class="faculty-inner">
      <div class="faculty-seal">MH</div>
      <div class="faculty-body">
        <span class="faculty-kicker">Faculty · Medical Direction</span>
        <h2>Dr. Mohanad Hamad</h2>
        <div class="faculty-badges">
          <span class="faculty-badge">🎓 Lead Medical Educator</span>
          <span class="faculty-badge">⚕ Chief Medical Educator</span>
        </div>
        <p class="faculty-bio">Course director and chief medical educator behind every module on this platform — thread selection, needle choice, technique, and complication management, authored and reviewed against current surgical standards.</p>
      </div>
    </div>
  </section>

  <section class="pathway" id="pathway">
    <div class="pathway-head">
      <span class="cat-no">🧭</span>
      <h2>The Complete Clinical Pathway</h2>
    </div>
    <p class="pathway-sub">A surgeon-structured systematic guide — pre-suturing preparation, local anesthesia, the full ER-to-discharge workflow.</p>
    <div class="acc" id="pathwayCtn"></div>
  </section>

  <main class="main">
    <section class="category" id="cat-basic">
      <h2><span class="cat-no">01</span> Basic Wound Closure</h2>
      <div class="grid" id="grid-basic"></div>
    </section>

    <section class="category" id="cat-advanced">
      <h2><span class="cat-no">02</span> Hemostasis &amp; Advanced Closure</h2>
      <div class="grid" id="grid-advanced"></div>
    </section>

    <section class="category" id="cat-ortho">
      <h2><span class="cat-no">03</span> Orthopedic Tendon Repair</h2>
      <div class="grid" id="grid-ortho"></div>
    </section>
  </main>

  <footer class="footer">
    <div class="footer-inner">
      <div class="footer-brand">
        <span class="brand-mark">🧵</span>
        <span class="footer-brand-name">Suture<span>Master</span><span class="footer-pro">PRO</span></span>
      </div>
      <div class="footer-contact">
        <a class="contact-link" href="https://www.instagram.com/dr.mhn.d?igsh=bnh6bGIwOGNxbTl0" target="_blank">
          <span>@dr.mhn.d</span>
        </a>
        <span class="contact-dot"></span>
        <a class="contact-link" href="mailto:drmohanad8hamad@gmail.com">
          <span>drmohanad8hamad@gmail.com</span>
        </a>
      </div>
      <p class="footer-copy">© <span id="footYear"></span> SutureMaster PRO · Directed by <b>Dr. Mohanad Hamad</b></p>
    </div>
  </footer>

  <!-- Modal -->
  <div class="modal-backdrop" id="modalBackdrop">
    <div class="modal" id="sutureModal">
      <div class="modal-head">
        <div>
          <span class="modal-cat" id="mCat"></span>
          <h3 id="mName"></h3>
          <p id="mTagline"></p>
        </div>
        <button class="modal-close" id="modalClose">✕</button>
      </div>
      <div class="modal-body" id="modalBody"></div>
    </div>
  </div>

  <!-- AI Drawer -->
  <div class="drawer" id="drawer">
    <div class="drawer-head">
      <div>
        <b>🧑‍⚕️ Prof. Surgeon</b>
        <span>مدربك الجراحي التفاعلي</span>
      </div>
      <button id="drawerClose">✕</button>
    </div>
    <div class="drawer-chat" id="chatEl"></div>
    <div class="drawer-input">
      <input id="chatInput" placeholder="اسأل البروفيسور عن أي تقنية..." autocomplete="off">
      <button id="sendBtn">➤</button>
    </div>
  </div>
  <button class="fab" id="chatFab">🧑‍⚕️</button>

  <script>
    (function () {
      "use strict";

      // البيانات الجراحية متضمنة تماماً كما طلبت
      const SUTURES = [
        {
          id: "simple", category: "basic", icon: "🪡",
          name: "Simple Interrupted",
          tagline: "The workhorse of wound closure — independent, secure, and easy to revise.",
          videoId: "z8oWv-nVO6g", videoSource: "Geeky Medics", tags: ["Skin", "Low tension", "Versatile"],
          thread: { material: "Non-absorbable monofilament (Nylon, Prolene) for skin.", absorbable: "No for skin", sizes: "Face 5-0 / 6-0 · Trunk 4-0", needle: "Reverse-cutting, 3/8 circle", brands: "Ethilon 4-0" },
          indications: ["Linear lacerations", "Low-to-moderate tension skin closure"],
          technique: ["Enter perpendicular (90°) to the skin surface", "Mirror the bite on the opposite side", "Evert the edges with gentle traction"],
          complications: [["Cross-hatching", "Remove on schedule; avoid tight throws"], ["Wound dehiscence", "Re-assess tension"]],
          removal: "Face 5 days · Trunk 7–10 days",
          steps: [
            { t: "Load the needle", c: "Grasp the needle in the needle holder two-thirds of the way back." },
            { t: "Enter at 90°", c: "Insert the tip perpendicular to the skin surface." },
            { t: "Mirror the bite", c: "On the opposite edge take a bite of equal depth." },
            { t: "Evert & appose", c: "Draw both ends together with opposing traction." },
            { t: "Instrument tie", c: "Tie a surgeon's knot, then 3–4 square throws." }
          ]
        },
        {
          id: "running", category: "basic", icon: "🧵",
          name: "Running Continuous",
          tagline: "Fast, even-tension closure for long linear wounds and fascial closure.",
          videoId: "afUcrlHA358", videoSource: "MedSync", tags: ["Skin", "Fascia", "Speed"],
          thread: { material: "Monofilament non-absorbable", absorbable: "Optional", sizes: "Skin 3-0 / 4-0", needle: "Skin: reverse-cutting 3/8 circle", brands: "Prolene 4-0" },
          indications: ["Long linear incisions", "Low-to-moderate tension wounds"],
          technique: ["Place an anchoring knot", "Run the suture in a continuous spiral", "Keep constant tension"],
          complications: [["Total line failure", "One break compromises the whole line"]],
          removal: "Remove at 7–14 days",
          steps: [
            { t: "Anchor knot", c: "Place the first (anchoring) knot 3–5 mm beyond the wound apex." },
            { t: "First pass", c: "Take bites ~1 cm apart at equal depth." },
            { t: "Maintain tension", c: "Pull each pass snug against the previous bite." },
            { t: "Finish & tie", c: "Leave a loop at the end, and tie to the standing end." }
          ]
        },
        {
          id: "vertical", category: "basic", icon: "🪡",
          name: "Vertical Mattress",
          tagline: "Deep + superficial bites produce strong eversion for thick skin.",
          videoId: "aKwrhjVd-fg", videoSource: "BMJ Learning", tags: ["Thick skin", "Eversion"],
          thread: { material: "Non-absorbable monofilament", absorbable: "No", sizes: "Trunk 3-0", needle: "Reverse-cutting", brands: "Ethilon 2-0" },
          indications: ["Skin under high tension", "Thick or dermis-heavy skin"],
          technique: ["Far bite: enter ~1 cm from edge", "Near bite: re-enter 2–3 mm from edge"],
          complications: [["Tissue strangulation", "Loosen over-tightened throws"]],
          removal: "10-14 days",
          steps: [
            { t: "Far-far deep bite", c: "Enter 8–10 mm from the edge." },
            { t: "Near-near bite", c: "Re-enter 2–3 mm from the edge." },
            { t: "Tie & trim", c: "Tie a surgeon's knot." }
          ]
        },
        {
          id: "horizontal", category: "basic", icon: "🪡",
          name: "Horizontal Mattress",
          tagline: "Distributes tension parallel to the wound.",
          videoId: "6qF4mxB7KzM", videoSource: "Geeky Medics", tags: ["High tension"],
          thread: { material: "Non-absorbable monofilament", absorbable: "No", sizes: "Skin 2-0 / 3-0", needle: "Reverse-cutting", brands: "Prolene 2-0" },
          indications: ["High-tension wound closure", "Fascia and muscle approximation"],
          technique: ["Enter 5–10 mm from edge", "Cross wound and exit", "Re-enter on same side"],
          complications: [["Tissue ischemia", "Monitor capillary refill"]],
          removal: "10-14 days",
          steps: [
            { t: "Entry", c: "Insert needle parallel to wound." },
            { t: "Cross & exit", c: "Drive across wound." },
            { t: "Parallel tension", c: "Tie so tension runs parallel." }
          ]
        },
        {
          id: "subcuticular", category: "basic", icon: "✨",
          name: "Subcuticular (Buried Running)",
          tagline: "Cosmetic gold standard — buried in the dermis.",
          videoId: "bhN60YMyXos", videoSource: "Center for Medical Ed", tags: ["Cosmetic"],
          thread: { material: "Absorbable monofilament", absorbable: "Yes", sizes: "Face 4-0 / 5-0", needle: "Tapercut", brands: "Monocryl 4-0" },
          indications: ["Cosmetically sensitive areas"],
          technique: ["Buried anchor knot", "Run horizontally through mid-dermis"],
          complications: [["Gaping", "Add skin tape for support"]],
          removal: "No removal needed with absorbable",
          steps: [
            { t: "Bury the anchor", c: "Start with a buried knot." },
            { t: "Run in dermis", c: "Pass horizontally through mid-dermis." },
            { t: "Exit & tie", c: "Exit ~1 cm beyond wound." }
          ]
        },
        {
          id: "figure8", category: "advanced", icon: "🔁",
          name: "Figure-of-Eight",
          tagline: "Two crossing loops compress tissue.",
          videoId: "yaG_vJRD13s", videoSource: "MiniMedLessons", tags: ["Hemostasis"],
          thread: { material: "Absorbable or Non-absorbable", absorbable: "Optional", sizes: "Vessel ligation 2-0", needle: "Tapered point", brands: "Vicryl 1" },
          indications: ["Hemostatic ligation"],
          technique: ["Pass deep to bleeding point", "Cross midline", "Loop back over top"],
          complications: [["Tissue necrosis", "Apply only enough to appose"]],
          removal: "Leave in place unless infected",
          steps: [
            { t: "Deep pass", c: "Enter base of wound." },
            { t: "Cross & Form 8", c: "Cross midline twice." },
            { t: "Compress & Tie", c: "Tension both loops." }
          ]
        },
        {
          id: "purse", category: "advanced", icon: "🎯",
          name: "Purse-String",
          tagline: "Circumferential gather that inverts tissue.",
          videoId: "mvFfm0Msbwo", videoSource: "Andrew Wright", tags: ["Stoma", "Inversion"],
          thread: { material: "Non-absorbable", absorbable: "Optional", sizes: "Stoma 2-0 / 3-0", needle: "Tapered point", brands: "Prolene 3-0" },
          indications: ["Stoma creation", "Securing drains"],
          technique: ["Continuous circumferential bites", "Gather and tie"],
          complications: [["Stenosis", "Tie gently"]],
          removal: "Depends on indication",
          steps: [
            { t: "Circumferential bites", c: "Take bites around opening." },
            { t: "Gather", c: "Draw ends taut." },
            { t: "Tie", c: "Tie gently to appose." }
          ]
        },
        {
          id: "kessler", category: "ortho", icon: "🦴",
          name: "Modified Kessler",
          tagline: "Core locking suture for flexor tendon.",
          videoId: "IUk26UtHRCg", videoSource: "MedSync", tags: ["Tendon"],
          thread: { material: "Non-absorbable braided core", absorbable: "No", sizes: "Core 3-0", needle: "Round-bodied", brands: "FiberWire 3-0" },
          indications: ["Flexor tendon lacerations"],
          technique: ["Run longitudinally", "Exit transversely to lock"],
          complications: [["Adhesion", "Early protected motion"]],
          removal: "Permanent",
          steps: [
            { t: "Freshen ends", c: "Trim tendon ends." },
            { t: "Core bite", c: "Create locking loop." },
            { t: "Tie core", c: "Appose stumps." }
          ]
        },
        {
          id: "bunnell", category: "ortho", icon: "🦴",
          name: "Bunnell Tendon Repair",
          tagline: "Criss-cross multi-strand core.",
          videoId: "paXHJl_Hccc", videoSource: "Hand Surgery", tags: ["Tendon"],
          thread: { material: "Non-absorbable braided", absorbable: "No", sizes: "Core 3-0", needle: "Round-bodied", brands: "Ethibond 3-0" },
          indications: ["Tendon lacerations"],
          technique: ["Weave in criss-cross pattern"],
          complications: [["Rupture", "Protect repair for 8-12 weeks"]],
          removal: "Permanent",
          steps: [
            { t: "Criss-cross weave", c: "Diagonal weave along tendon." },
            { t: "Mirror & Tie", c: "Mirror on distal stump." }
          ]
        }
      ];

      const CATS = {
        basic:    { no: "01", grid: "grid-basic" },
        advanced: { no: "02", grid: "grid-advanced" },
        ortho:    { no: "03", grid: "grid-ortho" }
      };

      const PATHWAY = [
        {
          no: "01", title: "Pre-Suturing Preparation", sub: "Equipment, sterility, wound cleaning.",
          intro: "Preparation prevents most complications.",
          video: { label: "Intro to suturing", id: "NnKdmjX5pWU", src: "Buck Parker, M.D." },
          topics: [
            { icon: "🧰", t: "Equipment setup", items: ["Suture tray, needle holder, forceps", "Appropriate suture and needle", "Irrigation syringe"] },
            { icon: "🧤", t: "Sterile field", items: ["Aseptic technique", "Chlorhexidine prep"] },
            { icon: "💧", t: "Wound cleaning", items: ["Irrigate under pressure", "Debride devitalized tissue"] },
            { icon: "🩺", t: "Patient assessment", items: ["History mechanism", "Tetanus status"] }
          ]
        },
        {
          no: "02", title: "Local Anesthesia", sub: "Agents, indications, dosing.",
          intro: "Effective and safe anesthesia.",
          video: { label: "Infiltrating local anesthetic", id: "ssLuaeo1VTk", src: "Apprentice Doctor" },
          topics: [
            { icon: "💉", t: "Types", items: ["Lidocaine 1%", "Bupivacaine 0.25%"] },
            { icon: "⚖️", t: "Dosing", items: ["Lidocaine: max 4 mg/kg", "Bupivacaine: max 2 mg/kg"] },
            { icon: "🎯", t: "Indications", items: ["Direct infiltration", "Digital block"] },
            { icon: "✍️", t: "Technique", items: ["Aspirate before injection", "Inject slowly"] }
          ]
        }
      ];

      function renderPathway() {
        const ctn = document.getElementById("pathwayCtn");
        if (!ctn) return;
        ctn.innerHTML = PATHWAY.map(sec => {
          const topics = sec.topics ? `<div class="acc-grid">${sec.topics.map(t => 
            `<div class="topic-card"><h5>${t.icon} ${t.t}</h5><ul>${t.items.map(i => `<li>${i}</li>`).join("")}</ul></div>`
          ).join("")}</div>` : "";
          const video = sec.video ? `<div class="video-frame-sm"><iframe src="https://www.youtube-nocookie.com/embed/${sec.video.id}" allowfullscreen></iframe></div>` : "";
          return `
            <div class="acc-item">
              <button class="acc-btn"><span class="acc-num">${sec.no}</span><div class="acc-btn-tx"><b>${sec.title}</b><span>${sec.sub}</span></div></button>
              <div class="acc-panel"><div class="acc-inner"><p class="acc-intro">${sec.intro}</p>${video}${topics}</div></div>
            </div>`;
        }).join("");

        ctn.querySelectorAll(".acc-item").forEach((item, idx) => {
          const btn = item.querySelector(".acc-btn");
          btn.addEventListener("click", () => {
            const wasOpen = item.classList.contains("open");
            ctn.querySelectorAll(".acc-item.open").forEach(o => o.classList.remove("open"));
            if (!wasOpen) item.classList.add("open");
          });
          if (idx === 0) item.classList.add("open");
        });
      }

      function renderGrids() {
        Object.keys(CATS).forEach(cat => {
          const grid = document.getElementById(CATS[cat].grid);
          const items = SUTURES.filter(s => s.category === cat);
          grid.innerHTML = items.map(d => `
            <article class="card" data-id="${d.id}">
              <div class="card-top"><div class="card-icon">${d.icon}</div></div>
              <h3>${d.name}</h3><p>${d.tagline}</p>
              <div class="tags">${d.tags.map(t => `<span>${t}</span>`).join("")}</div>
            </article>`).join("");
        });
        document.querySelectorAll(".card").forEach(card => {
          card.addEventListener("click", () => openModal(card.dataset.id));
        });
      }

      function buildModal(d) {
        const specRows = [
          ["Material", d.thread.material], ["Absorbable", d.thread.absorbable],
          ["Size", d.thread.sizes], ["Needle", d.thread.needle]
        ].map(r => `<div class="row"><div class="k">${r[0]}</div><div class="v">${r[1]}</div></div>`).join("");
        
        return `
          <div class="m-sec"><div class="m-sec-title">01 Thread Specs</div><div class="spec">${specRows}</div></div>
          <div class="m-sec"><div class="m-sec-title">02 Video Demo</div>
            <div class="stepper">
              <div class="video-wrap"><div class="video-frame"><iframe src="https://www.youtube-nocookie.com/embed/${d.videoId}" allowfullscreen></iframe></div></div>
              <div class="stage-cap"><h5 id="stepTitle">${d.steps[0].t}</h5><p id="stepCap">${d.steps[0].c}</p></div>
              <div class="stage-controls">
                <button id="stepPrev" disabled>←</button>
                <div class="dots" id="stepDots"></div>
                <button id="stepNext">→</button>
              </div>
            </div>
          </div>`;
      }

      let currentSteps = [], stepIndex = 0;
      function renderStepper() {
        document.getElementById("stepTitle").textContent = currentSteps[stepIndex].t;
        document.getElementById("stepCap").textContent = currentSteps[stepIndex].c;
        document.getElementById("stepPrev").disabled = stepIndex === 0;
        document.getElementById("stepNext").disabled = stepIndex === currentSteps.length - 1;
        document.getElementById("stepDots").innerHTML = currentSteps.map((_, i) => `<span class="${i===stepIndex?'active':''}" onclick="setStep(${i})"></span>`).join("");
      }
      window.setStep = function(i) {
        if (i < 0 || i >= currentSteps.length) return;
        stepIndex = i;
        renderStepper();
      };

      function openModal(id) {
        const d = SUTURES.find(s => s.id === id);
        if (!d) return;
        document.getElementById("mName").textContent = d.name;
        document.getElementById("modalBody").innerHTML = buildModal(d);
        currentSteps = d.steps; stepIndex = 0;
        renderStepper();
        document.getElementById("stepPrev").addEventListener("click", () => setStep(stepIndex - 1));
        document.getElementById("stepNext").addEventListener("click", () => setStep(stepIndex + 1));
        document.getElementById("modalBackdrop").classList.add("open");
        document.body.style.overflow = "hidden";
      }

      document.getElementById("modalClose").addEventListener("click", () => {
        document.getElementById("modalBackdrop").classList.remove("open");
        document.body.style.overflow = "";
      });

      // AI Drawer Mock for GitHub Pages
      const drawer = document.getElementById("drawer");
      const chatEl = document.getElementById("chatEl");
      const chatInput = document.getElementById("chatInput");
      const sendBtn = document.getElementById("sendBtn");

      function toggleDrawer() {
        drawer.classList.toggle("open");
        if (drawer.classList.contains("open") && chatEl.innerHTML === "") {
          chatEl.innerHTML = `<div class="msg msg-ai">أهلاً بك يا دكتور مهند في SutureMaster PRO. يمكنك سؤالي عن أي تقنية جراحية وسأقوم بشرحها لك.</div>`;
        }
      }

      document.getElementById("aiToggle").addEventListener("click", toggleDrawer);
      document.getElementById("chatFab").addEventListener("click", toggleDrawer);
      document.getElementById("drawerClose").addEventListener("click", toggleDrawer);

      sendBtn.addEventListener("click", () => {
        const text = chatInput.value.trim();
        if (!text) return;
        chatEl.innerHTML += `<div class="msg msg-user">${text}</div>`;
        chatInput.value = "";
        chatEl.innerHTML += `<div class="msg msg-ai">أهلاً بك يا دكتور. هذا الموقع مستضاف حالياً كصفحة ثابتة (Static Page) على GitHub Pages، لذلك فإن محرك الذكاء الاصطناعي يعمل في وضع المحاكاة التجريبية.</div>`;
        chatEl.scrollTop = chatEl.scrollHeight;
      });

      document.getElementById("footYear").textContent = new Date().getFullYear();
      renderPathway();
      renderGrids();
    })();
  </script>
</body>
</html>
هذا الكود عندما اضغط على الفديو يظهر لي خطأ ولا يعمل
