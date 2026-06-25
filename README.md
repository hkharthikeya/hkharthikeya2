<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Hruthwik Kharthikeya — Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet" />
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css" />
  <style>
    :root {
      --bg: #0d0f14;
      --bg-card: #13161e;
      --bg-card2: #181c25;
      --border: rgba(255,255,255,0.07);
      --border-accent: rgba(56,189,248,0.3);
      --text: #e8eaf0;
      --text-muted: #7a8090;
      --text-dim: #4a5060;
      --accent: #38bdf8;
      --accent-dim: rgba(56,189,248,0.12);
      --green: #34d399;
      --amber: #fbbf24;
      --purple: #a78bfa;
      --coral: #fb7185;
      --font: 'Inter', system-ui, sans-serif;
      --mono: 'JetBrains Mono', monospace;
      --radius: 10px;
      --radius-lg: 14px;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: var(--font);
      font-size: 15px;
      line-height: 1.65;
      min-height: 100vh;
    }

    /* ── Layout ── */
    .container {
      max-width: 860px;
      margin: 0 auto;
      padding: 0 24px;
    }

    /* ── Nav ── */
    nav {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(13,15,20,0.85);
      backdrop-filter: blur(12px);
      border-bottom: 0.5px solid var(--border);
      padding: 14px 24px;
    }
    nav .inner {
      max-width: 860px;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .nav-logo {
      font-family: var(--mono);
      font-size: 13px;
      color: var(--accent);
      letter-spacing: 0.04em;
    }
    .nav-links {
      display: flex;
      gap: 24px;
      list-style: none;
    }
    .nav-links a {
      font-size: 13px;
      color: var(--text-muted);
      text-decoration: none;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--text); }

    /* ── Hero ── */
    .hero {
      padding: 80px 0 64px;
      border-bottom: 0.5px solid var(--border);
    }
    .hero-eyebrow {
      font-family: var(--mono);
      font-size: 12px;
      color: var(--accent);
      letter-spacing: 0.1em;
      text-transform: uppercase;
      margin-bottom: 18px;
    }
    .hero-name {
      font-size: clamp(32px, 5vw, 52px);
      font-weight: 600;
      letter-spacing: -1px;
      line-height: 1.1;
      color: var(--text);
    }
    .hero-name span { color: var(--accent); }
    .hero-tagline {
      font-size: 16px;
      color: var(--text-muted);
      margin-top: 14px;
      max-width: 560px;
      line-height: 1.7;
    }
    .badge-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 24px;
    }
    .badge {
      display: inline-flex;
      align-items: center;
      gap: 5px;
      font-size: 12px;
      font-weight: 500;
      padding: 5px 12px;
      border-radius: 20px;
      border: 0.5px solid;
    }
    .badge-blue  { background: rgba(56,189,248,0.08); color: #7dd3fc; border-color: rgba(56,189,248,0.2); }
    .badge-green { background: rgba(52,211,153,0.08); color: #6ee7b7; border-color: rgba(52,211,153,0.2); }
    .badge-purple{ background: rgba(167,139,250,0.08); color: #c4b5fd; border-color: rgba(167,139,250,0.2); }
    .badge-amber { background: rgba(251,191,36,0.08); color: #fcd34d; border-color: rgba(251,191,36,0.2); }

    .hero-contact {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
      margin-top: 28px;
    }
    .contact-link {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      font-size: 13px;
      color: var(--text-muted);
      text-decoration: none;
      transition: color 0.2s;
    }
    .contact-link i { font-size: 16px; }
    .contact-link:hover { color: var(--accent); }

    /* ── Section ── */
    section {
      padding: 56px 0;
      border-bottom: 0.5px solid var(--border);
    }
    .section-label {
      font-family: var(--mono);
      font-size: 11px;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 28px;
    }

    /* ── Experience card ── */
    .exp-card {
      background: var(--bg-card);
      border: 0.5px solid var(--border);
      border-left: 2px solid var(--accent);
      border-radius: var(--radius-lg);
      padding: 20px 22px;
    }
    .exp-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 4px;
    }
    .exp-title { font-size: 15px; font-weight: 600; color: var(--text); }
    .exp-org { font-size: 13px; color: var(--text-muted); margin-top: 2px; }
    .exp-date {
      font-family: var(--mono);
      font-size: 11px;
      color: var(--accent);
      background: var(--accent-dim);
      padding: 3px 10px;
      border-radius: 20px;
      white-space: nowrap;
    }
    .exp-desc { font-size: 13px; color: var(--text-muted); margin-top: 10px; line-height: 1.7; }

    /* ── Boards grid ── */
    .boards-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
      gap: 12px;
    }
    .board-card {
      background: var(--bg-card);
      border: 0.5px solid var(--border);
      border-radius: var(--radius-lg);
      padding: 18px 14px;
      text-align: center;
      transition: border-color 0.2s, transform 0.2s;
    }
    .board-card:hover {
      border-color: var(--border-accent);
      transform: translateY(-2px);
    }
    .board-icon { font-size: 26px; color: var(--accent); margin-bottom: 8px; }
    .board-name { font-size: 13px; font-weight: 600; color: var(--text); }
    .board-sub { font-size: 11px; color: var(--text-muted); margin-top: 3px; font-family: var(--mono); }

    /* ── Projects ── */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(360px, 1fr));
      gap: 14px;
    }
    .project-card {
      background: var(--bg-card);
      border: 0.5px solid var(--border);
      border-radius: var(--radius-lg);
      padding: 20px 22px;
      transition: border-color 0.2s;
    }
    .project-card:hover { border-color: var(--border-accent); }
    .project-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 8px;
      margin-bottom: 8px;
    }
    .project-title { font-size: 14px; font-weight: 600; color: var(--text); }
    .project-live {
      font-size: 11px;
      color: var(--green);
      background: rgba(52,211,153,0.1);
      padding: 2px 8px;
      border-radius: 12px;
      white-space: nowrap;
    }
    .project-desc { font-size: 13px; color: var(--text-muted); line-height: 1.65; }
    .tag-row { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 14px; }
    .tag {
      font-family: var(--mono);
      font-size: 11px;
      padding: 3px 9px;
      background: var(--bg-card2);
      color: var(--text-dim);
      border-radius: 6px;
      border: 0.5px solid var(--border);
    }

    /* ── Skills ── */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
      gap: 12px;
    }
    .skill-block {
      background: var(--bg-card);
      border: 0.5px solid var(--border);
      border-radius: var(--radius);
      padding: 14px 16px;
    }
    .skill-cat {
      font-family: var(--mono);
      font-size: 11px;
      color: var(--text-dim);
      letter-spacing: 0.06em;
      text-transform: uppercase;
      margin-bottom: 10px;
    }
    .skill-tags { display: flex; flex-wrap: wrap; gap: 5px; }
    .skill-tag {
      font-size: 12px;
      padding: 3px 9px;
      background: var(--bg-card2);
      color: var(--text-muted);
      border-radius: 6px;
      border: 0.5px solid var(--border);
    }

    /* ── Achievements ── */
    .ach-list { display: flex; flex-direction: column; gap: 14px; }
    .ach-item {
      display: flex;
      gap: 14px;
      align-items: flex-start;
      background: var(--bg-card);
      border: 0.5px solid var(--border);
      border-radius: var(--radius);
      padding: 16px 18px;
    }
    .ach-icon { font-size: 20px; color: var(--amber); flex-shrink: 0; margin-top: 1px; }
    .ach-title { font-size: 14px; font-weight: 500; color: var(--text); }
    .ach-sub { font-size: 12px; color: var(--text-muted); margin-top: 2px; }

    /* ── Leadership ── */
    .lead-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
      gap: 12px;
    }

    /* ── Certs ── */
    .cert-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }
    .cert-card {
      background: var(--bg-card);
      border: 0.5px solid var(--border);
      border-radius: var(--radius);
      padding: 12px 16px;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .cert-card i { font-size: 18px; color: var(--purple); }
    .cert-name { font-size: 13px; font-weight: 500; color: var(--text); }
    .cert-year { font-size: 11px; color: var(--text-muted); margin-top: 1px; font-family: var(--mono); }

    /* ── Footer ── */
    footer {
      padding: 36px 0;
      text-align: center;
      font-size: 12px;
      color: var(--text-dim);
      font-family: var(--mono);
    }

    /* ── Responsive ── */
    @media (max-width: 600px) {
      .projects-grid { grid-template-columns: 1fr; }
      .lead-grid { grid-template-columns: 1fr; }
      nav .nav-links { display: none; }
      .hero { padding: 52px 0 40px; }
    }

    /* ── Scroll reveal ── */
    .reveal {
      opacity: 0;
      transform: translateY(16px);
      transition: opacity 0.5s ease, transform 0.5s ease;
    }
    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }
  </style>
