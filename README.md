<html lang="uz" data-theme="light">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<meta name="description" content="Ingliz tilini o'zbek tilida o'rgan - A1 dan B1 gacha">
<meta name="theme-color" content="#f5f5ff">
<title>LinguaUZ — Ingliz Tili Platformasi</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=Space+Grotesk:wght@400;500;700&family=Unbounded:wght@700;900&display=swap" rel="stylesheet">
<link rel="manifest" href="manifest.json">
<style>
/* ══════════════════════════════════════════════
   DESIGN TOKENS — LIGHT MODE BY DEFAULT
══════════════════════════════════════════════ */
:root {
  /* Brand */
  --brand: #6c63ff;
  --brand-2: #ff5c8a;
  --brand-3: #00e5a0;
  --brand-4: #ffb347;
  --brand-glow: rgba(108,99,255,.12);

  /* Light theme (Default oq rangli dizayn) */
  --bg: #f5f5ff;
  --surface: #ffffff;
  --surface-2: #eeeeff;
  --surface-3: #e0e0f5;
  --border: rgba(108,99,255,.18);
  --border-hover: rgba(108,99,255,.45);
  --text: #0d0d2a;
  --text-2: #4a4a6a;
  --text-3: #8080a0;
  --shadow: rgba(108,99,255,.12);
  --card-hover: rgba(108,99,255,.05);

  /* Transitions */
  --ease: cubic-bezier(.25,.46,.45,.94);
  --spring: cubic-bezier(.34,1.56,.64,1);

  /* Layout */
  --max: 960px;
  --radius: 18px;
  --radius-sm: 10px;
  --nav-h: 64px;
}

/* To'q rangli rejim varianti (agar kerak bo'lsa) */
[data-theme="dark"] {
  --bg: #0d0d1a;
  --surface: #13132a;
  --surface-2: #1c1c38;
  --surface-3: #252545;
  --border: rgba(108,99,255,.15);
  --border-hover: rgba(108,99,255,.4);
  --text: #f0f0ff;
  --text-2: #9090b8;
  --text-3: #5a5a80;
  --shadow: rgba(0,0,0,.45);
  --card-hover: rgba(108,99,255,.06);
}

/* ══════════════════════════════════════════════
   RESET & BASE
══════════════════════════════════════════════ */
*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }

html { scroll-behavior:smooth; }

body {
  font-family:'Plus Jakarta Sans',sans-serif;
  background:var(--bg);
  color:var(--text);
  overflow-x:hidden;
  min-height:100vh;
  transition:background .3s var(--ease), color .3s var(--ease);
}

/* Scrollbar */
::-webkit-scrollbar { width:5px; height:5px; }
::-webkit-scrollbar-track { background:transparent; }
::-webkit-scrollbar-thumb { background:var(--brand); border-radius:99px; }

/* ══════════════════════════════════════════════
   BACKGROUND PARTICLES CANVAS
══════════════════════════════════════════════ */
#particles {
  position:fixed; inset:0; pointer-events:none; z-index:0;
  opacity:.4;
}

/* ══════════════════════════════════════════════
   TOP NAVBAR
══════════════════════════════════════════════ */
.navbar {
  position:fixed; top:0; left:0; right:0; z-index:100;
  height:var(--nav-h);
  background:rgba(245,245,255,.85);
  backdrop-filter:blur(20px) saturate(180%);
  border-bottom:1px solid var(--border);
  display:flex; align-items:center;
  padding:0 20px;
  gap:12px;
}
[data-theme="dark"] .navbar {
  background:rgba(13,13,26,.85);
}

.nav-logo {
  font-family:'Unbounded',sans-serif;
  font-size:16px; font-weight:900;
  background:linear-gradient(135deg,var(--brand),var(--brand-3));
  -webkit-background-clip:text; -webkit-text-fill-color:transparent;
  background-clip:text;
  cursor:pointer; flex-shrink:0;
  text-decoration:none;
}

.nav-tabs {
  display:flex; gap:4px; flex:1;
  overflow-x:auto; -ms-overflow-style:none; scrollbar-width:none;
  padding:4px 0;
}
.nav-tabs::-webkit-scrollbar { display:none; }

