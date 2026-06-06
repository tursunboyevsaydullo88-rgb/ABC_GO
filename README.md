<!DOCTYPE html>
<html lang="uz" data-theme="dark">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<meta name="description" content="Ingliz tilini o'zbek tilida o'rgan - A1 dan B1 gacha">
<meta name="theme-color" content="#0d0d1a">
<title>LinguaUZ — Ingliz Tili Platformasi</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=Space+Grotesk:wght@400;500;700&family=Unbounded:wght@700;900&display=swap" rel="stylesheet">
<link rel="manifest" href="manifest.json">
<style>
/* ══════════════════════════════════════════════
   DESIGN TOKENS — DARK/LIGHT MODE
══════════════════════════════════════════════ */
:root {
  /* Brand */
  --brand: #6c63ff;
  --brand-2: #ff5c8a;
  --brand-3: #00e5a0;
  --brand-4: #ffb347;
  --brand-glow: rgba(108,99,255,.22);

  /* Dark theme (default) */
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

  /* Transitions */
  --ease: cubic-bezier(.25,.46,.45,.94);
  --spring: cubic-bezier(.34,1.56,.64,1);

  /* Layout */
  --max: 960px;
  --radius: 18px;
  --radius-sm: 10px;
  --nav-h: 64px;
}

[data-theme="light"] {
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
  background:rgba(13,13,26,.85);
  backdrop-filter:blur(20px) saturate(180%);
  border-bottom:1px solid var(--border);
  display:flex; align-items:center;
  padding:0 20px;
  gap:12px;
}
[data-theme="light"] .navbar {
  background:rgba(245,245,255,.85);
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
  border-bottom:1px solid rgba(255,255,255,.03);
  vertical-align:top;
  line-height:1.5;
}
[data-theme="light"] .data-table td { border-bottom-color:rgba(0,0,0,.04); }
.data-table tr:last-child td { border-bottom:none; }
.data-table tr:hover td { background:var(--card-hover); }
.en-word { font-weight:700; color:var(--brand); font-size:14px; }
.phon-word { color:#a0a0d0; font-style:italic; font-size:12px; }
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
  background:rgba(108,99,255,.18);
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
  background:linear-gradient(135deg,rgba(108,99,255,.12),rgba(255,92,138,.08),rgba(0,229,160,.06));
  border:1px solid rgba(108,99,255,.25);
  border-radius:var(--radius);
  padding:28px 24px;
  margin-bottom:20px;
  position:relative; overflow:hidden;
}
.gram-quest-hero::before {
  content:''; position:absolute;
  top:-80px; right:-80px;
  width:280px; height:280px;
  background:radial-gradient(ellipse,rgba(108,99,255,.2),transparent 70%);
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

.xp-wrap { width:100%; height:9px; background:rgba(255,255,255,.07); border-radius:99px; overflow:hidden; margin-bottom:6px; }
.xp-fill {
  height:100%;
  background:linear-gradient(90deg,var(--brand),var(--brand-3));
  border-radius:99px;
  transition:width .8s var(--spring);
}
.xp-lbl { font-size:11px; color:var(--text-2); font-weight:700; letter-spacing:.5px; }

/* Daily Challenge Banner */
.daily-banner {
  background:linear-gradient(135deg,rgba(255,179,71,.15),rgba(255,92,138,.08));
  border:1px solid rgba(255,179,71,.3);
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
  0%,100%  { box-shadow:0 0 0 0 rgba(108,99,255,.2); }
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
  background:rgba(108,99,255,.15); color:#b0a8ff;
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
  background:linear-gradient(135deg,rgba(108,99,255,.08),rgba(0,229,160,.04));
  border:1px solid rgba(108,99,255,.2);
  border-radius:var(--radius-sm);
  padding:16px 18px; margin-bottom:12px;
}
.rule-card.warn { background:rgba(255,179,71,.07); border-color:rgba(255,179,71,.25); }
.rule-card.danger { background:rgba(255,92,138,.07); border-color:rgba(255,92,138,.25); }
.rule-card-title { font-weight:700; font-size:13px; margin-bottom:7px; }
.rule-card-body { font-size:13px; line-height:1.8; color:#c0c0e0; }

.formula-box {
  background:rgba(0,0,0,.35);
  border:1px solid rgba(108,99,255,.3);
  border-radius:var(--radius-sm);
  padding:10px 14px;
  font-family:'Space Grotesk',monospace;
  font-size:13px; color:var(--brand);
  margin:8px 0; letter-spacing:.5px;
}
[data-theme="light"] .formula-box { background:rgba(108,99,255,.07); }

.ex-grid { display:grid; gap:8px; }
.ex-item {
  background:var(--surface-2);
  border-radius:10px;
  padding:12px 14px;
  border-left:3px solid var(--brand);
}
.ex-item.neg { border-color:var(--brand-2); }
.ex-item.q   { border-color:var(--brand-3); }
.ex-en { font-weight:600; font-size:13px; color:#e0dcff; margin-bottom:3px; }
[data-theme="light"] .ex-en { color:#2a2a4a; }
.ex-uz { font-size:11px; color:var(--text-2); }
.ex-note { font-size:10px; color:var(--brand-4); margin-top:4px; font-style:italic; }

.tip-card {
  background:rgba(255,179,71,.08);
  border:1px solid rgba(255,179,71,.22);
  border-radius:var(--radius-sm);
  padding:12px 14px;
  font-size:12px; line-height:1.7; color:#e8c070;
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
.q-text { font-size:17px; font-weight:700; margin-bottom:18px; line-height:1.5; }

.q-opts {
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:8px; margin-bottom:14px;
}
.q-opt {
  background:var(--surface-2);
  border:1.5px solid var(--border);
  border-radius:var(--radius-sm);
  padding:12px 14px;
  cursor:pointer; font-size:13px;
  text-align:center;
  transition:all .2s;
  font-family:'Plus Jakarta Sans',sans-serif;
}
.q-opt:hover:not(.done) { border-color:var(--brand); background:rgba(108,99,255,.08); }
.q-opt.correct { border-color:var(--brand-3); background:rgba(0,229,160,.12); color:var(--brand-3); font-weight:700; }
.q-opt.wrong   { border-color:var(--brand-2); background:rgba(255,92,138,.10); color:var(--brand-2); }
.q-opt.done    { cursor:default; }

.q-explain {
  background:rgba(0,229,160,.07);
  border:1px solid rgba(0,229,160,.2);
  border-radius:var(--radius-sm);
  padding:10px 14px;
  font-size:12px; color:#80f0c0;
  margin-top:10px; display:none;
}
.q-fill-input {
  width:100%;
  background:var(--surface-2);
  border:1.5px solid var(--border);
  border-radius:var(--radius-sm);
  padding:12px 14px;
  color:var(--text); font-size:14px;
  font-family:'Plus Jakarta Sans',sans-serif;
  transition:border-color .2s; outline:none;
}
.q-fill-input:focus { border-color:var(--brand); }
.q-fill-input.correct { border-color:var(--brand-3); background:rgba(0,229,160,.07); }
.q-fill-input.wrong   { border-color:var(--brand-2); background:rgba(255,92,138,.07); }

.q-submit-btn {
  background:var(--brand); color:#fff;
  border:none; border-radius:var(--radius-sm);
  padding:10px 22px; font-size:13px; font-weight:700;
  cursor:pointer; margin-top:10px;
  font-family:'Plus Jakarta Sans',sans-serif;
  transition:all .2s;
}
.q-submit-btn:hover { opacity:.85; }

.q-next-btn {
  background:linear-gradient(135deg,var(--brand),#8a80ff);
  color:#fff; border:none;
  border-radius:var(--radius-sm);
  padding:12px 28px;
  font-family:'Space Grotesk',sans-serif; font-size:12px; font-weight:700;
  cursor:pointer; display:none;
  transition:all .2s; letter-spacing:.5px;
  margin-top:12px;
}
.q-next-btn:hover { opacity:.88; transform:translateY(-1px); }

/* ══════════════════════════════════════════════
   RESULT PANEL
══════════════════════════════════════════════ */
.result-card {
  background:linear-gradient(135deg,rgba(108,99,255,.1),rgba(255,92,138,.06));
  border:1px solid rgba(108,99,255,.3);
  border-radius:calc(var(--radius)*1.3);
  padding:36px 28px;
  text-align:center;
  max-width:460px; margin:20px auto;
  animation:resultPop .5s var(--spring);
}
@keyframes resultPop { from{transform:scale(.85);opacity:0} to{transform:scale(1);opacity:1} }

.result-emoji { font-size:60px; margin-bottom:10px; }
.result-score {
  font-family:'Unbounded',sans-serif;
  font-size:46px; font-weight:900; margin-bottom:5px;
}
.result-score.pass { color:var(--brand-3); }
.result-score.fail { color:var(--brand-2); }
.result-msg { font-size:17px; font-weight:700; color:#b0a8ff; margin-bottom:8px; }
.result-detail { font-size:12px; color:var(--text-2); margin-bottom:22px; line-height:1.7; }

.unlock-banner {
  background:linear-gradient(135deg,rgba(0,229,160,.12),rgba(108,99,255,.12));
  border:1px solid rgba(0,229,160,.3);
  border-radius:var(--radius-sm);
  padding:14px 18px;
  margin-bottom:22px;
  position:relative; overflow:hidden;
}
.unlock-banner::before {
  content:''; position:absolute; inset:0;
  background:radial-gradient(ellipse at center,rgba(0,229,160,.15),transparent);
  animation:glow 1.5s ease-in-out infinite;
}
@keyframes glow { 0%,100%{opacity:.3} 50%{opacity:1} }
.unlock-text {
  font-family:'Unbounded',sans-serif;
  font-size:13px; font-weight:700; color:var(--brand-3);
  position:relative; z-index:1;
}

.result-btns { display:flex; gap:8px; justify-content:center; flex-wrap:wrap; }
.rbtn {
  border:none; border-radius:var(--radius-sm);
  padding:12px 20px;
  font-family:'Plus Jakarta Sans',sans-serif;
  font-size:13px; font-weight:700;
  cursor:pointer; transition:all .2s;
}
.rbtn.retry { background:rgba(108,99,255,.15); color:var(--brand); border:1px solid rgba(108,99,255,.3); }
.rbtn.retry:hover { background:rgba(108,99,255,.25); }
.rbtn.next-btn { background:linear-gradient(135deg,var(--brand),var(--brand-3)); color:#fff; }
.rbtn.next-btn:hover { opacity:.88; }
.rbtn.home-btn { background:var(--surface-2); color:var(--text-2); border:1px solid var(--border); }

/* ══════════════════════════════════════════════
   MODALS
══════════════════════════════════════════════ */
.modal-overlay {
  display:none; position:fixed; inset:0;
  background:rgba(0,0,0,.88);
  backdrop-filter:blur(14px);
  z-index:1000;
  align-items:center; justify-content:center;
  padding:14px;
}
.modal-overlay.open { display:flex; }

.modal-box {
  background:var(--surface);
  border:1px solid rgba(108,99,255,.3);
  border-radius:calc(var(--radius)*1.3);
  padding:24px 20px;
  max-width:420px; width:100%;
  animation:modalIn .3s var(--spring);
  position:relative;
}
.modal-wide { max-width:480px; }
@keyframes modalIn { from{opacity:0;transform:scale(.82)} to{opacity:1;transform:scale(1)} }

/* Letter modal canvas */
.canvas-wrap {
  width:240px; height:240px;
  margin:0 auto 14px;
  border-radius:14px; overflow:hidden;
  background:var(--surface-2);
  border:2px solid var(--border);
  position:relative;
}
#letterCanvas { display:block; width:240px; height:240px; }

.progress-bar-outer { width:100%; height:4px; background:var(--surface-3); border-radius:99px; margin-bottom:12px; overflow:hidden; }
.progress-bar-inner { height:100%; background:var(--brand); border-radius:99px; transition:width .05s linear; }

.ctrl-row { display:flex; gap:7px; justify-content:center; margin-bottom:12px; }
.ctrl-btn {
  background:var(--surface-2); border:1px solid var(--border); color:var(--text);
  border-radius:var(--radius-sm); padding:7px 16px;
  cursor:pointer; font-size:12px; font-family:'Plus Jakarta Sans',sans-serif;
  transition:all .2s;
}
.ctrl-btn:hover { background:var(--brand); border-color:var(--brand); color:#fff; }
.ctrl-btn.playing { background:rgba(0,229,160,.12); border-color:var(--brand-3); color:var(--brand-3); }

.modal-letter { font-family:'Unbounded',sans-serif; font-size:19px; font-weight:900; color:var(--brand); margin-bottom:3px; }
.modal-phon   { font-size:15px; color:#b0a8ff; margin-bottom:3px; }
.modal-ex     { font-size:12px; color:var(--text-2); margin-bottom:12px; }

.word-pills { display:flex; gap:7px; justify-content:center; flex-wrap:wrap; margin-bottom:14px; }
.word-pill {
  background:var(--surface-2); border:1px solid var(--border);
  border-radius:99px; padding:5px 14px;
  font-size:12px; cursor:pointer; transition:all .2s;
}
.word-pill:hover { border-color:var(--brand); color:var(--brand); }

.speak-big-btn {
  background:var(--brand); color:#fff;
  border:none; border-radius:var(--radius-sm);
  padding:12px; font-size:14px; font-weight:700;
  cursor:pointer; font-family:'Plus Jakarta Sans',sans-serif;
  width:100%; margin-bottom:8px; transition:all .2s;
}
.speak-big-btn:hover { opacity:.85; }
.modal-close-btn {
  background:var(--surface-2); border:1px solid var(--border); color:var(--text);
  border-radius:var(--radius-sm); padding:10px;
  cursor:pointer; font-family:'Plus Jakarta Sans',sans-serif; font-size:13px; width:100%;
}

/* Leaderboard */
.lb-header { display:flex; align-items:center; justify-content:space-between; margin-bottom:18px; }
.lb-title { font-family:'Unbounded',sans-serif; font-size:16px; font-weight:900; color:var(--brand-4); }
.lb-close-btn {
  background:var(--surface-2); border:1px solid var(--border); color:var(--text-2);
  border-radius:var(--radius-sm); padding:5px 12px; cursor:pointer;
  font-family:'Plus Jakarta Sans',sans-serif; font-size:12px; transition:all .2s;
}
.lb-close-btn:hover { color:var(--text); }

.lb-input-row { display:flex; gap:8px; margin-bottom:16px; }
.lb-input {
  flex:1; background:var(--surface-2); border:1px solid var(--border);
  border-radius:var(--radius-sm); padding:10px 12px;
  color:var(--text); font-size:13px;
  font-family:'Plus Jakarta Sans',sans-serif; outline:none;
  transition:border-color .2s;
}
.lb-input:focus { border-color:var(--brand); }
.lb-save-btn {
  background:var(--brand); color:#fff;
  border:none; border-radius:var(--radius-sm);
  padding:10px 16px; font-size:13px; font-weight:700;
  cursor:pointer; font-family:'Plus Jakarta Sans',sans-serif;
  white-space:nowrap; transition:all .2s;
}
.lb-save-btn:hover { opacity:.88; }

.lb-entry {
  display:flex; align-items:center; gap:12px;
  padding:11px 13px;
  border-radius:var(--radius-sm);
  margin-bottom:6px;
  background:var(--surface-2); border:1px solid var(--border);
  transition:all .2s;
}
.lb-entry.me { border-color:rgba(108,99,255,.5); background:rgba(108,99,255,.08); }
.lb-rank { font-family:'Unbounded',sans-serif; font-size:14px; font-weight:900; min-width:30px; text-align:center; }
.lb-rank.gold   { color:#ffd700; }
.lb-rank.silver { color:#c0c0c0; }
.lb-rank.bronze { color:#cd7f32; }
.lb-name { flex:1; font-size:13px; font-weight:600; }
.lb-lessons { font-size:12px; color:var(--text-2); }
.lb-xp { font-family:'Unbounded',sans-serif; font-size:12px; color:var(--brand); font-weight:700; }
.lb-empty { text-align:center; color:var(--text-2); font-size:13px; padding:24px; }

/* Max-height scroll for lb */
#lbList { max-height:320px; overflow-y:auto; }

/* ══════════════════════════════════════════════
   VOCABULARY GAME
══════════════════════════════════════════════ */
.game-banner {
  background:linear-gradient(135deg,rgba(0,229,160,.1),rgba(108,99,255,.08));
  border:1px solid rgba(0,229,160,.25);
  border-radius:var(--radius);
  padding:22px;
  margin-bottom:14px;
  text-align:center;
}
.game-score-row { display:flex; justify-content:space-between; align-items:center; margin-bottom:16px; }
.game-score-chip {
  background:var(--surface-2); border:1px solid var(--border);
  border-radius:99px; padding:6px 16px;
  font-family:'Unbounded',sans-serif; font-size:12px; font-weight:700;
  color:var(--brand-3);
}
.game-lives { font-size:14px; letter-spacing:2px; }
.game-word {
  font-family:'Unbounded',sans-serif;
  font-size:clamp(26px,6vw,42px); font-weight:900;
  margin-bottom:8px; color:var(--brand);
}
.game-hint { font-size:13px; color:var(--text-2); margin-bottom:18px; }
.game-opts {
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:8px;
}
.game-opt {
  background:var(--surface);
  border:1.5px solid var(--border);
  border-radius:var(--radius-sm);
  padding:13px 14px;
  cursor:pointer; font-size:13px; font-weight:600;
  text-align:center;
  transition:all .2s;
}
.game-opt:hover { border-color:var(--brand); background:rgba(108,99,255,.08); }
.game-opt.correct { border-color:var(--brand-3); background:rgba(0,229,160,.12); color:var(--brand-3); }
.game-opt.wrong   { border-color:var(--brand-2); background:rgba(255,92,138,.10); color:var(--brand-2); }

/* ══════════════════════════════════════════════
   ACHIEVEMENTS PAGE
══════════════════════════════════════════════ */
.ach-grid {
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(160px,1fr));
  gap:12px;
}
.ach-card {
  background:var(--surface);
  border:1px solid var(--border);
  border-radius:var(--radius);
  padding:20px 16px;
  text-align:center;
  transition:all .25s;
  position:relative; overflow:hidden;
}
.ach-card.earned {
  border-color:rgba(255,179,71,.4);
  background:linear-gradient(135deg,rgba(255,179,71,.08),rgba(255,92,138,.04));
}
.ach-card.locked { opacity:.45; filter:grayscale(.7); }
.ach-emoji { font-size:36px; margin-bottom:10px; }
.ach-name { font-family:'Space Grotesk',sans-serif; font-size:13px; font-weight:700; margin-bottom:5px; }
.ach-desc { font-size:11px; color:var(--text-2); line-height:1.5; }
.ach-earned-badge {
  position:absolute; top:10px; right:10px;
  background:var(--brand-4); color:#fff;
  font-size:9px; font-weight:800; padding:2px 7px;
  border-radius:99px; letter-spacing:.5px;
}

/* ══════════════════════════════════════════════
   STREAK & CALENDAR
══════════════════════════════════════════════ */
.streak-card {
  background:linear-gradient(135deg,rgba(255,179,71,.12),rgba(255,92,138,.06));
  border:1px solid rgba(255,179,71,.3);
  border-radius:var(--radius);
  padding:24px 20px;
  display:flex; align-items:center; gap:18px;
  margin-bottom:16px;
}
.streak-fire { font-size:48px; }
.streak-info { flex:1; }
.streak-num {
  font-family:'Unbounded',sans-serif;
  font-size:36px; font-weight:900; color:var(--brand-4);
  line-height:1;
}
.streak-lbl { font-size:12px; color:var(--text-2); margin-top:4px; }

/* ══════════════════════════════════════════════
   TOAST NOTIFICATION
══════════════════════════════════════════════ */
.toast {
  position:fixed; bottom:24px; left:50%;
  transform:translateX(-50%) translateY(80px);
  background:var(--surface);
  border:1px solid var(--border);
  border-radius:var(--radius-sm);
  padding:12px 20px;
  font-size:13px; font-weight:600;
  box-shadow:0 8px 28px var(--shadow);
  z-index:2000;
  transition:transform .3s var(--spring), opacity .3s;
  opacity:0; pointer-events:none;
  white-space:nowrap;
}
.toast.show { transform:translateX(-50%) translateY(0); opacity:1; }
.toast.xp { color:var(--brand-3); border-color:rgba(0,229,160,.3); }
.toast.error { color:var(--brand-2); border-color:rgba(255,92,138,.3); }

/* ══════════════════════════════════════════════
   MOBILE BOTTOM NAV
══════════════════════════════════════════════ */
.bottom-nav {
  display:none;
  position:fixed; bottom:0; left:0; right:0;
  background:rgba(13,13,26,.92);
  backdrop-filter:blur(20px);
  border-top:1px solid var(--border);
  padding:8px 0 env(safe-area-inset-bottom,8px);
  z-index:100;
}
[data-theme="light"] .bottom-nav { background:rgba(245,245,255,.92); }

.bottom-nav-inner {
  display:flex; justify-content:space-around; align-items:center;
  max-width:var(--max); margin:0 auto;
}
.bnav-btn {
  display:flex; flex-direction:column; align-items:center; gap:3px;
  background:none; border:none; color:var(--text-3);
  cursor:pointer; padding:6px 12px;
  font-family:'Plus Jakarta Sans',sans-serif;
  transition:color .2s;
  min-width:56px;
}
.bnav-btn.active { color:var(--brand); }
.bnav-icon { font-size:20px; }
.bnav-lbl { font-size:9px; font-weight:700; letter-spacing:.5px; text-transform:uppercase; }

@media (max-width:600px) {
  .navbar { padding:0 12px; }
  .nav-tabs { display:none; }
  .bottom-nav { display:block; }
  .main { padding-bottom:80px; }
  .q-opts, .quiz-opts, .game-opts { grid-template-columns:1fr; }
  .hero-stats { gap:18px; }
  .course-grid { grid-template-columns:repeat(2,1fr); }
  .ach-grid { grid-template-columns:repeat(2,1fr); }
}

/* ══════════════════════════════════════════════
   UTILITY
══════════════════════════════════════════════ */
.mt-8  { margin-top:8px; }
.mt-14 { margin-top:14px; }
.mt-20 { margin-top:20px; }
.mb-8  { margin-bottom:8px; }
.mb-16 { margin-bottom:16px; }
.hidden { display:none !important; }
.text-center { text-align:center; }
.flex-center { display:flex; align-items:center; justify-content:center; }
.gap-8 { gap:8px; }
.w100 { width:100%; }
</style>
</head>
<body>

<!-- Background canvas -->
<canvas id="particles"></canvas>

<!-- ═══════════ TOP NAVBAR ═══════════ -->
<nav class="navbar">
  <span class="nav-logo" onclick="goPage('home')">🌐 LinguaUZ</span>
  <div class="nav-tabs" id="navTabs">
    <button class="nav-tab active" onclick="goPage('home')" data-page="home">🏠 Bosh sahifa</button>
    <button class="nav-tab" onclick="goPage('alphabet')" data-page="alphabet">🔤 Alifbo</button>
    <button class="nav-tab" onclick="goPage('words')" data-page="words">📚 So'zlar</button>
    <button class="nav-tab" onclick="goPage('grammar')" data-page="grammar">🎮 Grammatika</button>
    <button class="nav-tab" onclick="goPage('conversation')" data-page="conversation">💬 Suhbat</button>
    <button class="nav-tab" onclick="goPage('advanced')" data-page="advanced">🚀 Keyingi Level</button>
    <button class="nav-tab" onclick="goPage('game')" data-page="game">🎯 O'yin</button>
    <button class="nav-tab" onclick="goPage('achievements')" data-page="achievements">🏆 Yutuqlar</button>
  </div>
  <div class="nav-right">
    <div class="nav-streak" id="navStreak" title="Kunlik seriya">🔥 <span id="streakCount">0</span></div>
    <div class="nav-xp" onclick="goPage('achievements')">
      <span class="nav-xp-icon">⚡</span>
      <span id="navXP">0 XP</span>
    </div>
    <button class="theme-btn" onclick="toggleTheme()" id="themeBtn" title="Tema o'zgartirish">🌙</button>
  </div>
</nav>

<!-- ═══════════ MAIN CONTENT ═══════════ -->
<div class="main">

<!-- ═══ PAGE: HOME ═══ -->
<div class="page active" id="page-home">

  <div class="hero-section">
    <div class="hero-glow"></div>
    <div class="hero-badge">🇬🇧 A1 → B1 · O'zbek tilida · Offline ishlaydi</div>
    <h1 class="hero-title">
      Inglizchani<br>
      <span class="grad">bosqichma-bosqich</span><br>
      o'rgan
    </h1>
    <p class="hero-sub">Professional ingliz tili kursi. Grammatika, lug'at, suhbat va testlar — barchasi o'zbek tilida.</p>
    <div class="hero-cta">
      <button class="btn-primary" onclick="goPage('grammar')">🚀 Darsni boshlash</button>
      <button class="btn-secondary" onclick="goPage('alphabet')">🔤 Alifbodan boshlash</button>
    </div>
  </div>

  <div class="hero-stats" id="heroStats">
    <div class="hero-stat">
      <div class="hero-stat-num" id="statLessons">0</div>
      <div class="hero-stat-lbl">Tugatilgan dars</div>
    </div>
    <div class="hero-stat">
      <div class="hero-stat-num" id="statXP">0</div>
      <div class="hero-stat-lbl">XP ballari</div>
    </div>
    <div class="hero-stat">
      <div class="hero-stat-num" id="statStreak">0</div>
      <div class="hero-stat-lbl">Kun seriyasi</div>
    </div>
    <div class="hero-stat">
      <div class="hero-stat-num" id="statBadges">0</div>
      <div class="hero-stat-lbl">Yutuqlar</div>
    </div>
  </div>

  <div class="section-title">📋 Kurs bo'limlari</div>
  <div class="course-grid">
    <div class="course-card" style="--card-accent:#6c63ff" onclick="goPage('alphabet')">
      <div class="course-card-icon">🔤</div>
      <div class="course-card-num">Bo'lim 1</div>
      <div class="course-card-title">Alifbo va Salomlashish</div>
      <div class="course-card-sub">A–Z harflar · Birinchi iboralar · O'zini tanishtirish</div>
      <div class="course-card-progress">
        <div class="prog-bar"><div class="prog-fill" id="prog-0" style="width:0%"></div></div>
        <div class="prog-label" id="prog-lbl-0">Boshlanmagan</div>
      </div>
    </div>
    <div class="course-card" style="--card-accent:#ff5c8a" onclick="goPage('words')">
      <div class="course-card-icon">📚</div>
      <div class="course-card-num">Bo'lim 2</div>
      <div class="course-card-title">So'zlar Olami</div>
      <div class="course-card-sub">Sonlar · Ranglar · Kunlar · Oylar · Kasblar</div>
      <div class="course-card-progress">
        <div class="prog-bar"><div class="prog-fill" id="prog-1" style="width:0%"></div></div>
        <div class="prog-label" id="prog-lbl-1">Boshlanmagan</div>
      </div>
    </div>
    <div class="course-card" style="--card-accent:#00e5a0" onclick="goPage('grammar')">
      <div class="course-card-icon">🎮</div>
      <div class="course-card-num">Bo'lim 3</div>
      <div class="course-card-title">Grammar Quest</div>
      <div class="course-card-sub">7 ta dars · Test tizimi · Qulfni ochish</div>
      <div class="course-card-progress">
        <div class="prog-bar"><div class="prog-fill" id="prog-2" style="width:0%"></div></div>
        <div class="prog-label" id="prog-lbl-2">Boshlanmagan</div>
      </div>
    </div>
    <div class="course-card" style="--card-accent:#ffb347" onclick="goPage('conversation')">
      <div class="course-card-icon">💬</div>
      <div class="course-card-num">Bo'lim 4</div>
      <div class="course-card-title">Suhbatlar</div>
      <div class="course-card-sub">Do'kon · Restoran · Yo'l · Telefon</div>
      <div class="course-card-progress">
        <div class="prog-bar"><div class="prog-fill" id="prog-3" style="width:100%"></div></div>
        <div class="prog-label">Mavjud</div>
      </div>
    </div>
    <div class="course-card" style="--card-accent:#b0a8ff" onclick="goPage('advanced')">
      <div class="course-card-icon">🚀</div>
      <div class="course-card-num">Bo'lim 5</div>
      <div class="course-card-title">Keyingi Level</div>
      <div class="course-card-sub">Past · Future · Modal · Comparison</div>
      <div class="course-card-progress">
        <div class="prog-bar"><div class="prog-fill" style="width:100%"></div></div>
        <div class="prog-label">Mavjud</div>
      </div>
    </div>
    <div class="course-card" style="--card-accent:#36a2eb" onclick="goPage('game')">
      <div class="course-card-icon">🎯</div>
      <div class="course-card-num">Bonus</div>
      <div class="course-card-title">Vocabulary Game</div>
      <div class="course-card-sub">So'zlarni bilasizmi? XP yig'ing!</div>
      <div class="course-card-progress">
        <div class="prog-bar"><div class="prog-fill" style="width:100%"></div></div>
        <div class="prog-label">Har doim ochiq</div>
      </div>
    </div>
  </div>

  <div class="section-title">📊 Mening progressim</div>
  <div class="dashboard-grid">
    <div class="dash-card">
      <div class="dash-card-num" style="color:var(--brand)" id="dashXP">0</div>
      <div class="dash-card-lbl">Jami XP</div>
    </div>
    <div class="dash-card">
      <div class="dash-card-num" style="color:var(--brand-3)" id="dashLessons">0</div>
      <div class="dash-card-lbl">Darslar</div>
    </div>
    <div class="dash-card">
      <div class="dash-card-num" style="color:var(--brand-4)" id="dashStreak">0</div>
      <div class="dash-card-lbl">Seriya 🔥</div>
    </div>
    <div class="dash-card">
      <div class="dash-card-num" style="color:var(--brand-2)" id="dashBadges">0</div>
      <div class="dash-card-lbl">Yutuqlar</div>
    </div>
  </div>

</div><!-- /page-home -->

<!-- ═══ PAGE: ALPHABET ═══ -->
<div class="page" id="page-alphabet">

  <div class="section-title mt-8">🔤 Ingliz Alifbosi</div>

  <div class="card open">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(108,99,255,.15)">📝</div>
      <div class="card-meta">
        <h3>Ingliz Alifbosi (A–Z)</h3>
        <p>Har bir harfni bosing → animatsiya + ovoz</p>
      </div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <div class="alpha-grid" id="alphaGrid"></div>
    </div>
  </div>

  <div class="card open">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(255,92,138,.15)">👋</div>
      <div class="card-meta">
        <h3>Salomlashish</h3>
        <p>Birinchi muhim iboralar</p>
      </div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <table class="data-table">
        <tr><th>Inglizcha</th><th>Talaffuz</th><th>O'zbekcha</th></tr>
        <tr><td class="en-word">Hello <button class="speak-btn" onclick="sp('Hello')">🔊</button></td><td class="phon-word">[heˈloʊ]</td><td class="uz-word">Salom</td></tr>
        <tr><td class="en-word">Hi <button class="speak-btn" onclick="sp('Hi')">🔊</button></td><td class="phon-word">[haɪ]</td><td class="uz-word">Salom (norasmiy)</td></tr>
        <tr><td class="en-word">Good morning <button class="speak-btn" onclick="sp('Good morning')">🔊</button></td><td class="phon-word">[gʊd ˈmɔːrnɪŋ]</td><td class="uz-word">Xayrli tong</td></tr>
        <tr><td class="en-word">Good afternoon <button class="speak-btn" onclick="sp('Good afternoon')">🔊</button></td><td class="phon-word">[gʊd ˌæftərˈnuːn]</td><td class="uz-word">Xayrli kun</td></tr>
        <tr><td class="en-word">Good evening <button class="speak-btn" onclick="sp('Good evening')">🔊</button></td><td class="phon-word">[gʊd ˈiːvnɪŋ]</td><td class="uz-word">Xayrli kech</td></tr>
        <tr><td class="en-word">Goodbye <button class="speak-btn" onclick="sp('Goodbye')">🔊</button></td><td class="phon-word">[ˌgʊdˈbaɪ]</td><td class="uz-word">Xayr</td></tr>
        <tr><td class="en-word">How are you? <button class="speak-btn" onclick="sp('How are you?')">🔊</button></td><td class="phon-word">[haʊ ɑːr juː]</td><td class="uz-word">Qandaysiz?</td></tr>
        <tr><td class="en-word">I'm fine, thank you <button class="speak-btn" onclick="sp(&quot;I'm fine, thank you&quot;)">🔊</button></td><td class="phon-word">[aɪm faɪn θæŋk juː]</td><td class="uz-word">Yaxshi, rahmat</td></tr>
        <tr><td class="en-word">Nice to meet you <button class="speak-btn" onclick="sp('Nice to meet you')">🔊</button></td><td class="phon-word">[naɪs tə miːt juː]</td><td class="uz-word">Tanishganimdan xursandman</td></tr>
        <tr><td class="en-word">See you later <button class="speak-btn" onclick="sp('See you later')">🔊</button></td><td class="phon-word">[siː juː ˈleɪtər]</td><td class="uz-word">Ko'rishguncha</td></tr>
      </table>
    </div>
  </div>

  <div class="card">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(0,229,160,.15)">😊</div>
      <div class="card-meta">
        <h3>O'zingni tanishtirish</h3>
        <p>My name is... I am from...</p>
      </div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <table class="data-table">
        <tr><th>Inglizcha</th><th>O'zbekcha</th></tr>
        <tr><td class="en-word">My name is Ali. <button class="speak-btn" onclick="sp('My name is Ali.')">🔊</button></td><td class="uz-word">Mening ismim Ali.</td></tr>
        <tr><td class="en-word">I am from Uzbekistan. <button class="speak-btn" onclick="sp('I am from Uzbekistan.')">🔊</button></td><td class="uz-word">Men O'zbekistondan.</td></tr>
        <tr><td class="en-word">I am 20 years old. <button class="speak-btn" onclick="sp('I am 20 years old.')">🔊</button></td><td class="uz-word">Men 20 yoshdaman.</td></tr>
        <tr><td class="en-word">I am a student. <button class="speak-btn" onclick="sp('I am a student.')">🔊</button></td><td class="uz-word">Men talabaman.</td></tr>
        <tr><td class="en-word">I live in Tashkent. <button class="speak-btn" onclick="sp('I live in Tashkent.')">🔊</button></td><td class="uz-word">Men Toshkentda yashayman.</td></tr>
        <tr><td class="en-word">What is your name? <button class="speak-btn" onclick="sp('What is your name?')">🔊</button></td><td class="uz-word">Ismingiz nima?</td></tr>
        <tr><td class="en-word">Where are you from? <button class="speak-btn" onclick="sp('Where are you from?')">🔊</button></td><td class="uz-word">Qayerdansiz?</td></tr>
        <tr><td class="en-word">How old are you? <button class="speak-btn" onclick="sp('How old are you?')">🔊</button></td><td class="uz-word">Nechanchi yoshdasiz?</td></tr>
      </table>
      <div class="section-label mt-14">Namuna suhbat</div>
      <div class="dialogue">
        <div class="bubble left"><div class="bubble-who">A — Sarah</div><div class="bubble-en">Hello! My name is Sarah. What is your name?</div><div class="bubble-uz">Salom! Mening ismim Sarah. Ismingiz nima?</div></div>
        <div class="bubble right"><div class="bubble-who">B — Ali</div><div class="bubble-en">Hi! My name is Ali. Nice to meet you!</div><div class="bubble-uz">Salom! Mening ismim Ali. Tanishganimdan xursandman!</div></div>
        <div class="bubble left"><div class="bubble-who">A</div><div class="bubble-en">Where are you from?</div><div class="bubble-uz">Qayerdansiz?</div></div>
        <div class="bubble right"><div class="bubble-who">B</div><div class="bubble-en">I am from Uzbekistan. And you?</div><div class="bubble-uz">Men O'zbekistondan. Siz-chi?</div></div>
      </div>
    </div>
  </div>
</div><!-- /page-alphabet -->

<!-- ═══ PAGE: WORDS ═══ -->
<div class="page" id="page-words">

  <div class="section-title mt-8">📚 So'zlar Olami</div>

  <div class="card open">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(255,179,71,.15)">🔢</div>
      <div class="card-meta"><h3>Sonlar (1–100)</h3><p>Bosing va eshiting</p></div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <div class="section-label">1–20</div>
      <div class="num-grid" id="numGrid1"></div>
      <div class="section-label mt-14">O'nlar</div>
      <div class="num-grid" id="numGrid2"></div>
    </div>
  </div>

  <div class="card">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(255,92,138,.15)">🎨</div>
      <div class="card-meta"><h3>Ranglar (Colors)</h3><p>Bosing va eshiting</p></div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <div class="color-grid" id="colorGrid"></div>
    </div>
  </div>

  <div class="card">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(108,99,255,.15)">📅</div>
      <div class="card-meta"><h3>Hafta kunlari &amp; Oylar</h3><p>Days &amp; Months</p></div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <div class="section-label">Hafta kunlari</div>
      <table class="data-table">
        <tr><th>Inglizcha</th><th>Talaffuz</th><th>O'zbekcha</th></tr>
        <tr><td class="en-word">Monday <button class="speak-btn" onclick="sp('Monday')">🔊</button></td><td class="phon-word">[ˈmʌndeɪ]</td><td class="uz-word">Dushanba</td></tr>
        <tr><td class="en-word">Tuesday <button class="speak-btn" onclick="sp('Tuesday')">🔊</button></td><td class="phon-word">[ˈtjuːzdeɪ]</td><td class="uz-word">Seshanba</td></tr>
        <tr><td class="en-word">Wednesday <button class="speak-btn" onclick="sp('Wednesday')">🔊</button></td><td class="phon-word">[ˈwenzdeɪ]</td><td class="uz-word">Chorshanba</td></tr>
        <tr><td class="en-word">Thursday <button class="speak-btn" onclick="sp('Thursday')">🔊</button></td><td class="phon-word">[ˈθɜːrzdeɪ]</td><td class="uz-word">Payshanba</td></tr>
        <tr><td class="en-word">Friday <button class="speak-btn" onclick="sp('Friday')">🔊</button></td><td class="phon-word">[ˈfraɪdeɪ]</td><td class="uz-word">Juma</td></tr>
        <tr><td class="en-word">Saturday <button class="speak-btn" onclick="sp('Saturday')">🔊</button></td><td class="phon-word">[ˈsætərdeɪ]</td><td class="uz-word">Shanba</td></tr>
        <tr><td class="en-word">Sunday <button class="speak-btn" onclick="sp('Sunday')">🔊</button></td><td class="phon-word">[ˈsʌndeɪ]</td><td class="uz-word">Yakshanba</td></tr>
      </table>
      <div class="section-label mt-14">Oylar</div>
      <table class="data-table">
        <tr><th>Inglizcha</th><th>O'zbek</th><th>Inglizcha</th><th>O'zbek</th></tr>
        <tr><td class="en-word">January</td><td class="uz-word">Yanvar</td><td class="en-word">July</td><td class="uz-word">Iyul</td></tr>
        <tr><td class="en-word">February</td><td class="uz-word">Fevral</td><td class="en-word">August</td><td class="uz-word">Avgust</td></tr>
        <tr><td class="en-word">March</td><td class="uz-word">Mart</td><td class="en-word">September</td><td class="uz-word">Sentyabr</td></tr>
        <tr><td class="en-word">April</td><td class="uz-word">Aprel</td><td class="en-word">October</td><td class="uz-word">Oktyabr</td></tr>
        <tr><td class="en-word">May</td><td class="uz-word">May</td><td class="en-word">November</td><td class="uz-word">Noyabr</td></tr>
        <tr><td class="en-word">June</td><td class="uz-word">Iyun</td><td class="en-word">December</td><td class="uz-word">Dekabr</td></tr>
      </table>
    </div>
  </div>

  <div class="card">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(0,229,160,.15)">👔</div>
      <div class="card-meta"><h3>Kasblar (Jobs)</h3><p>Kasb-korlar inglizcha</p></div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <table class="data-table">
        <tr><th>Inglizcha</th><th>O'zbekcha</th><th>Inglizcha</th><th>O'zbekcha</th></tr>
        <tr><td class="en-word">Teacher</td><td class="uz-word">O'qituvchi</td><td class="en-word">Doctor</td><td class="uz-word">Shifokor</td></tr>
        <tr><td class="en-word">Engineer</td><td class="uz-word">Muhandis</td><td class="en-word">Driver</td><td class="uz-word">Haydovchi</td></tr>
        <tr><td class="en-word">Nurse</td><td class="uz-word">Hamshira</td><td class="en-word">Chef</td><td class="uz-word">Oshpaz</td></tr>
        <tr><td class="en-word">Lawyer</td><td class="uz-word">Advokat</td><td class="en-word">Programmer</td><td class="uz-word">Dasturchi</td></tr>
        <tr><td class="en-word">Farmer</td><td class="uz-word">Dehqon</td><td class="en-word">Artist</td><td class="uz-word">Rassom</td></tr>
        <tr><td class="en-word">Journalist</td><td class="uz-word">Jurnalist</td><td class="en-word">Manager</td><td class="uz-word">Menejer</td></tr>
      </table>
      <div class="quiz-wrap mt-14">
        <div class="quiz-label">SAVOL — KASBLAR</div>
        <div class="quiz-q" id="qJobQ"></div>
        <div class="quiz-opts" id="qJobO" style="grid-template-columns:1fr 1fr"></div>
        <button class="quiz-next" id="qJobNext" onclick="nextJobQ()">Keyingi →</button>
        <div class="quiz-score" id="qJobS"></div>
      </div>
    </div>
  </div>
</div><!-- /page-words -->

<!-- ═══ PAGE: GRAMMAR ═══ -->
<div class="page" id="page-grammar">

  <!-- Grammar Quest Hero -->
  <div class="gram-quest-hero" id="gramHero">
    <div class="gram-quest-inner">
      <div class="gq-top">
        <span class="gq-pill">🎮 GRAMMAR QUEST</span>
        <button class="gq-lb-btn" onclick="openLB()">🏆 Reyting</button>
      </div>
      <div class="gq-title">Grammatika <span>bosqichlari</span></div>
      <div class="gq-sub">Darsni o'rgan → test topshir → keyingi darajani oching (75+ ball kerak)</div>
      <div class="xp-wrap"><div class="xp-fill" id="gramXPBar" style="width:0%"></div></div>
      <div class="xp-lbl" id="gramXPLabel">XP: 0 / 700</div>
    </div>
  </div>

  <!-- Daily Challenge -->
  <div class="daily-banner" id="dailyChallenge" onclick="startDailyChallenge()">
    <div class="daily-icon">⚡</div>
    <div class="daily-body">
      <div class="daily-title">Kunlik vazifa</div>
      <div class="daily-sub" id="dailySub">Bugungi grammatika testini topshiring!</div>
    </div>
    <div class="daily-arrow" id="dailyArrow">→</div>
  </div>

  <!-- Lesson Road -->
  <div class="lesson-road" id="lessonRoad"></div>

  <!-- Lesson Panel -->
  <div id="lessonPanel" class="hidden">
    <div class="lesson-panel-header">
      <button class="lp-back-btn" onclick="closeLessonPanel()">← Orqaga</button>
      <div class="lp-info">
        <span class="lp-emoji" id="lpEmoji">📘</span>
        <div>
          <div class="lp-title" id="lpTitle">Dars</div>
          <div class="lp-sub" id="lpSub">Easy</div>
        </div>
      </div>
      <div class="lp-diff-chip" id="lpDiff">A1</div>
    </div>
    <div id="lpContent"></div>
    <div class="start-test-area">
      <div class="start-test-note" id="startTestNote"></div>
      <button class="start-test-btn" onclick="startTest()">✏️ Testni boshlash</button>
    </div>
  </div>

  <!-- Test Panel -->
  <div id="testPanel" class="hidden">
    <div class="lesson-panel-header">
      <button class="lp-back-btn" onclick="backToLesson()">← Darsga qaytish</button>
      <div class="lp-info">
        <span class="lp-emoji">✏️</span>
        <div>
          <div class="lp-title" id="tpTitle">Test</div>
          <div class="lp-sub" id="tpSub">Savollar</div>
        </div>
      </div>
      <div class="test-score-chip" id="tpChip">0/0</div>
    </div>
    <div class="test-progress-bar-outer"><div class="test-progress-bar-inner" id="tpBar" style="width:0%"></div></div>
    <div id="tpContent"></div>
  </div>

  <!-- Result Panel -->
  <div id="resultPanel" class="hidden">
    <div class="result-card">
      <div class="result-emoji" id="resultEmoji">🎉</div>
      <div class="result-score" id="resultScore">85/100</div>
      <div class="result-msg" id="resultMsg">Ajoyib!</div>
      <div class="result-detail" id="resultDetail"></div>
      <div id="unlockBanner" class="unlock-banner hidden">
        <div class="unlock-text">🔓 Yangi dars ochildi!</div>
      </div>
      <div class="result-btns">
        <button class="rbtn retry" onclick="retryTest()">🔁 Qayta</button>
        <button class="rbtn next-btn" id="nextLessonBtn" onclick="goNextLesson()" style="display:none">▶ Keyingi →</button>
        <button class="rbtn home-btn" onclick="closeLessonPanel()">🏠 Xarita</button>
      </div>
    </div>
  </div>

</div><!-- /page-grammar -->

<!-- ═══ PAGE: CONVERSATION ═══ -->
<div class="page" id="page-conversation">

  <div class="section-title mt-8">💬 Kundalik Suhbatlar</div>

  <div class="card open">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(255,179,71,.15)">🛍️</div>
      <div class="card-meta"><h3>Do'konda suhbat</h3><p>Shopping conversation</p></div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <div class="dialogue">
        <div class="bubble left"><div class="bubble-who">Sotuvchi</div><div class="bubble-en">Can I help you? <button class="speak-btn" onclick="sp('Can I help you?')">🔊</button></div><div class="bubble-uz">Sizga yordam bera olamanmi?</div></div>
        <div class="bubble right"><div class="bubble-who">Mijoz</div><div class="bubble-en">Yes, I'm looking for a jacket.</div><div class="bubble-uz">Ha, men kurtka qidirmoqdaman.</div></div>
        <div class="bubble left"><div class="bubble-who">Sotuvchi</div><div class="bubble-en">What size do you need?</div><div class="bubble-uz">Qanday o'lcham kerak?</div></div>
        <div class="bubble right"><div class="bubble-who">Mijoz</div><div class="bubble-en">Medium, please. How much is it?</div><div class="bubble-uz">O'rta. Narxi necha?</div></div>
        <div class="bubble left"><div class="bubble-who">Sotuvchi</div><div class="bubble-en">It's fifty dollars.</div><div class="bubble-uz">Ellik dollar.</div></div>
        <div class="bubble right"><div class="bubble-who">Mijoz</div><div class="bubble-en">I'll take it. Thank you!</div><div class="bubble-uz">Olaman. Rahmat!</div></div>
      </div>
      <div class="section-label mt-14">Foydali so'zlar</div>
      <table class="data-table">
        <tr><th>Inglizcha</th><th>O'zbekcha</th></tr>
        <tr><td class="en-word">How much is this? <button class="speak-btn" onclick="sp('How much is this?')">🔊</button></td><td class="uz-word">Bu qancha turadi?</td></tr>
        <tr><td class="en-word">That's too expensive.</td><td class="uz-word">Bu juda qimmat.</td></tr>
        <tr><td class="en-word">Do you have a discount?</td><td class="uz-word">Chegirma bormi?</td></tr>
        <tr><td class="en-word">I'll pay by card.</td><td class="uz-word">Karta bilan to'layman.</td></tr>
        <tr><td class="en-word">Can I try this on?</td><td class="uz-word">Kiyib ko'rsam bo'ladimi?</td></tr>
      </table>
    </div>
  </div>

  <div class="card">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(255,92,138,.15)">🍽️</div>
      <div class="card-meta"><h3>Restoranda suhbat</h3><p>At a restaurant</p></div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <div class="dialogue">
        <div class="bubble left"><div class="bubble-who">Ofitsiant</div><div class="bubble-en">Good evening! Do you have a reservation?</div><div class="bubble-uz">Xayrli kech! Buyurtmangiz bormi?</div></div>
        <div class="bubble right"><div class="bubble-who">Mehmon</div><div class="bubble-en">No, but we'd like a table for two.</div><div class="bubble-uz">Yo'q, lekin ikki kishilik stol kerak.</div></div>
        <div class="bubble left"><div class="bubble-who">Ofitsiant</div><div class="bubble-en">Of course! Here is the menu.</div><div class="bubble-uz">Albatta! Mana menyu.</div></div>
        <div class="bubble right"><div class="bubble-who">Mehmon</div><div class="bubble-en">I'd like chicken soup and rice, please.</div><div class="bubble-uz">Menga tovuq sho'rva va guruch bering.</div></div>
        <div class="bubble left"><div class="bubble-who">Ofitsiant</div><div class="bubble-en">And to drink?</div><div class="bubble-uz">Ichimlik-chi?</div></div>
        <div class="bubble right"><div class="bubble-who">Mehmon</div><div class="bubble-en">Water, please. And the bill at the end.</div><div class="bubble-uz">Suv iltimos. Va oxirida hisob-kitob.</div></div>
      </div>
    </div>
  </div>

  <div class="card">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(0,229,160,.15)">🗺️</div>
      <div class="card-meta"><h3>Yo'l so'rash</h3><p>Asking for directions</p></div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <table class="data-table">
        <tr><th>Inglizcha</th><th>O'zbekcha</th></tr>
        <tr><td class="en-word">Excuse me, where is the hospital? <button class="speak-btn" onclick="sp('Excuse me, where is the hospital?')">🔊</button></td><td class="uz-word">Kechirasiz, kasalxona qayerda?</td></tr>
        <tr><td class="en-word">Go straight. <button class="speak-btn" onclick="sp('Go straight.')">🔊</button></td><td class="uz-word">To'g'ri boring.</td></tr>
        <tr><td class="en-word">Turn left. <button class="speak-btn" onclick="sp('Turn left.')">🔊</button></td><td class="uz-word">Chapga buriling.</td></tr>
        <tr><td class="en-word">Turn right. <button class="speak-btn" onclick="sp('Turn right.')">🔊</button></td><td class="uz-word">O'ngga buriling.</td></tr>
        <tr><td class="en-word">It's near / far.</td><td class="uz-word">U yaqin / uzoq.</td></tr>
        <tr><td class="en-word">About 5 minutes on foot.</td><td class="uz-word">Piyoda taxminan 5 daqiqa.</td></tr>
      </table>
    </div>
  </div>

  <div class="card">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(108,99,255,.15)">📞</div>
      <div class="card-meta"><h3>Telefon suhbatlari</h3><p>Phone conversations</p></div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <table class="data-table">
        <tr><th>Inglizcha</th><th>O'zbekcha</th></tr>
        <tr><td class="en-word">Hello, this is Ali speaking. <button class="speak-btn" onclick="sp('Hello, this is Ali speaking.')">🔊</button></td><td class="uz-word">Allo, bu Ali gapiryapti.</td></tr>
        <tr><td class="en-word">Can I speak to Sara, please?</td><td class="uz-word">Sara bilan gaplashsam bo'ladimi?</td></tr>
        <tr><td class="en-word">Hold on, please.</td><td class="uz-word">Bir daqiqa kuting.</td></tr>
        <tr><td class="en-word">I'll call back later.</td><td class="uz-word">Keyinroq qayta qo'ng'iroq qilaman.</td></tr>
        <tr><td class="en-word">Wrong number, sorry!</td><td class="uz-word">Noto'g'ri raqam, kechirasiz!</td></tr>
      </table>
    </div>
  </div>

  <div class="card">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(255,92,138,.15)">❓</div>
      <div class="card-meta"><h3>Savol so'zlari</h3><p>What, Where, When, Why, How...</p></div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <table class="data-table">
        <tr><th>So'z</th><th>Tarjima</th><th>Misol</th></tr>
        <tr><td class="en-word">What?</td><td class="uz-word">Nima?</td><td class="en-word">What is your job?</td></tr>
        <tr><td class="en-word">Where?</td><td class="uz-word">Qayerda?</td><td class="en-word">Where do you live?</td></tr>
        <tr><td class="en-word">When?</td><td class="uz-word">Qachon?</td><td class="en-word">When is your birthday?</td></tr>
        <tr><td class="en-word">Why?</td><td class="uz-word">Nima uchun?</td><td class="en-word">Why are you sad?</td></tr>
        <tr><td class="en-word">Who?</td><td class="uz-word">Kim?</td><td class="en-word">Who is that man?</td></tr>
        <tr><td class="en-word">How?</td><td class="uz-word">Qanday?</td><td class="en-word">How do you feel?</td></tr>
        <tr><td class="en-word">How much?</td><td class="uz-word">Qancha?</td><td class="en-word">How much does it cost?</td></tr>
        <tr><td class="en-word">How many?</td><td class="uz-word">Nechta?</td><td class="en-word">How many students?</td></tr>
      </table>
    </div>
  </div>

</div><!-- /page-conversation -->

<!-- ═══ PAGE: ADVANCED ═══ -->
<div class="page" id="page-advanced">

  <div class="section-title mt-8">🚀 Keyingi Level — B1</div>

  <div class="card open">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(108,99,255,.15)">⏮️</div>
      <div class="card-meta"><h3>Past Simple — O'tgan zamon</h3><p>Tugagan harakatlar</p></div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <div class="gram-box"><strong>Tuzilishi:</strong> Subject + fe'l<strong>-ed</strong> yoki irregular 2-shakl</div>
      <table class="data-table">
        <tr><th>Shakl</th><th>Misol</th><th>Tarjima</th></tr>
        <tr><td><span class="tag g">✅</span></td><td class="en-word">I worked yesterday.</td><td class="uz-word">Men kecha ishladim.</td></tr>
        <tr><td><span class="tag r">❌</span></td><td class="en-word">I didn't work yesterday.</td><td class="uz-word">Men kecha ishlamadim.</td></tr>
        <tr><td><span class="tag">❓</span></td><td class="en-word">Did you work yesterday?</td><td class="uz-word">Kecha ishladingizmi?</td></tr>
      </table>
      <div class="section-label mt-14">Notartibli fe'llar (Irregular verbs)</div>
      <table class="data-table">
        <tr><th>Hozirgi</th><th>O'tgani</th><th>Tarjima</th></tr>
        <tr><td class="en-word">go</td><td class="en-word">went</td><td class="uz-word">bormoq</td></tr>
        <tr><td class="en-word">come</td><td class="en-word">came</td><td class="uz-word">kelmoq</td></tr>
        <tr><td class="en-word">see</td><td class="en-word">saw</td><td class="uz-word">ko'rmoq</td></tr>
        <tr><td class="en-word">eat</td><td class="en-word">ate</td><td class="uz-word">yemoq</td></tr>
        <tr><td class="en-word">drink</td><td class="en-word">drank</td><td class="uz-word">ichmoq</td></tr>
        <tr><td class="en-word">buy</td><td class="en-word">bought</td><td class="uz-word">sotib olmoq</td></tr>
        <tr><td class="en-word">say</td><td class="en-word">said</td><td class="uz-word">demoq</td></tr>
        <tr><td class="en-word">make</td><td class="en-word">made</td><td class="uz-word">yasamoq</td></tr>
        <tr><td class="en-word">take</td><td class="en-word">took</td><td class="uz-word">olmoq</td></tr>
        <tr><td class="en-word">get</td><td class="en-word">got</td><td class="uz-word">olmoq / bo'lmoq</td></tr>
      </table>
    </div>
  </div>

  <div class="card">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(0,229,160,.15)">⏭️</div>
      <div class="card-meta"><h3>Future Simple — Kelasi zamon</h3><p>will bilan kelajak</p></div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <div class="gram-box green"><strong>Tuzilishi:</strong> Subject + <strong>will</strong> + fe'l — Barcha shaxslar uchun bir xil!</div>
      <table class="data-table">
        <tr><th>Shakl</th><th>Misol</th><th>Tarjima</th></tr>
        <tr><td><span class="tag g">✅</span></td><td class="en-word">I will call you tomorrow.</td><td class="uz-word">Ertaga qo'ng'iroq qilaman.</td></tr>
        <tr><td><span class="tag r">❌</span></td><td class="en-word">She won't come today.</td><td class="uz-word">U bugun kelmaydi.</td></tr>
        <tr><td><span class="tag">❓</span></td><td class="en-word">Will you help me?</td><td class="uz-word">Menga yordam berasizmi?</td></tr>
      </table>
      <div class="gram-box orange mt-8"><strong>will not = won't</strong> &nbsp;|&nbsp; I will = I'll &nbsp;|&nbsp; She will = She'll</div>
    </div>
  </div>

  <div class="card">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(255,92,138,.15)">🎯</div>
      <div class="card-meta"><h3>Modal Verbs</h3><p>can · should · must</p></div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <table class="data-table">
        <tr><th>Modal</th><th>Ma'no</th><th>Misol</th><th>Tarjima</th></tr>
        <tr><td class="en-word">can</td><td class="uz-word">imkoniyat</td><td class="en-word">I can swim.</td><td class="uz-word">Men suza olaman.</td></tr>
        <tr><td class="en-word">can't</td><td class="uz-word">imkonsizlik</td><td class="en-word">He can't drive.</td><td class="uz-word">U hayday olmaydi.</td></tr>
        <tr><td class="en-word">should</td><td class="uz-word">maslahat</td><td class="en-word">You should sleep early.</td><td class="uz-word">Erta uxlashingiz kerak.</td></tr>
        <tr><td class="en-word">shouldn't</td><td class="uz-word">kerak emas</td><td class="en-word">You shouldn't smoke.</td><td class="uz-word">Chekmasligingiz kerak.</td></tr>
        <tr><td class="en-word">must</td><td class="uz-word">majburiyat</td><td class="en-word">You must wear a seatbelt.</td><td class="uz-word">Kamar taqish shart.</td></tr>
        <tr><td class="en-word">mustn't</td><td class="uz-word">man etilgan</td><td class="en-word">You mustn't smoke here.</td><td class="uz-word">Bu yerda chekish mumkin emas.</td></tr>
      </table>
    </div>
  </div>

  <div class="card">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-icon" style="background:rgba(255,179,71,.15)">📊</div>
      <div class="card-meta"><h3>Comparison — Taqqoslash</h3><p>big → bigger → biggest</p></div>
      <span class="card-chevron">⌄</span>
    </div>
    <div class="card-body">
      <table class="data-table">
        <tr><th>Asl</th><th>Qiyosiy</th><th>Orttirma</th><th>Tarjima</th></tr>
        <tr><td class="en-word">big</td><td class="en-word">bigger</td><td class="en-word">the biggest</td><td class="uz-word">katta / kattaroq / eng katta</td></tr>
        <tr><td class="en-word">small</td><td class="en-word">smaller</td><td class="en-word">the smallest</td><td class="uz-word">kichik / kichikroq / eng kichik</td></tr>
        <tr><td class="en-word">fast</td><td class="en-word">faster</td><td class="en-word">the fastest</td><td class="uz-word">tez / tezroq / eng tez</td></tr>
        <tr><td class="en-word">good</td><td class="en-word">better</td><td class="en-word">the best</td><td class="uz-word">yaxshi / yaxshiroq / eng yaxshi</td></tr>
        <tr><td class="en-word">bad</td><td class="en-word">worse</td><td class="en-word">the worst</td><td class="uz-word">yomon / yomonroq / eng yomon</td></tr>
        <tr><td class="en-word">beautiful</td><td class="en-word">more beautiful</td><td class="en-word">the most beautiful</td><td class="uz-word">chiroyli / chiroliroq / eng chiroyli</td></tr>
        <tr><td class="en-word">expensive</td><td class="en-word">more expensive</td><td class="en-word">the most expensive</td><td class="uz-word">qimmat / qimmatroq / eng qimmat</td></tr>
      </table>
      <div class="gram-box mt-8">📏 <strong>Qisqa (1 bo'g'in):</strong> + er/est → big<strong>ger</strong>, bigg<strong>est</strong></div>
      <div class="gram-box green">📐 <strong>Uzun (2+ bo'g'in):</strong> more/most + sifat → <strong>more</strong> beautiful</div>
      <div class="example-box mt-8"><div class="example-en">My car is <strong>faster than</strong> your car.</div><div class="example-uz">Mening mashinam siznikidan tezroq.</div></div>
      <div class="example-box"><div class="example-en">This is <strong>the best</strong> restaurant in the city.</div><div class="example-uz">Bu shahardagi eng yaxshi restoran.</div></div>
    </div>
  </div>

</div><!-- /page-advanced -->

<!-- ═══ PAGE: GAME ═══ -->
<div class="page" id="page-game">

  <div class="section-title mt-8">🎯 Vocabulary Game</div>

  <div class="game-banner">
    <div class="game-score-row">
      <div class="game-score-chip">✅ <span id="gameScore">0</span> ball</div>
      <div class="game-lives" id="gameLives">❤️❤️❤️</div>
      <div class="game-score-chip">🔥 <span id="gameStreak">0</span> seriya</div>
    </div>
    <div class="game-word" id="gameWord">---</div>
    <div class="game-hint" id="gameHint">Tarjimasini tanlang</div>
    <div class="game-opts" id="gameOpts"></div>
  </div>

  <div class="text-center mt-14" id="gameEndArea" style="display:none">
    <div style="font-size:48px;margin-bottom:12px" id="gameEndEmoji">🎉</div>
    <div style="font-family:'Unbounded',sans-serif;font-size:28px;font-weight:900;margin-bottom:8px;color:var(--brand)" id="gameEndScore"></div>
    <div style="color:var(--text-2);font-size:14px;margin-bottom:24px">Ajoyib natija!</div>
    <button class="btn-primary" onclick="restartGame()">🎮 Qayta o'ynash</button>
  </div>

</div><!-- /page-game -->

<!-- ═══ PAGE: ACHIEVEMENTS ═══ -->
<div class="page" id="page-achievements">

  <div class="section-title mt-8">🏆 Yutuqlar va Muvaffaqiyatlar</div>

  <div class="streak-card">
    <div class="streak-fire">🔥</div>
    <div class="streak-info">
      <div class="streak-num" id="achStreak">0</div>
      <div class="streak-lbl">Kun seriyasi · Har kun o'rgan!</div>
    </div>
  </div>

  <div class="section-title">🎖️ Yutuqlar</div>
  <div class="ach-grid" id="achGrid"></div>

  <div class="section-title mt-20">📈 Batafsil statistika</div>
  <div class="dashboard-grid">
    <div class="dash-card"><div class="dash-card-num" style="color:var(--brand)" id="ds1">0</div><div class="dash-card-lbl">Jami XP</div></div>
    <div class="dash-card"><div class="dash-card-num" style="color:var(--brand-3)" id="ds2">0</div><div class="dash-card-lbl">Darslar</div></div>
    <div class="dash-card"><div class="dash-card-num" style="color:var(--brand-4)" id="ds3">0</div><div class="dash-card-lbl">Test o'tilgan</div></div>
    <div class="dash-card"><div class="dash-card-num" style="color:var(--brand-2)" id="ds4">0</div><div class="dash-card-lbl">Yutuqlar</div></div>
    <div class="dash-card"><div class="dash-card-num" style="color:#b0a8ff" id="ds5">0</div><div class="dash-card-lbl">O'yin ballari</div></div>
    <div class="dash-card"><div class="dash-card-num" style="color:var(--brand-3)" id="ds6">0</div><div class="dash-card-lbl">Eng yaxshi ball</div></div>
  </div>

</div><!-- /page-achievements -->

</div><!-- /main -->

<!-- ═══════════ MOBILE BOTTOM NAV ═══════════ -->
<nav class="bottom-nav">
  <div class="bottom-nav-inner">
    <button class="bnav-btn active" onclick="goPage('home')" data-bpage="home">
      <div class="bnav-icon">🏠</div>
      <div class="bnav-lbl">Bosh</div>
    </button>
    <button class="bnav-btn" onclick="goPage('alphabet')" data-bpage="alphabet">
      <div class="bnav-icon">🔤</div>
      <div class="bnav-lbl">Alifbo</div>
    </button>
    <button class="bnav-btn" onclick="goPage('grammar')" data-bpage="grammar">
      <div class="bnav-icon">🎮</div>
      <div class="bnav-lbl">Grammatika</div>
    </button>
    <button class="bnav-btn" onclick="goPage('game')" data-bpage="game">
      <div class="bnav-icon">🎯</div>
      <div class="bnav-lbl">O'yin</div>
    </button>
    <button class="bnav-btn" onclick="goPage('achievements')" data-bpage="achievements">
      <div class="bnav-icon">🏆</div>
      <div class="bnav-lbl">Yutuqlar</div>
    </button>
  </div>
</nav>

<!-- ═══════════ LETTER MODAL ═══════════ -->
<div class="modal-overlay" id="letterModal" onclick="if(event.target===this)closeLetterModal()">
  <div class="modal-box text-center">
    <div class="canvas-wrap">
      <canvas id="letterCanvas" width="480" height="480"></canvas>
    </div>
    <div class="progress-bar-outer"><div class="progress-bar-inner" id="animPB"></div></div>
    <div class="ctrl-row">
      <button class="ctrl-btn" id="playPauseBtn" onclick="toggleAnim()">▶ Ijro</button>
      <button class="ctrl-btn" onclick="replayAnim()">↺ Qayta</button>
    </div>
    <div class="modal-letter" id="modalLetter">A a</div>
    <div class="modal-phon" id="modalPhon">[eɪ]</div>
    <div class="modal-ex" id="modalEx">Apple, Ant, Air</div>
    <div class="word-pills" id="wordPills"></div>
    <button class="speak-big-btn" onclick="spkLetter()">🔊 Ovozini eshitish</button>
    <button class="modal-close-btn" onclick="closeLetterModal()">✕ Yopish</button>
  </div>
</div>

<!-- ═══════════ LEADERBOARD MODAL ═══════════ -->
<div class="modal-overlay" id="lbModal" onclick="if(event.target===this)closeLB()">
  <div class="modal-box modal-wide" style="max-height:90vh;overflow-y:auto">
    <div class="lb-header">
      <div class="lb-title">🏆 Global Reyting</div>
      <button class="lb-close-btn" onclick="closeLB()">✕ Yopish</button>
    </div>
    <div style="font-size:12px;color:var(--text-2);margin-bottom:12px">Ismingizni kiriting va natijangizni global reytingga saqlang!</div>
    <div class="lb-input-row">
      <input class="lb-input" id="lbNameInput" placeholder="Ismingizni kiriting..." maxlength="20">
      <button class="lb-save-btn" onclick="saveLBEntry()">Saqlash</button>
    </div>
    <div id="lbList"></div>
  </div>
</div>

<!-- ═══════════ TOAST ═══════════ -->
<div class="toast" id="toast"></div>

<script>
/* ══════════════════════════════════════════════
   ALPHABET DATA
══════════════════════════════════════════════ */
const AD=[
  {l:'A',p:'[eɪ]',ex:'Apple, Ant, Air',w:['Apple','Ant','Air'],c:'#ff6b8a'},
  {l:'B',p:'[biː]',ex:'Ball, Book, Bird',w:['Ball','Book','Bird'],c:'#ff9f40'},
  {l:'C',p:'[siː]',ex:'Cat, Car, Cup',w:['Cat','Car','Cup'],c:'#ffcd56'},
  {l:'D',p:'[diː]',ex:'Dog, Door, Day',w:['Dog','Door','Day'],c:'#4bc0c0'},
  {l:'E',p:'[iː]',ex:'Egg, Eye, Ear',w:['Egg','Eye','Ear'],c:'#36a2eb'},
  {l:'F',p:'[ef]',ex:'Fish, Fire, Face',w:['Fish','Fire','Face'],c:'#9966ff'},
  {l:'G',p:'[dʒiː]',ex:'Girl, Game, Gold',w:['Girl','Game','Gold'],c:'#ff6b8a'},
  {l:'H',p:'[eɪtʃ]',ex:'Hat, Hand, Home',w:['Hat','Hand','Home'],c:'#3ee8a0'},
  {l:'I',p:'[aɪ]',ex:'Ice, Ink, Iron',w:['Ice','Ink','Iron'],c:'#7c6fff'},
  {l:'J',p:'[dʒeɪ]',ex:'Juice, Jam, Jump',w:['Juice','Jam','Jump'],c:'#ff9f40'},
  {l:'K',p:'[keɪ]',ex:'Key, King, Kite',w:['Key','King','Kite'],c:'#ffcd56'},
  {l:'L',p:'[el]',ex:'Lion, Love, Lake',w:['Lion','Love','Lake'],c:'#4bc0c0'},
  {l:'M',p:'[em]',ex:'Man, Moon, Milk',w:['Man','Moon','Milk'],c:'#36a2eb'},
  {l:'N',p:'[en]',ex:'Night, Nose, Nut',w:['Night','Nose','Nut'],c:'#9966ff'},
  {l:'O',p:'[oʊ]',ex:'Open, Old, Orange',w:['Open','Old','Orange'],c:'#ff6b8a'},
  {l:'P',p:'[piː]',ex:'Park, Pink, Pen',w:['Park','Pink','Pen'],c:'#3ee8a0'},
  {l:'Q',p:'[kjuː]',ex:'Queen, Quiz, Quick',w:['Queen','Quiz','Quick'],c:'#7c6fff'},
  {l:'R',p:'[ɑːr]',ex:'Rain, Red, Ring',w:['Rain','Red','Ring'],c:'#ff9f40'},
  {l:'S',p:'[es]',ex:'Sun, Star, Snow',w:['Sun','Star','Snow'],c:'#ffcd56'},
  {l:'T',p:'[tiː]',ex:'Tree, Time, Talk',w:['Tree','Time','Talk'],c:'#4bc0c0'},
  {l:'U',p:'[juː]',ex:'Umbrella, Up, Use',w:['Umbrella','Up','Use'],c:'#36a2eb'},
  {l:'V',p:'[viː]',ex:'Van, Voice, Vase',w:['Van','Voice','Vase'],c:'#9966ff'},
  {l:'W',p:'[ˈdʌbljuː]',ex:'Water, Wind, Walk',w:['Water','Wind','Walk'],c:'#ff6b8a'},
  {l:'X',p:'[eks]',ex:'X-ray, Box, Fox',w:['X-ray','Box','Fox'],c:'#3ee8a0'},
  {l:'Y',p:'[waɪ]',ex:'Year, Yellow, Yes',w:['Year','Yellow','Yes'],c:'#7c6fff'},
  {l:'Z',p:'[ziː]',ex:'Zoo, Zero, Zone',w:['Zoo','Zero','Zone'],c:'#ff9f40'}
];

/* ══════════════════════════════════════════════
   GLOBAL STATE
══════════════════════════════════════════════ */
let APP = {
  xp: 0,
  streak: 0,
  lastLogin: null,
  gameBestScore: 0,
  testsCompleted: 0,
  theme: 'dark',
  gramState: {
    unlocked: [true,false,false,false,false,false,false],
    scores:   [null,null,null,null,null,null,null],
    xp: 0
  }
};

const STORE_KEY = 'linguauz_v2';
const LB_KEY   = 'linguauz_lb2';

function loadApp(){
  try {
    const d = localStorage.getItem(STORE_KEY);
    if(d){ const p=JSON.parse(d); Object.assign(APP,p); }
  } catch(e){}
}
function saveApp(){
  try { localStorage.setItem(STORE_KEY, JSON.stringify(APP)); } catch(e){}
}

/* ══════════════════════════════════════════════
   STREAK SYSTEM
══════════════════════════════════════════════ */
function updateStreak(){
  const today = new Date().toDateString();
  const yesterday = new Date(Date.now()-86400000).toDateString();
  if(APP.lastLogin === today){
    /* same day, no change */
  } else if(APP.lastLogin === yesterday){
    APP.streak++;
    showToast('🔥 '+APP.streak+' kun seriyasi!', 'xp');
  } else if(APP.lastLogin !== today){
    if(APP.lastLogin && APP.lastLogin !== yesterday) APP.streak = 1;
    else if(!APP.lastLogin) APP.streak = 1;
  }
  APP.lastLogin = today;
  saveApp();
  refreshUI();
}

/* ══════════════════════════════════════════════
   XP SYSTEM
══════════════════════════════════════════════ */
function addXP(amount, label){
  APP.xp += amount;
  APP.gramState.xp += amount;
  saveApp();
  showToast('⚡ +' + amount + ' XP' + (label ? ' — ' + label : ''), 'xp');
  refreshUI();
  checkAchievements();
}

/* ══════════════════════════════════════════════
   ACHIEVEMENTS
══════════════════════════════════════════════ */
const ACHIEVEMENTS = [
  {id:'first_lesson', icon:'🌱', name:'Birinchi qadam', desc:'Birinchi darsni tugatdingiz', cond: s => s.testsCompleted >= 1},
  {id:'three_lessons', icon:'📚', name:'O\'quvchi', desc:'3 ta darsni tugatdingiz', cond: s => s.testsCompleted >= 3},
  {id:'all_lessons', icon:'🎓', name:'Grammatika ustasi', desc:'Barcha darslarni tugatdingiz', cond: s => s.gramState.scores.filter(x=>x!==null&&x>=75).length >= 7},
  {id:'xp_100', icon:'⚡', name:'XP 100', desc:'100 XP yig\'dingiz', cond: s => s.xp >= 100},
  {id:'xp_500', icon:'🌟', name:'XP 500', desc:'500 XP yig\'dingiz', cond: s => s.xp >= 500},
  {id:'xp_1000', icon:'👑', name:'XP 1000', desc:'1000 XP yig\'dingiz', cond: s => s.xp >= 1000},
  {id:'streak_3', icon:'🔥', name:'3 kun seriya', desc:'3 kun ketma-ket o\'rgandingiz', cond: s => s.streak >= 3},
  {id:'streak_7', icon:'🌈', name:'Haftalik seriya', desc:'7 kun ketma-ket o\'rgandingiz', cond: s => s.streak >= 7},
  {id:'perfect_score', icon:'💯', name:'Mukammal!', desc:'Bir testda 100/100 oldingiz', cond: s => (s.gramState.scores||[]).some(x=>x===100)},
  {id:'game_master', icon:'🎯', name:'O\'yin ustasi', desc:'O\'yinda 10+ ball', cond: s => s.gameBestScore >= 10},
];

function getEarnedAchs(){
  return ACHIEVEMENTS.filter(a => a.cond(APP));
}

function checkAchievements(){
  const earned = getEarnedAchs();
  const prev = JSON.parse(localStorage.getItem('linguauz_achs') || '[]');
  earned.forEach(a => {
    if(!prev.includes(a.id)){
      showToast('🏆 Yutuq: ' + a.name + '!', 'xp');
      prev.push(a.id);
    }
  });
  try { localStorage.setItem('linguauz_achs', JSON.stringify(prev)); } catch(e){}
}

function renderAchievements(){
  const grid = document.getElementById('achGrid');
  if(!grid) return;
  const earned = getEarnedAchs().map(a=>a.id);
  grid.innerHTML = ACHIEVEMENTS.map(a => `
    <div class="ach-card ${earned.includes(a.id) ? 'earned' : 'locked'}">
      ${earned.includes(a.id) ? '<div class="ach-earned-badge">EARNED</div>' : ''}
      <div class="ach-emoji">${a.icon}</div>
      <div class="ach-name">${a.name}</div>
      <div class="ach-desc">${a.desc}</div>
    </div>
  `).join('');
}

/* ══════════════════════════════════════════════
   UI REFRESH
══════════════════════════════════════════════ */
function refreshUI(){
  const earned = getEarnedAchs().length;

  // Nav XP
  const navXPEl = document.getElementById('navXP');
  if(navXPEl) navXPEl.textContent = APP.xp + ' XP';

  // Nav streak
  const sc = document.getElementById('streakCount');
  if(sc) sc.textContent = APP.streak;

  // Home stats
  const completed = (APP.gramState.scores || []).filter(x=>x!==null&&x>=75).length;
  const ids = {statLessons:completed, statXP:APP.xp, statStreak:APP.streak, statBadges:earned};
  Object.entries(ids).forEach(([id,v])=>{ const el=document.getElementById(id); if(el) el.textContent=v; });

  // Dashboard
  const dashIds = {dashXP:APP.xp, dashLessons:completed, dashStreak:APP.streak, dashBadges:earned};
  Object.entries(dashIds).forEach(([id,v])=>{ const el=document.getElementById(id); if(el) el.textContent=v; });

  // Achievements page stats
  const dsIds = {ds1:APP.xp, ds2:completed, ds3:APP.testsCompleted||0, ds4:earned, ds5:APP.gameBestScore||0, ds6:Math.max(...(APP.gramState.scores||[]).filter(x=>x!==null),0)||0};
  Object.entries(dsIds).forEach(([id,v])=>{ const el=document.getElementById(id); if(el) el.textContent=v; });

  // Achievements streak
  const as = document.getElementById('achStreak');
  if(as) as.textContent = APP.streak;

  // Grammar XP bar
  const total = 7 * 100;
  const pct = Math.min((APP.gramState.xp / total)*100, 100);
  const xpBar = document.getElementById('gramXPBar');
  if(xpBar) xpBar.style.width = pct + '%';
  const xpLbl = document.getElementById('gramXPLabel');
  if(xpLbl) xpLbl.textContent = 'XP: ' + APP.gramState.xp + ' / ' + total;

  // Course progress bars
  const gramDone = completed;
  const gramPct = Math.round((gramDone / 7)*100);
  const p2 = document.getElementById('prog-2');
  if(p2) p2.style.width = gramPct + '%';
  const pl2 = document.getElementById('prog-lbl-2');
  if(pl2) pl2.textContent = gramDone + '/7 dars';

  // Render achievements grid if on that page
  renderAchievements();
}

/* ══════════════════════════════════════════════
   NAVIGATION
══════════════════════════════════════════════ */
function goPage(name){
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.nav-tab').forEach(b => {
    b.classList.toggle('active', b.dataset.page === name);
  });
  document.querySelectorAll('.bnav-btn').forEach(b => {
    b.classList.toggle('active', b.dataset.bpage === name);
  });
  const page = document.getElementById('page-'+name);
  if(page) page.classList.add('active');
  window.scrollTo({top:0, behavior:'smooth'});
  refreshUI();
  if(name === 'grammar') renderLessonRoad();
  if(name === 'game')    startGame();
  if(name === 'achievements') { renderAchievements(); }
}

function toggleCard(header){
  header.closest('.card').classList.toggle('open');
}

/* ══════════════════════════════════════════════
   THEME
══════════════════════════════════════════════ */
function toggleTheme(){
  const isDark = document.documentElement.dataset.theme === 'dark';
  const next = isDark ? 'light' : 'dark';
  document.documentElement.dataset.theme = next;
  APP.theme = next;
  document.getElementById('themeBtn').textContent = isDark ? '☀️' : '🌙';
  saveApp();
}

/* ══════════════════════════════════════════════
   TOAST
══════════════════════════════════════════════ */
let toastTimer;
function showToast(msg, type=''){
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.className = 'toast ' + type + ' show';
  clearTimeout(toastTimer);
  toastTimer = setTimeout(() => t.classList.remove('show'), 2400);
}

/* ══════════════════════════════════════════════
   SPEECH SYNTHESIS
══════════════════════════════════════════════ */
const synth = window.speechSynthesis;
let voices = [];
function loadVoices(){ voices = synth ? synth.getVoices() : []; }
if(synth){ loadVoices(); synth.onvoiceschanged = loadVoices; setTimeout(loadVoices,800); }

function sp(text){
  if(!synth) return;
  synth.cancel();
  const u = new SpeechSynthesisUtterance(text);
  u.lang = 'en-US'; u.rate = 0.82; u.pitch = 1.05; u.volume = 1.0;
  const v = voices.find(v=>v.lang==='en-US'&&v.localService) || voices.find(v=>v.lang.startsWith('en'));
  if(v) u.voice = v;
  synth.speak(u);
}
function spkLetter(){ if(curLetterData) sp(curLetterData.l); }

/* ══════════════════════════════════════════════
   CANVAS ANIMATION
══════════════════════════════════════════════ */
const cvs = document.getElementById('letterCanvas');
const cx  = cvs.getContext('2d');
const CW=480, CH=480;
let animT=0, animDur=150, animRaf=null, animOn=false, curLetterData=null;

function drawLetterFrame(t, d){
  cx.clearRect(0,0,CW,CH);
  const isDark = document.documentElement.dataset.theme === 'dark';
  cx.fillStyle = isDark ? '#13132a' : '#eeeeff';
  cx.fillRect(0,0,CW,CH);
  for(let i=0;i<4;i++){
    const ph=((t/animDur)+i*0.25)%1;
    const r=60+ph*200, al=(1-ph)*0.3;
    cx.beginPath(); cx.arc(CW/2,CH/2,r,0,Math.PI*2);
    const hexA=Math.floor(al*255).toString(16).padStart(2,'0');
    cx.strokeStyle=d.c+hexA; cx.lineWidth=2; cx.stroke();
  }
  for(let j=0;j<8;j++){
    const ang=(j/8)*Math.PI*2+t*0.05;
    const or=160+Math.sin(t*0.07+j)*15;
    const px=CW/2+Math.cos(ang)*or, py=CH/2+Math.sin(ang)*or;
    cx.beginPath(); cx.arc(px,py,3+Math.sin(t*0.1+j)*1.5,0,Math.PI*2);
    cx.fillStyle=d.c; cx.globalAlpha=0.65; cx.fill(); cx.globalAlpha=1;
  }
  const g=cx.createRadialGradient(CW/2,CH/2,0,CW/2,CH/2,140);
  g.addColorStop(0,d.c+'44'); g.addColorStop(1,'transparent');
  cx.fillStyle=g; cx.fillRect(0,0,CW,CH);
  const prog=Math.min(t/20,1), ease=1-Math.pow(1-prog,3);
  const sc=(0.2+ease*0.8)*(1+Math.sin(t*0.07)*0.025);
  cx.save(); cx.translate(CW/2,CH/2+10); cx.scale(sc,sc);
  cx.shadowColor=d.c; cx.shadowBlur=25+Math.sin(t*0.05)*8;
  const lg=cx.createLinearGradient(-80,-100,80,100);
  lg.addColorStop(0,'#ffffff'); lg.addColorStop(0.5,d.c); lg.addColorStop(1,'#ffffffaa');
  cx.font='900 190px Unbounded,sans-serif'; cx.textAlign='center'; cx.textBaseline='middle';
  cx.fillStyle=lg; cx.fillText(d.l,0,0); cx.shadowBlur=0; cx.restore();
  const sp2=Math.min(Math.max(t-10,0)/18,1);
  cx.globalAlpha=sp2; cx.font='500 46px Unbounded,sans-serif'; cx.textAlign='center';
  cx.fillStyle='#ffffff55'; cx.fillText(d.l.toLowerCase(),CW/2,CH/2+118); cx.globalAlpha=1;
  if(t<25){
    for(let k=0;k<8;k++){
      const sa=(k/8)*Math.PI*2, sr=t*6;
      cx.beginPath(); cx.arc(CW/2+Math.cos(sa)*sr,CH/2+Math.sin(sa)*sr,3,0,Math.PI*2);
      cx.fillStyle=d.c; cx.globalAlpha=(1-t/25)*0.9; cx.fill(); cx.globalAlpha=1;
    }
  }
  const pb=document.getElementById('animPB');
  if(pb) pb.style.width=Math.min((t/animDur)*100,100)+'%';
}

function animLoop(){
  if(!animOn) return;
  animT++;
  drawLetterFrame(animT, curLetterData);
  if(animT < animDur){ animRaf = requestAnimationFrame(animLoop); }
  else { animOn=false; updatePlayBtn(); }
}

function startAnim(){
  if(animRaf) cancelAnimationFrame(animRaf);
  animT=0; animOn=true; updatePlayBtn();
  animLoop();
  setTimeout(()=>sp(curLetterData.l), 350);
}

function updatePlayBtn(){
  const b=document.getElementById('playPauseBtn');
  if(b){ b.textContent=animOn?'⏸ To\'xtat':'▶ Ijro'; b.classList.toggle('playing',animOn); }
}

function toggleAnim(){
  if(animOn){ animOn=false; if(animRaf)cancelAnimationFrame(animRaf); }
  else { if(animT>=animDur) animT=0; animOn=true; animLoop(); }
  updatePlayBtn();
}
function replayAnim(){ startAnim(); }

/* ══════════════════════════════════════════════
   LETTER MODAL
══════════════════════════════════════════════ */
function openLetterModal(d){
  curLetterData = d;
  document.getElementById('modalLetter').textContent = d.l+' '+d.l.toLowerCase();
  document.getElementById('modalPhon').textContent   = d.p;
  document.getElementById('modalEx').textContent     = 'Misollar: '+d.ex;
  const pills = document.getElementById('wordPills');
  pills.innerHTML = d.w.map(w=>`<div class="word-pill" onclick="sp('${w}')">${w}</div>`).join('');
  document.getElementById('letterModal').classList.add('open');
  document.body.style.overflow = 'hidden';
  drawLetterFrame(0, d);
  setTimeout(startAnim, 150);
}
function closeLetterModal(){
  document.getElementById('letterModal').classList.remove('open');
  document.body.style.overflow = '';
  animOn=false; if(animRaf)cancelAnimationFrame(animRaf);
  synth && synth.cancel();
}

/* ══════════════════════════════════════════════
   BUILD ALPHABET
══════════════════════════════════════════════ */
function buildAlpha(){
  const g = document.getElementById('alphaGrid');
  if(!g) return;
  AD.forEach(d => {
    const el = document.createElement('div');
    el.className = 'alpha-card';
    el.style.borderColor = d.c + '44';
    el.innerHTML = `
      <div class="alpha-letter" style="color:${d.c}">${d.l}</div>
      <div class="alpha-phon">${d.p}</div>
      <div class="alpha-hint">▶ bosing</div>
    `;
    el.onclick = () => openLetterModal(d);
    g.appendChild(el);
  });
}

/* ══════════════════════════════════════════════
   NUMBERS
══════════════════════════════════════════════ */
const N20=[[1,'one'],[2,'two'],[3,'three'],[4,'four'],[5,'five'],[6,'six'],[7,'seven'],[8,'eight'],[9,'nine'],[10,'ten'],[11,'eleven'],[12,'twelve'],[13,'thirteen'],[14,'fourteen'],[15,'fifteen'],[16,'sixteen'],[17,'seventeen'],[18,'eighteen'],[19,'nineteen'],[20,'twenty']];
const N10=[[20,'twenty'],[30,'thirty'],[40,'forty'],[50,'fifty'],[60,'sixty'],[70,'seventy'],[80,'eighty'],[90,'ninety'],[100,'one hundred']];

function buildNums(){
  const g1=document.getElementById('numGrid1'), g2=document.getElementById('numGrid2');
  if(!g1) return;
  N20.forEach(x=>{
    const c=document.createElement('div'); c.className='num-card';
    c.innerHTML=`<span class="n">${x[0]}</span><span>${x[1]}</span>`;
    c.onclick=()=>sp(x[1]); g1.appendChild(c);
  });
  N10.forEach(x=>{
    const c=document.createElement('div'); c.className='num-card';
    c.innerHTML=`<span class="n">${x[0]}</span><span>${x[1]}</span>`;
    c.onclick=()=>sp(x[1]); g2.appendChild(c);
  });
}

/* ══════════════════════════════════════════════
   COLORS
══════════════════════════════════════════════ */
const CLR=[
  {en:'Red',uz:'Qizil',bg:'#c0392b',fg:'#fff'},
  {en:'Blue',uz:"Ko'k",bg:'#2980b9',fg:'#fff'},
  {en:'Green',uz:'Yashil',bg:'#27ae60',fg:'#fff'},
  {en:'Yellow',uz:'Sariq',bg:'#f1c40f',fg:'#000'},
  {en:'Orange',uz:"To'q sariq",bg:'#e67e22',fg:'#fff'},
  {en:'Purple',uz:'Binafsha',bg:'#8e44ad',fg:'#fff'},
  {en:'Pink',uz:'Pushti',bg:'#e91e8c',fg:'#fff'},
  {en:'Black',uz:'Qora',bg:'#222244',fg:'#eee'},
  {en:'White',uz:"Oq",bg:'#dce0e8',fg:'#333'},
  {en:'Grey',uz:'Kulrang',bg:'#7f8c8d',fg:'#fff'},
  {en:'Brown',uz:'Jigarrang',bg:'#7d4f2a',fg:'#fff'},
  {en:'Gold',uz:'Oltin',bg:'#d4a017',fg:'#000'}
];
function buildColors(){
  const g=document.getElementById('colorGrid');
  if(!g) return;
  CLR.forEach(c=>{
    const el=document.createElement('div'); el.className='color-card';
    el.style.background=c.bg;
    el.innerHTML=`<span class="c-en" style="color:${c.fg}">${c.en}</span><span class="c-uz" style="color:${c.fg}">${c.uz}</span>`;
    el.onclick=()=>sp(c.en);
    g.appendChild(el);
  });
}

/* ══════════════════════════════════════════════
   JOBS QUIZ
══════════════════════════════════════════════ */
const QD=[
  {q:'Who treats sick people?',o:['Teacher','Doctor','Driver','Cook'],a:1},
  {q:'Who drives a car for work?',o:['Nurse','Lawyer','Driver','Engineer'],a:2},
  {q:'Who teaches students?',o:['Teacher','Doctor','Chef','Programmer'],a:0},
  {q:'Who writes code?',o:['Lawyer','Police officer','Chef','Programmer'],a:3},
  {q:'"Hamshira" inglizcha nima?',o:['Doctor','Nurse','Cook','Teacher'],a:1},
  {q:'"Oshpaz" inglizcha nima?',o:['Driver','Engineer','Chef','Lawyer'],a:2},
  {q:'Who builds machines?',o:['Nurse','Engineer','Student','Cook'],a:1}
];
let qi=0, qs=0, qAnswered=false;
function buildJobQuiz(){ qi=0; qs=0; showJobQ(); }
function showJobQ(){
  qAnswered=false;
  const q=QD[qi];
  document.getElementById('qJobQ').textContent=q.q;
  document.getElementById('qJobNext').style.display='none';
  const c=document.getElementById('qJobO'); c.innerHTML='';
  q.o.forEach((opt,i)=>{
    const b=document.createElement('div'); b.className='quiz-opt'; b.textContent=opt;
    b.onclick=()=>checkJobQ(i,b); c.appendChild(b);
  });
  document.getElementById('qJobS').textContent='Savol '+(qi+1)+'/'+QD.length+' | To\'g\'ri: '+qs;
}
function checkJobQ(idx,btn){
  if(qAnswered) return; qAnswered=true;
  const a=QD[qi].a;
  document.querySelectorAll('#qJobO .quiz-opt')[a].classList.add('ok');
  if(idx!==a) btn.classList.add('no'); else { qs++; addXP(5,'To\'g\'ri javob!'); }
  sp(QD[qi].o[a]);
  document.getElementById('qJobS').textContent='Savol '+(qi+1)+'/'+QD.length+' | To\'g\'ri: '+qs;
  if(qi<QD.length-1) document.getElementById('qJobNext').style.display='inline-block';
  else document.getElementById('qJobS').textContent='Natija: '+qs+'/'+QD.length+' to\'g\'ri! 🎉';
}
function nextJobQ(){ qi++; if(qi<QD.length) showJobQ(); }

/* ══════════════════════════════════════════════
   GRAMMAR QUEST — LESSON DATA
══════════════════════════════════════════════ */
const LESSONS=[
  {id:0,icon:'🔵',title:'To Be: am / is / are',sub:"Ingliz tilining asosiy fe'li",diff:'A1',tag:'a1',xp:100,content:buildToBeLesson,questions:buildToBeQs},
  {id:1,icon:'💚',title:'Olmoshlar (Pronouns)',sub:'I, You, He, She, It, We, They',diff:'A1',tag:'a1',xp:100,content:buildPronounLesson,questions:buildPronounQs},
  {id:2,icon:'⏰',title:'Simple Present Tense',sub:'Hozirgi oddiy zamon',diff:'A1',tag:'a1',xp:100,content:buildSPTLesson,questions:buildSPTQs},
  {id:3,icon:'📦',title:"Have / Has & There is/are",sub:'Egalik va mavjudlik',diff:'A2',tag:'a2',xp:100,content:buildHaveLesson,questions:buildHaveQs},
  {id:4,icon:'👉',title:'This / That / These / Those',sub:"Ko'rsatish olmoshlari + Articles",diff:'A2',tag:'a2',xp:100,content:buildDemLesson,questions:buildDemQs},
  {id:5,icon:'🌀',title:'Present Continuous',sub:"Hozir bo'layotgan harakatlar",diff:'A2',tag:'a2',xp:100,content:buildPContLesson,questions:buildPContQs},
  {id:6,icon:'🔮',title:'Prepositions of Time & Place',sub:'in / on / at / under / next to',diff:'B1',tag:'b1',xp:100,content:buildPrepLesson,questions:buildPrepQs}
];

/* Grammar Engine State */
let curLesson=-1, curQ=0, curScore=0, curAnswered=false, curQList=[];

function saveGramState(){ saveApp(); }
function loadGramState(){
  const gs = APP.gramState;
  if(!gs.unlocked || gs.unlocked.length < 7){
    gs.unlocked=[true,false,false,false,false,false,false];
    gs.scores=[null,null,null,null,null,null,null];
    gs.xp=0;
  }
}

/* ══ RENDER LESSON ROAD ══ */
function renderLessonRoad(){
  loadGramState();
  const road=document.getElementById('lessonRoad');
  if(!road) return;

  // Make sure panels are hidden, road visible
  document.getElementById('lessonPanel').classList.add('hidden');
  document.getElementById('testPanel').classList.add('hidden');
  document.getElementById('resultPanel').classList.add('hidden');
  document.getElementById('gramHero').classList.remove('hidden');
  document.getElementById('dailyChallenge').classList.remove('hidden');
  road.classList.remove('hidden');

  road.innerHTML='';
  const gs = APP.gramState;

  LESSONS.forEach((l,i)=>{
    if(i>0){ const c=document.createElement('div'); c.className='road-connector'; road.appendChild(c); }
    const locked=!gs.unlocked[i];
    const comp=gs.scores[i]!==null && gs.scores[i]>=75;
    const stars=gs.scores[i]===null ? '○○○' : gs.scores[i]>=90?'★★★':gs.scores[i]>=75?'★★○':'★○○';
    const scoreDisp=gs.scores[i]===null?(locked?'🔒':'-'):(gs.scores[i]+'/100');
    const scoreColor=gs.scores[i]===null?'var(--text-3)':(gs.scores[i]>=75?'var(--brand-3)':'var(--brand-2)');

    const cls='lesson-node '+(locked?'locked':comp?'completed':'unlocked-active');
    const node=document.createElement('div');
    node.className=cls;
    node.innerHTML=`
      <div class="ln-icon-wrap">
        ${l.icon}
        ${locked?'<div class="ln-lock">🔒</div>':''}
      </div>
      <div class="ln-info">
        <div class="ln-title">${l.title}</div>
        <div class="ln-meta">
          <span class="diff-tag diff-${l.tag}">${l.diff}</span>
          <span>${l.sub}</span>
        </div>
      </div>
      <div class="ln-score">
        <div class="ln-score-num" style="color:${scoreColor}">${scoreDisp}</div>
        <div class="ln-score-lbl">BALL</div>
        <div class="ln-stars">${stars}</div>
      </div>
    `;
    if(!locked){ (function(idx){ node.onclick=()=>openLesson(idx); })(i); }
    road.appendChild(node);
  });
}

/* ══ OPEN LESSON ══ */
function openLesson(idx){
  curLesson=idx;
  const l=LESSONS[idx];
  const gs=APP.gramState;

  document.getElementById('lpEmoji').textContent=l.icon;
  document.getElementById('lpTitle').textContent=l.title;
  document.getElementById('lpSub').textContent=l.sub;
  document.getElementById('lpDiff').textContent=l.diff;
  document.getElementById('lpContent').innerHTML=l.content();

  const prev=gs.scores[idx];
  let note='';
  if(prev!==null) note=`So'nggi ball: <strong style="color:${prev>=75?'var(--brand-3)':'var(--brand-2)'}">${prev}/100</strong>`;
  document.getElementById('startTestNote').innerHTML=note;

  document.getElementById('gramHero').classList.add('hidden');
  document.getElementById('dailyChallenge').classList.add('hidden');
  document.getElementById('lessonRoad').classList.add('hidden');
  document.getElementById('testPanel').classList.add('hidden');
  document.getElementById('resultPanel').classList.add('hidden');
  document.getElementById('lessonPanel').classList.remove('hidden');
  window.scrollTo({top:0,behavior:'smooth'});
}

function closeLessonPanel(){
  document.getElementById('lessonPanel').classList.add('hidden');
  document.getElementById('testPanel').classList.add('hidden');
  document.getElementById('resultPanel').classList.add('hidden');
  document.getElementById('gramHero').classList.remove('hidden');
  document.getElementById('dailyChallenge').classList.remove('hidden');
  document.getElementById('lessonRoad').classList.remove('hidden');
  renderLessonRoad();
  refreshUI();
}

/* ══ TEST ENGINE ══ */
function startTest(){
  const l=LESSONS[curLesson];
  curQList=l.questions(); curQ=0; curScore=0; curAnswered=false;
  document.getElementById('tpTitle').textContent=l.title+' — Test';
  document.getElementById('tpSub').textContent='Savollar: '+curQList.length+' | 75+ ball kerak';
  document.getElementById('lessonPanel').classList.add('hidden');
  document.getElementById('resultPanel').classList.add('hidden');
  document.getElementById('testPanel').classList.remove('hidden');
  showQuestion();
  window.scrollTo({top:0,behavior:'smooth'});
}

function backToLesson(){
  document.getElementById('testPanel').classList.add('hidden');
  document.getElementById('lessonPanel').classList.remove('hidden');
}

function updateTestProgress(){
  const pct=(curQ/curQList.length)*100;
  document.getElementById('tpBar').style.width=pct+'%';
  const pts=Math.round((curScore/curQList.length)*100);
  document.getElementById('tpChip').textContent=curQ+'/'+curQList.length+' | '+pts+'%';
}

function showQuestion(){
  if(curQ>=curQList.length){ endTest(); return; }
  const q=curQList[curQ]; curAnswered=false;
  updateTestProgress();
  let html=`<div class="question-block"><div class="q-num">Savol ${curQ+1} / ${curQList.length}</div>`;
  if(q.type==='mc'){
    html+=`<div class="q-text">${q.q}</div><div class="q-opts" id="qOpts">`;
    q.opts.forEach((o,i)=>{ html+=`<div class="q-opt" onclick="checkMC(${i},${q.a})">${o}</div>`; });
    html+='</div>';
  } else if(q.type==='fill'||q.type==='transform'){
    html+=`<div class="q-text">${q.q}</div>`;
    if(q.type==='transform') html+=`<div class="rule-card warn" style="padding:10px 14px;margin-bottom:10px"><em style="font-size:12px;color:var(--text-2)">Hint: </em><span style="font-size:12px;color:#b0a8ff">${q.hint}</span></div>`;
    html+=`<input class="q-fill-input" id="fillIn" placeholder="Javobingizni yozing..." autocomplete="off"><br><button class="q-submit-btn" onclick="checkFill()">Tekshirish ✓</button>`;
  }
  html+=`<div class="q-explain" id="qExp">${q.exp}</div>`;
  html+=`<button class="q-next-btn" id="qNext" onclick="nextQuestion()">Keyingi →</button></div>`;
  document.getElementById('tpContent').innerHTML=html;
}

function checkMC(sel,ans){
  if(curAnswered)return; curAnswered=true;
  const opts=document.querySelectorAll('.q-opt');
  opts.forEach(o=>o.classList.add('done'));
  if(sel===ans){ curScore++; opts[ans].classList.add('correct'); }
  else{ opts[ans].classList.add('correct'); opts[sel].classList.add('wrong'); }
  document.getElementById('qExp').style.display='block';
  document.getElementById('qNext').style.display='inline-block';
}

function checkFill(){
  if(curAnswered) return;
  const inp=document.getElementById('fillIn'); if(!inp) return;
  const val=inp.value.trim().toLowerCase();
  const q=curQList[curQ];
  const correct=Array.isArray(q.a)?q.a.map(x=>x.toLowerCase()):q.a.toLowerCase().split('|');
  const ok=correct.includes(val);
  inp.classList.add(ok?'correct':'wrong'); inp.disabled=true;
  if(ok) curScore++;
  else{
    const hint=document.createElement('div');
    hint.style.cssText='font-size:12px;color:var(--brand-2);margin-top:6px';
    hint.textContent="To'g'ri javob: "+correct[0];
    inp.parentNode.insertBefore(hint, inp.nextElementSibling?.nextElementSibling || null);
  }
  curAnswered=true;
  document.getElementById('qExp').style.display='block';
  document.getElementById('qNext').style.display='inline-block';
}

function nextQuestion(){ curQ++; showQuestion(); window.scrollTo({top:0,behavior:'smooth'}); }

function endTest(){
  const pct=Math.round((curScore/curQList.length)*100);
  const pass=pct>=75;
  const gs=APP.gramState;
  const wasScore=gs.scores[curLesson];

  APP.testsCompleted = (APP.testsCompleted||0)+1;
  if(wasScore===null||pct>wasScore){
    const xpGain=wasScore===null?LESSONS[curLesson].xp:Math.max(0,pct-wasScore);
    gs.xp+=xpGain; APP.xp+=xpGain; gs.scores[curLesson]=pct;
  }

  let unlockNext=false;
  if(pass && curLesson+1<LESSONS.length && !gs.unlocked[curLesson+1]){
    gs.unlocked[curLesson+1]=true; unlockNext=true;
    showToast('🔓 Yangi dars ochildi!','xp');
  }
  saveApp(); checkAchievements();

  document.getElementById('testPanel').classList.add('hidden');
  document.getElementById('resultPanel').classList.remove('hidden');

  const icon=pct>=90?'🌟':pct>=75?'🎉':'😤';
  const msg=pct>=90?"Mukammal! Ajoyib natija!":pct>=75?"Zo'r! Siz o'tdingiz!":"Hali ozroq mashq kerak...";
  document.getElementById('resultEmoji').textContent=icon;
  const scoreEl=document.getElementById('resultScore');
  scoreEl.textContent=pct+'/100'; scoreEl.className='result-score '+(pass?'pass':'fail');
  document.getElementById('resultMsg').textContent=msg;
  document.getElementById('resultDetail').innerHTML=`To'g'ri: <strong>${curScore}/${curQList.length}</strong> savol`+(pass?' &nbsp;|&nbsp; ✅ Keyingi dars uchun ruxsat!':" &nbsp;|&nbsp; ❌ 75+ ball kerak");

  const ub=document.getElementById('unlockBanner');
  ub.classList.toggle('hidden', !unlockNext);
  const nb=document.getElementById('nextLessonBtn');
  nb.style.display=(pass&&curLesson+1<LESSONS.length)?'inline-block':'none';

  window.scrollTo({top:0,behavior:'smooth'});
  refreshUI();
  updateLBIfRegistered();
}

function retryTest(){ startTest(); }
function goNextLesson(){ openLesson(curLesson+1); }

/* Daily Challenge */
function startDailyChallenge(){
  const today=new Date().toDateString();
  const doneDC=localStorage.getItem('dailyDone');
  if(doneDC===today){
    showToast('Bugungi vazifa allaqachon bajarildi! ✅','xp');
    return;
  }
  // Open first incomplete lesson
  const gs=APP.gramState;
  let target=0;
  for(let i=0;i<LESSONS.length;i++){
    if(gs.scores[i]===null&&gs.unlocked[i]){ target=i; break; }
  }
  openLesson(target);
}
function markDailyDone(){
  localStorage.setItem('dailyDone',new Date().toDateString());
  document.getElementById('dailySub').textContent='Bugungi vazifa bajarildi! ✅';
  document.getElementById('dailyArrow').textContent='✅';
}

/* ══════════════════════════════════════════════
   LEADERBOARD
══════════════════════════════════════════════ */
let myLBName='';
function loadLB(){ try{return JSON.parse(localStorage.getItem(LB_KEY))||[];}catch(e){return[];} }
function saveLB(arr){ try{localStorage.setItem(LB_KEY,JSON.stringify(arr));}catch(e){} }

function saveLBEntry(){
  const inp=document.getElementById('lbNameInput');
  if(!inp||!inp.value.trim()){ alert("Ismingizni kiriting!"); return; }
  myLBName=inp.value.trim();
  updateLBIfRegistered();
}

function updateLBIfRegistered(){
  if(!myLBName) return;
  const arr=loadLB();
  const completed=(APP.gramState.scores||[]).filter(x=>x!==null&&x>=75).length;
  const entry={name:myLBName, xp:APP.xp, lessons:completed};
  const idx=arr.findIndex(e=>e.name===myLBName);
  if(idx>=0) arr[idx]=entry; else arr.push(entry);
  arr.sort((a,b)=>b.xp-a.xp);
  saveLB(arr); renderLB();
}

function renderLB(){
  const arr=loadLB();
  const el=document.getElementById('lbList');
  if(!el) return;
  if(!arr.length){ el.innerHTML='<div class="lb-empty">Hali hech kim yo\'q. Birinchi bo\'ling! 🏆</div>'; return; }
  el.innerHTML=arr.slice(0,20).map((e,i)=>{
    const rank=i+1;
    const rankDisp=rank===1?'🥇':rank===2?'🥈':rank===3?'🥉':'#'+rank;
    const rankCls=rank===1?'gold':rank===2?'silver':rank===3?'bronze':'';
    const isMe=e.name===myLBName;
    return `
      <div class="lb-entry ${isMe?'me':''}">
        <div class="lb-rank ${rankCls}">${rankDisp}</div>
        <div class="lb-name">${isMe?'⭐ ':''} ${e.name}</div>
        <div class="lb-lessons">${e.lessons||0}/7 🎓</div>
        <div class="lb-xp">${e.xp} XP</div>
      </div>
    `;
  }).join('');
}

function openLB(){
  document.getElementById('lbModal').classList.add('open');
  document.body.style.overflow='hidden';
  renderLB();
}
function closeLB(){
  document.getElementById('lbModal').classList.remove('open');
  document.body.style.overflow='';
}

/* ══════════════════════════════════════════════
   VOCABULARY GAME
══════════════════════════════════════════════ */
const VOCAB=[
  {en:'Apple',uz:'Olma'},{en:'Water',uz:'Suv'},{en:'House',uz:'Uy'},{en:'Book',uz:'Kitob'},
  {en:'Dog',uz:'It'},{en:'Cat',uz:'Mushuk'},{en:'Sun',uz:'Quyosh'},{en:'Moon',uz:'Oy'},
  {en:'School',uz:'Maktab'},{en:'Friend',uz:"Do'st"},{en:'Food',uz:'Ovqat'},{en:'Car',uz:'Mashina'},
  {en:'Love',uz:'Sevgi'},{en:'Time',uz:'Vaqt'},{en:'Work',uz:'Ish'},{en:'Family',uz:'Oila'},
  {en:'Money',uz:'Pul'},{en:'Health',uz:'Salomatlik'},{en:'Music',uz:'Musiqa'},{en:'City',uz:'Shahar'},
  {en:'Tree',uz:'Daraxt'},{en:'Flower',uz:"Gul"},{en:'Rain',uz:'Yomg\'ir'},{en:'Wind',uz:'Shamol'},
  {en:'Fire',uz:'Olov'},{en:'Night',uz:'Tun'},{en:'Day',uz:'Kun'},{en:'Year',uz:'Yil'},
  {en:'King',uz:'Qirol'},{en:'Star',uz:'Yulduz'},{en:'Ocean',uz:'Okean'},{en:'Mountain',uz:'Tog\''}
];

let gameIdx=0, gameScore=0, gameLives=3, gameStreak=0, gameAnswered=false, gameWords=[];

function shuffleArr(a){ return a.sort(()=>Math.random()-.5); }

function startGame(){
  gameWords = shuffleArr([...VOCAB]);
  gameIdx=0; gameScore=0; gameLives=3; gameStreak=0;
  document.getElementById('gameEndArea').style.display='none';
  document.getElementById('gameScore').textContent='0';
  document.getElementById('gameStreak').textContent='0';
  showGameQ();
}

function showGameQ(){
  if(gameLives<=0 || gameIdx>=gameWords.length){ endGame(); return; }
  gameAnswered=false;
  const word=gameWords[gameIdx];
  document.getElementById('gameWord').textContent=word.en;
  document.getElementById('gameHint').textContent='O\'zbekcha tarjimasini tanlang';
  document.getElementById('gameLives').textContent='❤️'.repeat(gameLives)+'🖤'.repeat(3-gameLives);

  // 4 options: 1 correct + 3 wrong
  const others=shuffleArr(VOCAB.filter(v=>v.en!==word.en)).slice(0,3);
  const opts=shuffleArr([word,...others]);
  const container=document.getElementById('gameOpts');
  container.innerHTML=opts.map((o,i)=>
    `<div class="game-opt" onclick="checkGameQ(this,'${o.uz}','${word.uz}')">${o.uz}</div>`
  ).join('');
}

function checkGameQ(el, selected, correct){
  if(gameAnswered) return; gameAnswered=true;
  const allOpts=document.querySelectorAll('.game-opt');
  allOpts.forEach(o=>{ if(o.textContent===correct) o.classList.add('correct'); });
  if(selected===correct){
    el.classList.add('correct'); gameScore++; gameStreak++;
    addXP(2,'O\'yin');
    if(gameScore > APP.gameBestScore){ APP.gameBestScore=gameScore; saveApp(); }
  } else {
    el.classList.add('wrong'); gameLives--; gameStreak=0;
  }
  document.getElementById('gameScore').textContent=gameScore;
  document.getElementById('gameStreak').textContent=gameStreak;
  sp(gameWords[gameIdx].en);
  setTimeout(()=>{ gameIdx++; showGameQ(); }, 1200);
}

function endGame(){
  document.getElementById('gameEndArea').style.display='block';
  document.getElementById('gameOpts').innerHTML='';
  document.getElementById('gameWord').textContent='🎮';
  document.getElementById('gameHint').textContent='O\'yin tugadi!';
  const emoji=gameScore>=20?'🏆':gameScore>=10?'🌟':gameScore>=5?'😊':'😅';
  document.getElementById('gameEndEmoji').textContent=emoji;
  document.getElementById('gameEndScore').textContent=gameScore+' ball';
  checkAchievements(); refreshUI();
}

function restartGame(){ startGame(); }

/* ══════════════════════════════════════════════
   PARTICLES BACKGROUND
══════════════════════════════════════════════ */
(function(){
  const cv=document.getElementById('particles');
  const ct=cv.getContext('2d');
  let W,H,particles=[];
  function resize(){ W=cv.width=window.innerWidth; H=cv.height=window.innerHeight; }
  resize(); window.addEventListener('resize',resize);
  for(let i=0;i<50;i++){
    particles.push({x:Math.random()*window.innerWidth,y:Math.random()*window.innerHeight,r:Math.random()*2+.5,vx:(Math.random()-.5)*.3,vy:(Math.random()-.5)*.3,a:Math.random()*.5+.1});
  }
  function loop(){
    ct.clearRect(0,0,W,H);
    const isDark=document.documentElement.dataset.theme!=='light';
    particles.forEach(p=>{
      p.x+=p.vx; p.y+=p.vy;
      if(p.x<0)p.x=W; if(p.x>W)p.x=0;
      if(p.y<0)p.y=H; if(p.y>H)p.y=0;
      ct.beginPath(); ct.arc(p.x,p.y,p.r,0,Math.PI*2);
      ct.fillStyle=isDark?`rgba(108,99,255,${p.a})`:`rgba(108,99,255,${p.a*.4})`;
      ct.fill();
    });
    requestAnimationFrame(loop);
  }
  loop();
})();

/* ══════════════════════════════════════════════
   LESSON CONTENT BUILDERS
══════════════════════════════════════════════ */
function sec(title, content){ return `<div class="lc-section"><div class="lc-heading">${title}</div>${content}</div>`; }
function rule(body, type=''){ return `<div class="rule-card ${type}"><div class="rule-card-body">${body}</div></div>`; }
function formula(f){ return `<div class="formula-box">${f}</div>`; }
function exGrid(items){ return `<div class="ex-grid">${items}</div>`; }
function ex(en,uz,cls='',note=''){ return `<div class="ex-item ${cls}"><div class="ex-en">${en}</div><div class="ex-uz">${uz}</div>${note?'<div class="ex-note">'+note+'</div>':''}</div>`; }
function tip(body){ return `<div class="tip-card">${body}</div>`; }

function buildToBeLesson(){
  return sec('📖 Qoida',
    rule('<strong>To Be nima?</strong><br>O&#x02BC;zbek tilidagi <strong>"bo\'lmoq"</strong> ga to\'g\'ri keladi. Uch shakli bor: <strong>am, is, are</strong>.')
    +formula('I &rarr; <strong>am</strong> &nbsp;|&nbsp; He/She/It &rarr; <strong>is</strong> &nbsp;|&nbsp; You/We/They &rarr; <strong>are</strong>')
  )
  +sec('✅ Tasdiqlash (Positive)', exGrid(
    ex('I <strong>am</strong> a student.','Men talabaman.')
    +ex('He <strong>is</strong> a doctor.','U shifokor.')
    +ex('She <strong>is</strong> beautiful.','U chiroyli.')
    +ex('We <strong>are</strong> friends.','Biz do\'stmiz.')
    +ex('They <strong>are</strong> happy.','Ular xursand.')
    +ex('It <strong>is</strong> a cat.','Bu mushuk.')
  ))
  +sec('❌ Inkor (Negative)',
    formula('am/is/are + NOT')
    +exGrid(
      ex('I <strong>am not</strong> tired.','Men charchamadim.','neg')
      +ex('He <strong>is not</strong> here. (He isn\'t)','U bu yerda emas.','neg')
      +ex('They <strong>are not</strong> ready. (aren\'t)','Ular tayyor emas.','neg')
    )
  )
  +sec('❓ Savol (Question)',
    formula('Am/Is/Are + Subject + ...?')
    +exGrid(
      ex('<strong>Are</strong> you okay?','Yaxshimisiz?','q')
      +ex('<strong>Is</strong> she a teacher?','U o\'qituvchimi?','q')
      +ex('<strong>Am</strong> I late?','Kechikdimmi?','q')
    )
  )
  +sec('💡 Qisqartmalar',
    tip('<strong>I\'m &bull; He\'s &bull; She\'s &bull; We\'re &bull; They\'re</strong> &bull; isn\'t &bull; aren\'t<br><br>⚠️ <strong>Am not</strong> ning rasmiy qisqartmasi yo\'q!')
  );
}

function buildPronounLesson(){
  return sec('📖 Olmoshlar turlari',
    rule('<strong>Subject</strong> — gap egasi (I, You, He...)<br><strong>Object</strong> — to\'ldiruvchi (me, you, him...)<br><strong>Possessive</strong> — egalik (my, your, his...)')
  )
  +sec('📊 To\'liq jadval',
    `<div style="overflow-x:auto"><table class="data-table">
    <tr><th>Shaxs</th><th>Subject</th><th>Object</th><th>Possessive</th><th>O\'zbek</th></tr>
    <tr><td>1-shaxs</td><td class="en-word">I</td><td class="en-word">me</td><td class="en-word">my</td><td class="uz-word">Men/Mening</td></tr>
    <tr><td>2-shaxs</td><td class="en-word">You</td><td class="en-word">you</td><td class="en-word">your</td><td class="uz-word">Siz/Sening</td></tr>
    <tr><td>3 (erkak)</td><td class="en-word">He</td><td class="en-word">him</td><td class="en-word">his</td><td class="uz-word">U/Uning</td></tr>
    <tr><td>3 (ayol)</td><td class="en-word">She</td><td class="en-word">her</td><td class="en-word">her</td><td class="uz-word">U/Uning</td></tr>
    <tr><td>3 (narsa)</td><td class="en-word">It</td><td class="en-word">it</td><td class="en-word">its</td><td class="uz-word">U/Uning</td></tr>
    <tr><td>Ko\'plik 1</td><td class="en-word">We</td><td class="en-word">us</td><td class="en-word">our</td><td class="uz-word">Biz/Bizning</td></tr>
    <tr><td>Ko\'plik 2/3</td><td class="en-word">They</td><td class="en-word">them</td><td class="en-word">their</td><td class="uz-word">Ular/Ularning</td></tr>
    </table></div>`
  )
  +sec('✅ Misollar', exGrid(
    ex('<strong>I</strong> love <strong>my</strong> country.','Men vatanimni yaxshi ko\'raman.','','I=subject | my=possessive')
    +ex('She gave <strong>him</strong> a book.','U unga kitob berdi.','','him=object (not he!)')
    +ex('This is <strong>her</strong> bag.','Bu uning sumkasi.')
    +ex('<strong>We</strong> invited <strong>them</strong> to <strong>our</strong> party.','Biz ularni bizning ziyofatimizga taklif qildik.')
  ))
  +sec('💡 Eslatma', tip('⚠️ <strong>Its</strong> (egalik) ≠ <strong>It\'s</strong> (It is)'));
}

function buildSPTLesson(){
  return sec('📖 Qoida',
    rule('<strong>Simple Present nima uchun?</strong><br>• Odatdagi harakatlar (every day, always)<br>• Umumiy haqiqatlar (The sun rises)<br>• Doimiy holat (I live in Tashkent)')
    +formula('Tasdiq: Subject + verb (+s/es — he/she/it)')
    +formula('Inkor: Subject + don\'t/doesn\'t + verb')
    +formula('Savol: Do/Does + Subject + verb?')
  )
  +sec('⚠️ He/She/It qoidasi', rule(
    'Ko\'pchilik: +<strong>s</strong> → works, eats<br>'
    +'-ch/-sh/-ss/-o: +<strong>es</strong> → watches, goes<br>'
    +'Undosh+y: y→<strong>ies</strong> → studies, flies<br>'
    +'Unli+y: +<strong>s</strong> → plays, says','warn'
  ))
  +sec('✅ Misollar', exGrid(
    ex('I <strong>work</strong> every day.','Men har kun ishlayman.')
    +ex('She <strong>works</strong> at 8 AM.','U soat 8 da ishlaydi.')
    +ex('He <strong>studies</strong> English.','U ingliz tilini o\'qiydi.')
    +ex('I <strong>don\'t</strong> like coffee.','Men qahvani yoqtirmayman.','neg')
    +ex('She <strong>doesn\'t</strong> eat meat.','U go\'sht emaydi.','neg',"doesn't → fe'l oddiy shaklda!")
    +ex('<strong>Does</strong> he live here?','U bu yerda yashaydimi?','q')
  ))
  +sec('💡 Signal so\'zlar', tip('<strong>always</strong> | <strong>usually</strong> | <strong>often</strong> | <strong>sometimes</strong> | <strong>never</strong> | <strong>every day/week</strong>'));
}

function buildHaveLesson(){
  return sec('📖 Have vs Has',
    rule('<strong>have</strong> → I / You / We / They<br><strong>has</strong> → He / She / It')
    +formula('I have a book. / She has a car.')
  )
  +sec('✅ Misollar', exGrid(
    ex('I <strong>have</strong> a dog.','Mening itim bor.')
    +ex('She <strong>has</strong> long hair.','Uning uzun sochi bor.')
    +ex('He <strong>doesn\'t have</strong> a phone.','Uning telefoni yo\'q.','neg')
    +ex('<strong>Do</strong> you <strong>have</strong> time?','Vaqtingiz bormi?','q')
  ))
  +sec('🏠 There is / There are',
    rule('<strong>There is</strong> → bitta narsa (singular)<br><strong>There are</strong> → ko\'p narsa (plural)')
    +exGrid(
      ex('<strong>There is</strong> a book on the table.','Stolda bir kitob bor.')
      +ex('<strong>There are</strong> 20 students in class.','Sinfda 20 o\'quvchi bor.')
      +ex('<strong>There isn\'t</strong> any water.','Hech qanday suv yo\'q.','neg')
      +ex('<strong>Is there</strong> a bank near here?','Bu yaqinda bank bormi?','q')
    )
  )
  +sec('💡 Some / Any', tip('<strong>some</strong> — tasdiq: I have <strong>some</strong> money.<br><strong>any</strong> — inkor va savolda: I don\'t have <strong>any</strong> money.'));
}

function buildDemLesson(){
  return sec('📖 Ko\'rsatish olmoshlari',
    rule('<strong>This</strong> — yaqin, bitta &nbsp;|&nbsp; <strong>That</strong> — uzoq, bitta<br><strong>These</strong> — yaqin, ko\'p &nbsp;|&nbsp; <strong>Those</strong> — uzoq, ko\'p')
  )
  +sec('✅ Misollar', exGrid(
    ex('<strong>This</strong> is my phone.','Bu (yaqinimda) mening telefonim.')
    +ex('<strong>That</strong> is a school.','U (narida) maktab.')
    +ex('<strong>These</strong> are my keys.','Bular mening kalitlarim.')
    +ex('<strong>Those</strong> books are interesting.','U narida kitoblar qiziqarli.')
  ))
  +sec('📰 Articles: a / an / the',
    rule('<strong>a / an</strong> — noaniq (birinchi marta)<br><strong>the</strong> — aniq (allaqachon ma\'lum)')
    +formula('a + undosh: a book, a car')
    +formula('an + unli: an apple, an orange')
    +exGrid(
      ex('I saw <strong>a</strong> cat. <strong>The</strong> cat was black.','Men bir mushuk ko\'rdim. U mushuk qora edi.')
      +ex('She is <strong>an</strong> engineer.','U muhandis.')
    )
  )
  +sec('💡 Artikl ishlatilmaydi', tip('Umumiy: <strong>Dogs are friendly.</strong><br>Mavhum: <strong>I like music.</strong><br>Kasb: <strong>He is a doctor.</strong>'));
}

function buildPContLesson(){
  return sec('📖 Present Continuous nima?',
    rule('<strong>Hozir davom etayotgan harakat</strong><br>Signal so\'zlar: <strong>now, right now, at the moment, look!, listen!</strong>')
    +formula('Subject + am/is/are + verb-ING')
  )
  +sec('⚠️ -ing qo\'shish qoidalari', rule(
    'Ko\'pchilik: +<strong>ing</strong> → working<br>'
    +'-e bilan tugasa: e o\'chir + <strong>ing</strong> → making<br>'
    +'Qisqa+undosh: ikkilashtir + <strong>ing</strong> → running, sitting<br>'
    +'-ie bilan: ie→y + <strong>ing</strong> → lying','warn'
  ))
  +sec('✅ Misollar', exGrid(
    ex('I <strong>am studying</strong> now.','Men hozir o\'qiyapman.')
    +ex('She <strong>is cooking</strong> dinner.','U kechki ovqat pishiryapti.')
    +ex('He <strong>is not watching</strong> TV.','U TV ko\'rmayapti.','neg')
    +ex('<strong>Are</strong> you <strong>listening</strong>?','Tinglayapsizmi?','q')
  ))
  +sec('⚡ Simple Present vs Continuous',
    tip('<strong>I read every day.</strong> → Odatdagi (Simple Present)<br><strong>I am reading now.</strong> → Hozir (Continuous)<br><br>⚠️ Bu fe\'llar Continuous bilan ishlatilmaydi: <strong>know, like, love, want, need, understand, believe</strong>')
  );
}

function buildPrepLesson(){
  return sec('📖 Vaqt predloglari',
    rule('<strong>at</strong> — aniq vaqt: at 5 PM, at noon, at midnight<br><strong>on</strong> — kun va sana: on Monday, on July 4th<br><strong>in</strong> — oy, yil, mavsim: in January, in 2025, in summer')
  )
  +sec('🏠 Joy predloglari',
    rule('<strong>at</strong> — aniq nuqta: at school, at home, at the door<br><strong>on</strong> — yuzada: on the table, on the wall<br><strong>in</strong> — ichida: in the box, in Tashkent')
    +exGrid(
      ex('The book is <strong>on</strong> the table.','Kitob stolning ustida.')
      +ex('She lives <strong>in</strong> London.','U Londonda yashaydi.')
      +ex('I\'ll meet you <strong>at</strong> the station.','Stantsiyada ko\'rishamiz.')
    )
  )
  +sec('↔️ Qo\'shimcha predloglar', exGrid(
    ex('<strong>under</strong> the table','stolning tagida')
    +ex('<strong>next to</strong> the bank','bank yonida')
    +ex('<strong>between</strong> the shops','do\'konlar orasida')
    +ex('<strong>in front of</strong> the school','maktab oldida')
    +ex('<strong>behind</strong> the house','uy orqasida')
    +ex('<strong>above</strong> the clouds','bulutlar ustida')
  ))
  +sec('💡 Eslatma', tip('<strong>in the morning/afternoon/evening</strong> (kun qismlarida IN)<br><strong>at night, at noon, at midnight</strong> (maxsus vaqtlarda AT)'));
}

/* ══════════════════════════════════════════════
   QUESTION BUILDERS
══════════════════════════════════════════════ */
function buildToBeQs(){return[
  {type:'mc',q:'Qaysi variant to\'g\'ri? "Men shifokorman."',opts:['I is a doctor.','I am a doctor.','I are a doctor.','Am I a doctor.'],a:1,exp:'I bilan faqat AM ishlatiladi.'},
  {type:'mc',q:'"She ___ a teacher." — bo\'sh joyga nima?',opts:['am','are','is','be'],a:2,exp:'He/She/It bilan IS ishlatiladi.'},
  {type:'mc',q:'Qaysi gap to\'g\'ri? (Inkor)',opts:['They not are ready.','They are not ready.','They aren\'t not ready.','Are they not ready?'],a:1,exp:'are + not yoki aren\'t.'},
  {type:'fill',q:'To\'ldiring: "We ___ students."',a:'are',exp:'We bilan ARE.'},
  {type:'mc',q:'"___ you tired?" — savol shakli',opts:['Am','Is','Are','Be'],a:2,exp:'You bilan Are savol shaklida birinchi.'},
  {type:'mc',q:'"He ___ not at home." — to\'g\'ri shakl',opts:['am','are','is','be'],a:2,exp:'He bilan IS.'},
  {type:'mc',q:'Qaysi gap xato?',opts:['She is my friend.','He am a student.','They are happy.','It is a car.'],a:1,exp:'He bilan AM emas, IS.'},
  {type:'fill',q:'To\'ldiring: "I ___ not hungry."',a:['am'],exp:'I am not hungry.'},
  {type:'mc',q:'"___ it a cat or a dog?"',opts:['Am','Are','Is','Be'],a:2,exp:'It bilan Is.'},
  {type:'mc',q:'Qaysi qisqartma to\'g\'ri?',opts:['I amn\'t late.','I\'m not late.','I not am late.','Am not I late.'],a:1,exp:'I am not = I\'m not.'}
];}
function buildPronounQs(){return[
  {type:'mc',q:'"Ali is my friend. ___ is a doctor."',opts:['She','He','They','It'],a:1,exp:'Ali erkak ism — He.'},
  {type:'mc',q:'"Give ___ the book, please." (menga)',opts:['I','my','me','mine'],a:2,exp:'To\'ldiruvchi holda "me".'},
  {type:'fill',q:'To\'ldiring: "This is ___ bag." (Sara — unga tegishli)',a:['her'],exp:'She (ayol) possessive = her.'},
  {type:'mc',q:'Qaysi gapda xato?',opts:['I love my dog.','Her is a teacher.','We need your help.','They gave us a gift.'],a:1,exp:'"Her is" xato — to\'g\'risi "She is".'},
  {type:'mc',q:'"Biz ularni kutdik." — to\'g\'ri tarjima',opts:['We waited us.','We waited they.','We waited them.','Us waited them.'],a:2,exp:'them = object (ular).'},
  {type:'mc',q:'"___ book is interesting." (uning — erkak)',opts:['He','Him','His','Her'],a:2,exp:'Egalik (erkak) = His.'},
  {type:'mc',q:'"The cat licked ___ paw."',opts:['his','her','its','their'],a:2,exp:'Narsa/hayvon = its.'},
  {type:'fill',q:'Bo\'sh joy: "What is ___ phone number?" (Siz uchun)',a:['your'],exp:'Siz/Sening = your.'},
  {type:'fill',q:'"This is ___ bag." (u erkak — uning)',a:['his'],exp:'He (erkak) → his.'},
  {type:'mc',q:'Qaysi gap grammatik to\'g\'ri?',opts:['Me and him went there.','He and I went there.','Him and I went there.','I and him went there.'],a:1,exp:'Gap egasi: He and I.'}
];}
function buildSPTQs(){return[
  {type:'mc',q:'"She ___ to school every day."',opts:['go','goes','goed','is going'],a:1,exp:'She uchun goes (go+es).'},
  {type:'fill',q:'"He ___ English every day." (study)',a:['studies'],exp:'study + 3-shaxs = studies (y→ies).'},
  {type:'mc',q:'Inkor: "I ___ meat."',opts:['don\'t eat','doesn\'t eat','not eat','don\'t eats'],a:0,exp:'I + don\'t + verb.'},
  {type:'mc',q:'Savol: "___ she like pizza?"',opts:['Do','Does','Is','Are'],a:1,exp:'3-shaxs savolda Does.'},
  {type:'fill',q:'"He ___ TV every night." (watch)',a:['watches'],exp:'watch + es = watches.'},
  {type:'mc',q:'Qaysi gapda xato?',opts:['I work here.','She works hard.','He don\'t like it.','They study English.'],a:2,exp:'He bilan "doesn\'t" (don\'t emas).'},
  {type:'fill',q:'"They ___ football." (inkor — play)',a:["don't play","do not play"],exp:'They + don\'t + play.'},
  {type:'mc',q:'"The sun ___ in the east." — umumiy haqiqat',opts:['rise','rises','is rising','rose'],a:1,exp:'Simple Present + rises (3-shaxs).'},
  {type:'mc',q:'Signal so\'z: "I ___ go to the gym on Mondays."',opts:['usually go','go usually','goes usually','usually goes'],a:0,exp:'"usually" fe\'ldan oldin. I + go.'},
  {type:'transform',q:'"I play tennis." → U (He) haqida ayting',hint:'He/She/It uchun fe\'lga -s/-es',a:['he plays tennis','he plays tennis.'],exp:'He plays tennis.'}
];}
function buildHaveQs(){return[
  {type:'mc',q:'"She ___ a new car."',opts:['have','has','haves','is have'],a:1,exp:'She uchun HAS.'},
  {type:'fill',q:'"They ___ two dogs." (have/has)',a:['have'],exp:'They bilan HAVE.'},
  {type:'mc',q:'Inkor: "He ___ time."',opts:['don\'t have','hasn\'t have','doesn\'t have','not has'],a:2,exp:'3-shaxs inkor: doesn\'t have.'},
  {type:'mc',q:'"___ there a bank near here?"',opts:['Is','Are','Have','Does'],a:0,exp:'"There is" savolda = Is there.'},
  {type:'fill',q:'"There ___ many students in the class."',a:['are'],exp:'Ko\'plik uchun There ARE.'},
  {type:'mc',q:'"___ you have a pen?"',opts:['Does','Is','Do','Have'],a:2,exp:'You bilan savol DO.'},
  {type:'mc',q:'Qaysi gap to\'g\'ri?',opts:['There are a book.','There is some books.','There are some books.','There have books.'],a:2,exp:'Ko\'plik (books) + There are.'},
  {type:'fill',q:'"Do you have ___ questions?" (savolda)',a:['any'],exp:'Savol va inkorda ANY.'},
  {type:'mc',q:'"She has long hair." — inkor',opts:['She doesn\'t has long hair.','She don\'t have long hair.','She doesn\'t have long hair.','She hasn\'t long hair.'],a:2,exp:'doesn\'t + have (has emas!).'},
  {type:'transform',q:'"There is a cat." → Ko\'plikka o\'tkazing (cats)',hint:'Ko\'plik: There are',a:['there are cats','there are some cats'],exp:'There are cats.'}
];}
function buildDemQs(){return[
  {type:'mc',q:'"___ is my phone." — qo\'lingizdagi narsa',opts:['That','Those','This','These'],a:2,exp:'Yaqin, bitta: THIS.'},
  {type:'fill',q:'"___ are my keys." (qo\'lingizdagi, ko\'p)',a:['These','these'],exp:'Yaqin, ko\'p: THESE.'},
  {type:'mc',q:'Uzoqdagi bitta kitob:',opts:['This is a book.','These is a book.','That is a book.','Those is a book.'],a:2,exp:'Uzoq, bitta: THAT.'},
  {type:'mc',q:'"___ apple" yoki "___ apple"?',opts:['a apple','an apple','the apple','one apple'],a:1,exp:'Unli tovush (a) dan oldin AN.'},
  {type:'fill',q:'"She is ___ engineer." (artikl)',a:['an'],exp:'"Engineer" unli tovush bilan boshlanadi → AN.'},
  {type:'mc',q:'"I saw a dog. ___ dog was brown." — 2-gapda',opts:['A','An','The','This'],a:2,exp:'Allaqachon aytilgan = THE.'},
  {type:'mc',q:'Uzoqdagi ko\'p kitob:',opts:['This','These','That','Those'],a:3,exp:'Uzoq, ko\'p: THOSE.'},
  {type:'fill',q:'"___ are his shoes." (u narida, ko\'p)',a:['Those','those'],exp:'Uzoq, ko\'p: THOSE.'},
  {type:'mc',q:'Qaysi gapda artikl xato?',opts:['I have a car.','She is an actress.','He is the doctor.','I like the music.'],a:3,exp:'"I like the music" xato — umumiy: I like music.'},
  {type:'transform',q:'"This is my book." → Ko\'plikka',hint:'This → These, is → are',a:['these are my books'],exp:'These are my books.'}
];}
function buildPContQs(){return[
  {type:'mc',q:'"She ___ dinner now."',opts:['cook','is cooking','cooks','was cooking'],a:1,exp:'Hozir: is + cooking.'},
  {type:'fill',q:'"They ___ football right now." (play)',a:['are playing'],exp:'They + are + playing.'},
  {type:'mc',q:'"run" + ing = ?',opts:['runing','running','runeing','runnes'],a:1,exp:'Qisqa fe\'l + undosh → ikkilashtir: running.'},
  {type:'mc',q:'Inkor: "I ___ TV." (not watch)',opts:['am not watching','am not watch','is not watching','not watching'],a:0,exp:'I am not watching.'},
  {type:'fill',q:'"make" + ing = ?',a:['making'],exp:'make → e o\'chir → making.'},
  {type:'mc',q:'Qaysi gapda Present Continuous to\'g\'ri?',opts:['I am liking coffee.','She is knowing the answer.','He is running in the park.','They are wanting to leave.'],a:2,exp:'like/know/want Continuous bilan ishlatilmaydi. running ✓'},
  {type:'mc',q:'Savol: "___ you ___ to music?" (hozir)',opts:['Are...listening','Do...listen','Is...listening','Were...listening'],a:0,exp:'Are you listening? ✓'},
  {type:'fill',q:'"He is sit___ on the chair."',a:['sitting'],exp:'sit → sitting (t ikkilashadi).'},
  {type:'mc',q:'"She ___ English every morning." — oddiy harakat',opts:['is studying','studies','study','are studying'],a:1,exp:'"every morning" = Simple Present: studies.'},
  {type:'transform',q:'"I work at home." → Hozir bo\'layotgan shaklda',hint:'am/is/are + verb-ing',a:['i am working at home','i\'m working at home'],exp:'I am working at home.'}
];}
function buildPrepQs(){return[
  {type:'mc',q:'"I wake up ___ 7 AM."',opts:['in','on','at','by'],a:2,exp:'Aniq vaqt → AT.'},
  {type:'fill',q:'"She was born ___ 1999."',a:['in'],exp:'Yil uchun IN.'},
  {type:'mc',q:'"The meeting is ___ Monday."',opts:['in','at','on','for'],a:2,exp:'Kun uchun ON.'},
  {type:'mc',q:'"The book is ___ the table." — ustida',opts:['under','in','on','at'],a:2,exp:'Yuzada → ON.'},
  {type:'fill',q:'"She lives ___ Tashkent."',a:['in'],exp:'Shahar uchun IN.'},
  {type:'mc',q:'"I\'ll meet you ___ the airport."',opts:['in','on','at','by'],a:2,exp:'Aniq joy/nuqta → AT.'},
  {type:'mc',q:'"The cat is ___ the chair." — tagida',opts:['on','in','under','above'],a:2,exp:'Tagida → UNDER.'},
  {type:'fill',q:'"I study English ___ the morning."',a:['in'],exp:'Kun qismlari uchun IN.'},
  {type:'mc',q:'Qaysi gap to\'g\'ri?',opts:['She was born in Monday.','He works at 9 AM on weekdays.','They arrived in midnight.','I go to school on morning.'],a:1,exp:'"at 9 AM" + "on weekdays" ✓'},
  {type:'mc',q:'"The park is ___ the school and the bank."',opts:['next to','between','behind','in front of'],a:1,exp:'Ikki narsa orasida → BETWEEN.'}
];}

/* ══════════════════════════════════════════════
   INIT
══════════════════════════════════════════════ */
function init(){
  loadApp();
  // Apply saved theme
  if(APP.theme === 'light'){
    document.documentElement.dataset.theme = 'light';
    document.getElementById('themeBtn').textContent = '☀️';
  }
  updateStreak();
  buildAlpha();
  buildNums();
  buildColors();
  buildJobQuiz();
  loadVoices(); setTimeout(loadVoices,800); setTimeout(loadVoices,2000);
  drawLetterFrame(0, AD[0]);
  renderLessonRoad();
  refreshUI();
  checkAchievements();
}

window.addEventListener('DOMContentLoaded', init);
</script>
</body>
</html>