</head>
<body>

<nav>
  <div class="inner">
    <span class="nav-logo">hruthwik.dev</span>
    <ul class="nav-links">
      <li><a href="#experience">Experience</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#achievements">Achievements</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>
</nav>

<div class="container">

  <!-- Hero -->
  <div class="hero reveal">
    <div class="hero-eyebrow">// Electronics & Communication Engineering</div>
    <h1 class="hero-name">Bhimavarapu<br><span>Hruthwik</span> Kharthikeya</h1>
    <p class="hero-tagline">
      Electronics student building IoT systems, autonomous drones, and computer vision tools.
      Currently interning at MCEME — Simulation Development Division, Hyderabad.
    </p>
    <div class="badge-row">
      <span class="badge badge-blue"><i class="ti ti-cpu"></i> Embedded Systems</span>
      <span class="badge badge-green"><i class="ti ti-drone"></i> Autonomous Drones</span>
      <span class="badge badge-purple"><i class="ti ti-eye"></i> Computer Vision</span>
      <span class="badge badge-amber"><i class="ti ti-building"></i> MCEME Intern (SDD)</span>
    </div>
    <div class="hero-contact" id="contact">
      <a href="mailto:bhruthwik536@gmail.com" class="contact-link">
        <i class="ti ti-mail"></i> bhruthwik536@gmail.com
      </a>
      <a href="tel:+919110544685" class="contact-link">
        <i class="ti ti-phone"></i> +91 9110544685
      </a>
      <a href="https://github.com/" target="_blank" rel="noopener" class="contact-link">
        <i class="ti ti-brand-github"></i> GitHub
      </a>
      <a href="https://linkedin.com/" target="_blank" rel="noopener" class="contact-link">
        <i class="ti ti-brand-linkedin"></i> LinkedIn
      </a>
      <span class="contact-link">
        <i class="ti ti-map-pin"></i> Hyderabad, India
      </span>
    </div>
  </div>

  <!-- Experience -->
  <section id="experience" class="reveal">
    <div class="section-label">// experience</div>
    <div class="exp-card">
      <div class="exp-header">
        <div>
          <div class="exp-title">Intern — Simulation Development Division (SDD)</div>
          <div class="exp-org">MCEME · Military College of Electronics &amp; Mechanical Engineering, Secunderabad</div>
        </div>
        <span class="exp-date">Current</span>
      </div>
      <p class="exp-desc">
        Working within the SDD on simulation systems, contributing electronics and embedded solutions
        for defence-grade training environments. Applying skills in embedded platforms, PCB design,
        and systems integration.
      </p>
    </div>
  </section>

  <!-- Education -->
  <section class="reveal">
    <div class="section-label">// education</div>
    <div style="display:flex;flex-direction:column;gap:12px">
      <div class="exp-card">
        <div class="exp-header">
          <div>
            <div class="exp-title">B.Tech — Electronics &amp; Communication Engineering</div>
            <div class="exp-org">CMR College of Engineering and Technology, Hyderabad</div>
          </div>
          <span class="exp-date">2024 – 2028</span>
        </div>
        <p class="exp-desc">CGPA: <strong style="color:var(--accent)">8.55 / 10</strong></p>
      </div>
      <div class="exp-card" style="border-left-color:var(--text-dim)">
        <div class="exp-header">
          <div>
            <div class="exp-title">Intermediate (MPC)</div>
            <div class="exp-org">SASI Junior College</div>
          </div>
          <span class="exp-date" style="color:var(--text-muted);background:var(--bg-card2)">2022 – 2024</span>
        </div>
        <p class="exp-desc">Score: 911 / 1000</p>
      </div>
    </div>
  </section>

  <!-- Hardware Boards -->
  <section class="reveal">
    <div class="section-label">// hardware boards</div>
    <div class="boards-grid">
      <div class="board-card">
        <div class="board-icon"><i class="ti ti-circuit-board"></i></div>
        <div class="board-name">Arduino</div>
        <div class="board-sub">Uno · Nano</div>
      </div>
      <div class="board-card">
        <div class="board-icon"><i class="ti ti-wifi"></i></div>
        <div class="board-name">ESP32</div>
        <div class="board-sub">Dev Module</div>
      </div>
      <div class="board-card">
        <div class="board-icon"><i class="ti ti-server"></i></div>
        <div class="board-name">Raspberry Pi</div>
        <div class="board-sub">3B+ · 4</div>
      </div>
      <div class="board-card">
        <div class="board-icon"><i class="ti ti-brain"></i></div>
        <div class="board-name">Jetson Orin</div>
        <div class="board-sub">Nano</div>
      </div>
      <div class="board-card">
        <div class="board-icon"><i class="ti ti-drone"></i></div>
        <div class="board-name">Pixhawk</div>
        <div class="board-sub">Flight Controller</div>
      </div>
    </div>
  </section>

  <!-- Projects -->
  <section id="projects" class="reveal">
    <div class="section-label">// projects</div>
    <div class="projects-grid">

      <div class="project-card">
        <div class="project-header">
          <div class="project-title">Trinetra — Autonomous Surveillance Drone</div>
          <span class="project-live">Ongoing</span>
        </div>
        <p class="project-desc">
          Pixhawk-based quadcopter with GPS autonomous navigation. Integrated live camera telemetry
          for stable real-time monitoring. Core initiative for accessible IoT security solutions.
        </p>
        <div class="tag-row">
          <span class="tag">Pixhawk</span>
          <span class="tag">GPS Nav</span>
          <span class="tag">Telemetry</span>
          <span class="tag">IoT Security</span>
          <span class="tag">ArduPilot</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-header">
          <div class="project-title">Suspicious Human Detection &amp; Tracking</div>
        </div>
        <p class="project-desc">
          YOLO-based real-time computer vision system for human detection and abnormal behaviour alerts.
          Built with Python and OpenCV for live surveillance monitoring on Jetson Orin Nano.
        </p>
        <div class="tag-row">
          <span class="tag">YOLO</span>
          <span class="tag">Python</span>
          <span class="tag">OpenCV</span>
          <span class="tag">Jetson Orin Nano</span>
          <span class="tag">CV</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-header">
          <div class="project-title">Niyantra — Zone-Based Speed Limiting</div>
        </div>
        <p class="project-desc">
          ESP32-based vehicle speed control system using PWM and L298N motor driver for smart
          safe-zone enforcement. Bluetooth control with adaptive speed regulation.
        </p>
        <div class="tag-row">
          <span class="tag">ESP32</span>
          <span class="tag">PWM</span>
          <span class="tag">L298N</span>
          <span class="tag">Bluetooth</span>
          <span class="tag">Embedded C</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-header">
          <div class="project-title">Smart Garbage Monitoring System</div>
        </div>
        <p class="project-desc">
          IoT waste management using ESP32 and ultrasonic sensors for real-time bin monitoring.
          Data-driven scheduling and automated alerts to optimise garbage collection routes.
        </p>
        <div class="tag-row">
          <span class="tag">ESP32</span>
          <span class="tag">Ultrasonic</span>
          <span class="tag">Firebase</span>
          <span class="tag">IoT</span>
          <span class="tag">Docker</span>
        </div>
      </div>

    </div>
  </section>

  <!-- Skills -->
  <section id="skills" class="reveal">
    <div class="section-label">// technical skills</div>
    <div class="skills-grid">
      <div class="skill-block">
        <div class="skill-cat">Programming</div>
        <div class="skill-tags">
          <span class="skill-tag">C</span>
          <span class="skill-tag">C++</span>
          <span class="skill-tag">Python</span>
          <span class="skill-tag">HTML</span>
        </div>
      </div>
      <div class="skill-block">
        <div class="skill-cat">IoT & Embedded</div>
        <div class="skill-tags">
          <span class="skill-tag">Arduino</span>
          <span class="skill-tag">ESP32</span>
          <span class="skill-tag">Raspberry Pi</span>
          <span class="skill-tag">Pixhawk</span>
          <span class="skill-tag">Jetson Orin</span>
        </div>
      </div>
      <div class="skill-block">
        <div class="skill-cat">Cloud & Infra</div>
        <div class="skill-tags">
          <span class="skill-tag">Firebase</span>
          <span class="skill-tag">Docker</span>
          <span class="skill-tag">Git</span>
          <span class="skill-tag">GitHub</span>
        </div>
      </div>
      <div class="skill-block">
        <div class="skill-cat">Design & Tools</div>
        <div class="skill-tags">
          <span class="skill-tag">KiCad</span>
          <span class="skill-tag">AutoCAD</span>
          <span class="skill-tag">LaTeX</span>
          <span class="skill-tag">DaVinci Resolve</span>
          <span class="skill-tag">VS Code</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Achievements -->
  <section id="achievements" class="reveal">
    <div class="section-label">// achievements</div>
    <div class="ach-list">
      <div class="ach-item">
        <i class="ti ti-trophy ach-icon"></i>
        <div>
          <div class="ach-title">4th Place — Gist 2K26 National Hackathon</div>
          <div class="ach-sub">Sreenidhi Institute of Science and Technology (SNIST)</div>
        </div>
      </div>
      <div class="ach-item">
        <i class="ti ti-medal ach-icon"></i>
        <div>
          <div class="ach-title">5th Place — Forge Inspira</div>
          <div class="ach-sub">Indian Institute(s) of Technology (IIT)</div>
        </div>
      </div>
      <div class="ach-item">
        <i class="ti ti-tournament ach-icon"></i>
        <div>
          <div class="ach-title">10+ Hackathons &amp; Technical Competitions</div>
          <div class="ach-sub">Active national-level competitor since 2024</div>
        </div>
      </div>
    </div>
  </section>

  <!-- Leadership -->
  <section class="reveal">
    <div class="section-label">// leadership</div>
    <div class="lead-grid">
      <div class="exp-card" style="border-left-color:var(--purple)">
        <div class="exp-header">
          <div>
            <div class="exp-title">Coordinator — Circutronix 2026</div>
            <div class="exp-org">CMR College of Engineering and Technology</div>
          </div>
          <span class="exp-date" style="color:var(--purple);background:rgba(167,139,250,0.1)">2026</span>
        </div>
        <p class="exp-desc">Assisted 35 teams with circuit design and technical problem solving, ensuring the event ran smoothly and on schedule.</p>
      </div>
      <div class="exp-card" style="border-left-color:var(--green)">
        <div class="exp-header">
          <div>
            <div class="exp-title">Coordinator — Azura 2026</div>
            <div class="exp-org">CMR College of Engineering and Technology</div>
          </div>
          <span class="exp-date" style="color:var(--green);background:rgba(52,211,153,0.1)">2026</span>
        </div>
        <p class="exp-desc">Assisted 45 teams with architecture decisions, debugging, and technical problem solving across the event.</p>
      </div>
    </div>
  </section>

  <!-- Certifications -->
  <section class="reveal">
    <div class="section-label">// certifications</div>
    <div class="cert-grid">
      <div class="cert-card">
        <i class="ti ti-circuit-board"></i>
        <div>
          <div class="cert-name">PCB Design</div>
          <div class="cert-year">2023</div>
        </div>
      </div>
      <div class="cert-card">
        <i class="ti ti-robot"></i>
        <div>
          <div class="cert-name">Robotics</div>
          <div class="cert-year">2023</div>
        </div>
      </div>
      <div class="cert-card">
        <i class="ti ti-language"></i>
        <div>
          <div class="cert-name">Cambridge English Upskill — B1</div>
          <div class="cert-year">English Proficiency</div>
        </div>
      </div>
    </div>
  </section>

</div><!-- /container -->

<footer>
  <div>Bhimavarapu Hruthwik Kharthikeya · Hyderabad, India · bhruthwik536@gmail.com</div>
  <div style="margin-top:6px;color:var(--text-dim)">Built with HTML · CSS · &lt;3</div>
</footer>

<script>
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.08 });
  reveals.forEach(el => observer.observe(el));
</script>

</body>
</html>