.nav-tab {
  flex-shrink:0;
  padding:7px 14px;
  border-radius:99px;
  border:1px solid transparent;
  background:transparent;
  color:var(--text-2);
  font-family:'Plus Jakarta Sans',sans-serif;
  font-size:12px; font-weight:600;
  cursor:pointer;
  transition:all .2s var(--ease);
  white-space:nowrap;
  display:flex; align-items:center; gap:6px;
}
.nav-tab:hover { color:var(--text); background:var(--surface-2); }
.nav-tab.active {
  background:var(--brand);
  color:#fff;
  border-color:var(--brand);
  box-shadow:0 4px 16px rgba(108,99,255,.35);
}

.nav-right {
  display:flex; align-items:center; gap:10px; flex-shrink:0;
}

/* XP Pill in Nav */
.nav-xp {
  display:flex; align-items:center; gap:6px;
  background:var(--surface-2);
  border:1px solid var(--border);
  border-radius:99px;
  padding:5px 12px;
  font-size:12px; font-weight:700;
  color:var(--brand);
  cursor:pointer;
  transition:all .2s;
}
.nav-xp:hover { border-color:var(--brand); }
.nav-xp-icon { font-size:14px; }

/* Streak */
.nav-streak {
  display:flex; align-items:center; gap:5px;
  font-size:12px; font-weight:700;
  color:var(--brand-4);
}

/* Theme toggle */
.theme-btn {
  width:36px; height:36px;
  border-radius:99px;
  border:1px solid var(--border);
  background:var(--surface-2);
  color:var(--text-2);
  cursor:pointer;
  display:flex; align-items:center; justify-content:center;
  font-size:16px;
  transition:all .2s;
}
.theme-btn:hover { border-color:var(--brand); color:var(--brand); }

/* ══════════════════════════════════════════════
   MAIN CONTENT WRAPPER
══════════════════════════════════════════════ */
.main {
  max-width:var(--max);
  margin:0 auto;
  padding:calc(var(--nav-h) + 20px) 16px 100px;
  position:relative; z-index:1;
}

/* Page sections */
.page { display:none; animation:pageIn .35s var(--ease); }
.page.active { display:block; }
@keyframes pageIn {
  from { opacity:0; transform:translateY(16px); }
  to   { opacity:1; transform:translateY(0); }
}

/* ══════════════════════════════════════════════
   LANDING / HOME PAGE
══════════════════════════════════════════════ */
.hero-section {
  text-align:center;
  padding:40px 0 50px;
  position:relative;
}

.hero-glow {
  position:absolute; top:-100px; left:50%;
  transform:translateX(-50%);
  width:700px; height:500px;
  background:radial-gradient(ellipse,rgba(108,99,255,.18) 0%,transparent 65%);
  pointer-events:none;
}

.hero-badge {
  display:inline-flex; align-items:center; gap:7px;
  background:var(--surface-2);
  border:1px solid var(--border);
  border-radius:99px;
  padding:7px 18px;
  font-size:11px; font-weight:700;
  letter-spacing:1.5px; text-transform:uppercase;
  color:var(--brand);
  margin-bottom:24px;
  animation:badgePop .5s var(--spring) .1s both;
}
@keyframes badgePop { from{opacity:0;transform:scale(.8)} to{opacity:1;transform:scale(1)} }

.hero-title {
  font-family:'Unbounded',sans-serif;
  font-size:clamp(28px,6vw,56px);
  font-weight:900;
  line-height:1.08;
  margin-bottom:16px;
  animation:heroIn .6s var(--ease) .15s both;
}
@keyframes heroIn { from{opacity:0;transform:translateY(20px)} to{opacity:1;transform:translateY(0)} }

.hero-title .grad {
  background:linear-gradient(135deg,var(--brand) 0%,var(--brand-2) 50%,var(--brand-3) 100%);
  -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;
}

.hero-sub {
  color:var(--text-2);
  font-size:16px; line-height:1.7;
  max-width:480px; margin:0 auto 36px;
  animation:heroIn .6s var(--ease) .25s both;
}

.hero-cta {
  display:flex; gap:12px; justify-content:center; flex-wrap:wrap;
  animation:heroIn .6s var(--ease) .35s both;
}

