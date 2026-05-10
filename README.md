# trioventra.github.io
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>TrioVentra JRP | Virtual Assistant Agency</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root {
      --navy: #071527;
      --navy-soft: #0d213a;
      --sky: #38bdf8;
      --sky-dark: #0284c7;
      --white: #ffffff;
      --muted: #a8b3c7;
      --card: rgba(255, 255, 255, 0.06);
      --border: rgba(255, 255, 255, 0.12);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: "Inter", sans-serif;
      background: var(--navy);
      color: var(--white);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1120px, 92%);
      margin: auto;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 10;
      background: rgba(7, 21, 39, 0.92);
      backdrop-filter: blur(14px);
      border-bottom: 1px solid var(--border);
    }

    .navbar {
      min-height: 78px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 24px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .logo-mark {
      position: relative;
      width: 42px;
      height: 42px;
      border: 1px solid var(--sky);
      border-radius: 14px;
      display: grid;
      place-items: center;
      background: linear-gradient(135deg, rgba(56, 189, 248, 0.22), rgba(255, 255, 255, 0.04));
    }

    .logo-mark::before,
    .logo-mark::after {
      content: "";
      position: absolute;
      width: 7px;
      height: 7px;
      background: var(--sky);
      border-radius: 50%;
    }

    .logo-mark::before {
      top: 10px;
      left: 12px;
    }

    .logo-mark::after {
      bottom: 10px;
      right: 12px;
    }

    .logo-mark span {
      width: 7px;
      height: 7px;
      background: var(--white);
      border-radius: 50%;
    }

    .brand-name {
      font-size: 1.1rem;
      font-weight: 800;
      letter-spacing: -0.03em;
    }

    .brand-name .ventra {
      color: var(--sky);
    }

    .brand-name .jrp {
      font-style: italic;
      font-weight: 500;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 28px;
      color: var(--muted);
      font-size: 0.95rem;
    }

    nav a:hover {
      color: var(--sky);
    }

    .nav-cta,
    .btn-primary,
    .btn-secondary {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      border-radius: 999px;
      font-weight: 700;
      transition: 0.25s ease;
    }

    .nav-cta {
      padding: 11px 18px;
      background: var(--sky);
      color: var(--navy);
    }

    .nav-cta:hover,
    .btn-primary:hover {
      transform: translateY(-2px);
      background: #7dd3fc;
    }

    .hero {
      position: relative;
      overflow: hidden;
      padding: 110px 0 90px;
      background:
        radial-gradient(circle at top right, rgba(56, 189, 248, 0.22), transparent 34%),
        linear-gradient(180deg, var(--navy), #06111f);
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.08fr 0.92fr;
      align-items: center;
      gap: 54px;
    }

    .eyebrow {
      display: inline-flex;
      margin-bottom: 18px;
      padding: 8px 14px;
      border: 1px solid var(--border);
      border-radius: 999px;
      color: var(--sky);
      background: rgba(56, 189, 248, 0.08);
      font-size: 0.9rem;
      font-weight: 700;
    }

    .hero h1 {
      font-size: clamp(2.6rem, 6vw, 5.4rem);
      line-height: 0.95;
      letter-spacing: -0.08em;
      margin-bottom: 24px;
    }

    .hero h1 span {
      color: var(--sky);
    }

    .hero p {
      max-width: 640px;
      color: var(--muted);
      font-size: 1.12rem;
      margin-bottom: 34px;
    }

    .hero-actions {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
    }

    .btn-primary {
      padding: 15px 24px;
      background: var(--sky);
      color: var(--navy);
    }

    .btn-secondary {
      padding: 15px 24px;
      border: 1px solid var(--border);
      color: var(--white);
      background: rgba(255, 255, 255, 0.04);
    }

    .btn-secondary:hover {
      border-color: var(--sky);
      color: var(--sky);
      transform: translateY(-2px);
    }

    .hero-card {
      padding: 28px;
      border: 1px solid var(--border);
      border-radius: 28px;
      background: linear-gradient(145deg, rgba(255, 255, 255, 0.09), rgba(255, 255, 255, 0.03));
      box-shadow: 0 24px 80px rgba(0, 0, 0, 0.28);
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 16px;
      margin-bottom: 18px;
    }

    .stat-box,
    .service-card,
    .process-card {
      border: 1px solid var(--border);
      border-radius: 22px;
      background: var(--card);
    }

    .stat-box {
      padding: 22px;
    }

    .stat-box strong {
      display: block;
      color: var(--sky);
      font-size: 2rem;
      line-height: 1;
      margin-bottom: 8px;
    }

    .stat-box span {
      color: var(--muted);
      font-size: 0.9rem;
    }

    .support-list {
      display: grid;
      gap: 12px;
      margin-top: 18px;
    }

    .support-item {
      display: flex;
      align-items: center;
      gap: 12px;
      color: var(--muted);
    }

    .check {
      width: 22px;
      height: 22px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      background: rgba(56, 189, 248, 0.16);
      color: var(--sky);
      font-weight: 800;
      flex: none;
    }

    section {
      padding: 90px 0;
    }

    .section-heading {
      max-width: 700px;
      margin-bottom: 42px;
    }

    .section-heading h2 {
      font-size: clamp(2rem, 4vw, 3.4rem);
      line-height: 1;
      letter-spacing: -0.06em;
      margin-bottom: 16px;
    }

    .section-heading p {
      color: var(--muted);
      font-size: 1.05rem;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .service-card {
      padding: 28px;
      transition: 0.25s ease;
    }

    .service-card:hover {
      transform: translateY(-6px);
      border-color: rgba(56, 189, 248, 0.5);
      background: rgba(56, 189, 248, 0.08);
    }

    .service-icon {
      width: 46px;
      height: 46px;
      border-radius: 16px;
      display: grid;
      place-items: center;
      background: rgba(56, 189, 248, 0.14);
      color: var(--sky);
      font-size: 1.35rem;
      margin-bottom: 18px;
    }

    .service-card h3 {
      margin-bottom: 10px;
      font-size: 1.15rem;
    }

    .service-card p {
      color: var(--muted);
      font-size: 0.95rem;
    }

    .about {
      background: var(--navy-soft);
    }

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 36px;
      align-items: center;
    }

    .about-panel {
      padding: 36px;
      border-radius: 28px;
      border: 1px solid var(--border);
      background: rgba(255, 255, 255, 0.055);
    }

    .about-panel h2 {
      font-size: clamp(2rem, 4vw, 3.2rem);
      line-height: 1;
      letter-spacing: -0.06em;
      margin-bottom: 18px;
    }

    .about-panel p {
      color: var(--muted);
      margin-bottom: 18px;
    }

    .process-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .process-card {
      padding: 26px;
    }

    .step {
      color: var(--sky);
      font-weight: 800;
      margin-bottom: 14px;
    }

    .process-card h3 {
      margin-bottom: 8px;
    }

    .process-card p {
      color: var(--muted);
      font-size: 0.94rem;
    }

    .cta-footer {
      padding: 90px 0;
      background:
        radial-gradient(circle at bottom left, rgba(56, 189, 248, 0.2), transparent 34%),
        #030b15;
      border-top: 1px solid var(--border);
    }

    .cta-box {
      text-align: center;
      max-width: 780px;
      margin: auto;
    }

    .cta-box h2 {
      font-size: clamp(2.2rem, 5vw, 4.2rem);
      line-height: 1;
      letter-spacing: -0.07em;
      margin-bottom: 18px;
    }

    .cta-box p {
      color: var(--muted);
      margin-bottom: 30px;
      font-size: 1.05rem;
    }

    footer {
      padding: 26px 0;
      background: #030b15;
      border-top: 1px solid var(--border);
      color: var(--muted);
      font-size: 0.92rem;
    }

    .footer-row {
      display: flex;
      justify-content: space-between;
      gap: 18px;
      flex-wrap: wrap;
    }

    @media (max-width: 900px) {
      nav ul {
        display: none;
      }

      .hero-grid,
      .about-grid {
        grid-template-columns: 1fr;
      }

      .services-grid,
      .process-grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    @media (max-width: 580px) {
      .navbar {
        min-height: 72px;
      }

      .nav-cta {
        display: none;
      }

      .hero {
        padding: 78px 0 70px;
      }

      .services-grid,
      .process-grid,
      .stats {
        grid-template-columns: 1fr;
      }

      .hero-card,
      .about-panel {
        padding: 24px;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="container navbar">
      <a href="#" class="brand" aria-label="TrioVentra JRP Home">
        <div class="logo-mark"><span></span></div>
        <div class="brand-name">
          Trio<span class="ventra">Ventra</span> <span class="jrp">JRP</span>
        </div>
      </a>

      <nav aria-label="Main navigation">
        <ul>
          <li><a href="#services">Services</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#process">Process</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>

      <a href="#contact" class="nav-cta">Get Started</a>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="container hero-grid">
        <div>
          <div class="eyebrow">Startup VA Agency for Growing Teams</div>
          <h1>Your Partner in <span>Virtual Excellence.</span></h1>
          <p>
            Driven by service. Powered by people. TrioVentra JRP helps businesses stay responsive, organized, and ready to grow through reliable virtual assistant support.
          </p>
          <div class="hero-actions">
            <a href="#services" class="btn-secondary">Explore Services</a>
          </div>
        </div>

        <aside class="hero-card" aria-label="Company highlights">
          <div class="stats">
            <div class="stat-box">
              <strong>12+</strong>
              <span>Years combined customer service experience</span>
            </div>
            <div class="stat-box">
              <strong>24/7</strong>
              <span>Support-ready mindset for global clients</span>
            </div>
            <div class="stat-box">
              <strong>3</strong>
              <span>Founders connected by service excellence</span>
            </div>
            <div class="stat-box">
              <strong>100%</strong>
              <span>People-first virtual support</span>
            </div>
          </div>

          <div class="support-list">
            <div class="support-item"><span class="check">✓</span>Email, live chat, phone, and ticket support</div>
            <div class="support-item"><span class="check">✓</span>CRM, admin, booking, and e-commerce assistance</div>
            <div class="support-item"><span class="check">✓</span>Lead generation, outreach, and appointment setting</div>
          </div>
        </aside>
      </div>
    </section>

    <section id="services">
      <div class="container">
        <div class="section-heading">
          <h2>Virtual support built for daily business momentum.</h2>
          <p>From customer communication to backend operations, we help you handle the work that keeps your business moving.</p>
        </div>

        <div class="services-grid">
          <article class="service-card">
            <div class="service-icon">✉</div>
            <h3>Customer Support</h3>
            <p>Email support, live chat, phone support, ticket handling, CRM management, and customer follow-ups.</p>
          </article>

          <article class="service-card">
            <div class="service-icon">📈</div>
            <h3>Sales & Lead Generation</h3>
            <p>Appointment setting, cold outreach, lead qualification, CRM updates, and prospect communication.</p>
          </article>

          <article class="service-card">
            <div class="service-icon">⚙</div>
            <h3>Technical & Operations</h3>
            <p>Technical support, admin support, reservations, bookings, and operational task management.</p>
          </article>

          <article class="service-card">
            <div class="service-icon">🛒</div>
            <h3>E-commerce Support</h3>
            <p>Order inquiries, product questions, refunds, returns, customer updates, and store support tasks.</p>
          </article>

          <article class="service-card">
            <div class="service-icon">🎨</div>
            <h3>Creative Services</h3>
            <p>Graphic design, social media materials, basic brand visuals, and promotional content support.</p>
          </article>

          <article class="service-card">
            <div class="service-icon">📋</div>
            <h3>Admin Assistance</h3>
            <p>Inbox management, data entry, file organization, calendar support, reporting, and daily admin tasks.</p>
          </article>
        </div>
      </div>
    </section>

    <section id="about" class="about">
      <div class="container about-grid">
        <div class="about-panel">
          <h2>Service-first support with real frontline experience.</h2>
          <p>
            TrioVentra JRP combines customer service, technical support, lead generation, administrative, financial, and hotel reservation experience to provide dependable virtual assistance.
          </p>
          <p>
            We are built for startups, small businesses, agencies, and growing teams that need reliable people behind their customer and operational workflows.
          </p>
        </div>

        <div class="about-panel">
          <div class="support-list">
            <div class="support-item"><span class="check">✓</span>Call center and customer service background</div>
            <div class="support-item"><span class="check">✓</span>Technical support and troubleshooting experience</div>
            <div class="support-item"><span class="check">✓</span>Lead generation and sales support exposure</div>
            <div class="support-item"><span class="check">✓</span>Admin tasks, CRM updates, and inbox management</div>
            <div class="support-item"><span class="check">✓</span>Financial, hotel, reservations, and booking support</div>
          </div>
        </div>
      </div>
    </section>

    <section id="process">
      <div class="container">
        <div class="section-heading">
          <h2>A simple process for smoother delegation.</h2>
          <p>We help you define the work, organize the workflow, and provide support that fits your business needs.</p>
        </div>

        <div class="process-grid">
          <article class="process-card">
            <div class="step">01</div>
            <h3>Discover</h3>
            <p>We learn your business, goals, tools, and support requirements.</p>
          </article>

          <article class="process-card">
            <div class="step">02</div>
            <h3>Match</h3>
            <p>We align the right VA service with the tasks you need handled.</p>
          </article>

          <article class="process-card">
            <div class="step">03</div>
            <h3>Launch</h3>
            <p>We set up workflows, communication channels, and task expectations.</p>
          </article>

          <article class="process-card">
            <div class="step">04</div>
            <h3>Support</h3>
            <p>We provide consistent service while improving the process over time.</p>
          </article>
        </div>
      </div>
    </section>

    <section id="contact" class="cta-footer">
      <div class="container cta-box">
        <h2>Ready to build your virtual support team?</h2>
        <p>
          Partner with TrioVentra JRP and free up your time with people-powered support for customer service, admin, sales, technical, and creative tasks.
        </p>
        <a href="mailto:perxcyval@gmail.com" class="btn-primary">Contact Us Today</a>
<a href="https://wa.me/639288123453"  class="btn-primary">Message us on WhatsApp</a> 
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-row">
      <p>© 2026 TrioVentra JRP. All rights reserved.</p>
      <p>Your Partner in Virtual Excellence.</p>
    </div>
  </footer>
</body>
</html>
