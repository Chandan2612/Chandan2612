
<style>
  @import url('https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap');
  *{box-sizing:border-box;margin:0;padding:0}
  :root{
    --ink:#0a0a0f;--ink2:#3a3a4a;--ink3:#6b6b80;
    --surface:#ffffff;--surface2:#f4f3ff;--surface3:#eceaff;
    --accent:#5b47e0;--accent2:#8b6cf7;--accent3:#c4b8ff;
    --teal:#0fb8a0;--coral:#ff6b6b;--amber:#f5a623;
    --border:rgba(91,71,224,0.12);--border2:rgba(91,71,224,0.22);
    --mono:'JetBrains Mono',monospace;
    --display:'Syne',sans-serif;
  }
  body{font-family:var(--display);background:var(--surface);color:var(--ink);line-height:1.6;padding:0}

  .readme{max-width:860px;margin:0 auto;padding:2.5rem 1.5rem}

  /* HERO */
  .hero{text-align:center;padding:3rem 2rem 2.5rem;background:linear-gradient(135deg,#f4f3ff 0%,#eceaff 50%,#f9f5ff 100%);border-radius:20px;border:1px solid var(--border2);margin-bottom:2.5rem;position:relative;overflow:hidden}
  .hero::before{content:'';position:absolute;top:-60px;right:-60px;width:220px;height:220px;background:radial-gradient(circle,rgba(139,108,247,0.18) 0%,transparent 70%);pointer-events:none}
  .hero::after{content:'';position:absolute;bottom:-40px;left:-40px;width:160px;height:160px;background:radial-gradient(circle,rgba(15,184,160,0.15) 0%,transparent 70%);pointer-events:none}
  .hero-avatar{width:80px;height:80px;border-radius:50%;background:linear-gradient(135deg,var(--accent),var(--teal));display:flex;align-items:center;justify-content:center;font-size:28px;font-weight:800;color:#fff;margin:0 auto 1.2rem;letter-spacing:-1px;box-shadow:0 8px 24px rgba(91,71,224,0.25)}
  .hero h1{font-size:clamp(1.8rem,4vw,2.6rem);font-weight:800;letter-spacing:-0.03em;color:var(--ink);margin-bottom:0.4rem}
  .hero h1 span{color:var(--accent)}
  .hero-role{font-size:1rem;color:var(--accent);font-weight:600;letter-spacing:0.06em;text-transform:uppercase;margin-bottom:1rem;font-family:var(--mono)}
  .hero-desc{font-size:0.97rem;color:var(--ink2);max-width:520px;margin:0 auto 1.5rem;line-height:1.7}
  .badges{display:flex;flex-wrap:wrap;gap:10px;justify-content:center;margin-bottom:1.5rem}
  .badge{display:inline-flex;align-items:center;gap:6px;padding:7px 14px;border-radius:50px;font-size:0.82rem;font-weight:600;text-decoration:none;letter-spacing:0.02em;transition:transform 0.15s,box-shadow 0.15s}
  .badge:hover{transform:translateY(-2px);box-shadow:0 6px 20px rgba(91,71,224,0.2)}
  .badge-primary{background:var(--accent);color:#fff}
  .badge-ghost{background:var(--surface);color:var(--ink2);border:1px solid var(--border2)}
  .badge-dot{width:7px;height:7px;border-radius:50%;background:currentColor;opacity:0.7}
  .badge-live{background:#ecfdf5;color:#065f46;border:1px solid #bbf7d0}

  /* SECTION */
  .section{margin-bottom:2.5rem}
  .section-header{display:flex;align-items:center;gap:10px;margin-bottom:1.25rem;padding-bottom:0.75rem;border-bottom:1px solid var(--border)}
  .section-icon{width:32px;height:32px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:15px}
  .icon-purple{background:var(--surface3)}
  .icon-teal{background:#e0faf7}
  .icon-amber{background:#fdf8ea}
  .section-title{font-size:1.15rem;font-weight:700;letter-spacing:-0.02em;color:var(--ink)}

  /* EXPERIENCE CARD */
  .exp-card{background:var(--surface2);border:1px solid var(--border2);border-radius:14px;padding:1.5rem;position:relative;overflow:hidden}
  .exp-card::before{content:'';position:absolute;top:0;left:0;width:3px;height:100%;background:linear-gradient(180deg,var(--accent),var(--teal))}
  .exp-header{display:flex;justify-content:space-between;align-items:flex-start;gap:12px;margin-bottom:1rem;flex-wrap:wrap}
  .exp-title{font-size:1rem;font-weight:700;color:var(--ink)}
  .exp-company{font-size:0.85rem;color:var(--accent);font-weight:600;margin-top:2px}
  .exp-badge{font-size:0.75rem;font-weight:600;color:var(--accent);background:rgba(91,71,224,0.1);padding:4px 10px;border-radius:50px;white-space:nowrap;height:fit-content}
  .metrics{display:grid;grid-template-columns:repeat(auto-fit,minmax(130px,1fr));gap:10px;margin-bottom:1.2rem}
  .metric{background:var(--surface);border-radius:10px;padding:0.9rem;text-align:center;border:1px solid var(--border)}
  .metric-num{font-size:1.4rem;font-weight:800;color:var(--accent);line-height:1}
  .metric-lbl{font-size:0.73rem;color:var(--ink3);font-weight:500;margin-top:4px;text-transform:uppercase;letter-spacing:0.05em;font-family:var(--mono)}
  .exp-items{list-style:none;display:flex;flex-direction:column;gap:6px}
  .exp-items li{font-size:0.88rem;color:var(--ink2);padding-left:1.1rem;position:relative;line-height:1.6}
  .exp-items li::before{content:'▸';position:absolute;left:0;color:var(--accent);font-size:0.75rem;top:3px}
  .exp-items li strong{color:var(--ink);font-weight:600}

  /* TECH GRID */
  .tech-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(90px,1fr));gap:8px}
  .tech-chip{display:flex;flex-direction:column;align-items:center;gap:5px;padding:0.8rem 0.5rem;border-radius:10px;background:var(--surface2);border:1px solid var(--border);transition:all 0.2s;cursor:default}
  .tech-chip:hover{background:var(--surface3);border-color:var(--border2);transform:translateY(-2px)}
  .tech-chip-icon{font-size:1.4rem;width:32px;height:32px;display:flex;align-items:center;justify-content:center;border-radius:8px}
  .tech-chip-name{font-size:0.73rem;font-weight:600;color:var(--ink2);text-align:center;font-family:var(--mono)}

  /* PROJECTS */
  .proj-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:12px}
  .proj-card{border-radius:14px;border:1px solid var(--border);padding:1.25rem;background:var(--surface);transition:all 0.2s}
  .proj-card:hover{border-color:var(--border2);background:var(--surface2);transform:translateY(-2px);box-shadow:0 8px 24px rgba(91,71,224,0.1)}
  .proj-top{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:0.75rem}
  .proj-icon{width:38px;height:38px;border-radius:9px;display:flex;align-items:center;justify-content:center;font-size:18px}
  .proj-tag{font-size:0.7rem;font-weight:700;padding:3px 8px;border-radius:50px;letter-spacing:0.04em;font-family:var(--mono)}
  .tag-ext{background:#eff6ff;color:#1d4ed8;border:1px solid #bfdbfe}
  .tag-pkg{background:#f0fdf4;color:#166534;border:1px solid #bbf7d0}
  .proj-name{font-size:0.95rem;font-weight:700;color:var(--ink);margin-bottom:0.4rem}
  .proj-desc{font-size:0.83rem;color:var(--ink3);line-height:1.6;margin-bottom:0.9rem}
  .proj-link{font-size:0.78rem;font-weight:600;color:var(--accent);text-decoration:none;font-family:var(--mono);display:inline-flex;align-items:center;gap:4px}
  .proj-link:hover{text-decoration:underline}

  /* SKILLS BARS */
  .skill-bars{display:flex;flex-direction:column;gap:10px}
  .skill-row{display:flex;align-items:center;gap:10px}
  .skill-name{font-size:0.83rem;font-weight:600;color:var(--ink2);width:130px;flex-shrink:0;font-family:var(--mono)}
  .skill-track{flex:1;height:6px;background:var(--surface3);border-radius:50px;overflow:hidden}
  .skill-fill{height:100%;border-radius:50px;background:linear-gradient(90deg,var(--accent),var(--accent2))}
  .skill-pct{font-size:0.75rem;font-weight:700;color:var(--accent);width:36px;text-align:right;font-family:var(--mono)}

  /* STATS */
  .stats-row{display:grid;grid-template-columns:repeat(auto-fit,minmax(100px,1fr));gap:10px}
  .stat-card{background:var(--surface2);border:1px solid var(--border);border-radius:12px;padding:1rem;text-align:center}
  .stat-num{font-size:1.6rem;font-weight:800;color:var(--accent);display:block}
  .stat-lbl{font-size:0.72rem;color:var(--ink3);text-transform:uppercase;letter-spacing:0.06em;font-family:var(--mono);font-weight:500}

  /* ARCH */
  .arch-pills{display:flex;flex-wrap:wrap;gap:8px}
  .arch-pill{display:inline-flex;align-items:center;gap:6px;padding:6px 12px;border-radius:50px;background:var(--surface2);border:1px solid var(--border2);font-size:0.8rem;font-weight:600;color:var(--ink2)}
  .arch-pill-dot{width:6px;height:6px;border-radius:50%;background:var(--accent)}

  /* FOOTER */
  .footer{text-align:center;padding:1.5rem;border-top:1px solid var(--border);margin-top:1rem}
  .quote{font-size:0.88rem;color:var(--ink3);font-style:italic}
  .quote strong{color:var(--ink2);font-style:normal}

  @media(max-width:500px){
    .readme{padding:1.5rem 1rem}
    .hero{padding:2rem 1rem 1.5rem}
    .hero h1{font-size:1.6rem}
    .metrics{grid-template-columns:repeat(2,1fr)}
  }
</style>

<div class="readme">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-avatar">CK</div>
    <h1>Chandan <span>Kumar</span></h1>
    <div class="hero-role">Lead Frontend Engineer · Flutter Specialist</div>
    <div class="hero-desc">Architecting production-grade mobile experiences at scale. Building the Flutter ecosystem — one commit at a time.</div>
    <div class="badges">
      <a class="badge badge-live" href="#">
        <span class="badge-dot" style="background:#22c55e"></span> Open to Collab
      </a>
      <a class="badge badge-primary" href="mailto:chandan9035@gmail.com">✉ chandan9035@gmail.com</a>
      <a class="badge badge-ghost" href="https://linkedin.com/in/YOUR_LINKEDIN_USERNAME">in LinkedIn</a>
      <a class="badge badge-ghost" href="#"><span style="font-family:var(--mono);font-size:0.75em">📍</span> Bengaluru, IN</a>
    </div>
  </div>

  <!-- EXPERIENCE -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon icon-purple">💼</div>
      <div class="section-title">Professional Experience</div>
    </div>
    <div class="exp-card">
      <div class="exp-header">
        <div>
          <div class="exp-title">Lead Frontend Engineer</div>
          <div class="exp-company">Herody · Jaketa Media and Entertainment · Bengaluru</div>
        </div>
        <div class="exp-badge">2025 – Present</div>
      </div>
      <div class="metrics">
        <div class="metric"><div class="metric-num">100k+</div><div class="metric-lbl">Active Users</div></div>
        <div class="metric"><div class="metric-num">99.9%</div><div class="metric-lbl">Crash-Free</div></div>
        <div class="metric"><div class="metric-num">40%</div><div class="metric-lbl">Faster Load</div></div>
        <div class="metric"><div class="metric-num">100+</div><div class="metric-lbl">Device Types</div></div>
      </div>
      <ul class="exp-items">
        <li>Architected the core mobile app from scratch with <strong>Flutter & BLoC</strong> — zero-compromise on stability or scale</li>
        <li>Owned complex modules: real-time task tracking, automated merchant onboarding, geofencing-based verification</li>
        <li>Optimised widget tree rendering and image caching pipelines, delivering <strong>40% faster load times</strong></li>
        <li>Built secure API layers and automated payment integrations via <strong>REST / Dio</strong></li>
      </ul>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon icon-teal">⚙️</div>
      <div class="section-title">Tech Stack</div>
    </div>
    <div class="tech-grid">
      <div class="tech-chip"><div class="tech-chip-icon" style="background:#e8f4fd">🐦</div><div class="tech-chip-name">Flutter</div></div>
      <div class="tech-chip"><div class="tech-chip-icon" style="background:#e8f7ef">🎯</div><div class="tech-chip-name">Dart</div></div>
      <div class="tech-chip"><div class="tech-chip-icon" style="background:#f3f0ff">🤖</div><div class="tech-chip-name">Kotlin</div></div>
      <div class="tech-chip"><div class="tech-chip-icon" style="background:#fff3e0">🌐</div><div class="tech-chip-name">HTML/CSS</div></div>
      <div class="tech-chip"><div class="tech-chip-icon" style="background:#fffde7">⚡</div><div class="tech-chip-name">JavaScript</div></div>
      <div class="tech-chip"><div class="tech-chip-icon" style="background:#e8f5e9">🐍</div><div class="tech-chip-name">Python</div></div>
      <div class="tech-chip"><div class="tech-chip-icon" style="background:#e0f7fa">⚡</div><div class="tech-chip-name">FastAPI</div></div>
      <div class="tech-chip"><div class="tech-chip-icon" style="background:#e8eaf6">🐘</div><div class="tech-chip-name">PostgreSQL</div></div>
      <div class="tech-chip"><div class="tech-chip-icon" style="background:#fff8e1">🔥</div><div class="tech-chip-name">Firebase</div></div>
      <div class="tech-chip"><div class="tech-chip-icon" style="background:#fce4ec">🔧</div><div class="tech-chip-name">Git</div></div>
      <div class="tech-chip"><div class="tech-chip-icon" style="background:#f3e5f5">📮</div><div class="tech-chip-name">Postman</div></div>
      <div class="tech-chip"><div class="tech-chip-icon" style="background:#e8f5e9">🎨</div><div class="tech-chip-name">Figma</div></div>
    </div>
  </div>

  <!-- SKILL DEPTH -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon icon-amber">📊</div>
      <div class="section-title">Skill Depth</div>
    </div>
    <div class="skill-bars">
      <div class="skill-row"><div class="skill-name">Flutter / Dart</div><div class="skill-track"><div class="skill-fill" style="width:96%"></div></div><div class="skill-pct">96%</div></div>
      <div class="skill-row"><div class="skill-name">BLoC / Cubit</div><div class="skill-track"><div class="skill-fill" style="width:93%"></div></div><div class="skill-pct">93%</div></div>
      <div class="skill-row"><div class="skill-name">REST / Dio / API</div><div class="skill-track"><div class="skill-fill" style="width:90%"></div></div><div class="skill-pct">90%</div></div>
      <div class="skill-row"><div class="skill-name">Python / FastAPI</div><div class="skill-track"><div class="skill-fill" style="width:78%"></div></div><div class="skill-pct">78%</div></div>
      <div class="skill-row"><div class="skill-name">Firebase</div><div class="skill-track"><div class="skill-fill" style="width:82%"></div></div><div class="skill-pct">82%</div></div>
      <div class="skill-row"><div class="skill-name">CI/CD</div><div class="skill-track"><div class="skill-fill" style="width:72%"></div></div><div class="skill-pct">72%</div></div>
    </div>
  </div>

  <!-- OPEN SOURCE -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon icon-teal">🛠</div>
      <div class="section-title">Open Source & Products</div>
    </div>
    <div class="proj-grid">
      <div class="proj-card">
        <div class="proj-top">
          <div class="proj-icon" style="background:#eff6ff">🧪</div>
          <span class="proj-tag tag-ext">Chrome Extension</span>
        </div>
        <div class="proj-name">TestAPI Tool</div>
        <div class="proj-desc">Lightweight REST API tester right in the browser — no heavy external software needed. Built for frontend devs who move fast.</div>
        <a class="proj-link" href="https://chromewebstore.google.com/detail/testapi-tool/oemjninopbfidcppomcengldnanofljb">View on Chrome Web Store →</a>
      </div>
      <div class="proj-card">
        <div class="proj-top">
          <div class="proj-icon" style="background:#f0fdf4">📦</div>
          <span class="proj-tag tag-pkg">pub.dev Package</span>
        </div>
        <div class="proj-name">dev_loggers_flutter</div>
        <div class="proj-desc">Structured, readable, feature-rich debug logging for Flutter apps. Because <code style="font-size:0.78em;background:var(--surface3);padding:1px 5px;border-radius:4px">print()</code> just doesn't cut it.</div>
        <a class="proj-link" href="https://pub.dev/packages/dev_loggers_flutter">View on pub.dev →</a>
      </div>
    </div>
  </div>

  <!-- FLUTTER MASTERY -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon icon-purple">🏗</div>
      <div class="section-title">Flutter Architectural Mastery</div>
    </div>
    <div class="arch-pills">
      <div class="arch-pill"><div class="arch-pill-dot"></div>BLoC / Cubit</div>
      <div class="arch-pill"><div class="arch-pill-dot"></div>Repository Pattern</div>
      <div class="arch-pill"><div class="arch-pill-dot"></div>Dependency Injection</div>
      <div class="arch-pill"><div class="arch-pill-dot"></div>GetIt</div>
      <div class="arch-pill"><div class="arch-pill-dot"></div>Provider</div>
      <div class="arch-pill"><div class="arch-pill-dot"></div>Custom Animations</div>
      <div class="arch-pill"><div class="arch-pill-dot"></div>Responsive Layouts</div>
      <div class="arch-pill"><div class="arch-pill-dot"></div>Codemagic CI/CD</div>
      <div class="arch-pill"><div class="arch-pill-dot"></div>GitHub Actions</div>
      <div class="arch-pill"><div class="arch-pill-dot"></div>Geofencing</div>
      <div class="arch-pill"><div class="arch-pill-dot"></div>Secure API Layers</div>
    </div>
  </div>

  <!-- GITHUB STATS -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon icon-amber">📈</div>
      <div class="section-title">GitHub Stats</div>
    </div>
    <div style="display:flex;flex-wrap:wrap;gap:12px;justify-content:center">
      <img src="https://github-readme-stats.vercel.app/api?username=Chandan2612&show_icons=true&theme=tokyonight&hide_border=true&border_radius=12&bg_color=f4f3ff&title_color=5b47e0&icon_color=0fb8a0&text_color=3a3a4a" style="border-radius:12px;max-width:100%" />
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Chandan2612&layout=compact&theme=tokyonight&hide_border=true&border_radius=12&bg_color=f4f3ff&title_color=5b47e0&text_color=3a3a4a" style="border-radius:12px;max-width:100%" />
    </div>
    <div style="display:flex;justify-content:center;margin-top:12px">
      <img src="https://streak-stats.demolab.com/?user=Chandan2612&theme=tokyonight&hide_border=true&border_radius=12&background=f4f3ff&ring=5b47e0&fire=ff6b6b&currStreakLabel=3a3a4a&sideLabels=3a3a4a&dates=6b6b80&currStreakNum=5b47e0&sideNums=5b47e0" style="border-radius:12px;max-width:100%" />
    </div>
    <div style="display:flex;justify-content:center;margin-top:12px">
      <img src="https://github-readme-activity-graph.vercel.app/graph?username=Chandan2612&theme=tokyo-night&hide_border=true&radius=12&bg_color=f4f3ff&color=5b47e0&line=8b6cf7&point=0fb8a0" style="border-radius:12px;max-width:100%" />
    </div>
    <div style="display:flex;justify-content:center;margin-top:12px">
      <img src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg" style="max-width:100%;border-radius:12px" />
    </div>
    <div style="text-align:center;margin-top:14px">
      <img src="https://komarev.com/ghpvc/?username=Chandan2612&style=for-the-badge&color=5b47e0&label=Profile+Views" style="border-radius:8px" />
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="quote">"Code is like humor. When you have to explain it, it's bad." <strong>— Let's build something clean.</strong></div>
  </div>

</div>