.btn-primary {
  padding:14px 32px;
  background:linear-gradient(135deg,var(--brand),var(--brand-2));
  color:#fff;
  border:none; border-radius:var(--radius);
  font-family:'Plus Jakarta Sans',sans-serif;
  font-size:14px; font-weight:700;
  cursor:pointer;
  transition:all .25s var(--ease);
  box-shadow:0 8px 28px rgba(108,99,255,.38);
  display:inline-flex; align-items:center; gap:8px;
}
.btn-primary:hover { transform:translateY(-2px); box-shadow:0 14px 36px rgba(108,99,255,.5); }
.btn-primary:active { transform:translateY(0); }

.btn-secondary {
  padding:14px 28px;
  background:var(--surface-2);
  color:var(--text);
  border:1px solid var(--border);
  border-radius:var(--radius);
  font-family:'Plus Jakarta Sans',sans-serif;
  font-size:14px; font-weight:600;
  cursor:pointer;
  transition:all .25s var(--ease);
  display:inline-flex; align-items:center; gap:8px;
}
.btn-secondary:hover { border-color:var(--brand); color:var(--brand); }

/* Stats Row */
.hero-stats {
  display:flex; justify-content:center; gap:32px;
  padding:28px 0;
  border-top:1px solid var(--border);
  border-bottom:1px solid var(--border);
  margin:36px 0;
  animation:heroIn .6s var(--ease) .45s both;
  flex-wrap:wrap;
}
.hero-stat { text-align:center; }
.hero-stat-num {
  font-family:'Unbounded',sans-serif;
  font-size:28px; font-weight:900;
  background:linear-gradient(135deg,var(--brand),var(--brand-3));
  -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;
}
.hero-stat-lbl { font-size:11px; color:var(--text-2); font-weight:600; margin-top:3px; letter-spacing:.5px; text-transform:uppercase; }

/* Course Overview Cards */
.section-title {
  font-family:'Unbounded',sans-serif;
  font-size:14px; font-weight:700;
  letter-spacing:1px; text-transform:uppercase;
  color:var(--text-2);
  margin-bottom:16px;
  display:flex; align-items:center; gap:10px;
}
.section-title::after { content:''; flex:1; height:1px; background:var(--border); }

.course-grid {
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(200px,1fr));
  gap:12px;
  margin-bottom:32px;
}

.course-card {
  background:var(--surface);
  border:1px solid var(--border);
  border-radius:var(--radius);
  padding:22px 18px;
  cursor:pointer;
  transition:all .25s var(--ease);
  position:relative; overflow:hidden;
}
.course-card::before {
  content:''; position:absolute;
  top:0; left:0; right:0; height:3px;
  background:var(--card-accent, var(--brand));
  border-radius:var(--radius) var(--radius) 0 0;
}
.course-card:hover {
  border-color:var(--border-hover);
  transform:translateY(-4px);
  box-shadow:0 12px 32px var(--shadow);
  background:var(--card-hover);
}

.course-card-icon { font-size:32px; margin-bottom:12px; }
.course-card-num {
  font-family:'Unbounded',sans-serif;
  font-size:11px; font-weight:700;
  color:var(--text-3);
  letter-spacing:2px; text-transform:uppercase;
  margin-bottom:6px;
}
.course-card-title {
  font-family:'Space Grotesk',sans-serif;
  font-size:15px; font-weight:700;
  margin-bottom:5px;
}
.course-card-sub { font-size:11px; color:var(--text-2); line-height:1.6; }

.course-card-progress {
  margin-top:14px;
}
.prog-bar {
  width:100%; height:5px;
  background:var(--surface-3);
  border-radius:99px; overflow:hidden;
}
.prog-fill {
  height:100%;
  background:linear-gradient(90deg,var(--brand),var(--brand-3));
  border-radius:99px;
  transition:width .6s var(--ease);
}
.prog-label { font-size:10px; color:var(--text-3); margin-top:5px; }

/* Progress Dashboard */
.dashboard-grid {
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(150px,1fr));
  gap:10px;
  margin-bottom:28px;
}
.dash-card {
  background:var(--surface);
  border:1px solid var(--border);
  border-radius:var(--radius-sm);
  padding:16px 14px;
  text-align:center;
}
.dash-card-num {
  font-family:'Unbounded',sans-serif;
  font-size:26px; font-weight:900;
  margin-bottom:3px;
}
.dash-card-lbl { font-size:10px; color:var(--text-2); font-weight:600; letter-spacing:.5px; text-transform:uppercase; }

