<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shravan Timalsina — Electrical Engineering</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #f9f8f5;
    --surface: #ffffff;
    --border: rgba(0,0,0,0.09);
    --border-strong: rgba(0,0,0,0.18);
    --text: #1a1917;
    --text-secondary: #6b6860;
    --text-tertiary: #a09e99;
    --accent: #1a1917;
    --accent-bg: #1a1917;
    --accent-text: #f9f8f5;
    --tag-bg: #eeecea;
    --tag-text: #6b6860;
    --info-bg: #e8f0fb;
    --info-text: #2655a3;
    --radius: 10px;
    --radius-lg: 14px;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--bg);
    color: var(--text);
    font-size: 16px;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  a { color: inherit; text-decoration: none; }

  /* Nav */
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.1rem 2rem;
    border-bottom: 1px solid var(--border);
    background: var(--bg);
    position: sticky;
    top: 0;
    z-index: 100;
    backdrop-filter: blur(8px);
  }
  .nav-logo { font-size: 15px; font-weight: 500; letter-spacing: -0.01em; }
  .nav-links { display: flex; gap: 2rem; }
  .nav-links a { font-size: 13px; color: var(--text-secondary); transition: color 0.15s; }
  .nav-links a:hover { color: var(--text); }

  /* Layout */
  .container { max-width: 740px; margin: 0 auto; padding: 0 2rem; }
  section { padding: 4.5rem 0; }
  .divider { border: none; border-top: 1px solid var(--border); margin: 0; }
  .section-label {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--text-tertiary);
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin-bottom: 1.75rem;
  }

  /* Hero */
  .hero { padding: 5.5rem 0 4rem; }
  .hero-eyebrow {
    font-family: 'DM Mono', monospace;
    font-size: 12px;
    color: var(--text-tertiary);
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 1.25rem;
  }
  .hero h1 {
    font-size: clamp(32px, 5vw, 44px);
    font-weight: 500;
    line-height: 1.15;
    letter-spacing: -0.03em;
    margin-bottom: 1.25rem;
  }
  .hero h1 em { color: var(--text-secondary); font-style: normal; }
  .hero-desc {
    font-size: 16px;
    color: var(--text-secondary);
    line-height: 1.75;
    max-width: 500px;
    margin-bottom: 2.25rem;
  }
  .hero-btns { display: flex; gap: 10px; flex-wrap: wrap; }
  .btn {
    display: inline-block;
    padding: 10px 22px;
    border-radius: var(--radius);
    font-size: 14px;
    font-family: 'DM Sans', sans-serif;
    font-weight: 500;
    cursor: pointer;
    border: 1px solid var(--border-strong);
    background: transparent;
    color: var(--text);
    transition: background 0.15s, border-color 0.15s;
  }
  .btn:hover { background: var(--surface); }
  .btn-primary {
    background: var(--accent-bg);
    color: var(--accent-text);
    border-color: transparent;
  }
  .btn-primary:hover { opacity: 0.85; background: var(--accent-bg); }

  /* About */
  .about-text p {
    font-size: 15px;
    color: var(--text-secondary);
    line-height: 1.8;
    margin-bottom: 0.85rem;
  }
  .skills-row { display: flex; flex-wrap: wrap; gap: 7px; margin-top: 1.5rem; }
  .skill-pill {
    font-size: 12px;
    font-family: 'DM Mono', monospace;
    background: var(--tag-bg);
    color: var(--tag-text);
    padding: 5px 12px;
    border-radius: 99px;
    border: 1px solid var(--border);
  }

  /* Projects */
  .projects-grid { display: grid; gap: 12px; }
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: var(--radius-lg);
    padding: 1.4rem 1.5rem;
    transition: border-color 0.15s, box-shadow 0.15s;
  }
  .project-card:hover {
    border-color: var(--border-strong);
    box-shadow: 0 2px 12px rgba(0,0,0,0.06);
  }
  .project-top {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 10px;
    gap: 1rem;
  }
  .project-name { font-size: 15px; font-weight: 500; letter-spacing: -0.01em; }
  .project-tag {
    font-size: 11px;
    font-family: 'DM Mono', monospace;
    background: var(--info-bg);
    color: var(--info-text);
    padding: 3px 10px;
    border-radius: 99px;
    white-space: nowrap;
    flex-shrink: 0;
  }
  .project-desc {
    font-size: 13.5px;
    color: var(--text-secondary);
    line-height: 1.7;
    margin-bottom: 14px;
  }
  .project-stack { display: flex; gap: 6px; flex-wrap: wrap; }
  .stack-pill {
    font-size: 11px;
    font-family: 'DM Mono', monospace;
    background: var(--tag-bg);
    color: var(--tag-text);
    padding: 3px 10px;
    border-radius: 99px;
  }

  /* Contact */
  .contact-desc {
    font-size: 15px;
    color: var(--text-secondary);
    line-height: 1.8;
    margin-bottom: 1.5rem;
    max-width: 460px;
  }
  .contact-links { display: flex; flex-direction: column; gap: 10px; max-width: 420px; }
  .contact-link {
    display: flex;
    align-items: center;
    gap: 12px;
    font-size: 14px;
    color: var(--text-secondary);
    padding: 11px 16px;
    border: 1px solid var(--border);
    border-radius: var(--radius);
    background: var(--surface);
    transition: border-color 0.15s, color 0.15s;
  }
  .contact-link:hover { border-color: var(--border-strong); color: var(--text); }
  .contact-icon { width: 15px; height: 15px; opacity: 0.45; flex-shrink: 0; }

  /* Footer */
  footer {
    padding: 2rem;
    border-top: 1px solid var(--border);
    font-family: 'DM Mono', monospace;
    font-size: 12px;
    color: var(--text-tertiary);
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 100%;
  }

  /* Animations */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .hero > * { animation: fadeUp 0.5s ease both; }
  .hero-eyebrow { animation-delay: 0.05s; }
  .hero h1 { animation-delay: 0.12s; }
  .hero-desc { animation-delay: 0.2s; }
  .hero-btns { animation-delay: 0.28s; }

  @media (max-width: 600px) {
    nav { padding: 1rem 1.25rem; }
    .nav-links { gap: 1.25rem; }
    .container { padding: 0 1.25rem; }
    .hero { padding: 3.5rem 0 2.5rem; }
    section { padding: 3rem 0; }
  }
