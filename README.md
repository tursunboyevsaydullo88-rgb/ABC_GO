<html lang="uz" data-theme="dark">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Ingliz tilini o'zbek tilida o'rganish platformasi">
<meta name="theme-color" content="#0a0a1a">
<title>LinguaUz — Ingliz Tili Platformasi</title>
<link rel="manifest" href="data:application/json,{}">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Syne:wght@700;800;900&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet">
<style>
/* ============================================================
   LINGUAUZ — DESIGN SYSTEM
   ============================================================ */
:root {
  --bg:       #060610;
  --bg1:      #0d0d20;
  --bg2:      #14142a;
  --bg3:      #1c1c38;
  --surface:  #12122a;
  --border:   rgba(120,100,255,0.15);
  --border2:  rgba(120,100,255,0.28);

  --violet:   #7b5ef8;
  --violet-l: #a98bff;
  --violet-d: #5a3ecc;
  --emerald:  #34d88c;
  --rose:     #f05a7e;
  --amber:    #f5a623;
  --sky:      #38bdf8;
  --indigo:   #818cf8;

  --tx:       #e8e8f4;
  --tx2:      #8888aa;
  --tx3:      #555577;

  --radius:   14px;
  --radius-lg:20px;
  --radius-xl:28px;

  --shadow-sm: 0 2px 12px rgba(0,0,0,.4);
  --shadow:    0 8px 32px rgba(0,0,0,.5);
  --shadow-lg: 0 20px 60px rgba(0,0,0,.6);

  --glow-v:   0 0 40px rgba(123,94,248,.25);
  --glow-e:   0 0 40px rgba(52,216,140,.2);

  --font-head: 'Syne', sans-serif;
  --font-body: 'Space Grotesk', sans-serif;
  --font-mono: 'JetBrains Mono', monospace;

  --nav-h: 64px;
  --sidebar-w: 240px;

  --trans: all .2s cubic-bezier(.4,0,.2,1);
  --trans-spring: all .4s cubic-bezier(.34,1.56,.64,1);
}

[data-theme="light"] {
  --bg:       #f5f5fc;
  --bg1:      #ffffff;
  --bg2:      #f0f0fa;
  --bg3:      #e8e8f5;
  --surface:  #ffffff;
  --border:   rgba(120,100,255,0.2);
  --border2:  rgba(120,100,255,0.4);
  --tx:       #1a1a2e;
  --tx2:      #5a5a7a;
  --tx3:      #9090aa;
  --shadow-sm: 0 2px 12px rgba(0,0,0,.08);
  --shadow:    0 8px 32px rgba(0,0,0,.12);
  --shadow-lg: 0 20px 60px rgba(0,0,0,.15);
  --glow-v:   0 0 40px rgba(123,94,248,.12);
}

*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  font-family: var(--font-body);
  background: var(--bg);
  color: var(--tx);
  line-height: 1.6;
  overflow-x: hidden;
  transition: background .3s, color .3s;
}

/* ── SCROLLBAR ── */
::-webkit-scrollbar { width: 5px; height: 5px; }
::-webkit-scrollbar-track { background: var(--bg1); }
::-webkit-scrollbar-thumb { background: var(--violet-d); border-radius: 99px; }

/* ── SELECTION ── */
::selection { background: rgba(123,94,248,.35); color: #fff; }

/* ── TYPOGRAPHY ── */
h1,h2,h3,h4,h5 { font-family: var(--font-head); line-height: 1.15; }
.mono { font-family: var(--font-mono); }

/* ── BUTTONS ── */
.btn {
  display: inline-flex; align-items: center; gap: 8px;
  padding: 10px 20px; border-radius: var(--radius);
  font-family: var(--font-body); font-size: 14px; font-weight: 600;
  border: none; cursor: pointer; transition: var(--trans);
  white-space: nowrap; text-decoration: none;
}
.btn-primary {
  background: var(--violet); color: #fff;
  box-shadow: 0 4px 16px rgba(123,94,248,.4);
}
.btn-primary:hover { background: var(--violet-l); transform: translateY(-1px); box-shadow: 0 8px 24px rgba(123,94,248,.5); }
.btn-outline {
  background: transparent; color: var(--violet);
  border: 1.5px solid var(--border2);
}
.btn-outline:hover { background: rgba(123,94,248,.1); border-color: var(--violet); }
.btn-ghost { background: transparent; color: var(--tx2); }
.btn-ghost:hover { background: var(--bg2); color: var(--tx); }
.btn-emerald { background: var(--emerald); color: #0a2e1a; box-shadow: 0 4px 16px rgba(52,216,140,.35); }
.btn-emerald:hover { opacity: .88; transform: translateY(-1px); }
.btn-sm { padding: 7px 14px; font-size: 12px; border-radius: 10px; }
.btn-lg { padding: 14px 28px; font-size: 16px; border-radius: var(--radius-lg); }
.btn-icon { padding: 8px; width: 38px; height: 38px; border-radius: 10px; justify-content: center; }

/* ── CARDS ── */
.card {
  background: var(--bg1); border: 1px solid var(--border);
  border-radius: var(--radius-lg); padding: 20px;
  transition: var(--trans);
}
.card:hover { border-color: var(--border2); box-shadow: var(--shadow-sm); }
.card-glass {
  background: rgba(255,255,255,.04); backdrop-filter: blur(12px);
  border: 1px solid rgba(255,255,255,.08);
}

/* ── BADGE ── */
.badge {
  display: inline-flex; align-items: center; gap: 5px;
  padding: 4px 10px; border-radius: 99px;
  font-size: 11px; font-weight: 600; letter-spacing: .5px;
}
.badge-violet { background: rgba(123,94,248,.15); color: var(--violet-l); border: 1px solid rgba(123,94,248,.25); }
.badge-emerald { background: rgba(52,216,140,.12); color: var(--emerald); border: 1px solid rgba(52,216,140,.2); }
.badge-rose { background: rgba(240,90,126,.12); color: var(--rose); border: 1px solid rgba(240,90,126,.2); }
.badge-amber { background: rgba(245,166,35,.12); color: var(--amber); border: 1px solid rgba(245,166,35,.2); }

/* ── PROGRESS BAR ── */
.progress-wrap { height: 6px; background: var(--bg3); border-radius: 99px; overflow: hidden; }
.progress-fill { height: 100%; border-radius: 99px; transition: width .6s cubic-bezier(.34,1.56,.64,1); background: linear-gradient(90deg, var(--violet), var(--emerald)); }

/* ── DIVIDER ── */
.divider { height: 1px; background: var(--border); margin: 20px 0; }

/* ======================================================
   LAYOUT — TOPBAR + SIDEBAR + MAIN
   ====================================================== */

/* TOPBAR */
#topbar {
  position: fixed; top: 0; left: 0; right: 0; height: var(--nav-h);
  background: rgba(6,6,16,.85); backdrop-filter: blur(16px) saturate(1.8);
  border-bottom: 1px solid var(--border);
  display: flex; align-items: center; padding: 0 20px; gap: 16px;
  z-index: 800;
  transition: background .3s;
}
[data-theme="light"] #topbar { background: rgba(245,245,252,.88); }

.topbar-logo {
  font-family: var(--font-head); font-size: 20px; font-weight: 900;
  background: linear-gradient(135deg, var(--violet), var(--emerald));
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  letter-spacing: -1px; white-space: nowrap; flex-shrink: 0;
}

.topbar-stats {
  display: flex; align-items: center; gap: 8px; margin-left: auto;
}
.stat-pill {
  display: flex; align-items: center; gap: 5px;
  background: var(--bg2); border: 1px solid var(--border);
  border-radius: 99px; padding: 5px 12px; font-size: 12px; font-weight: 600;
}
.stat-pill .icon { font-size: 14px; }
.stat-pill .val { color: var(--tx); }

.topbar-right { display: flex; align-items: center; gap: 8px; }

#themeToggle {
  background: var(--bg2); border: 1px solid var(--border);
  color: var(--tx2); border-radius: 10px; padding: 7px 10px;
  cursor: pointer; font-size: 16px; transition: var(--trans);
  line-height: 1;
}
#themeToggle:hover { background: var(--bg3); color: var(--tx); }

.hamburger {
  display: none; flex-direction: column; gap: 5px;
  background: var(--bg2); border: 1px solid var(--border);
  border-radius: 10px; padding: 8px 10px; cursor: pointer;
}
.hamburger span { display: block; width: 20px; height: 2px; background: var(--tx2); border-radius: 2px; transition: var(--trans); }

/* SIDEBAR */
#sidebar {
  position: fixed; top: var(--nav-h); left: 0; bottom: 0;
  width: var(--sidebar-w); background: var(--bg1);
  border-right: 1px solid var(--border);
  display: flex; flex-direction: column; overflow-y: auto;
  z-index: 700; transition: transform .3s cubic-bezier(.4,0,.2,1);
}
#sidebar.collapsed { transform: translateX(-100%); }

.sidebar-nav { padding: 16px 12px; flex: 1; }

.nav-section-label {
  font-size: 9px; letter-spacing: 2px; text-transform: uppercase;
  color: var(--tx3); padding: 8px 12px 4px; font-weight: 700;
}

.nav-item {
  display: flex; align-items: center; gap: 10px;
  padding: 10px 12px; border-radius: 12px;
  font-size: 13px; font-weight: 500; color: var(--tx2);
  cursor: pointer; transition: var(--trans);
  border: none; background: none; width: 100%; text-align: left;
  margin-bottom: 2px;
}
.nav-item:hover { background: var(--bg2); color: var(--tx); }
.nav-item.active { background: rgba(123,94,248,.15); color: var(--violet-l); font-weight: 700; }
.nav-item.active .nav-icon { color: var(--violet); }
.nav-icon { font-size: 18px; flex-shrink: 0; width: 22px; text-align: center; }
.nav-label { flex: 1; }
.nav-badge { background: var(--violet); color: #fff; font-size: 9px; font-weight: 700; padding: 2px 6px; border-radius: 99px; min-width: 18px; text-align: center; }

.sidebar-bottom { padding: 12px; border-top: 1px solid var(--border); }

.user-card {
  display: flex; align-items: center; gap: 10px;
  padding: 10px 12px; background: var(--bg2);
  border: 1px solid var(--border); border-radius: 12px;
  cursor: pointer; transition: var(--trans);
}
.user-card:hover { border-color: var(--border2); }
.user-avatar {
  width: 34px; height: 34px; border-radius: 10px;
  background: linear-gradient(135deg, var(--violet), var(--emerald));
  display: flex; align-items: center; justify-content: center;
  font-size: 16px; flex-shrink: 0;
}
.user-info { flex: 1; min-width: 0; }
.user-name { font-size: 13px; font-weight: 700; truncate: ellipsis; white-space: nowrap; overflow: hidden; }
.user-level { font-size: 10px; color: var(--violet-l); font-weight: 600; }

/* MAIN CONTENT */
#main {
  margin-left: var(--sidebar-w);
  margin-top: var(--nav-h);
  padding: 28px 28px 80px;
  min-height: calc(100vh - var(--nav-h));
  transition: margin-left .3s;
}
#main.full { margin-left: 0; }
#main.content-max { max-width: calc(960px + var(--sidebar-w)); }

/* ── SECTION SYSTEM ── */
.page { display: none; animation: pageIn .3s ease; }
.page.active { display: block; }
@keyframes pageIn { from { opacity:0; transform: translateY(16px); } to { opacity:1; transform: translateY(0); } }

/* ======================================================
   LANDING / DASHBOARD PAGE
   ====================================================== */

.landing-hero {
  text-align: center; padding: 48px 20px 40px;
  position: relative; overflow: hidden;
}
.landing-hero::before {
  content: ''; position: absolute; top: -100px; left: 50%; transform: translateX(-50%);
  width: 800px; height: 500px;
  background: radial-gradient(ellipse, rgba(123,94,248,.18) 0%, transparent 65%);
  pointer-events: none;
}
.hero-badge {
  display: inline-flex; align-items: center; gap: 6px;
  background: rgba(123,94,248,.1); border: 1px solid rgba(123,94,248,.3);
  color: var(--violet-l); font-size: 11px; font-weight: 700;
  letter-spacing: 2px; text-transform: uppercase;
  padding: 6px 16px; border-radius: 99px; margin-bottom: 20px;
}
.hero-badge::before { content: '✦'; color: var(--violet); }

.hero-title {
  font-size: clamp(32px, 6vw, 64px); font-weight: 900;
  line-height: 1.05; margin-bottom: 16px;
  letter-spacing: -2px;
}
.hero-title .accent { color: var(--violet); }
.hero-title .accent2 { color: var(--emerald); }

.hero-sub { font-size: 16px; color: var(--tx2); max-width: 480px; margin: 0 auto 28px; }

.hero-cta { display: flex; gap: 12px; justify-content: center; flex-wrap: wrap; margin-bottom: 40px; }

.stats-row {
  display: flex; justify-content: center; gap: 40px;
  flex-wrap: wrap; padding: 20px 0;
}
.stat-item { text-align: center; }
.stat-num { font-family: var(--font-head); font-size: 28px; font-weight: 900; color: var(--violet-l); }
.stat-lbl { font-size: 12px; color: var(--tx2); margin-top: 2px; }

/* ── DASHBOARD GRID ── */
.dash-grid { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 16px; margin-bottom: 24px; }
.dash-grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 24px; }

.metric-card {
  background: var(--bg1); border: 1px solid var(--border);
  border-radius: var(--radius-lg); padding: 18px 20px;
  position: relative; overflow: hidden; transition: var(--trans);
}
.metric-card:hover { border-color: var(--border2); box-shadow: var(--shadow-sm); }
.metric-card::after {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px;
  border-radius: var(--radius-lg) var(--radius-lg) 0 0;
}
.metric-card.violet::after { background: linear-gradient(90deg, var(--violet), var(--indigo)); }
.metric-card.emerald::after { background: linear-gradient(90deg, var(--emerald), var(--sky)); }
.metric-card.rose::after { background: linear-gradient(90deg, var(--rose), var(--amber)); }
.metric-card.amber::after { background: linear-gradient(90deg, var(--amber), var(--rose)); }

.metric-icon { font-size: 28px; margin-bottom: 8px; }
.metric-val { font-family: var(--font-head); font-size: 32px; font-weight: 900; line-height: 1; margin-bottom: 4px; }
.metric-label { font-size: 12px; color: var(--tx2); font-weight: 500; }
.metric-change { font-size: 11px; color: var(--emerald); margin-top: 6px; font-weight: 600; }

/* ── SECTION TITLE ── */
.section-head {
  display: flex; align-items: center; justify-content: space-between;
  margin-bottom: 16px;
}
.section-title {
  font-family: var(--font-head); font-size: 18px; font-weight: 800;
  letter-spacing: -0.5px;
}
.section-title span { color: var(--violet-l); }

/* ── COURSE CARDS ── */
.course-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(200px,1fr)); gap: 14px; margin-bottom: 24px; }
.course-card {
  background: var(--bg1); border: 1.5px solid var(--border);
  border-radius: var(--radius-lg); padding: 18px; cursor: pointer;
  transition: var(--trans); position: relative; overflow: hidden;
  text-align: center;
}
.course-card:hover { border-color: var(--border2); transform: translateY(-3px); box-shadow: var(--shadow); }
.course-card .cc-icon { font-size: 32px; margin-bottom: 10px; }
.course-card .cc-title { font-family: var(--font-head); font-size: 13px; font-weight: 700; margin-bottom: 4px; }
.course-card .cc-sub { font-size: 11px; color: var(--tx2); margin-bottom: 10px; }
.course-card .cc-prog { }

.course-card.locked { opacity: .55; filter: grayscale(.5); }
.course-card.locked:hover { transform: none; }
.course-card.active-course { border-color: rgba(123,94,248,.5); background: rgba(123,94,248,.06); }
.course-card.active-course::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px;
  background: linear-gradient(90deg, var(--violet), var(--emerald));
}

/* ── STREAK CARD ── */
.streak-display {
  display: flex; align-items: center; gap: 16px;
  background: linear-gradient(135deg, rgba(245,166,35,.1), rgba(240,90,126,.08));
  border: 1px solid rgba(245,166,35,.2); border-radius: var(--radius-lg); padding: 20px;
  margin-bottom: 24px;
}
.streak-fire { font-size: 48px; animation: fireWobble 1.5s ease-in-out infinite; }
@keyframes fireWobble { 0%,100%{transform:rotate(-5deg) scale(1)} 50%{transform:rotate(5deg) scale(1.08)} }
.streak-num { font-family: var(--font-head); font-size: 42px; font-weight: 900; color: var(--amber); line-height: 1; }
.streak-lbl { font-size: 13px; color: var(--tx2); margin-top: 2px; }
.streak-calendar { display: flex; gap: 6px; flex-wrap: wrap; }
.streak-day { width: 30px; height: 30px; border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 10px; font-weight: 700; }
.streak-day.done { background: var(--amber); color: #2a1a00; }
.streak-day.today { background: rgba(245,166,35,.2); border: 1.5px solid var(--amber); color: var(--amber); }
.streak-day.miss { background: var(--bg2); color: var(--tx3); }

/* ── ACHIEVEMENTS ── */
.achievement-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(160px,1fr)); gap: 10px; }
.achievement {
  background: var(--bg2); border: 1px solid var(--border);
  border-radius: 14px; padding: 14px; text-align: center;
  transition: var(--trans); cursor: default;
}
.achievement:hover { border-color: var(--border2); }
.achievement.earned { border-color: rgba(245,166,35,.3); background: rgba(245,166,35,.05); }
.achievement-icon { font-size: 28px; margin-bottom: 6px; filter: grayscale(1); }
.achievement.earned .achievement-icon { filter: none; }
.achievement-title { font-size: 11px; font-weight: 700; margin-bottom: 3px; }
.achievement-desc { font-size: 10px; color: var(--tx2); }

/* ── DAILY CHALLENGE ── */
.daily-card {
  background: linear-gradient(135deg, rgba(56,189,248,.08), rgba(123,94,248,.08));
  border: 1px solid rgba(56,189,248,.2); border-radius: var(--radius-xl); padding: 24px;
  margin-bottom: 24px; position: relative; overflow: hidden;
}
.daily-card::before {
  content: ''; position: absolute; top: -40px; right: -40px;
  width: 180px; height: 180px;
  background: radial-gradient(ellipse, rgba(56,189,248,.12), transparent 70%);
}
.daily-label { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: var(--sky); font-weight: 700; margin-bottom: 8px; }
.daily-q { font-family: var(--font-head); font-size: 20px; font-weight: 800; margin-bottom: 16px; }
.daily-opts { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; }
.daily-opt {
  background: var(--bg1); border: 1.5px solid var(--border);
  border-radius: 12px; padding: 12px 16px; cursor: pointer;
  font-size: 14px; font-weight: 500; transition: var(--trans); text-align: center;
}
.daily-opt:hover:not(.done) { border-color: var(--violet); background: rgba(123,94,248,.06); }
.daily-opt.correct { border-color: var(--emerald); background: rgba(52,216,140,.1); color: var(--emerald); font-weight: 700; }
.daily-opt.wrong { border-color: var(--rose); background: rgba(240,90,126,.1); color: var(--rose); }
.daily-opt.done { cursor: default; }
.daily-reward { display: flex; align-items: center; gap: 8px; margin-top: 14px; padding: 10px 14px; background: rgba(245,166,35,.1); border-radius: 10px; font-size: 13px; font-weight: 600; color: var(--amber); border: 1px solid rgba(245,166,35,.2); }

/* ======================================================
   ALPHABET PAGE (S1)
   ====================================================== */

.alphabet-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(82px,1fr)); gap: 10px; }
.alpha-card {
  background: var(--bg1); border: 1.5px solid var(--border);
  border-radius: 14px; padding: 14px 8px 10px; text-align: center;
  cursor: pointer; transition: var(--trans-spring); user-select: none;
}
.alpha-card:hover { transform: translateY(-4px) scale(1.04); box-shadow: var(--glow-v); border-color: var(--border2); }
.alpha-card:active { transform: scale(.96); }
.alpha-letter { font-family: var(--font-head); font-size: 28px; font-weight: 900; line-height: 1; margin-bottom: 4px; }
.alpha-phone { font-size: 10px; color: var(--tx2); margin-bottom: 3px; }
.alpha-hint { font-size: 9px; color: var(--violet-l); font-weight: 600; letter-spacing: .5px; }

/* ── COLLAPSIBLE CARDS ── */
.collapse-card { background: var(--bg1); border: 1px solid var(--border); border-radius: var(--radius-lg); margin-bottom: 12px; overflow: hidden; }
.collapse-header { display: flex; align-items: center; gap: 12px; padding: 16px 20px; cursor: pointer; transition: background .15s; }
.collapse-header:hover { background: var(--bg2); }
.ch-icon { width: 40px; height: 40px; border-radius: 11px; display: flex; align-items: center; justify-content: center; font-size: 18px; flex-shrink: 0; }
.ch-body { flex: 1; }
.ch-title { font-family: var(--font-head); font-size: 14px; font-weight: 700; margin-bottom: 2px; }
.ch-sub { font-size: 12px; color: var(--tx2); }
.ch-arrow { color: var(--tx3); font-size: 14px; transition: transform .3s; }
.collapse-card.open .ch-arrow { transform: rotate(180deg); }
.collapse-body { display: none; padding: 0 20px 20px; }
.collapse-card.open .collapse-body { display: block; }