/* Achievement badges */
.badges-row {
  display:flex; gap:10px; flex-wrap:wrap; margin-bottom:28px;
}
.badge-item {
  display:flex; align-items:center; gap:8px;
  background:var(--surface);
  border:1px solid var(--border);
  border-radius:99px;
  padding:8px 14px;
  font-size:12px; font-weight:600;
  transition:all .2s;
  cursor:default;
}
.badge-item.earned {
  border-color:rgba(255,179,71,.4);
  background:rgba(255,179,71,.08);
  color:var(--brand-4);
}
.badge-item.locked { opacity:.4; filter:grayscale(1); }

/* ══════════════════════════════════════════════
   CARDS (COLLAPSIBLE)
══════════════════════════════════════════════ */
.card {
  background:var(--surface);
  border:1px solid var(--border);
  border-radius:var(--radius);
  padding:0;
  margin-bottom:12px;
  overflow:hidden;
  transition:border-color .2s, box-shadow .2s;
}
.card:hover { border-color:var(--border-hover); }

.card-header {
  display:flex; align-items:center; gap:14px;
  padding:18px 20px;
  cursor:pointer;
  user-select:none;
  transition:background .2s;
}
.card-header:hover { background:var(--card-hover); }

.card-icon {
  width:44px; height:44px;
  border-radius:12px;
  display:flex; align-items:center; justify-content:center;
  font-size:20px; flex-shrink:0;
  background:var(--surface-2);
}

.card-meta { flex:1; }
.card-meta h3 {
  font-family:'Space Grotesk',sans-serif;
  font-size:14px; font-weight:700;
  margin-bottom:3px;
}
.card-meta p { font-size:12px; color:var(--text-2); }

.card-chevron {
  color:var(--text-3);
  font-size:16px;
  transition:transform .3s var(--ease);
}
.card.open .card-chevron { transform:rotate(180deg); }

.card-body {
  display:none;
  padding:0 20px 20px;
  border-top:1px solid var(--border);
}
.card.open .card-body { display:block; }

/* ══════════════════════════════════════════════
   ALPHABET GRID
══════════════════════════════════════════════ */
.alpha-grid {
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(72px,1fr));
  gap:8px;
  padding-top:16px;
}
.alpha-card {
  background:var(--surface-2);
  border:1.5px solid var(--border);
  border-radius:12px;
  padding:12px 6px 10px;
  text-align:center;
  cursor:pointer;
  transition:all .2s var(--ease);
  position:relative; overflow:hidden;
}
.alpha-card::before {
  content:''; position:absolute; inset:0;
  background:radial-gradient(circle at center,currentColor,transparent);
  opacity:0; transition:opacity .2s;
}
.alpha-card:hover { transform:translateY(-4px); box-shadow:0 10px 24px var(--shadow); }
.alpha-card:hover::before { opacity:.05; }
.alpha-letter {
  font-family:'Unbounded',sans-serif;
  font-size:26px; font-weight:900;
  line-height:1; margin-bottom:4px;
}
.alpha-phon { font-size:9px; color:var(--text-2); margin-bottom:2px; }
.alpha-hint { font-size:8px; color:var(--brand); font-weight:600; }

