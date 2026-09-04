# poortfolio
personal
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chheang Sivly — Software Developer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #10121B;
    --bg-raised: #171A26;
    --bg-raised-2: #1E2233;
    --border: #2A2F45;
    --text: #E7E6ED;
    --text-muted: #8B90A8;
    --accent: #5EEAD4;
    --accent-dim: #3A6E68;
    --amber: #F0A857;

    --font-display: 'Space Grotesk', sans-serif;
    --font-body: 'Inter', sans-serif;
    --font-mono: 'JetBrains Mono', monospace;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--font-body);
    line-height: 1.6;
    background-image:
      radial-gradient(circle at 1px 1px, rgba(94, 234, 212, 0.07) 1px, transparent 0);
    background-size: 28px 28px;
  }

  a { color: inherit; text-decoration: none; }

  ::selection { background: var(--accent); color: #0A0B10; }

  :focus-visible {
    outline: 2px solid var(--accent);
    outline-offset: 3px;
  }

  .wrap {
    max-width: 880px;
    margin: 0 auto;
    padding: 0 28px;
  }

  header {
    position: sticky;
    top: 0;
    z-index: 10;
    background: rgba(16, 18, 27, 0.85);
    backdrop-filter: blur(8px);
    border-bottom: 1px solid var(--border);
  }

  nav {
    max-width: 880px;
    margin: 0 auto;
    padding: 18px 28px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    font-family: var(--font-display);
    font-weight: 600;
    font-size: 1.05rem;
    letter-spacing: -0.01em;
  }

  .logo span { color: var(--accent); }

  .nav-links {
    display: flex;
    gap: 28px;
    list-style: none;
  }

  .nav-links a {
    font-size: 0.92rem;
    color: var(--text-muted);
    position: relative;
    padding-bottom: 3px;
    transition: color 0.15s ease;
  }

  .nav-links a:hover { color: var(--text); }

  .nav-links a::after {
    content: '';
    position: absolute;
    left: 0;
    bottom: -2px;
    width: 0;
    height: 1px;
    background: var(--accent);
    transition: width 0.2s ease;
  }

  .nav-links a:hover::after { width: 100%; }

  .hero {
    padding: 100px 0 80px;
    border-bottom: 1px solid var(--border);
  }

  .hero-kicker {
    font-family: var(--font-mono);
    font-size: 0.85rem;
    color: var(--accent);
    margin-bottom: 22px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .hero-kicker .dot {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 8px var(--accent);
  }

  .hero h1 {
    font-family: var(--font-display);
    font-weight: 700;
    font-size: clamp(2.6rem, 6vw, 4.2rem);
    line-height: 1.05;
    letter-spacing: -0.02em;
    color: #fff;
    max-width: 11ch;
  }

  .hero-role {
    margin-top: 22px;
    font-family: var(--font-mono);
    font-size: 1.15rem;
    color: var(--text-muted);
    height: 1.6em;
  }

  .hero-role .cursor {
    display: inline-block;
    width: 2px;
    height: 1.05em;
    background: var(--accent);
    margin-left: 2px;
    vertical-align: text-bottom;
    animation: blink 1s step-start infinite;
  }

  @keyframes blink { 50% { opacity: 0; } }

  .hero p.lede {
    margin-top: 26px;
    max-width: 54ch;
    color: var(--text-muted);
    font-size: 1.05rem;
  }

  .hero-cta {
    margin-top: 36px;
    display: flex;
    gap: 14px;
    flex-wrap: wrap;
  }

  .btn {
    font-family: var(--font-body);
    font-weight: 500;
    font-size: 0.92rem;
    padding: 12px 22px;
    border-radius: 6px;
    border: 1px solid transparent;
    cursor: pointer;
    transition: transform 0.15s ease, border-color 0.15s ease, background 0.15s ease;
  }

  .btn-primary {
    background: var(--accent);
    color: #0A0B10;
  }

  .btn-primary:hover { transform: translateY(-1px); }

  .btn-ghost {
    border-color: var(--border);
    color: var(--text);
    background: transparent;
  }

  .btn-ghost:hover { border-color: var(--accent); }

  section { padding: 76px 0; border-bottom: 1px solid var(--border); }
  section:last-of-type { border-bottom: none; }

  .section-head {
    display: flex;
    align-items: baseline;
    gap: 14px;
    margin-bottom: 40px;
  }

  .section-head .num {
    font-family: var(--font-mono);
    color: var(--accent-dim);
    font-size: 0.95rem;
  }

  .section-head h2 {
    font-family: var(--font-display);
    font-weight: 600;
    font-size: 1.6rem;
    color: #fff;
  }

  .about-grid {
    display: grid;
    grid-template-columns: 1.3fr 1fr;
    gap: 48px;
  }

  .about-grid p { color: var(--text-muted); margin-bottom: 16px; max-width: 56ch; }

  .facts {
    border-left: 1px solid var(--border);
    padding-left: 24px;
    display: flex;
    flex-direction: column;
    gap: 18px;
  }

  .fact-label {
    font-family: var(--font-mono);
    font-size: 0.78rem;
    color: var(--text-muted);
  }

  .fact-value { font-size: 0.98rem; margin-top: 3px; }

  .project {
    padding: 28px 0;
    border-top: 1px solid var(--border);
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 20px;
    align-items: start;
  }

  .project:first-of-type { border-top: none; }

  .project h3 {
    font-family: var(--font-display);
    font-size: 1.2rem;
    font-weight: 600;
    margin-bottom: 8px;
  }

  .project p {
    color: var(--text-muted);
    max-width: 56ch;
    font-size: 0.96rem;
  }

  .project-stack {
    margin-top: 12px;
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
  }

  .project-stack span {
    font-family: var(--font-mono);
    font-size: 0.75rem;
    color: var(--accent);
    background: var(--bg-raised-2);
    padding: 4px 9px;
    border-radius: 4px;
    border: 1px solid var(--border);
  }

  .project-link {
    font-size: 0.88rem;
    color: var(--text);
    border-bottom: 1px solid var(--border);
    white-space: nowrap;
    padding-bottom: 2px;
  }

  .project-link:hover { border-color: var(--accent); color: var(--accent); }

  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 28px;
  }

  .skill-group h4 {
    font-family: var(--font-mono);
    font-size: 0.82rem;
    color: var(--accent);
    margin-bottom: 12px;
    font-weight: 500;
  }

  .skill-group ul { list-style: none; display: flex; flex-direction: column; gap: 8px; }

  .skill-group li { color: var(--text-muted); font-size: 0.94rem; }

  .contact h2 {
    font-family: var(--font-display);
    font-size: clamp(2rem, 4.5vw, 2.8rem);
    font-weight: 700;
    color: #fff;
    max-width: 14ch;
    margin-bottom: 20px;
  }

  .contact p { color: var(--text-muted); max-width: 48ch; margin-bottom: 32px; }

  .contact-links {
    display: flex;
    gap: 26px;
    flex-wrap: wrap;
  }

  .contact-links a {
    font-family: var(--font-mono);
    font-size: 0.95rem;
    color: var(--text);
    border-bottom: 1px solid var(--border);
    padding-bottom: 2px;
  }

  .contact-links a:hover { color: var(--accent); border-color: var(--accent); }

  footer {
    padding: 28px 0 50px;
    text-align: center;
    color: var(--text-muted);
    font-size: 0.82rem;
  }

  @media (max-width: 680px) {
    .about-grid { grid-template-columns: 1fr; }
    .facts { border-left: none; border-top: 1px solid var(--border); padding-left: 0; padding-top: 20px; }
    .skills-grid { grid-template-columns: 1fr 1fr; }
    .project { grid-template-columns: 1fr; }
    .nav-links { gap: 16px; }
  }

  @media (max-width: 460px) {
    .skills-grid { grid-template-columns: 1fr; }
  }

  @media (prefers-reduced-motion: reduce) {
    html { scroll-behavior: auto; }
    .hero-role .cursor { animation: none; opacity: 1; }
  }
</style>
</head>
<body>

<header>
  <nav>
    <div class="logo">Sivly<span>.</span>dev</div>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>

<main class="wrap">

  <section class="hero">
    <div class="hero-kicker"><span class="dot"></span>Available for new projects</div>
    <h1>Chheang Sivly</h1>
    <div class="hero-role" id="heroRole"></div>
    <p class="lede">
      I build web applications end to end — from database schema to the pixel on screen —
      based in Phnom Penh, Cambodia.
    </p>
    <div class="hero-cta">
      <a class="btn btn-primary" href="#projects">View projects</a>
      <a class="btn btn-ghost" href="#contact">Get in touch</a>
    </div>
  </section>

  <section id="about">
    <div class="section-head"><span class="num">01</span><h2>About</h2></div>
    <div class="about-grid">
      <div>
        <p>
          I'm a software developer who enjoys turning ambiguous problems into working
          systems. Most of my time is spent in React and Node, but I'm comfortable moving
          across the stack — writing an API, shaping a database, or debugging a build
          pipeline at 1am.
        </p>
        <p>
          I care about code that the next person can actually read, and about shipping
          things that hold up once real users touch them. Replace this paragraph with
          your own story — what got you into development, and what you're looking for next.
        </p>
      </div>
      <div class="facts">
        <div>
          <div class="fact-label">LOCATION</div>
          <div class="fact-value">Phnom Penh, Cambodia</div>
        </div>
        <div>
          <div class="fact-label">FOCUS</div>
          <div class="fact-value">Full-stack web development</div>
        </div>
        <div>
          <div class="fact-label">CURRENTLY</div>
          <div class="fact-value">Open to new roles &amp; freelance work</div>
        </div>
      </div>
    </div>
  </section>

  <section id="projects">
    <div class="section-head"><span class="num">02</span><h2>Projects</h2></div>

    <div class="project">
      <div>
        <h3>Project Name One</h3>
        <p>One or two sentences on the problem this project solved and the part you
          were responsible for. Replace with a real project.</p>
        <div class="project-stack">
          <span>React</span><span>Node.js</span><span>PostgreSQL</span>
        </div>
      </div>
      <a class="project-link" href="#" target="_blank" rel="noopener">View project</a>
    </div>

    <div class="project">
      <div>
        <h3>Project Name Two</h3>
        <p>What it does, who it's for, and one detail that shows real engineering
          judgment — a tricky bug, a scaling decision, a tradeoff you made.</p>
        <div class="project-stack">
          <span>Next.js</span><span>TypeScript</span><span>Redis</span>
        </div>
      </div>
      <a class="project-link" href="#" target="_blank" rel="noopener">View project</a>
    </div>

    <div class="project">
      <div>
        <h3>Project Name Three</h3>
        <p>Keep this short — a hiring manager should be able to understand the project
          in five seconds and dig deeper only if it's relevant to them.</p>
        <div class="project-stack">
          <span>Python</span><span>FastAPI</span><span>Docker</span>
        </div>
      </div>
      <a class="project-link" href="#" target="_blank" rel="noopener">View project</a>
    </div>
  </section>

  <section id="skills">
    <div class="section-head"><span class="num">03</span><h2>Skills</h2></div>
    <div class="skills-grid">
      <div class="skill-group">
        <h4>LANGUAGES</h4>
        <ul>
          <li>JavaScript / TypeScript</li>
          <li>Python</li>
          <li>SQL</li>
        </ul>
      </div>
      <div class="skill-group">
        <h4>FRAMEWORKS</h4>
        <ul>
          <li>React / Next.js</li>
          <li>Node.js / Express</li>
          <li>FastAPI</li>
        </ul>
      </div>
      <div class="skill-group">
        <h4>TOOLS</h4>
        <ul>
          <li>PostgreSQL / Redis</li>
          <li>Docker</li>
          <li>Git &amp; CI/CD</li>
        </ul>
      </div>
    </div>
  </section>

  <section id="contact" class="contact">
    <div class="section-head"><span class="num">04</span><h2 style="font-family: var(--font-mono); font-size: 0.85rem; color: var(--accent); font-weight: 500;">Contact</h2></div>
    <h2>Let's build something together.</h2>
    <p>The fastest way to reach me is email. I'm also on GitHub and LinkedIn if you'd
      rather see the code first.</p>
    <div class="contact-links">
      <a href="mailto:sivly@example.com">sivly@example.com</a>
      <a href="https://github.com/" target="_blank" rel="noopener">GitHub</a>
      <a href="https://linkedin.com/" target="_blank" rel="noopener">LinkedIn</a>
    </div>
  </section>

</main>

<footer>© 2026 Chheang Sivly. Built with care in Phnom Penh.</footer>

<script>
  const roles = [
    "Full-Stack Developer",
    "React & Node.js",
    "Problem Solver",
    "Open-Source Contributor"
  ];
  const el = document.getElementById('heroRole');
  const reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

  if (reduceMotion) {
    el.textContent = roles[0];
  } else {
    let roleIdx = 0, charIdx = 0, deleting = false;

    function tick() {
      const current = roles[roleIdx];
      if (!deleting) {
        charIdx++;
        if (charIdx > current.length) { deleting = true; setTimeout(tick, 1400); return; }
      } else {
        charIdx--;
        if (charIdx < 0) { deleting = false; roleIdx = (roleIdx + 1) % roles.length; charIdx = 0; }
      }
      el.innerHTML = current.slice(0, charIdx) + '<span class="cursor"></span>';
      setTimeout(tick, deleting ? 35 : 65);
    }
    tick();
  }
</script>

</body>
</html>