/* ── DATA TABLE ── */
.data-table { width: 100%; border-collapse: collapse; font-size: 13px; }
.data-table th {
  text-align: left; padding: 10px 12px;
  font-size: 10px; letter-spacing: 1.5px; text-transform: uppercase;
  color: var(--tx3); border-bottom: 1px solid var(--border); font-weight: 700;
}
.data-table td { padding: 10px 12px; border-bottom: 1px solid rgba(255,255,255,.03); vertical-align: middle; }
[data-theme="light"] .data-table td { border-bottom: 1px solid rgba(0,0,0,.05); }
.data-table tr:last-child td { border-bottom: none; }
.data-table tr:hover td { background: rgba(123,94,248,.04); }
.td-en { font-weight: 600; color: var(--violet-l); font-size: 14px; }
.td-ph { color: var(--indigo); font-style: italic; font-size: 12px; }
.td-uz { color: var(--tx); }

.spk-btn {
  background: rgba(123,94,248,.12); border: 1px solid rgba(123,94,248,.25);
  color: var(--violet-l); font-size: 10px; padding: 3px 8px;
  border-radius: 99px; cursor: pointer; font-family: var(--font-body);
  transition: var(--trans); margin-left: 6px;
}
.spk-btn:hover { background: var(--violet); color: #fff; border-color: var(--violet); }

/* ── DIALOGUE ── */
.dialogue { display: flex; flex-direction: column; gap: 10px; }
.bubble { max-width: 80%; padding: 12px 16px; border-radius: 16px; font-size: 13px; line-height: 1.5; }
.bubble-a { align-self: flex-start; background: var(--bg2); border-bottom-left-radius: 4px; }
.bubble-b { align-self: flex-end; background: rgba(123,94,248,.18); border-bottom-right-radius: 4px; }
.bubble-who { font-size: 9px; letter-spacing: 1px; text-transform: uppercase; color: var(--tx3); margin-bottom: 4px; font-weight: 700; }
.bubble-en { font-weight: 500; }
.bubble-uz { font-size: 11px; color: var(--tx2); margin-top: 3px; }

/* ── NUMBER GRID ── */
.num-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(110px,1fr)); gap: 8px; }
.num-card {
  background: var(--bg2); border: 1px solid var(--border); border-radius: 10px;
  padding: 8px 12px; display: flex; align-items: center; gap: 10px;
  cursor: pointer; transition: var(--trans);
}
.num-card:hover { border-color: var(--amber); background: rgba(245,166,35,.05); }
.num-card .nc-n { font-family: var(--font-head); font-weight: 700; color: var(--amber); font-size: 15px; min-width: 28px; }

/* ── COLOR GRID ── */
.color-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(120px,1fr)); gap: 8px; }
.color-card { border-radius: 12px; padding: 14px; cursor: pointer; transition: transform .2s; }
.color-card:hover { transform: scale(1.06); }

/* ──────────── SECTION LABEL ──────────── */
.section-label {
  font-family: var(--font-head); font-size: 10px; letter-spacing: 2px;
  text-transform: uppercase; color: var(--tx3); margin: 20px 0 10px;
  display: flex; align-items: center; gap: 8px;
}
.section-label::after { content:''; flex:1; height:1px; background: var(--border); }

/* ======================================================
   GRAMMAR QUEST PAGE (S3)
   ====================================================== */

