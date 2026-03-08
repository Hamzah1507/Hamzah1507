<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Hamzah1507 — GitHub Profile Preview</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&family=Inter:wght@400;500;600;700&display=swap');

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: #010409;
    color: #e6edf3;
    font-family: 'Inter', sans-serif;
    min-height: 100vh;
    padding: 0;
  }

  .profile-wrapper {
    max-width: 860px;
    margin: 0 auto;
    background: #0d1117;
    border: 1px solid #30363d;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 0 60px rgba(110,64,201,0.15);
  }

  /* HEADER BANNER */
  .header-banner {
    background: linear-gradient(135deg, #0d1117 0%, #1a0a2e 50%, #6e40c9 100%);
    padding: 44px 32px 32px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .header-banner::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse at 70% 50%, rgba(110,64,201,0.25) 0%, transparent 70%);
  }
  .header-banner h1 {
    font-size: 30px;
    font-weight: 700;
    color: #fff;
    letter-spacing: -0.5px;
    position: relative;
  }
  .header-banner p {
    color: #b8bfc7;
    font-size: 14px;
    margin-top: 6px;
    font-family: 'Fira Code', monospace;
    position: relative;
  }
  .typing-bar {
    margin-top: 14px;
    display: flex;
    justify-content: center;
    position: relative;
  }
  .typing-text {
    font-family: 'Fira Code', monospace;
    font-size: 13px;
    color: #58a6ff;
    border-right: 2px solid #58a6ff;
    animation: blink 1s infinite;
    padding-right: 4px;
  }
  @keyframes blink { 0%,100%{border-color:#58a6ff} 50%{border-color:transparent} }

  .badges-row {
    display: flex;
    justify-content: center;
    gap: 8px;
    margin-top: 16px;
    position: relative;
    flex-wrap: wrap;
  }
  .badge {
    height: 25px;
    border-radius: 4px;
    display: flex;
    align-items: center;
    gap: 6px;
    padding: 0 10px;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.3px;
  }
  .badge-linkedin { background: #0A66C2; color: #fff; }
  .badge-gmail { background: #EA4335; color: #fff; }
  .badge-views { background: #6e40c9; color: #fff; }

  /* CONTENT */
  .content { padding: 24px 32px; }

  .section-title {
    font-size: 16px;
    font-weight: 700;
    color: #e6edf3;
    margin-bottom: 14px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  hr.divider {
    border: none;
    border-top: 1px solid #21262d;
    margin: 22px 0;
  }

  /* ABOUT */
  .about-list { list-style: none; display: flex; flex-direction: column; gap: 7px; }
  .about-list li {
    font-size: 13.5px;
    color: #c9d1d9;
    display: flex;
    align-items: flex-start;
    gap: 8px;
    line-height: 1.5;
  }
  .about-list li b { color: #e6edf3; }

  /* TECH STACK */
  .stack-section { margin-bottom: 12px; }
  .stack-label {
    font-size: 12px;
    color: #8b949e;
    font-family: 'Fira Code', monospace;
    margin-bottom: 8px;
    font-weight: 500;
  }
  .tags { display: flex; flex-wrap: wrap; gap: 6px; }
  .tag {
    padding: 4px 10px;
    border-radius: 5px;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.2px;
    color: #fff;
  }

  /* PROJECTS TABLE */
  .projects-table { width: 100%; border-collapse: collapse; font-size: 13px; }
  .projects-table th {
    text-align: left;
    color: #8b949e;
    font-weight: 600;
    padding: 8px 12px;
    border-bottom: 1px solid #21262d;
    font-size: 12px;
  }
  .projects-table td {
    padding: 10px 12px;
    border-bottom: 1px solid #161b22;
    color: #c9d1d9;
    vertical-align: top;
  }
  .projects-table td:first-child { color: #58a6ff; font-weight: 500; }
  .stack-pills { display: flex; flex-wrap: wrap; gap: 4px; margin-top: 4px; }
  .stack-pill {
    background: #161b22;
    border: 1px solid #30363d;
    color: #8b949e;
    padding: 2px 7px;
    border-radius: 20px;
    font-size: 10px;
    font-family: 'Fira Code', monospace;
  }

  /* STATS */
  .stats-area {
    background: #161b22;
    border: 1px solid #21262d;
    border-radius: 10px;
    padding: 20px;
    text-align: center;
    margin-bottom: 14px;
  }
  .streak-mock {
    display: flex;
    justify-content: center;
    gap: 32px;
    flex-wrap: wrap;
  }
  .streak-item { text-align: center; }
  .streak-num { font-size: 28px; font-weight: 700; color: #6e40c9; font-family: 'Fira Code', monospace; }
  .streak-label { font-size: 11px; color: #8b949e; margin-top: 2px; }

  .activity-mock {
    background: #161b22;
    border: 1px solid #21262d;
    border-radius: 10px;
    padding: 16px;
    display: flex;
    gap: 3px;
    flex-wrap: wrap;
    justify-content: center;
  }
  .act-cell {
    width: 11px; height: 11px;
    border-radius: 2px;
    background: #21262d;
  }
  .act-cell.l1 { background: #2d1b69; }
  .act-cell.l2 { background: #4a2ea0; }
  .act-cell.l3 { background: #6e40c9; }
  .act-cell.l4 { background: #9a6dd7; }

  /* ✨ ACHIEVEMENTS SECTION */
  .achievements-section {
    background: linear-gradient(135deg, #0d1117 0%, #130d2b 100%);
    border: 1px solid #30363d;
    border-radius: 12px;
    padding: 24px;
    position: relative;
    overflow: hidden;
  }
  .achievements-section::before {
    content: '';
    position: absolute;
    top: -40px; right: -40px;
    width: 180px; height: 180px;
    background: radial-gradient(circle, rgba(110,64,201,0.2) 0%, transparent 70%);
    pointer-events: none;
  }

  .achievements-grid {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
    margin-top: 4px;
  }

  .achievement-card {
    background: #161b22;
    border: 1px solid #30363d;
    border-radius: 12px;
    padding: 20px 24px;
    text-align: center;
    width: 175px;
    position: relative;
    transition: transform 0.2s, border-color 0.2s, box-shadow 0.2s;
    cursor: default;
  }
  .achievement-card:hover {
    transform: translateY(-4px);
    border-color: #6e40c9;
    box-shadow: 0 8px 24px rgba(110,64,201,0.3);
  }
  .achievement-card::after {
    content: '';
    position: absolute;
    inset: 0;
    border-radius: 12px;
    background: linear-gradient(135deg, rgba(110,64,201,0.05) 0%, transparent 100%);
    pointer-events: none;
  }

  .achievement-img {
    width: 72px;
    height: 72px;
    border-radius: 50%;
    margin: 0 auto 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 36px;
    position: relative;
  }
  .achievement-img.pull-shark {
    background: radial-gradient(circle, #0d3b6e, #1a6eb5);
    box-shadow: 0 0 20px rgba(26,110,181,0.4);
  }
  .achievement-img.yolo {
    background: radial-gradient(circle, #3d1a00, #b85c00);
    box-shadow: 0 0 20px rgba(184,92,0,0.4);
  }
  .achievement-img.quickdraw {
    background: radial-gradient(circle, #2d1a00, #a07000);
    box-shadow: 0 0 20px rgba(160,112,0,0.4);
  }

  .achievement-name {
    font-size: 14px;
    font-weight: 700;
    color: #e6edf3;
    margin-bottom: 6px;
  }
  .achievement-desc {
    font-size: 11px;
    color: #8b949e;
    line-height: 1.5;
  }
  .achievement-badge-label {
    display: inline-block;
    margin-top: 10px;
    background: rgba(110,64,201,0.15);
    border: 1px solid rgba(110,64,201,0.4);
    color: #9a6dd7;
    font-size: 10px;
    font-weight: 600;
    padding: 2px 8px;
    border-radius: 20px;
    font-family: 'Fira Code', monospace;
    letter-spacing: 0.3px;
  }

  /* FOOTER */
  .footer {
    text-align: center;
    padding: 20px 32px;
    font-size: 13px;
    color: #8b949e;
    border-top: 1px solid #21262d;
  }
  .footer a { color: #58a6ff; text-decoration: none; font-weight: 600; }
</style>
</head>
<body>
<div class="profile-wrapper">

  <!-- HEADER -->
  <div class="header-banner">
    <h1>Mohammed Hamzah Saiyed</h1>
    <p>Data Scientist | AI/ML | Generative AI</p>
    <div class="typing-bar">
      <span class="typing-text">Building AI Systems · End-to-End ML 🚀</span>
    </div>
    <div class="badges-row">
      <span class="badge badge-linkedin">🔗 LinkedIn</span>
      <span class="badge badge-gmail">✉ Gmail</span>
      <span class="badge badge-views">👁 Profile Views · 280</span>
    </div>
  </div>

  <div class="content">

    <!-- ABOUT -->
    <div class="section-title">🧑‍💻 About Me</div>
    <ul class="about-list">
      <li>🎓 Final-year <b>iMSc.IT</b> student with <b>6+ months of hands-on AI/ML internship experience</b></li>
      <li>🔭 I build <b>end-to-end ML systems</b> — from raw data to deployed, production-grade models</li>
      <li>🧠 Core focus: <b>Deep Learning</b> · <b>Computer Vision</b> · <b>NLP/LLMs</b> · <b>Generative AI</b></li>
      <li>🔬 Currently building <b>RAG pipelines</b>, fine-tuning <b>LLMs</b>, and exploring <b>multimodal systems</b></li>
      <li>🟢 <b>Open to Data Science / AI-ML roles</b></li>
    </ul>

    <hr class="divider"/>

    <!-- TECH STACK -->
    <div class="section-title">🛠 Tech Stack</div>

    <div class="stack-section">
      <div class="stack-label">💻 Languages</div>
      <div class="tags">
        <span class="tag" style="background:#3776AB">Python</span>
        <span class="tag" style="background:#4479A1">SQL</span>
        <span class="tag" style="background:#276DC3">R</span>
        <span class="tag" style="background:#00599C">C++</span>
        <span class="tag" style="background:#4EAA25">Bash</span>
      </div>
    </div>

    <div class="stack-section" style="margin-top:12px">
      <div class="stack-label">🧠 ML & Deep Learning</div>
      <div class="tags">
        <span class="tag" style="background:#013243">NumPy</span>
        <span class="tag" style="background:#150458">Pandas</span>
        <span class="tag" style="background:#F7931E">Scikit-Learn</span>
        <span class="tag" style="background:#FF6F00">TensorFlow</span>
        <span class="tag" style="background:#EE4C2C">PyTorch</span>
      </div>
    </div>

    <div class="stack-section" style="margin-top:12px">
      <div class="stack-label">🤖 Generative AI & NLP</div>
      <div class="tags">
        <span class="tag" style="background:#7a6000;color:#FFD21E">HuggingFace</span>
        <span class="tag" style="background:#1C3C3C">LangChain</span>
        <span class="tag" style="background:#412991">OpenAI</span>
        <span class="tag" style="background:#09A3D5">spaCy</span>
      </div>
    </div>

    <div class="stack-section" style="margin-top:12px">
      <div class="stack-label">⚙️ Backend & Tools</div>
      <div class="tags">
        <span class="tag" style="background:#009688">FastAPI</span>
        <span class="tag" style="background:#092E20">Django</span>
        <span class="tag" style="background:#316192">PostgreSQL</span>
        <span class="tag" style="background:#4EA94B">MongoDB</span>
        <span class="tag" style="background:#F05032">Git</span>
        <span class="tag" style="background:#2496ED">Docker</span>
      </div>
    </div>

    <hr class="divider"/>

    <!-- PROJECTS -->
    <div class="section-title">🚀 Featured Projects</div>
    <table class="projects-table">
      <thead>
        <tr>
          <th>Project</th>
          <th>Description</th>
          <th>Stack</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>🧠 AI Healthcare Diagnosis</td>
          <td>Multimodal clinical risk prediction using deep learning for early diagnosis support</td>
          <td><div class="stack-pills"><span class="stack-pill">Python</span><span class="stack-pill">TensorFlow</span><span class="stack-pill">Multimodal ML</span></div></td>
        </tr>
        <tr>
          <td>🖼️ Image Classification VGG16</td>
          <td>Transfer learning image classification using VGG16 architecture</td>
          <td><div class="stack-pills"><span class="stack-pill">Python</span><span class="stack-pill">Keras</span><span class="stack-pill">OpenCV</span></div></td>
        </tr>
        <tr>
          <td>💊 MediConnect</td>
          <td>Full-stack telemedicine and online pharmacy web application</td>
          <td><div class="stack-pills"><span class="stack-pill">Django</span><span class="stack-pill">MySQL</span><span class="stack-pill">REST API</span></div></td>
        </tr>
      </tbody>
    </table>

    <hr class="divider"/>

    <!-- STATS -->
    <div class="section-title">📊 GitHub Stats</div>
    <div class="stats-area">
      <div class="streak-mock">
        <div class="streak-item">
          <div class="streak-num">12</div>
          <div class="streak-label">Current Streak</div>
        </div>
        <div class="streak-item">
          <div class="streak-num">55</div>
          <div class="streak-label">Total Commits</div>
        </div>
        <div class="streak-item">
          <div class="streak-num">7</div>
          <div class="streak-label">Repositories</div>
        </div>
      </div>
    </div>
    <div class="activity-mock">
      <!-- Simulated activity graph cells -->
      <script>
        document.addEventListener('DOMContentLoaded', () => {
          const grid = document.querySelector('.activity-mock');
          const levels = ['','l1','l2','l3','l4'];
          for(let i=0;i<364;i++){
            const d = document.createElement('div');
            const r = Math.random();
            d.className = 'act-cell ' + (r<0.5?'':r<0.7?'l1':r<0.85?'l2':r<0.95?'l3':'l4');
            grid.appendChild(d);
          }
        });
      </script>
    </div>

    <hr class="divider"/>

    <!-- ✨ ACHIEVEMENTS — NEW SECTION -->
    <div class="achievements-section">
      <div class="section-title" style="justify-content:center; margin-bottom:20px;">🏅 GitHub Achievements</div>
      <div class="achievements-grid">

        <div class="achievement-card">
          <div class="achievement-img pull-shark">🦈</div>
          <div class="achievement-name">Pull Shark</div>
          <div class="achievement-desc">Opened pull requests that have been merged</div>
        </div>

        <div class="achievement-card">
          <div class="achievement-img yolo">🤠</div>
          <div class="achievement-name">YOLO</div>
          <div class="achievement-desc">Merged a pull request without a code review</div>
        </div>

        <div class="achievement-card">
          <div class="achievement-img quickdraw">⚡</div>
          <div class="achievement-name">Quickdraw</div>
          <div class="achievement-desc">Closed an issue or PR within 5 minutes of opening</div>
        </div>

      </div>
    </div>

  </div>

  <!-- FOOTER -->
  <div class="footer">
    📫 <a href="/cdn-cgi/l/email-protection#1b737a76617a7335292b2b2f687a72627e7f5b7c767a727735787476"><span class="__cf_email__" data-cfemail="abc3cac6d1cac385999b9b9fd8cac2d2cecfebccc6cac2c785c8c4c6">[email
