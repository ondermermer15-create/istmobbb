<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>İstmop — Evden Eve Nakliyat & İstanbul Mobil Otopark</title>
<meta name="description" content="İstmop ile evden eve nakliyatta profesyonel ekipler, otopark bulmada akıllı çözümler. Sigortalı taşımacılık, asansörlü sistem ve mobil ödeme tek çatı altında.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Hanken+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#141A2E;
    --ink-soft:#454D63;
    --paper:#F5F6F9;
    --surface:#FFFFFF;
    --line:#E5E8EF;
    --blue:#2A4DFF;
    --blue-deep:#1B36C9;
    --blue-soft:#EBEEFF;
    --amber:#FF9D2E;
    --amber-deep:#E07C0A;
    --amber-soft:#FFF1DF;
    --radius:18px;
    --radius-sm:12px;
    --maxw:1140px;
    --ease:cubic-bezier(.22,.61,.36,1);
  }

  *{box-sizing:border-box;margin:0;padding:0}
  html{scroll-behavior:smooth}

  body{
    font-family:"Hanken Grotesk",system-ui,-apple-system,sans-serif;
    color:var(--ink);
    background:var(--paper);
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
  }

  h1,h2,h3,.display{font-family:"Space Grotesk",system-ui,sans-serif;letter-spacing:-.02em;line-height:1.05}

  a{color:inherit;text-decoration:none}
  img{max-width:100%;display:block}

  .wrap{max-width:var(--maxw);margin:0 auto;padding:0 24px}

  .eyebrow{
    font-family:"Space Grotesk",sans-serif;
    font-size:.78rem;font-weight:600;letter-spacing:.16em;text-transform:uppercase;
    display:inline-flex;align-items:center;gap:9px;color:var(--ink-soft);
  }
  .eyebrow::before{content:"";width:7px;height:7px;border-radius:50%;background:var(--blue);flex:0 0 auto}
  .eyebrow.amber::before{background:var(--amber)}

  /* ---------- Buttons ---------- */
  .btn{
    display:inline-flex;align-items:center;gap:9px;
    font-family:"Space Grotesk",sans-serif;font-weight:600;font-size:.95rem;
    padding:14px 24px;border-radius:100px;border:1.5px solid transparent;
    cursor:pointer;transition:transform .25s var(--ease),box-shadow .25s var(--ease),background .2s;
    will-change:transform;
  }
  .btn svg{transition:transform .3s var(--ease)}
  .btn:hover{transform:translateY(-2px)}
  .btn:hover svg{transform:translateX(3px)}
  .btn-blue{background:var(--blue);color:#fff;box-shadow:0 10px 26px -10px rgba(42,77,255,.65)}
  .btn-blue:hover{box-shadow:0 16px 34px -10px rgba(42,77,255,.75)}
  .btn-amber{background:var(--amber);color:#241200;box-shadow:0 10px 26px -10px rgba(255,157,46,.65)}
  .btn-amber:hover{box-shadow:0 16px 34px -10px rgba(255,157,46,.75)}
  .btn-ghost{border-color:var(--line);color:var(--ink);background:transparent}
  .btn-ghost:hover{border-color:var(--ink);background:var(--ink);color:#fff}
  .btn-outline-light{border-color:rgba(255,255,255,.3);color:#fff}
  .btn-outline-light:hover{border-color:#fff;background:#fff;color:var(--ink)}

  :focus-visible{outline:3px solid var(--blue);outline-offset:3px;border-radius:6px}

  /* ---------- Header ---------- */
  header{
    position:sticky;top:0;z-index:60;
    background:rgba(245,246,249,.82);backdrop-filter:blur(14px);
    border-bottom:1px solid transparent;transition:border-color .3s,background .3s;
  }
  header.scrolled{border-bottom-color:var(--line)}
  .nav{display:flex;align-items:center;justify-content:space-between;height:72px}
  .brand{display:flex;align-items:center;gap:11px;font-family:"Space Grotesk",sans-serif;font-weight:700;font-size:1.25rem;letter-spacing:-.03em}
  .brand .mark{
    width:30px;height:30px;border-radius:9px;background:var(--ink);position:relative;flex:0 0 auto;
  }
  .brand .mark::before{content:"";position:absolute;width:8px;height:8px;border-radius:50%;background:var(--amber);top:7px;left:7px}
  .brand .mark::after{content:"";position:absolute;width:8px;height:8px;border-radius:50%;background:var(--blue);bottom:7px;right:7px;box-shadow:-3px -3px 0 -2px var(--paper)}
  .navlinks{display:flex;align-items:center;gap:34px}
  .navlinks a{font-size:.95rem;font-weight:500;color:var(--ink-soft);transition:color .2s;position:relative}
  .navlinks a:hover{color:var(--ink)}
  .navlinks a::after{content:"";position:absolute;left:0;bottom:-5px;height:2px;width:0;background:var(--blue);transition:width .25s var(--ease)}
  .navlinks a:hover::after{width:100%}
  .nav-cta{display:flex;align-items:center;gap:14px}
  .menu-toggle{display:none;background:none;border:none;cursor:pointer;padding:8px;color:var(--ink)}

  /* ---------- Hero ---------- */
  .hero{
    background:var(--ink);color:#fff;position:relative;overflow:hidden;
    padding:84px 0 96px;
  }
  .hero::before{
    content:"";position:absolute;inset:0;
    background:radial-gradient(900px 500px at 78% 12%,rgba(42,77,255,.28),transparent 60%),
               radial-gradient(700px 500px at 12% 96%,rgba(255,157,46,.16),transparent 55%);
    pointer-events:none;
  }
  .hero .wrap{position:relative;display:grid;grid-template-columns:1.05fr .95fr;gap:56px;align-items:center}
  .hero-eyebrow{color:rgba(255,255,255,.7)}
  .hero-eyebrow::before{background:var(--amber)}
  .hero h1{font-size:clamp(2.5rem,5.4vw,4.1rem);font-weight:700;margin:22px 0 20px}
  .hero h1 em{font-style:normal;color:var(--amber);position:relative;white-space:nowrap}
  .hero p.lead{font-size:1.18rem;color:rgba(255,255,255,.74);max-width:30ch;margin-bottom:34px}
  .hero-cta{display:flex;flex-wrap:wrap;gap:14px}

  /* route visual */
  .route{width:100%;height:auto;overflow:visible}
  .route-path{
    fill:none;stroke:rgba(255,255,255,.22);stroke-width:2.5;stroke-dasharray:8 9;stroke-linecap:round;
  }
  .route-draw{
    fill:none;stroke:url(#grad);stroke-width:3;stroke-linecap:round;
    stroke-dasharray:560;stroke-dashoffset:560;
    animation:draw 2.4s var(--ease) .3s forwards;
  }
  @keyframes draw{to{stroke-dashoffset:0}}
  .node-label{font-family:"Space Grotesk",sans-serif;font-size:13px;font-weight:600;fill:#fff}
  .node-sub{font-family:"Hanken Grotesk",sans-serif;font-size:11px;fill:rgba(255,255,255,.6)}
  .pulse{transform-origin:center;animation:pulse 2.4s ease-in-out infinite}
  @keyframes pulse{0%,100%{opacity:.35;r:18}50%{opacity:0;r:30}}
  .mover{
    offset-path:path("M 60 250 C 150 250 150 90 250 90 C 360 90 340 250 440 250");
    offset-distance:0%;
    animation:travel 4s var(--ease) 2.2s infinite;
  }
  @keyframes travel{0%{offset-distance:0%;opacity:0}8%{opacity:1}92%{opacity:1}100%{offset-distance:100%;opacity:0}}

  /* ---------- Value strip ---------- */
  .strip{background:var(--surface);border-bottom:1px solid var(--line)}
  .strip .wrap{display:flex;flex-wrap:wrap;gap:14px 40px;padding-top:26px;padding-bottom:26px;justify-content:center}
  .chip{display:flex;align-items:center;gap:11px;font-weight:500;font-size:.97rem;color:var(--ink)}
  .chip svg{flex:0 0 auto}

  /* ---------- Sections ---------- */
  .sec{padding:96px 0}
  .sec-head{max-width:620px;margin-bottom:52px}
  .sec-head h2{font-size:clamp(2rem,4vw,2.9rem);font-weight:700;margin:18px 0 16px}
  .sec-head p{font-size:1.12rem;color:var(--ink-soft)}

  /* nakliyat cards */
  .cards{display:grid;grid-template-columns:repeat(2,1fr);gap:20px}
  .card{
    background:var(--surface);border:1px solid var(--line);border-radius:var(--radius);
    padding:30px 28px;transition:transform .35s var(--ease),box-shadow .35s var(--ease),border-color .35s;
    position:relative;overflow:hidden;
  }
  .card::after{content:"";position:absolute;left:0;top:0;height:100%;width:4px;background:var(--amber);transform:scaleY(0);transform-origin:top;transition:transform .35s var(--ease)}
  .card:hover{transform:translateY(-5px);box-shadow:0 22px 44px -24px rgba(20,26,46,.3);border-color:transparent}
  .card:hover::after{transform:scaleY(1)}
  .card .ico{
    width:52px;height:52px;border-radius:14px;background:var(--amber-soft);color:var(--amber-deep);
    display:flex;align-items:center;justify-content:center;margin-bottom:20px;
  }
  .card h3{font-size:1.22rem;font-weight:600;margin-bottom:9px}
  .card p{color:var(--ink-soft);font-size:.99rem}

  /* checklist panel */
  .panel{
    margin-top:24px;background:var(--ink);color:#fff;border-radius:24px;
    padding:48px;display:grid;grid-template-columns:.85fr 1.15fr;gap:40px;align-items:center;
    position:relative;overflow:hidden;
  }
  .panel::before{content:"";position:absolute;inset:0;background:radial-gradient(600px 400px at 100% 0,rgba(255,157,46,.18),transparent 60%);pointer-events:none}
  .panel-l{position:relative}
  .panel-l .eyebrow{color:rgba(255,255,255,.7)}
  .panel-l .eyebrow::before{background:var(--amber)}
  .panel-l h3{font-size:1.7rem;font-weight:700;margin:16px 0 10px;color:#fff}
  .panel-l p{color:rgba(255,255,255,.66)}
  .checklist{position:relative;display:flex;flex-direction:column;gap:2px}
  .check-item{display:flex;gap:16px;padding:16px 0;border-bottom:1px solid rgba(255,255,255,.1)}
  .check-item:last-child{border-bottom:none}
  .check-num{
    font-family:"Space Grotesk",sans-serif;font-weight:600;font-size:.85rem;
    width:30px;height:30px;flex:0 0 auto;border-radius:9px;background:rgba(255,255,255,.08);
    color:var(--amber);display:flex;align-items:center;justify-content:center;
  }
  .check-item h4{font-size:1.02rem;font-weight:600;margin-bottom:3px}
  .check-item p{font-size:.92rem;color:rgba(255,255,255,.6)}

  /* ---------- İSTMOP section ---------- */
  .istmop{background:var(--surface);border-top:1px solid var(--line);border-bottom:1px solid var(--line)}
  .istmop-grid{display:grid;grid-template-columns:1fr 1fr;gap:64px;align-items:center}
  .feat-list{display:flex;flex-direction:column;gap:8px;margin-top:8px}
  .feat{display:flex;gap:16px;align-items:flex-start;padding:14px 0}
  .feat .fic{
    width:46px;height:46px;flex:0 0 auto;border-radius:13px;background:var(--blue-soft);color:var(--blue);
    display:flex;align-items:center;justify-content:center;
  }
  .feat h4{font-size:1.08rem;font-weight:600;margin-bottom:3px}
  .feat p{color:var(--ink-soft);font-size:.96rem}

  /* phone mockup */
  .phone-stage{display:flex;justify-content:center;position:relative}
  .phone-stage::before{
    content:"";position:absolute;width:320px;height:320px;border-radius:50%;
    background:radial-gradient(circle,var(--blue-soft),transparent 70%);z-index:0;
  }
  .phone{
    position:relative;z-index:1;width:286px;height:580px;background:var(--ink);border-radius:42px;
    padding:13px;box-shadow:0 40px 80px -30px rgba(20,26,46,.5);
  }
  .phone-screen{width:100%;height:100%;background:#EEF1F6;border-radius:30px;overflow:hidden;position:relative;display:flex;flex-direction:column}
  .ph-notch{position:absolute;top:10px;left:50%;transform:translateX(-50%);width:96px;height:20px;background:var(--ink);border-radius:0 0 14px 14px;z-index:5}
  .ph-top{padding:30px 20px 14px;background:var(--blue);color:#fff}
  .ph-top .pt-row{display:flex;align-items:center;justify-content:space-between;margin-bottom:14px}
  .ph-top .pt-title{font-family:"Space Grotesk",sans-serif;font-weight:600;font-size:1.05rem}
  .ph-search{background:rgba(255,255,255,.18);border-radius:11px;padding:10px 13px;display:flex;align-items:center;gap:9px;font-size:.82rem;color:rgba(255,255,255,.9)}
  .ph-map{flex:1;position:relative;background:
      linear-gradient(0deg,rgba(0,0,0,.02),rgba(0,0,0,.02)),
      repeating-linear-gradient(90deg,#E3E8F0 0 1px,transparent 1px 46px),
      repeating-linear-gradient(0deg,#E3E8F0 0 1px,transparent 1px 46px),
      #EEF1F6;overflow:hidden}
  .road{position:absolute;background:#D5DCE7}
  .road.r1{top:30%;left:-10%;width:130%;height:14px;transform:rotate(-7deg)}
  .road.r2{top:0;left:58%;width:13px;height:120%;transform:rotate(6deg)}
  .pin{position:absolute;display:flex;flex-direction:column;align-items:center;z-index:3}
  .pin .dot{width:30px;height:30px;border-radius:50% 50% 50% 2px;transform:rotate(45deg);display:flex;align-items:center;justify-content:center;box-shadow:0 6px 14px -4px rgba(0,0,0,.4)}
  .pin .dot span{transform:rotate(-45deg);color:#fff;font-family:"Space Grotesk",sans-serif;font-weight:700;font-size:.8rem}
  .pin.green .dot{background:#16A34A}
  .pin.blue .dot{background:var(--blue)}
  .pin.red .dot{background:#E0492F}
  .pin.p1{top:22%;left:24%}
  .pin.p2{top:54%;left:60%}
  .pin.p3{top:38%;left:74%}
  .pin.sel .dot{width:38px;height:38px;animation:bob 2.2s ease-in-out infinite}
  @keyframes bob{0%,100%{transform:rotate(45deg) translateY(0)}50%{transform:rotate(45deg) translateY(-6px)}}
  .ph-card{position:absolute;left:12px;right:12px;bottom:12px;background:#fff;border-radius:18px;padding:15px 16px;box-shadow:0 14px 30px -12px rgba(20,26,46,.35);z-index:4}
  .ph-card .pc-row{display:flex;align-items:center;justify-content:space-between;margin-bottom:4px}
  .ph-card .pc-name{font-family:"Space Grotesk",sans-serif;font-weight:600;font-size:.98rem;color:var(--ink)}
  .pc-badge{font-size:.68rem;font-weight:600;color:#16A34A;background:#E7F6ED;padding:4px 9px;border-radius:100px}
  .ph-card .pc-meta{font-size:.78rem;color:var(--ink-soft);margin-bottom:12px}
  .pc-btn{background:var(--blue);color:#fff;text-align:center;font-family:"Space Grotesk",sans-serif;font-weight:600;font-size:.86rem;padding:11px;border-radius:11px}

  .callout{
    margin-top:34px;display:flex;gap:14px;align-items:flex-start;
    background:var(--blue-soft);border-radius:var(--radius-sm);padding:18px 20px;
  }
  .callout svg{flex:0 0 auto;color:var(--blue);margin-top:2px}
  .callout p{font-size:.93rem;color:var(--ink)}
  .callout strong{color:var(--blue-deep)}

  /* ---------- Benefits ---------- */
  .benefits-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-top:8px}
  .bcard{background:var(--surface);border:1px solid var(--line);border-radius:var(--radius);padding:34px 32px}
  .bcard .tag{display:inline-flex;align-items:center;gap:8px;font-family:"Space Grotesk",sans-serif;font-size:.74rem;font-weight:600;letter-spacing:.1em;text-transform:uppercase;padding:6px 12px;border-radius:100px;margin-bottom:18px}
  .bcard.amber-tag .tag{background:var(--amber-soft);color:var(--amber-deep)}
  .bcard.blue-tag .tag{background:var(--blue-soft);color:var(--blue-deep)}
  .bcard h3{font-size:1.3rem;font-weight:600;margin-bottom:10px}
  .bcard ul{list-style:none;display:flex;flex-direction:column;gap:10px;margin-top:16px}
  .bcard li{display:flex;gap:11px;font-size:.97rem;color:var(--ink-soft)}
  .bcard li svg{flex:0 0 auto;margin-top:4px}
  .unite{text-align:center;margin-top:34px;max-width:680px;margin-left:auto;margin-right:auto;font-size:1.12rem;color:var(--ink-soft)}

  /* ---------- CTA ---------- */
  .cta{background:var(--ink);color:#fff;position:relative;overflow:hidden;padding:90px 0}
  .cta::before{content:"";position:absolute;inset:0;background:radial-gradient(700px 400px at 20% 0,rgba(42,77,255,.3),transparent 55%),radial-gradient(700px 400px at 90% 100%,rgba(255,157,46,.18),transparent 55%);pointer-events:none}
  .cta .wrap{position:relative;text-align:center}
  .cta h2{font-size:clamp(2rem,4.4vw,3.1rem);font-weight:700;margin-bottom:16px}
  .cta p{font-size:1.15rem;color:rgba(255,255,255,.72);max-width:46ch;margin:0 auto 16px}
  .cta-note{font-size:.85rem;color:rgba(255,255,255,.45);margin:6px auto 32px}
  .cta-actions{display:flex;flex-wrap:wrap;gap:14px;justify-content:center}

  /* ---------- Footer ---------- */
  footer{background:var(--ink);color:rgba(255,255,255,.6);border-top:1px solid rgba(255,255,255,.1);padding:34px 0}
  .foot{display:flex;flex-wrap:wrap;align-items:center;justify-content:space-between;gap:18px}
  .foot .brand{color:#fff}
  .foot-links{display:flex;gap:26px;font-size:.92rem}
  .foot-links a:hover{color:#fff}
  .foot small{font-size:.85rem}

  /* ---------- Reveal ---------- */
  .reveal{opacity:0;transform:translateY(26px);transition:opacity .7s var(--ease),transform .7s var(--ease)}
  .reveal.in{opacity:1;transform:none}

  /* ---------- Responsive ---------- */
  @media(max-width:920px){
    .hero .wrap{grid-template-columns:1fr;gap:40px}
    .hero-visual{max-width:480px}
    .istmop-grid{grid-template-columns:1fr;gap:48px}
    .phone-stage{order:-1}
    .panel{grid-template-columns:1fr;gap:30px;padding:38px 30px}
    .navlinks,.nav-cta .btn{display:none}
    .menu-toggle{display:block}
  }
  @media(max-width:680px){
    .cards{grid-template-columns:1fr}
    .benefits-grid{grid-template-columns:1fr}
    .sec{padding:70px 0}
    .hero{padding:60px 0 72px}
    .panel{padding:30px 22px}
    .strip .wrap{justify-content:flex-start}
  }

  /* mobile menu */
  .mobile-menu{display:none;position:fixed;inset:72px 0 0;background:var(--paper);z-index:55;padding:30px 24px;flex-direction:column;gap:8px}
  .mobile-menu.open{display:flex}
  .mobile-menu a{font-family:"Space Grotesk",sans-serif;font-size:1.4rem;font-weight:600;padding:14px 0;border-bottom:1px solid var(--line)}
  .mobile-menu .btn{margin-top:18px;justify-content:center}

  @media(prefers-reduced-motion:reduce){
    *{animation:none !important;transition:none !important}
    .route-draw{stroke-dashoffset:0}
    .reveal{opacity:1;transform:none}
    html{scroll-behavior:auto}
  }
</style>
</head>
<body>

<header id="top">
  <div class="wrap nav">
    <a href="#top" class="brand"><span class="mark"></span>istmop</a>
    <nav class="navlinks">
      <a href="#nakliyat">Nakliyat</a>
      <a href="#istmop">İSTMOP</a>
      <a href="#faydalar">Neden İstmop</a>
      <a href="#iletisim">İletişim</a>
    </nav>
    <div class="nav-cta">
      <a href="#iletisim" class="btn btn-blue">İletişime geç
        <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14M13 6l6 6-6 6"/></svg>
      </a>
      <button class="menu-toggle" aria-label="Menüyü aç" aria-expanded="false" id="menuBtn">
        <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round"><path d="M4 7h16M4 12h16M4 17h16"/></svg>
      </button>
    </div>
  </div>
</header>

<div class="mobile-menu" id="mobileMenu">
  <a href="#nakliyat">Nakliyat</a>
  <a href="#istmop">İSTMOP</a>
  <a href="#faydalar">Neden İstmop</a>
  <a href="#iletisim">İletişim</a>
  <a href="#iletisim" class="btn btn-blue">İletişime geç</a>
</div>

<!-- HERO -->
<section class="hero">
  <div class="wrap">
    <div class="hero-text">
      <span class="eyebrow hero-eyebrow">Nakliyat &nbsp;·&nbsp; Mobil Otopark</span>
      <h1>Şehirde her şey <em>yerli yerinde</em>.</h1>
      <p class="lead">Evden eve nakliyatta profesyonel ekipler, otopark bulmada akıllı çözümler. İstmop ile zamandan kazanın, gününüzü kolaylaştırın.</p>
      <div class="hero-cta">
        <a href="#nakliyat" class="btn btn-amber">Nakliyat hizmeti
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14M13 6l6 6-6 6"/></svg>
        </a>
        <a href="#istmop" class="btn btn-outline-light">İSTMOP'u keşfet</a>
      </div>
    </div>
    <div class="hero-visual">
      <svg class="route" viewBox="0 0 500 320" role="img" aria-label="Evden otoparka uzanan rota">
        <defs>
          <linearGradient id="grad" x1="0" y1="0" x2="1" y2="0">
            <stop offset="0%" stop-color="#FF9D2E"/>
            <stop offset="100%" stop-color="#2A4DFF"/>
          </linearGradient>
        </defs>
        <!-- dashed base -->
        <path class="route-path" d="M 60 250 C 150 250 150 90 250 90 C 360 90 340 250 440 250"/>
        <!-- animated draw -->
        <path class="route-draw" d="M 60 250 C 150 250 150 90 250 90 C 360 90 340 250 440 250"/>
        <!-- moving dot -->
        <circle class="mover" r="6" fill="#fff"/>

        <!-- origin: home -->
        <circle class="pulse" cx="60" cy="250" r="18" fill="#FF9D2E"/>
        <circle cx="60" cy="250" r="22" fill="#1B2138" stroke="#FF9D2E" stroke-width="2"/>
        <g transform="translate(48,238)" stroke="#FF9D2E" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round">
          <path d="M2 11 L12 3 L22 11"/><path d="M5 9 V20 H19 V9"/>
        </g>
        <text class="node-label" x="32" y="296">Eski adres</text>
        <text class="node-sub" x="32" y="312">eşyalar hazır</text>

        <!-- destination: parking P -->
        <circle cx="440" cy="250" r="22" fill="#1B2138" stroke="#2A4DFF" stroke-width="2"/>
        <text x="440" y="258" text-anchor="middle" font-family="Space Grotesk" font-weight="700" font-size="20" fill="#2A4DFF">P</text>
        <text class="node-label" x="448" y="296" text-anchor="end">Yeni hayat</text>
        <text class="node-sub" x="448" y="312" text-anchor="end">park yeri hazır</text>
      </svg>
    </div>
  </div>
</section>

<!-- VALUE STRIP -->
<div class="strip">
  <div class="wrap">
    <span class="chip"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#FF9D2E" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>Sigortalı taşımacılık</span>
    <span class="chip"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#FF9D2E" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M6 22V8l6-4 6 4v14M9 22v-6h6v6"/></svg>Asansörlü sistem</span>
    <span class="chip"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#2A4DFF" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 10c0 6-9 12-9 12S3 16 3 10a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>Harita üzerinden otopark</span>
    <span class="chip"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#2A4DFF" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="6" y="2" width="12" height="20" rx="3"/><path d="M11 18h2"/></svg>Mobil ödeme</span>
    <span class="chip"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#454D63" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M12 7v5l3 2"/></svg>7/24 erişim</span>
  </div>
</div>

<!-- NAKLIYAT -->
<section class="sec" id="nakliyat">
  <div class="wrap">
    <div class="sec-head reveal">
      <span class="eyebrow amber">Evden Eve Nakliyat</span>
      <h2>Taşınmak artık yorucu değil</h2>
      <p>Profesyonel ekipler eşyalarınızı paketlemekten yeni adreste yeniden kurmaya kadar tüm süreci üstlenir. Siz sadece yeni evinizin keyfini çıkarın.</p>
    </div>

    <div class="cards">
      <div class="card reveal">
        <div class="ico"><svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 16V8a2 2 0 00-1-1.7l-7-4a2 2 0 00-2 0l-7 4A2 2 0 003 8v8a2 2 0 001 1.7l7 4a2 2 0 002 0l7-4A2 2 0 0021 16z"/><path d="M3.3 7L12 12l8.7-5M12 22V12"/></svg></div>
        <h3>Profesyonel paketleme</h3>
        <p>Kırılabilir eşyalarınız özel ambalaj malzemeleriyle tek tek korunur; hiçbir parça zarar görmeden yola çıkar.</p>
      </div>
      <div class="card reveal">
        <div class="ico"><svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M14.7 6.3a4 4 0 00-5.4 5.4l-6 6 3 3 6-6a4 4 0 005.4-5.4l-2.5 2.5-2.5-2.5z"/></svg></div>
        <h3>Demontaj &amp; montaj</h3>
        <p>Mobilyalarınız uzman ekipler tarafından sökülür, taşınır ve yeni evinizde aynı özenle yeniden kurulur.</p>
      </div>
      <div class="card reveal">
        <div class="ico"><svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M6 22V8l6-4 6 4v14"/><path d="M9 22v-6h6v6M9 11h6M9 14.5h6"/></svg></div>
        <h3>Asansörlü taşımacılık</h3>
        <p>Yüksek katlı binalarda eşyalar hızlı ve güvenli şekilde taşınır; hem zaman kazanırsınız hem de risk en aza iner.</p>
      </div>
      <div class="card reveal">
        <div class="ico"><svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/><path d="M9 12l2 2 4-4"/></svg></div>
        <h3>Sigortalı taşıma</h3>
        <p>Sigortalı taşımacılık sayesinde süreç boyunca oluşabilecek olası zararlar tamamen güvence altındadır.</p>
      </div>
    </div>

    <!-- checklist -->
    <div class="panel reveal">
      <div class="panel-l">
        <span class="eyebrow amber">Karar verirken</span>
        <h3>Doğru firmayı seçmenin yolu</h3>
        <p>Birkaç basit kontrol, taşınma gününüzü sürprizlerden korur.</p>
      </div>
      <div class="checklist">
        <div class="check-item">
          <span class="check-num">01</span>
          <div><h4>Güvenilir ve sigortalı firma</h4><p>Sigortalı taşımacılık sunan firmaları tercih edin; eşyalarınız güvence altına alınsın.</p></div>
        </div>
        <div class="check-item">
          <span class="check-num">02</span>
          <div><h4>Müşteri yorumlarını inceleyin</h4><p>Daha önce hizmet alanların deneyimi, firmanın kalitesi hakkında en net fikri verir.</p></div>
        </div>
        <div class="check-item">
          <span class="check-num">03</span>
          <div><h4>Birden fazla teklif alın</h4><p>Farklı firmalardan fiyat teklifi alarak hem bütçenizi hem de hizmet kapsamını karşılaştırın.</p></div>
        </div>
        <div class="check-item">
          <span class="check-num">04</span>
          <div><h4>Detayları baştan netleştirin</h4><p>Hizmetin neleri kapsadığını önceden konuşun; sonradan sürprizle karşılaşmayın.</p></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- İSTMOP -->
<section class="istmop" id="istmop">
  <div class="wrap sec">
    <div class="istmop-grid">
      <div class="istmop-text reveal">
        <span class="eyebrow">İstanbul Mobil Otopark</span>
        <h2 style="font-family:'Space Grotesk';font-size:clamp(2rem,4vw,2.9rem);font-weight:700;margin:18px 0 16px;letter-spacing:-.02em">Boş park yeri aramak tarih oldu</h2>
        <p style="font-size:1.1rem;color:var(--ink-soft);margin-bottom:8px">İSTMOP, şehirdeki otoparkları ve yol kenarı alanları haritada gösterir, doluluk durumunu anlık iletir ve ödemeyi tek dokunuşla halleder. Telefonunuz cebinizdeyken park sorunu da çözülmüş demektir.</p>

        <div class="feat-list">
          <div class="feat">
            <div class="fic"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 10c0 6-9 12-9 12S3 16 3 10a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg></div>
            <div><h4>En yakın otoparkı haritada bul</h4><p>Bulunduğunuz bölgedeki müsait park alanlarını saniyeler içinde görün.</p></div>
          </div>
          <div class="feat">
            <div class="fic"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 12h4l3 8 4-16 3 8h4"/></svg></div>
            <div><h4>Anlık doluluk bilgisi</h4><p>Hangi otoparkta yer var, gitmeden önce öğrenin; boşuna tur atmayın.</p></div>
          </div>
          <div class="feat">
            <div class="fic"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="6" y="2" width="12" height="20" rx="3"/><path d="M10 18h4"/></svg></div>
            <div><h4>Mobil ödeme</h4><p>Nakit taşıma zorunluluğu yok; ücretinizi uygulama üzerinden anında ödeyin.</p></div>
          </div>
          <div class="feat">
            <div class="fic"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M12 7v5l3 2"/></svg></div>
            <div><h4>Park süresini yönet</h4><p>Park sürenizi başlatın, durdurun ve geçmiş işlemlerinizi kolayca takip edin.</p></div>
          </div>
        </div>

        <div class="callout">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="M12 16v-4M12 8h.01"/></svg>
          <p>Sürenizi doğru başlatıp bitirdiğinizde otopark doluluk bilgileri güncel kalır. Böylece boşalan yerler <strong>başka sürücüler tarafından da hızlıca</strong> kullanılır.</p>
        </div>
      </div>

      <!-- phone mockup -->
      <div class="phone-stage reveal" aria-hidden="true">
        <div class="phone">
          <div class="phone-screen">
            <div class="ph-notch"></div>
            <div class="ph-top">
              <div class="pt-row">
                <span class="pt-title">İSTMOP</span>
                <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><circle cx="11" cy="11" r="7"/><path d="M21 21l-4-4"/></svg>
              </div>
              <div class="ph-search">
                <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 10c0 6-9 12-9 12S3 16 3 10a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>
                Yakınımdaki otoparklar
              </div>
            </div>
            <div class="ph-map">
              <span class="road r1"></span>
              <span class="road r2"></span>
              <div class="pin green p1"><span class="dot"><span>P</span></span></div>
              <div class="pin red p3"><span class="dot"><span>P</span></span></div>
              <div class="pin blue sel p2"><span class="dot"><span>P</span></span></div>
              <div class="ph-card">
                <div class="pc-row">
                  <span class="pc-name">Merkez Otoparkı</span>
                  <span class="pc-badge">12 yer boş</span>
                </div>
                <div class="pc-meta">350 m · ₺25 / saat · Açık</div>
                <div class="pc-btn">Park et</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- BENEFITS -->
<section class="sec" id="faydalar">
  <div class="wrap">
    <div class="sec-head reveal" style="max-width:680px">
      <span class="eyebrow">Neden İstmop</span>
      <h2>İki hizmet, tek amaç: zamanınız</h2>
      <p>Farklı alanlarda görünseler de nakliyat ve İSTMOP aynı sözü verir — günlük işlerinizi dijital kolaylıkla, hızlı ve düzenli yürütmek.</p>
    </div>

    <div class="benefits-grid">
      <div class="bcard amber-tag reveal">
        <span class="tag">Nakliyat tarafında</span>
        <h3>Taşınma sürecini hızlandırır</h3>
        <p style="color:var(--ink-soft)">Dijital çözümlerle planlama, eskiden günler süren işi saatlere indirir.</p>
        <ul>
          <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#FF9D2E" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6L9 17l-5-5"/></svg>Online teklif alma</li>
          <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#FF9D2E" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6L9 17l-5-5"/></svg>Keşif hizmeti</li>
          <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#FF9D2E" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6L9 17l-5-5"/></svg>Taşıma takibi</li>
        </ul>
      </div>
      <div class="bcard blue-tag reveal">
        <span class="tag">Otopark tarafında</span>
        <h3>Park ve ödemeyi kolaylaştırır</h3>
        <p style="color:var(--ink-soft)">Boş yer aramak için harcanan zaman, yakıt ve trafik yükü ortadan kalkar.</p>
        <ul>
          <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#2A4DFF" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6L9 17l-5-5"/></svg>Harita entegrasyonu</li>
          <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#2A4DFF" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6L9 17l-5-5"/></svg>Anlık doluluk bilgisi</li>
          <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#2A4DFF" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6L9 17l-5-5"/></svg>Mobil ödeme</li>
        </ul>
      </div>
    </div>
    <p class="unite reveal">Sonuç olarak her iki hizmet de modern şehir yaşamında zamanı daha verimli kullanmanıza ve gündelik işlerinizi daha konforlu yürütmenize yardımcı olur.</p>
  </div>
</section>

<!-- CTA -->
<section class="cta" id="iletisim">
  <div class="wrap">
    <h2>Başlamaya hazır mısınız?</h2>
    <p>İster yeni evinize taşının, ister şehirde park yeri bulun — İstmop yanınızda.</p>
    <p class="cta-note">İletişim bilgilerinizi buraya ekleyin · örnek: 0850 000 00 00 · info@istmop.com</p>
    <div class="cta-actions">
      <a href="tel:08500000000" class="btn btn-blue">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M22 16.9v3a2 2 0 01-2.2 2 19.8 19.8 0 01-8.6-3 19.5 19.5 0 01-6-6 19.8 19.8 0 01-3-8.6A2 2 0 014.1 2h3a2 2 0 012 1.7c.1.9.3 1.8.6 2.6a2 2 0 01-.5 2.1L8.1 9.9a16 16 0 006 6l1.5-1.1a2 2 0 012.1-.5c.8.3 1.7.5 2.6.6a2 2 0 011.7 2z"/></svg>
        Hemen arayın
      </a>
      <a href="#nakliyat" class="btn btn-outline-light">Hizmetleri incele</a>
    </div>
  </div>
</section>

<footer>
  <div class="wrap foot">
    <a href="#top" class="brand"><span class="mark"></span>istmop</a>
    <nav class="foot-links">
      <a href="#nakliyat">Nakliyat</a>
      <a href="#istmop">İSTMOP</a>
      <a href="#faydalar">Neden İstmop</a>
      <a href="#iletisim">İletişim</a>
    </nav>
    <small>© 2026 İstmop · Evden eve nakliyat &amp; mobil otopark</small>
  </div>
</footer>

<script>
  // header shadow on scroll
  const header = document.querySelector('header');
  const onScroll = () => header.classList.toggle('scrolled', window.scrollY > 12);
  onScroll();
  window.addEventListener('scroll', onScroll, {passive:true});

  // mobile menu
  const menuBtn = document.getElementById('menuBtn');
  const mobileMenu = document.getElementById('mobileMenu');
  menuBtn.addEventListener('click', () => {
    const open = mobileMenu.classList.toggle('open');
    menuBtn.setAttribute('aria-expanded', open);
    document.body.style.overflow = open ? 'hidden' : '';
  });
  mobileMenu.querySelectorAll('a').forEach(a => a.addEventListener('click', () => {
    mobileMenu.classList.remove('open');
    menuBtn.setAttribute('aria-expanded', false);
    document.body.style.overflow = '';
  }));

  // scroll reveal
  const reduce = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  if (!reduce) {
    const io = new IntersectionObserver((entries) => {
      entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('in'); io.unobserve(e.target); } });
    }, {threshold:0.14, rootMargin:'0px 0px -40px 0px'});
    document.querySelectorAll('.reveal').forEach(el => io.observe(el));
  } else {
    document.querySelectorAll('.reveal').forEach(el => el.classList.add('in'));
  }
</script>
</body>
</html>