.gram-hero-card {
  background: linear-gradient(135deg, #0d0d2a 0%, #1a0f40 50%, #0a1530 100%);
  border: 1px solid rgba(123,94,248,.3); border-radius: var(--radius-xl);
  padding: 28px; margin-bottom: 20px; position: relative; overflow: hidden;
}
.gram-hero-card::before {
  content: ''; position: absolute; top: -80px; right: -80px;
  width: 320px; height: 320px;
  background: radial-gradient(ellipse, rgba(123,94,248,.18), transparent 70%);
  pointer-events: none;
}
.gram-hero-card::after {
  content: ''; position: absolute; bottom: -40px; left: -40px;
  width: 200px; height: 200px;
  background: radial-gradient(ellipse, rgba(52,216,140,.1), transparent 70%);
  pointer-events: none;
}
.ghc-inner { position: relative; z-index: 1; }
.ghc-top { display: flex; align-items: center; justify-content: space-between; margin-bottom: 12px; flex-wrap: wrap; gap: 10px; }
.ghc-badge {
  display: inline-flex; align-items: center; gap: 6px;
  background: linear-gradient(90deg, rgba(123,94,248,.3), rgba(52,216,140,.2));
  border: 1px solid rgba(123,94,248,.3); color: #fff;
  font-size: 10px; letter-spacing: 2px; text-transform: uppercase;
  padding: 5px 14px; border-radius: 99px; font-weight: 700;
}
.ghc-lb-btn {
  background: rgba(245,166,35,.12); border: 1px solid rgba(245,166,35,.3);
  color: var(--amber); font-size: 12px; padding: 7px 16px;
  border-radius: 99px; cursor: pointer; font-family: var(--font-body);
  font-weight: 600; transition: var(--trans);
}
.ghc-lb-btn:hover { background: rgba(245,166,35,.22); }

.ghc-title { font-family: var(--font-head); font-size: clamp(20px,4vw,32px); font-weight: 900; margin-bottom: 6px; letter-spacing: -1px; }
.ghc-title span { color: var(--violet-l); }
.ghc-sub { font-size: 13px; color: rgba(255,255,255,.6); margin-bottom: 16px; }
.ghc-xp-wrap { height: 8px; background: rgba(255,255,255,.08); border-radius: 99px; overflow: hidden; margin-bottom: 6px; }
.ghc-xp-fill { height: 100%; background: linear-gradient(90deg, var(--violet), var(--emerald)); border-radius: 99px; transition: width .6s cubic-bezier(.34,1.56,.64,1); }
.ghc-xp-label { font-size: 11px; color: rgba(255,255,255,.5); font-weight: 600; }

/* ── LESSON ROAD ── */
.lesson-road { display: flex; flex-direction: column; }
.road-connector { width: 2px; height: 14px; background: linear-gradient(180deg, rgba(123,94,248,.4), rgba(123,94,248,.1)); margin: 0 auto; }

.lesson-node {
  display: flex; align-items: center; gap: 14px;
  background: var(--bg1); border: 1.5px solid var(--border);
  border-radius: var(--radius-lg); padding: 14px 18px;
  cursor: pointer; transition: var(--trans); margin: 0;
}
.lesson-node.unlocked:hover { border-color: rgba(123,94,248,.5); transform: translateX(5px); box-shadow: -4px 0 20px rgba(123,94,248,.15); }
.lesson-node.locked { opacity: .5; cursor: not-allowed; filter: grayscale(.5); }
.lesson-node.completed { border-color: rgba(52,216,140,.3); background: rgba(52,216,140,.03); }
.lesson-node.current { border-color: rgba(123,94,248,.55); background: rgba(123,94,248,.05); animation: nodePulse 2.5s ease-in-out infinite; }
@keyframes nodePulse { 0%,100%{box-shadow:0 0 0 0 rgba(123,94,248,.25)} 50%{box-shadow:0 0 0 8px rgba(123,94,248,0)} }

.ln-icon-wrap { width: 48px; height: 48px; border-radius: 13px; background: var(--bg2); display: flex; align-items: center; justify-content: center; font-size: 22px; flex-shrink: 0; position: relative; }
.ln-lock { position: absolute; bottom: -3px; right: -3px; font-size: 12px; }
.ln-body { flex: 1; min-width: 0; }
.ln-title { font-family: var(--font-head); font-size: 13px; font-weight: 700; margin-bottom: 3px; }
.ln-meta { display: flex; align-items: center; gap: 7px; flex-wrap: wrap; }
.ln-tag { padding: 2px 8px; border-radius: 99px; font-size: 9px; font-weight: 700; letter-spacing: .5px; }
.ln-tag.a1 { background: rgba(52,216,140,.15); color: var(--emerald); }
.ln-tag.a2 { background: rgba(123,94,248,.15); color: var(--violet-l); }
.ln-tag.b1 { background: rgba(240,90,126,.15); color: var(--rose); }
.ln-sub-text { font-size: 11px; color: var(--tx2); }
.ln-score-wrap { text-align: right; flex-shrink: 0; }
.ln-score-num { font-family: var(--font-head); font-size: 17px; font-weight: 900; }
.ln-score-label { font-size: 9px; color: var(--tx3); letter-spacing: .5px; }
.ln-stars { font-size: 13px; }

/* ── LESSON / TEST PANELS ── */
.panel-header {
  display: flex; align-items: center; gap: 12px; margin-bottom: 20px;
  background: var(--bg1); border: 1px solid var(--border);
  border-radius: var(--radius-lg); padding: 14px 18px;
}
.ph-back { background: none; border: 1.5px solid var(--border); color: var(--tx2); font-size: 12px; padding: 6px 14px; border-radius: 10px; cursor: pointer; font-family: var(--font-body); white-space: nowrap; transition: var(--trans); }
.ph-back:hover { border-color: var(--violet); color: var(--violet); }
.ph-title-wrap { display: flex; align-items: center; gap: 10px; flex: 1; min-width: 0; }
.ph-icon { font-size: 24px; flex-shrink: 0; }
.ph-title { font-family: var(--font-head); font-size: 14px; font-weight: 700; }
.ph-sub { font-size: 11px; color: var(--tx2); }
.ph-diff { background: rgba(123,94,248,.15); color: var(--violet-l); font-size: 10px; font-weight: 700; padding: 4px 12px; border-radius: 99px; flex-shrink: 0; }
.ph-score-chip { background: rgba(52,216,140,.12); border: 1px solid rgba(52,216,140,.25); color: var(--emerald); font-family: var(--font-head); font-size: 11px; font-weight: 700; padding: 5px 14px; border-radius: 99px; flex-shrink: 0; }

/* ── LESSON CONTENT ── */
.lc-section { margin-bottom: 22px; }
.lcs-title {
  font-family: var(--font-head); font-size: 10px; letter-spacing: 2px;
  text-transform: uppercase; color: var(--violet-l); margin-bottom: 12px;
  display: flex; align-items: center; gap: 8px;
}
.lcs-title::after { content: ''; flex: 1; height: 1px; background: var(--border); }

.rule-box {
  background: linear-gradient(135deg, rgba(123,94,248,.07), rgba(52,216,140,.04));
  border: 1px solid rgba(123,94,248,.18); border-radius: 14px; padding: 16px 18px; margin-bottom: 12px;
}
.rule-box.warn { background: rgba(245,166,35,.06); border-color: rgba(245,166,35,.22); }
.rule-box.info { background: rgba(56,189,248,.06); border-color: rgba(56,189,248,.2); }
.rule-title { font-weight: 700; font-size: 13px; margin-bottom: 7px; display: flex; align-items: center; gap: 7px; }
.rule-body { font-size: 13px; line-height: 1.8; color: var(--tx2); }

.formula {
  background: rgba(0,0,0,.3); border: 1px solid rgba(123,94,248,.25);
  border-radius: 10px; padding: 10px 16px;
  font-family: var(--font-mono); font-size: 13px; color: var(--violet-l); margin: 8px 0;
}
[data-theme="light"] .formula { background: rgba(123,94,248,.06); }

.examples-grid { display: grid; gap: 8px; }
.ex-card { background: var(--bg2); border-radius: 12px; padding: 12px 14px; border-left: 3px solid var(--violet); }
.ex-card.neg { border-color: var(--rose); }
.ex-card.q { border-color: var(--emerald); }
.ex-en { font-weight: 600; font-size: 13px; color: var(--tx); margin-bottom: 3px; }
.ex-uz { font-size: 11px; color: var(--tx2); }
.ex-note { font-size: 10px; color: var(--amber); margin-top: 3px; font-style: italic; }

.tip-box { background: rgba(245,166,35,.07); border: 1px solid rgba(245,166,35,.18); border-radius: 12px; padding: 12px 16px; font-size: 12px; line-height: 1.7; color: #f0c860; }
.tip-box strong { color: var(--amber); }

.start-test-btn {
  background: linear-gradient(135deg, var(--violet), var(--rose));
  color: #fff; border: none; border-radius: var(--radius-lg);
  padding: 15px 36px; font-family: var(--font-head); font-size: 14px; font-weight: 700;
  cursor: pointer; transition: var(--trans); letter-spacing: .5px;
  box-shadow: 0 8px 24px rgba(123,94,248,.4);
}
.start-test-btn:hover { transform: translateY(-2px); box-shadow: 0 12px 32px rgba(123,94,248,.55); }
.start-test-note { font-size: 12px; color: var(--tx2); margin-bottom: 10px; }

/* ── TEST ── */
.test-progress { height: 4px; background: var(--bg3); border-radius: 99px; overflow: hidden; margin-bottom: 24px; }
.test-prog-fill { height: 100%; background: linear-gradient(90deg, var(--violet), var(--emerald)); border-radius: 99px; transition: width .3s ease; }

.q-block { background: var(--bg1); border: 1px solid var(--border); border-radius: var(--radius-xl); padding: 22px; }
.q-num { font-size: 10px; color: var(--violet-l); letter-spacing: 2px; text-transform: uppercase; margin-bottom: 10px; font-weight: 700; }
.q-text { font-size: 17px; font-weight: 700; margin-bottom: 18px; line-height: 1.5; }
.q-opts { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; margin-bottom: 12px; }
.q-opt {
  background: var(--bg2); border: 1.5px solid var(--border);
  border-radius: 12px; padding: 12px 14px; cursor: pointer; font-size: 13px;
  text-align: center; transition: var(--trans); font-family: var(--font-body);
}
.q-opt:hover:not(.done) { border-color: var(--violet); background: rgba(123,94,248,.08); }
.q-opt.correct { border-color: var(--emerald); background: rgba(52,216,140,.1); color: var(--emerald); font-weight: 700; }
.q-opt.wrong { border-color: var(--rose); background: rgba(240,90,126,.1); color: var(--rose); }
.q-opt.done { cursor: default; }
.q-explain { background: rgba(52,216,140,.06); border: 1px solid rgba(52,216,140,.18); border-radius: 10px; padding: 10px 14px; font-size: 12px; color: #8ef0c0; margin-top: 10px; display: none; }
.q-next-btn { background: linear-gradient(135deg, var(--violet), var(--indigo)); color: #fff; border: none; border-radius: 12px; padding: 12px 28px; font-family: var(--font-head); font-size: 12px; font-weight: 700; cursor: pointer; display: none; transition: var(--trans); margin-top: 10px; letter-spacing: .5px; }
.q-next-btn:hover { opacity: .88; transform: translateY(-1px); }
.q-fill-input { width: 100%; background: var(--bg2); border: 1.5px solid var(--border); border-radius: 12px; padding: 12px 16px; color: var(--tx); font-size: 14px; font-family: var(--font-body); transition: var(--trans); outline: none; }
.q-fill-input:focus { border-color: var(--violet); }
.q-fill-input.correct { border-color: var(--emerald); background: rgba(52,216,140,.07); }
.q-fill-input.wrong { border-color: var(--rose); background: rgba(240,90,126,.07); }
.q-submit-btn { background: var(--violet); color: #fff; border: none; border-radius: 10px; padding: 10px 20px; font-family: var(--font-body); font-size: 13px; font-weight: 600; cursor: pointer; margin-top: 8px; transition: var(--trans); }
.q-submit-btn:hover { opacity: .88; }

/* ── RESULT ── */
.result-wrap {
  background: linear-gradient(135deg, #0d0d2a, #1a0f40);
  border: 1px solid rgba(123,94,248,.3); border-radius: var(--radius-xl);
  padding: 36px 28px; text-align: center; max-width: 480px; margin: 20px auto;
}
.result-icon { font-size: 60px; margin-bottom: 10px; animation: popIn .5s cubic-bezier(.34,1.56,.64,1); }
@keyframes popIn { from{transform:scale(0)} to{transform:scale(1)} }
.result-score { font-family: var(--font-head); font-size: 48px; font-weight: 900; margin-bottom: 6px; }
.result-score.pass { color: var(--emerald); }
.result-score.fail { color: var(--rose); }
.result-msg { font-size: 17px; font-weight: 600; color: var(--violet-l); margin-bottom: 8px; }
.result-detail { font-size: 13px; color: var(--tx2); margin-bottom: 20px; line-height: 1.7; }
.unlock-banner { background: linear-gradient(135deg, rgba(52,216,140,.1), rgba(123,94,248,.1)); border: 1px solid rgba(52,216,140,.3); border-radius: 12px; padding: 14px; margin-bottom: 20px; font-family: var(--font-head); font-size: 14px; font-weight: 800; color: var(--emerald); animation: glowPulse 1.5s ease-in-out infinite; }
@keyframes glowPulse { 0%,100%{opacity:.7} 50%{opacity:1} }
.result-btns { display: flex; gap: 8px; justify-content: center; flex-wrap: wrap; }

/* ── LEADERBOARD MODAL ── */
.modal-overlay { display: none; position: fixed; inset: 0; background: rgba(0,0,0,.88); backdrop-filter: blur(12px); z-index: 1000; align-items: center; justify-content: center; padding: 16px; }
.modal-overlay.open { display: flex; }
.modal-box { background: var(--bg1); border: 1px solid rgba(123,94,248,.3); border-radius: var(--radius-xl); padding: 24px 22px; max-width: 420px; width: 100%; max-height: 85vh; overflow-y: auto; animation: modalIn .3s cubic-bezier(.34,1.56,.64,1); }
@keyframes modalIn { from{opacity:0;transform:scale(.88)} to{opacity:1;transform:scale(1)} }
.modal-head { display: flex; align-items: center; justify-content: space-between; margin-bottom: 16px; }
.modal-title { font-family: var(--font-head); font-size: 17px; font-weight: 800; color: var(--amber); }
.modal-close { background: var(--bg2); border: 1px solid var(--border); color: var(--tx2); border-radius: 9px; padding: 5px 12px; cursor: pointer; font-family: var(--font-body); font-size: 12px; transition: var(--trans); }
.modal-close:hover { background: var(--bg3); color: var(--tx); }
.lb-input-row { display: flex; gap: 8px; margin-bottom: 16px; }
.lb-input { flex: 1; background: var(--bg2); border: 1.5px solid var(--border); border-radius: 10px; padding: 9px 14px; color: var(--tx); font-size: 13px; font-family: var(--font-body); outline: none; transition: var(--trans); }
.lb-input:focus { border-color: var(--violet); }
.lb-save-btn { background: var(--violet); color: #fff; border: none; border-radius: 10px; padding: 9px 16px; font-family: var(--font-body); font-size: 13px; font-weight: 600; cursor: pointer; white-space: nowrap; transition: var(--trans); }
.lb-save-btn:hover { opacity: .88; }
.lb-entry { display: flex; align-items: center; gap: 12px; padding: 10px 12px; border-radius: 12px; margin-bottom: 6px; background: var(--bg2); border: 1px solid var(--border); transition: var(--trans); }
.lb-entry.me { border-color: rgba(123,94,248,.4); background: rgba(123,94,248,.07); }
.lb-rank { font-family: var(--font-head); font-size: 15px; font-weight: 900; min-width: 30px; text-align: center; }
.lb-name { flex: 1; font-size: 13px; font-weight: 600; }
.lb-lessons { font-size: 12px; color: var(--tx2); }
.lb-xp { font-family: var(--font-head); font-size: 13px; color: var(--violet-l); font-weight: 700; }
.lb-empty { text-align: center; color: var(--tx2); font-size: 13px; padding: 24px; }

/* ── LETTER MODAL ── */
.letter-modal-overlay { display: none; position: fixed; inset: 0; background: rgba(0,0,0,.9); backdrop-filter: blur(10px); z-index: 999; align-items: center; justify-content: center; padding: 16px; }
.letter-modal-overlay.open { display: flex; }
.letter-modal-box { background: var(--bg1); border: 1px solid rgba(123,94,248,.3); border-radius: var(--radius-xl); padding: 24px 20px; max-width: 380px; width: 100%; text-align: center; animation: modalIn .3s cubic-bezier(.34,1.56,.64,1); }
.canvas-wrap { width: 240px; height: 240px; margin: 0 auto 12px; border-radius: 14px; overflow: hidden; background: #0f0f1e; border: 2px solid var(--border); position: relative; }
#lc { display: block; width: 240px; height: 240px; }
.pbw { width: 100%; height: 4px; background: var(--bg3); border-radius: 4px; margin-bottom: 12px; overflow: hidden; }
.pbi { height: 100%; background: var(--violet); border-radius: 4px; transition: width .05s linear; }
.anim-ctrl { display: flex; gap: 7px; justify-content: center; margin-bottom: 12px; }
.anim-btn { background: var(--bg2); border: 1px solid var(--border); color: var(--tx); border-radius: 8px; padding: 7px 14px; cursor: pointer; font-size: 12px; font-family: var(--font-body); transition: var(--trans); }
.anim-btn:hover { background: var(--violet); border-color: var(--violet); color: #fff; }
.anim-btn.active { background: rgba(52,216,140,.12); border-color: var(--emerald); color: var(--emerald); }
.lm-letter { font-family: var(--font-head); font-size: 22px; font-weight: 900; color: var(--violet-l); margin-bottom: 3px; }
.lm-phone { font-size: 15px; color: var(--indigo); margin-bottom: 3px; }
.lm-examples { font-size: 12px; color: var(--tx2); margin-bottom: 12px; }
.lm-words { display: flex; gap: 6px; justify-content: center; flex-wrap: wrap; margin-bottom: 14px; }
.lm-word { background: var(--bg2); border: 1px solid var(--border); border-radius: 99px; padding: 5px 12px; font-size: 12px; cursor: pointer; transition: var(--trans); }
.lm-word:hover { border-color: var(--violet); color: var(--violet-l); }
.lm-speak-btn { background: var(--violet); color: #fff; border: none; border-radius: 12px; padding: 11px 24px; font-size: 14px; font-weight: 700; cursor: pointer; font-family: var(--font-body); width: 100%; transition: var(--trans); margin-bottom: 8px; }
.lm-speak-btn:hover { opacity: .88; }
.lm-close-btn { background: var(--bg2); border: 1px solid var(--border); color: var(--tx); border-radius: 12px; padding: 9px 22px; cursor: pointer; font-family: var(--font-body); font-size: 13px; width: 100%; transition: var(--trans); }
.lm-close-btn:hover { background: var(--bg3); }

/* ── VOCABULARY GAME ── */
.vocab-game {
  background: var(--bg1); border: 1px solid var(--border);
  border-radius: var(--radius-xl); padding: 24px; text-align: center;
}
.vg-word { font-family: var(--font-head); font-size: 36px; font-weight: 900; color: var(--violet-l); margin: 20px 0; letter-spacing: -1px; }
.vg-opts { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin: 20px 0; }
.vg-opt { background: var(--bg2); border: 1.5px solid var(--border); border-radius: 12px; padding: 14px; cursor: pointer; font-size: 14px; font-weight: 500; transition: var(--trans); }
.vg-opt:hover:not(.done) { border-color: var(--violet); background: rgba(123,94,248,.08); }
.vg-opt.correct { border-color: var(--emerald); background: rgba(52,216,140,.12); color: var(--emerald); font-weight: 700; }
.vg-opt.wrong { border-color: var(--rose); background: rgba(240,90,126,.1); color: var(--rose); }
.vg-opt.done { cursor: default; }
.vg-score-bar { display: flex; align-items: center; justify-content: space-between; margin-bottom: 16px; }
.vg-timer { font-family: var(--font-head); font-size: 24px; font-weight: 900; }
.vg-timer.urgent { color: var(--rose); animation: pulse .5s ease-in-out infinite; }
@keyframes pulse { 0%,100%{transform:scale(1)} 50%{transform:scale(1.08)} }
.vg-pts { font-family: var(--font-head); font-size: 20px; font-weight: 900; color: var(--amber); }

/* ── GRAMMAR QUIZ COMPONENT ── */
.mini-quiz { background: var(--bg2); border-radius: 14px; padding: 18px; margin-top: 14px; }
.mq-label { font-family: var(--font-head); font-size: 10px; color: var(--violet-l); margin-bottom: 10px; letter-spacing: 1px; }
.mq-q { font-size: 16px; font-weight: 700; margin-bottom: 14px; }
.mq-opts { display: grid; grid-template-columns: 1fr 1fr; gap: 7px; margin-bottom: 12px; }
.mq-opt { background: var(--bg1); border: 1.5px solid var(--border); border-radius: 10px; padding: 10px 12px; cursor: pointer; font-size: 13px; transition: var(--trans); text-align: center; }
.mq-opt:hover { border-color: var(--violet); }
.mq-opt.ok { border-color: var(--emerald); background: rgba(52,216,140,.1); color: var(--emerald); }
.mq-opt.no { border-color: var(--rose); background: rgba(240,90,126,.1); color: var(--rose); }
.mq-next { background: var(--violet); color: #fff; border: none; border-radius: 9px; padding: 10px 20px; font-family: var(--font-body); font-size: 13px; font-weight: 600; cursor: pointer; display: none; transition: var(--trans); }
.mq-next:hover { opacity: .88; }
.mq-score { font-size: 12px; color: var(--tx2); margin-top: 6px; }

/* ── CONVERSATION PAGE ── */
.conv-scenarios { display: grid; grid-template-columns: repeat(auto-fill, minmax(180px,1fr)); gap: 12px; margin-bottom: 24px; }
.scenario-card { background: var(--bg1); border: 1.5px solid var(--border); border-radius: var(--radius-lg); padding: 16px; cursor: pointer; transition: var(--trans); text-align: center; }
.scenario-card:hover { border-color: var(--border2); transform: translateY(-3px); box-shadow: var(--shadow-sm); }
.scenario-icon { font-size: 28px; margin-bottom: 8px; }
.scenario-title { font-family: var(--font-head); font-size: 13px; font-weight: 700; margin-bottom: 3px; }
.scenario-sub { font-size: 11px; color: var(--tx2); }

/* ======================================================
   RESPONSIVE
   ====================================================== */

@media (max-width: 900px) {
  :root { --sidebar-w: 0px; }
  #sidebar { transform: translateX(-100%); width: 260px; }
  #sidebar.open { transform: translateX(0); box-shadow: var(--shadow-lg); }
  #main { margin-left: 0; }
  .hamburger { display: flex; }
  .topbar-stats { display: none; }
  .dash-grid { grid-template-columns: 1fr 1fr; }
}

@media (max-width: 600px) {
  #main { padding: 16px 14px 80px; }
  .dash-grid { grid-template-columns: 1fr 1fr; }
  .dash-grid-2 { grid-template-columns: 1fr; }
  .q-opts { grid-template-columns: 1fr; }
  .mq-opts { grid-template-columns: 1fr; }
  .daily-opts { grid-template-columns: 1fr; }
  .hero-title { letter-spacing: -1px; }
  .result-btns { flex-direction: column; align-items: center; }
  .stat-pill { padding: 4px 8px; font-size: 11px; }
  .streak-display { flex-wrap: wrap; }
}

@media (min-width: 901px) {
  .hamburger { display: none !important; }
}

/* ── OVERLAY FOR MOBILE SIDEBAR ── */
#sidebarOverlay { display: none; position: fixed; inset: 0; background: rgba(0,0,0,.6); z-index: 699; }
#sidebarOverlay.show { display: block; }

/* ── ANIMATIONS ── */
.fade-in { animation: fadeIn .4s ease both; }
@keyframes fadeIn { from{opacity:0;transform:translateY(8px)} to{opacity:1;transform:translateY(0)} }

.stagger > * { opacity: 0; animation: fadeIn .4s ease both; }
.stagger > *:nth-child(1) { animation-delay: .05s; }
.stagger > *:nth-child(2) { animation-delay: .1s; }
.stagger > *:nth-child(3) { animation-delay: .15s; }
.stagger > *:nth-child(4) { animation-delay: .2s; }
.stagger > *:nth-child(5) { animation-delay: .25s; }
.stagger > *:nth-child(6) { animation-delay: .3s; }

/* ── TOAST NOTIFICATION ── */
#toast-container { position: fixed; bottom: 24px; right: 24px; z-index: 2000; display: flex; flex-direction: column; gap: 8px; pointer-events: none; }
.toast { background: var(--bg1); border: 1px solid var(--border2); border-radius: 12px; padding: 12px 18px; font-size: 13px; font-weight: 600; display: flex; align-items: center; gap: 10px; box-shadow: var(--shadow); animation: toastIn .3s cubic-bezier(.34,1.56,.64,1); min-width: 220px; max-width: 320px; }
@keyframes toastIn { from{opacity:0;transform:translateX(40px)} to{opacity:1;transform:translateX(0)} }
.toast.out { animation: toastOut .3s ease forwards; }
@keyframes toastOut { to{opacity:0;transform:translateX(40px)} }
.toast.success { border-color: rgba(52,216,140,.3); }
.toast.error { border-color: rgba(240,90,126,.3); }
.toast.info { border-color: rgba(123,94,248,.3); }

/* ── EXTRA VISUAL ── */
.glow-dot { width: 6px; height: 6px; border-radius: 99px; background: var(--emerald); box-shadow: 0 0 8px var(--emerald); animation: blink 1.5s ease-in-out infinite; }
@keyframes blink { 0%,100%{opacity:1} 50%{opacity:.3} }

.grammar-info-box { background: var(--bg2); border-left: 3px solid var(--violet); border-radius: 0 10px 10px 0; padding: 12px 16px; margin: 8px 0; font-size: 13px; line-height: 1.8; }
.grammar-info-box.green { border-color: var(--emerald); }
.grammar-info-box.orange { border-color: var(--amber); }
.grammar-info-box.red { border-color: var(--rose); }

.vocab-pill { display: inline-flex; align-items: center; gap: 5px; background: var(--bg2); border: 1px solid var(--border); border-radius: 99px; padding: 4px 12px; font-size: 12px; cursor: pointer; transition: var(--trans); margin: 3px; }
.vocab-pill:hover { border-color: var(--violet); color: var(--violet-l); }

/* END STYLES */
</style>
</head>
<body>

<!-- ============================================================
     TOPBAR
     ============================================================ -->
<nav id="topbar">
  <button class="hamburger" id="hamburger" onclick="toggleSidebar()" aria-label="Menu">
    <span></span><span></span><span></span>
  </button>
  <div class="topbar-logo">Lingua<span style="color:var(--emerald)">Uz</span></div>

  <div class="topbar-stats">
    <div class="stat-pill"><span class="icon">🔥</span><span class="val" id="topStreak">0</span></div>
    <div class="stat-pill"><span class="icon">⚡</span><span class="val" id="topXP">0 XP</span></div>
    <div class="stat-pill"><span class="icon">🏆</span><span class="val" id="topLevel">A1</span></div>
  </div>

  <div class="topbar-right">
    <button id="themeToggle" onclick="toggleTheme()" title="Rangni o'zgartirish">🌙</button>
    <button class="btn btn-primary btn-sm" onclick="openLB()">🏆 Reyting</button>
  </div>
</nav>

<!-- Sidebar overlay (mobile) -->
<div id="sidebarOverlay" onclick="closeSidebar()"></div>

<!-- ============================================================
     SIDEBAR
     ============================================================ -->
<aside id="sidebar">
  <nav class="sidebar-nav">
    <div class="nav-section-label">Asosiy</div>
    <button class="nav-item active" onclick="navTo('dashboard')" id="nav-dashboard">
      <span class="nav-icon">🏠</span>
      <span class="nav-label">Bosh sahifa</span>
    </button>
    <button class="nav-item" onclick="navTo('progress')" id="nav-progress">
      <span class="nav-icon">📊</span>
      <span class="nav-label">Mening progressim</span>
    </button>

    <div class="nav-section-label" style="margin-top:12px">Darslar</div>
    <button class="nav-item" onclick="navTo('alphabet')" id="nav-alphabet">
      <span class="nav-icon">🔤</span>
      <span class="nav-label">Alifbo & Salomlashish</span>
    </button>
    <button class="nav-item" onclick="navTo('vocabulary')" id="nav-vocabulary">
      <span class="nav-icon">📚</span>
      <span class="nav-label">So'z boyligi</span>
    </button>
    <button class="nav-item" onclick="navTo('grammar')" id="nav-grammar">
      <span class="nav-icon">🎮</span>
      <span class="nav-label">Grammatika Quest</span>
      <span class="nav-badge" id="navGramBadge"></span>
    </button>
    <button class="nav-item" onclick="navTo('advanced')" id="nav-advanced">
      <span class="nav-icon">🚀</span>
      <span class="nav-label">Ilg'or daraja</span>
    </button>
    <button class="nav-item" onclick="navTo('conversation')" id="nav-conversation">
      <span class="nav-icon">💬</span>
      <span class="nav-label">Suhbat</span>
    </button>

    <div class="nav-section-label" style="margin-top:12px">O'yinlar</div>
    <button class="nav-item" onclick="navTo('vocabgame')" id="nav-vocabgame">
      <span class="nav-icon">⚡</span>
      <span class="nav-label">So'z O'yini</span>
    </button>

    <div class="nav-section-label" style="margin-top:12px">Reyting</div>
    <button class="nav-item" onclick="openLB()">
      <span class="nav-icon">🏆</span>
      <span class="nav-label">Global Reyting</span>
    </button>
  </nav>

  <div class="sidebar-bottom">
    <div class="user-card" onclick="openLB()">
      <div class="user-avatar">🦊</div>
      <div class="user-info">
        <div class="user-name" id="sidebarUserName">Mehmon</div>
        <div class="user-level" id="sidebarUserLevel">⚡ 0 XP · A1 daraja</div>
      </div>
    </div>
  </div>
</aside>

<!-- ============================================================
     MAIN CONTENT
     ============================================================ -->
<main id="main">

  <!-- ========== DASHBOARD PAGE ========== -->
  <div class="page active" id="page-dashboard">

    <!-- Hero -->
    <div class="landing-hero fade-in">
      <div class="hero-badge">✦ O'zbek tilida ingliz tili</div>
      <h1 class="hero-title">
        Ingliz tilini <span class="accent">o'rganing</span><br>
        <span class="accent2">qiziqarli</span> usulda
      </h1>
      <p class="hero-sub">7 ta grammatika dars · So'z o'yinlari · Kunlik vazifalar · Global reyting</p>
      <div class="hero-cta">
        <button class="btn btn-primary btn-lg" onclick="navTo('grammar')">🎮 Grammar Quest</button>
        <button class="btn btn-outline btn-lg" onclick="navTo('vocabgame')">⚡ So'z O'yini</button>
      </div>
      <div class="stats-row">
        <div class="stat-item"><div class="stat-num">7</div><div class="stat-lbl">Grammatika darsi</div></div>
        <div class="stat-item"><div class="stat-num">26</div><div class="stat-lbl">Alifbo harflari</div></div>
        <div class="stat-item"><div class="stat-num">100+</div><div class="stat-lbl">Test savollari</div></div>
        <div class="stat-item"><div class="stat-num">∞</div><div class="stat-lbl">So'z o'yinlari</div></div>
      </div>
    </div>

    <!-- Streak -->
    <div class="streak-display fade-in">
      <div class="streak-fire">🔥</div>
      <div>
        <div class="streak-num" id="dashStreak">0</div>
        <div class="streak-lbl">kunlik streak</div>
      </div>
      <div style="flex:1"></div>
      <div>
        <div style="font-size:11px;color:var(--tx2);margin-bottom:6px;font-weight:600">Bu hafta:</div>
        <div class="streak-calendar" id="streakCalendar"></div>
      </div>
    </div>

    <!-- Metrics -->
    <div class="dash-grid stagger">
      <div class="metric-card violet">
        <div class="metric-icon">⚡</div>
        <div class="metric-val" id="dashXP">0</div>
        <div class="metric-label">Jami XP</div>
        <div class="metric-change" id="dashLevel">A1 daraja</div>
      </div>
      <div class="metric-card emerald">
        <div class="metric-icon">✅</div>
        <div class="metric-val" id="dashLessons">0/7</div>
        <div class="metric-label">Darslar yakunlandi</div>
        <div class="metric-change">75+ ball kerak</div>
      </div>
      <div class="metric-card rose">
        <div class="metric-icon">🎯</div>
        <div class="metric-val" id="dashAccuracy">—</div>
        <div class="metric-label">O'rtacha ball</div>
        <div class="metric-change">Testlar bo'yicha</div>
      </div>
    </div>

    <!-- Daily Challenge -->
    <div class="section-head">
      <div class="section-title">⚡ <span>Kunlik vazifa</span></div>
      <span class="badge badge-amber">+50 XP</span>
    </div>
    <div class="daily-card" id="dailyCard">
      <div class="daily-label">📅 Bugungi savol</div>
      <div class="daily-q" id="dailyQ">Yuklanmoqda...</div>
      <div class="daily-opts" id="dailyOpts"></div>
      <div class="daily-reward" id="dailyReward" style="display:none">🎉 Ajoyib! +50 XP oldiniz!</div>
    </div>

    <!-- Quick access -->
    <div class="section-head" style="margin-top:8px">
      <div class="section-title">📖 <span>Darslar</span></div>
    </div>
    <div class="course-grid stagger">
      <div class="course-card active-course" onclick="navTo('alphabet')">
        <div class="cc-icon">🔤</div>
        <div class="cc-title">Alifbo</div>
        <div class="cc-sub">26 harf · Animatsiya</div>
        <span class="badge badge-emerald">A1</span>
      </div>
      <div class="course-card" onclick="navTo('vocabulary')">
        <div class="cc-icon">📚</div>
        <div class="cc-title">So'z boyligi</div>
        <div class="cc-sub">Sonlar · Ranglar · Kasblar</div>
        <span class="badge badge-emerald">A1</span>
      </div>
      <div class="course-card" onclick="navTo('grammar')">
        <div class="cc-icon">🎮</div>
        <div class="cc-title">Grammar Quest</div>
        <div class="cc-sub">7 bosqich · Unlock tizimi</div>
        <span class="badge badge-violet">A1-B1</span>
      </div>
      <div class="course-card" onclick="navTo('advanced')">
        <div class="cc-icon">🚀</div>
        <div class="cc-title">Ilg'or daraja</div>
        <div class="cc-sub">Past · Kelajak · Modal</div>
        <span class="badge badge-rose">B1</span>
      </div>
      <div class="course-card" onclick="navTo('conversation')">
        <div class="cc-icon">💬</div>
        <div class="cc-title">Suhbat</div>
        <div class="cc-sub">Do'kon · Restoran</div>
        <span class="badge badge-amber">A2</span>
      </div>
      <div class="course-card" onclick="navTo('vocabgame')">
        <div class="cc-icon">⚡</div>
        <div class="cc-title">So'z O'yini</div>
        <div class="cc-sub">Tezkor savol-javob</div>
        <span class="badge badge-violet">O'yin</span>
      </div>
    </div>

    <!-- Achievements -->
    <div class="section-head">
      <div class="section-title">🏅 <span>Yutuqlar</span></div>
    </div>
    <div class="achievement-grid stagger" id="achievementGrid"></div>
  </div><!-- /dashboard -->

  <!-- ========== PROGRESS PAGE ========== -->
  <div class="page" id="page-progress">
    <div class="section-head">
      <div class="section-title">📊 Mening <span>progressim</span></div>
    </div>
    <div class="dash-grid stagger">
      <div class="metric-card violet">
        <div class="metric-icon">⚡</div>
        <div class="metric-val" id="progXP">0</div>
        <div class="metric-label">Jami XP</div>
        <div class="metric-change" id="progLevel">A1 daraja</div>
      </div>
      <div class="metric-card emerald">
        <div class="metric-icon">🔥</div>
        <div class="metric-val" id="progStreak">0</div>
        <div class="metric-label">Kunlik streak</div>
      </div>
      <div class="metric-card amber">
        <div class="metric-icon">✅</div>
        <div class="metric-val" id="progDone">0</div>
        <div class="metric-label">Darslar o'tildi</div>
      </div>
    </div>
    <div class="section-head">
      <div class="section-title">📈 <span>Dars natijalari</span></div>
    </div>
    <div id="progressLessons" class="stagger"></div>
    <div class="section-head" style="margin-top:20px">
      <div class="section-title">🏅 <span>Barcha yutuqlar</span></div>
    </div>
    <div class="achievement-grid stagger" id="allAchievements"></div>
  </div><!-- /progress -->

  <!-- ========== ALPHABET PAGE ========== -->
  <div class="page" id="page-alphabet">
    <div class="section-head">
      <div class="section-title">🔤 Ingliz <span>Alifbosi</span></div>
      <span class="badge badge-emerald">A1</span>
    </div>
    <div class="alphabet-grid stagger" id="alphabetGrid"></div>

    <div class="section-label" style="margin-top:24px">Salomlashish iboralari</div>
    <div class="collapse-card open">
      <div class="collapse-header" onclick="toggleCollapse(this)">
        <div class="ch-icon" style="background:rgba(240,90,126,.12)">👋</div>
        <div class="ch-body"><div class="ch-title">Salomlashish</div><div class="ch-sub">Birinchi iboralar</div></div>
        <span class="ch-arrow">▾</span>
      </div>
      <div class="collapse-body">
        <table class="data-table">
          <tr><th>Inglizcha</th><th>Talaffuz</th><th>O'zbekcha</th></tr>
          <tr><td class="td-en">Hello <button class="spk-btn" onclick="sp('Hello')">🔊</button></td><td class="td-ph">[heˈloʊ]</td><td class="td-uz">Salom</td></tr>
          <tr><td class="td-en">Hi <button class="spk-btn" onclick="sp('Hi')">🔊</button></td><td class="td-ph">[haɪ]</td><td class="td-uz">Salom (norasmiy)</td></tr>
          <tr><td class="td-en">Good morning <button class="spk-btn" onclick="sp('Good morning')">🔊</button></td><td class="td-ph">[gʊd ˈmɔːrnɪŋ]</td><td class="td-uz">Xayrli tong</td></tr>
          <tr><td class="td-en">Good afternoon <button class="spk-btn" onclick="sp('Good afternoon')">🔊</button></td><td class="td-ph">[gʊd ˌæftərˈnuːn]</td><td class="td-uz">Xayrli kun</td></tr>
          <tr><td class="td-en">Good evening <button class="spk-btn" onclick="sp('Good evening')">🔊</button></td><td class="td-ph">[gʊd ˈiːvnɪŋ]</td><td class="td-uz">Xayrli kech</td></tr>
          <tr><td class="td-en">Goodbye <button class="spk-btn" onclick="sp('Goodbye')">🔊</button></td><td class="td-ph">[ˌgʊdˈbaɪ]</td><td class="td-uz">Xayr</td></tr>
          <tr><td class="td-en">How are you? <button class="spk-btn" onclick="sp('How are you?')">🔊</button></td><td class="td-ph">[haʊ ɑːr juː]</td><td class="td-uz">Qandaysiz?</td></tr>
          <tr><td class="td-en">I'm fine, thank you <button class="spk-btn" onclick="sp(&quot;I'm fine, thank you&quot;)">🔊</button></td><td class="td-ph">[aɪm faɪn θæŋk juː]</td><td class="td-uz">Yaxshi, rahmat</td></tr>
          <tr><td class="td-en">Nice to meet you <button class="spk-btn" onclick="sp('Nice to meet you')">🔊</button></td><td class="td-ph">[naɪs tə miːt juː]</td><td class="td-uz">Tanishganimdan xursandman</td></tr>
          <tr><td class="td-en">See you later <button class="spk-btn" onclick="sp('See you later')">🔊</button></td><td class="td-ph">[siː juː ˈleɪtər]</td><td class="td-uz">Ko'rishguncha</td></tr>
        </table>
      </div>
    </div>
    <div class="collapse-card">
      <div class="collapse-header" onclick="toggleCollapse(this)">
        <div class="ch-icon" style="background:rgba(52,216,140,.12)">🙋</div>
        <div class="ch-body"><div class="ch-title">O'zingni tanishtirish</div><div class="ch-sub">My name is... I am from...</div></div>
        <span class="ch-arrow">▾</span>
      </div>
      <div class="collapse-body">
        <table class="data-table">
          <tr><th>Inglizcha</th><th>O'zbekcha</th></tr>
          <tr><td class="td-en">My name is Ali. <button class="spk-btn" onclick="sp('My name is Ali.')">🔊</button></td><td class="td-uz">Mening ismim Ali.</td></tr>
          <tr><td class="td-en">I am from Uzbekistan. <button class="spk-btn" onclick="sp('I am from Uzbekistan.')">🔊</button></td><td class="td-uz">Men O'zbekistondan.</td></tr>
          <tr><td class="td-en">I am 20 years old. <button class="spk-btn" onclick="sp('I am 20 years old.')">🔊</button></td><td class="td-uz">Men 20 yoshdaman.</td></tr>
          <tr><td class="td-en">I am a student. <button class="spk-btn" onclick="sp('I am a student.')">🔊</button></td><td class="td-uz">Men talabaman.</td></tr>
          <tr><td class="td-en">I live in Tashkent. <button class="spk-btn" onclick="sp('I live in Tashkent.')">🔊</button></td><td class="td-uz">Men Toshkentda yashayman.</td></tr>
          <tr><td class="td-en">What is your name? <button class="spk-btn" onclick="sp('What is your name?')">🔊</button></td><td class="td-uz">Ismingiz nima?</td></tr>
          <tr><td class="td-en">Where are you from? <button class="spk-btn" onclick="sp('Where are you from?')">🔊</button></td><td class="td-uz">Qayerdansiz?</td></tr>
        </table>
        <div class="section-label" style="margin-top:16px">Namuna suhbat</div>
        <div class="dialogue">
          <div class="bubble bubble-a"><div class="bubble-who">A</div><div class="bubble-en">Hello! My name is Sarah. What is your name?</div><div class="bubble-uz">Salom! Mening ismim Sarah. Ismingiz nima?</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">B</div><div class="bubble-en">Hi! My name is Ali. Nice to meet you!</div><div class="bubble-uz">Salom! Mening ismim Ali. Tanishganimdan xursandman!</div></div>
          <div class="bubble bubble-a"><div class="bubble-who">A</div><div class="bubble-en">Where are you from?</div><div class="bubble-uz">Qayerdansiz?</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">B</div><div class="bubble-en">I am from Uzbekistan. And you?</div><div class="bubble-uz">Men O'zbekistondan. Siz-chi?</div></div>
        </div>
      </div>
    </div>
  </div><!-- /alphabet -->

  <!-- ========== VOCABULARY PAGE ========== -->
  <div class="page" id="page-vocabulary">
    <div class="section-head">
      <div class="section-title">📚 <span>So'z boyligi</span></div>
      <span class="badge badge-emerald">A1</span>
    </div>
    <!-- Numbers -->
    <div class="collapse-card open">
      <div class="collapse-header" onclick="toggleCollapse(this)">
        <div class="ch-icon" style="background:rgba(245,166,35,.12)">🔢</div>
        <div class="ch-body"><div class="ch-title">Sonlar (1–100)</div><div class="ch-sub">Bosing va eshiting</div></div>
        <span class="ch-arrow">▾</span>
      </div>
      <div class="collapse-body">
        <div class="section-label">1–20</div>
        <div class="num-grid" id="numGrid1"></div>
        <div class="section-label">O'nlar</div>
        <div class="num-grid" id="numGrid2"></div>
      </div>
    </div>
    <!-- Colors -->
    <div class="collapse-card">
      <div class="collapse-header" onclick="toggleCollapse(this)">
        <div class="ch-icon" style="background:rgba(240,90,126,.12)">🎨</div>
        <div class="ch-body"><div class="ch-title">Ranglar (Colors)</div><div class="ch-sub">Bosing va eshiting</div></div>
        <span class="ch-arrow">▾</span>
      </div>
      <div class="collapse-body"><div class="color-grid" id="colorGrid"></div></div>
    </div>
    <!-- Days & Months -->
    <div class="collapse-card">
      <div class="collapse-header" onclick="toggleCollapse(this)">
        <div class="ch-icon" style="background:rgba(123,94,248,.12)">📅</div>
        <div class="ch-body"><div class="ch-title">Hafta kunlari &amp; Oylar</div><div class="ch-sub">Days &amp; Months</div></div>
        <span class="ch-arrow">▾</span>
      </div>
      <div class="collapse-body">
        <div class="section-label">Hafta kunlari</div>
        <table class="data-table">
          <tr><th>Inglizcha</th><th>Talaffuz</th><th>O'zbekcha</th></tr>
          <tr><td class="td-en">Monday <button class="spk-btn" onclick="sp('Monday')">🔊</button></td><td class="td-ph">[ˈmʌndeɪ]</td><td class="td-uz">Dushanba</td></tr>
          <tr><td class="td-en">Tuesday <button class="spk-btn" onclick="sp('Tuesday')">🔊</button></td><td class="td-ph">[ˈtjuːzdeɪ]</td><td class="td-uz">Seshanba</td></tr>
          <tr><td class="td-en">Wednesday <button class="spk-btn" onclick="sp('Wednesday')">🔊</button></td><td class="td-ph">[ˈwenzdeɪ]</td><td class="td-uz">Chorshanba</td></tr>
          <tr><td class="td-en">Thursday <button class="spk-btn" onclick="sp('Thursday')">🔊</button></td><td class="td-ph">[ˈθɜːrzdeɪ]</td><td class="td-uz">Payshanba</td></tr>
          <tr><td class="td-en">Friday <button class="spk-btn" onclick="sp('Friday')">🔊</button></td><td class="td-ph">[ˈfraɪdeɪ]</td><td class="td-uz">Juma</td></tr>
          <tr><td class="td-en">Saturday <button class="spk-btn" onclick="sp('Saturday')">🔊</button></td><td class="td-ph">[ˈsætərdeɪ]</td><td class="td-uz">Shanba</td></tr>
          <tr><td class="td-en">Sunday <button class="spk-btn" onclick="sp('Sunday')">🔊</button></td><td class="td-ph">[ˈsʌndeɪ]</td><td class="td-uz">Yakshanba</td></tr>
        </table>
        <div class="section-label">Oylar</div>
        <table class="data-table">
          <tr><th>Inglizcha</th><th>O'zbek</th><th>Inglizcha</th><th>O'zbek</th></tr>
          <tr><td class="td-en">January</td><td class="td-uz">Yanvar</td><td class="td-en">July</td><td class="td-uz">Iyul</td></tr>
          <tr><td class="td-en">February</td><td class="td-uz">Fevral</td><td class="td-en">August</td><td class="td-uz">Avgust</td></tr>
          <tr><td class="td-en">March</td><td class="td-uz">Mart</td><td class="td-en">September</td><td class="td-uz">Sentyabr</td></tr>
          <tr><td class="td-en">April</td><td class="td-uz">Aprel</td><td class="td-en">October</td><td class="td-uz">Oktyabr</td></tr>
          <tr><td class="td-en">May</td><td class="td-uz">May</td><td class="td-en">November</td><td class="td-uz">Noyabr</td></tr>
          <tr><td class="td-en">June</td><td class="td-uz">Iyun</td><td class="td-en">December</td><td class="td-uz">Dekabr</td></tr>
        </table>
      </div>
    </div>
    <!-- Family -->
    <div class="collapse-card">
      <div class="collapse-header" onclick="toggleCollapse(this)">
        <div class="ch-icon" style="background:rgba(52,216,140,.12)">👨‍👩‍👧‍👦</div>
        <div class="ch-body"><div class="ch-title">Oila a'zolari</div><div class="ch-sub">Family members</div></div>
        <span class="ch-arrow">▾</span>
      </div>
      <div class="collapse-body">
        <table class="data-table">
          <tr><th>Inglizcha</th><th>Talaffuz</th><th>O'zbekcha</th></tr>
          <tr><td class="td-en">Mother / Mom <button class="spk-btn" onclick="sp('Mother')">🔊</button></td><td class="td-ph">[ˈmʌðər]</td><td class="td-uz">Ona</td></tr>
          <tr><td class="td-en">Father / Dad <button class="spk-btn" onclick="sp('Father')">🔊</button></td><td class="td-ph">[ˈfɑːðər]</td><td class="td-uz">Ota</td></tr>
          <tr><td class="td-en">Brother <button class="spk-btn" onclick="sp('Brother')">🔊</button></td><td class="td-ph">[ˈbrʌðər]</td><td class="td-uz">Aka / Uka</td></tr>
          <tr><td class="td-en">Sister <button class="spk-btn" onclick="sp('Sister')">🔊</button></td><td class="td-ph">[ˈsɪstər]</td><td class="td-uz">Opa / Singil</td></tr>
          <tr><td class="td-en">Son <button class="spk-btn" onclick="sp('Son')">🔊</button></td><td class="td-ph">[sʌn]</td><td class="td-uz">O'g'il</td></tr>
          <tr><td class="td-en">Daughter <button class="spk-btn" onclick="sp('Daughter')">🔊</button></td><td class="td-ph">[ˈdɔːtər]</td><td class="td-uz">Qiz</td></tr>
          <tr><td class="td-en">Grandfather <button class="spk-btn" onclick="sp('Grandfather')">🔊</button></td><td class="td-ph">[ˈɡrændˌfɑːðər]</td><td class="td-uz">Bobo</td></tr>
          <tr><td class="td-en">Grandmother <button class="spk-btn" onclick="sp('Grandmother')">🔊</button></td><td class="td-ph">[ˈɡrændˌmʌðər]</td><td class="td-uz">Buvi</td></tr>
        </table>
      </div>
    </div>
    <!-- Jobs with mini quiz -->
    <div class="collapse-card">
      <div class="collapse-header" onclick="toggleCollapse(this)">
        <div class="ch-icon" style="background:rgba(240,90,126,.12)">💼</div>
        <div class="ch-body"><div class="ch-title">Kasblar (Jobs)</div><div class="ch-sub">Mini test bilan!</div></div>
        <span class="ch-arrow">▾</span>
      </div>
      <div class="collapse-body">
        <table class="data-table">
          <tr><th>Inglizcha</th><th>Talaffuz</th><th>O'zbekcha</th></tr>
          <tr><td class="td-en">Doctor <button class="spk-btn" onclick="sp('Doctor')">🔊</button></td><td class="td-ph">[ˈdɒktər]</td><td class="td-uz">Shifokor</td></tr>
          <tr><td class="td-en">Teacher <button class="spk-btn" onclick="sp('Teacher')">🔊</button></td><td class="td-ph">[ˈtiːtʃər]</td><td class="td-uz">O'qituvchi</td></tr>
          <tr><td class="td-en">Student <button class="spk-btn" onclick="sp('Student')">🔊</button></td><td class="td-ph">[ˈstjuːdənt]</td><td class="td-uz">Talaba</td></tr>
          <tr><td class="td-en">Engineer <button class="spk-btn" onclick="sp('Engineer')">🔊</button></td><td class="td-ph">[ˌendʒɪˈnɪər]</td><td class="td-uz">Muhandis</td></tr>
          <tr><td class="td-en">Lawyer <button class="spk-btn" onclick="sp('Lawyer')">🔊</button></td><td class="td-ph">[ˈlɔːjər]</td><td class="td-uz">Huquqshunos</td></tr>
          <tr><td class="td-en">Driver <button class="spk-btn" onclick="sp('Driver')">🔊</button></td><td class="td-ph">[ˈdraɪvər]</td><td class="td-uz">Haydovchi</td></tr>
          <tr><td class="td-en">Chef <button class="spk-btn" onclick="sp('Chef')">🔊</button></td><td class="td-ph">[ʃef]</td><td class="td-uz">Oshpaz</td></tr>
          <tr><td class="td-en">Programmer <button class="spk-btn" onclick="sp('Programmer')">🔊</button></td><td class="td-ph">[ˈproʊɡræmər]</td><td class="td-uz">Dasturchi</td></tr>
          <tr><td class="td-en">Nurse <button class="spk-btn" onclick="sp('Nurse')">🔊</button></td><td class="td-ph">[nɜːrs]</td><td class="td-uz">Hamshira</td></tr>
        </table>
        <div class="mini-quiz" id="jobQuizWrap">
          <div class="mq-label">🧠 MINI TEST — Kasblar</div>
          <div class="mq-q" id="mqqt">...</div>
          <div class="mq-opts" id="mqqo"></div>
          <button class="mq-next" id="mqqn" onclick="mqNext()">Keyingi ▶</button>
          <div class="mq-score" id="mqqs"></div>
        </div>
      </div>
    </div>
  </div><!-- /vocabulary -->

  <!-- ========== GRAMMAR QUEST PAGE ========== -->
  <div class="page" id="page-grammar">
    <div class="gram-hero-card" id="gramHeroCard">
      <div class="ghc-inner">
        <div class="ghc-top">
          <div class="ghc-badge">🎮 Grammar Quest</div>
          <button class="ghc-lb-btn" onclick="openLB()">🏆 Reyting</button>
        </div>
        <div class="ghc-title">Grammatika <span>bosqichlari</span></div>
        <div class="ghc-sub">Har bir darsni o'rgan → Test topshir → Keyingi darajani oching</div>
        <div class="ghc-xp-wrap"><div class="ghc-xp-fill" id="gramXpFill" style="width:0%"></div></div>
        <div class="ghc-xp-label" id="gramXpLabel">XP: 0 / 700</div>
      </div>
    </div>
    <div id="lessonRoad" class="lesson-road"></div>
    <!-- Lesson panel -->
    <div id="lessonPanel" style="display:none">
      <div class="panel-header">
        <button class="ph-back" onclick="closeLessonPanel()">← Orqaga</button>
        <div class="ph-title-wrap">
          <span class="ph-icon" id="lpIcon">📘</span>
          <div><div class="ph-title" id="lpTitle">Dars</div><div class="ph-sub" id="lpSub"></div></div>
        </div>
        <div class="ph-diff" id="lpDiff">A1</div>
      </div>
      <div id="lpContent"></div>
      <div style="text-align:center;margin:28px 0">
        <div class="start-test-note" id="startTestNote"></div>
        <button class="start-test-btn" onclick="startTest()">✏️ Testni boshlash</button>
      </div>
    </div>
    <!-- Test panel -->
    <div id="testPanel" style="display:none">
      <div class="panel-header">
        <button class="ph-back" onclick="backToLesson()">← Darsga qaytish</button>
        <div class="ph-title-wrap">
          <span class="ph-icon">✏️</span>
          <div><div class="ph-title" id="tpTitle">Test</div><div class="ph-sub" id="tpSub"></div></div>
        </div>
        <div class="ph-score-chip" id="tpChip">0/0</div>
      </div>
      <div class="test-progress"><div class="test-prog-fill" id="tpBar" style="width:0%"></div></div>
      <div id="tpContent"></div>
    </div>
    <!-- Result panel -->
    <div id="resultPanel" style="display:none">
      <div class="result-wrap">
        <div class="result-icon" id="resultIcon">🎉</div>
        <div class="result-score" id="resultScore">85/100</div>
        <div class="result-msg" id="resultMsg">Ajoyib!</div>
        <div class="result-detail" id="resultDetail"></div>
        <div id="unlockBanner" class="unlock-banner" style="display:none">🔓 Yangi dars ochildi!</div>
        <div class="result-btns">
          <button class="btn btn-outline" onclick="retryTest()">🔁 Qayta</button>
          <button class="btn btn-emerald" id="rNextBtn" onclick="goNextLesson()" style="display:none">▶ Keyingi dars</button>
          <button class="btn btn-ghost" onclick="closeLessonPanel()">🏠 Xaritaga</button>
        </div>
      </div>
    </div>
  </div><!-- /grammar -->

  <!-- ========== ADVANCED PAGE ========== -->
  <div class="page" id="page-advanced">
    <div class="section-head">
      <div class="section-title">🚀 <span>Ilg'or daraja</span></div>
      <span class="badge badge-rose">B1</span>
    </div>

    <div class="collapse-card open">
      <div class="collapse-header" onclick="toggleCollapse(this)">
        <div class="ch-icon" style="background:rgba(52,216,140,.12)">⬆️</div>
        <div class="ch-body"><div class="ch-title">Future Simple — Kelasi zamon</div><div class="ch-sub">will bilan kelajak</div></div>
        <span class="ch-arrow">▾</span>
      </div>
      <div class="collapse-body">
        <div class="grammar-info-box green"><strong>Tuzilishi:</strong> Subject + <strong>will</strong> + fe'l — Barcha shaxslar uchun bir xil!</div>
        <table class="data-table">
          <tr><th>Shakl</th><th>Misol</th><th>Tarjima</th></tr>
          <tr><td><span class="badge badge-emerald">✅</span></td><td class="td-en">I will call you tomorrow.</td><td class="td-uz">Ertaga qo'ng'iroq qilaman.</td></tr>
          <tr><td><span class="badge badge-rose">❌</span></td><td class="td-en">She won't come today.</td><td class="td-uz">U bugun kelmaydi.</td></tr>
          <tr><td><span class="badge badge-violet">❓</span></td><td class="td-en">Will you help me?</td><td class="td-uz">Menga yordam berasizmi?</td></tr>
        </table>
        <div class="grammar-info-box orange"><strong>will not = won't</strong> &nbsp;|&nbsp; I will = I'll &nbsp;|&nbsp; She will = She'll</div>
      </div>
    </div>

    <div class="collapse-card">
      <div class="collapse-header" onclick="toggleCollapse(this)">
        <div class="ch-icon" style="background:rgba(240,90,126,.12)">🎯</div>
        <div class="ch-body"><div class="ch-title">Modal Verbs</div><div class="ch-sub">can · should · must</div></div>
        <span class="ch-arrow">▾</span>
      </div>
      <div class="collapse-body">
        <table class="data-table">
          <tr><th>Modal</th><th>Ma'no</th><th>Misol</th><th>Tarjima</th></tr>
          <tr><td class="td-en">can</td><td class="td-uz">imkoniyat</td><td class="td-en">I can swim.</td><td class="td-uz">Men suza olaman.</td></tr>
          <tr><td class="td-en">can't</td><td class="td-uz">imkonsizlik</td><td class="td-en">He can't drive.</td><td class="td-uz">U hayday olmaydi.</td></tr>
          <tr><td class="td-en">should</td><td class="td-uz">maslahat</td><td class="td-en">You should sleep early.</td><td class="td-uz">Erta uxlashingiz kerak.</td></tr>
          <tr><td class="td-en">shouldn't</td><td class="td-uz">kerak emas</td><td class="td-en">You shouldn't smoke.</td><td class="td-uz">Chekmasligingiz kerak.</td></tr>
          <tr><td class="td-en">must</td><td class="td-uz">majburiyat</td><td class="td-en">You must wear a seatbelt.</td><td class="td-uz">Kamar taqish shart.</td></tr>
          <tr><td class="td-en">mustn't</td><td class="td-uz">man etilgan</td><td class="td-en">You mustn't smoke here.</td><td class="td-uz">Bu yerda chekish mumkin emas.</td></tr>
        </table>
      </div>
    </div>

    <div class="collapse-card">
      <div class="collapse-header" onclick="toggleCollapse(this)">
        <div class="ch-icon" style="background:rgba(245,166,35,.12)">📊</div>
        <div class="ch-body"><div class="ch-title">Comparison — Taqqoslash</div><div class="ch-sub">big → bigger → biggest</div></div>
        <span class="ch-arrow">▾</span>
      </div>
      <div class="collapse-body">
        <table class="data-table">
          <tr><th>Asl</th><th>Qiyosiy</th><th>Orttirma</th><th>Tarjima</th></tr>
          <tr><td class="td-en">big</td><td class="td-en">bigger</td><td class="td-en">the biggest</td><td class="td-uz">katta → kattaroq → eng katta</td></tr>
          <tr><td class="td-en">small</td><td class="td-en">smaller</td><td class="td-en">the smallest</td><td class="td-uz">kichik → kichikroq → eng kichik</td></tr>
          <tr><td class="td-en">fast</td><td class="td-en">faster</td><td class="td-en">the fastest</td><td class="td-uz">tez → tezroq → eng tez</td></tr>
          <tr><td class="td-en">good</td><td class="td-en">better</td><td class="td-en">the best</td><td class="td-uz">yaxshi → yaxshiroq → eng yaxshi</td></tr>
          <tr><td class="td-en">bad</td><td class="td-en">worse</td><td class="td-en">the worst</td><td class="td-uz">yomon → yomonroq → eng yomon</td></tr>
          <tr><td class="td-en">beautiful</td><td class="td-en">more beautiful</td><td class="td-en">the most beautiful</td><td class="td-uz">chiroyli → chiroliroq → eng chiroyli</td></tr>
          <tr><td class="td-en">expensive</td><td class="td-en">more expensive</td><td class="td-en">the most expensive</td><td class="td-uz">qimmat → qimmatroq → eng qimmat</td></tr>
        </table>
        <div class="grammar-info-box" style="margin-top:10px">📐 <strong>Qisqa (1 bo'g'in):</strong> + er/est → bigger, biggest</div>
        <div class="grammar-info-box green">📏 <strong>Uzun (2+ bo'g'in):</strong> more/most → more beautiful</div>
        <div class="ex-card" style="margin-top:10px"><div class="ex-en">My car is <strong>faster than</strong> your car.</div><div class="ex-uz">Mening mashinam siznikidan tezroq.</div></div>
        <div class="ex-card" style="margin-top:8px"><div class="ex-en">This is <strong>the best</strong> restaurant in the city.</div><div class="ex-uz">Bu shahardagi eng yaxshi restoran.</div></div>
      </div>
    </div>
  </div><!-- /advanced -->

  <!-- ========== CONVERSATION PAGE ========== -->
  <div class="page" id="page-conversation">
    <div class="section-head">
      <div class="section-title">💬 <span>Suhbat</span></div>
      <span class="badge badge-amber">A2</span>
    </div>
    <div class="conv-scenarios">
      <div class="scenario-card" onclick="toggleCollapse(document.querySelector('#scen1 .collapse-header'))">
        <div class="scenario-icon">🛒</div>
        <div class="scenario-title">Do'konda</div>
        <div class="scenario-sub">Shopping dialogue</div>
      </div>
      <div class="scenario-card" onclick="toggleCollapse(document.querySelector('#scen2 .collapse-header'))">
        <div class="scenario-icon">🍽️</div>
        <div class="scenario-title">Restoranda</div>
        <div class="scenario-sub">Restaurant dialogue</div>
      </div>
      <div class="scenario-card" onclick="toggleCollapse(document.querySelector('#scen3 .collapse-header'))">
        <div class="scenario-icon">✈️</div>
        <div class="scenario-title">Aeroportda</div>
        <div class="scenario-sub">Airport dialogue</div>
      </div>
    </div>

    <div class="collapse-card open" id="scen1">
      <div class="collapse-header" onclick="toggleCollapse(this)">
        <div class="ch-icon" style="background:rgba(245,166,35,.12)">🛒</div>
        <div class="ch-body"><div class="ch-title">Do'konda</div><div class="ch-sub">Shopping suhbati</div></div>
        <span class="ch-arrow">▾</span>
      </div>
      <div class="collapse-body">
        <div class="dialogue">
          <div class="bubble bubble-a"><div class="bubble-who">Sotuvchi</div><div class="bubble-en">Good morning! Can I help you?</div><div class="bubble-uz">Xayrli tong! Sizga yordam bera olamanmi?</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">Xaridor</div><div class="bubble-en">Yes, please. How much is this shirt?</div><div class="bubble-uz">Ha, iltimos. Bu ko'ylak qancha turadi?</div></div>
          <div class="bubble bubble-a"><div class="bubble-who">Sotuvchi</div><div class="bubble-en">It's 25 dollars. Do you want to try it on?</div><div class="bubble-uz">25 dollar. Kiyib ko'rmoqchimisiz?</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">Xaridor</div><div class="bubble-en">Yes, please. Where is the fitting room?</div><div class="bubble-uz">Ha, iltimos. Kiyinish xonasi qayerda?</div></div>
          <div class="bubble bubble-a"><div class="bubble-who">Sotuvchi</div><div class="bubble-en">It's on the left, next to the counter.</div><div class="bubble-uz">Chapda, kassaning yonida.</div></div>
        </div>
        <div class="section-label">Foydali iboralar</div>
        <table class="data-table">
          <tr><th>Inglizcha</th><th>O'zbekcha</th></tr>
          <tr><td class="td-en">How much is it? <button class="spk-btn" onclick="sp('How much is it?')">🔊</button></td><td class="td-uz">Bu qancha turadi?</td></tr>
          <tr><td class="td-en">Can I try it on? <button class="spk-btn" onclick="sp('Can I try it on?')">🔊</button></td><td class="td-uz">Kiyib ko'ra olamanmi?</td></tr>
          <tr><td class="td-en">Do you have a bigger size? <button class="spk-btn" onclick="sp('Do you have a bigger size?')">🔊</button></td><td class="td-uz">Kattaroq o'lcham bormi?</td></tr>
          <tr><td class="td-en">I'll take it. <button class="spk-btn" onclick="sp('I will take it.')">🔊</button></td><td class="td-uz">Olaman.</td></tr>
          <tr><td class="td-en">Can I pay by card? <button class="spk-btn" onclick="sp('Can I pay by card?')">🔊</button></td><td class="td-uz">Kartochka bilan to'lasam bo'ladimi?</td></tr>
        </table>
      </div>
    </div>

    <div class="collapse-card" id="scen2">
      <div class="collapse-header" onclick="toggleCollapse(this)">
        <div class="ch-icon" style="background:rgba(240,90,126,.12)">🍽️</div>
        <div class="ch-body"><div class="ch-title">Restoranda</div><div class="ch-sub">Restaurant suhbati</div></div>
        <span class="ch-arrow">▾</span>
      </div>
      <div class="collapse-body">
        <div class="dialogue">
          <div class="bubble bubble-a"><div class="bubble-who">Ofitsiant</div><div class="bubble-en">Welcome! Do you have a reservation?</div><div class="bubble-uz">Xush kelibsiz! Bronimiz bormi?</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">Mehmon</div><div class="bubble-en">No, we don't. Table for two, please.</div><div class="bubble-uz">Yo'q. Ikki kishilik stol, iltimos.</div></div>
          <div class="bubble bubble-a"><div class="bubble-who">Ofitsiant</div><div class="bubble-en">Of course! Follow me, please. Here is your menu.</div><div class="bubble-uz">Albatta! Meni kuzating, iltimos. Bu sizning menyungiz.</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">Mehmon</div><div class="bubble-en">Thank you. I'd like to order a pizza and a salad.</div><div class="bubble-uz">Rahmat. Men pizza va salat buyurtma qilmoqchiman.</div></div>
          <div class="bubble bubble-a"><div class="bubble-who">Ofitsiant</div><div class="bubble-en">Great choice! And what would you like to drink?</div><div class="bubble-uz">Ajoyib tanlov! Va nima ichmoqchisiz?</div></div>
        </div>
      </div>
    </div>

    <div class="collapse-card" id="scen3">
      <div class="collapse-header" onclick="toggleCollapse(this)">
        <div class="ch-icon" style="background:rgba(56,189,248,.12)">✈️</div>
        <div class="ch-body"><div class="ch-title">Aeroportda</div><div class="ch-sub">Airport suhbati</div></div>
        <span class="ch-arrow">▾</span>
      </div>
      <div class="collapse-body">
        <div class="dialogue">
          <div class="bubble bubble-a"><div class="bubble-who">Xodim</div><div class="bubble-en">Good morning. Your passport and ticket, please.</div><div class="bubble-uz">Xayrli tong. Pasportingiz va chiptan, iltimos.</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">Yo'lovchi</div><div class="bubble-en">Here you are. I have one suitcase to check in.</div><div class="bubble-uz">Mana. Menda topshirish uchun bitta chemodan bor.</div></div>
          <div class="bubble bubble-a"><div class="bubble-who">Xodim</div><div class="bubble-en">Do you have any hand luggage?</div><div class="bubble-uz">Qo'l yugi bormi?</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">Yo'lovchi</div><div class="bubble-en">Yes, just this backpack. Where is gate 12?</div><div class="bubble-uz">Ha, faqat bu ryukzak. 12-eshik qayerda?</div></div>
        </div>
      </div>
    </div>
  </div><!-- /conversation -->

  <!-- ========== VOCAB GAME PAGE ========== -->
  <div class="page" id="page-vocabgame">
    <div class="section-head">
      <div class="section-title">⚡ <span>So'z O'yini</span></div>
      <span class="badge badge-violet">O'yin</span>
    </div>
    <div class="vocab-game" id="vocabGameBox">
      <div class="vg-score-bar">
        <div>
          <div class="vg-pts" id="vgPts">0 pts</div>
          <div style="font-size:11px;color:var(--tx2)">Natija</div>
        </div>
        <div style="text-align:center">
          <div class="vg-timer" id="vgTimer">15</div>
          <div style="font-size:11px;color:var(--tx2)">Soniya</div>
        </div>
        <div style="text-align:right">
          <div style="font-family:var(--font-head);font-size:18px;font-weight:700" id="vgQ">1/10</div>
          <div style="font-size:11px;color:var(--tx2)">Savol</div>
        </div>
      </div>
      <div class="progress-wrap" style="margin-bottom:20px"><div class="progress-fill" id="vgTimerBar" style="width:100%"></div></div>
      <div class="vg-word" id="vgWord">—</div>
      <div style="font-size:12px;color:var(--tx2);margin-bottom:12px">O'zbekcha tarjimasini toping:</div>
      <div class="vg-opts" id="vgOpts"></div>
      <div id="vgResult" style="display:none;text-align:center;padding:24px">
        <div style="font-size:48px;margin-bottom:12px" id="vgEndIcon">🎯</div>
        <div style="font-family:var(--font-head);font-size:32px;font-weight:900;margin-bottom:8px" id="vgEndScore">0</div>
        <div style="font-size:15px;color:var(--tx2);margin-bottom:20px" id="vgEndMsg">Juda yaxshi!</div>
        <button class="btn btn-primary" onclick="startVocabGame()">🔄 Qayta o'ynash</button>
      </div>
    </div>
  </div><!-- /vocabgame -->

</main><!-- /main -->

<!-- ============================================================
     LETTER MODAL
     ============================================================ -->
<div class="letter-modal-overlay" id="letterModal" onclick="if(event.target===this)closeLetterModal()">
  <div class="letter-modal-box">
    <div class="canvas-wrap"><canvas id="lc" width="480" height="480"></canvas></div>
    <div class="pbw"><div class="pbi" id="pb"></div></div>
    <div class="anim-ctrl">
      <button class="anim-btn" id="pbtn" onclick="togAnim()">▶ Ijro</button>
      <button class="anim-btn" onclick="reAnim()">↺ Qayta</button>
    </div>
    <div class="lm-letter" id="mlt">A a</div>
    <div class="lm-phone" id="mpr">[eɪ]</div>
    <div class="lm-examples" id="mex">Apple, Ant, Air</div>
    <div class="lm-words" id="mwr"></div>
    <button class="lm-speak-btn" onclick="spkNow()">🔊 Ovozini eshitish</button>
    <button class="lm-close-btn" onclick="closeLetterModal()">✕ Yopish</button>
  </div>
</div>

<!-- ============================================================
     LEADERBOARD MODAL
     ============================================================ -->
<div class="modal-overlay" id="lbModal" onclick="if(event.target===this)closeLB()">
  <div class="modal-box">
    <div class="modal-head">
      <div class="modal-title">🏆 Global Reyting</div>
      <button class="modal-close" onclick="closeLB()">✕ Yopish</button>
    </div>
    <div style="font-size:12px;color:var(--tx2);margin-bottom:12px">Ismingizni kiriting va natijangizni global reytingga saqlang!</div>
    <div class="lb-input-row">
      <input class="lb-input" id="lbNameIn" placeholder="Ismingizni kiriting..." maxlength="20">
      <button class="lb-save-btn" onclick="saveLBEntry()">Saqlash</button>
    </div>
    <div id="lbList"></div>
  </div>
</div>

<!-- Toast container -->
<div id="toast-container"></div>

<!-- ============================================================
     JAVASCRIPT
     ============================================================ -->
<script>
'use strict';

/* ================================================================
   DATA
   ================================================================ */
var AD=[
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

var N20=[[1,'one'],[2,'two'],[3,'three'],[4,'four'],[5,'five'],[6,'six'],[7,'seven'],[8,'eight'],[9,'nine'],[10,'ten'],[11,'eleven'],[12,'twelve'],[13,'thirteen'],[14,'fourteen'],[15,'fifteen'],[16,'sixteen'],[17,'seventeen'],[18,'eighteen'],[19,'nineteen'],[20,'twenty']];
var N10=[[20,'twenty'],[30,'thirty'],[40,'forty'],[50,'fifty'],[60,'sixty'],[70,'seventy'],[80,'eighty'],[90,'ninety'],[100,'one hundred']];

var CLR=[
  {en:'Red',uz:'Qizil',bg:'#c0392b',fg:'#fff'},
  {en:'Blue',uz:"Ko'k",bg:'#2980b9',fg:'#fff'},
  {en:'Green',uz:'Yashil',bg:'#27ae60',fg:'#fff'},
  {en:'Yellow',uz:'Sariq',bg:'#f1c40f',fg:'#000'},
  {en:'Orange',uz:"To'q sariq",bg:'#e67e22',fg:'#fff'},
  {en:'Purple',uz:'Binafsha',bg:'#8e44ad',fg:'#fff'},
  {en:'Pink',uz:'Pushti',bg:'#e91e8c',fg:'#fff'},
  {en:'Black',uz:'Qora',bg:'#222244',fg:'#eee'},
  {en:'White',uz:"Oq",bg:'#ecf0f1',fg:'#333'},
  {en:'Grey',uz:'Kulrang',bg:'#7f8c8d',fg:'#fff'},
  {en:'Brown',uz:'Jigarrang',bg:'#7d4f2a',fg:'#fff'},
  {en:'Gold',uz:'Oltin',bg:'#d4a017',fg:'#000'}
];

var VOCAB_WORDS=[
  {en:'Apple',uz:'Olma'},{en:'Book',uz:'Kitob'},{en:'Cat',uz:'Mushuk'},{en:'Dog',uz:'It'},
  {en:'Water',uz:'Suv'},{en:'School',uz:'Maktab'},{en:'House',uz:'Uy'},{en:'Car',uz:'Mashina'},
  {en:'Tree',uz:'Daraxt'},{en:'Sun',uz:'Quyosh'},{en:'Moon',uz:'Oy'},{en:'Star',uz:'Yulduz'},
  {en:'Fish',uz:'Baliq'},{en:'Bird',uz:'Qush'},{en:'Food',uz:'Ovqat'},{en:'City',uz:'Shahar'},
  {en:'Road',uz:"Yo'l"},{en:'Friend',uz:"Do'st"},{en:'Time',uz:'Vaqt'},{en:'Work',uz:'Ish'}
];

var JOB_QUIZ=[
  {q:'Who treats sick people?',o:['Teacher','Doctor','Driver','Cook'],a:1},
  {q:'Who drives a car for work?',o:['Nurse','Lawyer','Driver','Engineer'],a:2},
  {q:'Who teaches students?',o:['Teacher','Doctor','Chef','Programmer'],a:0},
  {q:'Who writes code?',o:['Lawyer','Police officer','Chef','Programmer'],a:3},
  {q:'"Hamshira" inglizcha nima?',o:['Doctor','Nurse','Cook','Teacher'],a:1},
  {q:'"Oshpaz" inglizcha nima?',o:['Driver','Engineer','Chef','Lawyer'],a:2}
];

var DAILY_QS=[
  {q:'"I ___ a student." — to\'g\'ri shakl',o:['am','is','are','be'],a:0,exp:'I bilan AM.'},
  {q:'"She ___ coffee every morning." (drink)',o:['drink','drinks','drinking','drank'],a:1,exp:'She/He/It uchun +s: drinks.'},
  {q:'"There ___ two books on the table."',o:['is','are','have','has'],a:1,exp:"Ko'plik uchun There ARE."},
  {q:'"___ you speak English?" — savol',o:['Are','Is','Do','Does'],a:2,exp:'You bilan savol DO.'},
  {q:'"He ___ not happy." — to\'g\'ri shakl',o:['am','are','is','be'],a:2,exp:'He bilan IS.'},
  {q:'"I ___ my keys." (not have)',o:["don't have","doesn't have","not have","haven't"],a:0,exp:"I + don't + have."},
  {q:'"The cat is ___ the table." — ustida',o:['under','in','on','at'],a:2,exp:'Yuzada → ON.'},
  {q:'"They ___ playing football now."',o:['is','am','was','are'],a:3,exp:'They bilan ARE + ing.'}
];

var ACHIEVEMENTS=[
  {id:'first_lesson',icon:'🎓',title:'Birinchi dars',desc:'Birinchi grammatika darsi',xp:50,earned:false},
  {id:'pass_3',icon:'🔥',title:'Trio',desc:'3 ta darsni yakunlash',xp:100,earned:false},
  {id:'perfect',icon:'⭐',title:'Mukammal',desc:'100/100 ball olish',xp:150,earned:false},
  {id:'all_done',icon:'🏆',title:'Grammatika ustasi',desc:'Barcha darslarni yakunlash',xp:300,earned:false},
  {id:'streak3',icon:'🔥',title:'3 kunlik streak',desc:'3 kun ketma-ket kirish',xp:75,earned:false},
  {id:'vocab_master',icon:'⚡',title:"So'z ustasi",desc:"So'z o'yinida 150+ ball",xp:100,earned:false},
  {id:'speed_demon',icon:'⚡',title:'Tezkor',desc:'Testni 2 daqiqada yakunlash',xp:80,earned:false},
  {id:'daily_hero',icon:'📅',title:'Kunlik qahramon',desc:'5 ta kunlik vazifani bajarish',xp:120,earned:false}
];

/* ================================================================
   APP STATE
   ================================================================ */
var APP = {
  theme: 'dark',
  page: 'dashboard',
  streak: 0,
  lastVisit: null,
  dailyDone: false,
  dailyDoneDate: null,
  dailyIdx: 0,
  dailyAnswered: false,
  vocabScore: 0
};

var GS = {
  unlocked:[true,false,false,false,false,false,false],
  scores:[null,null,null,null,null,null,null],
  xp:0,
  achievements:[],
  leaderboardName:''
};

var curLesson=-1, curQ=0, curScore=0, curAnswered=false, curQList=[];
var mqIdx=0, mqScore=0, mqAnswered=false;

/* ================================================================
   LOCAL STORAGE
   ================================================================ */
function saveAll(){
  try{
    localStorage.setItem('luApp', JSON.stringify(APP));
    localStorage.setItem('luGS', JSON.stringify(GS));
  }catch(e){}
}
function loadAll(){
  try{
    var a=localStorage.getItem('luApp');
    if(a){var p=JSON.parse(a);for(var k in p)if(p.hasOwnProperty(k))APP[k]=p[k];}
    var g=localStorage.getItem('luGS');
    if(g){var q=JSON.parse(g);
      GS.unlocked=q.unlocked||GS.unlocked;
      GS.scores=q.scores||GS.scores;
      GS.xp=q.xp||0;
      GS.achievements=q.achievements||[];
      GS.leaderboardName=q.leaderboardName||'';
    }
  }catch(e){}
}

/* ================================================================
   THEME
   ================================================================ */
function toggleTheme(){
  APP.theme = APP.theme==='dark'?'light':'dark';
  document.documentElement.setAttribute('data-theme',APP.theme);
  document.getElementById('themeToggle').textContent = APP.theme==='dark'?'🌙':'☀️';
  saveAll();
}

/* ================================================================
   NAVIGATION
   ================================================================ */
function navTo(page){
  // Hide all pages
  document.querySelectorAll('.page').forEach(function(p){p.classList.remove('active');});
  // Show target
  var el=document.getElementById('page-'+page);
  if(el) el.classList.add('active');
  // Update nav
  document.querySelectorAll('.nav-item').forEach(function(b){b.classList.remove('active');});
  var nb=document.getElementById('nav-'+page);
  if(nb) nb.classList.add('active');
  APP.page=page;
  closeSidebar();
  window.scrollTo({top:0,behavior:'smooth'});
  saveAll();
}

function toggleSidebar(){
  var sb=document.getElementById('sidebar');
  var ov=document.getElementById('sidebarOverlay');
  sb.classList.toggle('open');
  ov.classList.toggle('show');
}
function closeSidebar(){
  document.getElementById('sidebar').classList.remove('open');
  document.getElementById('sidebarOverlay').classList.remove('show');
}

/* ================================================================
   COLLAPSE
   ================================================================ */
function toggleCollapse(header){
  var card=header.closest('.collapse-card');
  card.classList.toggle('open');
}

/* ================================================================
   SPEECH
   ================================================================ */
var synth=window.speechSynthesis;
var voices=[];
function loadVoices(){ voices=synth?synth.getVoices():[];}
if(synth){loadVoices();synth.onvoiceschanged=loadVoices;}
function sp(txt){
  if(!synth)return;
  synth.cancel();
  var u=new SpeechSynthesisUtterance(txt);
  u.lang='en-US';u.rate=0.82;u.pitch=1.05;u.volume=1;
  var v=voices.find(function(v){return v.lang==='en-US'&&v.localService;})||voices.find(function(v){return v.lang.startsWith('en');});
  if(v)u.voice=v;
  synth.speak(u);
}
function spkNow(){if(curD)sp(curD.l);}

/* ================================================================
   CANVAS ANIMATION
   ================================================================ */
var cvs=document.getElementById('lc');
var cx=cvs.getContext('2d');
var W=480,H=480,animT=0,animDur=150,animRaf=null,animOn=false,curD=null;

function drawFrame(t,d){
  cx.clearRect(0,0,W,H);
  cx.fillStyle='#0f0f1e';cx.fillRect(0,0,W,H);
  for(var i=0;i<4;i++){
    var ph=((t/animDur)+i*0.25)%1,r=60+ph*200,al=(1-ph)*0.3;
    cx.beginPath();cx.arc(W/2,H/2,r,0,Math.PI*2);
    cx.strokeStyle=d.c+Math.floor(al*255).toString(16).padStart(2,'0');
    cx.lineWidth=2;cx.stroke();
  }
  for(var j=0;j<8;j++){
    var ang=(j/8)*Math.PI*2+t*0.05,or=160+Math.sin(t*0.07+j)*15;
    cx.beginPath();cx.arc(W/2+Math.cos(ang)*or,H/2+Math.sin(ang)*or,3+Math.sin(t*0.1+j)*1.5,0,Math.PI*2);
    cx.fillStyle=d.c;cx.globalAlpha=0.65;cx.fill();cx.globalAlpha=1;
  }
  var g=cx.createRadialGradient(W/2,H/2,0,W/2,H/2,140);
  g.addColorStop(0,d.c+'44');g.addColorStop(1,'transparent');
  cx.fillStyle=g;cx.fillRect(0,0,W,H);
  var prog=Math.min(t/20,1),ease=1-Math.pow(1-prog,3),sc=(0.2+ease*0.8)*(1+Math.sin(t*0.07)*0.025);
  cx.save();cx.translate(W/2,H/2+10);cx.scale(sc,sc);
  cx.shadowColor=d.c;cx.shadowBlur=25+Math.sin(t*0.05)*8;
  var lg=cx.createLinearGradient(-80,-100,80,100);
  lg.addColorStop(0,'#ffffff');lg.addColorStop(0.5,d.c);lg.addColorStop(1,'#ffffffaa');
  cx.font='900 190px Syne,sans-serif';cx.textAlign='center';cx.textBaseline='middle';
  cx.fillStyle=lg;cx.fillText(d.l,0,0);cx.shadowBlur=0;cx.restore();
  var sp2=Math.min(Math.max(t-10,0)/18,1);
  cx.globalAlpha=sp2;cx.font='500 46px Syne,sans-serif';cx.textAlign='center';
  cx.fillStyle='#ffffff55';cx.fillText(d.l.toLowerCase(),W/2,H/2+118);cx.globalAlpha=1;
  if(t<25){for(var k=0;k<8;k++){var sa=(k/8)*Math.PI*2,sr=t*6;cx.beginPath();cx.arc(W/2+Math.cos(sa)*sr,H/2+Math.sin(sa)*sr,3,0,Math.PI*2);cx.fillStyle=d.c;cx.globalAlpha=(1-t/25)*0.9;cx.fill();cx.globalAlpha=1;}}
  document.getElementById('pb').style.width=Math.min((t/animDur)*100,100)+'%';
}

function animLoop(){
  if(!animOn)return;animT++;drawFrame(animT,curD);
  if(animT<animDur){animRaf=requestAnimationFrame(animLoop);}
  else{animOn=false;var pb=document.getElementById('pbtn');pb.textContent='▶ Ijro';pb.classList.remove('active');}
}
function startAnim(){
  if(animRaf)cancelAnimationFrame(animRaf);
  animT=0;animOn=true;
  var pb=document.getElementById('pbtn');pb.textContent='⏸ To\'xtat';pb.classList.add('active');
  animLoop();setTimeout(function(){sp(curD.l);},350);
}
function togAnim(){
  if(animOn){animOn=false;if(animRaf)cancelAnimationFrame(animRaf);var pb=document.getElementById('pbtn');pb.textContent='▶ Ijro';pb.classList.remove('active');}
  else{if(animT>=animDur)animT=0;animOn=true;var pb=document.getElementById('pbtn');pb.textContent='⏸ To\'xtat';pb.classList.add('active');animLoop();}
}
function reAnim(){startAnim();}

/* ================================================================
   LETTER MODAL
   ================================================================ */
function openLetterModal(d){
  curD=d;
  document.getElementById('mlt').textContent=d.l+' '+d.l.toLowerCase();
  document.getElementById('mpr').textContent=d.p;
  document.getElementById('mex').textContent='Misollar: '+d.ex;
  var wr=document.getElementById('mwr');wr.innerHTML='';
  d.w.forEach(function(word){var pill=document.createElement('div');pill.className='lm-word';pill.textContent=word;pill.onclick=function(){sp(word);};wr.appendChild(pill);});
  document.getElementById('letterModal').classList.add('open');
  document.body.style.overflow='hidden';
  drawFrame(0,d);setTimeout(startAnim,150);
}
function closeLetterModal(){
  document.getElementById('letterModal').classList.remove('open');
  document.body.style.overflow='';
  animOn=false;if(animRaf)cancelAnimationFrame(animRaf);
  if(synth)synth.cancel();
}

/* ================================================================
   BUILD ALPHABET
   ================================================================ */
function buildAlphabet(){
  var g=document.getElementById('alphabetGrid');
  if(!g)return;g.innerHTML='';
  AD.forEach(function(d){
    var c=document.createElement('div');c.className='alpha-card';
    c.style.borderColor=d.c+'55';
    c.innerHTML='<div class="alpha-letter" style="color:'+d.c+'">'+d.l+'</div>'
      +'<div class="alpha-phone">'+d.p+'</div>'
      +'<div class="alpha-hint">▶ bosing</div>';
    c.onclick=function(){openLetterModal(d);};
    g.appendChild(c);
  });
}

/* ================================================================
   BUILD NUMBERS & COLORS
   ================================================================ */
function buildNumbers(){
  var g1=document.getElementById('numGrid1'),g2=document.getElementById('numGrid2');
  if(!g1)return;
  N20.forEach(function(x){var c=document.createElement('div');c.className='num-card';c.innerHTML='<span class="nc-n">'+x[0]+'</span><span>'+x[1]+'</span>';c.onclick=function(){sp(x[1]);};g1.appendChild(c);});
  N10.forEach(function(x){var c=document.createElement('div');c.className='num-card';c.innerHTML='<span class="nc-n">'+x[0]+'</span><span>'+x[1]+'</span>';c.onclick=function(){sp(x[1]);};g2.appendChild(c);});
}
function buildColors(){
  var g=document.getElementById('colorGrid');if(!g)return;
  CLR.forEach(function(c){
    var el=document.createElement('div');el.className='color-card';
    el.style.background=c.bg;
    el.innerHTML='<div style="font-weight:700;color:'+c.fg+';font-size:14px">'+c.en+'</div><div style="font-size:11px;opacity:.75;color:'+c.fg+'">'+c.uz+'</div>';
    el.onclick=function(){sp(c.en);};g.appendChild(el);
  });
}

/* ================================================================
   MINI QUIZ (Jobs)
   ================================================================ */
function buildMiniQuiz(){
  mqIdx=0;mqScore=0;mqAnswered=false;showMQ();
}
function showMQ(){
  mqAnswered=false;
  var q=JOB_QUIZ[mqIdx];
  var qt=document.getElementById('mqqt'),qo=document.getElementById('mqqo');
  if(!qt)return;
  qt.textContent=q.q;
  var nxt=document.getElementById('mqqn');if(nxt)nxt.style.display='none';
  qo.innerHTML='';
  q.o.forEach(function(opt,i){
    var b=document.createElement('div');b.className='mq-opt';b.textContent=opt;
    b.onclick=function(){mqCheck(i,b);};qo.appendChild(b);
  });
  var sc=document.getElementById('mqqs');if(sc)sc.textContent='Savol '+(mqIdx+1)+'/'+JOB_QUIZ.length+' | To\'g\'ri: '+mqScore;
}
function mqCheck(idx,btn){
  if(mqAnswered)return;mqAnswered=true;
  var a=JOB_QUIZ[mqIdx].a;
  document.querySelectorAll('#mqqo .mq-opt')[a].classList.add('ok');
  if(idx!==a)btn.classList.add('no');else mqScore++;
  sp(JOB_QUIZ[mqIdx].o[a]);
  var sc=document.getElementById('mqqs');if(sc)sc.textContent='Savol '+(mqIdx+1)+'/'+JOB_QUIZ.length+' | To\'g\'ri: '+mqScore;
  var nxt=document.getElementById('mqqn');
  if(nxt){if(mqIdx<JOB_QUIZ.length-1)nxt.style.display='inline-block';else if(sc)sc.textContent='Natija: '+mqScore+'/'+JOB_QUIZ.length+' to\'g\'ri!';}
}
function mqNext(){mqIdx++;if(mqIdx<JOB_QUIZ.length)showMQ();}

/* ================================================================
   DAILY CHALLENGE
   ================================================================ */
function initDaily(){
  var today=new Date().toDateString();
  if(APP.dailyDoneDate===today){
    var dr=document.getElementById('dailyReward');
    if(dr){dr.style.display='flex';dr.textContent='✅ Bugungi vazifani bajardingiz!';}
    var qEl=document.getElementById('dailyQ');if(qEl)qEl.textContent='Siz bugun kunlik vazifani bajardingiz!';
    var opts=document.getElementById('dailyOpts');if(opts)opts.innerHTML='';
    return;
  }
  var idx=Math.floor(Math.random()*DAILY_QS.length);
  APP.dailyIdx=idx;APP.dailyAnswered=false;
  var q=DAILY_QS[idx];
  var qEl=document.getElementById('dailyQ');if(qEl)qEl.textContent=q.q;
  var opts=document.getElementById('dailyOpts');if(!opts)return;
  opts.innerHTML='';
  q.o.forEach(function(o,i){
    var b=document.createElement('div');b.className='daily-opt';b.textContent=o;
    b.onclick=function(){checkDaily(i,b,q.a);};opts.appendChild(b);
  });
}
function checkDaily(sel,btn,ans){
  if(APP.dailyAnswered)return;APP.dailyAnswered=true;
  var opts=document.querySelectorAll('.daily-opt');
  opts.forEach(function(o){o.classList.add('done');});
  opts[ans].classList.add('correct');
  if(sel!==ans)btn.classList.add('wrong');
  else{
    GS.xp+=50;
    var today=new Date().toDateString();
    APP.dailyDoneDate=today;
    var dr=document.getElementById('dailyReward');if(dr)dr.style.display='flex';
    showToast('⚡ +50 XP kunlik vazifa uchun!','success');
    updateStrike();updateTopbar();saveAll();
  }
}

/* ================================================================
   STREAK
   ================================================================ */
function updateStrike(){
  var today=new Date().toDateString();
  if(APP.lastVisit===today)return;
  var yesterday=new Date(Date.now()-86400000).toDateString();
  if(APP.lastVisit===yesterday)APP.streak=(APP.streak||0)+1;
  else if(APP.lastVisit!==today)APP.streak=1;
  APP.lastVisit=today;
  if(APP.streak>=3)earnAchievement('streak3');
  saveAll();
}

function buildStreakCalendar(){
  var el=document.getElementById('streakCalendar');if(!el)return;
  var days=['Ya','Du','Se','Ch','Pa','Ju','Sh'];
  var today=new Date();var dow=today.getDay();
  el.innerHTML='';
  for(var i=6;i>=0;i--){
    var d=new Date(today);d.setDate(today.getDate()-i);
    var dDiv=document.createElement('div');
    var dayIdx=(dow-i+7)%7;
    dDiv.className='streak-day '+(i===0?'today':i<=(APP.streak-1)?'done':'miss');
    dDiv.textContent=days[(d.getDay()+6)%7];
    el.appendChild(dDiv);
  }
}

/* ================================================================
   ACHIEVEMENTS
   ================================================================ */
function earnAchievement(id){
  if(GS.achievements.indexOf(id)!==-1)return;
  GS.achievements.push(id);
  var ach=ACHIEVEMENTS.find(function(a){return a.id===id;});
  if(ach){GS.xp+=ach.xp;showToast('🏅 Yangi yutuq: '+ach.title+' (+'+ach.xp+' XP)','info');}
  saveAll();renderAchievements();
}

function renderAchievements(){
  ['achievementGrid','allAchievements'].forEach(function(gid){
    var g=document.getElementById(gid);if(!g)return;
    g.innerHTML='';
    ACHIEVEMENTS.forEach(function(a){
      var earned=GS.achievements.indexOf(a.id)!==-1;
      var div=document.createElement('div');div.className='achievement'+(earned?' earned':'');
      div.innerHTML='<div class="achievement-icon">'+a.icon+'</div>'
        +'<div class="achievement-title">'+a.title+'</div>'
        +'<div class="achievement-desc">'+a.desc+'</div>'
        +(earned?'<div style="font-size:10px;color:var(--amber);margin-top:4px;font-weight:700">+'+a.xp+' XP ✓</div>':'<div style="font-size:10px;color:var(--tx3);margin-top:4px">+'+a.xp+' XP</div>');
      g.appendChild(div);
    });
  });
}

/* ================================================================
   PROGRESS PAGE
   ================================================================ */
function renderProgressPage(){
  var px=document.getElementById('progXP');if(px)px.textContent=GS.xp;
  var pl=document.getElementById('progLevel');if(pl)pl.textContent=getLevel();
  var ps=document.getElementById('progStreak');if(ps)ps.textContent=APP.streak;
  var done=GS.scores.filter(function(s){return s!==null&&s>=75;}).length;
  var pd=document.getElementById('progDone');if(pd)pd.textContent=done;

  var pl2=document.getElementById('progressLessons');if(!pl2)return;
  pl2.innerHTML='';
  LESSONS.forEach(function(l,i){
    var s=GS.scores[i];
    var div=document.createElement('div');
    div.style.cssText='background:var(--bg1);border:1px solid var(--border);border-radius:14px;padding:14px 18px;margin-bottom:10px;display:flex;align-items:center;gap:14px;';
    var color=s===null?'var(--tx3)':(s>=75?'var(--emerald)':'var(--rose)');
    div.innerHTML='<span style="font-size:22px">'+l.icon+'</span>'
      +'<div style="flex:1"><div style="font-family:var(--font-head);font-size:13px;font-weight:700;margin-bottom:4px">'+l.title+'</div>'
      +'<div class="progress-wrap"><div class="progress-fill" style="width:'+(s||0)+'%;background:'+(s>=75?'linear-gradient(90deg,var(--violet),var(--emerald))':'linear-gradient(90deg,var(--rose),var(--amber))')+'"></div></div></div>'
      +'<div style="font-family:var(--font-head);font-size:17px;font-weight:900;color:'+color+'">'+(s===null?'—':s+'/100')+'</div>';
    pl2.appendChild(div);
  });
}

/* ================================================================
   GRAMMAR — LESSON DEFINITIONS
   ================================================================ */
var LESSONS=[
  {id:0,icon:'🔵',title:'To Be: am / is / are',sub:"Ingliz tilining asosiy fe'li",diff:'A1',tag:'a1',xp:100,content:buildToBeLesson,questions:buildToBeQs},
  {id:1,icon:'💚',title:'Olmoshlar (Pronouns)',sub:'I, You, He, She, It, We, They',diff:'A1',tag:'a1',xp:100,content:buildPronounLesson,questions:buildPronounQs},
  {id:2,icon:'⏰',title:'Simple Present Tense',sub:'Hozirgi oddiy zamon',diff:'A1',tag:'a1',xp:100,content:buildSPTLesson,questions:buildSPTQs},
  {id:3,icon:'📦',title:'Have / Has & There is/are',sub:'Egalik va mavjudlik',diff:'A2',tag:'a2',xp:100,content:buildHaveLesson,questions:buildHaveQs},
  {id:4,icon:'👉',title:'This / That / These / Those',sub:"Ko'rsatish olmoshlari + Articles",diff:'A2',tag:'a2',xp:100,content:buildDemLesson,questions:buildDemQs},
  {id:5,icon:'🌀',title:'Present Continuous',sub:'Hozir bo&#x2019;layotgan harakatlar',diff:'A2',tag:'a2',xp:100,content:buildPContLesson,questions:buildPContQs},
  {id:6,icon:'🔮',title:'Prepositions of Time & Place',sub:'in / on / at / under / next to',diff:'B1',tag:'b1',xp:100,content:buildPrepLesson,questions:buildPrepQs}
];

/* ================================================================
   GRAMMAR ENGINE
   ================================================================ */
function loadGS(){
  try{var d=localStorage.getItem('luGS');if(d){var p=JSON.parse(d);GS.unlocked=p.unlocked||GS.unlocked;GS.scores=p.scores||GS.scores;GS.xp=p.xp||0;GS.achievements=p.achievements||[];GS.leaderboardName=p.leaderboardName||'';}}catch(e){}
}
function saveGS(){try{localStorage.setItem('luGS',JSON.stringify(GS));}catch(e){}}

function renderRoad(){
  var road=document.getElementById('lessonRoad');if(!road)return;
  road.innerHTML='';
  LESSONS.forEach(function(l,i){
    if(i>0){var conn=document.createElement('div');conn.className='road-connector';road.appendChild(conn);}
    var node=document.createElement('div');
    var locked=!GS.unlocked[i];
    var comp=GS.scores[i]!==null&&GS.scores[i]>=75;
    node.className='lesson-node '+(locked?'locked':(comp?'completed':'current'));
    var sc=GS.scores[i];
    var stars=sc===null?'&#9675;&#9675;&#9675;':(sc>=90?'&#9733;&#9733;&#9733;':sc>=75?'&#9733;&#9733;&#9675;':'&#9733;&#9675;&#9675;');
    var scDisp=sc===null?(locked?'&#128274;':'-'):(sc+'/100');
    var scColor=sc===null?'var(--tx3)':(sc>=75?'var(--emerald)':'var(--rose)');
    node.innerHTML='<div class="ln-icon-wrap">'+l.icon+(locked?'<div class="ln-lock">&#128274;</div>':'')+'</div>'
      +'<div class="ln-body"><div class="ln-title">'+l.title+'</div>'
      +'<div class="ln-meta"><span class="ln-tag '+l.tag+'">'+l.diff+'</span><span class="ln-sub-text">'+l.sub+'</span></div></div>'
      +'<div class="ln-score-wrap"><div class="ln-score-num" style="color:'+scColor+'">'+scDisp+'</div>'
      +'<div class="ln-score-label">BALL</div><div class="ln-stars">'+stars+'</div></div>';
    if(!locked){(function(idx){node.onclick=function(){openLesson(idx);};})(i);}
    road.appendChild(node);
  });
}

function updateGramXP(){
  var total=LESSONS.length*100;var pct=Math.min((GS.xp/total)*100,100);
  var f=document.getElementById('gramXpFill');if(f)f.style.width=pct+'%';
  var lb=document.getElementById('gramXpLabel');if(lb)lb.textContent='XP: '+GS.xp+' / '+total;
  var nb=document.getElementById('navGramBadge');
  var done=GS.scores.filter(function(s){return s!==null&&s>=75;}).length;
  if(nb)nb.textContent=done?done+'/7':'';
}

function showGramSections(which){
  ['gramHeroCard','lessonRoad','lessonPanel','testPanel','resultPanel'].forEach(function(id){
    var el=document.getElementById(id);if(el)el.style.display='none';
  });
  if(which==='road'){
    var hc=document.getElementById('gramHeroCard');if(hc)hc.style.display='block';
    var lr=document.getElementById('lessonRoad');if(lr)lr.style.display='flex';
  } else {
    var el2=document.getElementById(which);if(el2)el2.style.display='block';
  }
}

function openLesson(idx){
  curLesson=idx;var l=LESSONS[idx];
  var g=function(id){return document.getElementById(id);};
  if(g('lpIcon'))g('lpIcon').textContent=l.icon;
  if(g('lpTitle'))g('lpTitle').textContent=l.title;
  if(g('lpSub'))g('lpSub').textContent=l.sub;
  if(g('lpDiff'))g('lpDiff').textContent=l.diff;
  if(g('lpContent'))g('lpContent').innerHTML=l.content();
  var prev=GS.scores[idx];
  if(g('startTestNote'))g('startTestNote').innerHTML=prev!==null?"So'nggi ball: <strong style='color:"+(prev>=75?'var(--emerald)':'var(--rose)')+"'>"+prev+"/100</strong>":'';
  showGramSections('lessonPanel');
  window.scrollTo({top:0,behavior:'smooth'});
}

function closeLessonPanel(){
  showGramSections('road');
  renderRoad();updateGramXP();renderProgressPage();updateTopbar();
}

function startTest(){
  var l=LESSONS[curLesson];
  curQList=l.questions();curQ=0;curScore=0;curAnswered=false;
  var g=function(id){return document.getElementById(id);};
  if(g('tpTitle'))g('tpTitle').textContent=l.title+' — Test';
  if(g('tpSub'))g('tpSub').textContent='Savollar: '+curQList.length+' | 75+ ball kerak';
  showGramSections('testPanel');
  showQuestion();window.scrollTo({top:0,behavior:'smooth'});
}
function backToLesson(){showGramSections('lessonPanel');}

function updateTestProgress(){
  var pct=(curQ/curQList.length)*100;
  var tb=document.getElementById('tpBar');if(tb)tb.style.width=pct+'%';
  var pts=Math.round((curScore/curQList.length)*100);
  var ch=document.getElementById('tpChip');if(ch)ch.textContent=curQ+'/'+curQList.length+' | '+pts+'%';
}

function showQuestion(){
  if(curQ>=curQList.length){endTest();return;}
  var q=curQList[curQ];curAnswered=false;updateTestProgress();
  var html='<div class="q-block"><div class="q-num">Savol '+(curQ+1)+' / '+curQList.length+'</div>';
  if(q.type==='mc'){
    html+='<div class="q-text">'+q.q+'</div><div class="q-opts" id="qOpts">';
    q.opts.forEach(function(o,i){html+='<div class="q-opt" onclick="checkMC('+i+','+q.a+')">'+o+'</div>';});
    html+='</div>';
  } else if(q.type==='fill'||q.type==='transform'){
    html+='<div class="q-text">'+q.q+'</div>';
    if(q.type==='transform')html+='<div class="rule-box" style="margin-bottom:10px;padding:10px 14px"><em style="font-size:12px;color:var(--tx2)">Hint: </em><span style="font-size:12px;color:var(--violet-l)">'+q.hint+'</span></div>';
    html+='<input class="q-fill-input" id="fillIn" placeholder="Javobingizni yozing..." autocomplete="off"><br><button class="q-submit-btn" onclick="checkFill()">Tekshirish &#10003;</button>';
  }
  html+='<div class="q-explain" id="qExp">'+q.exp+'</div>';
  html+='<button class="q-next-btn" id="qNext" onclick="nextQ()">Keyingi &#8594;</button></div>';
  var tc=document.getElementById('tpContent');if(tc)tc.innerHTML=html;
}

function checkMC(sel,ans){
  if(curAnswered)return;curAnswered=true;
  var opts=document.querySelectorAll('.q-opt');
  opts.forEach(function(o){o.classList.add('done');});
  if(sel===ans){curScore++;opts[ans].classList.add('correct');}
  else{opts[ans].classList.add('correct');opts[sel].classList.add('wrong');}
  var ex=document.getElementById('qExp');if(ex)ex.style.display='block';
  var nx=document.getElementById('qNext');if(nx)nx.style.display='inline-block';
}
function checkFill(){
  if(curAnswered)return;
  var inp=document.getElementById('fillIn');if(!inp)return;
  var val=inp.value.trim().toLowerCase();
  var q=curQList[curQ];
  var correct=Array.isArray(q.a)?q.a.map(function(x){return x.toLowerCase();}):q.a.toLowerCase().split('|');
  var ok=correct.indexOf(val)!==-1;
  inp.classList.add(ok?'correct':'wrong');inp.disabled=true;
  if(ok)curScore++;
  else{var h=document.createElement('div');h.style.cssText='font-size:12px;color:var(--rose);margin-top:6px';h.textContent="To'g'ri javob: "+correct[0];inp.parentNode.insertBefore(h,inp.nextSibling.nextSibling);}
  curAnswered=true;
  var ex=document.getElementById('qExp');if(ex)ex.style.display='block';
  var nx=document.getElementById('qNext');if(nx)nx.style.display='inline-block';
}
function nextQ(){curQ++;showQuestion();window.scrollTo({top:0,behavior:'smooth'});}

function endTest(){
  var pct=Math.round((curScore/curQList.length)*100);
  var pass=pct>=75,was=GS.scores[curLesson];
  var improved=was===null||pct>was;
  if(improved){GS.xp+=(was===null?LESSONS[curLesson].xp:Math.max(0,pct-was));GS.scores[curLesson]=pct;}
  var unlockNext=false;
  if(pass&&curLesson+1<LESSONS.length&&!GS.unlocked[curLesson+1]){GS.unlocked[curLesson+1]=true;unlockNext=true;}
  saveGS();saveAll();

  // Achievements
  if(pct===100)earnAchievement('perfect');
  var done=GS.scores.filter(function(s){return s!==null&&s>=75;}).length;
  if(done>=1)earnAchievement('first_lesson');
  if(done>=3)earnAchievement('pass_3');
  if(done===7)earnAchievement('all_done');

  showGramSections('resultPanel');
  var ri=document.getElementById('resultIcon');if(ri)ri.innerHTML=pct>=90?'&#127775;':pct>=75?'&#127881;':'&#128548;';
  var rs=document.getElementById('resultScore');if(rs){rs.textContent=pct+'/100';rs.className='result-score '+(pass?'pass':'fail');}
  var rm=document.getElementById('resultMsg');if(rm)rm.textContent=pct>=90?'Mukammal! Ajoyib!':pct>=75?"Zo'r! O'tdingiz!":'Hali ozroq mashq kerak...';
  var rd=document.getElementById('resultDetail');
  if(rd)rd.innerHTML="To'g'ri: <strong>"+curScore+'/'+curQList.length+"</strong>"+(pass?' ✅ Keyingi dars ochildi!':" ❌ 75+ ball kerak.");
  var ub=document.getElementById('unlockBanner');if(ub)ub.style.display=unlockNext?'block':'none';
  var nb=document.getElementById('rNextBtn');if(nb)nb.style.display=(pass&&curLesson+1<LESSONS.length)?'inline-block':'none';

  updateGramXP();updateTopbar();updateLBEntry();
  if(pass)showToast('🎉 Test muvaffaqiyatli! +'+LESSONS[curLesson].xp+' XP','success');
  else showToast('❌ 75+ ball kerak. Qayta urinib ko\'ring.','error');
  window.scrollTo({top:0,behavior:'smooth'});
}

function retryTest(){startTest();}
function goNextLesson(){openLesson(curLesson+1);}

/* ================================================================
   TOPBAR UPDATER
   ================================================================ */
function getLevel(){
  if(GS.xp<100)return 'A1 — Boshlang\'ich';
  if(GS.xp<250)return 'A1 — Elementary';
  if(GS.xp<400)return 'A2 — Pre-Intermediate';
  if(GS.xp<550)return 'B1 — Intermediate';
  return 'B1+ — Upper-Int.';
}
function getLevelShort(){
  if(GS.xp<100)return 'A1';if(GS.xp<250)return 'A1';if(GS.xp<400)return 'A2';if(GS.xp<550)return 'B1';return 'B1+';
}
function updateTopbar(){
  var ts=document.getElementById('topStreak');if(ts)ts.textContent=APP.streak||0;
  var tx=document.getElementById('topXP');if(tx)tx.textContent=(GS.xp||0)+' XP';
  var tl=document.getElementById('topLevel');if(tl)tl.textContent=getLevelShort();
  var sun=document.getElementById('sidebarUserName');if(sun)sun.textContent=GS.leaderboardName||'Mehmon';
  var sul=document.getElementById('sidebarUserLevel');if(sul)sul.textContent='⚡ '+GS.xp+' XP · '+getLevelShort()+' daraja';
  var ds=document.getElementById('dashStreak');if(ds)ds.textContent=APP.streak||0;
  var dx=document.getElementById('dashXP');if(dx)dx.textContent=GS.xp||0;
  var dlv=document.getElementById('dashLevel');if(dlv)dlv.textContent=getLevelShort()+' daraja';
  var done=GS.scores.filter(function(s){return s!==null&&s>=75;}).length;
  var dl=document.getElementById('dashLessons');if(dl)dl.textContent=done+'/7';
  var scores=GS.scores.filter(function(s){return s!==null;});
  var avg=scores.length?Math.round(scores.reduce(function(a,b){return a+b;},0)/scores.length):null;
  var da=document.getElementById('dashAccuracy');if(da)da.textContent=avg!==null?avg+'/100':'—';
}

/* ================================================================
   LEADERBOARD
   ================================================================ */
var LB_KEY='lu_leaderboard';
function loadLB(){try{return JSON.parse(localStorage.getItem(LB_KEY))||[];}catch(e){return[];}}
function saveLB2(arr){try{localStorage.setItem(LB_KEY,JSON.stringify(arr));}catch(e){}}

function updateLBEntry(){
  if(!GS.leaderboardName)return;
  var arr=loadLB();
  var idx=-1;for(var i=0;i<arr.length;i++)if(arr[i].name===GS.leaderboardName){idx=i;break;}
  var done=GS.scores.filter(function(s){return s!==null&&s>=75;}).length;
  var entry={name:GS.leaderboardName,xp:GS.xp,lessons:done};
  if(idx>=0)arr[idx]=entry;else arr.push(entry);
  arr.sort(function(a,b){return b.xp-a.xp;});
  saveLB2(arr);
}

function openLB(){document.getElementById('lbModal').classList.add('open');renderLB();if(GS.leaderboardName){var inp=document.getElementById('lbNameIn');if(inp)inp.value=GS.leaderboardName;}}
function closeLB(){document.getElementById('lbModal').classList.remove('open');}

function saveLBEntry(){
  var inp=document.getElementById('lbNameIn');
  if(!inp||!inp.value.trim()){showToast('Ismingizni kiriting!','error');return;}
  GS.leaderboardName=inp.value.trim();
  updateLBEntry();saveGS();renderLB();updateTopbar();
  showToast('✅ Reytingga saqlandi!','success');
}

function renderLB(){
  var arr=loadLB();
  var el=document.getElementById('lbList');if(!el)return;
  if(!arr.length){el.innerHTML='<div class="lb-empty">Hali hech kim yo\'q. Birinchi bo\'ling! &#127942;</div>';return;}
  var medals=['&#129351;','&#129352;','&#129353;'];
  var html='';
  arr.slice(0,20).forEach(function(e,i){
    var isMe=e.name===GS.leaderboardName;
    html+='<div class="lb-entry'+(isMe?' me':'')+'">'
      +'<div class="lb-rank">'+(i<3?medals[i]:'#'+(i+1))+'</div>'
      +'<div class="lb-name">'+(isMe?'&#11088; ':'')+e.name+'</div>'
      +'<div class="lb-lessons">'+(e.lessons||0)+'/7 &#127891;</div>'
      +'<div class="lb-xp">'+e.xp+' XP</div>'
      +'</div>';
  });
  el.innerHTML=html;
}

/* ================================================================
   VOCAB GAME
   ================================================================ */
var vgWords=[], vgCurr=0, vgTimer=15, vgTimerInv=null, vgTotalQ=10, vgPts=0;

function startVocabGame(){
  vgWords=shuffle(VOCAB_WORDS.slice()).slice(0,vgTotalQ);
  vgCurr=0;vgPts=0;
  document.getElementById('vgResult').style.display='none';
  document.getElementById('vgOpts').style.display='grid';
  document.getElementById('vgWord').style.display='block';
  nextVgQ();
}
function shuffle(arr){for(var i=arr.length-1;i>0;i--){var j=Math.floor(Math.random()*(i+1));var t=arr[i];arr[i]=arr[j];arr[j]=t;}return arr;}

function nextVgQ(){
  if(vgCurr>=vgTotalQ){endVocabGame();return;}
  clearInterval(vgTimerInv);
  var w=vgWords[vgCurr];
  document.getElementById('vgWord').textContent=w.en;
  document.getElementById('vgQ').textContent=(vgCurr+1)+'/'+vgTotalQ;
  // Options
  var wrongs=VOCAB_WORDS.filter(function(v){return v.en!==w.en;});
  var opts=shuffle(wrongs).slice(0,3).map(function(v){return v.uz;});
  opts.push(w.uz);opts=shuffle(opts);
  var oc=document.getElementById('vgOpts');oc.innerHTML='';
  opts.forEach(function(o){
    var b=document.createElement('div');b.className='vg-opt';b.textContent=o;
    b.onclick=function(){vgCheck(o,w.uz,b);};oc.appendChild(b);
  });
  // Timer
  vgTimer=15;
  document.getElementById('vgTimer').textContent=vgTimer;
  document.getElementById('vgTimerBar').style.width='100%';
  vgTimerInv=setInterval(function(){
    vgTimer--;
    document.getElementById('vgTimer').textContent=vgTimer;
    document.getElementById('vgTimerBar').style.width=(vgTimer/15*100)+'%';
    var tv=document.getElementById('vgTimer');if(tv)tv.className='vg-timer'+(vgTimer<=5?' urgent':'');
    if(vgTimer<=0){clearInterval(vgTimerInv);vgCurr++;setTimeout(nextVgQ,500);}
  },1000);
}

function vgCheck(sel,correct,btn){
  clearInterval(vgTimerInv);
  document.querySelectorAll('.vg-opt').forEach(function(b){b.classList.add('done');});
  if(sel===correct){vgPts+=10;btn.classList.add('correct');showToast('+10 pts!','success');}
  else{btn.classList.add('wrong');}
  document.getElementById('vgPts').textContent=vgPts+' pts';
  vgCurr++;setTimeout(nextVgQ,900);
}
function endVocabGame(){
  clearInterval(vgTimerInv);
  document.getElementById('vgOpts').style.display='none';
  document.getElementById('vgWord').style.display='none';
  document.getElementById('vgResult').style.display='block';
  var icon=vgPts>=80?'🏆':vgPts>=50?'🎯':'📚';
  document.getElementById('vgEndIcon').textContent=icon;
  document.getElementById('vgEndScore').textContent=vgPts+' / '+vgTotalQ*10;
  document.getElementById('vgEndMsg').textContent=vgPts>=80?'Mukammal!':vgPts>=50?"Yaxshi natija!":"Ko'proq o'qing!";
  if(vgPts>=150){earnAchievement('vocab_master');GS.xp+=50;saveAll();}
  updateTopbar();
}

/* ================================================================
   TOAST
   ================================================================ */
function showToast(msg,type){
  var tc=document.getElementById('toast-container');if(!tc)return;
  var t=document.createElement('div');t.className='toast '+(type||'info');
  var icon=type==='success'?'✅':type==='error'?'❌':'ℹ️';
  t.innerHTML='<span>'+icon+'</span><span>'+msg+'</span>';
  tc.appendChild(t);
  setTimeout(function(){t.classList.add('out');setTimeout(function(){if(t.parentNode)t.parentNode.removeChild(t);},300);},3000);
}

/* ================================================================
   LESSON CONTENT BUILDERS
   ================================================================ */
function buildToBeLesson(){
  return '<div class="lc-section"><div class="lcs-title">&#128218; Qoida</div>'
  +'<div class="rule-box"><div class="rule-title">&#128309; To Be nima?</div>'
  +'<div class="rule-body">O&#x02BC;zbek tilidagi <strong>"bo&#x02BC;lmoq"</strong> ga to&#x02BC;g&#x02BC;ri keladi. Uch shakli bor: <strong>am, is, are</strong>.</div></div>'
  +'<div class="formula">I &rarr; am &nbsp;|&nbsp; He/She/It &rarr; is &nbsp;|&nbsp; You/We/They &rarr; are</div>'
  +'</div>'
  +'<div class="lc-section"><div class="lcs-title">&#9989; Tasdiq (Positive)</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en">I <strong>am</strong> a student.</div><div class="ex-uz">Men talabaman.</div></div>'
  +'<div class="ex-card"><div class="ex-en">He <strong>is</strong> a doctor.</div><div class="ex-uz">U shifokor.</div></div>'
  +'<div class="ex-card"><div class="ex-en">We <strong>are</strong> friends.</div><div class="ex-uz">Biz do&#x02BC;stmiz.</div></div>'
  +'<div class="ex-card"><div class="ex-en">They <strong>are</strong> happy.</div><div class="ex-uz">Ular xursand.</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#10060; Inkor (Negative)</div>'
  +'<div class="formula">am/is/are + NOT</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card neg"><div class="ex-en">I <strong>am not</strong> tired. (I\'m not)</div><div class="ex-uz">Men charchamadim.</div></div>'
  +'<div class="ex-card neg"><div class="ex-en">He <strong>is not</strong> here. (isn\'t)</div><div class="ex-uz">U bu yerda emas.</div></div>'
  +'<div class="ex-card neg"><div class="ex-en">They <strong>are not</strong> ready. (aren\'t)</div><div class="ex-uz">Ular tayyor emas.</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#10067; Savol (Question)</div>'
  +'<div class="formula">Am/Is/Are + Subject + ...?</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card q"><div class="ex-en"><strong>Are</strong> you okay?</div><div class="ex-uz">Yaxshimisiz?</div></div>'
  +'<div class="ex-card q"><div class="ex-en"><strong>Is</strong> she a teacher?</div><div class="ex-uz">U o&#x02BC;qituvchimi?</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#128161; Qisqartmalar</div>'
  +'<div class="tip-box"><strong>I\'m &bull; He\'s &bull; She\'s &bull; We\'re &bull; They\'re</strong><br>isn\'t &bull; aren\'t<br><br>&#9888;&#65039; <strong>Am not</strong> ning rasmiy qisqartmasi yo\'q!</div>'
  +'</div>';
}

function buildPronounLesson(){
  return '<div class="lc-section"><div class="lcs-title">&#128218; Olmoshlar turlari</div>'
  +'<div class="rule-box"><div class="rule-title">&#128100; 3 tur</div>'
  +'<div class="rule-body"><strong>Subject</strong> — gap egasi (I, You, He...)<br><strong>Object</strong> — to&#x02BC;ldiruvchi (me, you, him...)<br><strong>Possessive</strong> — egalik (my, your, his...)</div></div>'
  +'</div>'
  +'<div class="lc-section"><div class="lcs-title">&#128202; Jadval</div>'
  +'<div style="overflow-x:auto"><table class="data-table"><tr><th>Shaxs</th><th>Subject</th><th>Object</th><th>Possessive</th><th>O\'zbek</th></tr>'
  +'<tr><td>1-shaxs</td><td class="td-en">I</td><td class="td-en">me</td><td class="td-en">my</td><td class="td-uz">Men/Mening</td></tr>'
  +'<tr><td>2-shaxs</td><td class="td-en">You</td><td class="td-en">you</td><td class="td-en">your</td><td class="td-uz">Siz/Sening</td></tr>'
  +'<tr><td>3 (erkak)</td><td class="td-en">He</td><td class="td-en">him</td><td class="td-en">his</td><td class="td-uz">U/Uning</td></tr>'
  +'<tr><td>3 (ayol)</td><td class="td-en">She</td><td class="td-en">her</td><td class="td-en">her</td><td class="td-uz">U/Uning</td></tr>'
  +'<tr><td>3 (narsa)</td><td class="td-en">It</td><td class="td-en">it</td><td class="td-en">its</td><td class="td-uz">U/Uning</td></tr>'
  +'<tr><td>Ko\'plik 1</td><td class="td-en">We</td><td class="td-en">us</td><td class="td-en">our</td><td class="td-uz">Biz/Bizning</td></tr>'
  +'<tr><td>Ko\'plik 2/3</td><td class="td-en">They</td><td class="td-en">them</td><td class="td-en">their</td><td class="td-uz">Ular/Ularning</td></tr>'
  +'</table></div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#9989; Misollar</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en"><strong>I</strong> love <strong>my</strong> country.</div><div class="ex-uz">Men vatanimni yaxshi ko\'raman.</div><div class="ex-note">I=subject | my=possessive</div></div>'
  +'<div class="ex-card"><div class="ex-en">She gave <strong>him</strong> a book.</div><div class="ex-uz">U unga kitob berdi.</div><div class="ex-note">him=object (not he!)</div></div>'
  +'<div class="ex-card"><div class="ex-en">This is <strong>her</strong> bag.</div><div class="ex-uz">Bu uning sumkasi.</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#128161; Eslatma</div>'
  +'<div class="tip-box">&#9888;&#65039; <strong>Its</strong> (egalik) &#8800; <strong>It\'s</strong> (It is)</div>'
  +'</div>';
}

function buildSPTLesson(){
  return '<div class="lc-section"><div class="lcs-title">&#128218; Qoida</div>'
  +'<div class="rule-box"><div class="rule-title">&#9200; Simple Present</div>'
  +'<div class="rule-body">&#8226; Odatdagi harakatlar (every day, always)<br>&#8226; Umumiy haqiqatlar (The sun rises...)<br>&#8226; Doimiy holat (I live in Tashkent)</div></div>'
  +'<div class="formula">Tasdiq: Subject + verb (+s/es for 3rd person)</div>'
  +'<div class="formula">Inkor: don\'t / doesn\'t + verb</div>'
  +'<div class="formula">Savol: Do / Does + Subject + verb?</div>'
  +'</div>'
  +'<div class="lc-section"><div class="lcs-title">&#9888;&#65039; 3-shaxs qoidalari</div>'
  +'<div class="rule-box warn">'
  +'<div class="rule-body">Ko\'pchilik: + <strong>-s</strong> &rarr; works, eats<br>'
  +'-ch/-sh/-ss/-o: + <strong>-es</strong> &rarr; watches, goes<br>'
  +'Undosh+y: y&rarr;<strong>ies</strong> &rarr; studies, flies<br>'
  +'Unli+y: + <strong>-s</strong> &rarr; plays, says</div></div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#9989; Misollar</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en">I <strong>work</strong> every day.</div><div class="ex-uz">Men har kun ishlayman.</div></div>'
  +'<div class="ex-card"><div class="ex-en">She <strong>studies</strong> English.</div><div class="ex-uz">U ingliz tilini o\'qiydi.</div></div>'
  +'<div class="ex-card neg"><div class="ex-en">She <strong>doesn\'t</strong> eat meat.</div><div class="ex-uz">U go\'sht emaydi.</div><div class="ex-note">doesn\'t &rarr; fe\'l oddiy!</div></div>'
  +'<div class="ex-card q"><div class="ex-en"><strong>Does</strong> he live here?</div><div class="ex-uz">U bu yerda yashaydimi?</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#128161; Signal so\'zlar</div>'
  +'<div class="tip-box"><strong>always</strong> &bull; <strong>usually</strong> &bull; <strong>often</strong> &bull; <strong>sometimes</strong> &bull; <strong>never</strong> &bull; <strong>every day/week</strong></div>'
  +'</div>';
}

function buildHaveLesson(){
  return '<div class="lc-section"><div class="lcs-title">&#128218; Have vs Has</div>'
  +'<div class="rule-box"><div class="rule-title">&#128230; Egalik</div>'
  +'<div class="rule-body"><strong>have</strong> &rarr; I / You / We / They<br><strong>has</strong> &rarr; He / She / It</div></div>'
  +'<div class="formula">I have a book. / She has a car.</div>'
  +'</div>'
  +'<div class="lc-section"><div class="lcs-title">&#9989; Misollar</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en">I <strong>have</strong> a dog.</div><div class="ex-uz">Mening itim bor.</div></div>'
  +'<div class="ex-card"><div class="ex-en">She <strong>has</strong> long hair.</div><div class="ex-uz">Uning uzun sochi bor.</div></div>'
  +'<div class="ex-card neg"><div class="ex-en">He <strong>doesn\'t have</strong> a phone.</div><div class="ex-uz">Uning telefoni yo\'q.</div></div>'
  +'<div class="ex-card q"><div class="ex-en"><strong>Do</strong> you <strong>have</strong> time?</div><div class="ex-uz">Vaqtingiz bormi?</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#127968; There is / There are</div>'
  +'<div class="rule-box"><div class="rule-title">&#128205; Mavjudlik</div>'
  +'<div class="rule-body"><strong>There is</strong> &rarr; bitta (singular)<br><strong>There are</strong> &rarr; ko\'p (plural)</div></div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en"><strong>There is</strong> a book on the table.</div><div class="ex-uz">Stolda bir kitob bor.</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>There are</strong> 20 students.</div><div class="ex-uz">20 ta o\'quvchi bor.</div></div>'
  +'<div class="ex-card neg"><div class="ex-en"><strong>There isn\'t</strong> any water.</div><div class="ex-uz">Suv yo\'q.</div></div>'
  +'<div class="ex-card q"><div class="ex-en"><strong>Is there</strong> a bank near here?</div><div class="ex-uz">Bu yaqinda bank bormi?</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#128161; Some / Any</div>'
  +'<div class="tip-box"><strong>some</strong> &mdash; tasdiqda: I have <strong>some</strong> money.<br><strong>any</strong> &mdash; inkor/savolda: I don\'t have <strong>any</strong> money.</div>'
  +'</div>';
}

function buildDemLesson(){
  return '<div class="lc-section"><div class="lcs-title">&#128218; Ko\'rsatish olmoshlari</div>'
  +'<div class="rule-box"><div class="rule-title">&#128070; 4 ta shakl</div>'
  +'<div class="rule-body"><strong>This</strong> — yaqin, 1ta &nbsp;|&nbsp; <strong>That</strong> — uzoq, 1ta<br><strong>These</strong> — yaqin, ko\'p &nbsp;|&nbsp; <strong>Those</strong> — uzoq, ko\'p</div></div>'
  +'</div>'
  +'<div class="lc-section"><div class="lcs-title">&#9989; Misollar</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en"><strong>This</strong> is my phone.</div><div class="ex-uz">Bu (yaqinimda) telefonim.</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>That</strong> is a school.</div><div class="ex-uz">U (narida) maktab.</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>These</strong> are my keys.</div><div class="ex-uz">Bular kalitlarim.</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>Those</strong> books are interesting.</div><div class="ex-uz">U (narida) kitoblar qiziqarli.</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#128240; Articles: a / an / the</div>'
  +'<div class="rule-box"><div class="rule-body"><strong>a</strong> + undosh tovush: a book, a car<br><strong>an</strong> + unli tovush: an apple, an engineer<br><strong>the</strong> — allaqachon ma\'lum narsa</div></div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en">I saw <strong>a</strong> cat. <strong>The</strong> cat was black.</div><div class="ex-uz">Men bir mushuk ko\'rdim. U mushuk qora edi.</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#128161; Eslatma</div>'
  +'<div class="tip-box">Umumiy: <strong>Dogs are friendly.</strong> — artikl yo\'q<br>Kasb: <strong>He is a doctor.</strong> — a kerak</div>'
  +'</div>';
}

function buildPContLesson(){
  return '<div class="lc-section"><div class="lcs-title">&#128218; Present Continuous</div>'
  +'<div class="rule-box"><div class="rule-title">&#127744; Hozir davom etayotgan</div>'
  +'<div class="rule-body">Signal: <strong>now, right now, at the moment, look!, listen!</strong></div></div>'
  +'<div class="formula">Subject + am/is/are + verb-ING</div>'
  +'</div>'
  +'<div class="lc-section"><div class="lcs-title">&#9888;&#65039; -ing qoidalari</div>'
  +'<div class="rule-box warn">'
  +'<div class="rule-body">Ko\'pchilik: + <strong>ing</strong> &rarr; working<br>'
  +'-e bilan: e o\'chir + <strong>ing</strong> &rarr; making<br>'
  +'Qisqa+undosh: ikkilashtir + <strong>ing</strong> &rarr; running<br>'
  +'-ie bilan: ie&rarr;y + <strong>ing</strong> &rarr; lying</div></div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#9989; Misollar</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en">I <strong>am studying</strong> now.</div><div class="ex-uz">Men hozir o\'qiyapman.</div></div>'
  +'<div class="ex-card"><div class="ex-en">She <strong>is cooking</strong> dinner.</div><div class="ex-uz">U ovqat pishiryapti.</div></div>'
  +'<div class="ex-card neg"><div class="ex-en">He <strong>is not watching</strong> TV.</div><div class="ex-uz">U TV ko\'rmayapti.</div></div>'
  +'<div class="ex-card q"><div class="ex-en"><strong>Are</strong> you <strong>listening</strong>?</div><div class="ex-uz">Tinglayapsizmi?</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#9889; SP vs Continuous</div>'
  +'<div class="tip-box"><strong>I read every day.</strong> &rarr; Oddiy (Simple Present)<br><strong>I am reading now.</strong> &rarr; Hozir (Continuous)<br><br>&#9888;&#65039; Bu fe\'llar Continuous bilan ishlatilmaydi:<br><strong>know, like, love, want, need, understand</strong></div>'
  +'</div>';
}

function buildPrepLesson(){
  return '<div class="lc-section"><div class="lcs-title">&#128218; Vaqt predloglari</div>'
  +'<div class="rule-box"><div class="rule-title">&#128336; in / on / at</div>'
  +'<div class="rule-body"><strong>at</strong> — aniq vaqt: at 5 PM, at noon<br><strong>on</strong> — kun/sana: on Monday, on July 4th<br><strong>in</strong> — oy/yil/mavsim: in January, in 2025</div></div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#127968; Joy predloglari</div>'
  +'<div class="rule-box"><div class="rule-body"><strong>at</strong> — aniq nuqta: at school, at home<br><strong>on</strong> — yuzada: on the table, on the wall<br><strong>in</strong> — ichida: in the box, in Tashkent</div></div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en">The book is <strong>on</strong> the table.</div><div class="ex-uz">Kitob stolning ustida.</div></div>'
  +'<div class="ex-card"><div class="ex-en">She lives <strong>in</strong> London.</div><div class="ex-uz">U Londonda yashaydi.</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#8596;&#65039; Qo\'shimcha</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en"><strong>under</strong> — tagida</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>next to</strong> — yonida</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>between</strong> — orasida</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>in front of</strong> — oldida</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>behind</strong> — orqasida</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>above</strong> — ustida</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lcs-title">&#128161; Eslatma</div>'
  +'<div class="tip-box"><strong>in the morning/afternoon/evening</strong> (IN)<br><strong>at night, at noon, at midnight</strong> (AT)</div>'
  +'</div>';
}

/* ================================================================
   QUESTIONS
   ================================================================ */
function buildToBeQs(){return[
  {type:'mc',q:'Qaysi variant to\'g\'ri? "Men shifokorman."',opts:['I is a doctor.','I am a doctor.','I are a doctor.','Am I a doctor.'],a:1,exp:'I bilan faqat AM.'},
  {type:'mc',q:'"She ___ a teacher."',opts:['am','are','is','be'],a:2,exp:'He/She/It bilan IS.'},
  {type:'mc',q:'Inkor: qaysi gap to\'g\'ri?',opts:['They not are ready.','They are not ready.','They aren\'t not ready.','Are they not ready?'],a:1,exp:'are + not yoki aren\'t.'},
  {type:'fill',q:'"We ___ students."',a:'are',exp:'We bilan ARE.'},
  {type:'mc',q:'"___ you tired?" — savol',opts:['Am','Is','Are','Be'],a:2,exp:'You bilan Are.'},
  {type:'mc',q:'"He ___ not at home."',opts:['am','are','is','be'],a:2,exp:'He bilan IS.'},
  {type:'mc',q:'Qaysi gap xato?',opts:['She is my friend.','He am a student.','They are happy.','It is a car.'],a:1,exp:'He bilan IS, AM emas.'},
  {type:'fill',q:'"I ___ not hungry."',a:['am'],exp:'I am not.'},
  {type:'mc',q:'"___ it a cat or a dog?"',opts:['Am','Are','Is','Be'],a:2,exp:'It bilan Is.'},
  {type:'mc',q:'To\'g\'ri qisqartma?',opts:['I amn\'t late.','I\'m not late.','I not am late.','Am not I late.'],a:1,exp:'I am not = I\'m not.'}
];}

function buildPronounQs(){return[
  {type:'mc',q:'"Ali is my friend. ___ is a doctor."',opts:['She','He','They','It'],a:1,exp:'Ali erkak — He.'},
  {type:'mc',q:'"Give ___ the book." (menga)',opts:['I','my','me','mine'],a:2,exp:'Object — me.'},
  {type:'fill',q:'"This is ___ bag." (Sara — tegishli)',a:['her'],exp:'She possessive = her.'},
  {type:'mc',q:'Qaysi gapda xato?',opts:['I love my dog.','Her is a teacher.','We need your help.','They gave us a gift.'],a:1,exp:'"Her is" xato — "She is".'},
  {type:'mc',q:'"Biz ularni kutdik."',opts:['We waited us.','We waited they.','We waited them.','Us waited them.'],a:2,exp:'them = object.'},
  {type:'mc',q:'"___ book is interesting." (uning — erkak)',opts:['He','Him','His','Her'],a:2,exp:'Possessive — His.'},
  {type:'mc',q:'"The cat licked ___ paw."',opts:['his','her','its','their'],a:2,exp:'Narsa/hayvon — its.'},
  {type:'fill',q:'"What is ___ phone number?" (Siz)',a:['your'],exp:'Siz = your.'},
  {type:'mc',q:'To\'g\'ri gap:',opts:['Me and him went there.','He and I went there.','Him and I went there.','I and him went there.'],a:1,exp:'Subject: He and I.'},
  {type:'fill',q:'"___ and I went to school." (Ali)',a:['ali'],exp:'Ali and I (subject).'}
];}

function buildSPTQs(){return[
  {type:'mc',q:'"She ___ to school every day."',opts:['go','goes','goed','is going'],a:1,exp:'She uchun goes.'},
  {type:'fill',q:'"He ___ English every day." (study)',a:['studies'],exp:'study + 3-shaxs = studies.'},
  {type:'mc',q:'Inkor: "I ___ meat."',opts:['don\'t eat','doesn\'t eat','not eat','don\'t eats'],a:0,exp:"I + don't + verb."},
  {type:'mc',q:'Savol: "___ she like pizza?"',opts:['Do','Does','Is','Are'],a:1,exp:'3-shaxs savolda Does.'},
  {type:'fill',q:'"He ___ TV every night." (watch)',a:['watches'],exp:'watch + es = watches.'},
  {type:'mc',q:'Qaysi gapda xato?',opts:['I work here.','She works hard.',"He don't like it.",'They study English.'],a:2,exp:"He bilan doesn't."},
  {type:'fill',q:'"They ___ football." (inkor — play)',a:["don't play","do not play"],exp:"They + don't + play."},
  {type:'mc',q:'"The sun ___ in the east."',opts:['rise','rises','is rising','rose'],a:1,exp:'Simple Present + rises.'},
  {type:'mc',q:'"I ___ go to gym on Mondays." (usually)',opts:['usually go','go usually','goes usually','usually goes'],a:0,exp:"'usually' fe'ldan oldin. I + go."},
  {type:'transform',q:'"I play tennis." → He haqida',hint:'He/She/It uchun -s/-es',a:['he plays tennis','he plays tennis.'],exp:'He plays tennis.'}
];}

function buildHaveQs(){return[
  {type:'mc',q:'"She ___ a new car."',opts:['have','has','haves','is have'],a:1,exp:'She uchun HAS.'},
  {type:'fill',q:'"They ___ two dogs." (have/has)',a:['have'],exp:'They bilan HAVE.'},
  {type:'mc',q:'Inkor: "He ___ time."',opts:["don't have","hasn't have","doesn't have",'not has'],a:2,exp:"doesn't have."},
  {type:'mc',q:'"___ there a bank near here?"',opts:['Is','Are','Have','Does'],a:0,exp:'"There is" savolda = Is there.'},
  {type:'fill',q:'"There ___ many students."',a:['are'],exp:'Ko\'plik uchun ARE.'},
  {type:'mc',q:'"___ you have a pen?"',opts:['Does','Is','Do','Have'],a:2,exp:'You bilan DO.'},
  {type:'mc',q:'To\'g\'ri gap?',opts:['There are a book.','There is some books.','There are some books.','There have books.'],a:2,exp:'Ko\'plik + There are.'},
  {type:'fill',q:'"Do you have ___ questions?"',a:['any'],exp:'Savol/inkorda ANY.'},
  {type:'mc',q:'"She has long hair." — inkor',opts:["She doesn't has long hair.","She don't have long hair.","She doesn't have long hair.","She hasn't long hair."],a:2,exp:"doesn't have!"},
  {type:'transform',q:'"There is a cat." → Ko\'plikka (cats)',hint:'Ko\'plik: There are',a:['there are cats','there are some cats'],exp:'There are cats.'}
];}

function buildDemQs(){return[
  {type:'mc',q:'"___ is my phone." — qo\'lingizdagi',opts:['That','Those','This','These'],a:2,exp:'Yaqin, bitta: THIS.'},
  {type:'fill',q:'"___ are my keys." (yaqin, ko\'p)',a:['These','these'],exp:'Yaqin, ko\'p: THESE.'},
  {type:'mc',q:'Uzoqdagi bitta kitob:',opts:['This is a book.','These is a book.','That is a book.','Those is a book.'],a:2,exp:'Uzoq, bitta: THAT.'},
  {type:'mc',q:'"___ apple" — to\'g\'ri artikl',opts:['a apple','an apple','the apple','one apple'],a:1,exp:'Unli (a) dan oldin AN.'},
  {type:'fill',q:'"She is ___ engineer."',a:['an'],exp:'"Engineer" unli bilan = AN.'},
  {type:'mc',q:'"I saw a dog. ___ dog was brown."',opts:['A','An','The','This'],a:2,exp:'Allaqachon aytilgan = THE.'},
  {type:'mc',q:'Uzoqdagi ko\'p kitob:',opts:['This','These','That','Those'],a:3,exp:'Uzoq, ko\'p: THOSE.'},
  {type:'fill',q:'"___ are his shoes." (u narida, ko\'p)',a:['Those','those'],exp:'THOSE.'},
  {type:'mc',q:'Artikl xato ishlatilgan gap:',opts:['I have a car.','She is an actress.','He is the doctor.','I like the music.'],a:3,exp:'"I like the music" xato — "I like music".'},
  {type:'transform',q:'"This is my book." → Ko\'plikka',hint:'This → These, is → are',a:['these are my books'],exp:'These are my books.'}
];}

function buildPContQs(){return[
  {type:'mc',q:'"She ___ dinner now."',opts:['cook','is cooking','cooks','was cooking'],a:1,exp:'Hozir: is + cooking.'},
  {type:'fill',q:'"They ___ football right now." (play)',a:['are playing'],exp:'They + are + playing.'},
  {type:'mc',q:'"run" + ing = ?',opts:['runing','running','runeing','runnes'],a:1,exp:'Qisqa+undosh → ikkilashtir: running.'},
  {type:'mc',q:'Inkor: "I ___ TV." (not watch)',opts:['am not watching','am not watch','is not watching','not watching'],a:0,exp:'I am not watching.'},
  {type:'fill',q:'"make" + ing = ?',a:['making'],exp:'make → e olib tashlang → making.'},
  {type:'mc',q:'To\'g\'ri Present Continuous gap:',opts:['I am liking coffee.','She is knowing the answer.','He is running in the park.','They are wanting to leave.'],a:2,exp:'like/know/want bilan ishlatilmaydi. running ✓'},
  {type:'mc',q:'Savol: "___ you ___ to music?" (hozir)',opts:['Are...listening','Do...listen','Is...listening','Were...listening'],a:0,exp:'Are you listening? ✓'},
  {type:'fill',q:'"He is sit___ on the chair."',a:['sitting'],exp:'sit → sitting.'},
  {type:'mc',q:'"She ___ English every morning." — oddiy',opts:['is studying','studies','study','are studying'],a:1,exp:'"every morning" = Simple Present: studies.'},
  {type:'transform',q:'"I work at home." → Present Continuous',hint:'am/is/are + verb-ing',a:['i am working at home',"i'm working at home"],exp:'I am working at home.'}
];}

function buildPrepQs(){return[
  {type:'mc',q:'"I wake up ___ 7 AM."',opts:['in','on','at','by'],a:2,exp:'Aniq vaqt → AT.'},
  {type:'fill',q:'"She was born ___ 1999."',a:['in'],exp:'Yil → IN.'},
  {type:'mc',q:'"The meeting is ___ Monday."',opts:['in','at','on','for'],a:2,exp:'Kun → ON.'},
  {type:'mc',q:'"The book is ___ the table." — ustida',opts:['under','in','on','at'],a:2,exp:'Yuzada → ON.'},
  {type:'fill',q:'"She lives ___ Tashkent."',a:['in'],exp:'Shahar → IN.'},
  {type:'mc',q:'"I\'ll meet you ___ the airport."',opts:['in','on','at','by'],a:2,exp:'Aniq joy → AT.'},
  {type:'mc',q:'"The cat is ___ the chair." — tagida',opts:['on','in','under','above'],a:2,exp:'Tagida → UNDER.'},
  {type:'fill',q:'"I study English ___ the morning."',a:['in'],exp:'Kun qismlari → IN.'},
  {type:'mc',q:'To\'g\'ri gap:',opts:['She was born in Monday.','He works at 9 AM on weekdays.','They arrived in midnight.','I go to school on morning.'],a:1,exp:'"at 9 AM" + "on weekdays" ✓'},
  {type:'mc',q:'"The park is ___ the school and the bank."',opts:['next to','between','behind','in front of'],a:1,exp:'Ikki narsa orasida → BETWEEN.'}
];}

/* ================================================================
   INIT
   ================================================================ */
function init(){
  loadAll();loadGS();

  // Theme
  document.documentElement.setAttribute('data-theme',APP.theme);
  document.getElementById('themeToggle').textContent=APP.theme==='dark'?'🌙':'☀️';

  // Streak
  updateStrike();buildStreakCalendar();

  // Build UI
  buildAlphabet();buildNumbers();buildColors();buildMiniQuiz();

  // Grammar
  renderRoad();updateGramXP();showGramSections('road');

  // Daily
  initDaily();

  // Achievements
  renderAchievements();

  // Topbar
  updateTopbar();

  // Progress page
  renderProgressPage();

  // Vocab game initial state
  startVocabGame();

  // Speech
  if(synth){loadVoices();setTimeout(loadVoices,500);setTimeout(loadVoices,1500);}

  // Canvas initial frame
  drawFrame(0,AD[0]);

  // PWA
  if('serviceWorker' in navigator){
    window.addEventListener('load',function(){
      // SW registration would go here for full PWA
    });
  }

  // Restore last page
  if(APP.page&&APP.page!=='dashboard'){
    navTo(APP.page);
  }

  // Preload voices
  setTimeout(function(){if(synth)loadVoices();},2000);
}

// Start
init();
</script>
</body>
</html>"""

with open('/home/claude/linguauz.html','w',encoding='utf-8') as f:
    f.write(html)
print("Done:", len(html), "chars")
PYEOF
python3 /home/claude/build_platform.py
Output

Command argument is 156_681 bytes, exceeding the 100_000-byte per-argument limit. For large content, pipe via stdin or use a file-write API instead of embedding the content inline in the command. Argument preview: 'cat > /home/claude/build_platform.py << \'PYEOF\'\nhtml = r"""<!DOCTYPE html>\n<html lang="uz" data-theme="dark">\n<head>\n<meta charset="UTF-8">\n<meta name="viewport" content="width=device-width, initial-s'
Done
https://namsifl.uz/ this is an example for may web side make ui like the webside  i dended to you

12:25 PM
Let me fetch and analyze that website first:


Fetched: Namangan davlat chet tillari instituti
Fetched: Namangan davlat chet tillari instituti
Namangan davlat chet tillari instituti

namsifl.uz
NAMANGAN DAVLAT CHET TILLARI INSTITUTINING YANGI BINOSI FOYDALANISHGA ...

fledu.uz
Namangan davlat chet tillari instituti

namsifl.uz
Results from the web
Now I have a clear picture. It's a clean, professional Uzbek university website with a white/light background, blue accent colors, top navigation bar, hero image section, news cards grid, and a formal footer. Let me rebuild LinguaUz with this exact UI style:


Check the uploaded file to extract all content data
Check the uploaded file to extract all content data
Now I have everything. Let me build the complete file with namsifl.uz-style UI:


Ran 3 commands, created 2 files
Ran 3 commands, created 2 files

Check file size

Script

Copy source file

Script

Create the main rebuild Python script - part 1: CSS and header
part1.py

Generate part 1 CSS

Script

Create HTML body part
part2.py
Done


You are out of free message
