<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Vineet Pratap Singh · GitHub Profile</title>
  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">
  <!-- Font Awesome 6 (free) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0d1117;
      color: #e6edf3;
      font-family: 'Inter', sans-serif;
      display: flex;
      justify-content: center;
      padding: 2rem 1rem;
      min-height: 100vh;
      line-height: 1.6;
    }

    .container {
      max-width: 880px;
      width: 100%;
    }

    /* ----- HEADER / HERO ----- */
    .hero {
      text-align: center;
      padding: 2.5rem 0 2rem;
      border-bottom: 1px solid #30363d;
      margin-bottom: 2.5rem;
    }

    .hero h1 {
      font-size: 3.2rem;
      font-weight: 800;
      background: linear-gradient(135deg, #58a6ff, #f0883e, #f6a8d0);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      letter-spacing: -0.5px;
      margin-bottom: 0.35rem;
      animation: shimmer 4s ease-in-out infinite alternate;
    }

    @keyframes shimmer {
      0% { filter: hue-rotate(0deg); }
      100% { filter: hue-rotate(20deg); }
    }

    .hero .subhead {
      font-size: 1.1rem;
      font-weight: 500;
      color: #8b949e;
      letter-spacing: 0.3px;
      margin-bottom: 0.75rem;
    }

    .hero .subhead i {
      color: #f0883e;
      margin: 0 0.25rem;
    }

    /* typing SVG wrapper */
    .typing-wrapper {
      display: flex;
      justify-content: center;
      margin-top: 0.5rem;
    }

    .typing-wrapper svg {
      max-width: 100%;
      height: auto;
    }

    /* ----- BIO CARD (About) ----- */
    .bio-card {
      background: #161b22;
      border: 1px solid #30363d;
      border-radius: 16px;
      padding: 1.5rem 2rem;
      margin-bottom: 2.5rem;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 1.5rem;
      transition: border-color 0.25s, box-shadow 0.3s;
    }

    .bio-card:hover {
      border-color: #58a6ff;
      box-shadow: 0 8px 24px rgba(88, 166, 255, 0.08);
    }

    .bio-icon {
      font-size: 2.4rem;
      color: #58a6ff;
      background: #0d1117;
      width: 60px;
      height: 60px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      border: 1px solid #30363d;
      flex-shrink: 0;
    }

    .bio-text {
      flex: 1;
    }

    .bio-text strong {
      color: #f0f6fc;
      font-weight: 700;
    }

    .bio-text .highlight {
      color: #f0883e;
      font-weight: 600;
    }

    .bio-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-top: 0.5rem;
    }

    .bio-tags span {
      background: #21262d;
      padding: 0.2rem 0.8rem;
      border-radius: 20px;
      font-size: 0.75rem;
      font-weight: 600;
      color: #8b949e;
      border: 1px solid #30363d;
      letter-spacing: 0.2px;
    }

    .bio-tags span i {
      margin-right: 0.3rem;
      color: #58a6ff;
    }

    /* ----- SECTION TITLE ----- */
    .section-title {
      display: flex;
      align-items: center;
      gap: 0.75rem;
      font-size: 1.4rem;
      font-weight: 700;
      margin-bottom: 1.2rem;
      color: #f0f6fc;
      border-bottom: 1px solid #21262d;
      padding-bottom: 0.6rem;
    }

    .section-title i {
      color: #58a6ff;
      font-size: 1.3rem;
    }

    /* ----- TECH STACK (skill icons) ----- */
    .tech-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.6rem 1rem;
      background: #161b22;
      border: 1px solid #30363d;
      border-radius: 16px;
      padding: 1.8rem 1.5rem;
      margin-bottom: 2.5rem;
      transition: border-color 0.25s;
    }

    .tech-grid:hover {
      border-color: #58a6ff;
    }

    .tech-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.2rem;
      font-size: 0.7rem;
      font-weight: 600;
      color: #8b949e;
      letter-spacing: 0.3px;
    }

    .tech-item img {
      width: 44px;
      height: 44px;
      transition: transform 0.2s, filter 0.2s;
      filter: grayscale(0.15);
    }

    .tech-item:hover img {
      transform: translateY(-4px) scale(1.05);
      filter: grayscale(0);
    }

    .tech-item span {
      margin-top: 2px;
    }

    /* ----- STATS ROW (streak + activity graph) ----- */
    .stats-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.5rem;
      margin-bottom: 2.5rem;
    }

    .stat-card {
      background: #161b22;
      border: 1px solid #30363d;
      border-radius: 16px;
      padding: 1.2rem 1rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      transition: border-color 0.25s, transform 0.15s;
    }

    .stat-card:hover {
      border-color: #58a6ff;
      transform: scale(1.01);
    }

    .stat-card img {
      max-width: 100%;
      height: auto;
      border-radius: 8px;
    }

    .stat-card .stat-label {
      font-size: 0.7rem;
      font-weight: 600;
      color: #8b949e;
      text-transform: uppercase;
      letter-spacing: 0.4px;
      margin-bottom: 0.5rem;
    }

    /* ----- ACTIVITY GRAPH (full width) ----- */
    .graph-wrapper {
      background: #161b22;
      border: 1px solid #30363d;
      border-radius: 16px;
      padding: 1.2rem 1rem;
      margin-bottom: 2.5rem;
      transition: border-color 0.25s;
    }

    .graph-wrapper:hover {
      border-color: #58a6ff;
    }

    .graph-wrapper img {
      width: 100%;
      height: auto;
      border-radius: 8px;
      display: block;
    }

    /* ----- RESPONSIVE ----- */
    @media (max-width: 700px) {
      .hero h1 { font-size: 2.4rem; }
      .stats-grid { grid-template-columns: 1fr; }
      .bio-card { flex-direction: column; align-items: flex-start; }
      .bio-icon { width: 48px; height: 48px; font-size: 1.8rem; }
    }

    @media (max-width: 480px) {
      .hero h1 { font-size: 1.8rem; }
      .tech-item img { width: 36px; height: 36px; }
    }

    /* small extras */
    .text-muted { color: #8b949e; }
    .mt-2 { margin-top: 0.5rem; }

    /* animated pulse for icons */
    .pulse {
      animation: pulse 2s infinite;
    }
    @keyframes pulse {
      0% { opacity: 0.7; transform: scale(1); }
      50% { opacity: 1; transform: scale(1.05); }
      100% { opacity: 0.7; transform: scale(1); }
    }

    /* custom scroll */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: #0d1117; }
    ::-webkit-scrollbar-thumb { background: #30363d; border-radius: 10px; }
  </style>
</head>
<body>
<div class="container">

  <!-- ========== HERO ========== -->
  <div class="hero">
    <h1>Vineet Pratap Singh</h1>
    <p class="subhead">
      <i class="fas fa-graduation-cap"></i> B.Pharm Student ·
      <i class="fas fa-shield-alt"></i> Cybersecurity ·
      <i class="fas fa-code"></i> Software Development
    </p>
    <!-- Typing SVG (inline) with animation + gradient -->
    <div class="typing-wrapper">
      <svg width="500" height="50" viewBox="0 0 500 50" xmlns="http://www.w3.org/2000/svg">
        <style>
          @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
          }
          @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
          }
          .type-text {
            font-family: 'JetBrains Mono', monospace;
            font-size: 20px;
            font-weight: 600;
            fill: #58a6ff;
            animation: typing 3s steps(30, end) forwards;
            white-space: nowrap;
            overflow: hidden;
          }
          .cursor {
            font-family: 'JetBrains Mono', monospace;
            font-size: 22px;
            fill: #f0883e;
            animation: blink 0.8s step-end infinite;
          }
          .type-bg {
            fill: #0d1117;
          }
        </style>
        <rect class="type-bg" width="500" height="50" rx="8" />
        <text x="20" y="34" class="type-text">
          <tspan>Cybersecurity Enthusiast</tspan>
        </text>
        <text x="20" y="34" class="cursor" dy="-1">|</text>
        <!-- second line – we use a second text with delayed animation (simplified) -->
        <text x="20" y="34" class="type-text" style="animation-delay: 3.2s; fill: #f0883e;" dy="0">
          <tspan>Pharma Tech · Full Stack · Forensics</tspan>
        </text>
        <!-- hide the cursor after typing (just for demo) -->
      </svg>
    </div>
  </div>

  <!-- ========== ABOUT (Bio) ========== -->
  <div class="bio-card">
    <div class="bio-icon">
      <i class="fas fa-brain"></i>
    </div>
    <div class="bio-text">
      <strong>🧠 About</strong>
      <p style="margin-top: 0.2rem; color: #c9d1d9;">
        Focused on building <span class="highlight">secure healthcare systems</span> combining
        pharmaceutical sciences, cybersecurity, and software engineering.
      </p>
      <div class="bio-tags">
        <span><i class="fas fa-lock"></i> Ethical Hacking</span>
        <span><i class="fas fa-microscope"></i> Network Pharmacology</span>
        <span><i class="fas fa-database"></i> Full-Stack</span>
        <span><i class="fas fa-search"></i> Digital Forensics</span>
        <span><i class="fas fa-heartbeat"></i> Health Tech</span>
      </div>
    </div>
  </div>

  <!-- ========== TECH STACK ========== -->
  <div class="section-title">
    <i class="fas fa-cogs"></i> Tech Stack
  </div>
  <div class="tech-grid">
    <!-- using skillicons.dev with standard icons + custom fallback -->
    <div class="tech-item"><img src="https://skillicons.dev/icons?i=html" alt="HTML5" loading="lazy"><span>HTML</span></div>
    <div class="tech-item"><img src="https://skillicons.dev/icons?i=css" alt="CSS3" loading="lazy"><span>CSS</span></div>
    <div class="tech-item"><img src="https://skillicons.dev/icons?i=js" alt="JavaScript" loading="lazy"><span>JS</span></div>
    <div class="tech-item"><img src="https://skillicons.dev/icons?i=python" alt="Python" loading="lazy"><span>Python</span></div>
    <div class="tech-item"><img src="https://skillicons.dev/icons?i=php" alt="PHP" loading="lazy"><span>PHP</span></div>
    <div class="tech-item"><img src="https://skillicons.dev/icons?i=linux" alt="Linux" loading="lazy"><span>Linux</span></div>
    <div class="tech-item"><img src="https://skillicons.dev/icons?i=git" alt="Git" loading="lazy"><span>Git</span></div>
    <div class="tech-item"><img src="https://skillicons.dev/icons?i=github" alt="GitHub" loading="lazy"><span>GitHub</span></div>
    <div class="tech-item"><img src="https://skillicons.dev/icons?i=vscode" alt="VS Code" loading="lazy"><span>VS Code</span></div>
    <!-- extra custom icons via font-awesome (since skillicons doesn't have all) -->
    <div class="tech-item" style="gap:0.1rem;">
      <i class="fas fa-shield-halved" style="font-size: 2.8rem; color: #58a6ff;"></i>
      <span>Security</span>
    </div>
    <div class="tech-item" style="gap:0.1rem;">
      <i class="fas fa-flask" style="font-size: 2.8rem; color: #f0883e;"></i>
      <span>Pharma</span>
    </div>
    <div class="tech-item" style="gap:0.1rem;">
      <i class="fas fa-database" style="font-size: 2.8rem; color: #3fb950;"></i>
      <span>MySQL</span>
    </div>
  </div>

  <!-- ========== STATS (Streak + Activity) ========== -->
  <div class="section-title">
    <i class="fas fa-chart-line"></i> GitHub Analytics
  </div>
  <div class="stats-grid">
    <div class="stat-card">
      <span class="stat-label"><i class="fas fa-fire" style="color: #f0883e;"></i> Streak</span>
      <img src="https://streak-stats.demolab.com?user=psvineet&theme=tokyonight&hide_border=true" alt="GitHub Streak" loading="lazy">
    </div>
    <div class="stat-card">
      <span class="stat-label"><i class="fas fa-chart-simple" style="color: #58a6ff;"></i> Activity</span>
      <img src="https://github-readme-activity-graph.vercel.app/graph?username=psvineet&theme=tokyo-night&hide_border=true" alt="GitHub Activity Graph" loading="lazy">
    </div>
  </div>

  <!-- ========== FULL WIDTH ACTIVITY GRAPH (enhanced) ========== -->
  <div class="section-title" style="margin-top: 0.5rem;">
    <i class="fas fa-wave-square"></i> Contribution Activity
  </div>
  <div class="graph-wrapper">
    <!-- using a more detailed graph – already have one above, but we show another style for variety -->
    <img src="https://github-readme-activity-graph.vercel.app/graph?username=psvineet&theme=github-light&hide_border=true&bg_color=161b22&color=58a6ff&line=f0883e&point=ffffff&area=true&area_color=58a6ff" 
         alt="Contribution Graph" loading="lazy">
  </div>

  <!-- ========== FOOTER / SOCIAL ========== -->
  <div style="text-align: center; padding: 1.5rem 0 0.5rem; border-top: 1px solid #21262d; margin-top: 1rem;">
    <div style="display: flex; justify-content: center; gap: 1.8rem; flex-wrap: wrap; font-size: 1.3rem;">
      <a href="https://github.com/psvineet" target="_blank" style="color: #8b949e; transition: color 0.2s;" onmouseover="this.style.color='#58a6ff'" onmouseout="this.style.color='#8b949e'">
        <i class="fab fa-github"></i>
      </a>
      <a href="https://linkedin.com/in/psvineet" target="_blank" style="color: #8b949e; transition: color 0.2s;" onmouseover="this.style.color='#0a66c2'" onmouseout="this.style.color='#8b949e'">
        <i class="fab fa-linkedin-in"></i>
      </a>
      <a href="https://tryhackme.com/p/psvineet" target="_blank" style="color: #8b949e; transition: color 0.2s;" onmouseover="this.style.color='#f0883e'" onmouseout="this.style.color='#8b949e'">
        <i class="fas fa-shield-halved"></i>
      </a>
      <a href="https://orcid.org/0009-0006-8424-0643" target="_blank" style="color: #8b949e; transition: color 0.2s;" onmouseover="this.style.color='#a6ce39'" onmouseout="this.style.color='#8b949e'">
        <i class="fab fa-orcid"></i>
      </a>
      <a href="mailto:connect.vps@icloud.com" style="color: #8b949e; transition: color 0.2s;" onmouseover="this.style.color='#f0883e'" onmouseout="this.style.color='#8b949e'">
        <i class="fas fa-envelope"></i>
      </a>
    </div>
    <p style="margin-top: 0.8rem; font-size: 0.7rem; color: #484f58; letter-spacing: 0.3px;">
      <i class="fas fa-code"></i> with <i class="fas fa-heart" style="color: #f0883e;"></i> · built for the GitHub community
    </p>
  </div>

</div>
</body>
</html>

