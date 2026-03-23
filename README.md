<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kirthi Shanbhag — Senior AI Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@400;500&family=Instrument+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0c0e0f;
    --surface: #141618;
    --surface2: #1c1f21;
    --border: #252a2d;
    --accent: #4fffb0;
    --accent2: #7c6dfa;
    --accent3: #ff7c5c;
    --text: #e8eaeb;
    --muted: #6b7580;
    --tag-bg: #1c2a22;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Instrument Sans', sans-serif;
    line-height: 1.6;
    min-height: 100vh;
  }

  /* Noise overlay */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 0;
    opacity: 0.4;
  }

  .container {
    max-width: 900px;
    margin: 0 auto;
    padding: 64px 32px 96px;
    position: relative;
    z-index: 1;
  }

  /* ── HERO ── */
  .hero {
    display: grid;
    grid-template-columns: 1fr auto;
    align-items: start;
    gap: 32px;
    margin-bottom: 64px;
    padding-bottom: 48px;
    border-bottom: 1px solid var(--border);
  }

  .hero-eyebrow {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.14em;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .hero-eyebrow::before {
    content: '';
    display: inline-block;
    width: 20px;
    height: 1px;
    background: var(--accent);
  }

  h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(38px, 6vw, 58px);
    font-weight: 400;
    line-height: 1.1;
    letter-spacing: -0.02em;
    color: var(--text);
    margin-bottom: 20px;
  }

  h1 em {
    font-style: italic;
    color: var(--accent);
  }

  .hero-bio {
    font-size: 15px;
    color: var(--muted);
    max-width: 520px;
    line-height: 1.8;
    margin-bottom: 28px;
  }

  .hero-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .tag {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    padding: 5px 12px;
    border-radius: 3px;
    border: 1px solid var(--border);
    color: var(--muted);
    letter-spacing: 0.05em;
  }

  .tag.green { border-color: #1a3d2b; color: var(--accent); background: rgba(79,255,176,0.04); }
  .tag.purple { border-color: #2a2050; color: #a89cff; background: rgba(124,109,250,0.05); }
  .tag.orange { border-color: #3d2010; color: #ff9e7a; background: rgba(255,124,92,0.05); }

  .status-pill {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    background: var(--tag-bg);
    border: 1px solid #1a3d2b;
    border-radius: 20px;
    padding: 8px 16px;
    font-size: 12px;
    color: var(--accent);
    font-family: 'DM Mono', monospace;
    white-space: nowrap;
    letter-spacing: 0.02em;
  }

  .status-dot {
    width: 7px; height: 7px;
    border-radius: 50%;
    background: var(--accent);
    animation: pulse 2s ease-in-out infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.8); }
  }

  /* ── SECTION HEADERS ── */
  .section-label {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 24px;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  section { margin-bottom: 64px; }

  /* ── FEATURED PROJECT CARD ── */
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    overflow: hidden;
    transition: border-color 0.2s;
  }

  .project-card:hover { border-color: #2e3840; }

  /* Screenshot placeholder */
  .screenshot-zone {
    width: 100%;
    aspect-ratio: 16/8;
    background: var(--surface2);
    border-bottom: 1px solid var(--border);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 12px;
    cursor: pointer;
    position: relative;
    overflow: hidden;
    transition: background 0.2s;
  }

  .screenshot-zone:hover { background: #1f2325; }

  .screenshot-zone::before {
    content: '';
    position: absolute;
    inset: 0;
    background: repeating-linear-gradient(
      -45deg,
      transparent,
      transparent 20px,
      rgba(255,255,255,0.012) 20px,
      rgba(255,255,255,0.012) 21px
    );
  }

  .screenshot-icon {
    width: 48px; height: 48px;
    border: 2px dashed var(--border);
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--muted);
    font-size: 20px;
    position: relative;
    z-index: 1;
  }

  .screenshot-label {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.08em;
    position: relative;
    z-index: 1;
  }

  .screenshot-hint {
    font-size: 10px;
    color: #3d4850;
    font-family: 'DM Mono', monospace;
    position: relative;
    z-index: 1;
  }

  /* Image upload input (hidden) */
  .screenshot-zone input[type="file"] {
    position: absolute;
    inset: 0;
    opacity: 0;
    cursor: pointer;
    z-index: 2;
  }

  .screenshot-zone img {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    z-index: 3;
  }

  .project-body {
    padding: 28px 32px 32px;
  }

  .project-title-row {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 16px;
    margin-bottom: 12px;
  }

  .project-name {
    font-family: 'DM Serif Display', serif;
    font-size: 26px;
    font-weight: 400;
    color: var(--text);
  }

  .project-link {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--accent);
    text-decoration: none;
    border: 1px solid #1a3d2b;
    padding: 6px 12px;
    border-radius: 4px;
    white-space: nowrap;
    transition: background 0.15s;
  }

  .project-link:hover { background: rgba(79,255,176,0.07); }

  .project-tagline {
    font-size: 14px;
    color: var(--muted);
    margin-bottom: 20px;
    line-height: 1.7;
  }

  .project-highlights {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    margin-bottom: 24px;
  }

  .highlight {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    font-size: 13px;
    color: #8a9aa8;
    line-height: 1.5;
  }

  .highlight::before {
    content: '→';
    color: var(--accent);
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    flex-shrink: 0;
    margin-top: 2px;
  }

  .tech-badges {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  .badge {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    padding: 4px 10px;
    border-radius: 3px;
    letter-spacing: 0.06em;
  }

  .badge.py { background: #1a2a3d; color: #6aadff; border: 1px solid #1e3050; }
  .badge.graph { background: #1d2e1d; color: #6adf6a; border: 1px solid #213521; }
  .badge.ai { background: #28203a; color: #b39dff; border: 1px solid #322850; }
  .badge.db { background: #2a1e10; color: #ffb86a; border: 1px solid #3a2810; }
  .badge.api { background: #2a1a1a; color: #ff8080; border: 1px solid #3a2020; }

  /* ── SKILLS GRID ── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
  }

  .skill-block {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 20px;
  }

  .skill-block-title {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 14px;
    padding-bottom: 10px;
    border-bottom: 1px solid var(--border);
  }

  .skill-list {
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
  }

  .skill-chip {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    padding: 3px 8px;
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 2px;
    color: #8a9aa8;
    letter-spacing: 0.04em;
  }

  /* ── IMPACT TABLE ── */
  .impact-table {
    width: 100%;
    border-collapse: collapse;
  }

  .impact-table tr {
    border-bottom: 1px solid var(--border);
    transition: background 0.15s;
  }

  .impact-table tr:hover { background: var(--surface); }
  .impact-table tr:last-child { border-bottom: none; }

  .impact-table td {
    padding: 14px 0;
    font-size: 13px;
    vertical-align: top;
  }

  .impact-table td:first-child {
    color: var(--text);
    padding-right: 24px;
    width: 65%;
  }

  .impact-table td:last-child {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--accent);
    text-align: right;
    white-space: nowrap;
  }

  /* ── CONNECT ── */
  .connect-row {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
  }

  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    border-radius: 4px;
    font-family: 'DM Mono', monospace;
    font-size: 12px;
    text-decoration: none;
    border: 1px solid var(--border);
    color: var(--muted);
    transition: all 0.15s;
    letter-spacing: 0.04em;
  }

  .connect-btn:hover { border-color: var(--accent); color: var(--accent); }
  .connect-btn svg { width: 14px; height: 14px; fill: currentColor; }

  /* ── FOOTER ── */
  footer {
    padding-top: 48px;
    border-top: 1px solid var(--border);
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 12px;
  }

  footer p {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.04em;
  }

  @media (max-width: 640px) {
    .hero { grid-template-columns: 1fr; }
    .project-highlights { grid-template-columns: 1fr; }
    .skills-grid { grid-template-columns: 1fr 1fr; }
    .project-title-row { flex-direction: column; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- HERO -->
  <header class="hero">
    <div>
      <p class="hero-eyebrow">Senior AI Engineer & Data Scientist</p>
      <h1>Kirthi <em>Shanbhag</em></h1>
      <p class="hero-bio">
        7+ years building production-grade AI systems, scalable analytics platforms, and applied ML solutions. Currently focused on agentic AI, RAG systems, and knowledge graph-powered applications. UC Berkeley MIDS.
      </p>
      <div class="hero-tags">
        <span class="tag green">Agentic AI</span>
        <span class="tag purple">RAG Systems</span>
        <span class="tag orange">Production ML</span>
        <span class="tag">Cloud Infrastructure</span>
        <span class="tag">Knowledge Graphs</span>
      </div>
    </div>
    <div>
      <div class="status-pill">
        <span class="status-dot"></span>
        Open to roles
      </div>
    </div>
  </header>

  <!-- FEATURED PROJECT -->
  <section>
    <p class="section-label">Featured Project</p>

    <div class="project-card">
      <!-- SCREENSHOT PLACEHOLDER — click or drag an image here -->
      <div class="screenshot-zone" id="screenshotZone" title="Click to upload a screenshot">
        <input type="file" accept="image/*" onchange="loadScreenshot(event)">
        <div class="screenshot-icon">📸</div>
        <span class="screenshot-label">ADD PROJECT SCREENSHOT</span>
        <span class="screenshot-hint">Click to upload · 16:8 ratio works best</span>
      </div>

      <div class="project-body">
        <div class="project-title-row">
          <h2 class="project-name">ConfidenceOS</h2>
          <a href="https://github.com/kirthistaank/confidenceos" class="project-link" target="_blank">↗ GitHub</a>
        </div>

        <p class="project-tagline">
          A full-stack agentic AI interview coach — helps job seekers practice interviews, reframe self-doubt, and negotiate offers. Runs entirely on-device, zero API cost.
        </p>

        <div class="project-highlights">
          <span class="highlight">End-to-end LangGraph agentic loop with tool calling, memory & emotion detection</span>
          <span class="highlight">Hybrid RAG — dense (Pinecone) + sparse (BM25) with cross-encoder reranking</span>
          <span class="highlight">Knowledge graph retrieval via Neo4j AuraDB with Cypher query generation</span>
          <span class="highlight">Multi-mode coaching: Mock Interview, CBT Reframe, Salary Negotiation, STAR</span>
          <span class="highlight">Voice input via Web Speech API with live confidence scoring</span>
          <span class="highlight">Modular architecture — prompts, tools, memory, emotion fully decoupled</span>
        </div>

        <div class="tech-badges">
          <span class="badge py">Python 3.10+</span>
          <span class="badge ai">LangGraph</span>
          <span class="badge ai">Ollama (local LLM)</span>
          <span class="badge db">Pinecone</span>
          <span class="badge db">Neo4j AuraDB</span>
          <span class="badge api">FastAPI</span>
          <span class="badge graph">BM25 + Reranker</span>
        </div>
      </div>
    </div>
  </section>

  <!-- SKILLS -->
  <section>
    <p class="section-label">Technical Skills</p>
    <div class="skills-grid">
      <div class="skill-block">
        <p class="skill-block-title">AI & ML</p>
        <div class="skill-list">
          <span class="skill-chip">LangGraph</span>
          <span class="skill-chip">LangChain</span>
          <span class="skill-chip">PyTorch</span>
          <span class="skill-chip">TensorFlow</span>
          <span class="skill-chip">Hugging Face</span>
          <span class="skill-chip">OpenAI APIs</span>
          <span class="skill-chip">FAISS</span>
          <span class="skill-chip">Pinecone</span>
          <span class="skill-chip">Neo4j</span>
          <span class="skill-chip">Vertex AI</span>
          <span class="skill-chip">Dataiku</span>
          <span class="skill-chip">Databricks</span>
        </div>
      </div>
      <div class="skill-block">
        <p class="skill-block-title">Cloud & Big Data</p>
        <div class="skill-list">
          <span class="skill-chip">GCP</span>
          <span class="skill-chip">AWS</span>
          <span class="skill-chip">BigQuery</span>
          <span class="skill-chip">Spark</span>
          <span class="skill-chip">Kafka</span>
          <span class="skill-chip">Hive</span>
          <span class="skill-chip">Dataflow</span>
          <span class="skill-chip">Dataproc</span>
          <span class="skill-chip">Redshift</span>
        </div>
      </div>
      <div class="skill-block">
        <p class="skill-block-title">Infra & APIs</p>
        <div class="skill-list">
          <span class="skill-chip">Kubernetes</span>
          <span class="skill-chip">Docker</span>
          <span class="skill-chip">Airflow</span>
          <span class="skill-chip">Terraform</span>
          <span class="skill-chip">FastAPI</span>
          <span class="skill-chip">Flask</span>
          <span class="skill-chip">Plotly Dash</span>
          <span class="skill-chip">Looker</span>
        </div>
      </div>
    </div>
  </section>

  <!-- IMPACT -->
  <section>
    <p class="section-label">Industry Impact</p>
    <table class="impact-table">
      <tr>
        <td>Containerized ML apps on GCP — early failure detection</td>
        <td>↓ 20% analysis time</td>
      </tr>
      <tr>
        <td>Terabyte-scale automated data pipelines</td>
        <td>↓ 40% dev effort</td>
      </tr>
      <tr>
        <td>Centralized log analytics with ML-driven dashboards</td>
        <td>Predictive failure detection</td>
      </tr>
      <tr>
        <td>Image segmentation with Mask R-CNN</td>
        <td>↓ 50% labeling time</td>
      </tr>
      <tr>
        <td>Correlation analysis framework in PySpark</td>
        <td>↓ 30% manual engineering</td>
      </tr>
      <tr>
        <td>LLM-powered onboarding chatbot — Hugging Face + FAISS</td>
        <td>Accelerated onboarding</td>
      </tr>
    </table>
  </section>

  <!-- CONNECT -->
  <section>
    <p class="section-label">Let's Connect</p>
    <div class="connect-row">
      <a href="https://www.linkedin.com/in/kirthishanbhag/" class="connect-btn" target="_blank">
        <svg viewBox="0 0 24 24"><path d="M19 3a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h14m-.5 15.5v-5.3a3.26 3.26 0 0 0-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.79v8.37h2.79v-4.93c0-.77.62-1.4 1.39-1.4a1.4 1.4 0 0 1 1.4 1.4v4.93h2.79M6.88 8.56a1.68 1.68 0 0 0 1.68-1.68c0-.93-.75-1.69-1.68-1.69a1.69 1.69 0 0 0-1.69 1.69c0 .93.76 1.68 1.69 1.68m1.39 9.94v-8.37H5.5v8.37h2.77z"/></svg>
        LinkedIn
      </a>
      <a href="https://github.com/kirthistaank" class="connect-btn" target="_blank">
        <svg viewBox="0 0 24 24"><path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.09-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z"/></svg>
        GitHub
      </a>
      <a href="mailto:kirthi.genai@gmail.com" class="connect-btn">
        <svg viewBox="0 0 24 24"><path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
        Email
      </a>
    </div>
  </section>

  <footer>
    <p>Open to Senior AI Engineer · Senior Data Scientist · ML Engineer roles</p>
    <p>UC Berkeley MIDS · 7+ years industry</p>
  </footer>

</div>

<script>
function loadScreenshot(event) {
  const file = event.target.files[0];
  if (!file) return;
  const zone = document.getElementById('screenshotZone');
  const reader = new FileReader();
  reader.onload = (e) => {
    // Remove placeholder content
    zone.querySelectorAll('.screenshot-icon, .screenshot-label, .screenshot-hint').forEach(el => el.remove());
    // Add image
    const img = document.createElement('img');
    img.src = e.target.result;
    img.alt = 'Project screenshot';
    zone.appendChild(img);
  };
  reader.readAsDataURL(file);
}
</script>
</body>
</html>
