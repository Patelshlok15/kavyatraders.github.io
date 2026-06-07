# kavyatraders.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kavya Traders – Quality. Trust. Service.</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400;1,500&family=Josefin+Sans:wght@300;400;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --gold: #b8922a;
    --gold-light: #d4aa4a;
    --gold-pale: #f5e9c8;
    --gold-dark: #7a5e12;
    --cream: #faf7f0;
    --cream-dark: #f0ead8;
    --text-dark: #2c2010;
    --text-mid: #5a4520;
    --text-light: #8a7040;
    --white: #ffffff;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Josefin Sans', sans-serif;
    background: var(--cream);
    color: var(--text-dark);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(250,247,240,0.95);
    backdrop-filter: blur(8px);
    border-bottom: 1px solid var(--gold-pale);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%;
    height: 72px;
  }
  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px; font-weight: 600;
    color: var(--gold-dark); letter-spacing: 0.08em;
  }
  .nav-links { display: flex; gap: 40px; list-style: none; }
  .nav-links a {
    font-size: 12px; font-weight: 600; letter-spacing: 0.18em;
    text-transform: uppercase; text-decoration: none;
    color: var(--text-mid); transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--gold); }
  .nav-cta {
    background: var(--gold); color: var(--white);
    border: none; padding: 10px 24px;
    font-family: 'Josefin Sans', sans-serif;
    font-size: 12px; font-weight: 600; letter-spacing: 0.15em;
    text-transform: uppercase; cursor: pointer;
    transition: background 0.2s;
  }
  .nav-cta:hover { background: var(--gold-dark); }
  .nav-hamburger { display: none; flex-direction: column; gap: 5px; cursor: pointer; }
  .nav-hamburger span { width: 24px; height: 2px; background: var(--gold-dark); display: block; }

  /* ── HERO ── */
  #hero {
    min-height: 100vh;
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    text-align: center; padding: 120px 5% 80px;
    position: relative; overflow: hidden;
    background: linear-gradient(160deg, #faf7f0 0%, #f0e8cc 60%, #faf7f0 100%);
  }
  .hero-ornament {
    position: absolute; opacity: 0.08;
    font-family: 'Cormorant Garamond', serif;
    font-size: 380px; font-weight: 600; color: var(--gold);
    line-height: 1; user-select: none; pointer-events: none;
    top: 50%; left: 50%; transform: translate(-50%,-50%);
    letter-spacing: -0.05em;
  }
  .hero-badge {
    display: inline-block;
    border: 1px solid var(--gold);
    color: var(--gold);
    font-size: 11px; font-weight: 600; letter-spacing: 0.3em;
    text-transform: uppercase; padding: 6px 20px;
    margin-bottom: 32px;
    animation: fadeUp 0.8s ease both;
  }
  .hero-logo-circle {
    width: 110px; height: 110px;
    border: 2px solid var(--gold);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    margin: 0 auto 28px;
    position: relative;
    animation: fadeUp 0.8s 0.1s ease both;
  }
  .hero-logo-circle::before {
    content: '';
    position: absolute; inset: 6px;
    border: 1px solid var(--gold-pale);
    border-radius: 50%;
  }
  .hero-logo-initials {
    font-family: 'Cormorant Garamond', serif;
    font-size: 42px; font-weight: 600;
    color: var(--gold-dark); line-height: 1;
  }
  h1 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(56px, 10vw, 100px);
    font-weight: 500; letter-spacing: 0.1em;
    color: var(--gold-dark); line-height: 0.95;
    margin-bottom: 10px;
    animation: fadeUp 0.8s 0.15s ease both;
  }
  .hero-subtitle {
    font-size: 13px; font-weight: 600; letter-spacing: 0.35em;
    text-transform: uppercase; color: var(--text-light);
    margin-bottom: 20px;
    display: flex; align-items: center; gap: 16px;
    justify-content: center;
    animation: fadeUp 0.8s 0.2s ease both;
  }
  .hero-subtitle::before, .hero-subtitle::after {
    content: ''; width: 40px; height: 1px; background: var(--gold-light);
  }
  .hero-tagline {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(20px, 3vw, 28px); font-style: italic;
    color: var(--text-mid); margin-bottom: 40px;
    animation: fadeUp 0.8s 0.25s ease both;
  }
  .hero-desc {
    font-size: 14px; font-weight: 300; letter-spacing: 0.06em;
    color: var(--text-light); max-width: 480px;
    line-height: 1.9; margin-bottom: 48px;
    animation: fadeUp 0.8s 0.3s ease both;
  }
  .hero-actions {
    display: flex; gap: 16px; flex-wrap: wrap; justify-content: center;
    animation: fadeUp 0.8s 0.35s ease both;
  }
  .btn-primary {
    background: var(--gold); color: var(--white);
    border: none; padding: 16px 36px;
    font-family: 'Josefin Sans', sans-serif;
    font-size: 12px; font-weight: 600; letter-spacing: 0.2em;
    text-transform: uppercase; cursor: pointer;
    text-decoration: none; display: inline-block;
    transition: background 0.2s, transform 0.15s;
  }
  .btn-primary:hover { background: var(--gold-dark); transform: translateY(-1px); }
  .btn-outline {
    background: transparent; color: var(--gold-dark);
    border: 1px solid var(--gold); padding: 16px 36px;
    font-family: 'Josefin Sans', sans-serif;
    font-size: 12px; font-weight: 600; letter-spacing: 0.2em;
    text-transform: uppercase; cursor: pointer;
    text-decoration: none; display: inline-block;
    transition: background 0.2s, color 0.2s;
  }
  .btn-outline:hover { background: var(--gold-pale); }

  /* ── DIVIDER ── */
  .divider {
    display: flex; align-items: center; gap: 16px;
    padding: 0 5%; margin: 0 auto; max-width: 1200px;
  }
  .divider-line { flex: 1; height: 1px; background: var(--gold-pale); }
  .divider-icon { color: var(--gold); font-size: 18px; }

  /* ── FEATURES ── */
  #features {
    padding: 100px 5%;
    background: var(--white);
  }
  .section-header { text-align: center; margin-bottom: 64px; }
  .section-label {
    font-size: 11px; font-weight: 600; letter-spacing: 0.35em;
    text-transform: uppercase; color: var(--gold);
    display: block; margin-bottom: 16px;
  }
  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(34px, 5vw, 54px); font-weight: 500;
    color: var(--gold-dark); line-height: 1.15;
  }
  .features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 2px;
    max-width: 1200px; margin: 0 auto;
    border: 1px solid var(--gold-pale);
  }
  .feature-card {
    padding: 48px 36px;
    background: var(--cream);
    border: 1px solid var(--gold-pale);
    transition: background 0.25s;
    text-align: center;
  }
  .feature-card:hover { background: var(--gold-pale); }
  .feature-icon {
    width: 64px; height: 64px;
    border: 1px solid var(--gold);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    margin: 0 auto 24px;
    font-size: 26px; color: var(--gold);
    transition: background 0.25s;
  }
  .feature-card:hover .feature-icon { background: var(--gold); color: var(--white); }
  .feature-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 20px; font-weight: 600;
    color: var(--gold-dark); margin-bottom: 12px;
  }
  .feature-desc { font-size: 13px; font-weight: 300; letter-spacing: 0.04em; color: var(--text-light); line-height: 1.8; }

  /* ── GEM BADGE ── */
  .gem-section {
    background: var(--gold-dark);
    padding: 60px 5%; text-align: center;
  }
  .gem-section p {
    font-size: 11px; letter-spacing: 0.3em; text-transform: uppercase;
    color: rgba(255,255,255,0.6); margin-bottom: 10px;
  }
  .gem-section h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 32px; font-weight: 500; color: var(--gold-pale);
    margin-bottom: 20px;
  }
  .gem-badge-inline {
    display: inline-flex; align-items: center; gap: 12px;
    background: rgba(255,255,255,0.1);
    border: 1px solid rgba(255,255,255,0.2);
    padding: 14px 28px;
    font-size: 13px; letter-spacing: 0.1em; color: var(--gold-pale);
  }
  .gem-badge-inline svg { width: 28px; height: 28px; }

  /* ── ABOUT ── */
  #about { padding: 100px 5%; max-width: 1200px; margin: 0 auto; }
  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 80px; align-items: center; }
  .about-visual {
    position: relative; height: 420px;
    border: 1px solid var(--gold-pale);
  }
  .about-visual-inner {
    position: absolute; inset: 20px;
    background: var(--gold-pale);
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    gap: 16px;
  }
  .about-big-initial {
    font-family: 'Cormorant Garamond', serif;
    font-size: 120px; font-weight: 600;
    color: var(--gold); line-height: 1; opacity: 0.3;
  }
  .about-stats { display: flex; gap: 48px; justify-content: center; }
  .stat { text-align: center; }
  .stat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 48px; font-weight: 600; color: var(--gold-dark);
    display: block; line-height: 1;
  }
  .stat-label { font-size: 11px; letter-spacing: 0.2em; text-transform: uppercase; color: var(--text-light); }
  .about-content { }
  .about-content .section-label { text-align: left; }
  .about-content .section-title { text-align: left; margin-bottom: 28px; }
  .about-text { font-size: 14px; font-weight: 300; line-height: 2; color: var(--text-mid); margin-bottom: 16px; }
  .about-list { list-style: none; margin-top: 24px; display: flex; flex-direction: column; gap: 12px; }
  .about-list li {
    display: flex; align-items: center; gap: 12px;
    font-size: 13px; letter-spacing: 0.05em; color: var(--text-mid);
  }
  .about-list li::before {
    content: ''; width: 20px; height: 1px; background: var(--gold); flex-shrink: 0;
  }

  /* ── CONTACT ── */
  #contact {
    padding: 100px 5%;
    background: var(--cream-dark);
  }
  .contact-inner { max-width: 900px; margin: 0 auto; }
  .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 48px; margin-top: 56px; }
  .contact-card {
    background: var(--white);
    border: 1px solid var(--gold-pale);
    padding: 40px 36px;
    display: flex; flex-direction: column; gap: 8px;
  }
  .contact-label {
    font-size: 10px; letter-spacing: 0.3em; text-transform: uppercase;
    color: var(--gold); margin-bottom: 4px;
  }
  .contact-value {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px; font-weight: 500; color: var(--gold-dark);
    line-height: 1.3;
  }
  .contact-icon { font-size: 28px; color: var(--gold-light); margin-bottom: 12px; }
  .contact-full { grid-column: 1 / -1; }

  /* ── FOOTER ── */
  footer {
    background: var(--text-dark);
    padding: 60px 5% 32px;
    text-align: center;
  }
  .footer-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 32px; font-weight: 600;
    color: var(--gold); letter-spacing: 0.15em;
    margin-bottom: 6px;
  }
  .footer-tagline {
    font-family: 'Cormorant Garamond', serif;
    font-style: italic; font-size: 16px;
    color: var(--gold-pale); opacity: 0.7;
    margin-bottom: 32px;
  }
  .footer-divider { width: 60px; height: 1px; background: var(--gold); margin: 0 auto 24px; }
  .footer-links { display: flex; gap: 32px; justify-content: center; list-style: none; margin-bottom: 32px; }
  .footer-links a {
    font-size: 11px; letter-spacing: 0.2em; text-transform: uppercase;
    color: rgba(255,255,255,0.4); text-decoration: none; transition: color 0.2s;
  }
  .footer-links a:hover { color: var(--gold-light); }
  .footer-copy { font-size: 12px; color: rgba(255,255,255,0.25); letter-spacing: 0.05em; }
  .footer-trust {
    font-family: 'Cormorant Garamond', serif;
    font-style: italic; font-size: 17px;
    color: rgba(255,255,255,0.3); margin-top: 24px;
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .reveal { opacity: 0; transform: translateY(30px); transition: opacity 0.7s ease, transform 0.7s ease; }
  .reveal.visible { opacity: 1; transform: translateY(0); }

  /* ── MOBILE ── */
  @media (max-width: 768px) {
    .nav-links, .nav-cta { display: none; }
    .nav-hamburger { display: flex; }
    .about-grid, .contact-grid { grid-template-columns: 1fr; }
    .about-visual { height: 260px; }
    .contact-full { grid-column: 1; }
    .hero-ornament { font-size: 200px; }
    footer { padding: 48px 5% 28px; }
    .footer-links { flex-wrap: wrap; gap: 20px; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">KT · Kavya Traders</div>
  <ul class="nav-links">
    <li><a href="#features">Services</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <button class="nav-cta" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Get in Touch</button>
  <div class="nav-hamburger" onclick="this.classList.toggle('open')">
    <span></span><span></span><span></span>
  </div>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-ornament" aria-hidden="true">KT</div>

  <div class="hero-badge">Est. — Gandhinagar, Gujarat</div>

  <div class="hero-logo-circle">
    <span class="hero-logo-initials">KT</span>
  </div>

  <h1>KAVYA<br>TRADERS</h1>

  <p class="hero-subtitle">Quality · Trust · Service</p>

  <p class="hero-tagline">Delivering excellence, one page at a time.</p>

  <p class="hero-desc">
    Your trusted partner for all stationery and printing needs — from daily office supplies to government-grade procurement. Registered on GeM. Rooted in Gandhinagar.
  </p>

  <div class="hero-actions">
    <a href="#contact" class="btn-primary">Contact Us</a>
    <a href="#features" class="btn-outline">Our Services</a>
  </div>
</section>

<!-- FEATURES -->
<section id="features">
  <div class="section-header reveal">
    <span class="section-label">What We Offer</span>
    <h2 class="section-title">Premium Stationery &amp;<br>Printing Solutions</h2>
  </div>

  <div class="features-grid">
    <div class="feature-card reveal">
      <div class="feature-icon">✏️</div>
      <h3 class="feature-title">Quality Stationery</h3>
      <p class="feature-desc">All types of stationery items — pens, notebooks, files, folders, office supplies and more. Sourced for quality, priced for value.</p>
    </div>
    <div class="feature-card reveal">
      <div class="feature-icon">🖨️</div>
      <h3 class="feature-title">Printing Services</h3>
      <p class="feature-desc">Professional printing for letterheads, brochures, banners, visiting cards, and all official documentation needs.</p>
    </div>
    <div class="feature-card reveal">
      <div class="feature-icon">🏛️</div>
      <h3 class="feature-title">Government Dealing</h3>
      <p class="feature-desc">Experienced in government department procurement. We understand official requirements and deliver on time, every time.</p>
    </div>
    <div class="feature-card reveal">
      <div class="feature-icon">🌐</div>
      <h3 class="feature-title">GeM Registered</h3>
      <p class="feature-desc">Registered on the Government e-Marketplace (GeM portal) — making procurement seamless for government buyers.</p>
    </div>
  </div>
</section>

<!-- GEM BANNER -->
<div class="gem-section">
  <p>Verified Vendor</p>
  <h3>Registered on Government e-Marketplace</h3>
  <div class="gem-badge-inline">
    <svg viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
      <polygon points="20,4 25,16 38,16 28,24 32,36 20,28 8,36 12,24 2,16 15,16" fill="#d4aa4a" opacity="0.8"/>
    </svg>
    GeM · Government e-Marketplace · Certified Supplier
  </div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="about-grid">
    <div class="about-visual reveal">
      <div class="about-visual-inner">
        <span class="about-big-initial">KT</span>
        <div class="about-stats">
          <div class="stat">
            <span class="stat-num">100+</span>
            <span class="stat-label">Products</span>
          </div>
          <div class="stat">
            <span class="stat-num">GeM</span>
            <span class="stat-label">Certified</span>
          </div>
          <div class="stat">
            <span class="stat-num">24/7</span>
            <span class="stat-label">Support</span>
          </div>
        </div>
      </div>
    </div>
    <div class="about-content reveal">
      <span class="section-label">About Us</span>
      <h2 class="section-title">Built on Trust,<br>Delivered with Care</h2>
      <p class="about-text">Kavya Traders is a Gandhinagar-based supplier committed to delivering high-quality stationery and printing items. We serve private businesses, educational institutions, and government departments alike.</p>
      <p class="about-text">With our GeM portal registration, we simplify government procurement while maintaining the highest standards of quality and timely delivery.</p>
      <ul class="about-list">
        <li>All types of stationery & printing items</li>
        <li>Government department procurement specialists</li>
        <li>Registered on GeM portal</li>
        <li>GST compliant business</li>
        <li>Based in Sector 3-C, Gandhinagar</li>
      </ul>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="contact-inner">
    <div class="section-header reveal">
      <span class="section-label">Get In Touch</span>
      <h2 class="section-title">We're Here to Help</h2>
    </div>

    <div class="contact-grid">
      <div class="contact-card reveal">
        <div class="contact-icon">📞</div>
        <span class="contact-label">Mobile</span>
        <a class="contact-value" href="tel:9213438258" style="text-decoration:none; color: inherit;">9213 438 258</a>
      </div>

      <div class="contact-card reveal">
        <div class="contact-icon">🧾</div>
        <span class="contact-label">GST Number</span>
        <span class="contact-value" style="font-size:18px; letter-spacing:0.05em;">24FAAPP7788D1ZE</span>
      </div>

      <div class="contact-card contact-full reveal">
        <div class="contact-icon">📍</div>
        <span class="contact-label">Address</span>
        <span class="contact-value">685/1, Sector 3-C,<br>Gandhinagar, Gujarat — 382006</span>
        <a href="https://maps.google.com/?q=Sector+3-C+Gandhinagar+Gujarat+382006" target="_blank" style="margin-top:16px; display:inline-block; font-size:12px; letter-spacing:0.15em; text-transform:uppercase; color:var(--gold); text-decoration:none;">Open in Maps →</a>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">KAVYA TRADERS</div>
  <div class="footer-tagline">Quality. Trust. Service.</div>
  <div class="footer-divider"></div>
  <ul class="footer-links">
    <li><a href="#features">Services</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="tel:9213438258">Call Us</a></li>
  </ul>
  <p class="footer-copy">© 2026 Kavya Traders · GST: 24FAAPP7788D1ZE · Gandhinagar, Gujarat 382006</p>
  <p class="footer-trust">Thank you for your trust and support.</p>
</footer>

<script>
  const reveals = document.querySelectorAll('.reveal');
  const obs = new IntersectionObserver(entries => {
    entries.forEach((e, i) => {
      if (e.isIntersecting) {
        setTimeout(() => e.target.classList.add('visible'), i * 80);
        obs.unobserve(e.target);
      }
    });
  }, { threshold: 0.12 });
  reveals.forEach(el => obs.observe(el));
</script>
</body>
</html>