/* ══════════════════════════════════════════════
   DATA TABLE
══════════════════════════════════════════════ */
.data-table {
  width:100%; border-collapse:collapse;
  font-size:13px; margin-top:14px;
}
.data-table th {
  text-align:left; padding:8px 12px;
  font-size:10px; letter-spacing:1.5px;
  text-transform:uppercase; color:var(--text-3);
  border-bottom:1px solid var(--border);
  font-weight:700;
}
.data-table td {
  padding:11px 12px;
  border-bottom:1px solid rgba(0,0,0,.04);
  vertical-align:top;
  line-height:1.5;
}
.data-table tr:last-child td { border-bottom:none; }
.data-table tr:hover td { background:var(--card-hover); }
.en-word { font-weight:700; color:var(--brand); font-size:14px; }
.phon-word { color:#5a5a80; font-style:italic; font-size:12px; }
.uz-word { color:var(--text); }
.speak-btn {
  background:rgba(108,99,255,.15);
  border:1px solid rgba(108,99,255,.3);
  color:var(--brand);
  font-size:10px; padding:3px 8px;
  border-radius:99px; cursor:pointer;
  font-family:'Plus Jakarta Sans',sans-serif;
  transition:all .2s; margin-left:5px;
}
.speak-btn:hover { background:var(--brand); color:#fff; }

/* ══════════════════════════════════════════════
   NUMBER GRID
══════════════════════════════════════════════ */
.num-grid {
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(110px,1fr));
  gap:7px; margin-top:10px;
}
.num-card {
  background:var(--surface-2);
  border:1px solid var(--border);
  border-radius:var(--radius-sm);
  padding:10px 12px;
  display:flex; align-items:center; gap:10px;
  cursor:pointer;
  transition:all .2s;
}
.num-card:hover { border-color:var(--brand-4); background:rgba(255,179,71,.07); }
.num-card .n { font-family:'Unbounded',sans-serif; font-weight:700; color:var(--brand-4); font-size:15px; min-width:28px; }

/* Color grid */
.color-grid {
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(120px,1fr));
  gap:8px; margin-top:10px;
}
.color-card {
  border-radius:12px; padding:14px;
  cursor:pointer;
  transition:transform .2s var(--spring);
  display:flex; flex-direction:column; gap:4px;
}
.color-card:hover { transform:scale(1.05); }
.color-card .c-en { font-weight:700; font-size:14px; }
.color-card .c-uz { font-size:11px; opacity:.75; }

/* ══════════════════════════════════════════════
   DIALOGUE BUBBLES
══════════════════════════════════════════════ */
.dialogue { display:flex; flex-direction:column; gap:10px; padding-top:14px; }
.bubble {
  max-width:82%;
  padding:12px 16px;
  border-radius:16px;
  font-size:13px; line-height:1.6;
}
.bubble.left {
  align-self:flex-start;
  background:var(--surface-2);
  border-bottom-left-radius:4px;
}
.bubble.right {
  align-self:flex-end;
  background:rgba(108,99,255,.12);
  border-bottom-right-radius:4px;
}
.bubble-who { font-size:9px; letter-spacing:1px; text-transform:uppercase; color:var(--text-3); margin-bottom:4px; font-weight:700; }
.bubble-en { font-weight:600; font-size:13px; }
.bubble-uz { font-size:11px; color:var(--text-2); margin-top:3px; }

/* ══════════════════════════════════════════════
   GRAMMAR HIGHLIGHT BOXES
══════════════════════════════════════════════ */
.gram-box {
  background:var(--surface-2);
  border-left:3px solid var(--brand);
  border-radius:0 10px 10px 0;
  padding:12px 16px;
  margin:8px 0;
  font-size:13px; line-height:1.8;
}
.gram-box.green { border-color:var(--brand-3); }
.gram-box.orange { border-color:var(--brand-4); }
.gram-box.red { border-color:var(--brand-2); }

.example-box {
  background:rgba(108,99,255,.07);
  border:1px solid var(--border);
  border-radius:var(--radius-sm);
  padding:12px 14px; margin:8px 0;
}
.example-en { color:var(--brand); font-weight:600; font-size:13px; margin-bottom:3px; }
.example-uz { color:var(--text-2); font-size:12px; }

/* Tags */
.tag {
  display:inline-block;
  background:rgba(108,99,255,.12); color:var(--brand);
  font-size:10px; padding:2px 8px;
  border-radius:99px; font-weight:700; margin-right:3px;
}
.tag.g { background:rgba(0,229,160,.1); color:var(--brand-3); }
.tag.o { background:rgba(255,179,71,.1); color:var(--brand-4); }
.tag.r { background:rgba(255,92,138,.1); color:var(--brand-2); }

.section-label {
  font-family:'Unbounded',sans-serif;
  font-size:9px; letter-spacing:2px;
  text-transform:uppercase; color:var(--text-3);
  margin:20px 0 9px;
}
hr { border:none; border-top:1px solid var(--border); margin:14px 0; }

