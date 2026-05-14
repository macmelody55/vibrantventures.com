# vibrantventures.com
Vibrant Ventures Elevate your Business Vision
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vibrant Ventures | Business Consultancy</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --gold: #C9A84C;
    --gold-light: #E8C96B;
    --gold-pale: #F5E9C8;
    --forest: #1A2E1E;
    --forest-mid: #243828;
    --forest-light: #2F4A36;
    --cream: #FAF6EF;
    --warm-white: #FFFDF8;
    --text-dark: #1A1A1A;
    --text-mid: #4A4A4A;
    --text-light: #888;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--text-dark);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; width: 100%; z-index: 100;
    background: rgba(26,46,30,0.97);
    backdrop-filter: blur(12px);
    padding: 18px 60px;
    display: flex; align-items: center; justify-content: space-between;
    border-bottom: 1px solid rgba(201,168,76,0.2);
  }
  .logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem; font-weight: 700;
    color: var(--gold);
    letter-spacing: 0.02em;
  }
  .logo span { color: var(--warm-white); font-style: italic; }
  nav ul { list-style: none; display: flex; gap: 40px; }
  nav ul a {
    color: rgba(255,255,255,0.75);
    text-decoration: none; font-size: 0.85rem;
    letter-spacing: 0.1em; text-transform: uppercase; font-weight: 500;
    transition: color 0.3s;
  }
  nav ul a:hover { color: var(--gold); }
  .nav-cta {
    background: var(--gold); color: var(--forest) !important;
    padding: 10px 24px; border-radius: 2px;
    font-weight: 600 !important; letter-spacing: 0.05em !important;
    transition: background 0.3s !important;
  }
  .nav-cta:hover { background: var(--gold-light) !important; color: var(--forest) !important; }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    background: var(--forest);
    display: grid; grid-template-columns: 1fr 1fr;
    position: relative; overflow: hidden;
    padding-top: 80px;
  }
  .hero::before {
    content: '';
    position: absolute; inset: 0;
    background: radial-gradient(ellipse at 70% 50%, rgba(201,168,76,0.08) 0%, transparent 60%);
    pointer-events: none;
  }
  /* Decorative diagonal stripe */
  .hero::after {
    content: '';
    position: absolute; right: 48%; top: 0; bottom: 0; width: 2px;
    background: linear-gradient(to bottom, transparent, var(--gold), transparent);
    opacity: 0.4;
  }
  .hero-left {
    display: flex; flex-direction: column; justify-content: center;
    padding: 80px 60px 80px 80px;
    position: relative; z-index: 2;
    animation: fadeUp 1s ease both;
  }
  .hero-eyebrow {
    font-size: 0.75rem; letter-spacing: 0.25em; text-transform: uppercase;
    color: var(--gold); font-weight: 600; margin-bottom: 28px;
    display: flex; align-items: center; gap: 14px;
  }
  .hero-eyebrow::before {
    content: ''; display: block; width: 40px; height: 1px; background: var(--gold);
  }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.8rem, 5vw, 4.5rem);
    font-weight: 900; line-height: 1.08;
    color: var(--warm-white);
    margin-bottom: 30px;
  }
  .hero h1 em {
    font-style: italic; color: var(--gold);
    display: block;
  }
  .hero-desc {
    font-size: 1rem; line-height: 1.8;
    color: rgba(255,255,255,0.6);
    max-width: 420px; margin-bottom: 48px;
  }
  .hero-btns { display: flex; gap: 16px; flex-wrap: wrap; }
  .btn-primary {
    background: var(--gold); color: var(--forest);
    padding: 15px 36px; border-radius: 2px;
    font-weight: 600; font-size: 0.9rem; text-decoration: none;
    letter-spacing: 0.05em; text-transform: uppercase;
    transition: background 0.3s, transform 0.2s;
    display: inline-block;
  }
  .btn-primary:hover { background: var(--gold-light); transform: translateY(-2px); }
  .btn-outline {
    border: 1px solid rgba(201,168,76,0.5); color: var(--gold);
    padding: 15px 36px; border-radius: 2px;
    font-weight: 500; font-size: 0.9rem; text-decoration: none;
    letter-spacing: 0.05em; text-transform: uppercase;
    transition: all 0.3s; display: inline-block;
  }
  .btn-outline:hover { border-color: var(--gold); background: rgba(201,168,76,0.08); }

  .hero-right {
    display: flex; flex-direction: column; justify-content: center;
    padding: 80px 80px 80px 60px;
    position: relative; z-index: 2;
    animation: fadeUp 1s 0.2s ease both;
  }
  .stat-grid {
    display: grid; grid-template-columns: 1fr 1fr; gap: 2px;
    margin-bottom: 48px;
  }
  .stat-card {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(201,168,76,0.12);
    padding: 32px 28px;
    transition: background 0.3s;
  }
  .stat-card:hover { background: rgba(201,168,76,0.06); }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2.6rem; font-weight: 900;
    color: var(--gold); line-height: 1;
    margin-bottom: 8px;
  }
  .stat-label {
    font-size: 0.78rem; letter-spacing: 0.1em;
    text-transform: uppercase; color: rgba(255,255,255,0.45);
  }
  .hero-contact-card {
    background: rgba(201,168,76,0.08);
    border: 1px solid rgba(201,168,76,0.25);
    border-radius: 2px; padding: 28px 32px;
  }
  .contact-row {
    display: flex; align-items: flex-start; gap: 14px;
    color: rgba(255,255,255,0.7); font-size: 0.88rem;
    line-height: 1.6;
  }
  .contact-row + .contact-row { margin-top: 16px; padding-top: 16px; border-top: 1px solid rgba(201,168,76,0.12); }
  .contact-icon {
    width: 32px; height: 32px; border-radius: 50%;
    background: rgba(201,168,76,0.15);
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0; color: var(--gold); font-size: 0.85rem;
  }

  /* ── SECTION BASE ── */
  section { padding: 100px 80px; }
  .section-label {
    font-size: 0.72rem; letter-spacing: 0.25em; text-transform: uppercase;
    color: var(--gold); font-weight: 600; margin-bottom: 16px;
    display: flex; align-items: center; gap: 12px;
  }
  .section-label::before { content: ''; display: block; width: 30px; height: 1px; background: var(--gold); }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 3.5vw, 3rem);
    font-weight: 900; line-height: 1.15;
    margin-bottom: 20px;
  }

  /* ── ABOUT ── */
  .about { background: var(--warm-white); }
  .about-inner { max-width: 1200px; margin: 0 auto; display: grid; grid-template-columns: 1fr 1.2fr; gap: 100px; align-items: center; }
  .about-visual {
    position: relative;
  }
  .about-img-box {
    background: var(--forest);
    aspect-ratio: 4/5;
    display: flex; align-items: center; justify-content: center;
    font-family: 'Playfair Display', serif;
    font-size: 6rem; color: var(--gold);
    opacity: 0.7;
    position: relative;
    overflow: hidden;
  }
  .about-img-box::before {
    content: '';
    position: absolute; inset: 0;
    background: linear-gradient(135deg, rgba(201,168,76,0.1), transparent 60%);
  }
  .about-badge {
    position: absolute; bottom: -20px; right: -20px;
    background: var(--gold); color: var(--forest);
    padding: 24px 28px; font-family: 'Playfair Display', serif;
    text-align: center;
  }
  .about-badge strong { display: block; font-size: 2.2rem; font-weight: 900; line-height: 1; }
  .about-badge span { font-size: 0.75rem; font-weight: 400; letter-spacing: 0.05em; }
  .about-text .section-title { color: var(--forest); }
  .about-text p { color: var(--text-mid); line-height: 1.85; font-size: 0.95rem; margin-bottom: 20px; }
  .about-pillars { display: flex; gap: 32px; margin-top: 36px; }
  .pillar { flex: 1; border-left: 2px solid var(--gold); padding-left: 16px; }
  .pillar strong { display: block; font-size: 0.85rem; font-weight: 600; color: var(--forest); letter-spacing: 0.03em; margin-bottom: 4px; }
  .pillar span { font-size: 0.78rem; color: var(--text-light); }

  /* ── SERVICES ── */
  .services { background: var(--forest); }
  .services .section-title { color: var(--warm-white); }
  .services-header { max-width: 600px; margin-bottom: 64px; }
  .services-header p { color: rgba(255,255,255,0.55); font-size: 0.95rem; line-height: 1.8; margin-top: 16px; }
  .services-grid {
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 2px;
    max-width: 1200px;
  }
  .service-card {
    background: rgba(255,255,255,0.03);
    border: 1px solid rgba(201,168,76,0.1);
    padding: 44px 36px;
    transition: all 0.3s;
    position: relative; overflow: hidden;
  }
  .service-card::before {
    content: '';
    position: absolute; bottom: 0; left: 0; right: 0; height: 2px;
    background: var(--gold);
    transform: scaleX(0); transform-origin: left;
    transition: transform 0.4s ease;
  }
  .service-card:hover { background: rgba(201,168,76,0.07); }
  .service-card:hover::before { transform: scaleX(1); }
  .service-num {
    font-family: 'Playfair Display', serif;
    font-size: 3rem; font-weight: 900;
    color: rgba(201,168,76,0.15);
    line-height: 1; margin-bottom: 24px;
  }
  .service-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem; font-weight: 700;
    color: var(--warm-white); margin-bottom: 14px;
  }
  .service-card p { font-size: 0.85rem; line-height: 1.75; color: rgba(255,255,255,0.5); }
  .service-tag {
    display: inline-block; margin-top: 24px;
    font-size: 0.7rem; letter-spacing: 0.15em; text-transform: uppercase;
    color: var(--gold); border: 1px solid rgba(201,168,76,0.3);
    padding: 5px 14px; border-radius: 20px;
  }

  /* ── PROCESS ── */
  .process { background: var(--cream); }
  .process-inner { max-width: 1200px; margin: 0 auto; }
  .process .section-title { color: var(--forest); margin-bottom: 64px; }
  .process-steps { display: flex; gap: 0; position: relative; }
  .process-steps::before {
    content: '';
    position: absolute; top: 40px; left: 40px; right: 40px; height: 1px;
    background: linear-gradient(to right, var(--gold), rgba(201,168,76,0.2));
  }
  .step {
    flex: 1; padding: 0 24px; text-align: center;
    position: relative;
  }
  .step-dot {
    width: 80px; height: 80px; border-radius: 50%;
    background: var(--forest); border: 2px solid var(--gold);
    display: flex; align-items: center; justify-content: center;
    margin: 0 auto 28px;
    font-family: 'Playfair Display', serif;
    font-size: 1.6rem; font-weight: 900; color: var(--gold);
    position: relative; z-index: 2;
    transition: all 0.3s;
  }
  .step:hover .step-dot { background: var(--gold); color: var(--forest); transform: scale(1.1); }
  .step h4 { font-family: 'Playfair Display', serif; font-size: 1.05rem; font-weight: 700; color: var(--forest); margin-bottom: 10px; }
  .step p { font-size: 0.82rem; color: var(--text-light); line-height: 1.7; }

  /* ── CTA BAND ── */
  .cta-band {
    background: var(--gold);
    padding: 70px 80px;
    display: flex; align-items: center; justify-content: space-between;
    gap: 40px;
  }
  .cta-band h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3vw, 2.6rem);
    font-weight: 900; color: var(--forest);
    max-width: 500px; line-height: 1.2;
  }
  .btn-dark {
    background: var(--forest); color: var(--warm-white);
    padding: 16px 40px; border-radius: 2px;
    font-weight: 600; font-size: 0.9rem; text-decoration: none;
    letter-spacing: 0.05em; text-transform: uppercase;
    transition: all 0.3s; white-space: nowrap;
    display: inline-block;
  }
  .btn-dark:hover { background: var(--forest-light); transform: translateY(-2px); }

  /* ── CONTACT ── */
  .contact { background: var(--forest-mid); }
  .contact .section-title { color: var(--warm-white); }
  .contact-inner { max-width: 1200px; margin: 0 auto; display: grid; grid-template-columns: 1fr 1.4fr; gap: 80px; }
  .contact-info p { color: rgba(255,255,255,0.55); font-size: 0.92rem; line-height: 1.8; margin: 16px 0 40px; }
  .contact-detail {
    display: flex; align-items: flex-start; gap: 18px;
    margin-bottom: 28px;
  }
  .c-icon {
    width: 44px; height: 44px; border-radius: 50%;
    background: rgba(201,168,76,0.12);
    border: 1px solid rgba(201,168,76,0.25);
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0; color: var(--gold); font-size: 1rem;
  }
  .c-text strong { display: block; color: var(--gold); font-size: 0.75rem; letter-spacing: 0.12em; text-transform: uppercase; margin-bottom: 4px; }
  .c-text span { color: rgba(255,255,255,0.7); font-size: 0.9rem; line-height: 1.5; }

  .contact-form {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(201,168,76,0.15);
    padding: 44px;
  }
  .form-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem; color: var(--warm-white);
    margin-bottom: 32px;
  }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 16px; }
  .form-group { margin-bottom: 16px; }
  .form-group label { display: block; font-size: 0.75rem; letter-spacing: 0.1em; text-transform: uppercase; color: rgba(255,255,255,0.45); margin-bottom: 8px; }
  .form-group input, .form-group textarea, .form-group select {
    width: 100%; background: rgba(255,255,255,0.06);
    border: 1px solid rgba(201,168,76,0.2);
    color: var(--warm-white); padding: 14px 18px;
    font-family: 'DM Sans', sans-serif; font-size: 0.9rem;
    border-radius: 2px; outline: none;
    transition: border-color 0.3s;
    appearance: none;
  }
  .form-group input:focus, .form-group textarea:focus, .form-group select:focus { border-color: var(--gold); }
  .form-group textarea { resize: vertical; min-height: 120px; }
  .form-group select option { background: var(--forest); }
  .form-submit {
    width: 100%; background: var(--gold); color: var(--forest);
    border: none; padding: 16px; cursor: pointer;
    font-family: 'DM Sans', sans-serif; font-weight: 700;
    font-size: 0.9rem; letter-spacing: 0.1em; text-transform: uppercase;
    border-radius: 2px; transition: all 0.3s; margin-top: 8px;
  }
  .form-submit:hover { background: var(--gold-light); transform: translateY(-2px); }

  /* ── FOOTER ── */
  footer {
    background: var(--forest);
    padding: 50px 80px 30px;
    border-top: 1px solid rgba(201,168,76,0.15);
  }
  .footer-inner { max-width: 1200px; margin: 0 auto; }
  .footer-top { display: flex; justify-content: space-between; align-items: flex-start; gap: 60px; margin-bottom: 48px; }
  .footer-brand .logo { font-size: 1.8rem; display: block; margin-bottom: 14px; }
  .footer-brand p { color: rgba(255,255,255,0.4); font-size: 0.82rem; line-height: 1.7; max-width: 260px; }
  .footer-links h5 { color: var(--gold); font-size: 0.72rem; letter-spacing: 0.15em; text-transform: uppercase; margin-bottom: 18px; }
  .footer-links ul { list-style: none; }
  .footer-links ul li { margin-bottom: 10px; }
  .footer-links ul a { color: rgba(255,255,255,0.45); text-decoration: none; font-size: 0.85rem; transition: color 0.3s; }
  .footer-links ul a:hover { color: var(--gold); }
  .footer-bottom {
    border-top: 1px solid rgba(255,255,255,0.06);
    padding-top: 24px; display: flex; justify-content: space-between;
    align-items: center;
  }
  .footer-bottom p { color: rgba(255,255,255,0.25); font-size: 0.78rem; }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* ── SCROLL REVEAL ── */
  .reveal {
    opacity: 0; transform: translateY(24px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.visible { opacity: 1; transform: none; }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    nav { padding: 16px 24px; }
    nav ul { display: none; }
    .hero { grid-template-columns: 1fr; }
    .hero-left { padding: 80px 24px 40px; }
    .hero-right { padding: 20px 24px 60px; }
    section { padding: 70px 24px; }
    .about-inner { grid-template-columns: 1fr; gap: 50px; }
    .services-grid { grid-template-columns: 1fr; }
    .process-steps { flex-direction: column; gap: 32px; }
    .process-steps::before { display: none; }
    .cta-band { flex-direction: column; padding: 50px 24px; }
    .contact-inner { grid-template-columns: 1fr; }
    .contact-form { padding: 28px 20px; }
    .form-row { grid-template-columns: 1fr; }
    .footer-top { flex-direction: column; gap: 32px; }
    footer { padding: 40px 24px 24px; }
    .footer-bottom { flex-direction: column; gap: 10px; text-align: center; }
    .hero::after { display: none; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="logo">Vibrant <span>Ventures</span></div>
  <ul>
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#process">Process</a></li>
    <li><a href="#contact" class="nav-cta">Get Started</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-left">
    <div class="hero-eyebrow">Business Consultancy · Limpopo</div>
    <h1>
      Elevate Your<br>
      <em>Business Vision</em>
    </h1>
    <p class="hero-desc">Strategic consulting that transforms ambitious ideas into sustainable growth. We partner with businesses across South Africa to build ventures that truly thrive.</p>
    <div class="hero-btns">
      <a href="#contact" class="btn-primary">Book a Consultation</a>
      <a href="#services" class="btn-outline">Our Services</a>
    </div>
  </div>
  <div class="hero-right">
    <div class="stat-grid">
      <div class="stat-card">
        <div class="stat-num">10+</div>
        <div class="stat-label">Years Experience</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">200+</div>
        <div class="stat-label">Clients Served</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">95%</div>
        <div class="stat-label">Client Retention</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">R50M+</div>
        <div class="stat-label">Value Unlocked</div>
      </div>
    </div>
    <div class="hero-contact-card">
      <div class="contact-row">
        <div class="contact-icon">📞</div>
        <div>
          <strong style="color:rgba(255,255,255,0.9); font-weight:600">Call Us Anytime</strong>
          <div>+27 64 773 2908</div>
        </div>
      </div>
      <div class="contact-row">
        <div class="contact-icon">📍</div>
        <div>
          306 Ngoatle Street, Bela-Bela<br>
          Limpopo, 0480, South Africa
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section class="about" id="about">
  <div class="about-inner">
    <div class="about-visual reveal">
      <div class="about-img-box">✦</div>
      <div class="about-badge">
        <strong>VV</strong>
        <span>Est. 2015</span>
      </div>
    </div>
    <div class="about-text reveal">
      <div class="section-label">Who We Are</div>
      <h2 class="section-title">Rooted in Limpopo,<br>Built for Growth</h2>
      <p>Vibrant Ventures is a premier business consultancy headquartered in Bela-Bela, Limpopo. We combine deep local knowledge with world-class strategic frameworks to deliver measurable results for entrepreneurs and established enterprises alike.</p>
      <p>Our team of experienced consultants brings passion, precision, and proven methodology to every engagement — helping you navigate complexity and seize opportunity with confidence.</p>
      <div class="about-pillars">
        <div class="pillar">
          <strong>Strategic Clarity</strong>
          <span>Clear direction for every decision</span>
        </div>
        <div class="pillar">
          <strong>Local Insight</strong>
          <span>Deep Limpopo market knowledge</span>
        </div>
        <div class="pillar">
          <strong>Real Results</strong>
          <span>Measurable, sustainable growth</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section class="services" id="services">
  <div style="max-width:1200px; margin:0 auto;">
    <div class="services-header reveal">
      <div class="section-label">What We Offer</div>
      <h2 class="section-title" style="color:var(--warm-white);">Consulting Services<br>That Move the Needle</h2>
      <p>Comprehensive consulting tailored to where your business is today and where you want to be tomorrow.</p>
    </div>
    <div class="services-grid">
      <div class="service-card reveal">
        <div class="service-num">01</div>
        <h3>Business Strategy</h3>
        <p>Develop robust strategies that align your vision with market realities. We craft roadmaps that prioritise growth, resilience, and competitive advantage.</p>
        <span class="service-tag">Planning · Vision</span>
      </div>
      <div class="service-card reveal">
        <div class="service-num">02</div>
        <h3>Financial Advisory</h3>
        <p>From cash flow optimisation to investment structuring, our financial experts help you build a sound foundation and unlock new capital opportunities.</p>
        <span class="service-tag">Finance · Growth</span>
      </div>
      <div class="service-card reveal">
        <div class="service-num">03</div>
        <h3>Market Expansion</h3>
        <p>Identify and enter new markets with confidence. We analyse opportunity landscapes and develop go-to-market strategies built for South African conditions.</p>
        <span class="service-tag">Market · Entry</span>
      </div>
      <div class="service-card reveal">
        <div class="service-num">04</div>
        <h3>Operations Excellence</h3>
        <p>Streamline processes, eliminate waste, and build operational systems that scale. Turn your back-office into a competitive advantage.</p>
        <span class="service-tag">Process · Systems</span>
      </div>
      <div class="service-card reveal">
        <div class="service-num">05</div>
        <h3>Leadership & Talent</h3>
        <p>Build leadership capacity and develop the human capital your business needs to grow. Coaching, culture design, and succession planning included.</p>
        <span class="service-tag">People · Culture</span>
      </div>
      <div class="service-card reveal">
        <div class="service-num">06</div>
        <h3>Digital Transformation</h3>
        <p>Navigate digital change with a clear technology roadmap. From automation to digital marketing, we help you adopt the right tools at the right time.</p>
        <span class="service-tag">Tech · Innovation</span>
      </div>
    </div>
  </div>
</section>

<!-- PROCESS -->
<section class="process" id="process">
  <div class="process-inner">
    <div class="section-label reveal">How We Work</div>
    <h2 class="section-title reveal">Our Proven Process</h2>
    <div class="process-steps">
      <div class="step reveal">
        <div class="step-dot">1</div>
        <h4>Discovery</h4>
        <p>We immerse ourselves in your business — goals, challenges, market position, and culture — to understand the full picture.</p>
      </div>
      <div class="step reveal">
        <div class="step-dot">2</div>
        <h4>Diagnosis</h4>
        <p>Deep analysis of data and dynamics to identify root causes, hidden opportunities, and critical leverage points.</p>
      </div>
      <div class="step reveal">
        <div class="step-dot">3</div>
        <h4>Strategy</h4>
        <p>Co-create a focused, actionable strategy with clear milestones, priorities, and resource allocation.</p>
      </div>
      <div class="step reveal">
        <div class="step-dot">4</div>
        <h4>Execution</h4>
        <p>Hands-on support to implement the plan — steering through obstacles and adapting as conditions evolve.</p>
      </div>
      <div class="step reveal">
        <div class="step-dot">5</div>
        <h4>Growth</h4>
        <p>Measure outcomes, embed new capabilities, and build momentum for sustained, long-term performance.</p>
      </div>
    </div>
  </div>
</section>

<!-- CTA BAND -->
<div class="cta-band">
  <h2>Ready to build something <em style="font-style:italic">vibrant?</em></h2>
  <a href="#contact" class="btn-dark">Start the Conversation →</a>
</div>

<!-- CONTACT -->
<section class="contact" id="contact">
  <div class="contact-inner">
    <div class="contact-info reveal">
      <div class="section-label">Get In Touch</div>
      <h2 class="section-title">Let's Build Your<br>Next Chapter</h2>
      <p>Whether you're launching a new venture or scaling an existing business, we're ready to help. Reach out and let's explore what's possible together.</p>
      <div class="contact-detail">
        <div class="c-icon">📞</div>
        <div class="c-text">
          <strong>Phone</strong>
          <span>+27 64 773 2908</span>
        </div>
      </div>
      <div class="contact-detail">
        <div class="c-icon">📍</div>
        <div class="c-text">
          <strong>Office Address</strong>
          <span>306 Ngoatle Street, Bela-Bela<br>Limpopo, 0480<br>South Africa</span>
        </div>
      </div>
      <div class="contact-detail">
        <div class="c-icon">🕒</div>
        <div class="c-text">
          <strong>Business Hours</strong>
          <span>Monday – Friday: 08:00 – 17:00<br>Saturday: 09:00 – 13:00</span>
        </div>
      </div>
    </div>

    <div class="contact-form reveal">
      <div class="form-title">Send Us a Message</div>
      <div class="form-row">
        <div class="form-group">
          <label>First Name</label>
          <input type="text" placeholder="Your first name">
        </div>
        <div class="form-group">
          <label>Last Name</label>
          <input type="text" placeholder="Your last name">
        </div>
      </div>
      <div class="form-row">
        <div class="form-group">
          <label>Email</label>
          <input type="email" placeholder="your@email.com">
        </div>
        <div class="form-group">
          <label>Phone</label>
          <input type="tel" placeholder="+27 xxx xxx xxxx">
        </div>
      </div>
      <div class="form-group">
        <label>Service Interested In</label>
        <select>
          <option value="" disabled selected>Select a service...</option>
          <option>Business Strategy</option>
          <option>Financial Advisory</option>
          <option>Market Expansion</option>
          <option>Operations Excellence</option>
          <option>Leadership & Talent</option>
          <option>Digital Transformation</option>
          <option>General Inquiry</option>
        </select>
      </div>
      <div class="form-group">
        <label>Your Message</label>
        <textarea placeholder="Tell us about your business and what you'd like to achieve..."></textarea>
      </div>
      <button class="form-submit" onclick="handleSubmit(this)">Send Message →</button>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-top">
      <div class="footer-brand">
        <div class="logo">Vibrant <span>Ventures</span></div>
        <p>Premier business consultancy serving entrepreneurs and enterprises across Limpopo and South Africa.</p>
      </div>
      <div class="footer-links">
        <h5>Services</h5>
        <ul>
          <li><a href="#services">Business Strategy</a></li>
          <li><a href="#services">Financial Advisory</a></li>
          <li><a href="#services">Market Expansion</a></li>
          <li><a href="#services">Operations</a></li>
        </ul>
      </div>
      <div class="footer-links">
        <h5>Company</h5>
        <ul>
          <li><a href="#about">About Us</a></li>
          <li><a href="#process">Our Process</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </div>
      <div class="footer-links">
        <h5>Contact</h5>
        <ul>
          <li><a href="tel:+27647732908">+27 64 773 2908</a></li>
          <li><a href="#">306 Ngoatle Street</a></li>
          <li><a href="#">Bela-Bela, Limpopo</a></li>
          <li><a href="#">0480, South Africa</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <p>© 2025 Vibrant Ventures (Pty) Ltd. All rights reserved.</p>
      <p>Bela-Bela · Limpopo · South Africa</p>
    </div>
  </div>
</footer>

<script>
  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => entry.target.classList.add('visible'), i * 80);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.12 });
  reveals.forEach(el => observer.observe(el));

  // Form submit
  function handleSubmit(btn) {
    btn.textContent = 'Message Sent! ✓';
    btn.style.background = '#2F4A36';
    btn.style.color = '#C9A84C';
    btn.disabled = true;
    setTimeout(() => {
      btn.textContent = 'Send Message →';
      btn.style.background = '';
      btn.style.color = '';
      btn.disabled = false;
    }, 3000);
  }

  // Nav background on scroll
  const nav = document.querySelector('nav');
  window.addEventListener('scroll', () => {
    nav.style.boxShadow = window.scrollY > 60 ? '0 4px 40px rgba(0,0,0,0.3)' : 'none';
  });
</script>
</body>
</html>
