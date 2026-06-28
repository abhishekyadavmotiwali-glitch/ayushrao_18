<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Portfolio of Abhishek Yadav, a passionate Full Stack Developer specializing in React, Node.js, and modern web technologies." />
  <meta name="keywords" content="Abhishek Yadav, Full Stack Developer, React Developer, Frontend Developer, Web Developer, Portfolio, JavaScript, Next.js, Node.js" />
  <meta property="og:title" content="Abhishek Yadav | Full Stack Developer Portfolio" />
  <meta property="og:description" content="Portfolio of Abhishek Yadav, a passionate Full Stack Developer specializing in React, Node.js, and modern web technologies." />
  <meta name="theme-color" content="#09090b" />
  <title>Abhishek Yadav | Full Stack Developer Portfolio</title>

  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet" />
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />

  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg: #09090b;
      --bg2: #111113;
      --bg3: #18181b;
      --border: #27272a;
      --text: #fafafa;
      --muted: #a1a1aa;
      --purple: #a855f7;
      --purple-dark: #7c3aed;
      --cyan: #22d3ee;
      --green: #4ade80;
      --card: #111113;
      --radius: 12px;
    }

    html { scroll-behavior: smooth; }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'Inter', sans-serif;
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* Scrollbar */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: var(--bg); }
    ::-webkit-scrollbar-thumb { background: var(--border); border-radius: 3px; }

    /* ── NAV ── */
    nav {
      position: fixed; top: 0; width: 100%; z-index: 100;
      background: rgba(9,9,11,0.85);
      backdrop-filter: blur(16px);
      border-bottom: 1px solid var(--border);
      padding: 0 max(24px, calc((100vw - 1100px)/2));
      display: flex; align-items: center; justify-content: space-between;
      height: 64px;
    }

    .nav-logo {
      font-family: 'JetBrains Mono', monospace;
      font-size: 1.1rem; font-weight: 500;
      background: linear-gradient(135deg, var(--purple), var(--cyan));
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
      text-decoration: none;
    }

    .nav-links { display: flex; gap: 32px; list-style: none; }
    .nav-links a {
      color: var(--muted); text-decoration: none; font-size: 0.9rem;
      transition: color .2s;
    }
    .nav-links a:hover { color: var(--text); }

    .nav-cta {
      background: linear-gradient(135deg, var(--purple-dark), var(--purple));
      color: #fff; border: none; border-radius: 8px;
      padding: 8px 20px; font-size: 0.875rem; font-weight: 500;
      cursor: pointer; text-decoration: none; transition: opacity .2s;
    }
    .nav-cta:hover { opacity: 0.85; }

    /* hamburger */
    .hamburger { display: none; background: none; border: none; cursor: pointer; color: var(--text); font-size: 1.4rem; }
    .mobile-menu {
      display: none; position: fixed; top: 64px; left: 0; right: 0;
      background: var(--bg2); border-bottom: 1px solid var(--border);
      flex-direction: column; gap: 0; z-index: 99;
    }
    .mobile-menu.open { display: flex; }
    .mobile-menu a {
      color: var(--muted); text-decoration: none; padding: 16px 24px;
      border-bottom: 1px solid var(--border); font-size: 0.95rem;
      transition: color .2s;
    }
    .mobile-menu a:hover { color: var(--text); }

    /* ── SECTIONS ── */
    section { padding: 96px max(24px, calc((100vw - 1100px)/2)); }
    section:first-of-type { padding-top: 140px; }

    /* ── HERO ── */
    .hero {
      min-height: 100vh;
      display: flex; align-items: center;
      position: relative; overflow: hidden;
    }

    /* background glow blobs */
    .hero::before {
      content: '';
      position: absolute; top: -200px; right: -200px;
      width: 600px; height: 600px;
      background: radial-gradient(circle, rgba(168,85,247,0.15) 0%, transparent 70%);
      border-radius: 50%; pointer-events: none;
    }
    .hero::after {
      content: '';
      position: absolute; bottom: -200px; left: -100px;
      width: 500px; height: 500px;
      background: radial-gradient(circle, rgba(34,211,238,0.1) 0%, transparent 70%);
      border-radius: 50%; pointer-events: none;
    }

    .hero-inner {
      position: relative; z-index: 1;
      display: flex; align-items: center; gap: 64px;
      width: 100%;
    }

    .hero-text { flex: 1; }

    .hero-badge {
      display: inline-flex; align-items: center; gap: 8px;
      background: rgba(168,85,247,0.1);
      border: 1px solid rgba(168,85,247,0.3);
      border-radius: 100px; padding: 6px 16px;
      font-size: 0.8rem; color: var(--purple); font-weight: 500;
      margin-bottom: 24px;
    }
    .hero-badge .dot { width: 6px; height: 6px; background: var(--green); border-radius: 50%; animation: pulse 2s infinite; }
    @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:.4} }

    .hero h1 {
      font-size: clamp(2.2rem, 5vw, 3.8rem);
      font-weight: 700; line-height: 1.15;
      margin-bottom: 16px;
    }
    .hero h1 .name {
      background: linear-gradient(135deg, var(--purple), var(--cyan));
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    }

    .hero-role {
      font-family: 'JetBrains Mono', monospace;
      color: var(--cyan); font-size: 1.05rem; margin-bottom: 20px;
    }
    .hero-role span { color: var(--muted); }

    .hero p {
      color: var(--muted); font-size: 1.05rem; max-width: 520px;
      line-height: 1.75; margin-bottom: 36px;
    }

    .hero-btns { display: flex; gap: 16px; flex-wrap: wrap; }

    .btn-primary {
      display: inline-flex; align-items: center; gap: 8px;
      background: linear-gradient(135deg, var(--purple-dark), var(--purple));
      color: #fff; padding: 12px 28px; border-radius: 10px;
      font-size: 0.95rem; font-weight: 500;
      text-decoration: none; transition: transform .2s, box-shadow .2s;
      box-shadow: 0 0 20px rgba(168,85,247,0.3);
    }
    .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 4px 30px rgba(168,85,247,0.5); }

    .btn-outline {
      display: inline-flex; align-items: center; gap: 8px;
      border: 1px solid var(--border); color: var(--text);
      padding: 12px 28px; border-radius: 10px;
      font-size: 0.95rem; font-weight: 500;
      text-decoration: none; transition: border-color .2s, background .2s;
    }
    .btn-outline:hover { border-color: var(--purple); background: rgba(168,85,247,0.07); }

    .hero-stats {
      display: flex; gap: 32px; margin-top: 48px; padding-top: 32px;
      border-top: 1px solid var(--border);
    }
    .stat-val { font-size: 1.8rem; font-weight: 700; color: var(--text); }
    .stat-val span { color: var(--purple); }
    .stat-label { font-size: 0.8rem; color: var(--muted); margin-top: 2px; }

    /* Avatar */
    .hero-avatar {
      flex-shrink: 0;
      width: 320px; height: 320px;
      position: relative;
    }
    .avatar-ring {
      width: 100%; height: 100%;
      border-radius: 50%;
      background: conic-gradient(from 0deg, var(--purple), var(--cyan), var(--purple));
      padding: 3px; animation: spin 8s linear infinite;
    }
    @keyframes spin { to { transform: rotate(360deg); } }

    .avatar-inner {
      width: 100%; height: 100%;
      border-radius: 50%;
      background: var(--bg3);
      display: flex; align-items: center; justify-content: center;
      font-size: 5rem; position: relative; overflow: hidden;
    }
    .avatar-initials {
      font-size: 4.5rem; font-weight: 700;
      background: linear-gradient(135deg, var(--purple), var(--cyan));
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    }

    /* floating tags */
    .float-tag {
      position: absolute;
      background: var(--bg3); border: 1px solid var(--border);
      border-radius: 8px; padding: 8px 14px;
      font-size: 0.78rem; font-weight: 500;
      display: flex; align-items: center; gap: 6px;
      animation: float 3s ease-in-out infinite;
    }
    .float-tag.t1 { top: 20px; right: -30px; animation-delay: 0s; }
    .float-tag.t2 { bottom: 40px; right: -40px; animation-delay: 1s; }
    .float-tag.t3 { bottom: 20px; left: -30px; animation-delay: 2s; }
    @keyframes float { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-8px)} }
    .float-tag i { color: var(--cyan); }

    /* ── SECTION HEADERS ── */
    .sec-label {
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.78rem; color: var(--purple); letter-spacing: 2px;
      text-transform: uppercase; margin-bottom: 12px;
    }
    .sec-title {
      font-size: clamp(1.8rem, 3.5vw, 2.4rem);
      font-weight: 700; margin-bottom: 12px;
    }
    .sec-title span {
      background: linear-gradient(135deg, var(--purple), var(--cyan));
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    }
    .sec-desc { color: var(--muted); max-width: 560px; font-size: 1rem; line-height: 1.7; }

    /* ── ABOUT ── */
    #about { background: var(--bg2); }

    .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 64px; align-items: center; margin-top: 48px; }

    .about-text p { color: var(--muted); line-height: 1.8; margin-bottom: 20px; font-size: 0.975rem; }

    .about-highlights { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-top: 32px; }
    .highlight-card {
      background: var(--bg3); border: 1px solid var(--border);
      border-radius: 10px; padding: 20px;
    }
    .highlight-card .hi-icon { font-size: 1.5rem; margin-bottom: 10px; }
    .highlight-card h4 { font-size: 0.95rem; font-weight: 600; margin-bottom: 4px; }
    .highlight-card p { font-size: 0.82rem; color: var(--muted); margin: 0; }

    .about-skills-box {
      background: var(--bg3); border: 1px solid var(--border);
      border-radius: var(--radius); padding: 32px;
    }
    .about-skills-box h3 { font-size: 1rem; font-weight: 600; margin-bottom: 24px; }
    .skill-bar-item { margin-bottom: 20px; }
    .skill-bar-top { display: flex; justify-content: space-between; margin-bottom: 8px; font-size: 0.85rem; }
    .skill-bar-top span:last-child { color: var(--muted); }
    .bar-track { background: var(--border); border-radius: 4px; height: 6px; }
    .bar-fill { height: 6px; border-radius: 4px; background: linear-gradient(90deg, var(--purple-dark), var(--cyan)); }

    /* ── SKILLS ── */
    #skills {}

    .skills-header { margin-bottom: 48px; }
    .skills-cats { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 24px; }
    .skill-cat {
      background: var(--bg3); border: 1px solid var(--border);
      border-radius: var(--radius); padding: 28px;
      transition: border-color .25s, transform .25s;
    }
    .skill-cat:hover { border-color: rgba(168,85,247,0.4); transform: translateY(-3px); }
    .skill-cat-header {
      display: flex; align-items: center; gap: 12px; margin-bottom: 20px;
    }
    .cat-icon {
      width: 40px; height: 40px; border-radius: 8px;
      background: rgba(168,85,247,0.15); display: flex; align-items: center; justify-content: center;
      font-size: 1.1rem; color: var(--purple);
    }
    .skill-cat h3 { font-size: 1rem; font-weight: 600; }
    .skill-tags { display: flex; flex-wrap: wrap; gap: 8px; }
    .skill-tag {
      background: var(--bg2); border: 1px solid var(--border);
      border-radius: 6px; padding: 5px 12px;
      font-size: 0.78rem; color: var(--muted);
      transition: color .2s, border-color .2s;
    }
    .skill-tag:hover { color: var(--purple); border-color: rgba(168,85,247,0.4); }

    /* ── PROJECTS ── */
    #projects { background: var(--bg2); }

    .projects-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(340px, 1fr)); gap: 24px; margin-top: 48px; }
    .project-card {
      background: var(--bg3); border: 1px solid var(--border);
      border-radius: var(--radius); padding: 28px; position: relative;
      overflow: hidden; transition: border-color .25s, transform .25s;
    }
    .project-card::before {
      content: '';
      position: absolute; top: 0; left: 0; right: 0; height: 3px;
      background: linear-gradient(90deg, var(--purple-dark), var(--cyan));
      opacity: 0; transition: opacity .25s;
    }
    .project-card:hover { border-color: rgba(168,85,247,0.35); transform: translateY(-4px); }
    .project-card:hover::before { opacity: 1; }

    .project-top { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 16px; }
    .project-icon {
      width: 48px; height: 48px; border-radius: 10px;
      background: rgba(168,85,247,0.12); border: 1px solid rgba(168,85,247,0.25);
      display: flex; align-items: center; justify-content: center;
      font-size: 1.3rem;
    }
    .project-links { display: flex; gap: 10px; }
    .proj-link {
      width: 34px; height: 34px; border-radius: 8px;
      background: var(--bg2); border: 1px solid var(--border);
      display: flex; align-items: center; justify-content: center;
      color: var(--muted); text-decoration: none; font-size: 0.9rem;
      transition: color .2s, border-color .2s;
    }
    .proj-link:hover { color: var(--purple); border-color: rgba(168,85,247,0.4); }

    .project-card h3 { font-size: 1.05rem; font-weight: 600; margin-bottom: 10px; }
    .project-card p { color: var(--muted); font-size: 0.875rem; line-height: 1.65; margin-bottom: 20px; }

    .proj-tags { display: flex; flex-wrap: wrap; gap: 6px; }
    .proj-tag {
      background: rgba(168,85,247,0.1); border: 1px solid rgba(168,85,247,0.2);
      color: var(--purple); border-radius: 5px; padding: 4px 10px; font-size: 0.75rem;
    }

    /* ── EXPERIENCE ── */
    #experience {}

    .exp-header { margin-bottom: 48px; }
    .timeline { position: relative; padding-left: 28px; }
    .timeline::before {
      content: ''; position: absolute; left: 0; top: 0; bottom: 0;
      width: 2px; background: linear-gradient(180deg, var(--purple), var(--cyan), transparent);
    }
    .exp-item {
      position: relative; margin-bottom: 40px;
      background: var(--bg3); border: 1px solid var(--border);
      border-radius: var(--radius); padding: 28px;
      transition: border-color .25s;
    }
    .exp-item:hover { border-color: rgba(168,85,247,0.35); }
    .exp-dot {
      position: absolute; left: -37px; top: 28px;
      width: 12px; height: 12px; border-radius: 50%;
      background: var(--purple); border: 2px solid var(--bg);
      box-shadow: 0 0 10px rgba(168,85,247,0.5);
    }
    .exp-meta { display: flex; justify-content: space-between; align-items: flex-start; flex-wrap: wrap; gap: 8px; margin-bottom: 8px; }
    .exp-company { font-size: 0.82rem; color: var(--cyan); font-weight: 500; margin-bottom: 4px; }
    .exp-role { font-size: 1.05rem; font-weight: 600; }
    .exp-period {
      background: rgba(168,85,247,0.1); border: 1px solid rgba(168,85,247,0.2);
      color: var(--purple); border-radius: 6px; padding: 4px 12px; font-size: 0.78rem;
    }
    .exp-desc { color: var(--muted); font-size: 0.875rem; line-height: 1.7; margin-top: 12px; }
    .exp-bullets { list-style: none; margin-top: 12px; }
    .exp-bullets li { color: var(--muted); font-size: 0.875rem; padding: 4px 0; padding-left: 16px; position: relative; }
    .exp-bullets li::before { content: '▹'; position: absolute; left: 0; color: var(--purple); }

    /* ── CONTACT ── */
    #contact { background: var(--bg2); }

    .contact-wrap { display: grid; grid-template-columns: 1fr 1fr; gap: 64px; margin-top: 48px; align-items: start; }

    .contact-info p { color: var(--muted); font-size: 0.975rem; line-height: 1.75; margin-bottom: 32px; }
    .contact-item {
      display: flex; align-items: center; gap: 14px; margin-bottom: 20px;
    }
    .contact-icon {
      width: 44px; height: 44px; border-radius: 10px;
      background: rgba(168,85,247,0.1); border: 1px solid rgba(168,85,247,0.25);
      display: flex; align-items: center; justify-content: center;
      color: var(--purple); font-size: 1rem; flex-shrink: 0;
    }
    .contact-item-text .label { font-size: 0.78rem; color: var(--muted); }
    .contact-item-text a, .contact-item-text .val {
      font-size: 0.95rem; color: var(--text); text-decoration: none;
      transition: color .2s;
    }
    .contact-item-text a:hover { color: var(--purple); }

    .socials { display: flex; gap: 12px; margin-top: 32px; }
    .social-btn {
      width: 44px; height: 44px; border-radius: 10px;
      background: var(--bg3); border: 1px solid var(--border);
      display: flex; align-items: center; justify-content: center;
      color: var(--muted); text-decoration: none; font-size: 1.1rem;
      transition: color .2s, border-color .2s, transform .2s;
    }
    .social-btn:hover { color: var(--purple); border-color: rgba(168,85,247,0.4); transform: translateY(-2px); }

    /* Form */
    .contact-form { display: flex; flex-direction: column; gap: 18px; }
    .form-group { display: flex; flex-direction: column; gap: 6px; }
    .form-group label { font-size: 0.82rem; color: var(--muted); }
    .form-group input, .form-group textarea {
      background: var(--bg3); border: 1px solid var(--border);
      border-radius: 8px; padding: 12px 16px;
      color: var(--text); font-family: inherit; font-size: 0.9rem;
      transition: border-color .2s; outline: none;
    }
    .form-group input:focus, .form-group textarea:focus { border-color: var(--purple); }
    .form-group textarea { resize: vertical; min-height: 120px; }
    .form-submit {
      background: linear-gradient(135deg, var(--purple-dark), var(--purple));
      color: #fff; border: none; border-radius: 8px;
      padding: 13px 28px; font-size: 0.9rem; font-weight: 500;
      cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 8px;
      transition: opacity .2s, transform .2s;
    }
    .form-submit:hover { opacity: 0.85; transform: translateY(-1px); }

    /* ── FOOTER ── */
    footer {
      padding: 32px max(24px, calc((100vw - 1100px)/2));
      border-top: 1px solid var(--border);
      display: flex; align-items: center; justify-content: space-between;
      flex-wrap: wrap; gap: 16px;
    }
    .footer-logo {
      font-family: 'JetBrains Mono', monospace; font-size: 0.95rem;
      background: linear-gradient(135deg, var(--purple), var(--cyan));
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    }
    footer p { color: var(--muted); font-size: 0.82rem; }
    .footer-links { display: flex; gap: 20px; }
    .footer-links a { color: var(--muted); text-decoration: none; font-size: 0.82rem; transition: color .2s; }
    .footer-links a:hover { color: var(--text); }

    /* ── RESPONSIVE ── */
    @media (max-width: 900px) {
      .hero-inner { flex-direction: column-reverse; gap: 32px; text-align: center; }
      .hero-avatar { width: 220px; height: 220px; }
      .float-tag { display: none; }
      .hero-btns { justify-content: center; }
      .hero-stats { justify-content: center; }
      .about-grid { grid-template-columns: 1fr; gap: 32px; }
      .contact-wrap { grid-template-columns: 1fr; gap: 32px; }
    }
    @media (max-width: 700px) {
      .nav-links, .nav-cta { display: none; }
      .hamburger { display: block; }
      .about-highlights { grid-template-columns: 1fr; }
      .projects-grid { grid-template-columns: 1fr; }
    }

    /* scroll reveal */
    .reveal { opacity: 0; transform: translateY(24px); transition: opacity .55s ease, transform .55s ease; }
    .reveal.visible { opacity: 1; transform: translateY(0); }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">&lt;AY /&gt;</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a href="#contact" class="nav-cta">Hire Me</a>
  <button class="hamburger" id="menuBtn" aria-label="Menu"><i class="fas fa-bars"></i></button>