/* ══════════════════════════════════════════════
   QUIZ
══════════════════════════════════════════════ */
.quiz-wrap {
  background:var(--surface-2);
  border-radius:var(--radius);
  padding:18px;
  margin-top:14px;
}
.quiz-label {
  font-family:'Unbounded',sans-serif;
  font-size:10px; color:var(--brand);
  margin-bottom:8px; letter-spacing:1px;
}
.quiz-q {
  font-size:17px; font-weight:700;
  margin-bottom:14px; line-height:1.4;
}
.quiz-opts {
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:7px; margin-bottom:12px;
}
.quiz-opt {
  background:var(--surface);
  border:1.5px solid var(--border);
  border-radius:var(--radius-sm);
  padding:11px 12px;
  cursor:pointer;
  font-size:13px;
  text-align:center;
  transition:all .2s;
  font-family:'Plus Jakarta Sans',sans-serif;
}
.quiz-opt:hover { border-color:var(--brand); background:rgba(108,99,255,.08); }
.quiz-opt.ok { border-color:var(--brand-3); background:rgba(0,229,160,.1); color:var(--brand-3); font-weight:700; }
.quiz-opt.no { border-color:var(--brand-2); background:rgba(255,92,138,.1); color:var(--brand-2); }
.quiz-next {
  background:var(--brand); color:#fff;
  border:none; border-radius:var(--radius-sm);
  padding:10px 20px;
  font-family:'Plus Jakarta Sans',sans-serif; font-size:13px; font-weight:700;
  cursor:pointer; display:none; transition:all .2s;
}
.quiz-next:hover { opacity:.88; }
.quiz-score { font-size:12px; color:var(--text-2); margin-top:8px; }

/* ══════════════════════════════════════════════
   GRAMMAR QUEST (S3)
══════════════════════════════════════════════ */
.gram-quest-hero {
  background:linear-gradient(135deg,rgba(108,99,255,.08),rgba(255,92,138,.05),rgba(0,229,160,.04));
  border:1px solid rgba(108,99,255,.2);
  border-radius:var(--radius);
  padding:28px 24px;
  margin-bottom:20px;
  position:relative; overflow:hidden;
}
.gram-quest-hero::before {
  content:''; position:absolute;
  top:-80px; right:-80px;
  width:280px; height:280px;
  background:radial-gradient(ellipse,rgba(108,99,255,.15),transparent 70%);
  pointer-events:none;
}
.gram-quest-inner { position:relative; z-index:1; }

.gq-top { display:flex; align-items:center; justify-content:space-between; margin-bottom:12px; flex-wrap:wrap; gap:8px; }
.gq-pill {
  background:linear-gradient(90deg,var(--brand),var(--brand-2));
  color:#fff; font-size:10px;
  letter-spacing:2px; text-transform:uppercase;
  padding:5px 14px; border-radius:99px;
  font-weight:700; font-family:'Space Grotesk',sans-serif;
}
.gq-lb-btn {
  background:rgba(255,179,71,.12);
  border:1px solid rgba(255,179,71,.35);
  color:var(--brand-4);
  font-size:12px; padding:7px 16px;
  border-radius:99px; cursor:pointer;
  font-family:'Plus Jakarta Sans',sans-serif; font-weight:700;
  transition:all .2s; display:flex; align-items:center; gap:6px;
}
.gq-lb-btn:hover { background:rgba(255,179,71,.25); }

.gq-title {
  font-family:'Unbounded',sans-serif;
  font-size:clamp(18px,4vw,28px); font-weight:900;
  margin-bottom:6px;
}
.gq-title span { color:var(--brand); }
.gq-sub { font-size:13px; color:var(--text-2); margin-bottom:16px; }

.xp-wrap { width:100%; height:9px; background:rgba(0,0,0,.05); border-radius:99px; overflow:hidden; margin-bottom:6px; }
.xp-fill {
  height:100%;
  background:linear-gradient(90deg,var(--brand),var(--brand-3));
  border-radius:99px;
  transition:width .8s var(--spring);
}
.xp-lbl { font-size:11px; color:var(--text-2); font-weight:700; letter-spacing:.5px; }

/* Daily Challenge Banner */
.daily-banner {
  background:linear-gradient(135deg,rgba(255,179,71,.12),rgba(255,92,138,.05));
  border:1px solid rgba(255,179,71,.25);
  border-radius:var(--radius);
  padding:16px 20px;
  margin-bottom:14px;
  display:flex; align-items:center; gap:14px;
  cursor:pointer; transition:all .2s;
}
.daily-banner:hover { border-color:rgba(255,179,71,.5); transform:translateY(-2px); }
.daily-icon { font-size:28px; flex-shrink:0; }
.daily-body { flex:1; }
.daily-title { font-weight:700; font-size:14px; color:var(--brand-4); margin-bottom:2px; }
.daily-sub { font-size:12px; color:var(--text-2); }
.daily-arrow { color:var(--brand-4); font-size:18px; }
.daily-done { font-size:11px; color:var(--brand-3); font-weight:700; }