</style>
</head>
<body>

<nav>
  <span class="nav-logo">Shravan Timalsina</span>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<div class="container">

  <section class="hero" id="hero">
    <p class="hero-eyebrow">Electrical Engineering · UT Arlington</p>
    <h1>Building circuits,<br><em>robots, and systems.</em></h1>
    <p class="hero-desc">I'm Shravan, an EE student at UT Arlington (class of 2029) with hands-on experience in embedded systems, circuit design, CAD, and robotics. Passionate about hardware-software integration.</p>
    <div class="hero-btns">
      <a href="#projects" class="btn btn-primary">View my work</a>
      <a href="#contact" class="btn">Get in touch</a>
    </div>
  </section>

  <hr class="divider">

  <section id="about">
    <p class="section-label">About</p>
    <div class="about-text">
      <p>I'm studying Electrical Engineering at the University of Texas at Arlington, expected to graduate in May 2029. My work spans analog and digital circuit design, embedded systems with ESP32, and mechanical CAD using Fusion 360.</p>
      <p>I'm an active member of IEEE, IEEE GRSS, and an intern with the SASE UTA chapter — always looking for opportunities to collaborate and grow as an engineer.</p>
    </div>
    <div class="skills-row">
      <span class="skill-pill">Python</span>
      <span class="skill-pill">C/C++</span>
      <span class="skill-pill">Java</span>
      <span class="skill-pill">Circuit Analysis</span>
      <span class="skill-pill">ESP32</span>
      <span class="skill-pill">Multisim</span>
      <span class="skill-pill">LabVIEW</span>
      <span class="skill-pill">Fusion 360</span>
      <span class="skill-pill">KiCad</span>
      <span class="skill-pill">Microsoft Excel</span>
    </div>
  </section>

  <hr class="divider">

  <section id="projects">
    <p class="section-label">Projects</p>
    <div class="projects-grid">

      <div class="project-card">
        <div class="project-top">
          <div class="project-name">Hand-Controlled Robot — SASE RIG</div>
          <span class="project-tag">Ongoing</span>
        </div>
        <div class="project-desc">Part of the electrical team for SASE's Robotics Interest Group. Working on the robot-side electrical system using an ESP32 microcontroller — including wiring, power distribution planning, and ensuring the electrical design aligns with the overall system architecture.</div>
        <div class="project-stack">
          <span class="stack-pill">ESP32</span>
          <span class="stack-pill">Embedded Systems</span>
          <span class="stack-pill">Power Distribution</span>
          <span class="stack-pill">Sensors & Motors</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-top">
          <div class="project-name">FTC Robotics — CAD & Mechanical</div>
          <span class="project-tag">Team project</span>
        </div>
        <div class="project-desc">Designed robot components in Fusion 360 with a focus on size constraints and manufacturability. Assisted in mechanical assembly of the drivetrain and claw mechanisms, and collaborated with teammates to troubleshoot integration issues.</div>
        <div class="project-stack">
          <span class="stack-pill">Fusion 360</span>
          <span class="stack-pill">CAD</span>
          <span class="stack-pill">Mechanical Assembly</span>
          <span class="stack-pill">FTC Robotics</span>
        </div>
      </div>

    </div>
  </section>

  <hr class="divider">

  <section id="contact">
    <p class="section-label">Contact</p>
    <p class="contact-desc">I'm always open to new opportunities, collaborations, or just a conversation about engineering and robotics. Feel free to reach out!</p>
    <div class="contact-links">
      <a class="contact-link" href="mailto:shravantimalsina18@gmail.com">
        <svg class="contact-icon" viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="1.5"><rect x="1" y="3" width="14" height="10" rx="1.5"/><path d="M1 4l7 5 7-5"/></svg>
        shravantimalsina18@gmail.com
      </a>
      <a class="contact-link" href="https://linkedin.com/in/shravan-timalsina" target="_blank">
        <svg class="contact-icon" viewBox="0 0 16 16" fill="currentColor"><path d="M2 1a1 1 0 100 2 1 1 0 000-2zM1 4h2v8H1zm4 0h2v1.1C7.4 4.5 8 4 9 4c2 0 3 1.3 3 3.2V12h-2V7.5c0-.9-.4-1.5-1.2-1.5-.9 0-1.4.6-1.4 1.5V12H5V4z"/></svg>
        linkedin.com/in/shravan-timalsina
      </a>
      <a class="contact-link" href="tel:6823339182">
        <svg class="contact-icon" viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M2 2h3.5l1 3-1.5 1.5a9 9 0 003.5 3.5L10 8.5l3 1V13A1 1 0 0112 14C6.477 14 2 9.523 2 4a1 1 0 011-1z"/></svg>
        682-333-9182
      </a>
    </div>
  </section>

</div>

<footer>
  <span>Shravan Timalsina</span>
  <span>UTA Electrical Engineering · 2029</span>
</footer>

</body>
</html>