</nav>

<div class="mobile-menu" id="mobileMenu">
  <a href="#about">About</a>
  <a href="#skills">Skills</a>
  <a href="#projects">Projects</a>
  <a href="#experience">Experience</a>
  <a href="#contact">Contact</a>
</div>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-inner">
    <div class="hero-text reveal">
      <div class="hero-badge"><span class="dot"></span> Available for Work</div>
      <h1>Hi, I'm <span class="name">Abhishek<br/>Yadav</span></h1>
      <div class="hero-role"><span>// </span>Full Stack Developer</div>
      <p>I build scalable, high-performance web applications with modern technologies. Passionate about creating seamless user experiences from frontend to backend.</p>
      <div class="hero-btns">
        <a href="#projects" class="btn-primary"><i class="fas fa-rocket"></i> View Projects</a>
        <a href="#contact" class="btn-outline"><i class="fas fa-envelope"></i> Contact Me</a>
      </div>
      <div class="hero-stats">
        <div>
          <div class="stat-val">3<span>+</span></div>
          <div class="stat-label">Years Experience</div>
        </div>
        <div>
          <div class="stat-val">20<span>+</span></div>
          <div class="stat-label">Projects Built</div>
        </div>
        <div>
          <div class="stat-val">15<span>+</span></div>
          <div class="stat-label">Happy Clients</div>
        </div>
      </div>
    </div>

    <div class="hero-avatar reveal">
      <div class="avatar-ring">
        <div class="avatar-inner">
          <span class="avatar-initials">AY</span>
        </div>
      </div>
      <div class="float-tag t1"><i class="fas fa-code"></i> cyber expert</div>
      <div class="float-tag t2"><i class="fas fa-server"></i> hacker</div>
      <div class="float-tag t3"><i class="fas fa-database"></i> full stack developer</div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="reveal">
    <div class="sec-label">// about me</div>
    <div class="sec-title">Who I <span>Am</span></div>
    <div class="sec-desc">A passionate developer who loves turning ideas into reality through clean, efficient code.</div>
  </div>
  <div class="about-grid">
    <div class="about-text reveal">
      <p>I'm Abhishek Yadav, a Full Stack Developer with 3+ years of experience building modern web applications. I specialize in the MERN stack and have a deep passion for creating products that make a difference.</p>
      <p>From designing intuitive user interfaces to architecting robust backend systems, I enjoy every part of the development process. I'm always eager to learn new technologies and take on challenging projects.</p>
      <p>When I'm not coding, you'll find me exploring new tech trends, contributing to open-source projects, or leveling up my problem-solving skills on competitive platforms.</p>
      <div class="about-highlights">
        <div class="highlight-card">
          <div class="hi-icon">🎯</div>
          <h4>Problem Solver</h4>
          <p>Love tackling complex challenges</p>
        </div>
        <div class="highlight-card">
          <div class="hi-icon">🚀</div>
          <h4>Fast Learner</h4>
          <p>Quickly adapt to new technologies</p>
        </div>
        <div class="highlight-card">
          <div class="hi-icon">💡</div>
          <h4>Creative Mind</h4>
          <p>Unique approach to every project</p>
        </div>
        <div class="highlight-card">
          <div class="hi-icon">🤝</div>
          <h4>Team Player</h4>
          <p>Collaborative & communicative</p>
        </div>
      </div>
    </div>
    <div class="about-skills-box reveal">
      <h3>Core Proficiencies</h3>
      <div class="skill-bar-item">
        <div class="skill-bar-top"><span>java / python</span><span>90%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:90%"></div></div>
      </div>
      <div class="skill-bar-item">
        <div class="skill-bar-top"><span>c / c#</span><span>85%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:85%"></div></div>
      </div>
      <div class="skill-bar-item">
        <div class="skill-bar-top"><span>MySQL / SQL</span><span>80%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:80%"></div></div>
      </div>
      <div class="skill-bar-item">
        <div class="skill-bar-top"><span>TypeScript</span><span>78%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:78%"></div></div>
      </div>
      <div class="skill-bar-item">
        <div class="skill-bar-top"><span>html / css</span><span>70%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:70%"></div></div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="skills-header reveal">
    <div class="sec-label">// my expertise</div>
    <div class="sec-title">Technical <span>Skills</span></div>
    <div class="sec-desc">Technologies and tools I work with to build amazing products.</div>
  </div>
  <div class="skills-cats">
    <div class="skill-cat reveal">
      <div class="skill-cat-header">
        <div class="cat-icon"><i class="fas fa-laptop-code"></i></div>
        <h3>Frontend</h3>
      </div>
      <div class="skill-tags">
        <span class="skill-tag">python</span>
        <span class="skill-tag">Next.js</span>
        <span class="skill-tag">TypeScript</span>
        <span class="skill-tag">JavaScript</span>
        <span class="skill-tag">HTML5</span>
        <span class="skill-tag">CSS3</span>
        <span class="skill-tag">ML</span>
        <span class="skill-tag">java</span>
      </div>
    </div>
    <div class="skill-cat reveal">
      <div class="skill-cat-header">
        <div class="cat-icon"><i class="fas fa-server"></i></div>
        <h3>Backend</h3>
      </div>
      <div class="skill-tags">
        <span class="skill-tag">Python</span>
        <span class="skill-tag">cyber security</span>
        <span class="skill-tag">REST APIs</span>
        <span class="skill-tag">web designing</span>
        <span class="skill-tag"></span>
      </div>
    </div>
    <div class="skill-cat reveal">
      <div class="skill-cat-header">
        <div class="cat-icon"><i class="fas fa-database"></i></div>
        <h3>Database</h3>
      </div>
      <div class="skill-tags">
        <span class="skill-tag">MongoDB</span>
        <span class="skill-tag">MySQL</span>
        <span class="skill-tag">PostgreSQL</span>
        <span class="skill-tag">Redis</span>
        <span class="skill-tag">Firebase</span>
        <span class="skill-tag">Prisma</span>
      </div>
    </div>
    <div class="skill-cat reveal">
      <div class="skill-cat-header">
        <div class="cat-icon"><i class="fas fa-tools"></i></div>
        <h3>Tools & DevOps</h3>
      </div>
      <div class="skill-tags">
        <span class="skill-tag">Git / GitHub</span>
        <span class="skill-tag">Docker</span>
        <span class="skill-tag">AWS</span>
        <span class="skill-tag">Vercel</span>
        <span class="skill-tag">Linux</span>
        <span class="skill-tag">Postman</span>
        <span class="skill-tag">Figma</span>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="reveal">
    <div class="sec-label">// my work</div>
    <div class="sec-title">Featured <span>Projects</span></div>
    <div class="sec-desc">Some of the projects I've built that I'm proud of.</div>
  </div>
  <div class="projects-grid">

    <div class="project-card reveal">
      <div class="project-top">
        <div class="project-icon">🛒</div>
        <div class="project-links">
          <a href="#" class="proj-link"><i class="fab fa-github"></i></a>
          <a href="#" class="proj-link"><i class="fas fa-external-link-alt"></i></a>
        </div>
      </div>
      <h3>E-Commerce Platform</h3>
      <p>A full-featured e-commerce platform with product listings, cart management, payment integration, and an admin dashboard for order management.</p>
      <div class="proj-tags">
        <span class="proj-tag">React</span>
        <span class="proj-tag">Node.js</span>
        <span class="proj-tag">MongoDB</span>
        <span class="proj-tag">Stripe</span>
      </div>
    </div>

    <div class="project-card reveal">
      <div class="project-top">
        <div class="project-icon">💬</div>
        <div class="project-links">
          <a href="#" class="proj-link"><i class="fab fa-github"></i></a>
          <a href="#" class="proj-link"><i class="fas fa-external-link-alt"></i></a>
        </div>
      </div>
      <h3>Real-Time Chat App</h3>
      <p>A scalable real-time chat application with private messaging, group chats, file sharing, online status indicators, and push notifications.</p>
      <div class="proj-tags">
        <span class="proj-tag">React</span>
        <span class="proj-tag">Socket.io</span>
        <span class="proj-tag">Express</span>
        <span class="proj-tag">Redis</span>
      </div>
    </div>

    <div class="project-card reveal">
      <div class="project-top">
        <div class="project-icon">📊</div>
        <div class="project-links">
          <a href="#" class="proj-link"><i class="fab fa-github"></i></a>
          <a href="#" class="proj-link"><i class="fas fa-external-link-alt"></i></a>
        </div>
      </div>
      <h3>Task Management System</h3>
      <p>A collaborative project management tool with Kanban boards, task assignments, deadline tracking, and team analytics dashboard.</p>
      <div class="proj-tags">
        <span class="proj-tag">Next.js</span>
        <span class="proj-tag">PostgreSQL</span>
        <span class="proj-tag">Prisma</span>
        <span class="proj-tag">TypeScript</span>
      </div>
    </div>

    <div class="project-card reveal">
      <div class="project-top">
        <div class="project-icon">🤖</div>
        <div class="project-links">
          <a href="#" class="proj-link"><i class="fab fa-github"></i></a>
          <a href="#" class="proj-link"><i class="fas fa-external-link-alt"></i></a>
        </div>
      </div>
      <h3>AI Content Generator</h3>
      <p>An AI-powered platform that generates blog posts, social media content, and marketing copy using OpenAI API with custom fine-tuning options.</p>
      <div class="proj-tags">
        <span class="proj-tag">Next.js</span>
        <span class="proj-tag">OpenAI API</span>
        <span class="proj-tag">MongoDB</span>
        <span class="proj-tag">Tailwind</span>
      </div>
    </div>

    <div class="project-card reveal">
      <div class="project-top">
        <div class="project-icon">🏦</div>
        <div class="project-links">
          <a href="#" class="proj-link"><i class="fab fa-github"></i></a>
          <a href="#" class="proj-link"><i class="fas fa-external-link-alt"></i></a>
        </div>
      </div>
      <h3>Finance Tracker</h3>
      <p>A personal finance management app with expense tracking, budget planning, visual analytics, and bank statement import functionality.</p>
      <div class="proj-tags">
        <span class="proj-tag">React</span>
        <span class="proj-tag">Node.js</span>
        <span class="proj-tag">MySQL</span>
        <span class="proj-tag">Chart.js</span>
      </div>
    </div>

    <div class="project-card reveal">
      <div class="project-top">
        <div class="project-icon">📱</div>
        <div class="project-links">
          <a href="#" class="proj-link"><i class="fab fa-github"></i></a>
          <a href="#" class="proj-link"><i class="fas fa-external-link-alt"></i></a>
        </div>
      </div>
      <h3>Social Media Dashboard</h3>
      <p>A unified social media management dashboard for scheduling posts, tracking analytics, and managing multiple accounts across platforms.</p>
      <div class="proj-tags">
        <span class="proj-tag">React</span>
        <span class="proj-tag">GraphQL</span>
        <span class="proj-tag">Firebase</span>
        <span class="proj-tag">AWS</span>
      </div>
    </div>

  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="exp-header reveal">
    <div class="sec-label">// my journey</div>
    <div class="sec-title">Work <span>Experience</span></div>
    <div class="sec-desc">My professional journey in the software industry.</div>
  </div>
  <div class="timeline">

    <div class="exp-item reveal">
      <div class="exp-dot"></div>
      <div class="exp-meta">
        <div>
          <div class="exp-company">Tech Solutions Pvt. Ltd.</div>
          <div class="exp-role">Full Stack Developer</div>
        </div>
        <div class="exp-period">2026– Present</div>
      </div>
      <ul class="exp-bullets">
        <li>Built and maintained RESTful APIs serving 50,000+ daily active users</li>
        <li>Developed reusable React component library reducing development time by 40%</li>
        <li>Led migration from monolith to microservices architecture</li>
        <li>Implemented CI/CD pipelines with Docker and GitHub Actions</li>
      </ul>
    </div>

    <div class="exp-item reveal">
      <div class="exp-dot"></div>
      <div class="exp-meta">
        <div>
          <div class="exp-company">StartupHub India</div>
          <div class="exp-role">Frontend Developer</div>
        </div>
        <div class="exp-period">2025 – 2026</div>
      </div>
      <ul class="exp-bullets">
        <li>Developed responsive React web applications with pixel-perfect UI</li>
        <li>Integrated third-party APIs including payment gateways and mapping services</li>
        <li>Improved website performance score from 65 to 95 (Lighthouse)</li>
        <li>Collaborated with design team to implement UI/UX improvements</li>
      </ul>
    </div>

    <div class="exp-item reveal">
      <div class="exp-dot"></div>
      <div class="exp-meta">
        <div>
          <div class="exp-company">Freelance / Self-Employed</div>
          <div class="exp-role">Web Developer</div>
        </div>
        <div class="exp-period">2024– 2025</div>
      </div>
      <ul class="exp-bullets">
        <li>Delivered 15+ client projects including e-commerce sites and dashboards</li>
        <li>Maintained 100% client satisfaction rating across all projects</li>
        <li>Worked across full stack: design, frontend, backend, and deployment</li>
      </ul>
    </div>

  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="reveal">
    <div class="sec-label">// get in touch</div>
    <div class="sec-title">Let's <span>Connect</span></div>
    <div class="sec-desc">Have a project in mind or just want to say hi? I'd love to hear from you!</div>
  </div>
  <div class="contact-wrap">
    <div class="contact-info reveal">
      <p>I'm currently available for freelance work and full-time opportunities. Whether you have a project idea, want to collaborate, or just want to connect — my inbox is always open.</p>

      <div class="contact-item">
        <div class="contact-icon"><i class="fas fa-envelope"></i></div>
        <div class="contact-item-text">
          <div class="label">Email</div>
          <a href="mailto:abhishek.yadav@email.com">abhishekmotiwali@email.com</a>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-icon"><i class="fas fa-phone"></i></div>
        <div class="contact-item-text">
          <div class="label">Phone</div>
          <span class="val">+91 9887674985</span>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-icon"><i class="fas fa-map-marker-alt"></i></div>
        <div class="contact-item-text">
          <div class="label">Location</div>
          <span class="val">indian 🇮🇳</span>
        </div>
      </div>

      <div class="socials">
        <a href="#" class="social-btn" title="GitHub"><i class="fab fa-github"></i></a>
        <a href="#" class="social-btn" title="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
        <a href="#" class="social-btn" title="Twitter"><i class="fab fa-twitter"></i></a>
        <a href="#" class="social-btn" title="Instagram"><i class="fab fa-instagram"></i></a>
      </div>
    </div>

    <div class="contact-form reveal">
      <div class="form-group">
        <label>Your Name</label>
        <input type="text" placeholder="John Doe" />
      </div>
      <div class="form-group">
        <label>Email Address</label>
        <input type="email" placeholder="john@example.com" />
      </div>
      <div class="form-group">
        <label>Subject</label>
        <input type="text" placeholder="Project Inquiry" />
      </div>
      <div class="form-group">
        <label>Message</label>
        <textarea placeholder="Tell me about your project..."></textarea>
      </div>
      <button class="form-submit" onclick="alert('Message sent! I will get back to you soon.')">
        <i class="fas fa-paper-plane"></i> Send Message
      </button>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">&lt;Abhishek Yadav /&gt;</div>
  <p>© 2025 Abhishek Yadav. All rights reserved.</p>
  <div class="footer-links">
    <a href="#home">Home</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a>
  </div>
</footer>

<script>
  // Mobile menu toggle
  const menuBtn = document.getElementById('menuBtn');
  const mobileMenu = document.getElementById('mobileMenu');
  menuBtn.addEventListener('click', () => {
    mobileMenu.classList.toggle('open');
    menuBtn.querySelector('i').classList.toggle('fa-bars');
    menuBtn.querySelector('i').classList.toggle('fa-times');
  });
  mobileMenu.querySelectorAll('a').forEach(a => {
    a.addEventListener('click', () => {
      mobileMenu.classList.remove('open');
      menuBtn.querySelector('i').classList.add('fa-bars');
      menuBtn.querySelector('i').classList.remove('fa-times');
    });
  });

  // Scroll reveal
  const revealEls = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); } });
  }, { threshold: 0.12 });
  revealEls.forEach(el => observer.observe(el));

  // Active nav link highlight
  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('.nav-links a');
  window.addEventListener('scroll', () => {
    let curr = '';
    sections.forEach(s => { if (window.scrollY >= s.offsetTop - 80) curr = s.id; });
    navLinks.forEach(a => {
      a.style.color = a.getAttribute('href') === `#${curr}` ? 'var(--purple)' : '';
    });
  });
</script>
</body>
</html>
