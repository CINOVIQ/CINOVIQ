<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#080808">
  <meta name="description" content="CINOVIQ is a creative advertising agency specializing in AI commercials, Meta Ads management, lead generation, and creative strategy.">

  <title>CINOVIQ | The Art of Being Seen</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --black: #080808;
      --lime: #C6FF00;
      --violet: #7C3AED;
      --white: #FFFFFF;
      --graphite: #1A1A1A;
      --muted: #A1A1AA;
      --border: #292929;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--black);
      color: var(--white);
      font-family: 'DM Sans', sans-serif;
      overflow-x: hidden;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    button, input, textarea, select {
      font: inherit;
    }

    button {
      cursor: pointer;
    }

    h1, h2, h3, .logo {
      font-family: 'Space Grotesk', sans-serif;
    }

    .container {
      width: min(1180px, 90%);
      margin: auto;
    }

    .section {
      padding: 110px 0;
    }

    .eyebrow {
      color: var(--lime);
      font-size: 12px;
      letter-spacing: 3px;
      text-transform: uppercase;
      font-weight: 700;
      margin-bottom: 20px;
    }

    .section-title {
      font-size: clamp(36px, 5vw, 64px);
      line-height: 1.08;
      letter-spacing: -2px;
      margin-bottom: 24px;
    }

    .section-description {
      color: var(--muted);
      line-height: 1.8;
      max-width: 650px;
      font-size: 16px;
    }

    .lime {
      color: var(--lime);
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 12px;
      padding: 16px 26px;
      border-radius: 6px;
      font-weight: 700;
      font-size: 14px;
      transition: 0.3s;
      border: 1px solid transparent;
    }

    .btn-primary {
      background: var(--lime);
      color: var(--black);
    }

    .btn-primary:hover {
      background: white;
      transform: translateY(-3px);
    }

    .btn-outline {
      border-color: #555;
      color: white;
    }

    .btn-outline:hover {
      border-color: var(--lime);
      color: var(--lime);
    }

    /* NAVIGATION */

    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      background: rgba(8, 8, 8, 0.94);
      border-bottom: 1px solid var(--border);
      backdrop-filter: blur(18px);
    }

    nav {
      height: 82px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
    }

    .logo {
      font-size: 28px;
      font-weight: 700;
      letter-spacing: -1.5px;
      color: var(--lime);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 32px;
    }

    .nav-links a {
      font-size: 13px;
      color: #D4D4D4;
      transition: 0.3s;
    }

    .nav-links a:hover {
      color: var(--lime);
    }

    .menu-toggle {
      display: none;
      background: transparent;
      border: 1px solid var(--border);
      color: white;
      padding: 10px 14px;
      border-radius: 5px;
    }

    /* HERO */

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 160px 0 110px;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: "";
      position: absolute;
      width: 650px;
      height: 650px;
      border-radius: 50%;
      background: var(--violet);
      filter: blur(220px);
      opacity: 0.14;
      top: -350px;
      right: -150px;
      pointer-events: none;
    }

    .hero::after {
      content: "";
      position: absolute;
      width: 400px;
      height: 400px;
      border-radius: 50%;
      background: var(--lime);
      filter: blur(200px);
      opacity: 0.06;
      bottom: -250px;
      left: -150px;
      pointer-events: none;
    }

    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 1050px;
    }

    .hero-badge {
      display: inline-block;
      padding: 10px 18px;
      border: 1px solid #3A3A3A;
      border-radius: 100px;
      font-size: 11px;
      letter-spacing: 2px;
      color: #D4D4D4;
      margin-bottom: 36px;
    }

    .hero h1 {
      font-size: clamp(54px, 9vw, 118px);
      line-height: 0.98;
      letter-spacing: -5px;
      font-weight: 700;
      margin-bottom: 30px;
    }

    .hero p {
      color: #B5B5B5;
      max-width: 660px;
      margin: 0 auto 38px;
      line-height: 1.8;
      font-size: 17px;
    }

    .hero-buttons {
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
    }

    .hero-line {
      width: 1px;
      height: 65px;
      background: linear-gradient(var(--lime), transparent);
      margin: 75px auto 0;
    }

    /* SERVICES */

    .services {
      background: #0D0D0D;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
      margin-top: 55px;
    }

    .service-card {
      background: var(--graphite);
      padding: 42px;
      border: 1px solid var(--border);
      border-radius: 10px;
      transition: 0.3s;
    }

    .service-card:hover {
      border-color: var(--lime);
      transform: translateY(-5px);
    }

    .service-number {
      color: var(--lime);
      font-size: 13px;
      margin-bottom: 45px;
      display: block;
    }

    .service-card h3 {
      font-size: 26px;
      margin-bottom: 15px;
    }

    .service-card p {
      color: var(--muted);
      line-height: 1.8;
      font-size: 15px;
    }

    /* PORTFOLIO */

    .portfolio-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      margin-top: 55px;
    }

    .portfolio-card {
      background: var(--graphite);
      min-height: 310px;
      border-radius: 10px;
      border: 1px solid var(--border);
      padding: 28px;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      position: relative;
      overflow: hidden;
    }

    .portfolio-card::before {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(
        135deg,
        rgba(124,58,237,0.2),
        transparent 55%,
        rgba(198,255,0,0.06)
      );
    }

    .portfolio-card > * {
      position: relative;
      z-index: 1;
    }

    .portfolio-card span {
      color: var(--lime);
      font-size: 11px;
      letter-spacing: 2px;
      margin-bottom: 12px;
    }

    .portfolio-card h3 {
      font-size: 25px;
    }

    .portfolio-note {
      margin-top: 22px;
      color: var(--muted);
      font-size: 13px;
    }

    /* INDUSTRIES */

    .industries {
      background: #0D0D0D;
    }

    .industry-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 14px;
      margin-top: 50px;
    }

    .industry-item {
      padding: 28px;
      background: var(--graphite);
      border: 1px solid var(--border);
      border-radius: 8px;
      font-weight: 600;
      font-size: 16px;
      transition: 0.3s;
    }

    .industry-item:hover {
      color: var(--lime);
      border-color: var(--lime);
    }

    /* PROCESS */

    .process-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 25px;
      margin-top: 55px;
    }

    .process-card {
      border-top: 2px solid var(--lime);
      padding-top: 28px;
    }

    .process-card span {
      font-size: 13px;
      color: var(--violet);
      font-weight: 700;
    }

    .process-card h3 {
      font-size: 29px;
      margin: 22px 0;
    }

    .process-card p {
      color: var(--muted);
      line-height: 1.8;
    }

    /* ABOUT */

    .about {
      background: #0D0D0D;
    }

    .about-layout {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 80px;
      align-items: center;
    }

    .about-visual {
      min-height: 400px;
      background: var(--graphite);
      border: 1px solid var(--border);
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      overflow: hidden;
    }

    .about-visual::before {
      content: "";
      width: 230px;
      height: 230px;
      border: 2px solid var(--violet);
      transform: rotate(45deg);
      position: absolute;
    }

    .about-visual::after {
      content: "";
      width: 140px;
      height: 140px;
      border: 2px solid var(--lime);
      transform: rotate(45deg);
      position: absolute;
    }

    .about-visual span {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 40px;
      font-weight: 700;
      color: white;
      z-index: 2;
      letter-spacing: -2px;
    }

    /* FAQ */

    .faq-list {
      max-width: 850px;
      margin: 50px auto 0;
    }

    details {
      border-bottom: 1px solid var(--border);
      padding: 24px 0;
    }

    summary {
      font-weight: 600;
      font-size: 17px;
      cursor: pointer;
      list-style: none;
      display: flex;
      justify-content: space-between;
      gap: 20px;
    }

    summary::after {
      content: "+";
      color: var(--lime);
      font-size: 24px;
    }

    details[open] summary::after {
      content: "−";
    }

    details p {
      color: var(--muted);
      line-height: 1.8;
      margin-top: 18px;
    }

    /* CONTACT */

    .contact {
      background: #0D0D0D;
    }

    .contact-layout {
      display: grid;
      grid-template-columns: 0.85fr 1.15fr;
      gap: 80px;
      margin-top: 50px;
    }

    .contact-info h3 {
      font-size: 30px;
      margin-bottom: 20px;
    }

    .contact-info p {
      color: var(--muted);
      line-height: 1.8;
    }

    .contact-form {
      display: grid;
      gap: 18px;
    }

    .form-group {
      display: flex;
      flex-direction: column;
      gap: 9px;
    }

    .form-group label {
      font-size: 13px;
      color: #D4D4D4;
    }

    .form-group input,
    .form-group select,
    .form-group textarea {
      background: var(--graphite);
      border: 1px solid #353535;
      color: white;
      border-radius: 6px;
      padding: 15px;
      outline: none;
      width: 100%;
    }

    .form-group input:focus,
    .form-group select:focus,
    .form-group textarea:focus {
      border-color: var(--lime);
    }

    .form-group textarea {
      min-height: 130px;
      resize: vertical;
    }

    .checkbox-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
      margin-top: 8px;
    }

    .checkbox-item {
      display: flex;
      align-items: center;
      gap: 10px;
      color: var(--muted);
      font-size: 13px;
    }

    .checkbox-item input {
      accent-color: var(--lime);
      width: 16px;
      height: 16px;
    }

    .form-note {
      color: var(--muted);
      font-size: 12px;
      line-height: 1.6;
    }

    /* FOOTER */

    footer {
      padding: 55px 0 30px;
      border-top: 1px solid var(--border);
    }

    .footer-top {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 30px;
      margin-bottom: 50px;
    }

    .footer-bottom {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      border-top: 1px solid var(--border);
      padding-top: 25px;
      color: var(--muted);
      font-size: 12px;
    }

    /* MOBILE */

    @media (max-width: 900px) {
      .nav-links {
        display: none;
        position: absolute;
        top: 82px;
        left: 0;
        width: 100%;
        padding: 30px 5%;
        background: var(--black);
        flex-direction: column;
        align-items: flex-start;
        border-bottom: 1px solid var(--border);
      }

      .nav-links.active {
        display: flex;
      }

      .menu-toggle {
        display: block;
      }

      .nav-cta {
        display: none;
      }

      .portfolio-grid,
      .industry-grid,
      .process-grid {
        grid-template-columns: 1fr 1fr;
      }

      .about-layout,
      .contact-layout {
        grid-template-columns: 1fr;
        gap: 40px;
      }
    }

    @media (max-width: 600px) {
      .section {
        padding: 75px 0;
      }

      .hero h1 {
        letter-spacing: -3px;
      }

      .services-grid,
      .portfolio-grid,
      .industry-grid,
      .process-grid,
      .checkbox-grid {
        grid-template-columns: 1fr;
      }

      .service-card {
        padding: 30px;
      }

      .footer-top,
      .footer-bottom {
        flex-direction: column;
        align-items: flex-start;
      }

      .hero-buttons {
        flex-direction: column;
        align-items: stretch;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->

  <header>
    <nav class="container">

      <a href="#home" class="logo">CINOVIQ</a>

      <button
        class="menu-toggle"
        id="menuToggle"
        aria-label="Toggle navigation"
        aria-expanded="false"
      >
        ☰
      </button>

      <div class="nav-links" id="navLinks">
        <a href="#home">Home</a>
        <a href="#services">Services</a>
        <a href="#work">Our Work</a>
        <a href="#industries">Industries</a>
        <a href="#process">Process</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </div>

      <a href="#contact" class="btn btn-primary nav-cta">
        Let's Talk ↗
      </a>

    </nav>
  </header>

  <main>

    <!-- HERO -->

    <section class="hero" id="home">

      <div class="container hero-content">

        <div class="hero-badge">
          CREATIVE PRODUCTION × DIGITAL ADVERTISING
        </div>

        <h1>
          THE ART OF<br>
          <span class="lime">BEING SEEN.</span>
        </h1>

        <p>
          We create compelling AI-powered commercials,
          develop strategic advertising campaigns,
          and help ambitious brands stand out
          in a crowded digital world.
        </p>

        <div class="hero-buttons">
          <a href="#contact" class="btn btn-primary">
            Start Your Project ↗
          </a>

          <a href="#work" class="btn btn-outline">
            Explore Our Work →
          </a>
        </div>

        <div class="hero-line"></div>

      </div>

    </section>

    <!-- SERVICES -->

    <section class="section services" id="services">

      <div class="container">

        <div class="eyebrow">WHAT WE DO</div>

        <h2 class="section-title">
          Creativity Meets<br>
          <span class="lime">Strategy.</span>
        </h2>

        <p class="section-description">
          From attention-grabbing commercials to
          strategic digital campaigns, CINOVIQ
          brings creative ideas and advertising
          together to help brands reach the right audience.
        </p>

        <div class="services-grid">

          <div class="service-card">
            <span class="service-number">01 / CREATIVE</span>
            <h3>AI Commercial Production</h3>
            <p>
              Cinematic AI-generated commercials,
              promotional videos, and branded content
              designed to capture attention.
            </p>
          </div>

          <div class="service-card">
            <span class="service-number">02 / ADVERTISING</span>
            <h3>Meta Ads Management</h3>
            <p>
              Strategic Facebook and Instagram
              advertising campaigns designed to
              connect businesses with potential customers.
            </p>
          </div>

          <div class="service-card">
            <span class="service-number">03 / GROWTH</span>
            <h3>Lead Generation</h3>
            <p>
              Targeted campaigns focused on attracting
              potential customers and creating
              meaningful business opportunities.
            </p>
          </div>

          <div class="service-card">
            <span class="service-number">04 / STRATEGY</span>
            <h3>Creative Strategy</h3>
            <p>
              Creative concepts, advertising direction,
              and marketing strategies built around
              your brand's goals.
            </p>
          </div>

        </div>

      </div>

    </section>

    <!-- PORTFOLIO -->

    <section class="section" id="work">

      <div class="container">

        <div class="eyebrow">SELECTED CONCEPTS</div>

        <h2 class="section-title">
          Made to<br>
          <span class="lime">Stand Out.</span>
        </h2>

        <p class="section-description">
          Explore the creative directions CINOVIQ
          is developing for modern brands.
        </p>

        <div class="portfolio-grid">

          <div class="portfolio-card">
            <span>CREATIVE CONCEPT / 01</span>
            <h3>Fitness & Performance</h3>
          </div>

          <div class="portfolio-card">
            <span>CREATIVE CONCEPT / 02</span>
            <h3>Grooming & Beauty</h3>
          </div>

          <div class="portfolio-card">
            <span>CREATIVE CONCEPT / 03</span>
            <h3>Cafés & Lifestyle</h3>
          </div>

        </div>

        <p class="portfolio-note">
          Portfolio placeholders — replace these with your
          original CINOVIQ projects when ready.
        </p>

      </div>

    </section>

    <!-- INDUSTRIES -->

    <section class="section industries" id="industries">

      <div class="container">

        <div class="eyebrow">WHO WE WORK WITH</div>

        <h2 class="section-title">
          Every Industry.<br>
          <span class="lime">A Different Story.</span>
        </h2>

        <p class="section-description">
          Every business has something worth showing.
          CINOVIQ creates advertising and content
          tailored to the people you want to reach.
        </p>

        <div class="industry-grid">

          <div class="industry-item">Fitness & Wellness ↗</div>
          <div class="industry-item">Grooming & Beauty ↗</div>
          <div class="industry-item">Cafés & Coffee ↗</div>
          <div class="industry-item">Real Estate & Property ↗</div>
          <div class="industry-item">Auto Service & Repair ↗</div>
          <div class="industry-item">Cosmetic Clinics ↗</div>
          <div class="industry-item">Boutiques & Retail ↗</div>

        </div>

      </div>

    </section>

    <!-- PROCESS -->

    <section class="section" id="process">

      <div class="container">

        <div class="eyebrow">OUR APPROACH</div>

        <h2 class="section-title">
          Three Steps.<br>
          <span class="lime">One Vision.</span>
        </h2>

        <div class="process-grid">

          <div class="process-card">
            <span>STEP 01</span>
            <h3>Envision.</h3>
            <p>
              We learn about your business,
              your audience, and your goals.
              Then we develop a creative direction
              that fits your brand.
            </p>
          </div>

          <div class="process-card">
            <span>STEP 02</span>
            <h3>Execute.</h3>
            <p>
              We bring the concept to life through
              creative production and targeted
              advertising campaigns.
            </p>
          </div>

          <div class="process-card">
            <span>STEP 03</span>
            <h3>Elevate.</h3>
            <p>
              We review campaign performance,
              explore new creative opportunities,
              and make informed adjustments
              as your business evolves.
            </p>
          </div>

        </div>

      </div>

    </section>

    <!-- ABOUT -->

    <section class="section about" id="about">

      <div class="container about-layout">

        <div>

          <div class="eyebrow">ABOUT CINOVIQ</div>

          <h2 class="section-title">
            Built for<br>
            <span class="lime">What's Next.</span>
          </h2>

          <p class="section-description">
            CINOVIQ is a creative advertising agency
            bringing together artificial intelligence,
            visual storytelling, and digital marketing.
            <br><br>
            Our approach is simple: understand the brand,
            create something worth watching, and put it
            in front of the right audience.
            <br><br>
            We believe great advertising should
            do more than fill a screen.
            It should make an impression.
          </p>

        </div>

        <div class="about-visual">
          <span>CINOVIQ</span>
        </div>

      </div>

    </section>

    <!-- FAQ -->

    <section class="section" id="faq">

      <div class="container">

        <div class="eyebrow" style="text-align:center">
          FREQUENTLY ASKED QUESTIONS
        </div>

        <h2 class="section-title" style="text-align:center">
          Good Questions.<br>
          <span class="lime">Clear Answers.</span>
        </h2>

        <div class="faq-list">

          <details>
            <summary>
              What services does CINOVIQ offer?
            </summary>
            <p>
              CINOVIQ specializes in AI commercial production,
              Meta Ads management, lead generation,
              and creative marketing strategy.
            </p>
          </details>

          <details>
            <summary>
              Do you work with small businesses?
            </summary>
            <p>
              Yes. We work with businesses at different
              stages and tailor our approach to their
              goals, needs, and available budget.
            </p>
          </details>

          <details>
            <summary>
              Do I need a large advertising budget?
            </summary>
            <p>
              Not necessarily. We discuss your goals
              and budget before recommending an
              advertising approach.
            </p>
          </details>

          <details>
            <summary>
              Is advertising spend included in your fee?
            </summary>
            <p>
              Advertising spend is separate from
              CINOVIQ's management and creative fees.
              Your advertising budget goes toward
              the platforms running your campaigns.
            </p>
          </details>

          <details>
            <summary>
              Can I request creative production without ads?
            </summary>
            <p>
              Yes. Creative production and advertising
              management can be discussed separately
              based on your project's needs.
            </p>
          </details>

        </div>

      </div>

    </section>

    <!-- CONTACT -->

    <section class="section contact" id="contact">

      <div class="container">

        <div class="eyebrow">LET'S CONNECT</div>

        <h2 class="section-title">
          Your Vision.<br>
          <span class="lime">Our Next Project.</span>
        </h2>

        <div class="contact-layout">

          <div class="contact-info">

            <h3>Let's create something worth seeing.</h3>

            <p>
              Tell us a little about your business
              and what you're looking to accomplish.
              We'll take it from there.
            </p>

          </div>

          <form class="contact-form" id="contactForm">

            <div class="form-group">
              <label for="name">Full Name</label>
              <input
                type="text"
                id="name"
                name="name"
                placeholder="Your name"
                required
              >
            </div>

            <div class="form-group">
              <label for="email">Work Email</label>
              <input
                type="email"
                id="email"
                name="email"
                placeholder="you@company.com"
                required
              >
            </div>

            <div class="form-group">
              <label for="budget">Monthly Budget</label>

              <select id="budget" name="budget" required>
                <option value="">Select your budget</option>
                <option>$500 – $1,000</option>
                <option>$1,000 – $2,000</option>
                <option>$2,000 – $5,000</option>
                <option>$5,000 – $10,000</option>
                <option>$10,000+</option>
              </select>
            </div>

            <div class="form-group">
              <label>Services You're Interested In</label>

              <div class="checkbox-grid">

                <label class="checkbox-item">
                  <input type="checkbox" name="services" value="Digital Advertising">
                  Digital Advertising
                </label>

                <label class="checkbox-item">
                  <input type="checkbox" name="services" value="Meta Ads">
                  Meta Ads
                </label>

                <label class="checkbox-item">
                  <input type="checkbox" name="services" value="Creative Production">
                  Creative Production
                </label>

                <label class="checkbox-item">
                  <input type="checkbox" name="services" value="Lead Generation">
                  Lead Generation
                </label>

                <label class="checkbox-item">
                  <input type="checkbox" name="services" value="Marketing Strategy">
                  Marketing Strategy
                </label>

                <label class="checkbox-item">
                  <input type="checkbox" name="services" value="Creative Digital Solutions">
                  Creative Digital Solutions
                </label>

              </div>
            </div>

            <div class="form-group">
              <label for="message">Tell Us About Your Project</label>

              <textarea
                id="message"
                name="message"
                placeholder="What are you looking to create or accomplish?"
                required
              ></textarea>
            </div>

            <button type="submit" class="btn btn-primary">
              Prepare Inquiry ↗
            </button>

            <p class="form-note">
              This demo form does not send messages yet.
              You'll connect it to an email or form service
              before launching.
            </p>

          </form>

        </div>

      </div>

    </section>

  </main>

  <!-- FOOTER -->

  <footer>

    <div class="container">

      <div class="footer-top">

        <div>
          <div class="logo">CINOVIQ</div>

          <p style="color:#A1A1AA;margin-top:12px">
            The Art of Being Seen.
          </p>
        </div>

        <a href="#contact" class="btn btn-primary">
          Start a Conversation ↗
        </a>

      </div>

      <div class="footer-bottom">

        <span>
          © <span id="year"></span> CINOVIQ.
          All rights reserved.
        </span>

        <span>
          Creative Production × Digital Advertising
        </span>

      </div>

    </div>

  </footer>

  <script>
    // Current year
    document.getElementById("year").textContent =
      new Date().getFullYear();

    // Mobile navigation
    const menuToggle = document.getElementById("menuToggle");
    const navLinks = document.getElementById("navLinks");

    menuToggle.addEventListener("click", () => {
      const isOpen = navLinks.classList.toggle("active");

      menuToggle.setAttribute("aria-expanded", String(isOpen));
      menuToggle.textContent = isOpen ? "✕" : "☰";
    });

    navLinks.querySelectorAll("a").forEach(link => {
      link.addEventListener("click", () => {
        navLinks.classList.remove("active");
        menuToggle.setAttribute("aria-expanded", "false");
        menuToggle.textContent = "☰";
      });
    });

    // Contact form demo
    const contactForm = document.getElementById("contactForm");

    contactForm.addEventListener("submit", event => {
      event.preventDefault();

      if (!contactForm.reportValidity()) return;

      alert(
        "Your inquiry is ready. " +
        "Connect a form service before accepting real submissions."
      );
    });
  </script>

</body>
</html>
