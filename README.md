<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DPS Security Solutions | CCTV & Surveillance Experts</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Archivo:wght@500;600;700;800;900&family=Archivo+Expanded:wght@700;800&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#0c1015;
    --panel:#11161d;
    --panel-2:#161d26;
    --line: rgba(180,196,210,0.14);
    --line-strong: rgba(180,196,210,0.28);
    --fog:#7e8c9a;
    --paper:#e9edf1;
    --amber:#ff8a1f;
    --rec:#ff3b3b;
    --status:#34d399;
    --radius: 2px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--ink);
    color:var(--paper);
    font-family:'Archivo', sans-serif;
    -webkit-font-smoothing:antialiased;
  }
  .mono{ font-family:'IBM Plex Mono', monospace; }

  /* faint scanline + grid texture over whole page */
  body::before{
    content:"";
    position:fixed; inset:0;
    pointer-events:none;
    background-image:
      repeating-linear-gradient(0deg, rgba(255,255,255,0.018) 0px, rgba(255,255,255,0.018) 1px, transparent 1px, transparent 3px);
    z-index:9999;
    mix-blend-mode:overlay;
  }

  a{color:inherit;}
  img{max-width:100%; display:block;}

  .wrap{
    max-width:1180px;
    margin:0 auto;
    padding:0 32px;
  }

  /* ---------- HEADER ---------- */
  header{
    position:sticky; top:0; z-index:500;
    background:rgba(12,16,21,0.88);
    backdrop-filter:blur(10px);
    border-bottom:1px solid var(--line);
  }
  .nav-row{
    display:flex; align-items:center; justify-content:space-between;
    height:78px;
  }
  .brand{
    display:flex; align-items:center; gap:12px;
    text-decoration:none;
  }
  .brand-mark{
    width:38px;height:38px;
    border:1.5px solid var(--amber);
    border-radius:50%;
    display:flex;align-items:center;justify-content:center;
    position:relative;
    flex-shrink:0;
  }
  .brand-mark::before{
    content:"";
    width:9px;height:9px;border-radius:50%;
    background:var(--rec);
    box-shadow:0 0 8px 1px rgba(255,59,59,0.7);
    animation: blink 2.4s ease-in-out infinite;
  }
  @keyframes blink{ 0%,100%{opacity:1;} 50%{opacity:.35;} }
  .brand-text{ line-height:1.05; }
  .brand-text strong{
    display:block;
    font-weight:800; font-size:16.5px; letter-spacing:0.01em;
  }
  .brand-text span{
    display:block;
    font-family:'IBM Plex Mono',monospace;
    font-size:10.5px; letter-spacing:0.14em; text-transform:uppercase;
    color:var(--amber);
    margin-top:2px;
  }
  nav.links{
    display:flex; gap:36px;
    font-size:14px; font-weight:600;
  }
  nav.links a{
    text-decoration:none;
    color:var(--fog);
    position:relative;
    padding:6px 0;
    transition:color .2s ease;
  }
  nav.links a:hover{ color:var(--paper); }
  .nav-cta{
    display:flex; align-items:center; gap:18px;
  }
  .call-btn{
    text-decoration:none;
    background:var(--amber);
    color:#1a1004;
    font-weight:700; font-size:13.5px;
    padding:11px 20px;
    border-radius:var(--radius);
    letter-spacing:0.02em;
    transition: filter .2s ease, transform .2s ease;
  }
  .call-btn:hover{ filter:brightness(1.08); transform:translateY(-1px); }
  .menu-toggle{ display:none; }

  /* ---------- HERO ---------- */
  .hero{
    position:relative;
    padding:96px 0 70px;
    overflow:hidden;
    border-bottom:1px solid var(--line);
  }
  .hero::after{
    content:"";
    position:absolute; inset:0;
    background:
      radial-gradient(ellipse 700px 420px at 78% 18%, rgba(255,138,31,0.10), transparent 60%),
      radial-gradient(ellipse 500px 500px at 5% 95%, rgba(52,211,153,0.06), transparent 60%);
    pointer-events:none;
  }
  .hero-grid{
    display:grid;
    grid-template-columns: 1.05fr 0.95fr;
    gap:60px;
    align-items:center;
    position:relative;
  }
  .eyebrow{
    display:inline-flex; align-items:center; gap:8px;
    font-family:'IBM Plex Mono',monospace;
    font-size:11.5px; letter-spacing:0.16em; text-transform:uppercase;
    color:var(--status);
    border:1px solid rgba(52,211,153,0.35);
    background:rgba(52,211,153,0.06);
    padding:6px 12px;
    border-radius:20px;
    margin-bottom:26px;
  }
  .eyebrow .dot{
    width:6px;height:6px;border-radius:50%;background:var(--status);
    box-shadow:0 0 6px 1px rgba(52,211,153,0.8);
  }
  h1{
    font-family:'Archivo Expanded', sans-serif;
    font-weight:800;
    font-size:clamp(34px, 4.4vw, 54px);
    line-height:1.05;
    letter-spacing:-0.01em;
    margin:0 0 22px;
  }
  h1 .accent{ color:var(--amber); }
  .hero p.lead{
    font-size:17px;
    line-height:1.65;
    color:#bcc6cf;
    max-width:480px;
    margin:0 0 34px;
  }
  .hero-actions{
    display:flex; align-items:center; gap:18px; flex-wrap:wrap;
    margin-bottom:42px;
  }
  .btn-primary{
    text-decoration:none;
    background:var(--amber);
    color:#1a1004;
    font-weight:700; font-size:14.5px;
    padding:15px 26px;
    border-radius:var(--radius);
    display:inline-flex; align-items:center; gap:10px;
    transition: filter .2s ease, transform .2s ease;
  }
  .btn-primary:hover{ filter:brightness(1.08); transform:translateY(-1px); }
  .btn-ghost{
    text-decoration:none;
    color:var(--paper);
    font-weight:600; font-size:14.5px;
    padding:15px 22px;
    border:1px solid var(--line-strong);
    border-radius:var(--radius);
    transition: border-color .2s ease, background .2s ease;
  }
  .btn-ghost:hover{ border-color:var(--paper); background:rgba(255,255,255,0.03); }

  .hero-stats{
    display:flex; gap:0;
    border-top:1px solid var(--line);
    max-width:480px;
  }
  .hero-stats div{
    flex:1;
    padding:18px 18px 0 0;
  }
  .hero-stats strong{
    display:block;
    font-family:'Archivo Expanded',sans-serif;
    font-size:25px; font-weight:800; color:var(--paper);
  }
  .hero-stats span{
    display:block; margin-top:4px;
    font-size:11.5px; color:var(--fog);
    font-family:'IBM Plex Mono',monospace;
    letter-spacing:0.04em;
  }

  /* signature element: monitor wall */
  .monitor-wall{
    position:relative;
    background:var(--panel);
    border:1px solid var(--line-strong);
    border-radius:6px;
    padding:14px;
  }
  .monitor-wall-header{
    display:flex; align-items:center; justify-content:space-between;
    padding:2px 6px 14px;
    font-family:'IBM Plex Mono',monospace;
    font-size:10.5px; letter-spacing:0.1em; color:var(--fog);
    text-transform:uppercase;
  }
  .monitor-wall-header .live{
    display:flex;align-items:center;gap:6px; color:var(--rec);
  }
  .monitor-wall-header .live .dot{
    width:6px;height:6px;border-radius:50%;background:var(--rec);
    animation: blink 1.6s ease-in-out infinite;
  }
  .feed-grid{
    display:grid;
    grid-template-columns: repeat(2, 1fr);
    gap:10px;
  }
  .feed{
    position:relative;
    aspect-ratio: 4 / 3;
    border-radius:3px;
    overflow:hidden;
    border:1px solid var(--line);
    background:#0a0d11;
  }
  .feed img{ width:100%; height:100%; object-fit:cover; filter:saturate(0.85) contrast(1.05) brightness(0.9); }
  .feed .scan{
    position:absolute; inset:0;
    background:linear-gradient(180deg, transparent 0%, rgba(0,0,0,0.55) 100%);
  }
  .feed .tag{
    position:absolute; top:6px; left:7px;
    font-family:'IBM Plex Mono',monospace;
    font-size:9px; letter-spacing:0.05em;
    color:#cfe0ee;
    background:rgba(0,0,0,0.45);
    padding:2px 5px;
    border-radius:2px;
  }
  .feed .rec{
    position:absolute; top:6px; right:7px;
    display:flex; align-items:center; gap:4px;
    font-family:'IBM Plex Mono',monospace;
    font-size:9px; color:var(--rec);
  }
  .feed .rec .dot{
    width:5px;height:5px;border-radius:50%;background:var(--rec);
    animation: blink 1.4s ease-in-out infinite;
  }
  .feed .corner{
    position:absolute; width:12px; height:12px;
    border-color: rgba(255,255,255,0.55);
  }
  .feed .corner.tl{ top:5px; left:5px; border-top:1.5px solid; border-left:1.5px solid; }
  .feed .corner.br{ bottom:5px; right:5px; border-bottom:1.5px solid; border-right:1.5px solid; }

  /* ---------- SECTION GENERIC ---------- */
  section{ padding:88px 0; border-bottom:1px solid var(--line); }
  .section-head{ max-width:620px; margin-bottom:54px; }
  .kicker{
    font-family:'IBM Plex Mono',monospace;
    font-size:11.5px; letter-spacing:0.18em; text-transform:uppercase;
    color:var(--amber);
    margin-bottom:14px;
    display:flex; align-items:center; gap:10px;
  }
  .kicker::before{
    content:""; width:24px; height:1px; background:var(--amber);
  }
  h2{
    font-family:'Archivo Expanded', sans-serif;
    font-weight:800;
    font-size:clamp(26px, 3vw, 36px);
    line-height:1.15;
    letter-spacing:-0.01em;
    margin:0 0 16px;
  }
  .section-head p{
    color:var(--fog); font-size:15.5px; line-height:1.65; margin:0;
  }

  /* ABOUT */
  .about-grid{
    display:grid;
    grid-template-columns: 1fr 1fr;
    gap:64px;
    align-items:start;
  }
  .about-grid p{
    color:#bcc6cf; line-height:1.75; font-size:15.5px; margin:0 0 18px;
  }
  .badge-row{
    display:flex; flex-wrap:wrap; gap:10px;
    margin-top:28px;
  }
  .badge-row span{
    font-family:'IBM Plex Mono',monospace;
    font-size:11.5px; letter-spacing:0.04em;
    border:1px solid var(--line-strong);
    color:var(--fog);
    padding:8px 14px;
    border-radius:20px;
  }
  .why-list{ list-style:none; margin:0; padding:0; display:flex; flex-direction:column; gap:0; }
  .why-list li{
    display:flex; gap:16px; align-items:flex-start;
    padding:18px 0;
    border-top:1px solid var(--line);
    font-size:14.5px;
    color:var(--paper);
  }
  .why-list li:last-child{ border-bottom:1px solid var(--line); }
  .why-list .check{
    flex-shrink:0;
    width:22px;height:22px;
    border-radius:50%;
    border:1px solid var(--status);
    color:var(--status);
    display:flex; align-items:center; justify-content:center;
    font-size:12px;
    margin-top:1px;
  }

  /* SERVICES */
  .services-grid{
    display:grid;
    grid-template-columns: repeat(3, 1fr);
    gap:1px;
    background:var(--line);
    border:1px solid var(--line);
  }
  .service-card{
    background:var(--ink);
    padding:32px 28px;
    transition: background .25s ease;
  }
  .service-card:hover{ background:var(--panel); }
  .service-num{
    font-family:'IBM Plex Mono',monospace;
    font-size:11px; color:var(--amber); letter-spacing:0.08em;
    margin-bottom:18px; display:block;
  }
  .service-card h3{
    font-size:17px; font-weight:700; margin:0 0 10px;
    font-family:'Archivo',sans-serif;
  }
  .service-card p{
    font-size:13.5px; color:var(--fog); line-height:1.6; margin:0;
  }

  /* BRANDS */
  .brands-row{
    display:flex; gap:1px;
    background:var(--line);
    border:1px solid var(--line);
  }
  .brand-card{
    flex:1;
    background:var(--panel);
    padding:46px 36px;
    text-align:center;
  }
  .brand-card .blabel{
    font-family:'IBM Plex Mono',monospace;
    font-size:10.5px; letter-spacing:0.16em; text-transform:uppercase;
    color:var(--fog); margin-bottom:16px;
  }
  .brand-card .bname{
    font-family:'Archivo Expanded',sans-serif;
    font-size:30px; font-weight:800;
    letter-spacing:-0.01em;
  }
  .brand-card .btagline{
    margin-top:10px; font-size:13px; color:var(--fog);
  }

  /* AMC / CTA STRIP */
  .cta-strip{
    border-bottom:1px solid var(--line);
    padding:0;
  }
  .cta-strip-inner{
    display:flex; align-items:center; justify-content:space-between;
    gap:40px; flex-wrap:wrap;
    padding:56px 0;
  }
  .cta-strip h3{
    font-family:'Archivo Expanded',sans-serif;
    font-size:26px; font-weight:800; margin:0 0 10px;
    max-width:480px;
  }
  .cta-strip p{ color:var(--fog); margin:0; max-width:440px; font-size:14.5px; line-height:1.6;}

  /* CONTACT */
  .contact-grid{
    display:grid;
    grid-template-columns: 1fr 1fr;
    gap:64px;
  }
  .contact-card{
    background:var(--panel);
    border:1px solid var(--line);
    border-radius:6px;
    padding:38px;
  }
  .contact-line{
    display:flex; gap:16px; align-items:flex-start;
    padding:20px 0;
    border-top:1px solid var(--line);
  }
  .contact-line:first-child{ border-top:none; padding-top:0; }
  .contact-line .ic{
    width:38px;height:38px; flex-shrink:0;
    border:1px solid var(--line-strong);
    border-radius:50%;
    display:flex; align-items:center; justify-content:center;
    color:var(--amber);
  }
  .contact-line strong{ display:block; font-size:14.5px; margin-bottom:4px; }
  .contact-line a, .contact-line span.val{
    color:var(--fog); font-size:14px; text-decoration:none;
    font-family:'IBM Plex Mono',monospace;
  }
  .contact-line a:hover{ color:var(--paper); }

  .quote-box{
    background:var(--panel-2);
    border:1px solid var(--line);
    border-radius:6px;
    padding:38px;
    display:flex; flex-direction:column;
    justify-content:center;
  }
  .quote-box .tag{
    font-family:'IBM Plex Mono',monospace;
    font-size:11px; letter-spacing:0.14em; text-transform:uppercase;
    color:var(--status); margin-bottom:18px;
  }
  .quote-box h4{
    font-family:'Archivo Expanded',sans-serif;
    font-size:22px; font-weight:800; margin:0 0 14px; line-height:1.25;
  }
  .quote-box p{ color:var(--fog); font-size:14px; line-height:1.6; margin:0 0 26px; }

  /* FOOTER */
  footer{ padding:40px 0; }
  .footer-row{
    display:flex; align-items:center; justify-content:space-between;
    flex-wrap:wrap; gap:18px;
  }
  .footer-row .brand-text strong{ font-size:14.5px; }
  .footer-links{
    display:flex; gap:24px; font-size:13px; color:var(--fog);
  }
  .footer-links a{ text-decoration:none; color:var(--fog); }
  .footer-links a:hover{ color:var(--paper); }
  .footer-fine{
    font-family:'IBM Plex Mono',monospace;
    font-size:11px; color:#5b6772;
  }

  @media (max-width:980px){
    nav.links{ display:none; }
    .hero-grid{ grid-template-columns:1fr; gap:48px; }
    .about-grid{ grid-template-columns:1fr; gap:36px; }
    .services-grid{ grid-template-columns:1fr 1fr; }
    .brands-row{ flex-direction:column; }
    .contact-grid{ grid-template-columns:1fr; gap:32px; }
  }
  @media (max-width:600px){
    .wrap{ padding:0 20px; }
    .services-grid{ grid-template-columns:1fr; }
    .hero{ padding:64px 0 50px; }
    .hero-stats{ flex-wrap:wrap; }
    .hero-stats div{ flex:1 1 45%; padding-bottom:14px; }
    .cta-strip-inner{ padding:42px 0; }
  }