/* Lesson Road */
.lesson-road { display:flex; flex-direction:column; gap:10px; }
.road-connector { width:2px; height:14px; background:linear-gradient(180deg,rgba(108,99,255,.35),rgba(108,99,255,.08)); margin:0 auto; border-radius:99px; }

.lesson-node {
  display:flex; align-items:center; gap:14px;
  background:var(--surface);
  border:1.5px solid var(--border);
  border-radius:var(--radius);
  padding:16px 18px;
  cursor:pointer;
  transition:all .25s var(--ease);
  position:relative;
}
.lesson-node.unlocked:hover {
  border-color:rgba(108,99,255,.5);
  transform:translateX(5px);
  box-shadow:0 6px 28px rgba(108,99,255,.14);
}
.lesson-node.locked { opacity:.5; cursor:not-allowed; filter:grayscale(.5); }
.lesson-node.completed { border-color:rgba(0,229,160,.35); background:rgba(0,229,160,.04); }
.lesson-node.unlocked-active {
  border-color:rgba(108,99,255,.6);
  background:rgba(108,99,255,.07);
  animation:pulse 2.5s ease-in-out infinite;
}
@keyframes pulse {
  0%,100%  { box-shadow:0 0 0 0 rgba(108,99,255,.15); }
  50%      { box-shadow:0 0 0 8px rgba(108,99,255,0); }
}

