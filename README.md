<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Suhar Yaseen — Full Stack Developer & Business Analyst</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0d0d0f;
    --bg2: #141417;
    --bg3: #1c1c21;
    --border: rgba(255,255,255,0.07);
    --border2: rgba(255,255,255,0.13);
    --text: #f0eeff;
    --muted: #888891;
    --dim: #555560;
    --accent: #7c6ff7;
    --accent2: #a89df8;
    --teal: #3dd6ac;
    --amber: #f5b843;
    --coral: #f07060;
    --green: #5ecf7a;
    --font: 'Syne', sans-serif;
    --mono: 'DM Mono', monospace;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: var(--font);
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
    padding: 2.5rem 1.5rem 4rem;
  }

  .container {
    max-width: 820px;
    margin: 0 auto;
  }

  /* ---- HERO ---- */
  .hero {
    position: relative;
    border: 1px solid var(--border2);
    border-radius: 20px;
    padding: 3rem 2.5rem 2.5rem;
    margin-bottom: 1.25rem;
    overflow: hidden;
    background: var(--bg2);
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -120px; right: -120px;
    width: 420px; height: 420px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(124,111,247,0.18) 0%, transparent 65%);
    pointer-events: none;
  }

  .hero::after {
    content: '';
    position: absolute;
    bottom: -80px; left: -60px;
    width: 280px; height: 280px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(61,214,172,0.08) 0%, transparent 65%);
    pointer-events: none;
  }

  .avatar {
    width: 72px; height: 72px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent), var(--teal));
    display: flex; align-items: center; justify-content: center;
    font-size: 26px; font-weight: 800;
    color: #fff;
    margin-bottom: 1.5rem;
    letter-spacing: -1px;
    position: relative; z-index: 1;
    flex-shrink: 0;
  }

  .hero-top {
    display: flex;
    align-items: center;
    gap: 1.25rem;
    margin-bottom: 1.5rem;
  }

  .hero-meta {
    position: relative; z-index: 1;
  }

  .wave { font-size: 28px; }

  .name {
    font-size: clamp(28px, 5vw, 40px);
    font-weight: 800;
    letter-spacing: -0.035em;
    line-height: 1.08;
    background: linear-gradient(100deg, #fff 40%, var(--accent2) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .role {
    font-size: 14px;
    color: var(--muted);
    margin-top: 4px;
    letter-spacing: 0.02em;
  }

  .role span {
    color: var(--teal);
    font-weight: 600;
  }

  .tagline {
    font-size: 15px;
    line-height: 1.7;
    color: #a9a9bb;
    max-width: 560px;
    margin-bottom: 1.75rem;
    position: relative; z-index: 1;
  }

  .tag-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 1.75rem;
    position: relative; z-index: 1;
  }

  .tag {
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.06em;
    padding: 5px 12px;
    border-radius: 99px;
    text-transform: uppercase;
  }

  .tag-purple { background: rgba(124,111,247,0.15); color: var(--accent2); border: 1px solid rgba(124,111,247,0.3); }
  .tag-teal   { background: rgba(61,214,172,0.12);  color: var(--teal);    border: 1px solid rgba(61,214,172,0.25); }
  .tag-amber  { background: rgba(245,184,67,0.12);  color: var(--amber);   border: 1px solid rgba(245,184,67,0.25); }

  .social-row {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    position: relative; z-index: 1;
  }

  .social-btn {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    font-size: 13px;
    font-weight: 600;
    padding: 8px 16px;
    border-radius: 10px;
    text-decoration: none;
    transition: all 0.18s ease;
    border: 1px solid var(--border2);
    background: var(--bg3);
    color: var(--text);
  }

  .social-btn:hover {
    border-color: var(--accent);
    color: var(--accent2);
    background: rgba(124,111,247,0.08);
    transform: translateY(-1px);
  }

  .social-btn svg { flex-shrink: 0; }

  /* ---- STATS ---- */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
    margin-bottom: 1.25rem;
  }

  .stat {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 1.1rem 1rem;
    text-align: center;
    transition: border-color 0.2s;
  }

  .stat:hover { border-color: var(--border2); }

  .stat-num {
    font-size: 24px;
    font-weight: 800;
    letter-spacing: -0.03em;
  }

  .stat-num.c1 { color: var(--accent2); }
  .stat-num.c2 { color: var(--teal); }
  .stat-num.c3 { color: var(--amber); }
  .stat-num.c4 { color: var(--coral); }

  .stat-lbl {
    font-size: 11px;
    color: var(--dim);
    letter-spacing: 0.06em;
    text-transform: uppercase;
    margin-top: 3px;
  }

  /* ---- SKILL SECTION ---- */
  .section-title {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--dim);
    margin-bottom: 12px;
  }

  .grid-2 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    margin-bottom: 10px;
  }

  .skill-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 1.2rem 1.25rem;
    transition: border-color 0.2s, transform 0.2s;
  }

  .skill-card:hover {
    border-color: var(--border2);
    transform: translateY(-2px);
  }

  .skill-card-title {
    font-size: 13px;
    font-weight: 700;
    color: var(--muted);
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    gap: 7px;
  }

  .card-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    display: inline-block;
    flex-shrink: 0;
  }

  .dot-purple { background: var(--accent); }
  .dot-teal   { background: var(--teal); }
  .dot-amber  { background: var(--amber); }
  .dot-coral  { background: var(--coral); }

  .chips {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  .chip {
    font-family: var(--mono);
    font-size: 11.5px;
    padding: 4px 10px;
    border-radius: 6px;
    background: var(--bg3);
    border: 1px solid var(--border);
    color: var(--muted);
    transition: all 0.15s;
  }

  .chip:hover { border-color: var(--border2); color: var(--text); }

  .chip.p { background: rgba(124,111,247,0.1); border-color: rgba(124,111,247,0.2); color: var(--accent2); }
  .chip.t { background: rgba(61,214,172,0.08); border-color: rgba(61,214,172,0.2);  color: var(--teal); }
  .chip.a { background: rgba(245,184,67,0.08); border-color: rgba(245,184,67,0.2);  color: var(--amber); }
  .chip.r { background: rgba(240,112,96,0.08); border-color: rgba(240,112,96,0.2);  color: var(--coral); }

  /* ---- GITHUB STATS ---- */
  .github-section {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 1.5rem;
    margin-bottom: 10px;
  }

  .stats-imgs {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    margin-top: 12px;
  }

  .stats-imgs img {
    width: 100%;
    border-radius: 10px;
    display: block;
  }

  .stats-imgs .full {
    grid-column: 1 / -1;
  }

  /* ---- PROFILE VIEWS ---- */
  .profile-views {
    text-align: center;
    padding: 1rem;
    font-size: 13px;
    color: var(--dim);
  }

  .profile-views img { vertical-align: middle; margin-left: 6px; }

  /* ---- FOOTER ---- */
  .footer {
    margin-top: 2rem;
    text-align: center;
    font-size: 12px;
    color: var(--dim);
    letter-spacing: 0.04em;
  }

  .footer span { color: var(--accent); }

  /* ---- ANIMATIONS ---- */
  @keyframes fadein {
    from { opacity: 0; transform: translateY(14px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .hero        { animation: fadein 0.5s ease both; }
  .stats-row   { animation: fadein 0.5s 0.1s ease both; }
  .grid-2      { animation: fadein 0.5s 0.2s ease both; }
  .github-section { animation: fadein 0.5s 0.3s ease both; }

  /* ---- RESPONSIVE ---- */
  @media (max-width: 600px) {
    .stats-row { grid-template-columns: repeat(2, 1fr); }
    .grid-2    { grid-template-columns: 1fr; }
    .stats-imgs { grid-template-columns: 1fr; }
    .hero { padding: 2rem 1.5rem 2rem; }
    .hero-top { flex-direction: column; gap: 0.75rem; align-items: flex-start; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-top">
      <div class="avatar">SY</div>
      <div class="hero-meta">
        <div class="name">Suhar Yaseen <span class="wave">👋</span></div>
        <div class="role"><span>Full Stack Developer</span> · Business Analyst · India 🇮🇳</div>
      </div>
    </div>

    <p class="tagline">
      Passionate about building end-to-end digital products — clean APIs, scalable backends, and polished frontends.
      I bridge the gap between engineering and business strategy, turning complex requirements into real solutions.
    </p>

    <div class="tag-row">
      <span class="tag tag-purple">Full Stack Dev</span>
      <span class="tag tag-teal">Business Analyst</span>
      <span class="tag tag-amber">Open to Collaborate</span>
    </div>

    <div class="social-row">
      <a class="social-btn" href="mailto:Suharyaseen36@gmail.com">
        <svg width="15" height="15" viewBox="0 0 16 16" fill="none"><rect x="1" y="3" width="14" height="10" rx="2" stroke="currentColor" stroke-width="1.3"/><path d="M1 5.5l7 4.5 7-4.5" stroke="currentColor" stroke-width="1.3" stroke-linejoin="round"/></svg>
        Suharyaseen36@gmail.com
      </a>
      <a class="social-btn" href="https://twitter.com/suhar_yaseen" target="_blank">
        <svg width="15" height="15" viewBox="0 0 16 16" fill="currentColor"><path d="M13.5 2h-2.3L8 6.1 5.1 2H1.5l4.7 6.6L1.5 14H3.8l3.2-4.4L10.2 14h3.5l-5-6.9L13.5 2z"/></svg>
        @suhar_yaseen
      </a>
      <a class="social-btn" href="https://linkedin.com/in/suhar-yaseen-b525bb2b1" target="_blank">
        <svg width="15" height="15" viewBox="0 0 16 16" fill="currentColor"><path d="M2.5 5h2V13h-2V5zm1-3.5a1.25 1.25 0 110 2.5 1.25 1.25 0 010-2.5zM5.5 5h1.9v1.1h.02C7.77 5.5 8.72 5 10 5c2.2 0 2.6 1.45 2.6 3.33V13h-2V8.75c0-.75-.01-1.7-1.05-1.7-1.05 0-1.21.82-1.21 1.65V13H6.5V5z"/></svg>
        LinkedIn
      </a>
      <a class="social-btn" href="https://instagram.com/suharyaseen_" target="_blank">
        <svg width="15" height="15" viewBox="0 0 16 16" fill="none"><rect x="2" y="2" width="12" height="12" rx="3.5" stroke="currentColor" stroke-width="1.3"/><circle cx="8" cy="8" r="2.8" stroke="currentColor" stroke-width="1.3"/><circle cx="11.5" cy="4.5" r="0.85" fill="currentColor"/></svg>
        @suharyaseen_
      </a>
    </div>
  </div>

  <!-- STATS -->
  <div class="stats-row">
    <div class="stat">
      <div class="stat-num c1">50+</div>
      <div class="stat-lbl">Technologies</div>
    </div>
    <div class="stat">
      <div class="stat-num c2">Full</div>
      <div class="stat-lbl">Stack</div>
    </div>
    <div class="stat">
      <div class="stat-num c3">ML</div>
      <div class="stat-lbl">& AI Tools</div>
    </div>
    <div class="stat">
      <div class="stat-num c4">∞</div>
      <div class="stat-lbl">Curiosity</div>
    </div>
  </div>

  <!-- SKILLS GRID -->
  <div class="grid-2">
    <div class="skill-card">
      <div class="skill-card-title"><span class="card-dot dot-purple"></span>Frontend</div>
      <div class="chips">
        <span class="chip p">React</span>
        <span class="chip p">Next.js</span>
        <span class="chip p">Vue</span>
        <span class="chip p">React Native</span>
        <span class="chip">TypeScript</span>
        <span class="chip">Tailwind CSS</span>
        <span class="chip">Redux</span>
        <span class="chip">Bootstrap</span>
        <span class="chip">Figma</span>
        <span class="chip">Framer</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-card-title"><span class="card-dot dot-teal"></span>Backend & Infra</div>
      <div class="chips">
        <span class="chip t">Node.js</span>
        <span class="chip t">NestJS</span>
        <span class="chip t">Express</span>
        <span class="chip t">GraphQL</span>
        <span class="chip">Docker</span>
        <span class="chip">Kubernetes</span>
        <span class="chip">Jenkins</span>
        <span class="chip">Nginx</span>
        <span class="chip">AWS</span>
        <span class="chip">GCP</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-card-title"><span class="card-dot dot-amber"></span>Data & ML</div>
      <div class="chips">
        <span class="chip a">Python</span>
        <span class="chip a">TensorFlow</span>
        <span class="chip a">PyTorch</span>
        <span class="chip a">scikit-learn</span>
        <span class="chip">Pandas</span>
        <span class="chip">OpenCV</span>
        <span class="chip">Seaborn</span>
        <span class="chip">Hadoop</span>
        <span class="chip">Kafka</span>
        <span class="chip">Grafana</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-card-title"><span class="card-dot dot-coral"></span>Databases & Tools</div>
      <div class="chips">
        <span class="chip r">MongoDB</span>
        <span class="chip r">PostgreSQL</span>
        <span class="chip r">MySQL</span>
        <span class="chip r">Redis</span>
        <span class="chip">Cassandra</span>
        <span class="chip">Oracle</span>
        <span class="chip">SQLite</span>
        <span class="chip">Postman</span>
        <span class="chip">Git</span>
        <span class="chip">Linux</span>
      </div>
    </div>
  </div>

  <!-- ALSO: Creative Tools -->
  <div class="skill-card" style="margin-bottom:10px;">
    <div class="skill-card-title"><span class="card-dot" style="background:#a89df8"></span>Creative & Other</div>
    <div class="chips">
      <span class="chip">Blender</span>
      <span class="chip">Unreal Engine</span>
      <span class="chip">Photoshop</span>
      <span class="chip">Chart.js</span>
      <span class="chip">Arduino</span>
      <span class="chip">C / C++</span>
      <span class="chip">Bash</span>
    </div>
  </div>

  <!-- GITHUB STATS -->
  <div class="github-section">
    <div class="section-title">GitHub Activity</div>
    <div class="stats-imgs">
      <img src="https://github-readme-stats.vercel.app/api?username=suhar121&show_icons=true&theme=tokyonight&hide_border=true&bg_color=141417&title_color=7c6ff7&icon_color=3dd6ac&text_color=a9a9bb&border_radius=10" alt="GitHub Stats" />
      <img src="https://github-readme-stats.vercel.app/api/top-langs?username=suhar121&layout=compact&theme=tokyonight&hide_border=true&bg_color=141417&title_color=7c6ff7&text_color=a9a9bb&border_radius=10" alt="Top Languages" />
      <img class="full" src="https://github-readme-streak-stats.herokuapp.com/?user=suhar121&theme=tokyonight&hide_border=true&background=141417&ring=7c6ff7&fire=f5b843&currStreakLabel=a89df8&sideLabels=888891&dates=555560&border_radius=10" alt="GitHub Streak" />
    </div>
  </div>

  <!-- PROFILE VIEWS -->
  <div class="profile-views">
    Profile views
    <img src="https://komarev.com/ghpvc/?username=suhar121&label=&color=7c6ff7&style=flat" alt="views" />
  </div>

  <div class="footer">
    Built with code &amp; curiosity · <span>Open to collaborations</span> · Reach me at Suharyaseen36@gmail.com
  </div>

</div>
</body>
</html>