</style>
</head>
<body>

<header>
  <div class="wrap nav-row">
    <a href="#top" class="brand">
      <div class="brand-mark"></div>
      <div class="brand-text">
        <strong>DPS Security Solutions</strong>
        <span>Protecting What Matters Most</span>
      </div>
    </a>
    <nav class="links">
      <a href="#about">About Us</a>
      <a href="#services">Services</a>
      <a href="#brands">Brands</a>
      <a href="#contact">Contact</a>
    </nav>
    <div class="nav-cta">
      <a class="call-btn" href="tel:7701867115">Call Now</a>
    </div>
  </div>
</header>

<main id="top">

  <!-- HERO -->
  <section class="hero" style="border-bottom:1px solid var(--line); padding-bottom:0;">
    <div class="wrap hero-grid">
      <div>
        <div class="eyebrow"><span class="dot"></span>System Status: Monitoring Active</div>
        <h1>Professional CCTV Installation &amp; <span class="accent">Security Services</span></h1>
        <p class="lead">Secure your home, office, shop, or business with advanced surveillance systems installed by experienced professionals. Round-the-clock visibility, built right.</p>
        <div class="hero-actions">
          <a class="btn-primary" href="tel:7701867115">📞 Call Now: 7701867115</a>
          <a class="btn-ghost" href="#services">View Services</a>
        </div>
        <div class="hero-stats">
          <div>
            <strong>3–4+</strong>
            <span>Years Experience</span>
          </div>
          <div>
            <strong>2</strong>
            <span>Trusted Brands</span>
          </div>
          <div>
            <strong>24/7</strong>
            <span>Remote Monitoring</span>
          </div>
        </div>
      </div>

      <div class="monitor-wall">
        <div class="monitor-wall-header">
          <span>CAM ARRAY / SECTOR 04</span>
          <span class="live"><span class="dot"></span>LIVE</span>
        </div>
        <div class="feed-grid">
          <div class="feed">
            <img src="https://images.unsplash.com/photo-1557597774-9d273605dfa9?w=400&q=60" alt="Surveillance camera feed">
            <div class="scan"></div>
            <div class="corner tl"></div><div class="corner br"></div>
            <span class="tag">CAM-01 / ENTRANCE</span>
            <span class="rec"><span class="dot"></span>REC</span>
          </div>
          <div class="feed">
            <img src="https://images.unsplash.com/photo-1557597774-9d273605dfa9?w=400&q=60" alt="Surveillance camera feed">
            <div class="scan"></div>
            <div class="corner tl"></div><div class="corner br"></div>
            <span class="tag">CAM-02 / LOBBY</span>
            <span class="rec"><span class="dot"></span>REC</span>
          </div>
          <div class="feed">
            <img src="https://images.unsplash.com/photo-1574717024653-61fd2cf4d44d?w=400&q=60" alt="Security control room">
            <div class="scan"></div>
            <div class="corner tl"></div><div class="corner br"></div>
            <span class="tag">CAM-03 / YARD</span>
            <span class="rec"><span class="dot"></span>REC</span>
          </div>
          <div class="feed">
            <img src="https://images.unsplash.com/photo-1517649763962-0c623066013b?w=400&q=60" alt="Warehouse interior">
            <div class="scan"></div>
            <div class="corner tl"></div><div class="corner br"></div>
            <span class="tag">CAM-04 / STOCK</span>
            <span class="rec"><span class="dot"></span>REC</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <div class="wrap about-grid">
      <div>
        <div class="kicker">About Us</div>
        <h2>A trusted name in surveillance, built on hands-on expertise.</h2>
        <p>DPS Security Solutions is a trusted CCTV and surveillance service provider with over 3–4 years of experience delivering reliable security solutions. We specialize in professional installation, maintenance, repair, and support services for residential, commercial, and industrial clients.</p>
        <p>Our goal is simple: high-quality surveillance systems that ensure safety, security, and peace of mind — for your home, your shop, and your business.</p>
        <div class="badge-row">
          <span>Residential</span>
          <span>Commercial</span>
          <span>Industrial</span>
          <span>AMC Contracts</span>
        </div>
      </div>
      <div>
        <div class="kicker">Why Choose Us</div>
        <ul class="why-list">
          <li><span class="check">✓</span>3–4+ Years of Hands-On Experience</li>
          <li><span class="check">✓</span>Professional Installation Services</li>
          <li><span class="check">✓</span>Technical Expertise Across Brands</li>
          <li><span class="check">✓</span>Affordable, Transparent Pricing</li>
          <li><span class="check">✓</span>Reliable Customer Support</li>
          <li><span class="check">✓</span>Quality Equipment and Solutions</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- SERVICES -->
  <section id="services">
    <div class="wrap">
      <div class="section-head">
        <div class="kicker">Services We Offer</div>
        <h2>Full coverage, from first camera to ongoing maintenance.</h2>
        <p>Whatever the space — home, office, shop, or warehouse — we install, maintain, and support the system that fits it.</p>
      </div>
    </div>
    <div class="wrap" style="padding:0;">
      <div class="services-grid">
        <div class="service-card"><span class="service-num">01</span><h3>CCTV Camera Installation</h3><p>Complete setup and placement planning for clear, reliable coverage of every entry point.</p></div>
        <div class="service-card"><span class="service-num">02</span><h3>CCTV Repair &amp; Maintenance</h3><p>Fast diagnosis and repair of faulty cameras, cabling, and recording equipment.</p></div>
        <div class="service-card"><span class="service-num">03</span><h3>IP Camera Setup</h3><p>Network camera configuration for sharper footage and smarter remote access.</p></div>
        <div class="service-card"><span class="service-num">04</span><h3>DVR &amp; NVR Installation</h3><p>Recorder setup and storage configuration tailored to your footage retention needs.</p></div>
        <div class="service-card"><span class="service-num">05</span><h3>Wireless Camera Installation</h3><p>Clean, cable-free installs for spaces where flexibility matters most.</p></div>
        <div class="service-card"><span class="service-num">06</span><h3>Remote Mobile Monitoring</h3><p>View your property live from your phone, anywhere, anytime.</p></div>
        <div class="service-card"><span class="service-num">07</span><h3>Home Security Solutions</h3><p>Residential systems designed around how your household actually moves.</p></div>
        <div class="service-card"><span class="service-num">08</span><h3>Office Surveillance Systems</h3><p>Discreet, professional-grade coverage for workplaces of any size.</p></div>
        <div class="service-card"><span class="service-num">09</span><h3>Shop &amp; Warehouse Security</h3><p>Wide-coverage systems built for stock rooms, counters, and loading areas.</p></div>
        <div class="service-card"><span class="service-num">10</span><h3>Annual Maintenance Contracts</h3><p>Scheduled servicing so your system stays reliable year-round.</p></div>
        <div class="service-card"><span class="service-num">11</span><h3>Camera Upgrades &amp; Replacement</h3><p>Move up to newer equipment without redoing your entire setup.</p></div>
        <div class="service-card" style="display:flex; flex-direction:column; justify-content:center; background:var(--panel-2);">
          <h3 style="margin-bottom:14px;">Not sure what you need?</h3>
          <p style="margin-bottom:18px;">Tell us about the space and we'll recommend the right system.</p>
          <a href="tel:7701867115" class="btn-ghost" style="display:inline-block; width:fit-content;">Talk to Us →</a>
        </div>
      </div>
    </div>
  </section>

  <!-- BRANDS -->
  <section id="brands">
    <div class="wrap">
      <div class="section-head">
        <div class="kicker">Brands We Work With</div>
        <h2>Equipment we trust enough to put our name on.</h2>
      </div>
    </div>
    <div class="wrap" style="padding:0;">
      <div class="brands-row">
        <div class="brand-card">
          <div class="blabel">Brand Partner</div>
          <div class="bname">HIKVISION</div>
          <div class="btagline">Industry-leading CCTV &amp; IP camera systems</div>
        </div>
        <div class="brand-card">
          <div class="blabel">Brand Partner</div>
          <div class="bname">CP PLUS</div>
          <div class="btagline">Reliable surveillance hardware for every budget</div>
        </div>
      </div>
    </div>
  </section>

  <!-- CTA STRIP -->
  <section class="cta-strip">
    <div class="wrap cta-strip-inner">
      <div>
        <h3>Already have a system? Keep it running with an AMC.</h3>
        <p>Our Annual Maintenance Contracts cover scheduled checkups, repairs, and priority support — so small issues never become blind spots.</p>
      </div>
      <a class="btn-primary" href="tel:7701867115">Get an AMC Quote</a>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <div class="wrap">
      <div class="section-head">
        <div class="kicker">Contact</div>
        <h2>Let's secure your space.</h2>
        <p>Reach out for a site visit, a quote, or just to ask what setup makes sense for you.</p>
      </div>
      <div class="contact-grid">
        <div class="contact-card">
          <div class="contact-line">
            <div class="ic">☎</div>
            <div>
              <strong>Phone</strong>
              <a href="tel:7701867115">7701867115</a>
            </div>
          </div>
          <div class="contact-line">
            <div class="ic">✉</div>
            <div>
              <strong>Email</strong>
              <a href="mailto:Ujjwal6247@gmail.com">Ujjwal6247@gmail.com</a>
            </div>
          </div>
          <div class="contact-line">
            <div class="ic">⌖</div>
            <div>
              <strong>Address</strong>
              <span class="val">33 Feet Road</span>
            </div>
          </div>
        </div>
        <div class="quote-box">
          <div class="tag">Response Time · Same Day</div>
          <h4>Get a free site assessment</h4>
          <p>Call or email us with your space details — home, office, shop, or warehouse — and we'll get back to you with a tailored recommendation and quote.</p>
          <a class="btn-primary" href="tel:7701867115" style="align-self:flex-start;">📞 Call 7701867115</a>
        </div>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="wrap footer-row">
    <div class="brand">
      <div class="brand-mark"></div>
      <div class="brand-text">
        <strong>DPS Security Solutions</strong>
      </div>
    </div>
    <div class="footer-links">
      <a href="#about">About Us</a>
      <a href="#services">Services</a>
      <a href="#brands">Brands</a>
      <a href="#contact">Contact</a>
    </div>
    <div class="footer-fine">© 2026 DPS Security Solutions. All rights reserved.</div>
  </div>
</footer>

</body>
</html>
