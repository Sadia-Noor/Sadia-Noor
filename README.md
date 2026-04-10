<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Sadia Noor — GitHub Profile Preview</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;500;700&family=Syne:wght@400;600;700;800&family=Inter:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #0d1117;
    --surface: #161b22;
    --surface2: #1c2128;
    --border: #30363d;
    --accent: #64ffda;
    --accent2: #ff6b6b;
    --accent3: #bd93f9;
    --text: #e2e8f0;
    --muted: #8b949e;
    --heading: #f0f6fc;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Inter', sans-serif;
    font-size: 15px;
    line-height: 1.7;
  }

  /* HEADER */
  .header {
    background: linear-gradient(135deg, #0d1117 0%, #1a1a2e 50%, #16213e 100%);
    padding: 60px 40px 50px;
    text-align: center;
    position: relative;
    overflow: hidden;
    border-bottom: 1px solid var(--border);
  }
  .header::before {
    content: '';
    position: absolute;
    top: -80px; left: -80px;
    width: 300px; height: 300px;
    background: radial-gradient(circle, rgba(100,255,218,0.07) 0%, transparent 70%);
    border-radius: 50%;
  }
  .header::after {
    content: '';
    position: absolute;
    bottom: -80px; right: -40px;
    width: 250px; height: 250px;
    background: radial-gradient(circle, rgba(189,147,249,0.06) 0%, transparent 70%);
    border-radius: 50%;
  }
  .name {
    font-family: 'Syne', sans-serif;
    font-size: 52px;
    font-weight: 800;
    color: var(--heading);
    letter-spacing: -1px;
    margin-bottom: 8px;
  }
  .tagline {
    font-family: 'JetBrains Mono', monospace;
    font-size: 14px;
    color: var(--accent);
    margin-bottom: 28px;
    letter-spacing: 0.5px;
  }
  .typing-line {
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    color: var(--accent);
    background: rgba(100,255,218,0.05);
    border: 1px solid rgba(100,255,218,0.2);
    border-radius: 4px;
    padding: 10px 20px;
    display: inline-block;
    margin-bottom: 28px;
  }
  .typing-line::after { content: '|'; animation: blink 1s infinite; }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

  /* BADGES */
  .badges { display: flex; gap: 10px; flex-wrap: wrap; justify-content: center; margin-bottom: 8px; }
  .badge {
    display: inline-flex; align-items: center; gap: 7px;
    padding: 7px 14px;
    border-radius: 6px;
    font-size: 12px;
    font-weight: 500;
    font-family: 'JetBrains Mono', monospace;
    text-decoration: none;
    transition: transform 0.2s, opacity 0.2s;
    letter-spacing: 0.3px;
  }
  .badge:hover { transform: translateY(-2px); opacity: 0.9; }
  .badge-li { background: #0A66C2; color: white; }
  .badge-mail { background: #EA4335; color: white; }
  .badge-gh { background: #1a1a1a; color: white; border: 1px solid #444; }
  .badge-kg { background: #20BEFF; color: white; }

  /* MAIN CONTENT */
  .container { max-width: 860px; margin: 0 auto; padding: 48px 32px; }
  hr { border: none; border-top: 1px solid var(--border); margin: 40px 0; }

  h2 {
    font-family: 'Syne', sans-serif;
    font-size: 22px;
    font-weight: 700;
    color: var(--heading);
    margin-bottom: 20px;
    display: flex; align-items: center; gap: 10px;
  }
  h2 .emoji { font-size: 20px; }
  h3 {
    font-family: 'Syne', sans-serif;
    font-size: 16px;
    font-weight: 600;
    color: var(--accent);
    margin-bottom: 8px;
  }
  p { color: var(--text); margin-bottom: 12px; }

  /* ABOUT */
  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-top: 20px; }
  .about-item {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 14px 18px;
    font-size: 13.5px;
    color: var(--muted);
  }
  .about-item strong { color: var(--accent); }

  /* CODE BLOCK */
  .codeblock {
    background: #010409;
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 20px 24px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 12.5px;
    line-height: 1.9;
    color: #c9d1d9;
    overflow-x: auto;
    margin: 16px 0;
  }
  .codeblock .key { color: #79c0ff; }
  .codeblock .val { color: #a5d6ff; }
  .codeblock .accent { color: var(--accent); }
  .codeblock .comment { color: #8b949e; }

  /* SKILLS */
  .skill-group { margin-bottom: 24px; }
  .skill-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 1.5px;
    margin-bottom: 10px;
  }
  .pills { display: flex; flex-wrap: wrap; gap: 8px; }
  .pill {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 5px;
    padding: 5px 12px;
    font-size: 12.5px;
    font-family: 'JetBrains Mono', monospace;
    color: var(--text);
    transition: border-color 0.2s, color 0.2s;
  }
  .pill:hover { border-color: var(--accent); color: var(--accent); }
  .pill.highlight { border-color: rgba(100,255,218,0.4); color: var(--accent); background: rgba(100,255,218,0.05); }
  .pill.purple { border-color: rgba(189,147,249,0.4); color: var(--accent3); background: rgba(189,147,249,0.05); }
  .pill.red { border-color: rgba(255,107,107,0.4); color: var(--accent2); background: rgba(255,107,107,0.05); }

  /* PROJECTS */
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 22px 24px;
    margin-bottom: 16px;
    transition: border-color 0.2s, transform 0.2s;
    position: relative;
  }
  .project-card:hover { border-color: var(--accent); transform: translateY(-2px); }
  .project-card.thesis { border-left: 3px solid var(--accent); }
  .project-card.ml { border-left: 3px solid var(--accent3); }
  .project-card.nlp { border-left: 3px solid #ff9f43; }
  .project-meta {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    margin-top: 10px;
  }
  .project-meta span {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 3px;
    padding: 2px 8px;
    margin-right: 6px;
    display: inline-block;
    margin-top: 4px;
  }
  .score-badge {
    position: absolute; top: 16px; right: 20px;
    background: rgba(100,255,218,0.1);
    border: 1px solid rgba(100,255,218,0.3);
    color: var(--accent);
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    padding: 3px 10px;
    border-radius: 4px;
  }

  /* STATS */
  .stats-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin: 16px 0; }
  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 20px;
    text-align: center;
  }
  .stat-num {
    font-family: 'Syne', sans-serif;
    font-size: 32px;
    font-weight: 800;
    color: var(--accent);
    display: block;
  }
  .stat-label {
    font-size: 12px;
    color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
    text-transform: uppercase;
    letter-spacing: 1px;
  }
  .github-stats-img { width: 100%; border-radius: 8px; border: 1px solid var(--border); }

  /* TABLE */
  table { width: 100%; border-collapse: collapse; font-size: 14px; }
  th {
    background: var(--surface2);
    color: var(--accent);
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    text-transform: uppercase;
    letter-spacing: 1px;
    padding: 12px 16px;
    text-align: left;
    border: 1px solid var(--border);
  }
  td {
    padding: 12px 16px;
    border: 1px solid var(--border);
    color: var(--text);
    background: var(--surface);
  }
  td strong { color: var(--heading); }

  /* EXPERIENCE */
  .exp-card {
    border-left: 2px solid var(--border);
    padding-left: 20px;
    margin-bottom: 24px;
    position: relative;
  }
  .exp-card::before {
    content: '';
    width: 8px; height: 8px;
    background: var(--accent);
    border-radius: 50%;
    position: absolute;
    left: -5px; top: 6px;
  }
  .exp-title { font-family: 'Syne', sans-serif; font-weight: 600; color: var(--heading); font-size: 15px; }
  .exp-company { color: var(--accent); font-size: 13px; font-family: 'JetBrains Mono', monospace; }
  .exp-period { color: var(--muted); font-size: 12px; font-family: 'JetBrains Mono', monospace; margin-bottom: 8px; }

  /* CERTS */
  .cert-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
  .cert-item {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 7px;
    padding: 12px 16px;
    font-size: 13px;
    color: var(--muted);
    display: flex; align-items: flex-start; gap: 10px;
  }
  .cert-icon { color: var(--accent); font-size: 15px; flex-shrink: 0; margin-top: 1px; }

  /* FOOTER */
  .footer {
    background: linear-gradient(135deg, #16213e, #1a1a2e, #0d1117);
    padding: 40px;
    text-align: center;
    border-top: 1px solid var(--border);
    margin-top: 20px;
  }
  .quote {
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    color: var(--muted);
    font-style: italic;
    max-width: 600px;
    margin: 0 auto 12px;
  }
  .quote span { color: var(--accent); }

  /* ANIMATIONS */
  .section { animation: fadeUp 0.5s ease both; }
  @keyframes fadeUp { from { opacity: 0; transform: translateY(16px); } to { opacity: 1; transform: translateY(0); } }

  /* NOTE BANNER */
  .note {
    background: rgba(100,255,218,0.05);
    border: 1px solid rgba(100,255,218,0.2);
    border-radius: 8px;
    padding: 14px 18px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 12.5px;
    color: var(--accent);
    margin-bottom: 32px;
  }
  .note strong { color: var(--heading); }
</style>
</head>
<body>

<!-- HEADER -->
<div class="header">
  <div class="name">Sadia Noor</div>
  <div class="tagline">MS Data Science · NLP Researcher · SEECS, NUST</div>
  <div class="typing-line">→ Predicting Valence &amp; Arousal from Longitudinal Text</div>
  <div class="badges">
    <a class="badge badge-li" href="https://linkedin.com/in/sadianoor-06333218a" target="_blank">🔗 LinkedIn</a>
    <a class="badge badge-mail" href="mailto:sadianoor090@gmail.com">✉ Email</a>
    <a class="badge badge-gh" href="https://github.com/Sadia-Noor" target="_blank">⚙ GitHub</a>
    <a class="badge badge-kg" href="#" target="_blank">📊 Kaggle</a>
  </div>
</div>

<div class="container">

  <div class="note">
    <strong>📋 This is a preview of your GitHub Profile README.</strong> The actual README.md file is ready for upload to your <code>Sadia-Noor/Sadia-Noor</code> repository. Scroll down to see all sections.
  </div>

  <!-- ABOUT -->
  <div class="section">
    <h2><span class="emoji">🧠</span> About Me</h2>
    <p>MS Data Science student at <strong>SEECS, NUST</strong>, working on my thesis in <strong>personalized longitudinal emotion modeling</strong>. My research predicts continuous dimensional affect — <strong>valence and arousal</strong> — from natural language text, accounting for individual differences and temporal dynamics across multiple timepoints.</p>
    <p>My work is anchored in <strong>SemEval 2026 Task 2</strong>, using ~5,285 self-reported text–emotion pairs from 182 participants over seven collection phases.</p>
    <div class="about-grid">
      <div class="about-item">🔬 <strong>Thesis:</strong> Personalized Longitudinal Dimensional Affect Modeling</div>
      <div class="about-item">🏫 <strong>Institution:</strong> SEECS, NUST · Islamabad</div>
      <div class="about-item">📐 <strong>Background:</strong> BS Mathematics, Sukkur IBA University</div>
      <div class="about-item">📍 <strong>Location:</strong> Islamabad, Pakistan</div>
    </div>
  </div>

  <hr/>

  <!-- RESEARCH -->
  <div class="section">
    <h2><span class="emoji">🔭</span> Current Research</h2>
    <div class="codeblock">
<span class="key">Thesis</span>:         <span class="val">Emotion Modeling for Investigating Dimensional Affect in Longitudinal Texts</span>
<span class="key">Advisor</span>:        <span class="val">Dr. Mehwish Fatima</span> | SEECS, NUST

<span class="key">Architecture</span>:   <span class="accent">DistilBERT + Mean Pooling + 128d User Embedding + Dual Head + MSE</span>
               <span class="accent">+ Temporal Features (Prev VA + Rolling Window)</span>

<span class="key">Task</span>:           <span class="val">Valence (−2 to +2) &amp; Arousal (0 to 2) regression from free-form text</span>
<span class="key">Benchmark</span>:      <span class="val">SemEval 2026 Task 2, Subtask 1</span>
<span class="key">Score</span>:          <span class="accent">0.6549</span>  <span class="comment"># Composite Pearson r · Controlled Ablation</span>

<span class="key">Key Dimensions</span>: <span class="val">Dimensional representation · User personalization · Temporal modeling</span>
               <span class="val">EmoBank intermediate training · Trait-State Fusion</span>
    </div>
  </div>

  <hr/>

  <!-- SKILLS -->
  <div class="section">
    <h2><span class="emoji">🛠️</span> Technical Stack</h2>

    <div class="skill-group">
      <div class="skill-label">Languages</div>
      <div class="pills">
        <div class="pill highlight">Python</div>
        <div class="pill">R</div>
        <div class="pill">SQL</div>
        <div class="pill">MATLAB</div>
        <div class="pill">DAX</div>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-label">Deep Learning Frameworks</div>
      <div class="pills">
        <div class="pill highlight">PyTorch</div>
        <div class="pill highlight">TensorFlow</div>
        <div class="pill">Keras</div>
        <div class="pill">Scikit-learn</div>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-label">NLP / Transformers</div>
      <div class="pills">
        <div class="pill purple">HuggingFace Transformers</div>
        <div class="pill purple">DistilBERT</div>
        <div class="pill purple">BERT</div>
        <div class="pill purple">XLM-RoBERTa</div>
        <div class="pill purple">RoBERTa</div>
        <div class="pill purple">DeBERTa</div>
        <div class="pill purple">LangChain</div>
        <div class="pill purple">spaCy</div>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-label">Data & Visualization</div>
      <div class="pills">
        <div class="pill">Pandas</div>
        <div class="pill">NumPy</div>
        <div class="pill">Matplotlib</div>
        <div class="pill">Seaborn</div>
        <div class="pill">Plotly</div>
        <div class="pill">Power BI</div>
        <div class="pill">Tableau</div>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-label">Tools & Environments</div>
      <div class="pills">
        <div class="pill">Google Colab</div>
        <div class="pill">Jupyter</div>
        <div class="pill">VS Code</div>
        <div class="pill">Git</div>
        <div class="pill">GitHub</div>
        <div class="pill">Kaggle</div>
        <div class="pill">PyCharm</div>
        <div class="pill">RStudio</div>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-label">Computer Vision (Prior Work)</div>
      <div class="pills">
        <div class="pill red">OpenCV</div>
        <div class="pill red">Albumentation</div>
        <div class="pill red">CNN</div>
        <div class="pill red">VGG16</div>
        <div class="pill red">ResNet</div>
        <div class="pill red">AlexNet</div>
      </div>
    </div>
  </div>

  <hr/>

  <!-- PROJECTS -->
  <div class="section">
    <h2><span class="emoji">📌</span> Selected Projects</h2>

    <div class="project-card thesis">
      <div class="score-badge">r = 0.6549</div>
      <h3>🧬 Thesis — Personalized Longitudinal Affect Modeling <em>(In Progress)</em></h3>
      <p>Predicting continuous valence and arousal from longitudinal ecological essays using DistilBERT with user embeddings and temporal features. SemEval 2026 Task 2 benchmark.</p>
      <div class="project-meta">
        <span>DistilBERT</span><span>User Embeddings</span><span>Temporal Features</span><span>PyTorch</span><span>HuggingFace</span>
      </div>
    </div>

    <div class="project-card nlp">
      <div class="score-badge">F1 = 0.6229</div>
      <h3>🌐 Multilingual Emotion Detection — SemEval 2025 Task 11</h3>
      <p>Fine-tuned XLM-RoBERTa for multilingual emotion classification across 5 languages. Addressed low-resource cross-lingual challenges.</p>
      <div class="project-meta">
        <span>XLM-RoBERTa</span><span>PyTorch</span><span>HuggingFace</span><span>NLP</span>
      </div>
    </div>

    <div class="project-card ml">
      <div class="score-badge">93% Acc</div>
      <h3>🧠 Brain Tumor Detection — CNN &amp; ML</h3>
      <p>Detection models on 3,284 MRI images. CNN (93%), XGBoost and Random Forest (92%). TensorFlow-based pipeline.</p>
      <div class="project-meta">
        <span>TensorFlow</span><span>CNN</span><span>XGBoost</span><span>Medical Imaging</span>
      </div>
    </div>

    <div class="project-card">
      <h3>🫁 Real vs. Synthetic TB Image Classification</h3>
      <p>Pipeline distinguishing real and synthetic TB X-rays. Synthetic images generated via AutoEncoder. CNN and VGG16 implementation.</p>
      <div class="project-meta">
        <span>CNN</span><span>VGG16</span><span>AutoEncoder</span><span>Kaggle</span>
      </div>
    </div>

    <div class="project-card">
      <div class="score-badge">85% Acc</div>
      <h3>💬 Healthcare Sentiment Analysis — Twitter Pakistan</h3>
      <p>Public sentiment analysis on healthcare quality using VADER, TextBlob, and RoBERTa. Random Forest with TF-IDF achieved 85% accuracy.</p>
      <div class="project-meta">
        <span>spaCy</span><span>RoBERTa</span><span>TF-IDF</span><span>LDA</span><span>Apify</span>
      </div>
    </div>
  </div>

  <hr/>

  <!-- STATS PLACEHOLDER -->
  <div class="section">
    <h2><span class="emoji">📈</span> GitHub Stats</h2>
    <div class="stats-grid">
      <div class="stat-card">
        <span class="stat-num">5K+</span>
        <span class="stat-label">Lines of Research Code</span>
      </div>
      <div class="stat-card">
        <span class="stat-num">182</span>
        <span class="stat-label">Dataset Participants</span>
      </div>
      <div class="stat-card">
        <span class="stat-num">7</span>
        <span class="stat-label">Collection Phases</span>
      </div>
      <div class="stat-card">
        <span class="stat-num">0.65</span>
        <span class="stat-label">Composite Pearson r</span>
      </div>
    </div>
    <p style="font-size:12px; color: var(--muted); font-family: 'JetBrains Mono', monospace; margin-top: 12px;">
      ↑ Live GitHub stats cards will appear here once README is on your profile repo (Sadia-Noor/Sadia-Noor).
    </p>
  </div>

  <hr/>

  <!-- EDUCATION -->
  <div class="section">
    <h2><span class="emoji">🎓</span> Education</h2>
    <table>
      <tr>
        <th>Degree</th><th>Institution</th><th>Year</th><th>GPA</th>
      </tr>
      <tr>
        <td><strong>MS Data Science</strong></td>
        <td>SEECS, NUST</td>
        <td>2023 – Present</td>
        <td><span style="color:var(--accent)">3.25 / 4.0</span></td>
      </tr>
      <tr>
        <td><strong>BS Mathematics</strong></td>
        <td>Sukkur IBA University</td>
        <td>2018 – 2022</td>
        <td><span style="color:var(--accent)">3.35 / 4.0</span></td>
      </tr>
    </table>
  </div>

  <hr/>

  <!-- EXPERIENCE -->
  <div class="section">
    <h2><span class="emoji">💼</span> Experience</h2>

    <div class="exp-card">
      <div class="exp-title">Machine Learning & Data Augmentation Intern</div>
      <div class="exp-company">truID Technologies · NSTP @ NUST</div>
      <div class="exp-period">Jan 2024 – Feb 2024</div>
      <p>Data augmentation pipelines using NumPy, OpenCV, and Albumentation. CNN, ResNet, and AlexNet development in PyTorch for image classification.</p>
    </div>

    <div class="exp-card">
      <div class="exp-title">Data Science Intern</div>
      <div class="exp-company">CodSoft · Remote</div>
      <div class="exp-period">Nov 2023</div>
      <p>Data cleaning, EDA, and ML model development using Python, Pandas, Scikit-learn, and TensorFlow.</p>
    </div>

    <div class="exp-card">
      <div class="exp-title">Mathematics Teacher (EST)</div>
      <div class="exp-company">IBA District Montessori School, Shikarpur</div>
      <div class="exp-period">Sep 2022 – Sep 2023</div>
      <p>Taught Grades IX–X Mathematics. Designed assessments and managed classroom learning outcomes.</p>
    </div>
  </div>

  <hr/>

  <!-- CERTIFICATIONS -->
  <div class="section">
    <h2><span class="emoji">🏅</span> Certifications</h2>
    <div class="cert-grid">
      <div class="cert-item"><span class="cert-icon">🤗</span> Hugging Face Agents Course — Hugging Face</div>
      <div class="cert-item"><span class="cert-icon">📘</span> NLP and Large Language Models — Hugging Face</div>
      <div class="cert-item"><span class="cert-icon">📊</span> Power of Data with Power BI — Microsoft</div>
      <div class="cert-item"><span class="cert-icon">📑</span> Preparing Data for Analysis — Microsoft</div>
      <div class="cert-item"><span class="cert-icon">🐍</span> Python for Data Science and AI — Coursera</div>
      <div class="cert-item"><span class="cert-icon">🏆</span> McKinsey Forward Program — McKinsey</div>
      <div class="cert-item"><span class="cert-icon">📐</span> Excel Skills for Business — Macquarie Univ.</div>
      <div class="cert-item"><span class="cert-icon">📖</span> Data Science Foundations — Great Learning</div>
    </div>
  </div>

</div>

<!-- FOOTER -->
<div class="footer">
  <p class="quote">"<span>Emotions are not discrete categories to be classified</span> — they are continuous, personal, and time-dependent."</p>
  <p style="font-family:'JetBrains Mono',monospace; font-size:11px; color:var(--muted); margin-top: 8px;">
    sadianoor090@gmail.com · linkedin.com/in/sadianoor-06333218a · SEECS, NUST · Islamabad, PK
  </p>
</div>

</body>
</html>