.ln-icon-wrap {
  width:50px; height:50px;
  border-radius:14px;
  background:var(--surface-2);
  display:flex; align-items:center; justify-content:center;
  font-size:22px; flex-shrink:0; position:relative;
}
.ln-lock { position:absolute; bottom:-4px; right:-4px; font-size:13px; }
.ln-info { flex:1; }
.ln-title { font-family:'Space Grotesk',sans-serif; font-size:13px; font-weight:700; margin-bottom:3px; }
.ln-meta { font-size:11px; color:var(--text-2); display:flex; gap:8px; flex-wrap:wrap; align-items:center; }
.diff-tag {
  padding:2px 8px; border-radius:99px;
  font-size:9px; font-weight:800; letter-spacing:.5px;
}
.diff-a1 { background:rgba(0,229,160,.15); color:#00e5a0; }
.diff-a2 { background:rgba(108,99,255,.15); color:#6c63ff; }
.diff-b1 { background:rgba(255,92,138,.15); color:#ff5c8a; }

.ln-score { text-align:right; flex-shrink:0; }
.ln-score-num { font-family:'Unbounded',sans-serif; font-size:16px; font-weight:900; }
.ln-score-lbl { font-size:9px; color:var(--text-3); letter-spacing:.5px; text-transform:uppercase; }
.ln-stars { font-size:13px; margin-top:2px; }

/* ══════════════════════════════════════════════
   LESSON PANEL
══════════════════════════════════════════════ */
.lesson-panel-header {
  display:flex; align-items:center; gap:12px;
  background:var(--surface);
  border:1px solid var(--border);
  border-radius:var(--radius);
  padding:14px 16px;
  margin-bottom:18px;
}
.lp-back-btn {
  background:none; border:1px solid var(--border); color:var(--text-2);
  font-size:12px; padding:7px 12px; border-radius:var(--radius-sm);
  cursor:pointer; font-family:'Plus Jakarta Sans',sans-serif;
  transition:all .2s; white-space:nowrap;
}
.lp-back-btn:hover { border-color:var(--brand); color:var(--brand); }
.lp-info { flex:1; display:flex; align-items:center; gap:10px; }
.lp-emoji { font-size:24px; }
.lp-title { font-family:'Space Grotesk',sans-serif; font-size:13px; font-weight:700; margin-bottom:2px; }
.lp-sub { font-size:10px; color:var(--text-2); }
.lp-diff-chip {
  background:rgba(108,99,255,.15); color:#554cbd;
  font-size:10px; font-weight:800; padding:4px 10px;
  border-radius:99px; white-space:nowrap;
  font-family:'Space Grotesk',sans-serif;
}

/* Lesson Content Sections */
.lc-section { margin-bottom:22px; }
.lc-heading {
  font-family:'Space Grotesk',sans-serif;
  font-size:10px; letter-spacing:2px;
  text-transform:uppercase; color:var(--brand);
  margin-bottom:10px;
  display:flex; align-items:center; gap:8px;
}
.lc-heading::after { content:''; flex:1; height:1px; background:var(--border); }

.rule-card {
  background:linear-gradient(135deg,rgba(108,99,255,.05),rgba(0,229,160,.03));
  border:1px solid rgba(108,99,255,.18);
  border-radius:var(--radius-sm);
  padding:16px 18px; margin-bottom:12px;
}
.rule-card.warn { background:rgba(255,179,71,.07); border-color:rgba(255,179,71,.25); }
.rule-card.danger { background:rgba(255,92,138,.07); border-color:rgba(255,92,138,.25); }
.rule-card-title { font-weight:700; font-size:13px; margin-bottom:7px; }
.rule-card-body { font-size:13px; line-height:1.8; color:#3a3a5a; }

.formula-box {
  background:rgba(108,99,255,.07);
  border:1px solid rgba(108,99,255,.3);
  border-radius:var(--radius-sm);
  padding:10px 14px;
  font-family:'Space Grotesk',monospace;
  font-size:13px; color:var(--brand);
  margin:8px 0; letter-spacing:.5px;
}

.ex-grid { display:grid; gap:8px; }
.ex-item {
  background:var(--surface-2);
  border-radius:10px;
  padding:12px 14px;
  border-left:3px solid var(--brand);
}
.ex-item.neg { border-color:var(--brand-2); }
.ex-item.q   { border-color:var(--brand-3); }
.ex-en { font-weight:600; font-size:13px; color:#2a2a4a; margin-bottom:3px; }
.ex-uz { font-size:11px; color:var(--text-2); }
.ex-note { font-size:10px; color:var(--brand-4); margin-top:4px; font-style:italic; }

.tip-card {
  background:rgba(255,179,71,.08);
  border:1px solid rgba(255,179,71,.22);
  border-radius:var(--radius-sm);
  padding:12px 14px;
  font-size:12px; line-height:1.7; color:#a07010;
}
.tip-card strong { color:var(--brand-4); }

/* Start Test Area */
.start-test-area { text-align:center; margin:30px 0 10px; }
.start-test-note { font-size:12px; color:var(--text-2); margin-bottom:12px; }
.start-test-btn {
  background:linear-gradient(135deg,var(--brand),var(--brand-2));
  color:#fff; border:none;
  border-radius:var(--radius);
  padding:16px 40px;
  font-family:'Unbounded',sans-serif;
  font-size:13px; font-weight:700;
  cursor:pointer;
  transition:all .25s var(--ease);
  letter-spacing:.5px;
  box-shadow:0 8px 28px rgba(108,99,255,.38);
}
.start-test-btn:hover { transform:translateY(-2px); box-shadow:0 14px 36px rgba(108,99,255,.5); }

/* ══════════════════════════════════════════════
   TEST PANEL
══════════════════════════════════════════════ */
.test-progress-bar-outer {
  width:100%; height:6px;
  background:var(--surface-2); border-radius:99px;
  overflow:hidden; margin-bottom:22px;
}
.test-progress-bar-inner {
  height:100%;
  background:linear-gradient(90deg,var(--brand),var(--brand-3));
  border-radius:99px;
  transition:width .3s var(--ease);
}
.test-score-chip {
  background:rgba(0,229,160,.12);
  border:1px solid rgba(0,229,160,.3);
  color:var(--brand-3);
  font-family:'Unbounded',sans-serif;
  font-size:11px; font-weight:700;
  padding:4px 12px; border-radius:99px;
  white-space:nowrap;
}

.question-block {
  background:var(--surface);
  border:1px solid var(--border);
  border-radius:var(--radius);
  padding:22px;
}
.q-num {
  font-size:10px; color:var(--brand);
  letter-spacing:2px; text-transform:uppercase;
  margin-bottom:10px; font-weight:700;
  font-family:'Space Grotesk',sans-serif;
}
</style>
</head>
<body>
  <!-- Bu yerda sizning asosiy HTML kontentingiz davom etadi -->
</body>
</html>
