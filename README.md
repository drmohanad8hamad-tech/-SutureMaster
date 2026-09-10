<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
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
    html { scroll-behavior: smooth; overflow-x: hidden; -webkit-text-size-adjust: 100%; }
    
    body {
      margin: 0;
      background: var(--bg);
      font-family: 'Inter', 'Segoe UI', Tahoma, sans-serif;
      color: var(--ink);
      line-height: 1.6;
      text-align: left;
      /* تم إضافة Flexbox لجعل الواجهة تملأ ارتفاع الشاشة */
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    /* ---------- Top bar ---------- */
    .topbar {
      position: sticky;
      top: 0;
      z-index: 500;
      display: flex;
      align-items: center;
      gap: 24px;
      padding: 12px 4vw; /* هوامش ديناميكية */
      background: rgba(10, 31, 51, 0.92);
      backdrop-filter: blur(8px);
      border-bottom: 1px solid rgba(255,255,255,0.08);
    }
    .brand { display: flex; align-items: center; gap: 10px; color: #fff; }
    .brand-mark { font-size: 22px; }
    .brand-name { font-weight: 800; font-size: 18px; letter-spacing: 0.3px; }
    .brand-name span { color: var(--mint); }
    .brand-pro {
      background: linear-gradient(90deg, var(--mint), var(--teal));
      color: var(--navy-900);
      font-size: 10px;
      font-weight: 800;
      padding: 2px 7px;
      border-radius: 20px;
      letter-spacing: 1px;
    }
    .topnav { display: flex; gap: 4px; flex: 1; min-width: 0; justify-content: center; }
    .topnav a {
      color: #c3d2df;
      text-decoration: none;
      font-size: 13.5px;
      font-weight: 600;
      padding: 7px 12px;
      border-radius: 8px;
      transition: background 0.25s, color 0.25s;
    }
    .topnav a:hover { background: rgba(255,255,255,0.08); color: #fff; }
    .ai-btn {
      background: linear-gradient(90deg, var(--green-600), var(--teal));
      color: #fff;
      border: none;
      padding: 10px 16px;
      border-radius: 10px;
      font-weight: 700;
      font-size: 13.5px;
      cursor: pointer;
      font-family: inherit;
      box-shadow: 0 4px 14px rgba(14, 122, 95, 0.35);
      transition: transform 0.2s, box-shadow 0.2s;
    }
    .ai-btn:hover { transform: translateY(-1px); box-shadow: 0 6px 18px rgba(14, 122, 95, 0.45); }

    /* ---------- Hero ---------- */
    .hero {
      background:
        radial-gradient(900px 380px at 85% -10%, rgba(20,184,166,0.35), transparent 60%),
        radial-gradient(700px 320px at 10% -10%, rgba(14,122,95,0.45), transparent 60%),
        linear-gradient(160deg, var(--navy-900), var(--navy-800) 60%, var(--green-800));
      color: #fff;
      text-align: center;
      padding: 8vh 4vw 6vh; /* لتتجاوب مع طول وعرض الشاشة */
      border-bottom: 4px solid var(--mint);
    }
    .hero-badge {
      display: inline-block;
      background: rgba(52, 211, 153, 0.14);
      border: 1px solid rgba(52, 211, 153, 0.35);
      color: var(--mint);
      font-size: 12.5px;
      font-weight: 700;
      letter-spacing: 0.5px;
      padding: 6px 14px;
      border-radius: 30px;
      margin-bottom: 18px;
    }
    .hero h1 { margin: 0 0 12px; font-size: clamp(30px, 5vw, 48px); font-weight: 800; letter-spacing: -0.5px; }
    .hero h1 .grad { background: linear-gradient(90deg, var(--mint), var(--teal)); -webkit-background-clip: text; background-clip: text; color: transparent; }
    .hero p { max-width: 900px; margin: 0 auto 28px; color: #c9d8e4; font-size: 16.5px; }
    .hero-stats { display: flex; justify-content: center; gap: 14px; flex-wrap: wrap; }
    .stat {
      background: rgba(255,255,255,0.06);
      border: 1px solid rgba(255,255,255,0.12);
      border-radius: 14px;
      padding: 14px 22px;
      min-width: 130px;
    }
    .stat b { display: block; font-size: 22px; color: var(--mint); }
    .stat span { font-size: 12px; color: #b6c7d4; }

    /* ---------- Main / categories ---------- */
    .main { 
      flex: 1; /* لتأخذ المساحة المتبقية وتدفع الفوتر للأسفل */
      width: 100%;
      max-width: 100%; /* تملأ الشاشة بالكامل */
      margin: 0 auto; 
      padding: 44px 4vw 20px; 
    }
    .category { margin-bottom: 52px; }
    .category h2 { display: flex; align-items: center; gap: 12px; font-size: 24px; font-weight: 800; color: var(--navy-800); margin: 0 0 4px; }
    .cat-no {
      background: linear-gradient(135deg, var(--green-600), var(--teal));
      color: #fff;
      font-size: 13px;
      font-weight: 800;
      padding: 4px 11px;
      border-radius: 8px;
    }
    .cat-sub { color: var(--mut); margin: 0 0 20px 40px; font-size: 14.5px; }
    
    /* Auto-fit ليملأ الأعمدة في الشاشات العريضة تلقائياً */
    .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 20px; }

    /* ---------- Cards ---------- */
    .card {
      position: relative;
      background: var(--card);
      border: 1px solid var(--line);
      border-radius: var(--radius);
      padding: 22px 20px 18px;
      cursor: pointer;
      transition: transform 0.25s, box-shadow 0.25s, border-color 0.25s;
      overflow: hidden;
      display: flex;
      flex-direction: column;
    }
    .card::before {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 4px;
      background: linear-gradient(90deg, var(--green-600), var(--teal));
      opacity: 0.85;
    }
    .card:hover { transform: translateY(-5px); box-shadow: 0 16px 34px rgba(10, 45, 60, 0.14); border-color: var(--teal); }
    .card:focus-visible { outline: 3px solid var(--teal); outline-offset: 2px; }
    .card-top { display: flex; align-items: center; justify-content: space-between; margin-bottom: 10px; }
    .card-icon {
      width: 46px; height: 46px;
      display: grid; place-items: center;
      font-size: 22px;
      background: var(--soft);
      border: 1px solid var(--line);
      border-radius: 12px;
      transition: background 0.25s, transform 0.25s;
    }
    .card:hover .card-icon { background: #e0f2ea; transform: scale(1.06); }
    .card-arrow { color: var(--teal); font-size: 18px; opacity: 0; transform: translateX(-6px); transition: opacity 0.25s, transform 0.25s; }
    .card:hover .card-arrow { opacity: 1; transform: none; }
    .card h3 { margin: 0 0 6px; font-size: 17px; font-weight: 800; color: var(--navy-800); }
    .card p { margin: 0 0 14px; font-size: 13.5px; color: var(--mut); flex: 1; }
    .tags { display: flex; flex-wrap: wrap; gap: 6px; }
    .tags span {
      background: var(--soft);
      color: var(--green-700);
      border: 1px solid var(--line);
      font-size: 11.5px;
      font-weight: 700;
      padding: 3px 9px;
      border-radius: 20px;
    }

    /* ---------- Modal ---------- */
    .modal-backdrop {
      position: fixed;
      inset: 0;
      z-index: 1000;
      background: rgba(8, 20, 32, 0.6);
      backdrop-filter: blur(5px);
      display: grid;
      place-items: center;
      padding: 20px;
      opacity: 0;
      visibility: hidden;
      pointer-events: none;
      transition: opacity 0.25s, visibility 0.25s;
    }
    .modal-backdrop.open { 
      opacity: 1; 
      visibility: visible; 
      pointer-events: auto; 
    }
    .modal-backdrop[hidden] {
      display: none !important;
    }
    
    .modal {
      width: min(1200px, 95vw); /* توسيع العرض في الشاشات الكبيرة */
      max-height: 90vh;
      overflow-y: auto;
      background: #fff;
      border-radius: 20px;
      box-shadow: 0 30px 80px rgba(0,0,0,0.35);
      transform: translateY(16px) scale(0.98);
      transition: transform 0.3s;
    }
    .modal-backdrop.open .modal { transform: none; }
    .modal-head {
      position: sticky;
      top: 0;
      z-index: 5;
      background: linear-gradient(135deg, var(--navy-800), var(--green-800));
      color: #fff;
      padding: 24px 28px 22px;
      border-radius: 20px 20px 0 0;
      display: flex;
      justify-content: space-between;
      gap: 16px;
    }
    .modal-head h3 { margin: 6px 0 4px; font-size: 24px; font-weight: 800; }
    .modal-head p { margin: 0; color: #b9cddb; font-size: 14px; }
    .modal-cat {
      display: inline-block;
      background: rgba(52,211,153,0.18);
      border: 1px solid rgba(52,211,153,0.4);
      color: var(--mint);
      font-size: 11px;
      font-weight: 800;
      letter-spacing: 0.6px;
      padding: 3px 10px;
      border-radius: 20px;
      text-transform: uppercase;
    }
    .modal-close {
      background: rgba(255,255,255,0.12);
      color: #fff;
      border: none;
      width: 38px; height: 38px;
      border-radius: 10px;
      font-size: 16px;
      cursor: pointer;
      flex-shrink: 0;
      transition: background 0.2s;
    }
    .modal-close:hover { background: rgba(255,255,255,0.25); }
    .modal-body { padding: 26px 28px 34px; }

    .m-sec { margin-bottom: 30px; }
    .m-sec-title { display: flex; align-items: center; gap: 10px; font-size: 16.5px; font-weight: 800; color: var(--navy-800); margin: 0 0 14px; }
    .m-sec-title .num {
      background: linear-gradient(135deg, var(--green-600), var(--teal));
      color: #fff;
      width: 26px; height: 26px;
      display: grid; place-items: center;
      border-radius: 8px;
      font-size: 12px;
      font-weight: 800;
    }

    .spec { border: 1px solid var(--line); border-radius: 12px; overflow: hidden; }
    .spec .row { display: grid; grid-template-columns: 150px 1fr; }
    .spec .row + .row { border-top: 1px solid var(--line); }
    .spec .k { background: var(--soft); font-weight: 700; color: var(--green-700); padding: 10px 16px; font-size: 13px; }
    .spec .v { padding: 10px 16px; font-size: 13.5px; }

    .two-col { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
    .panel { background: #fafdfb; border: 1px solid var(--line); border-radius: 12px; padding: 16px 18px; }
    .panel h4 { margin: 0 0 10px; font-size: 13px; font-weight: 800; color: var(--green-700); text-transform: uppercase; letter-spacing: 0.4px; }
    .panel ul, .panel ol { margin: 0; padding-inline-start: 20px; }
    .panel li { margin-bottom: 7px; font-size: 13.5px; }
    .reminder {
      margin-top: 14px;
      background: var(--warn-bg);
      border: 1px solid var(--warn-line);
      border-inline-start: 4px solid #f59e0b;
      border-radius: 10px;
      padding: 12px 16px;
      font-size: 13.5px;
    }
    .reminder b { color: #b45309; }
    .clinic-note {
      margin-top: 14px;
      background: #ecfdf5;
      border: 1px solid #a7f3d0;
      border-inline-start: 4px solid var(--green-600);
      border-radius: 10px;
      padding: 12px 16px;
      font-size: 13.5px;
      color: #065f46;
    }

    .comp-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 14px; }
    .comp {
      border: 1px solid var(--line);
      border-radius: 12px;
      padding: 14px 16px;
      background: #fff;
    }
    .comp .c-name { font-weight: 800; font-size: 13.5px; color: #b91c1c; display: flex; align-items: center; gap: 7px; }
    .comp .c-name::before { content: "⚠"; font-size: 13px; }
    .comp .c-mgmt { font-size: 13px; color: var(--mut); margin-top: 6px; }
    .comp .c-mgmt b { color: var(--green-700); }

    /* ---------- Video demo + interactive stepper ---------- */
    .video-wrap { margin-bottom: 18px; }
    .video-frame {
      position: relative;
      aspect-ratio: 16 / 9;
      width: 100%;
      max-width: 1000px; /* تكبير الفيديو */
      margin: 0 auto;
      border-radius: 14px;
      overflow: hidden;
      background: #0a1f33;
      border: 1px solid var(--line);
      box-shadow: 0 12px 30px rgba(10, 45, 60, 0.18);
    }
    .video-frame iframe {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      border: 0;
    }
    .video-meta {
      text-align: center;
      font-size: 12.5px;
      color: var(--mut);
      margin: 10px auto 0;
      max-width: 640px;
    }
    .video-meta b { color: var(--green-700); }
    .stage-cap { text-align: center; margin-top: 16px; min-height: 78px; }
    .stage-cap h5 { margin: 0 0 6px; font-size: 16.5px; color: var(--navy-800); font-weight: 800; }
    .stage-cap p { margin: 0 auto; max-width: 600px; font-size: 13.5px; color: var(--mut); }
    .stage-controls { display: flex; align-items: center; justify-content: center; gap: 18px; margin-top: 16px; }
    .stage-controls button {
      width: 42px; height: 42px;
      border-radius: 50%;
      border: 1px solid var(--line);
      background: #fff;
      color: var(--green-700);
      font-size: 16px;
      cursor: pointer;
      transition: background 0.2s, transform 0.2s, opacity 0.2s;
      display: grid; place-items: center;
    }
    .stage-controls button:hover:not(:disabled) { background: var(--soft); transform: scale(1.08); }
    .stage-controls button:disabled { opacity: 0.3; cursor: default; }
    .dots { display: flex; gap: 8px; }
    .dots span {
      width: 9px; height: 9px;
      border-radius: 50%;
      background: #c6d9d2;
      cursor: pointer;
      transition: background 0.2s, transform 0.2s;
    }
    .dots span:hover { background: var(--teal); }
    .dots span.active { background: var(--green-600); transform: scale(1.3); }
    .progress { height: 6px; background: #e4efeb; border-radius: 6px; margin-top: 16px; overflow: hidden; }
    .progress .bar {
      height: 100%;
      width: 0%;
      background: linear-gradient(90deg, var(--green-600), var(--teal));
      transition: width 0.3s ease;
    }
    .step-counter { text-align: center; font-size: 12px; color: var(--mut); margin-top: 8px; }
    .anim { animation: stepIn 0.28s ease; }
    @keyframes stepIn {
      from { opacity: 0; transform: translateY(8px); }
      to { opacity: 1; transform: none; }
    }

    /* ---------- Faculty / professor branding ---------- */
    .prof-mini {
      display: flex;
      align-items: center;
      gap: 10px;
      padding: 4px 12px 4px 5px;
      border-radius: 40px;
      background: rgba(255,255,255,0.07);
      border: 1px solid rgba(212,175,55,0.35);
    }
    .avatar {
      width: 36px; height: 36px;
      flex-shrink: 0;
      border-radius: 50%;
      display: grid;
      place-items: center;
      font-size: 12.5px;
      font-weight: 800;
      letter-spacing: 0.5px;
      color: var(--navy-900);
      background: radial-gradient(circle at 30% 30%, #f7e6b0, var(--gold) 58%, var(--gold-deep));
      box-shadow: 0 0 0 2px rgba(212,175,55,0.4);
    }
    .avatar-lg { width: 46px; height: 46px; font-size: 16px; }
    .prof-id b { display: block; color: #fff; font-size: 13px; font-weight: 800; letter-spacing: 0.2px; line-height: 1.3; }
    .prof-id span { display: block; font-size: 10px; color: var(--gold); font-weight: 700; letter-spacing: 1px; text-transform: uppercase; }

    /* Hero faculty greeting */
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
      backdrop-filter: blur(6px);
    }
    .hf-kicker { display: block; font-size: 10px; font-weight: 800; letter-spacing: 1.6px; text-transform: uppercase; color: var(--gold); }
    .hf-name { display: block; font-size: 16.5px; font-weight: 800; color: #fff; letter-spacing: 0.3px; }

    /* Dedicated faculty section */
    .faculty { padding: 30px 4vw 6px; width: 100%; max-width: 100%; }
    .faculty-inner {
      position: relative;
      overflow: hidden;
      max-width: 100%;
      margin: 0 auto;
      background: #fff;
      border: 1px solid var(--line);
      border-radius: 20px;
      padding: 30px 34px;
      display: flex;
      align-items: center;
      gap: 30px;
      box-shadow: 0 18px 40px rgba(10, 45, 60, 0.10);
    }
    .faculty-inner::before {
      content: "";
      position: absolute;
      inset: 0 auto 0 0;
      width: 6px;
      background: linear-gradient(180deg, var(--gold), var(--teal));
    }
    .faculty-seal {
      width: 92px; height: 92px;
      flex-shrink: 0;
      border-radius: 50%;
      display: grid;
      place-items: center;
      font-size: 26px;
      font-weight: 800;
      letter-spacing: 1px;
      color: var(--navy-900);
      background: radial-gradient(circle at 30% 30%, #f7e6b0, var(--gold) 58%, var(--gold-deep));
      box-shadow: 0 0 0 6px #faf5e3, 0 10px 24px rgba(166, 124, 30, 0.35);
    }
    .faculty-kicker { font-size: 11px; font-weight: 800; letter-spacing: 1.8px; text-transform: uppercase; color: var(--gold-deep); }
    .faculty-body h2 { margin: 4px 0 8px; font-size: 26px; font-weight: 800; color: var(--navy-800); letter-spacing: -0.3px; }
    .faculty-badges { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 10px; }
    .faculty-badge {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      background: linear-gradient(135deg, #fdf6e3, var(--gold-soft));
      border: 1px solid rgba(212,175,55,0.5);
      color: var(--gold-deep);
      font-size: 11.5px;
      font-weight: 800;
      letter-spacing: 0.5px;
      padding: 5px 13px;
      border-radius: 30px;
    }
    .faculty-bio { margin: 0 0 14px; font-size: 13.5px; color: var(--mut); max-width: 800px; line-height: 1.7; }
    .faculty-meta { display: flex; flex-wrap: wrap; gap: 8px; }
    .faculty-meta span {
      font-size: 12px;
      font-weight: 700;
      color: var(--green-700);
      background: var(--soft);
      border: 1px solid var(--line);
      padding: 5px 12px;
      border-radius: 20px;
    }

    /* ---------- Clinical pathway accordion ---------- */
    .pathway {
      width: 100%;
      max-width: 100%;
      margin: 0 auto;
      padding: 20px 4vw 16px;
    }
    .pathway-head { display: flex; align-items: center; gap: 12px; margin-bottom: 6px; }
    .pathway-head h2 { margin: 0; font-size: 24px; font-weight: 800; color: var(--navy-800); }
    .pathway-sub { color: var(--mut); font-size: 14.5px; margin: 0 0 20px; max-width: 820px; }
    .acc { border: 1px solid var(--line); border-radius: 16px; background: #fff; box-shadow: 0 6px 18px rgba(10, 45, 60, 0.06); }
    .acc-item { border-bottom: 1px solid var(--line); }
    .acc-item:last-child { border-bottom: 0; }
    .acc-btn {
      width: 100%;
      display: flex;
      align-items: center;
      gap: 14px;
      padding: 18px 22px;
      background: none;
      border: none;
      cursor: pointer;
      font-family: inherit;
      text-align: left;
      transition: background 0.2s;
    }
    .acc-btn:hover { background: #fafdfb; }
    .acc-item.open .acc-btn { background: linear-gradient(90deg, #f0faf6, #ffffff); }
    .acc-num {
      background: linear-gradient(135deg, var(--green-600), var(--teal));
      color: #fff;
      font-size: 12px;
      font-weight: 800;
      padding: 5px 12px;
      border-radius: 8px;
      flex-shrink: 0;
    }
    .acc-btn-tx { flex: 1; min-width: 0; }
    .acc-btn-tx b { display: block; font-size: 16px; color: var(--navy-800); font-weight: 800; }
    .acc-btn-tx span { display: block; font-size: 13px; color: var(--mut); margin-top: 2px; }
    .acc-chev { color: var(--teal); font-size: 13px; transition: transform 0.3s; flex-shrink: 0; }
    .acc-item.open .acc-chev { transform: rotate(180deg); }
    .acc-panel { max-height: 0; overflow: hidden; transition: max-height 0.45s ease; }
    .acc-item.open .acc-panel { max-height: 4000px; }
    .acc-inner { padding: 4px 22px 26px; }
    .acc-intro { font-size: 14px; color: var(--mut); max-width: 780px; margin: 0 0 18px; }
    .acc-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 14px; }
    .topic-card { background: #fafdfb; border: 1px solid var(--line); border-radius: 12px; padding: 14px 16px; }
    .topic-card h5 { margin: 0 0 8px; font-size: 13px; font-weight: 800; color: var(--green-700); text-transform: uppercase; letter-spacing: 0.4px; display: flex; align-items: center; gap: 7px; }
    .topic-card ul { margin: 0; padding-inline-start: 18px; }
    .topic-card li { font-size: 13px; color: var(--ink); margin-bottom: 6px; }
    .video-slot {
      display: flex;
      align-items: center;
      gap: 14px;
      border: 1.5px dashed #a7c4bb;
      border-radius: 14px;
      background: linear-gradient(160deg, #eef7f2, #e0f0e8);
      padding: 16px 18px;
      margin-bottom: 20px;
    }
    .video-slot .play {
      width: 42px; height: 42px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      background: linear-gradient(135deg, var(--green-600), var(--teal));
      color: #fff;
      font-size: 15px;
      flex-shrink: 0;
      padding-inline-start: 3px;
    }
    .video-slot b { display: block; font-size: 13.5px; color: var(--navy-800); }
    .video-slot span { font-size: 12px; color: var(--mut); }
    .video-frame-sm {
      position: relative;
      aspect-ratio: 16 / 9;
      width: 100%;
      max-width: 800px;
      margin: 0 0 20px;
      border-radius: 12px;
      overflow: hidden;
      background: #0a1f33;
      border: 1px solid var(--line);
    }
    .video-frame-sm iframe { position: absolute; inset: 0; width: 100%; height: 100%; border: 0; }
    .timeline { position: relative; margin: 4px 0 22px; padding-inline-start: 26px; }
    .timeline::before {
      content: "";
      position: absolute;
      left: 8px; top: 8px; bottom: 8px;
      width: 2px;
      background: linear-gradient(180deg, var(--green-600), var(--teal));
    }
    .tl-step { position: relative; margin-bottom: 16px; }
    .tl-step::before {
      content: "";
      position: absolute;
      left: -23px; top: 5px;
      width: 12px; height: 12px;
      border-radius: 50%;
      background: #fff;
      border: 3px solid var(--green-600);
    }
    .tl-step .tl-tag {
      display: inline-block;
      font-size: 10.5px;
      font-weight: 800;
      color: var(--green-700);
      background: var(--soft);
      border: 1px solid var(--line);
      padding: 2px 9px;
      border-radius: 20px;
      letter-spacing: 0.4px;
      margin-bottom: 6px;
    }
    .tl-step b { display: block; font-size: 14.5px; color: var(--navy-800); }
    .tl-step p { margin: 3px 0 0; font-size: 13.5px; color: var(--mut); line-height: 1.65; }

    /* AI drawer & FAB */
    .drawer {
      position: fixed;
      top: 0; bottom: 0; right: 0;
      width: min(420px, 100%);
      z-index: 950;
      background: #fff;
      box-shadow: -10px 0 36px rgba(10,31,51,0.22);
      display: flex;
      flex-direction: column;
      transform: translateX(105%);
      transition: transform 0.32s ease;
    }
    .drawer.open { transform: none; }
    .drawer-head {
      background: linear-gradient(135deg, var(--navy-800), var(--green-800));
      color: #fff;
      padding: 16px 18px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      direction: rtl;
    }
    .drawer-head b { font-size: 15px; display: block; }
    .drawer-head span { font-size: 12px; color: #b9cddb; }
    .drawer-head button {
      background: rgba(255,255,255,0.12);
      color: #fff;
      border: none;
      width: 32px; height: 32px;
      border-radius: 8px;
      cursor: pointer;
    }
    .drawer-chat { flex: 1; overflow-y: auto; padding: 16px; display: flex; flex-direction: column; direction: rtl; min-height: 0; }
    .msg { max-width: 82%; padding: 10px 14px; border-radius: 14px; margin-bottom: 10px; line-height: 1.7; font-size: 14px; white-space: normal; }
    .msg-user { background: linear-gradient(135deg, var(--green-600), var(--teal)); color: #fff; align-self: flex-start; border-bottom-right-radius: 4px; }
    .msg-ai { background: #eef4f2; color: var(--ink); align-self: flex-end; border-bottom-left-radius: 4px; }
    .typing-dots span { display: inline-block; width: 8px; height: 8px; margin-left: 4px; border-radius: 50%; background: #6b7c88; animation: blink 1.4s infinite both; }
    .typing-dots span:nth-child(2) { animation-delay: 0.2s; }
    .typing-dots span:nth-child(3) { animation-delay: 0.4s; }
    @keyframes blink { 0%, 80%, 100% { opacity: 0.2; } 40% { opacity: 1; } }
    .drawer-input { display: flex; gap: 8px; padding: 12px; border-top: 1px solid var(--line); direction: rtl; }
    .drawer-input input { flex: 1; padding: 11px 14px; border: 1px solid var(--line); border-radius: 10px; font-size: 13.5px; font-family: inherit; }
    .drawer-input input:focus { outline: none; border-color: var(--teal); }
    .drawer-input button { background: linear-gradient(135deg, var(--green-600), var(--teal)); color: #fff; border: none; border-radius: 10px; width: 46px; font-size: 15px; cursor: pointer; }
    .drawer-input button:disabled { opacity: 0.5; }

    .fab {
      position: fixed;
      bottom: 22px; left: 22px;
      z-index: 900;
      width: 54px; height: 54px;
      border-radius: 50%;
      border: none;
      background: linear-gradient(135deg, var(--green-600), var(--teal));
      color: #fff;
      font-size: 24px;
      cursor: pointer;
      box-shadow: 0 10px 26px rgba(14, 122, 95, 0.45);
      transition: transform 0.2s;
      display: grid; place-items: center;
    }
    .fab:hover { transform: scale(1.08); }

    .footer {
      margin-top: 44px;
      background: linear-gradient(160deg, var(--navy-900), var(--navy-800) 55%, var(--green-800));
      border-top: 4px solid var(--mint);
    }
    .footer-inner {
      width: 100%;
      max-width: 100%;
      margin: 0 auto;
      padding: 36px 4vw 32px;
      text-align: center;
    }
    .footer-brand {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      margin-bottom: 14px;
    }
    .footer-brand .brand-mark { font-size: 20px; }
    .footer-brand-name { font-weight: 800; font-size: 17px; letter-spacing: 0.3px; color: #fff; }
    .footer-brand-name span { color: var(--mint); }
    .footer-brand-name span.footer-pro { background: linear-gradient(90deg, var(--mint), var(--teal)); color: var(--navy-900); font-size: 10px; font-weight: 800; padding: 2px 7px; border-radius: 20px; letter-spacing: 1px; }
    .footer-disclaimer { max-width: 680px; margin: 0 auto 20px; font-size: 12.5px; color: #a9bccb; line-height: 1.7; }
    .footer-contact { display: flex; align-items: center; justify-content: center; flex-wrap: wrap; gap: 12px; margin-bottom: 22px; }
    .contact-link { display: inline-flex; align-items: center; gap: 8px; color: #d7e6f2; text-decoration: none; font-size: 13.5px; font-weight: 600; padding: 8px 16px; border-radius: 30px; border: 1px solid rgba(255,255,255,0.14); background: rgba(255,255,255,0.05); transition: background 0.25s, border-color 0.25s, color 0.25s, transform 0.25s; }
    .contact-link svg { color: var(--mint); transition: color 0.25s, transform 0.25s; }
    .contact-link:hover { background: rgba(52, 211, 153, 0.12); border-color: rgba(52, 211, 153, 0.5); color: #fff; transform: translateY(-1px); }
    .contact-link:hover svg { color: var(--gold); transform: scale(1.12); }
    .contact-dot { width: 4px; height: 4px; border-radius: 50%; background: rgba(255,255,255,0.25); flex-shrink: 0; }
    .footer-copy { margin: 0; font-size: 12px; color: #8fa6b8; }
    .footer-copy b { color: var(--gold); font-weight: 700; }

    /* ============================================================
       RESPONSIVE SYSTEM
       ============================================================ */
    img, iframe, video { max-width: 100%; }
    .topnav { scrollbar-width: none; -ms-overflow-style: none; }
    .topnav::-webkit-scrollbar { display: none; }

    @media (max-width: 1024px) {
      .topbar { gap: 14px; padding: 12px 18px; }
      .brand-name { font-size: 17px; }
      .topnav { overflow-x: auto; flex-wrap: nowrap; -webkit-overflow-scrolling: touch; }
      .topnav a { flex-shrink: 0; font-size: 13px; padding: 7px 10px; }
      .ai-btn { font-size: 13px; padding: 9px 13px; white-space: nowrap; }

      .hero { padding: 54px 20px 46px; }
      .hero p { font-size: 15px; }
      
      .main { padding: 38px 20px 16px; }
      .pathway { padding: 10px 20px 8px; }
      .faculty { padding: 26px 20px 6px; }
      .faculty-inner { padding: 26px; gap: 24px; }
      .footer-inner { padding: 32px 20px 28px; }

      .modal { width: min(860px, 100%); }
    }

    @media (max-width: 768px) {
      .topbar { gap: 10px; padding: 10px 14px; }
      .topnav { display: none; }
      .brand-name { font-size: 16px; }
      .prof-id { display: none; }
      .prof-mini { padding: 4px; }
      .ai-btn { font-size: 12.5px; padding: 9px 12px; }

      .hero { padding: 44px 16px 36px; }
      .hero h1 { font-size: clamp(26px, 8vw, 34px); }
      .hero p { font-size: 14.5px; margin-bottom: 24px; }
      .stat { min-width: 0; flex: 1 1 140px; padding: 12px 16px; }

      .main { padding: 30px 16px 14px; }
      .category { margin-bottom: 40px; }
      .category h2 { font-size: 21px; }
      .cat-sub { margin-inline-start: 0; font-size: 14px; }
      .pathway { padding: 8px 16px; }
      .pathway-head h2 { font-size: 21px; }
      .pathway-sub { font-size: 14px; }

      /* لإبقاء شكل العمود الواحد في الجوال */
      .grid { grid-template-columns: 1fr; gap: 16px; }
      .acc-grid { grid-template-columns: 1fr; gap: 12px; }

      .faculty { padding: 22px 16px 6px; }
      .faculty-inner { flex-direction: column; text-align: center; padding: 26px 20px; gap: 18px; }
      .faculty-inner::before { inset: 0 0 auto 0; width: auto; height: 6px; }
      .faculty-body h2 { font-size: 23px; }
      .faculty-bio { margin-inline: auto; }
      .faculty-badges, .faculty-meta { justify-content: center; }
      .faculty-seal { width: 76px; height: 76px; font-size: 22px; }

      .acc-btn { padding: 16px; gap: 10px; }
      .acc-btn-tx b { font-size: 15px; }
      .acc-btn-tx span { font-size: 12.5px; }
      .acc-inner { padding: 2px 16px 22px; }
      .acc-intro { font-size: 13.5px; }
      .timeline { padding-inline-start: 22px; }

      .two-col, .comp-grid { grid-template-columns: 1fr; }
      .spec .row { grid-template-columns: 120px 1fr; }
      .reminder, .clinic-note { font-size: 13px; }

      .modal-backdrop { padding: 12px; }
      .modal { max-height: 92vh; border-radius: 16px; }
      .modal-head { padding: 18px; border-radius: 16px 16px 0 0; }
      .modal-head h3 { font-size: 20px; }
      .modal-body { padding: 20px 18px 26px; }
    }

    @media (max-width: 480px) {
      .topbar { gap: 8px; padding: 9px 10px; }
      .brand-mark { font-size: 18px; }
      .brand-name { font-size: 14.5px; letter-spacing: 0.1px; }
      .brand-pro { font-size: 9px; padding: 2px 6px; }
      .prof-mini { display: none; }
      .ai-btn { font-size: 11.5px; padding: 8px 9px; }

      .hero { padding: 36px 12px 30px; }
      .hero-badge { font-size: 11.5px; padding: 5px 11px; }
      .hero h1 { font-size: clamp(23px, 9vw, 30px); }
      .hero-stats { display: grid; grid-template-columns: repeat(2, 1fr); gap: 10px; }
      .stat { flex: none; }
      .stat:last-child { grid-column: 1 / -1; }
      .hero-faculty { padding: 7px 14px 7px 8px; gap: 10px; }

      .main { padding: 26px 12px 12px; }
      .pathway { padding: 6px 12px; }
      .faculty { padding: 20px 12px 6px; }

      .card { padding: 18px 16px 16px; }
      .m-sec-title { font-size: 15px; }
      .spec .row { grid-template-columns: 1fr; }
      .spec .k { padding: 9px 14px; }
      .spec .v { padding: 10px 14px; }
      .panel { padding: 14px; }

      .stage-controls { gap: 10px; }
      .stage-cap { min-height: 92px; }

      .modal-backdrop { padding: 0; }
      .modal { max-height: 100vh; height: 100%; border-radius: 0; }
      .modal-head { border-radius: 0; padding: 16px 14px 14px; }
      .modal-head h3 { font-size: 18px; }
      .modal-body { padding: 18px 14px 24px; }

      .footer-contact { flex-direction: column; gap: 10px; }
      .contact-dot { display: none; }
      .contact-link { max-width: 100%; word-break: break-word; font-size: 12.5px; padding: 8px 14px; }
      .footer-copy { font-size: 11.5px; }
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
    <p>Interactive modules covering thread selection, step-by-step technique, complication management, high-quality video demonstrations, and an interactive step walkthrough of every movement — from everyday skin closure to specialized flexor tendon repair.</p>
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
      <div class="faculty-seal" aria-hidden="true">MH</div>
      <div class="faculty-body">
        <span class="faculty-kicker">Faculty · Medical Direction</span>
        <h2>Dr. Mohanad Hamad</h2>
        <div class="faculty-badges">
          <span class="faculty-badge">🎓 Lead Medical Educator</span>
          <span class="faculty-badge">⚕ Chief Medical Educator</span>
        </div>
        <p class="faculty-bio">Course director and chief medical educator behind every module on this platform — thread selection, needle choice, technique, and complication management, authored and reviewed against current surgical standards.</p>
        <div class="faculty-meta">
          <span>✓ Curriculum authored &amp; reviewed</span>
          <span>✓ Surgically evidence-based</span>
          <span>✓ Institutional-grade accuracy</span>
        </div>
      </div>
    </div>
  </section>

  <section class="pathway" id="pathway">
    <div class="pathway-head">
      <span class="cat-no">🧭</span>
      <h2>The Complete Clinical Pathway</h2>
    </div>
    <p class="pathway-sub">A surgeon-structured systematic guide — pre-suturing preparation, local anesthesia, the full ER-to-discharge workflow, and complication management. Tap a stage to expand it.</p>
    <div class="acc" id="pathwayCtn"></div>
  </section>

  <main class="main">
    <section class="category" id="cat-basic">
      <h2><span class="cat-no">01</span> Basic Wound Closure</h2>
      <p class="cat-sub">The everyday staples of skin and soft-tissue closure.</p>
      <div class="grid" id="grid-basic"></div>
    </section>

    <section class="category" id="cat-advanced">
      <h2><span class="cat-no">02</span> Hemostasis &amp; Advanced Closure</h2>
      <p class="cat-sub">Specialized patterns for bleeding control and circular openings.</p>
      <div class="grid" id="grid-advanced"></div>
    </section>

    <section class="category" id="cat-ortho">
      <h2><span class="cat-no">03</span> Orthopedic Tendon Repair</h2>
      <p class="cat-sub">Core-suture strategies for flexor and extensor tendon injuries.</p>
      <div class="grid" id="grid-ortho"></div>
    </section>
  </main>

  <footer class="footer">
    <div class="footer-inner">
      <div class="footer-brand">
        <span class="brand-mark">🧵</span>
        <span class="footer-brand-name">Suture<span>Master</span><span class="footer-pro">PRO</span></span>
      </div>
      <p class="footer-disclaimer">Educational tool for training purposes only — not a substitute for supervised surgical training, local protocols, or institutional guidelines.</p>
      <div class="footer-contact">
        <a class="contact-link" href="https://www.instagram.com/dr.mhn.d?igsh=bnh6bGIwOGNxbTl0" target="_blank" rel="noopener noreferrer" aria-label="Instagram: @dr.mhn.d">
          <svg viewBox="0 0 24 24" width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"></rect><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line></svg>
          <span>@dr.mhn.d</span>
        </a>
        <span class="contact-dot" aria-hidden="true"></span>
        <a class="contact-link" href="mailto:drmohanad8hamad@gmail.com" aria-label="Email: drmohanad8hamad@gmail.com">
          <svg viewBox="0 0 24 24" width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>
          <span>drmohanad8hamad@gmail.com</span>
        </a>
      </div>
      <p class="footer-copy">© <span id="footYear"></span> SutureMaster PRO · Directed by <b>Dr. Mohanad Hamad</b> · Chief Medical Educator</p>
    </div>
  </footer>

  <!-- Module modal -->
  <div class="modal-backdrop" id="modalBackdrop" hidden>
    <div class="modal" id="sutureModal" role="dialog" aria-modal="true" aria-labelledby="mName">
      <div class="modal-head">
        <div>
          <span class="modal-cat" id="mCat"></span>
          <h3 id="mName"></h3>
          <p id="mTagline"></p>
        </div>
        <button class="modal-close" id="modalClose" aria-label="Close">✕</button>
      </div>
      <div class="modal-body" id="modalBody"></div>
    </div>
  </div>

  <!-- AI tutor drawer -->
  <div class="drawer" id="drawer" hidden>
    <div class="drawer-head">
      <div>
        <b>🧑‍⚕️ Prof. Surgeon</b>
        <span>مدربك الجراحي التفاعلي — تحدث بالعربية</span>
      </div>
      <button id="drawerClose" aria-label="Close chat">✕</button>
    </div>
    <div class="drawer-chat" id="chatEl"></div>
    <div class="drawer-input">
      <input id="chatInput" placeholder="اسأل البروفيسور عن أي تقنية..." autocomplete="off">
      <button id="sendBtn">➤</button>
    </div>
  </div>
  <button class="fab" id="chatFab" aria-label="Open AI tutor">🧑‍⚕️</button>

  <script>
    (function () {
      "use strict";

      // ============================================================
      // DATA MODULE — medically reviewed suture content
      // ============================================================
      const SUTURES = [
        {
          id: "simple", category: "basic", icon: "🪡",
          name: "Simple Interrupted",
          tagline: "The workhorse of wound closure — independent, secure, and easy to revise.",
          videoId: "z8oWv-nVO6g",
          videoSource: "Geeky Medics",
          tags: ["Skin", "Low tension", "Versatile"],
          thread: {
            material: "Non-absorbable monofilament (Nylon, Prolene) for skin; absorbable (Vicryl, Monocryl) for deep dermal or mucosal layers.",
            absorbable: "No for skin · Yes for deep dermal options",
            sizes: "Face 5-0 / 6-0 · Neck 4-0 / 5-0 · Trunk 4-0 · Extremities 3-0 / 4-0 · Scalp 3-0",
            needle: "Reverse-cutting (cutting edge away from the wound), 3/8 circle (e.g., PS-2, P-3)",
            brands: "Ethilon 4-0 · Prolene 4-0 · Monocryl 4-0 (deep)"
          },
          indications: [
            "Linear lacerations and clean surgical incisions",
            "Low-to-moderate tension skin closure",
            "Contaminated wounds — individual stitches can be removed selectively",
            "Reinforcement or revision of a failing continuous line"
          ],
          technique: [
            "Hold the needle in the needle holder two-thirds of the way back from the tip.",
            "Enter perpendicular (90°) to the skin surface, 2–3 mm from the wound edge, following the needle's curve through the full dermis.",
            "Mirror the bite on the opposite side at equal depth and distance.",
            "Evert the edges with gentle opposing traction as the knot is tied.",
            "Tie a surgeon's knot followed by 3–4 square throws (monofilament); leave 3–5 mm tails."
          ],
          complications: [
            ["Cross-hatching / stitch marks", "Remove on schedule; use fine monofilament; avoid tight throws; reinforce facial wounds with skin tape."],
            ["Suture abscess / wound infection", "Inspect daily; remove affected stitches; sterile dressings; culture and broad-spectrum antibiotics if cellulitis develops."],
            ["Wound dehiscence", "Re-assess tension; add deep dermal or mattress reinforcement; respect removal timing (trunk 7–10 days)."],
            ["Tissue strangulation", "Appose, never strangulate — loosen over-tightened throws; use square knots at minimal tension."]
          ],
          removal: "Removal schedule: Face 5 days · Scalp/Neck 7 days · Trunk 7–10 days · Extremities 10–14 days.",
          steps: [
            { t: "Load the needle", c: "Grasp the needle in the needle holder two-thirds of the way back from the tip, with the jaws perpendicular to the needle's curve." },
            { t: "Enter at 90°", c: "Insert the tip perpendicular to the skin surface 2–3 mm from the wound edge, rotating the wrist to follow the needle's arc through the full dermis." },
            { t: "Mirror the bite", c: "On the opposite edge take a bite of equal depth and distance, driving the needle out so the exit point sits at the same level as entry." },
            { t: "Evert & appose", c: "Draw both ends together with opposing traction so the edges evert slightly without blanching — apposition, never strangulation." },
            { t: "Instrument tie", c: "Tie a surgeon's knot, then 3–4 square throws for monofilament, keeping each throw flat and taut; cut tails 3–5 mm." }
          ]
        },
        {
          id: "running", category: "basic", icon: "🧵",
          name: "Running Continuous",
          tagline: "Fast, even-tension closure for long linear wounds and fascial closure.",
          videoId: "afUcrlHA358",
          videoSource: "MedSync — Surgical Skills",
          tags: ["Skin", "Fascia", "Speed"],
          thread: {
            material: "Monofilament non-absorbable (Prolene) for skin; absorbable (PDS, Maxon) for fascia.",
            absorbable: "Optional — PDS for fascia, Prolene for skin",
            sizes: "Skin 3-0 / 4-0 · Fascia 0 / 1 · Abdomen 1-0 loop (mass closure)",
            needle: "Skin: reverse-cutting 3/8 circle · Fascia: tapered, 1/2 circle (e.g., CT-1)",
            brands: "Prolene 4-0 · PDS II 3-0 · Maxon 0"
          },
          indications: [
            "Long linear incisions (e.g., midline laparotomy fascial closure)",
            "Low-to-moderate tension wounds where speed matters",
            "Flat cosmetic closures with even edge apposition",
            "Fascial closure where a running absorbable line is preferred"
          ],
          technique: [
            "Place an anchoring knot away from the wound edge.",
            "Run the suture in a continuous spiral with bites ~1 cm apart (small-bite 5 mm for fascia) and equal depth.",
            "Keep constant tension on each pass — no slack between bites.",
            "Optionally lock each pass for a continuous-locking pattern.",
            "Finish by tying the loop to the standing end, then bury the knot."
          ],
          note: "Evidence — laparotomy fascial closure: the STITCH trial (Lancet 2015) favors a small-bite technique (5 mm bites, 5 mm from the edge, suture length ≥ 4× wound length) over large bites for lower incisional hernia rates.",
          complications: [
            ["Total line failure on breakage", "One break compromises the whole line — reinforce every 3–4th bite in high-risk wounds; inspect for fraying."],
            ["Wound dehiscence", "A loosened running line fails completely — convert to interrupted closure when dehiscence risk is high."],
            ["Tissue ischemia / puckering", "Over-tension blanches the edge — if edges blanch, redo with looser tension."],
            ["Infection tracking", "Contaminated wounds: prefer interrupted stitches so individual sutures can be removed."]
          ],
          removal: "Remove at 7–14 days depending on site, as for interrupted sutures.",
          steps: [
            { t: "Anchor knot", c: "Place the first (anchoring) knot 3–5 mm beyond the wound apex so the running line begins cleanly outside the wound." },
            { t: "First pass", c: "Insert the needle perpendicular to the skin and take bites ~1 cm apart (5 mm for fascia), at equal depth on both sides." },
            { t: "Maintain tension", c: "Pull each pass snug against the previous bite, keeping uniform tension so no slack accumulates between bites." },
            { t: "Optional locking", c: "For a continuous-locking pattern, pass the needle through the loop of the previous bite before taking the next." },
            { t: "Finish & tie", c: "Leave a loop at the end, pass the needle through it and tie to the standing end; bury the knot away from the wound." }
          ]
        },
        {
          id: "vertical", category: "basic", icon: "🪡",
          name: "Vertical Mattress",
          tagline: "Deep + superficial bites produce strong eversion for thick skin.",
          videoId: "aKwrhjVd-fg",
          videoSource: "BMJ Learning",
          tags: ["Thick skin", "Eversion", "High tension"],
          thread: {
            material: "Non-absorbable monofilament (Nylon, Prolene).",
            absorbable: "No",
            sizes: "Scalp / Knee / Back 2-0 / 3-0 · Trunk 3-0 · Extremities 3-0 / 4-0",
            needle: "Reverse-cutting, 3/8 circle (e.g., FS-2, PS-4)",
            brands: "Ethilon 2-0 · Prolene 3-0"
          },
          indications: [
            "Skin under high tension (knee, back, palm, scalp)",
            "Thick or dermis-heavy skin that resists eversion",
            "Wounds needing simultaneous deep and superficial support",
            "Areas where edge eversion is critical to prevent inversion scarring"
          ],
          technique: [
            "Far bite: enter ~1 cm from the edge down to full wound depth.",
            "Exit the far bite on the opposite side at the same depth.",
            "Near bite: re-enter 2–3 mm from the edge, through dermis only.",
            "Exit the near bite on the opposite near side and tie — the knot sits on the near side.",
            "Sequence is 'far-far, near-near'; keep both loops at matching tension."
          ],
          complications: [
            ["Cross-hatching / stitch marks", "Keep far bites modest; remove at 10–14 days; avoid on face or thin skin."],
            ["Wound edge necrosis", "Excess tension strangulates the tissue island between the loops — loosen and add bolsters."],
            ["Edema of edge tissue", "The vertical loop can tourniquet the skin island — monitor for blanching and loosen early."],
            ["Infection", "Meticulous asepsis; remove individual loops early if infected."]
          ],
          removal: "Remove at 10–14 days; consider stage removal in high-tension areas.",
          steps: [
            { t: "Far-far deep bite", c: "Enter 8–10 mm from the edge; drive the needle to full wound depth and exit at the same depth on the opposite side." },
            { t: "Near-near bite", c: "Re-enter 2–3 mm from the edge on the near side, take a shallow dermal bite, and exit 2–3 mm from the edge on the same side." },
            { t: "Appose both loops", c: "Gently tension the deep (far) loop to close dead space and the superficial (near) loop to evert the skin edge." },
            { t: "Assess eversion", c: "Confirm the wound edges roll outward; the knot should sit on the near side, well away from the incision line." },
            { t: "Tie & trim", c: "Tie a surgeon's knot plus square throws, leaving tails long enough for removal at 10–14 days." }
          ]
        },
        {
          id: "horizontal", category: "basic", icon: "🪡",
          name: "Horizontal Mattress",
          tagline: "Distributes tension parallel to the wound — ideal for high-tension, low-vascularity areas.",
          videoId: "6qF4mxB7KzM",
          videoSource: "Geeky Medics",
          tags: ["High tension", "Fascia", "Poor vascularity"],
          thread: {
            material: "Non-absorbable monofilament (Prolene, Nylon); braided for fascia.",
            absorbable: "Optional (Vicryl for fascia and muscle)",
            sizes: "Fascia 0 / 1 · Skin 2-0 / 3-0 · Sacrum / pressure areas 2-0",
            needle: "Reverse-cutting for skin, tapered for fascia; 3/8 or 1/2 circle",
            brands: "Prolene 2-0 · Ethibond 0 (fascia)"
          },
          indications: [
            "High-tension wound closure",
            "Sacral and heel pressure areas with marginal blood supply",
            "Fascia and muscle approximation",
            "Reducing tension across a wound while distributing it along the edge"
          ],
          technique: [
            "Enter 5–10 mm from the wound edge.",
            "Cross the wound and exit on the opposite side.",
            "Re-enter on the same side immediately adjacent to the exit.",
            "Cross back and exit near the original entry point, then tie.",
            "Tension now runs parallel to the wound; use bolsters/buttons to spread load."
          ],
          complications: [
            ["Tissue strangulation", "The encircling loop compresses tissue — loosen aggressively, pad with bolsters, remove at 10–14 days."],
            ["Wound edge ischemia / necrosis", "Avoid in marginal-vascularity limbs; monitor capillary refill of the looped tissue."],
            ["Pressure necrosis under bolster", "Pad well and change dressings; convert to interrupted sutures if unmanageable."],
            ["Infection", "Remove affected loops; open and pack if an abscess forms."]
          ],
          removal: "Remove at 10–14 days; stage removal in high-tension closures.",
          steps: [
            { t: "Entry", c: "Insert the needle 5–10 mm from the wound edge, entering parallel to the line of the wound." },
            { t: "Cross & exit", c: "Drive the needle across the wound and exit on the opposite side at the same distance from the edge." },
            { t: "Re-enter & cross back", c: "Re-enter immediately adjacent to the exit point, cross back to the starting side, and exit next to the original entry." },
            { t: "Parallel tension", c: "Tie so the tension runs parallel to the wound, spreading the load along the entire edge rather than at one point." },
            { t: "Protect with bolsters", c: "Optionally pass the loop through bolster tubing or buttons to prevent pressure necrosis of the underlying skin." }
          ]
        },
        {
          id: "subcuticular", category: "basic", icon: "✨",
          name: "Subcuticular (Buried Running)",
          tagline: "Cosmetic gold standard — buried in the dermis with no surface marks.",
          videoId: "bhN60YMyXos",
          videoSource: "Center for Medical Education",
          tags: ["Cosmetic", "Dermal plane", "No stitch marks"],
          thread: {
            material: "Absorbable monofilament (Monocryl, PDS); occasionally removable non-absorbable (Prolene) for long incisions.",
            absorbable: "Yes (preferred)",
            sizes: "Face 4-0 / 5-0 · Trunk 3-0 / 4-0 · Breast 3-0 · Pediatric 4-0 / 5-0",
            needle: "Tapered or tapercut point, 3/8 circle (e.g., PS-2) to minimize dermal trauma",
            brands: "Monocryl 4-0 · PDS II 4-0 · Prolene 4-0 (removable)"
          },
          indications: [
            "Cosmetically sensitive areas (face, breast, neck)",
            "Long linear incisions where surface marks are unacceptable",
            "Pediatric closures",
            "Closures where deep dermal support plus epidermal apposition is needed"
          ],
          technique: [
            "Start with a buried anchor knot in the deepest dermis of one edge.",
            "Run the needle horizontally through the mid-dermis, alternating sides.",
            "Keep bites symmetric and tension constant so the two edges appose evenly.",
            "Exit ~1 cm beyond the end of the wound.",
            "Tie a buried knot, or rely on absorbable material for spontaneous absorption."
          ],
          complications: [
            ["Suture-track infection / sinus", "Absorbable material lowers the risk; if a sinus forms, remove the suture and pack."],
            ["Gaping / poor eversion", "Insufficient dermal bites — deepen the bites and add skin tape for support."],
            ["Knot prominence", "Bury knots in the deepest dermis; looped sutures halve the number of knots."],
            ["Allergic reaction to suture", "Switch material (e.g., PDS to Monocryl); remove early if the reaction is significant."]
          ],
          removal: "No removal needed with absorbable material; removable Prolene is taken out at 10–14 days.",
          steps: [
            { t: "Bury the anchor", c: "Start with a knot buried in the deep dermis at the wound apex so no knot is visible on the surface." },
            { t: "Run in the dermis", c: "Pass the needle horizontally through the mid-dermis, alternating sides of the wound with each bite." },
            { t: "Equal bites", c: "Keep every bite the same size and depth so both edges advance equally and tension stays even." },
            { t: "Exit & tie", c: "Exit the skin ~1 cm beyond the wound end, then tie and bury the final knot or trim the ends flush." },
            { t: "Support with tape", c: "Apply skin closure strips for extra edge support; with absorbable material no removal is needed." }
          ]
        },
        {
          id: "figure8", category: "advanced", icon: "🔁",
          name: "Figure-of-Eight",
          tagline: "Two crossing loops compress tissue and secure hemostasis.",
          videoId: "yaG_vJRD13s",
          videoSource: "MiniMedLessons",
          tags: ["Hemostasis", "Fascia", "Muscle"],
          thread: {
            material: "Non-absorbable braided (Ethibond) or absorbable (Vicryl) 0 / 1; stainless wire for sternal approximation.",
            absorbable: "Optional — absorbable preferred for muscle and fascia",
            sizes: "Fascia / Muscle 0 / 1 · Vessel ligation 2-0 / 3-0 · Sternum: steel wire",
            needle: "Tapered point for fascia/muscle (e.g., CT-1)",
            brands: "Ethibond 0 · Vicryl 1 · Steel wire"
          },
          indications: [
            "Hemostatic ligation of bleeding points and vessel stumps",
            "Fascial and muscle approximation under tension (abdominal wall)",
            "Sternal closure (figure-of-eight wires)",
            "Securing drains and cannulas"
          ],
          technique: [
            "Pass the needle deep to the bleeding point or across the fascial defect.",
            "Cross the midline and exit on the opposite side.",
            "Loop back over the top, crossing the first bite to form an '8'.",
            "Tension both loops simultaneously and tie — the crossing point compresses tissue between the loops."
          ],
          complications: [
            ["Tissue necrosis under loops", "Excess tension strangulates — apply only enough to appose and compress."],
            ["Nerve / vessel entrapment", "Keep bites superficial to named structures; dissect the tissue plane first."],
            ["Suture granuloma", "Use the smallest adequate caliber; remove non-absorbable material once healed."],
            ["Sternal instability (cardiac)", "Verify wire configuration and stability; manage parasternal motion."]
          ],
          removal: "Non-absorbable material is left in place unless it erodes or becomes infected.",
          steps: [
            { t: "Deep pass", c: "Enter at the base of the wound or fascial defect, taking a deep bite that includes the bleeding point in its grasp." },
            { t: "Cross the midline", c: "Exit on the opposite side, then loop the suture back over the top of the wound toward your starting side." },
            { t: "Form the 8", c: "Cross the midline a second time so the two bites form a figure-of-eight, intersecting at the center of the defect." },
            { t: "Compress", c: "Tension both loops simultaneously so the crossing point compresses the tissue between them — achieving hemostasis." },
            { t: "Tie & secure", c: "Tie firmly — apposition and compression, not strangulation — and cut the tails short." }
          ]
        },
        {
          id: "purse", category: "advanced", icon: "🎯",
          name: "Purse-String",
          tagline: "A circumferential gather that inverts tissue and closes circular openings.",
          videoId: "mvFfm0Msbwo",
          videoSource: "Andrew Wright",
          tags: ["Stoma", "Inversion", "Circular opening"],
          thread: {
            material: "Non-absorbable monofilament (Prolene) or absorbable (Vicryl) 2-0 / 3-0.",
            absorbable: "Optional",
            sizes: "Appendix stump 3-0 / 4-0 · Stoma 2-0 / 3-0 · Enterotomy 3-0",
            needle: "Tapered point, 3/8 circle (e.g., SH-1 taper)",
            brands: "Prolene 3-0 · Vicryl 3-0"
          },
          indications: [
            "Stoma creation (end colostomy or ileostomy)",
            "Enterotomy / cystotomy closure",
            "Securing catheters and drains; closing small circular wounds",
            "Appendiceal stump inversion (historic — often stapled or ligated today)"
          ],
          technique: [
            "Take continuous circumferential bites 3–5 mm from the opening edge.",
            "Complete the full circle back to the starting point.",
            "Gather both ends and tie — the tissue inverts and the opening closes.",
            "Tie gently: apposition without stenosis."
          ],
          note: "Modern practice: the appendiceal stump is usually closed with an endoloop or stapler; the purse-string remains essential for stomas and for securing tubes and drains.",
          complications: [
            ["Stenosis / stricture", "Over-tightening narrows the lumen — tie until apposed, not strangulated."],
            ["Leak (enterotomy)", "Take full-thickness bites; reinforce with interrupted seromuscular (Lembert) stitches."],
            ["Tissue tearing on gather", "Use an atraumatic tapered needle and gather gradually."],
            ["Inverted ischemic cuff", "Excess inversion devascularizes the rim — keep the inverted cuff small."]
          ],
          removal: "Usually left in place or removed once the tract matures, depending on indication.",
          steps: [
            { t: "Circumferential bites", c: "Take continuous bites 3–5 mm from the opening edge, at equal depth, traveling around the full circumference." },
            { t: "Complete the circle", c: "Return to the starting point with the needle — both ends now flank the first bite, forming a complete loop." },
            { t: "Gather", c: "Draw both ends taut like a drawstring to gather the tissue and invert the opening inward." },
            { t: "Assess inversion", c: "Confirm the edges invert cleanly and the lumen remains patent — no stenosis or tissue tearing." },
            { t: "Tie", c: "Tie both ends gently — apposed, not strangulated — and trim; reinforce with Lembert stitches if leakage is a concern." }
          ]
        },
        {
          id: "kessler", category: "ortho", icon: "🦴",
          name: "Modified Kessler (Tendon Repair)",
          tagline: "Core locking suture for flexor tendon repairs — strength where it counts.",
          videoId: "IUk26UtHRCg",
          videoSource: "MedSync — Surgical Skills",
          tags: ["Tendon", "Flexor", "Core suture"],
          thread: {
            material: "Non-absorbable braided core (Ethibond, FiberWire-style). Never absorbable for the tendon core.",
            absorbable: "No (core) · Epitendinous may be 6-0 Prolene / nylon",
            sizes: "Core 3-0 / 4-0 · Epitendinous 6-0",
            needle: "Round-bodied (tapered) point for tendon, 3/8 circle",
            brands: "Ethibond 3-0 · FiberWire 3-0 · Prolene 6-0"
          },
          indications: [
            "Flexor tendon lacerations (especially zone II, 'no man's land')",
            "Extensor tendon injuries",
            "Primary repair within 12–24 hours in a hand-surgery setting",
            "Repairs where early protected mobilization is planned"
          ],
          technique: [
            "Freshen both tendon ends with a sharp scalpel.",
            "Enter the core suture 1 cm proximal to the cut and run it longitudinally.",
            "Exit transversely to create a locking loop, then cross the repair site.",
            "Mirror the configuration on the distal stump and tie the core (4-strand preferred).",
            "Add a 6-0 epitendinous running suture to smooth the junction (adds ~25% strength)."
          ],
          note: "Repair strength scales with the number of core strands crossing the repair (2-strand < 4-strand < 6-strand). Four-strand repairs such as the modified Kessler permit earlier active mobilization, which reduces adhesion formation.",
          complications: [
            ["Adhesion formation", "Start early protected motion (short-arc protocol); atraumatic technique; structured hand therapy."],
            ["Tendon rupture / gap formation", "Use a multi-strand repair (4-strand beats 2-strand); protected mobilization; immediate re-repair if ruptured."],
            ["Pulley damage (zone II)", "Preserve A2/A4 pulleys; vent only when necessary; repair the sheath when feasible."],
            ["Stiffness / contracture", "Structured splinting and therapy; consider tenolysis only after 6–12 months of failed conservative treatment."]
          ],
          removal: "Permanent (non-absorbable). Protect the repair for 8–12 weeks.",
          steps: [
            { t: "Freshen the ends", c: "Trim both tendon ends with a fresh scalpel to remove frayed tissue, working on a firm, flat surface." },
            { t: "Core bite & locking loop", c: "Enter the core suture 1 cm from the cut end; run it longitudinally and exit transversely to create a locking loop." },
            { t: "Cross & mirror", c: "Cross to the distal stump and mirror the configuration, taking the same 1 cm bite with its own locking loop." },
            { t: "Tie the core", c: "Appose the stumps by tensioning both core limbs (4-strand preferred) and tie with square throws." },
            { t: "Epitendinous suture", c: "Add a 6-0 running peripheral suture around the repair junction to smooth the surface and add ~25% strength." }
          ]
        },
        {
          id: "bunnell", category: "ortho", icon: "🦴",
          name: "Bunnell Tendon Repair",
          tagline: "Criss-cross multi-strand core for robust tendon approximation.",
          videoId: "paXHJl_Hccc",
          videoSource: "Hand, Plastic, Reconstructive & Nerve Surgery",
          tags: ["Tendon", "Criss-cross", "Core suture"],
          thread: {
            material: "Non-absorbable braided core (Ethibond 3-0 / 4-0); epitendinous 6-0.",
            absorbable: "No",
            sizes: "Core 3-0 / 4-0 · Epitendinous 6-0",
            needle: "Round-bodied (tapered) point for tendon, 3/8 circle",
            brands: "Ethibond 3-0 · Prolene 6-0"
          },
          indications: [
            "Tendon lacerations needing a robust multi-strand core repair",
            "Historically the standard for flexor tendons — still taught for its crossing-lock mechanics",
            "Repairs where strong grasp of both stumps is essential"
          ],
          technique: [
            "Enter the proximal stump and weave the suture in a criss-cross (zig-zag) pattern along the tendon.",
            "Exit the proximal stump at the cut end.",
            "Cross to the distal stump and mirror the criss-cross weave.",
            "Tie the two ends with the repair tensioned to appose the stumps without bunching."
          ],
          note: "The criss-cross strands can compromise intratendinous blood supply; multi-strand locking repairs (modified Kessler, M-Tang) are generally preferred today. Bunnell remains valuable for its historical teaching and where a strong 2-strand grasp is acceptable.",
          complications: [
            ["Adhesion / impaired gliding", "Criss-crossing strands can cross intratendinous vessels — minimize passes; start early motion therapy."],
            ["Rupture", "Protect the repair for 8–12 weeks; educate the patient; avoid early resisted flexion."],
            ["Gap formation", "Take secure bites 1 cm from the cut end and lock each crossing loop."],
            ["Stiffness", "Splinting plus supervised therapy; address adhesions surgically only after prolonged conservative treatment."]
          ],
          removal: "Permanent (non-absorbable). Protect the repair for 8–12 weeks.",
          steps: [
            { t: "Entry & first limb", c: "Enter the proximal stump and run the first limb longitudinally toward the cut end." },
            { t: "Criss-cross weave", c: "Cross back diagonally to create a zig-zag weave that grasps multiple tendon fiber bundles." },
            { t: "Exit & mirror", c: "Exit at the cut end, cross to the distal stump, and mirror the criss-cross weave on that side." },
            { t: "Appose & tie", c: "Tension both limbs to appose the stumps without bunching, then tie with square throws." },
            { t: "Peripheral support", c: "Consider an epitendinous suture; protect the repair with splinting and controlled early mobilization." }
          ]
        }
      ];

      const CATS = {
        basic:    { no: "01", grid: "grid-basic" },
        advanced: { no: "02", grid: "grid-advanced" },
        ortho:    { no: "03", grid: "grid-ortho" }
      };

      // ============================================================
      // CLINICAL PATHWAY ACCORDION
      // ============================================================
      const PATHWAY = [
        {
          no: "01",
          title: "Pre-Suturing Preparation",
          sub: "Equipment, sterility, wound cleaning and patient assessment — everything before the first stitch.",
          intro: "Preparation prevents most complications. Assemble the tray, secure the sterile field, and prepare both the wound and the patient before a needle ever touches skin.",
          video: { label: "Intro to suturing — equipment & preparation", id: "NnKdmjX5pWU", src: "Buck Parker, M.D." },
          topics: [
            { icon: "🧰", t: "Equipment setup", items: [
              "Suture tray: needle holder, Adson toothed forceps, stitch scissors, scalpel (#11 / #15), skin hooks, gauze",
              "Suture and needle pre-selected by site (see each technique module's thread table)",
              "Irrigation: 50–100 mL syringe with 18–19G splash-shield needle, sterile saline",
              "Sterile gloves, gown, mask and eye protection",
              "Local anesthetic, 8.4% bicarbonate, 27–30G needles"
            ]},
            { icon: "🧤", t: "Sterile field", items: [
              "Full aseptic technique — never sacrifice sterility for speed",
              "Skin prep: 2% chlorhexidine or iodophor, from wound outward in concentric circles",
              "Remove gross contamination before prepping so debris is not pushed into the tissue",
              "Drape with fenestrated drapes to create a clean working field"
            ]},
            { icon: "💧", t: "Wound cleaning & irrigation", items: [
              "Irrigate with sterile saline under pressure (≈8 psi, via splash shield) until visibly clean",
              "Debride devitalized tissue and remove foreign bodies under good light",
              "Achieve hemostasis — pressure, ligature or cautery — before closure",
              "Culture only for gross infection or delayed presentation"
            ]},
            { icon: "🩺", t: "Patient assessment", items: [
              "History: mechanism, time since injury (over 6–8 h raises infection risk), contamination, allergies, tetanus status, anticoagulants, diabetes / immunosuppression",
              "Exam: distal neurovascular status, tendon and nerve function, bony tenderness, wound depth and involvement",
              "Tetanus: booster if last dose over 5–10 years; tetanus immunoglobulin for tetanus-prone wounds in the unvaccinated",
              "Antibiotics are not routine — reserve for bites, gross contamination and immunocompromised patients"
            ]}
          ]
        },
        {
          no: "02",
          title: "Local Anesthesia",
          sub: "Agents, indications, dosing and precise injection technique.",
          intro: "Effective and safe anesthesia gives you a comfortable patient and a controlled surgical field.",
          video: { label: "Infiltrating a wound with local anesthetic before suturing", id: "ssLuaeo1VTk", src: "Apprentice Doctor MedSkills" },
          topics: [
            { icon: "💉", t: "Types of anesthetics", items: [
              "Lidocaine 1% — onset 1–3 min, lasts 1–2 h (2–4 h with epinephrine)",
              "Bupivacaine 0.25–0.5% — slower onset, lasts 4–8 h, ideal for longer repairs",
              "Mepivacaine 1–2% — intermediate duration, low cardiac risk profile",
              "Buffering (10:1 lidocaine with 8.4% bicarbonate) markedly reduces the sting"
            ]},
            { icon: "⚖️", t: "Dosing & safety", items: [
              "Lidocaine plain: max 4 mg/kg (≈300 mg); with epinephrine: 7 mg/kg (≈500 mg)",
              "Bupivacaine: max 2–3 mg/kg",
              "Epinephrine: traditional caution in digits, pinna and penis — current evidence supports safe use in healthy patients; follow local protocol",
              "Toxicity (perioral tingling, metallic taste, tinnitus, confusion, seizures, arrhythmia): stop, oxygen, airway support, treat seizures"
            ]},
            { icon: "🎯", t: "Indications", items: [
              "Direct infiltration through the wound edges — most simple lacerations",
              "Field block — circumferential anesthesia around the area",
              "Digital block — two dorsal injections at the base of the digit; never a circumferential ring",
              "Regional blocks for complex hand and facial repairs"
            ]},
            { icon: "✍️", t: "Injection technique", items: [
              "Aspirate before every injection to avoid intravascular delivery",
              "Inject slowly into the subcutaneous plane; through open wound edges when possible — less painful",
              "Use the smallest gauge that flows (27–30G) and warm the solution",
              "Wait for full onset and test the field before starting"
            ]}
          ]
        },
        {
          no: "03",
          title: "Complete Step-by-Step Clinical Pathway",
          sub: "From the doors of the ER to discharge — one chronological workflow.",
          intro: "The entire journey of a laceration patient as a single, correct sequence. Each step flows into the next.",
          video: { label: "Hand laceration repair — full procedure", id: "3Zy1W31r6ME", src: "Dr. Carlo Oller" },
          steps: [
            { t: "Arrival & triage", c: "Assess life threats first (ABCDE). Control active bleeding with direct pressure. Note mechanism and time. Check tetanus status and allergies." },
            { t: "History taking", c: "Mechanism (sharp, crush or bite), time since injury, contamination (soil, glass, organic matter), handedness and occupation, anticoagulants, steroids, diabetes, prior wound infections." },
            { t: "Examination", c: "Distal neurovascular status — capillary refill, sensation, pulses. Test tendons and nerves. Palpate for bony tenderness; X-ray for suspected fracture or retained foreign body." },
            { t: "Wound exploration", c: "Assess depth under good light — does it reach fascia, joint, or tendon sheath? Look for tendon and nerve injury before closing." },
            { t: "Analgesia & anesthesia", c: "Analgesia for pain control, then local anesthesia with accurate dosing (Section 02). Wait for full effect before proceeding." },
            { t: "Wound preparation", c: "Irrigate under pressure until clean, debride devitalized edges, control bleeding, and dry the field." },
            { t: "Closure plan", c: "Select technique by site, tension and cosmesis — simple interrupted, running, mattress or subcuticular. Choose material and size from the site table." },
            { t: "Suture & tie", c: "Everting bites of equal depth and distance; surgeon's knot plus 3–4 square throws. Reassess symmetry as you work." },
            { t: "Dressing", c: "Non-adherent layer on the wound, absorbent dressing, secure with tape; splint across joints at risk." },
            { t: "Discharge & aftercare", c: "Removal schedule by site (face 5 d, scalp/neck 7 d, trunk 7–10 d, extremities 10–14 d). Return signs: spreading redness, swelling, discharge, fever. Tetanus booster if due." }
          ]
        },
        {
          no: "04",
          title: "Complications & Management",
          sub: "Identify post-suturing complications early and act decisively.",
          intro: "Know what to look for after closure — and intervene early before a small problem becomes a big one.",
          video: { label: "Diagnosis & treatment of surgical site infection", id: "8BZyEmIgx0k", src: "citizensurgeon" },
          topics: [
            { icon: "🦠", t: "Infection", items: [
              "Signs: spreading erythema, warmth, pain out of proportion, purulent discharge, fever",
              "Remove affected sutures; open and drain abscesses; culture purulent material",
              "Antibiotics covering staph and strep; add gram-negative cover for bites (e.g. amoxicillin-clavulanate)",
              "Review at 24–48 h"
            ]},
            { icon: "💥", t: "Wound dehiscence", items: [
              "Causes: excess tension, early suture removal, infection, poor technique",
              "Superficial gap → heal by secondary intention with dressings",
              "Clean full-thickness dehiscence → re-suture after reassessment",
              "Infected dehiscence → never close; manage as infection"
            ]},
            { icon: "🩸", t: "Bleeding / hematoma", items: [
              "Persistent ooze → direct pressure; consider reversing anticoagulation when indicated",
              "Expanding hematoma → evacuate, identify the bleeder, ligate or cauterize, re-close",
              "Observe for pressure symptoms in closed compartments"
            ]},
            { icon: "🪡", t: "Scarring & other", items: [
              "Stitch marks / cross-hatching → remove on schedule, avoid tension, reinforce with tape",
              "Keloid / hypertrophic scar → silicone gel or sheets, pressure, intralesional steroids, referral",
              "Suture granuloma / sinus → remove the suture, pack if draining",
              "Strangulation / necrosis → loosen over-tightened throws; allow necrotic tissue to declare and granulate",
              "Needle-stick exposure → first aid, report, follow institutional exposure protocol"
            ]}
          ]
        }
      ];

      function renderPathway() {
        const ctn = document.getElementById("pathwayCtn");
        if (!ctn) return;
        ctn.innerHTML = PATHWAY.map(function (sec) {
          const topics = sec.topics ? '<div class="acc-grid">' + sec.topics.map(function (t) {
            return (
              '<div class="topic-card"><h5>' + t.icon + " " + t.t + "</h5><ul>" +
              t.items.map(function (i) { return "<li>" + i + "</li>"; }).join("") +
              "</ul></div>"
            );
          }).join("") + "</div>" : "";

          const steps = sec.steps ? '<div class="timeline">' + sec.steps.map(function (s, i) {
            return '<div class="tl-step"><span class="tl-tag">Step ' + (i + 1) + '</span><b>' + s.t + "</b><p>" + s.c + "</p></div>";
          }).join("") + "</div>" : "";

          const video = sec.video
            ? (sec.video.id
                ? '<div class="video-frame-sm"><iframe src="https://www.youtube-nocookie.com/embed/' + sec.video.id + '" title="' + sec.video.label + '" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen loading="lazy" referrerpolicy="strict-origin-when-cross-origin"></iframe></div>' + (sec.video.src ? '<p class="video-meta">🎬 Video · <b>' + sec.video.src + '</b></p>' : "")
                : '<div class="video-slot" aria-label="' + sec.video.label + ' — video placeholder"><span class="play">▶</span><div><b>' + sec.video.label + "</b><span>Video placeholder — add a videoId in the data to embed a clip here</span></div></div>")
            : "";

          return (
            '<div class="acc-item">' +
              '<button type="button" class="acc-btn" aria-expanded="false">' +
                '<span class="acc-num">' + sec.no + "</span>" +
                '<span class="acc-btn-tx"><b>' + sec.title + "</b><span>" + sec.sub + "</span></span>" +
                '<span class="acc-chev">▾</span>' +
              "</button>" +
              '<div class="acc-panel"><div class="acc-inner">' +
                '<p class="acc-intro">' + sec.intro + "</p>" +
                video +
                steps +
                topics +
              "</div></div>" +
            "</div>"
          );
        }).join("");

        ctn.querySelectorAll(".acc-item").forEach(function (item, idx) {
          const btn = item.querySelector(".acc-btn");
          btn.addEventListener("click", function () {
            const wasOpen = item.classList.contains("open");
            ctn.querySelectorAll(".acc-item.open").forEach(function (o) {
              o.classList.remove("open");
              o.querySelector(".acc-btn").setAttribute("aria-expanded", "false");
            });
            if (!wasOpen) {
              item.classList.add("open");
              btn.setAttribute("aria-expanded", "true");
            }
          });
          if (idx === 0) {
            item.classList.add("open");
            btn.setAttribute("aria-expanded", "true");
          }
        });
      }

      // ============================================================
      // DASHBOARD RENDER
      // ============================================================
      const modalBackdrop = document.getElementById("modalBackdrop");
      const modalBody = document.getElementById("modalBody");

      function cardHTML(d) {
        const tags = d.tags.map(function (t) { return "<span>" + t + "</span>"; }).join("");
        return (
          '<article class="card" role="button" tabindex="0" aria-label="Open ' + d.name + ' module" data-id="' + d.id + '">' +
            '<div class="card-top"><div class="card-icon">' + d.icon + '</div><div class="card-arrow">→</div></div>' +
            "<h3>" + d.name + "</h3>" +
            "<p>" + d.tagline + "</p>" +
            '<div class="tags">' + tags + "</div>" +
          "</article>"
        );
      }

      function renderGrids() {
        Object.keys(CATS).forEach(function (cat) {
          const grid = document.getElementById(CATS[cat].grid);
          const items = SUTURES.filter(function (s) { return s.category === cat; });
          grid.innerHTML = items.map(cardHTML).join("");
        });
        document.querySelectorAll(".card").forEach(function (card) {
          const open = function () { openModal(card.dataset.id); };
          card.addEventListener("click", open);
          card.addEventListener("keydown", function (e) {
            if (e.key === "Enter" || e.key === " ") { e.preventDefault(); open(); }
          });
        });
      }

      // ============================================================
      // MODAL + INTERACTIVE STEPPER
      // ============================================================
      let currentSteps = [];
      let stepIndex = 0;

      function sectionTitle(no, title) {
        return '<div class="m-sec-title"><span class="num">' + no + "</span>" + title + "</div>";
      }

      function buildModal(d) {
        const specRows = [
          ["Material", d.thread.material],
          ["Absorbable", d.thread.absorbable],
          ["Recommended size", d.thread.sizes],
          ["Needle", d.thread.needle],
          ["Common brands", d.thread.brands]
        ].map(function (r) { return '<div class="row"><div class="k">' + r[0] + '</div><div class="v">' + r[1] + "</div></div>"; }).join("");

        const comps = d.complications.map(function (c) {
          return '<div class="comp"><div class="c-name">' + c[0] + '</div><div class="c-mgmt"><b>Management:</b> ' + c[1] + "</div></div>";
        }).join("");

        const reminder = d.removal ? '<div class="reminder">📅 <b>Suture removal / protection:</b> ' + d.removal + "</div>" : "";
        const note = d.note ? '<div class="clinic-note">💡 <b>Clinical note:</b> ' + d.note + "</div>" : "";

        return (
          '<div class="m-sec">' + sectionTitle("01", "Optimal Thread Specifications") +
            '<div class="spec">' + specRows + "</div>" +
          "</div>" +

          '<div class="m-sec">' + sectionTitle("02", "Indications & Technique") +
            '<div class="two-col">' +
              '<div class="panel"><h4>Indications</h4><ul>' + d.indications.map(function (i) { return "<li>" + i + "</li>"; }).join("") + "</ul></div>" +
              '<div class="panel"><h4>Step-by-step technique</h4><ol>' + d.technique.map(function (t) { return "<li>" + t + "</li>"; }).join("") + "</ol></div>" +
            "</div>" + reminder + note +
          "</div>" +

          '<div class="m-sec">' + sectionTitle("03", "Complications & Management") +
            '<div class="comp-grid">' + comps + "</div>" +
          "</div>" +

          '<div class="m-sec">' + sectionTitle("04", "Video Demonstration & Step-by-Step Guide") +
            '<div class="stepper">' +
              '<div class="video-wrap" id="videoWrap">' +
                '<div class="video-frame">' +
                  '<iframe src="https://www.youtube-nocookie.com/embed/' + d.videoId + '" title="' + d.name + ' — technique demonstration" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen loading="lazy" referrerpolicy="strict-origin-when-cross-origin"></iframe>' +
                "</div>" +
                '<p class="video-meta">🎬 Video demonstration · <b>' + d.videoSource + '</b> — watch the exact hand movements before practicing.</p>' +
              "</div>" +
              '<div class="stage-cap"><h5 id="stepTitle"></h5><p id="stepCap"></p></div>' +
              '<div class="stage-controls">' +
                '<button id="stepPrev" aria-label="Previous step">←</button>' +
                '<div class="dots" id="stepDots"></div>' +
                '<button id="stepNext" aria-label="Next step">→</button>' +
              "</div>" +
              '<div class="progress"><div class="bar" id="stepBar"></div></div>' +
              '<p class="step-counter" id="stepCounter"></p>' +
            "</div>" +
          "</div>"
        );
      }

      function renderStepper() {
        const total = currentSteps.length;
        const s = currentSteps[stepIndex];
        const titleEl = document.getElementById("stepTitle");
        const capEl = document.getElementById("stepCap");
        const counterEl = document.getElementById("stepCounter");
        const barEl = document.getElementById("stepBar");
        const dotsEl = document.getElementById("stepDots");
        const prevBtn = document.getElementById("stepPrev");
        const nextBtn = document.getElementById("stepNext");

        titleEl.textContent = s.t;
        capEl.textContent = s.c;
        counterEl.textContent = "Step " + (stepIndex + 1) + " of " + total;
        barEl.style.width = ((stepIndex + 1) / total * 100) + "%";
        prevBtn.disabled = stepIndex === 0;
        nextBtn.disabled = stepIndex === total - 1;

        dotsEl.innerHTML = "";
        for (let i = 0; i < total; i++) {
          const dot = document.createElement("span");
          if (i === stepIndex) dot.className = "active";
          dot.title = "Step " + (i + 1);
          dot.addEventListener("click", function () { setStep(i); });
          dotsEl.appendChild(dot);
        }
      }

      function setStep(i) {
        const total = currentSteps.length;
        if (i < 0 || i >= total || i === stepIndex) return;
        stepIndex = i;
        const cap = document.querySelector(".stage-cap");
        cap.classList.remove("anim");
        void cap.offsetWidth;
        renderStepper();
        cap.classList.add("anim");
      }

      function initStepper(steps) {
        currentSteps = steps;
        stepIndex = 0;
        renderStepper();
        const prev = document.getElementById("stepPrev");
        const next = document.getElementById("stepNext");
        prev.addEventListener("click", function () { setStep(stepIndex - 1); });
        next.addEventListener("click", function () { setStep(stepIndex + 1); });

        const stepperEl = document.querySelector(".stepper");
        let touchX = null;
        stepperEl.addEventListener("touchstart", function (e) { touchX = e.touches[0].clientX; }, { passive: true });
        stepperEl.addEventListener("touchend", function (e) {
          if (touchX === null) return;
          const dx = e.changedTouches[0].clientX - touchX;
          if (Math.abs(dx) > 45) setStep(dx < 0 ? stepIndex + 1 : stepIndex - 1);
          touchX = null;
        }, { passive: true });
      }

      function openModal(id) {
        const d = SUTURES.find(function (s) { return s.id === id; });
        if (!d) return;
        document.getElementById("mCat").textContent = CATS[d.category].no + " · " + d.category;
        document.getElementById("mName").textContent = d.name;
        document.getElementById("mTagline").textContent = d.tagline;
        modalBody.innerHTML = buildModal(d);
        initStepper(d.steps);
        modalBackdrop.hidden = false;
        requestAnimationFrame(function () { modalBackdrop.classList.add("open"); });
        document.body.style.overflow = "hidden";
      }

      function closeModal() {
        modalBackdrop.classList.remove("open");
        document.body.style.overflow = "";
        setTimeout(function () { modalBackdrop.hidden = true; }, 260);
      }

      // ============================================================
      // AI TUTOR CHAT - ADAPTED FOR GITHUB PAGES (STATIC HOSTING)
      // ============================================================
      const drawer = document.getElementById("drawer");
      const chatEl = document.getElementById("chatEl");
      const chatInput = document.getElementById("chatInput");
      const sendBtn = document.getElementById("sendBtn");

      let busy = false;

      function esc(t) { return String(t).replace(/&/g, "&amp;").replace(/</g, "&lt;").replace(/>/g, "&gt;"); }
      function md(t) { return esc(t).replace(/\*\*(.+?)\*\*/g, "<b>$1</b>").replace(/\n/g, "<br>"); }
      function scrollBottom() { chatEl.scrollTop = chatEl.scrollHeight; }

      function addBubble(kind, html) {
        const div = document.createElement("div");
        div.className = kind === "user" ? "msg msg-user" : "msg msg-ai";
        div.innerHTML = html;
        chatEl.appendChild(div);
        scrollBottom();
        return div;
      }

      function setTyping(on) {
        let t = document.getElementById("typingEl");
        if (on) {
          if (!t) {
            t = document.createElement("div");
            t.id = "typingEl";
            t.className = "msg msg-ai";
            t.innerHTML = '<span class="typing-dots"><span></span><span></span><span></span></span>';
          }
          chatEl.appendChild(t);
          scrollBottom();
        } else if (t && t.parentNode) {
          t.parentNode.removeChild(t);
        }
      }

      // Mock AI response function for GitHub Pages since root.generateText won't work without a backend
      function send() {
        const text = chatInput.value.trim();
        if (!text || busy) return;
        
        chatInput.value = "";
        addBubble("user", md(text));
        busy = true;
        sendBtn.disabled = true;
        setTyping(true);
        
        // Simulating network delay for AI response
        setTimeout(function() {
          setTyping(false);
          const mockResponse = "أهلاً بك يا دكتور. هذا الموقع مستضاف حالياً كصفحة ثابتة (Static Page) على GitHub Pages، لذلك فإن محرك الذكاء الاصطناعي يعمل في وضع المحاكاة التجريبية. لربط هذه الخاصية بمحرك حقيقي مثل OpenAI أو Gemini، ستحتاج إلى إعداد خادم خلفي (Backend) لضمان أمان مفاتيح الـ API. \n\nهل تود مراجعة أي خطوات أو تقنيات موجودة في المنهج المعروض أمامك؟";
          addBubble("ai", md(mockResponse));
          busy = false;
          sendBtn.disabled = false;
        }, 1500);
      }

      function resetChat() {
        chatEl.innerHTML = "";
        setTyping(false);
        const greeting = "أهلاً بك يا دكتور مهند في SutureMaster PRO. أنا الذكاء الاصطناعي الجراحي الخاص بك. يمكنك سؤالي عن أي تقنية أو خطوة من خطوات الخياطة الجراحية وسأقوم بشرحها لك.";
        addBubble("ai", md(greeting));
      }

      let chatInitialized = false;
      function toggleDrawer(forceOpen) {
        const open = forceOpen !== undefined ? forceOpen : drawer.classList.contains("open");
        if (open) {
          drawer.classList.remove("open");
          setTimeout(function () { drawer.hidden = true; }, 330);
        } else {
          if (!chatInitialized) { resetChat(); chatInitialized = true; }
          drawer.hidden = false;
          requestAnimationFrame(function () { drawer.classList.add("open"); });
        }
      }

      // ============================================================
      // BINDINGS & INIT
      // ============================================================
      document.getElementById("modalClose").addEventListener("click", closeModal);
      modalBackdrop.addEventListener("click", function (e) { if (e.target === modalBackdrop) closeModal(); });
      document.addEventListener("keydown", function (e) {
        if (e.key === "Escape") { closeModal(); return; }
        if (modalBackdrop.hidden || !modalBackdrop.classList.contains("open")) return;
        if (e.key === "ArrowRight") { e.preventDefault(); setStep(stepIndex + 1); }
        else if (e.key === "ArrowLeft") { e.preventDefault(); setStep(stepIndex - 1); }
      });

      document.getElementById("aiToggle").addEventListener("click", function () { toggleDrawer(false); });
      document.getElementById("chatFab").addEventListener("click", function () { toggleDrawer(false); });
      document.getElementById("drawerClose").addEventListener("click", function () { toggleDrawer(true); });
      sendBtn.addEventListener("click", send);
      chatInput.addEventListener("keydown", function (e) { if (e.key === "Enter" && !e.shiftKey) { e.preventDefault(); send(); } });

      const footYear = document.getElementById("footYear");
      if (footYear) footYear.textContent = new Date().getFullYear();

      renderPathway();
      renderGrids();
    })();
  </script>
</body>
</html>
