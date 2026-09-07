<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Carvanta Ship LLC — Nationwide Auto Transport Broker</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@600;700;800&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --navy-deep:#0d1b2e;
    --navy:#132743;
    --steel:#1c3a5e;
    --blue:#2f6fed;
    --blue-bright:#4c8cff;
    --paper:#f3f5f8;
    --white:#ffffff;
    --ink:#0d1b2e;
    --muted:#5c6b7f;
    --line:#dfe4ea;
    --amber:#f2a93b;
    --radius-s:4px;
    --radius-m:10px;
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  html{scroll-behavior:smooth;}
  body{
    font-family:'Inter',sans-serif;
    color:var(--ink);
    background:var(--paper);
    line-height:1.5;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,.display{
    font-family:'Big Shoulders Display',sans-serif;
    font-weight:800;
    text-transform:uppercase;
    letter-spacing:0.01em;
    line-height:0.95;
  }
  a{color:inherit;text-decoration:none;}
  img{max-width:100%;display:block;}
  .wrap{max-width:1180px;margin:0 auto;padding:0 28px;}
  button{font-family:inherit;cursor:pointer;border:none;}

  /* ===== HEADER ===== */
  header{
    position:sticky;top:0;z-index:50;
    background:var(--navy-deep);
    border-bottom:1px solid rgba(255,255,255,0.08);
  }
  .nav-row{display:flex;align-items:center;justify-content:space-between;padding:18px 0;}
  .brand{display:flex;align-items:center;gap:10px;}
  .brand-mark{
    width:36px;height:36px;border-radius:8px;
    background:linear-gradient(135deg,var(--blue-bright),var(--blue));
    display:flex;align-items:center;justify-content:center;
    color:white;font-family:'Big Shoulders Display';font-weight:800;font-size:20px;
  }
  .brand-name{color:white;font-size:16px;font-weight:700;letter-spacing:0.02em;}
  .brand-sub{color:#8fa3bd;font-size:11px;letter-spacing:0.12em;}
  nav ul{display:flex;gap:32px;list-style:none;}
  nav a{color:#c4d1e3;font-size:14px;font-weight:500;transition:color .15s;}
  nav a:hover{color:white;}
  .btn{
    display:inline-block;padding:12px 22px;border-radius:var(--radius-s);
    font-size:14px;font-weight:700;transition:transform .15s, box-shadow .15s;
  }
  .btn-primary{background:var(--blue);color:white;}
  .btn-primary:hover{background:var(--blue-bright);}
  .btn-ghost{background:transparent;color:white;border:1px solid rgba(255,255,255,0.35)!important;}
  .btn-ghost:hover{border-color:white!important;}
  .nav-toggle{display:none;background:none;color:white;font-size:26px;}

  /* ===== HERO ===== */
  .hero{
    background:
      linear-gradient(180deg,rgba(13,27,46,0.94),rgba(13,27,46,0.86)),
      repeating-linear-gradient(115deg, rgba(47,111,237,0.10) 0 2px, transparent 2px 90px);
    background-color:var(--navy-deep);
    color:white;
    padding:76px 0 90px;
    position:relative;
    overflow:hidden;
  }
  .hero-grid{display:grid;grid-template-columns:1.15fr 0.85fr;gap:56px;align-items:start;}
  .route-line{
    position:absolute;left:0;right:0;bottom:36px;height:2px;
    background:repeating-linear-gradient(90deg,var(--blue-bright) 0 14px, transparent 14px 24px);
    opacity:0.35;
  }
  .eyebrow-plain{color:#8fa3bd;font-size:14px;font-weight:600;margin-bottom:16px;}
  .hero h1{font-size:56px;color:white;margin-bottom:6px;}
  .hero h1 .accent{color:var(--blue-bright);}
  .hero p.lead{
    color:#c4d1e3;font-family:'Inter';font-weight:400;
    font-size:17px;max-width:440px;margin:22px 0 32px;
  }
  .hero-ctas{display:flex;gap:14px;flex-wrap:wrap;}
  .trust-strip{display:flex;gap:28px;margin-top:44px;flex-wrap:wrap;}
  .trust-item{display:flex;align-items:center;gap:9px;color:#c4d1e3;font-size:13px;font-weight:500;}
  .trust-item svg{flex-shrink:0;color:var(--blue-bright);}

  /* ===== QUOTE CARD ===== */
  .quote-card{
    background:var(--steel);
    border:1px solid rgba(255,255,255,0.1);
    border-radius:var(--radius-m);
    padding:28px;
    box-shadow:0 24px 60px rgba(0,0,0,0.35);
  }
  .quote-card h3{font-size:22px;color:white;margin-bottom:20px;letter-spacing:0.01em;}
  .field-row{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:14px;}
  .field label{display:block;font-size:11px;color:#9db0c9;font-weight:600;text-transform:uppercase;letter-spacing:0.06em;margin-bottom:6px;}
  .field input, .field select{
    width:100%;padding:11px 12px;border-radius:var(--radius-s);
    border:1px solid rgba(255,255,255,0.15);
    background:rgba(255,255,255,0.06);color:white;font-size:14px;font-family:inherit;
  }
  .field input::placeholder{color:#6b7f98;}
  .field select option{background:var(--steel);color:white;}
  .quote-submit{
    width:100%;background:var(--blue);color:white;padding:14px;border-radius:var(--radius-s);
    font-size:14px;font-weight:700;letter-spacing:0.03em;margin-top:6px;
  }
  .quote-submit:hover{background:var(--blue-bright);}
  .estimate-box{
    margin-top:18px;background:var(--navy-deep);border-radius:var(--radius-s);
    padding:18px 20px;display:none;
  }
  .estimate-box.show{display:block;}
  .estimate-box .label{font-size:11px;color:#9db0c9;text-transform:uppercase;letter-spacing:0.08em;}
  .estimate-box .price{font-family:'Big Shoulders Display';font-size:38px;color:var(--blue-bright);margin:4px 0;}
  .estimate-box .meta{font-size:12px;color:#8fa3bd;}

  /* ===== SECTION HEADERS ===== */
  .section{padding:84px 0;}
  .section-head{max-width:560px;margin-bottom:46px;}
  .section-head h2{font-size:34px;color:var(--ink);}
  .section-head p{color:var(--muted);font-size:15px;margin-top:10px;}
  .section-dark{background:var(--navy-deep);color:white;}
  .section-dark .section-head h2{color:white;}
  .section-dark .section-head p{color:#a9b8cc;}

  /* ===== SERVICES ===== */
  .services-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:20px;}
  .service-card{
    background:white;border:1px solid var(--line);border-radius:var(--radius-m);
    padding:26px 22px;
  }
  .service-icon{
    width:44px;height:44px;border-radius:8px;background:var(--navy-deep);
    display:flex;align-items:center;justify-content:center;color:var(--blue-bright);margin-bottom:18px;
  }
  .service-card h3{font-size:18px;text-transform:none;font-weight:700;letter-spacing:0;margin-bottom:8px;font-family:'Inter';}
  .service-card p{font-size:13.5px;color:var(--muted);}

  /* ===== HOW IT WORKS + WHY CHOOSE ===== */
  .split-band{display:grid;grid-template-columns:1.3fr 1fr;gap:0;}
  .how-block{background:var(--navy);color:white;padding:60px 48px;}
  .how-block h2{font-size:28px;color:white;margin-bottom:38px;}
  .steps{position:relative;}
  .steps::before{
    content:'';position:absolute;left:19px;top:20px;bottom:20px;width:2px;
    background:rgba(255,255,255,0.14);
  }
  .step{display:flex;gap:20px;margin-bottom:34px;position:relative;}
  .step:last-child{margin-bottom:0;}
  .step-num{
    width:40px;height:40px;border-radius:50%;background:var(--blue);
    display:flex;align-items:center;justify-content:center;font-weight:700;font-size:15px;
    flex-shrink:0;z-index:1;font-family:'Big Shoulders Display';
  }
  .step h4{font-size:16px;margin-bottom:4px;font-family:'Inter';font-weight:700;text-transform:none;letter-spacing:0;}
  .step p{font-size:13.5px;color:#a9b8cc;}
  .why-block{background:var(--steel);color:white;padding:60px 48px;}
  .why-block h2{font-size:28px;color:white;margin-bottom:26px;}
  .why-list{list-style:none;margin-bottom:34px;}
  .why-list li{display:flex;gap:12px;align-items:flex-start;padding:11px 0;border-bottom:1px solid rgba(255,255,255,0.1);font-size:14.5px;}
  .why-list li:last-child{border-bottom:none;}
  .why-list svg{color:var(--blue-bright);flex-shrink:0;margin-top:2px;}
  .why-stats{display:grid;grid-template-columns:1fr 1fr;gap:20px;}
  .why-stat .num{font-family:'Big Shoulders Display';font-size:32px;color:var(--blue-bright);}
  .why-stat .lab{font-size:12px;color:#c4d1e3;}

  /* ===== REVIEWS ===== */
  .reviews-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;}
  .review-card{background:white;border:1px solid var(--line);border-radius:var(--radius-m);padding:24px;}
  .review-top{display:flex;align-items:center;gap:12px;margin-bottom:14px;}
  .avatar{
    width:42px;height:42px;border-radius:50%;background:var(--navy);color:white;
    display:flex;align-items:center;justify-content:center;font-weight:700;font-size:15px;font-family:'Big Shoulders Display';
  }
  .review-name{font-weight:700;font-size:14.5px;}
  .stars{color:var(--amber);font-size:12px;letter-spacing:1px;}
  .review-card p{font-size:13.5px;color:var(--muted);}

  /* ===== CONTACT / CTA ===== */
  .cta-band{
    background:linear-gradient(120deg,var(--navy-deep),var(--navy));
    color:white;padding:64px 0;
  }
  .cta-inner{display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:24px;}
  .cta-inner h2{font-size:30px;color:white;max-width:480px;}
  .contact-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:24px;margin-top:10px;}
  .contact-item{display:flex;gap:14px;align-items:flex-start;}
  .contact-item svg{color:var(--blue-bright);flex-shrink:0;margin-top:2px;}
  .contact-item .lab{font-size:11px;color:#8fa3bd;text-transform:uppercase;letter-spacing:0.07em;margin-bottom:3px;}
  .contact-item .val{font-size:14.5px;font-weight:600;}

  /* ===== FOOTER ===== */
  footer{background:var(--navy-deep);color:#8fa3bd;padding:32px 0;border-top:1px solid rgba(255,255,255,0.08);}
  .footer-row{display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:16px;font-size:13px;}
  .footer-row nav ul{gap:22px;}
  .footer-row nav a{color:#8fa3bd;font-size:13px;}
  .footer-row nav a:hover{color:white;}

  /* ===== RESPONSIVE ===== */
  @media (max-width:920px){
    nav ul{display:none;}
    .nav-toggle{display:block;}
    .hero-grid{grid-template-columns:1fr;}
    .hero h1{font-size:40px;}
    .services-grid{grid-template-columns:1fr 1fr;}
    .split-band{grid-template-columns:1fr;}
    .reviews-grid{grid-template-columns:1fr;}
    .contact-grid{grid-template-columns:1fr;}
    .cta-inner{flex-direction:column;align-items:flex-start;}
  }
  @media (max-width:560px){
    .services-grid{grid-template-columns:1fr;}
    .field-row{grid-template-columns:1fr;}
    .hero h1{font-size:32px;}
    .btn-ghost{display:none;}
  }
  @media (prefers-reduced-motion:reduce){
    html{scroll-behavior:auto;}
  }

  /* ===== TELEGRAM FLOATING BUTTON ===== */
  .tg-float{
    position:fixed;bottom:26px;right:26px;z-index:60;
    width:58px;height:58px;border-radius:50%;
    background:var(--blue);
    display:flex;align-items:center;justify-content:center;
    box-shadow:0 10px 30px rgba(47,111,237,0.45);
    transition:transform .15s, background .15s;
  }
  .tg-float:hover{background:var(--blue-bright);transform:translateY(-2px);}
  .tg-tooltip{
    position:fixed;bottom:40px;right:92px;z-index:60;
    background:var(--navy-deep);color:white;font-size:13px;font-weight:600;
    padding:8px 14px;border-radius:6px;white-space:nowrap;
    opacity:0;pointer-events:none;transition:opacity .15s;
  }
  .tg-float:hover + .tg-tooltip{opacity:1;}
  @media (max-width:560px){
    .tg-float{width:52px;height:52px;bottom:18px;right:18px;}
    .tg-tooltip{display:none;}
  }
</style>
</head>
<body>

<header>
  <div class="wrap nav-row">
    <div class="brand">
      <div class="brand-mark">C</div>
      <div>
        <div class="brand-name">Carvanta</div>
        <div class="brand-sub">LOGISTICS</div>
      </div>
    </div>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#how">How It Works</a></li>
        <li><a href="#why">Why Us</a></li>
        <li><a href="#reviews">Reviews</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
    <a href="#quote" class="btn btn-primary">Get a Quote</a>
    <button class="nav-toggle" aria-label="Menu">☰</button>
  </div>
</header>

<section class="hero" id="home">
  <div class="wrap hero-grid">
    <div>
      <div class="eyebrow-plain">Licensed Auto Transport Broker · Nationwide USA</div>
      <h1>Ship your car<br>without the <span class="accent">guesswork</span></h1>
      <p class="lead">Carvanta matches you with vetted carriers, locks in a fair price, and keeps you posted from pickup to delivery — coast to coast.</p>
      <div class="hero-ctas">
        <a href="#quote" class="btn btn-primary">Get a Free Quote</a>
        <a href="#how" class="btn btn-ghost">See How It Works</a>
      </div>
      <div class="trust-strip">
        <div class="trust-item">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M20 6L9 17l-5-5"/></svg>
          FMCSA Licensed &amp; Bonded
        </div>
        <div class="trust-item">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M20 6L9 17l-5-5"/></svg>
          12,000+ Cars Shipped
        </div>
        <div class="trust-item">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M20 6L9 17l-5-5"/></svg>
          4.9/5 Customer Rating
        </div>
      </div>
    </div>

    <div class="quote-card" id="quote">
      <h3>Get Your Quote</h3>
      <div class="field-row">
        <div class="field">
          <label>Pickup ZIP</label>
          <input type="text" id="pickupZip" placeholder="e.g. 90210">
        </div>
        <div class="field">
          <label>Delivery ZIP</label>
          <input type="text" id="deliveryZip" placeholder="e.g. 10001">
        </div>
      </div>
      <div class="field-row">
        <div class="field">
          <label>Vehicle Type</label>
          <select id="vehicleType">
            <option>Sedan</option>
            <option>SUV</option>
            <option>Pickup Truck</option>
            <option>Motorcycle</option>
          </select>
        </div>
        <div class="field">
          <label>Transport Type</label>
          <select id="transportType">
            <option value="open">Open Transport</option>
            <option value="enclosed">Enclosed Transport</option>
          </select>
        </div>
      </div>
      <button class="quote-submit" id="estimateBtn">Get Estimate</button>
      <div id="zipWarning" style="display:none;color:#ff8a8a;font-size:12.5px;margin-top:10px;text-align:center;">Please enter both Pickup and Delivery ZIP codes.</div>
      <div class="estimate-box" id="estimateBox">
        <div class="label">Estimated Price</div>
        <div class="price" id="priceOut">$1,250</div>
        <div class="meta" id="metaOut">Open Transport · 2–5 Days</div>
      </div>
    </div>
  </div>
  <div class="route-line"></div>
</section>

<section class="section" id="services">
  <div class="wrap">
    <div class="section-head">
      <h2>Our Services</h2>
      <p>Whatever you're moving and wherever it's going, we match you with the right carrier for the job.</p>
    </div>
    <div class="services-grid">
      <div class="service-card">
        <div class="service-icon">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="1" y="8" width="14" height="8" rx="1"/><path d="M15 11h4l3 3v2h-7z"/><circle cx="5.5" cy="18" r="1.8"/><circle cx="17.5" cy="18" r="1.8"/></svg>
        </div>
        <h3>Open Transport</h3>
        <p>Cost-effective, reliable shipping for everyday vehicles — our most popular option.</p>
      </div>
      <div class="service-card">
        <div class="service-icon">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="6" width="20" height="12" rx="1"/><path d="M2 10h20"/></svg>
        </div>
        <h3>Enclosed Transport</h3>
        <p>Fully covered hauling for luxury, classic, and exotic cars that need extra protection.</p>
      </div>
      <div class="service-card">
        <div class="service-icon">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M13 2L4 14h6l-1 8 9-12h-6z"/></svg>
        </div>
        <h3>Expedited Shipping</h3>
        <p>Priority scheduling and faster pickup when your timeline can't wait.</p>
      </div>
      <div class="service-card">
        <div class="service-icon">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M3 11l9-7 9 7"/><path d="M5 10v10h14V10"/></svg>
        </div>
        <h3>Door-to-Door</h3>
        <p>Convenient pickup and delivery right at your driveway — no terminal drop-offs.</p>
      </div>
    </div>
  </div>
</section>

<div class="split-band" id="how">
  <div class="how-block">
    <h2>How It Works</h2>
    <div class="steps">
      <div class="step">
        <div class="step-num">1</div>
        <div><h4>Get a Quote</h4><p>Fill out our quick form with pickup, delivery, and vehicle details.</p></div>
      </div>
      <div class="step">
        <div class="step-num">2</div>
        <div><h4>Booking</h4><p>We match you with a vetted, insured carrier at a locked-in rate.</p></div>
      </div>
      <div class="step">
        <div class="step-num">3</div>
        <div><h4>Pickup</h4><p>Your carrier arrives on schedule and inspects the vehicle with you.</p></div>
      </div>
      <div class="step">
        <div class="step-num">4</div>
        <div><h4>Delivery</h4><p>We track the shipment and confirm safe, on-time delivery.</p></div>
      </div>
    </div>
  </div>
  <div class="why-block" id="why">
    <h2>Why Choose Carvanta</h2>
    <ul class="why-list">
      <li><svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M20 6L9 17l-5-5"/></svg> Licensed &amp; fully insured broker</li>
      <li><svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M20 6L9 17l-5-5"/></svg> Every carrier vetted before booking</li>
      <li><svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M20 6L9 17l-5-5"/></svg> Transparent, competitive pricing</li>
      <li><svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M20 6L9 17l-5-5"/></svg> 24/7 support from quote to delivery</li>
    </ul>
    <div class="why-stats">
      <div class="why-stat"><div class="num">12K+</div><div class="lab">Vehicles Shipped</div></div>
      <div class="why-stat"><div class="num">4.9★</div><div class="lab">Average Rating</div></div>
    </div>
  </div>
</div>

<section class="section" id="reviews">
  <div class="wrap">
    <div class="section-head">
      <h2>Customer Reviews</h2>
      <p>Real feedback from people who trusted us with their vehicles.</p>
    </div>
    <div class="reviews-grid">
      <div class="review-card">
        <div class="review-top">
          <div class="avatar">J</div>
          <div><div class="review-name">John D.</div><div class="stars">★★★★★</div></div>
        </div>
        <p>Great service — my car arrived on time and in perfect condition. Communication was clear the whole way.</p>
      </div>
      <div class="review-card">
        <div class="review-top">
          <div class="avatar">S</div>
          <div><div class="review-name">Sarah M.</div><div class="stars">★★★★★</div></div>
        </div>
        <p>The team was professional and kept me updated every step. Booking took five minutes, no surprises on price.</p>
      </div>
      <div class="review-card">
        <div class="review-top">
          <div class="avatar">M</div>
          <div><div class="review-name">Michael T.</div><div class="stars">★★★★★</div></div>
        </div>
        <p>Best auto transport experience I've had. The carrier called ahead and delivery was faster than quoted.</p>
      </div>
    </div>
  </div>
</section>

<section class="cta-band" id="contact">
  <div class="wrap">
    <div class="cta-inner">
      <h2>Ready to ship your car?</h2>
      <a href="#quote" class="btn btn-primary">Get a Free Quote</a>
    </div>
    <div class="contact-grid">
      <div class="contact-item">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M22 16.92v3a2 2 0 01-2.18 2 19.8 19.8 0 01-8.63-3.07 19.5 19.5 0 01-6-6 19.8 19.8 0 01-3.07-8.67A2 2 0 014.11 2h3a2 2 0 012 1.72c.12.9.34 1.79.65 2.65a2 2 0 01-.45 2.11L8.09 9.91a16 16 0 006 6l1.43-1.42a2 2 0 012.11-.45c.86.31 1.75.53 2.65.65A2 2 0 0122 16.92z"/></svg>
        <div><div class="lab">Call Us</div><a class="val" href="tel:+998952301500" style="color:inherit;text-decoration:none;">+998 95 230 15 00</a></div>
      </div>
      <div class="contact-item">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16v16H4z"/><path d="M22 6l-10 7L2 6"/></svg>
        <div><div class="lab">Email</div><a class="val" href="mailto:info@carvantaship.com" style="color:inherit;text-decoration:none;">info@carvantaship.com</a></div>
      </div>
      <div class="contact-item">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>
        <div><div class="lab">Based In</div><div class="val">Kosonsoy, Namangan Region, Uzbekistan</div></div>
      </div>
    </div>
  </div>
</section>

<footer>
  <div class="wrap footer-row">
    <div class="brand">
      <div class="brand-mark" style="width:28px;height:28px;font-size:15px;">C</div>
      <div class="brand-name" style="color:#c4d1e3;">Carvanta Ship LLC</div>
    </div>
    <nav><ul style="display:flex;list-style:none;"><li style="margin-right:22px;"><a href="#home">Home</a></li><li style="margin-right:22px;"><a href="#services">Services</a></li><li style="margin-right:22px;"><a href="#how">How It Works</a></li><li><a href="#contact">Contact</a></li></ul></nav>
    <div>© 2026 Carvanta Ship LLC. All rights reserved.</div>
  </div>
</footer>

<a href="https://t.me/bmzxcc" target="_blank" rel="noopener" class="tg-float" aria-label="Ask us on Telegram">
  <svg width="28" height="28" viewBox="0 0 240 240" fill="none">
    <path d="M180 62L44 113c-9 3-9 9-2 11l35 11 14 42c2 5 4 7 8 7 4 0 6-2 9-5l21-20 37 27c7 5 12 2 14-6l25-118c3-10-4-15-12-11z" fill="white"/>
  </svg>
</a>
<div class="tg-tooltip">Ask us on Telegram</div>

<script>
document.addEventListener('DOMContentLoaded', function(){
  var btn = document.getElementById('estimateBtn');
  if(!btn) return;
  btn.addEventListener('click', function(){
    var pickup = document.getElementById('pickupZip').value.trim();
    var delivery = document.getElementById('deliveryZip').value.trim();
    var vehicle = document.getElementById('vehicleType').value;
    var transport = document.getElementById('transportType').value;
    var warningEl = document.getElementById('zipWarning');

    if(!pickup || !delivery){
      if(warningEl) warningEl.style.display = 'block';
      document.getElementById('estimateBox').classList.remove('show');
      return;
    }
    if(warningEl) warningEl.style.display = 'none';

    // Simple illustrative estimate logic (placeholder — replace with real pricing API)
    var base = 650;
    var vehicleAdj = {Sedan:0, SUV:120, 'Pickup Truck':180, Motorcycle:-250};
    var transportAdj = transport === 'enclosed' ? 350 : 0;
    var distanceFactor = (pickup && delivery) ? Math.abs(hashZip(pickup) - hashZip(delivery)) % 900 : 400;

    var price = base + (vehicleAdj[vehicle] || 0) + transportAdj + distanceFactor;
    var days = transport === 'enclosed' ? '3–6 Days' : '2–5 Days';

    document.getElementById('priceOut').textContent = '$' + price.toLocaleString();
    document.getElementById('metaOut').textContent = (transport === 'enclosed' ? 'Enclosed' : 'Open') + ' Transport · ' + days;
    document.getElementById('estimateBox').classList.add('show');
  });

  function hashZip(z){
    var n = parseInt(z.replace(/\D/g,'').slice(0,5), 10);
    return isNaN(n) ? 500 : n % 1000;
  }
});
</script>

</body>
</html>

