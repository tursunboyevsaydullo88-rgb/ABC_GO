
<html lang="uz">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ingliz Tili | O'zbek tilida</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Unbounded:wght@700;900&family=DM+Sans:wght@400;500;700&display=swap');
:root{--bg:#070712;--s1:#0f0f1e;--s2:#181830;--s3:#222240;--ac:#7c6fff;--ac2:#ff6b8a;--ac3:#3ee8a0;--ac4:#ffb347;--tx:#eeeef8;--mt:#606090;--bd:rgba(124,111,255,.18);}
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'DM Sans',sans-serif;background:var(--bg);color:var(--tx);overflow-x:hidden;}
/* HERO */
.hero{text-align:center;padding:50px 16px 30px;position:relative;}
.hero::before{content:'';position:absolute;top:-60px;left:50%;transform:translateX(-50%);width:600px;height:400px;background:radial-gradient(ellipse,rgba(124,111,255,.18) 0%,transparent 70%);pointer-events:none;}
.badge{display:inline-block;background:rgba(124,111,255,.12);border:1px solid rgba(124,111,255,.4);color:#b0a8ff;font-size:11px;letter-spacing:3px;text-transform:uppercase;padding:6px 18px;border-radius:100px;margin-bottom:16px;}
.hero h1{font-family:'Unbounded',sans-serif;font-size:clamp(24px,5vw,48px);font-weight:900;line-height:1.1;margin-bottom:10px;}
.hero h1 span{color:var(--ac);}
.hero p{color:var(--mt);font-size:14px;max-width:400px;margin:0 auto;}
/* NAV */
.snav{display:flex;gap:7px;overflow-x:auto;padding:16px 14px;justify-content:center;flex-wrap:wrap;max-width:940px;margin:0 auto;}
.snav::-webkit-scrollbar{height:3px;}.snav::-webkit-scrollbar-thumb{background:var(--ac);border-radius:3px;}
.sbtn{flex-shrink:0;padding:9px 16px;border-radius:100px;border:1px solid var(--bd);background:var(--s1);color:var(--mt);font-family:'DM Sans',sans-serif;font-size:12px;cursor:pointer;transition:all .2s;white-space:nowrap;}
.sbtn:hover{border-color:var(--ac);color:var(--tx);}
.sbtn.on{background:var(--ac);border-color:var(--ac);color:#fff;font-weight:700;}
/* CONTENT */
.wrap{max-width:940px;margin:0 auto;padding:16px 14px 80px;}
.sec{display:none;animation:fu .35s ease;}
.sec.on{display:block;}
@keyframes fu{from{opacity:0;transform:translateY(12px)}to{opacity:1;transform:translateY(0)}}
/* CARDS */
.card{background:var(--s1);border:1px solid var(--bd);border-radius:18px;padding:22px;margin-bottom:16px;transition:border-color .2s;}
.card:hover{border-color:rgba(124,111,255,.35);}
.ch{display:flex;align-items:center;gap:12px;cursor:pointer;user-select:none;}
.ci{width:44px;height:44px;border-radius:12px;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;}
.ct{flex:1;}.ct h3{font-family:'Unbounded',sans-serif;font-size:13px;font-weight:700;margin-bottom:3px;}
.ct p{font-size:12px;color:var(--mt);}
.ti{color:var(--mt);transition:transform .3s;font-size:15px;}
.card.op .ti{transform:rotate(180deg);}
.cb{display:none;margin-top:18px;}
.card.op .cb{display:block;}
/* ALPHABET */
.agrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(75px,1fr));gap:9px;}
.alc{background:var(--s2);border:1.5px solid var(--bd);border-radius:13px;padding:12px 6px 9px;text-align:center;cursor:pointer;transition:all .2s;}
.alc:hover{transform:translateY(-3px);box-shadow:0 8px 20px rgba(124,111,255,.2);}
.alc .bl{font-family:'Unbounded',sans-serif;font-size:24px;font-weight:900;line-height:1;}
.alc .sl{font-size:10px;color:var(--mt);margin-top:3px;}
.alc .hl{font-size:9px;color:var(--ac);margin-top:2px;}
/* TABLE */
.wt{width:100%;border-collapse:collapse;font-size:13px;}
.wt th{text-align:left;padding:9px 11px;font-size:10px;letter-spacing:1.5px;text-transform:uppercase;color:var(--mt);border-bottom:1px solid var(--bd);}
.wt td{padding:10px 11px;border-bottom:1px solid rgba(255,255,255,.04);vertical-align:top;}
.wt tr:last-child td{border-bottom:none;}
.wt tr:hover td{background:rgba(124,111,255,.05);}
.en{font-weight:600;color:var(--ac);font-size:14px;}
.pr{color:#b0a8ff;font-style:italic;font-size:12px;}
.uz{color:var(--tx);}
.spk{background:rgba(124,111,255,.14);border:1px solid rgba(124,111,255,.3);color:var(--ac);font-size:11px;padding:3px 8px;border-radius:100px;cursor:pointer;font-family:'DM Sans',sans-serif;transition:all .2s;margin-left:4px;}
.spk:hover{background:var(--ac);color:#fff;}
/* NUMS */
.ngrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(100px,1fr));gap:7px;}
.nc{background:var(--s2);border:1px solid var(--bd);border-radius:9px;padding:8px 10px;display:flex;align-items:center;gap:8px;cursor:pointer;transition:border-color .2s;}
.nc:hover{border-color:var(--ac4);}
.nc .n{font-family:'Unbounded',sans-serif;font-weight:700;color:var(--ac4);font-size:14px;min-width:24px;}
/* COLORS */
.cgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(115px,1fr));gap:8px;}
.cc{border-radius:11px;padding:12px;cursor:pointer;transition:transform .2s;}
.cc:hover{transform:scale(1.04);}
/* GRAMMAR */
.gb{background:var(--s2);border-left:3px solid var(--ac);border-radius:0 11px 11px 0;padding:13px 16px;margin:9px 0;font-size:13px;line-height:1.8;}
.gb.g{border-color:var(--ac3);}
.gb.o{border-color:var(--ac4);}
.gb.r{border-color:var(--ac2);}
.ex{background:rgba(124,111,255,.07);border:1px solid var(--bd);border-radius:11px;padding:11px 14px;margin:8px 0;}
.ex .eg{color:var(--ac);font-weight:600;font-size:13px;margin-bottom:3px;}
.ex .uz2{color:var(--mt);font-size:12px;}
/* DIALOGUE */
.dlg{display:flex;flex-direction:column;gap:9px;}
.bbl{max-width:82%;padding:11px 14px;border-radius:14px;font-size:13px;line-height:1.5;}
.bbl.a{align-self:flex-start;background:var(--s2);border-bottom-left-radius:4px;}
.bbl.b{align-self:flex-end;background:rgba(124,111,255,.18);border-bottom-right-radius:4px;}
.bbl .wh{font-size:9px;letter-spacing:1px;text-transform:uppercase;color:var(--mt);margin-bottom:3px;}
.bbl .eg{font-weight:500;}
.bbl .uz3{font-size:11px;color:var(--mt);margin-top:2px;}
/* QUIZ */
.qa{background:var(--s2);border-radius:13px;padding:16px;margin-top:13px;}
.qq{font-family:'Unbounded',sans-serif;font-size:10px;color:var(--ac);margin-bottom:9px;letter-spacing:1px;}
.qqt{font-size:17px;font-weight:700;margin-bottom:13px;}
.qo{display:grid;grid-template-columns:1fr 1fr;gap:6px;margin-bottom:11px;}
.qb{background:var(--s1);border:1px solid var(--bd);border-radius:9px;padding:10px 11px;cursor:pointer;font-size:13px;transition:all .2s;text-align:center;}
.qb:hover{border-color:var(--ac);}
.qb.ok{border-color:var(--ac3);background:rgba(62,232,160,.1);color:var(--ac3);}
.qb.no{border-color:var(--ac2);background:rgba(255,107,138,.1);color:var(--ac2);}
.qnxt{background:var(--ac);color:#fff;border:none;border-radius:9px;padding:10px 20px;font-family:'DM Sans',sans-serif;font-size:13px;font-weight:600;cursor:pointer;display:none;}
.qsc{font-size:12px;color:var(--mt);margin-top:6px;}
/* OVERVIEW */
.ov{display:grid;grid-template-columns:repeat(auto-fill,minmax(145px,1fr));gap:9px;margin-bottom:24px;}
.ovc{background:var(--s1);border:1px solid var(--bd);border-radius:15px;padding:16px 13px;cursor:pointer;transition:all .22s;text-align:center;}
.ovc:hover{border-color:var(--ac);transform:translateY(-3px);}
.ovc .on2{font-family:'Unbounded',sans-serif;font-size:24px;font-weight:900;margin-bottom:5px;}
.ovc .ot{font-size:11px;font-weight:600;margin-bottom:2px;}
.ovc .os{font-size:10px;color:var(--mt);}
.tag{display:inline-block;background:rgba(124,111,255,.12);color:var(--ac);font-size:10px;padding:2px 8px;border-radius:100px;font-weight:600;margin-right:3px;}
.tag.g{background:rgba(62,232,160,.1);color:var(--ac3);}
.tag.o{background:rgba(255,179,71,.1);color:var(--ac4);}
.tag.r{background:rgba(255,107,138,.1);color:var(--ac2);}
.sl{font-family:'Unbounded',sans-serif;font-size:9px;letter-spacing:2px;text-transform:uppercase;color:var(--mt);margin:22px 0 9px;}
hr{border:none;border-top:1px solid var(--bd);margin:14px 0;}
/* MODAL */
.mo{display:none;position:fixed;inset:0;background:rgba(0,0,0,.88);backdrop-filter:blur(8px);z-index:999;align-items:center;justify-content:center;padding:14px;}
.mo.on{display:flex;}
.mi{background:var(--s1);border:1px solid rgba(124,111,255,.3);border-radius:22px;padding:24px 20px;max-width:380px;width:100%;text-align:center;animation:pi .3s cubic-bezier(.34,1.56,.64,1);}
@keyframes pi{from{opacity:0;transform:scale(.8)}to{opacity:1;transform:scale(1)}}
.cw{width:240px;height:240px;margin:0 auto 12px;border-radius:14px;overflow:hidden;background:var(--s2);border:2px solid var(--bd);position:relative;}
#lc{display:block;width:240px;height:240px;}
.pbw{width:100%;height:4px;background:var(--s3);border-radius:4px;margin-bottom:12px;overflow:hidden;}
.pbi{height:100%;background:var(--ac);border-radius:4px;transition:width .05s linear;}
.cc2{display:flex;gap:7px;justify-content:center;margin-bottom:12px;}
.cb2{background:var(--s2);border:1px solid var(--bd);color:var(--tx);border-radius:8px;padding:7px 14px;cursor:pointer;font-size:12px;font-family:'DM Sans',sans-serif;transition:all .2s;}
.cb2:hover{background:var(--ac);border-color:var(--ac);}
.cb2.pl{background:rgba(62,232,160,.12);border-color:var(--ac3);color:var(--ac3);}
.ml{font-family:'Unbounded',sans-serif;font-size:17px;font-weight:900;color:var(--ac);margin-bottom:3px;}
.mp{font-size:15px;color:#b0a8ff;margin-bottom:3px;}
.me{font-size:12px;color:var(--mt);margin-bottom:12px;}
.wr{display:flex;gap:7px;justify-content:center;flex-wrap:wrap;margin-bottom:14px;}
.wp{background:var(--s2);border:1px solid var(--bd);border-radius:100px;padding:5px 13px;font-size:12px;cursor:pointer;transition:all .2s;}
.wp:hover{border-color:var(--ac);color:var(--ac);}
.spkb{background:var(--ac);color:#fff;border:none;border-radius:11px;padding:11px 24px;font-size:14px;font-weight:700;cursor:pointer;font-family:'DM Sans',sans-serif;width:100%;transition:all .2s;margin-bottom:8px;}
.spkb:hover{opacity:.85;}
.spkb:active{transform:scale(.97);}
.cls{background:var(--s2);border:1px solid var(--bd);color:var(--tx);border-radius:11px;padding:9px 22px;cursor:pointer;font-family:'DM Sans',sans-serif;font-size:13px;width:100%;}
@media(max-width:460px){.qo{grid-template-columns:1fr;}.ov{grid-template-columns:repeat(2,1fr);}.agrid{grid-template-columns:repeat(auto-fill,minmax(62px,1fr));}}

/* ===== GRAMMAR QUEST STYLES ===== */
.gram-hero{background:linear-gradient(135deg,#0f0f28 0%,#1a1040 60%,#0a1a2e 100%);border:1px solid rgba(124,111,255,.25);border-radius:22px;padding:28px 24px 22px;margin-bottom:22px;position:relative;overflow:hidden;}
.gram-hero::before{content:'';position:absolute;top:-80px;right:-80px;width:300px;height:300px;background:radial-gradient(ellipse,rgba(124,111,255,.15) 0%,transparent 70%);pointer-events:none;}
.gram-hero-inner{position:relative;z-index:1;}
.gram-title-row{display:flex;align-items:center;justify-content:space-between;margin-bottom:10px;}
.gram-badge{background:linear-gradient(90deg,#7c6fff,#ff6b8a);color:#fff;font-size:10px;letter-spacing:2.5px;text-transform:uppercase;padding:5px 14px;border-radius:100px;font-weight:700;}
.lb-open-btn{background:rgba(255,179,71,.12);border:1px solid rgba(255,179,71,.35);color:#ffb347;font-size:12px;padding:6px 14px;border-radius:100px;cursor:pointer;font-family:'DM Sans',sans-serif;font-weight:600;transition:all .2s;}
.lb-open-btn:hover{background:rgba(255,179,71,.25);}
.gram-h2{font-family:'Unbounded',sans-serif;font-size:clamp(18px,4vw,28px);font-weight:900;margin-bottom:6px;}
.gram-h2 span{color:#7c6fff;}
.gram-sub{font-size:12px;color:var(--mt);margin-bottom:14px;}
.xp-bar-wrap{width:100%;height:8px;background:rgba(255,255,255,.06);border-radius:8px;overflow:hidden;margin-bottom:6px;}
.xp-bar-inner{height:100%;background:linear-gradient(90deg,#7c6fff,#3ee8a0);border-radius:8px;transition:width .6s cubic-bezier(.34,1.56,.64,1);}
.xp-label{font-size:11px;color:var(--mt);font-weight:600;letter-spacing:.5px;}

/* LESSON ROAD */
.lesson-road{display:flex;flex-direction:column;gap:14px;padding-bottom:10px;}
.lesson-node{position:relative;display:flex;align-items:center;gap:16px;background:var(--s1);border:1.5px solid var(--bd);border-radius:18px;padding:16px 18px;cursor:pointer;transition:all .25s;}
.lesson-node.unlocked:hover{border-color:rgba(124,111,255,.5);transform:translateX(4px);box-shadow:0 6px 24px rgba(124,111,255,.12);}
.lesson-node.locked{opacity:.55;cursor:not-allowed;filter:grayscale(.4);}
.lesson-node.completed{border-color:rgba(62,232,160,.35);background:rgba(62,232,160,.04);}
.lesson-node.active{border-color:rgba(124,111,255,.6);background:rgba(124,111,255,.06);animation:nodePulse 2.5s infinite;}
@keyframes nodePulse{0%,100%{box-shadow:0 0 0 0 rgba(124,111,255,.2)}50%{box-shadow:0 0 0 8px rgba(124,111,255,0)}}
.ln-icon{width:50px;height:50px;border-radius:14px;display:flex;align-items:center;justify-content:center;font-size:22px;flex-shrink:0;position:relative;}
.ln-lock{position:absolute;bottom:-4px;right:-4px;font-size:13px;}
.ln-body{flex:1;}
.ln-title{font-family:'Unbounded',sans-serif;font-size:12px;font-weight:700;margin-bottom:3px;}
.ln-meta{font-size:11px;color:var(--mt);display:flex;gap:8px;flex-wrap:wrap;}
.ln-tag{padding:2px 8px;border-radius:100px;font-size:9px;font-weight:700;letter-spacing:.5px;}
.ln-tag.a1{background:rgba(62,232,160,.15);color:#3ee8a0;}
.ln-tag.a2{background:rgba(124,111,255,.15);color:#7c6fff;}
.ln-tag.b1{background:rgba(255,107,138,.15);color:#ff6b8a;}
.ln-score{text-align:right;flex-shrink:0;}
.ln-score-num{font-family:'Unbounded',sans-serif;font-size:16px;font-weight:900;}
.ln-score-lbl{font-size:9px;color:var(--mt);letter-spacing:.5px;}
.ln-stars{font-size:14px;margin-top:2px;}
.connector-line{width:2px;height:16px;background:linear-gradient(180deg,rgba(124,111,255,.3),rgba(124,111,255,.1));margin:0 auto;border-radius:2px;}

/* LESSON PANEL */
.lp-header{display:flex;align-items:center;gap:14px;margin-bottom:20px;background:var(--s1);border:1px solid var(--bd);border-radius:16px;padding:14px 16px;}
.lp-back{background:none;border:1px solid var(--bd);color:var(--mt);font-size:12px;padding:6px 12px;border-radius:8px;cursor:pointer;font-family:'DM Sans',sans-serif;white-space:nowrap;transition:all .2s;}
.lp-back:hover{border-color:var(--ac);color:var(--ac);}
.lp-title-wrap{display:flex;align-items:center;gap:10px;flex:1;}
.lp-icon{font-size:24px;}
.lp-title{font-family:'Unbounded',sans-serif;font-size:13px;font-weight:700;}
.lp-sub{font-size:10px;color:var(--mt);}
.lp-diff{background:rgba(124,111,255,.15);color:#b0a8ff;font-size:10px;font-weight:700;padding:4px 10px;border-radius:100px;white-space:nowrap;}

/* LESSON CONTENT */
.lc-section{margin-bottom:22px;}
.lc-section-title{font-family:'Unbounded',sans-serif;font-size:10px;letter-spacing:2px;text-transform:uppercase;color:var(--ac);margin-bottom:10px;display:flex;align-items:center;gap:8px;}
.lc-section-title::after{content:'';flex:1;height:1px;background:var(--bd);}
.rule-box{background:linear-gradient(135deg,rgba(124,111,255,.08),rgba(62,232,160,.05));border:1px solid rgba(124,111,255,.2);border-radius:14px;padding:16px 18px;margin-bottom:12px;}
.rule-box.warn{background:rgba(255,179,71,.07);border-color:rgba(255,179,71,.25);}
.rule-box.danger{background:rgba(255,107,138,.07);border-color:rgba(255,107,138,.25);}
.rule-title{font-weight:700;font-size:13px;margin-bottom:7px;display:flex;align-items:center;gap:7px;}
.rule-body{font-size:13px;line-height:1.8;color:#c8c8e8;}
.formula{background:rgba(0,0,0,.35);border:1px solid rgba(124,111,255,.3);border-radius:10px;padding:10px 14px;font-family:'Courier New',monospace;font-size:13px;color:#7c6fff;margin:8px 0;letter-spacing:.5px;}
.examples-grid{display:grid;gap:8px;}
.ex-card{background:var(--s2);border-radius:12px;padding:12px 14px;border-left:3px solid var(--ac);}
.ex-card.neg{border-color:var(--ac2);}
.ex-card.q{border-color:var(--ac3);}
.ex-en{font-weight:600;font-size:13px;color:#e0dcff;margin-bottom:3px;}
.ex-uz{font-size:11px;color:var(--mt);}
.ex-note{font-size:10px;color:#ffb347;margin-top:4px;font-style:italic;}
.tip-box{background:rgba(255,179,71,.08);border:1px solid rgba(255,179,71,.2);border-radius:12px;padding:12px 14px;font-size:12px;line-height:1.7;color:#ffd080;}
.tip-box strong{color:#ffb347;}

/* TEST PANEL */
.tp-progress-wrap{width:100%;height:5px;background:var(--s3);border-radius:5px;overflow:hidden;margin-bottom:22px;}
.tp-progress-bar{height:100%;background:linear-gradient(90deg,#7c6fff,#3ee8a0);border-radius:5px;transition:width .3s ease;}
.tp-score-chip{background:rgba(62,232,160,.12);border:1px solid rgba(62,232,160,.3);color:#3ee8a0;font-family:'Unbounded',sans-serif;font-size:11px;font-weight:700;padding:4px 12px;border-radius:100px;white-space:nowrap;}
.q-block{background:var(--s1);border:1px solid var(--bd);border-radius:18px;padding:20px;}
.q-num{font-size:10px;color:var(--ac);letter-spacing:2px;text-transform:uppercase;margin-bottom:8px;font-weight:700;}
.q-text{font-size:16px;font-weight:700;margin-bottom:16px;line-height:1.5;}
.q-text .blank{display:inline-block;min-width:80px;height:24px;background:rgba(124,111,255,.15);border-bottom:2px solid var(--ac);border-radius:4px 4px 0 0;vertical-align:middle;text-align:center;}
.q-opts{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:12px;}
.q-opt{background:var(--s2);border:1.5px solid var(--bd);border-radius:11px;padding:11px 14px;cursor:pointer;font-size:13px;text-align:center;transition:all .2s;font-family:'DM Sans',sans-serif;}
.q-opt:hover:not(.done){border-color:var(--ac);background:rgba(124,111,255,.08);}
.q-opt.correct{border-color:#3ee8a0;background:rgba(62,232,160,.12);color:#3ee8a0;font-weight:700;}
.q-opt.wrong{border-color:#ff6b8a;background:rgba(255,107,138,.1);color:#ff6b8a;}
.q-opt.done{cursor:default;}
.q-explain{background:rgba(62,232,160,.07);border:1px solid rgba(62,232,160,.2);border-radius:10px;padding:10px 13px;font-size:12px;color:#a0f0c8;margin-top:8px;display:none;}
.q-next-btn{background:linear-gradient(135deg,#7c6fff,#9c8fff);color:#fff;border:none;border-radius:11px;padding:12px 28px;font-family:'Unbounded',sans-serif;font-size:11px;font-weight:700;cursor:pointer;display:none;transition:all .2s;letter-spacing:.5px;}
.q-next-btn:hover{opacity:.88;transform:translateY(-1px);}
.q-fill-input{width:100%;background:var(--s2);border:1.5px solid var(--bd);border-radius:11px;padding:11px 14px;color:var(--tx);font-size:14px;font-family:'DM Sans',sans-serif;transition:border-color .2s;outline:none;}
.q-fill-input:focus{border-color:var(--ac);}
.q-fill-input.correct{border-color:#3ee8a0;background:rgba(62,232,160,.08);}
.q-fill-input.wrong{border-color:#ff6b8a;background:rgba(255,107,138,.08);}
.q-submit-btn{background:var(--ac);color:#fff;border:none;border-radius:10px;padding:10px 20px;font-family:'DM Sans',sans-serif;font-size:13px;font-weight:600;cursor:pointer;margin-top:8px;transition:all .2s;}
.q-submit-btn:hover{opacity:.85;}

/* START TEST */
.start-test-btn{background:linear-gradient(135deg,#7c6fff,#ff6b8a);color:#fff;border:none;border-radius:14px;padding:15px 36px;font-family:'Unbounded',sans-serif;font-size:13px;font-weight:700;cursor:pointer;transition:all .25s;letter-spacing:.5px;box-shadow:0 8px 24px rgba(124,111,255,.35);}
.start-test-btn:hover{transform:translateY(-2px);box-shadow:0 12px 32px rgba(124,111,255,.45);}
.start-test-note{font-size:12px;color:var(--mt);margin-bottom:12px;}

/* RESULT */
.result-card{background:linear-gradient(135deg,#0f0f28,#1a1040);border:1px solid rgba(124,111,255,.3);border-radius:24px;padding:32px 24px;text-align:center;max-width:440px;margin:20px auto;}
.result-icon{font-size:56px;margin-bottom:8px;animation:bounce .6s cubic-bezier(.34,1.56,.64,1);}
@keyframes bounce{from{transform:scale(0)}to{transform:scale(1)}}
.result-score{font-family:'Unbounded',sans-serif;font-size:42px;font-weight:900;margin-bottom:4px;}
.result-score.pass{color:#3ee8a0;}
.result-score.fail{color:#ff6b8a;}
.result-msg{font-size:16px;font-weight:600;margin-bottom:8px;color:#b0a8ff;}
.result-detail{font-size:12px;color:var(--mt);margin-bottom:20px;line-height:1.7;}
.unlock-anim{background:linear-gradient(135deg,rgba(62,232,160,.12),rgba(124,111,255,.12));border:1px solid rgba(62,232,160,.3);border-radius:14px;padding:14px;margin-bottom:20px;position:relative;overflow:hidden;}
.unlock-glow{position:absolute;inset:0;background:radial-gradient(ellipse at center,rgba(62,232,160,.15),transparent);animation:glowPulse 1.5s ease-in-out infinite;}
@keyframes glowPulse{0%,100%{opacity:.3}50%{opacity:1}}
.unlock-text{font-family:'Unbounded',sans-serif;font-size:13px;font-weight:700;color:#3ee8a0;position:relative;z-index:1;}
.result-btns{display:flex;gap:8px;justify-content:center;flex-wrap:wrap;}
.rbtn{border:none;border-radius:11px;padding:11px 18px;font-family:'DM Sans',sans-serif;font-size:13px;font-weight:600;cursor:pointer;transition:all .2s;}
.rbtn.retry{background:rgba(124,111,255,.15);color:var(--ac);border:1px solid rgba(124,111,255,.3);}
.rbtn.retry:hover{background:rgba(124,111,255,.25);}
.rbtn.next{background:linear-gradient(135deg,#7c6fff,#3ee8a0);color:#fff;}
.rbtn.next:hover{opacity:.88;}
.rbtn.back{background:var(--s2);color:var(--mt);border:1px solid var(--bd);}

/* LEADERBOARD MODAL */
.lb-modal{display:none;position:fixed;inset:0;background:rgba(0,0,0,.9);backdrop-filter:blur(10px);z-index:1000;align-items:center;justify-content:center;padding:14px;}
.lb-modal.on{display:flex;}
.lb-inner{background:var(--s1);border:1px solid rgba(124,111,255,.3);border-radius:24px;padding:24px 20px;max-width:400px;width:100%;max-height:80vh;overflow-y:auto;animation:pi .3s cubic-bezier(.34,1.56,.64,1);}
.lb-top{display:flex;align-items:center;justify-content:space-between;margin-bottom:18px;}
.lb-heading{font-family:'Unbounded',sans-serif;font-size:15px;font-weight:900;color:#ffb347;}
.lb-close{background:var(--s2);border:1px solid var(--bd);color:var(--mt);border-radius:8px;padding:5px 12px;cursor:pointer;font-family:'DM Sans',sans-serif;font-size:12px;}
.lb-name-row{display:flex;gap:8px;margin-bottom:16px;}
.lb-name-in{flex:1;background:var(--s2);border:1px solid var(--bd);border-radius:10px;padding:9px 12px;color:var(--tx);font-size:13px;font-family:'DM Sans',sans-serif;outline:none;}
.lb-name-in:focus{border-color:var(--ac);}
.lb-save-btn{background:var(--ac);color:#fff;border:none;border-radius:10px;padding:9px 16px;font-family:'DM Sans',sans-serif;font-size:13px;font-weight:600;cursor:pointer;white-space:nowrap;}
.lb-entry{display:flex;align-items:center;gap:12px;padding:10px 12px;border-radius:12px;margin-bottom:6px;background:var(--s2);border:1px solid var(--bd);transition:all .2s;}
.lb-entry.me{border-color:rgba(124,111,255,.5);background:rgba(124,111,255,.08);}
.lb-rank{font-family:'Unbounded',sans-serif;font-size:14px;font-weight:900;min-width:28px;text-align:center;}
.lb-rank.gold{color:#ffd700;}
.lb-rank.silver{color:#c0c0c0;}
.lb-rank.bronze{color:#cd7f32;}
.lb-name{flex:1;font-size:13px;font-weight:600;}
.lb-xp{font-family:'Unbounded',sans-serif;font-size:12px;color:#7c6fff;font-weight:700;}
.lb-stars{font-size:12px;}
.lb-empty{text-align:center;color:var(--mt);font-size:13px;padding:20px;}

@media(max-width:460px){.q-opts{grid-template-columns:1fr;}.result-btns{flex-direction:column;}.ln-icon{width:40px;height:40px;font-size:18px;}}

</style>
</head>
<body>

<div class="hero">
  <div class="badge">&#127468;&#127463; Ingliz tili kursi &mdash; Offline</div>
  <h1>Inglizchani<br><span>bosqichma-bosqich</span><br>o'rgan</h1>
  <p>A1 &#8594; B1 &middot; O'zbek tilida &middot; Internetisiz ishlaydi</p>
</div>

<div class="snav">
  <button class="sbtn on" onclick="goS(0)">&#127968; Bosh sahifa</button>
  <button class="sbtn" onclick="goS(1)">1 &mdash; Alifbo</button>
  <button class="sbtn" onclick="goS(2)">2 &mdash; So'zlar</button>
  <button class="sbtn" onclick="goS(3)">3 &mdash; Grammatika</button>
  <button class="sbtn" onclick="goS(4)">4 &mdash; Suhbat</button>
  <button class="sbtn" onclick="goS(5)">5 &mdash; Keyingi level</button>
</div>

<div class="wrap">

<!-- S0 HOME -->
<div class="sec on" id="s0">
  <div class="ov">
    <div class="ovc" onclick="goS(1)"><div class="on2" style="color:#7c6fff">1</div><div class="ot">Boshlang'ich</div><div class="os">Alifbo &middot; Salomlashish</div></div>
    <div class="ovc" onclick="goS(2)"><div class="on2" style="color:#ff6b8a">2</div><div class="ot">So'zlar</div><div class="os">Sonlar &middot; Ranglar</div></div>
    <div class="ovc" onclick="goS(3)"><div class="on2" style="color:#3ee8a0">3</div><div class="ot">Grammatika</div><div class="os">To be &middot; Tenses</div></div>
    <div class="ovc" onclick="goS(4)"><div class="on2" style="color:#ffb347">4</div><div class="ot">Suhbat</div><div class="os">Do'kon &middot; Restoran</div></div>
    <div class="ovc" onclick="goS(5)"><div class="on2" style="color:#b0a8ff">5</div><div class="ot">Keyingi Level</div><div class="os">Past &middot; Future &middot; Modal</div></div>
  </div>
  <div class="card op">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(124,111,255,.12)">&#128161;</div>
      <div class="ct"><h3>Kursdan qanday foydalanish?</h3><p>Boshlash uchun o'qing</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <div class="gb">&#9989; <strong>Ketma-ket o'rganing</strong> &mdash; 1-bosqichdan boshlang</div>
      <div class="gb g">&#128266; <strong>Har bir harfni bosing</strong> &mdash; animatsiya va ovoz chiqadi</div>
      <div class="gb o">&#128241; <strong>Internetisiz ishlaydi</strong> &mdash; HTML faylni brauzerda oching</div>
    </div>
  </div>
</div>

<!-- S1 ALPHABET -->
<div class="sec" id="s1">
  <div class="card op">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(124,111,255,.15)">&#128292;</div>
      <div class="ct"><h3>Ingliz Alifbosi (A&ndash;Z)</h3><p>Har bir harfni bosing &rarr; animatsiya + ovoz</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb"><div class="agrid" id="agrid"></div></div>
  </div>
  <div class="card">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(255,107,138,.15)">&#128075;</div>
      <div class="ct"><h3>Salomlashish</h3><p>Birinchi iboralar</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <table class="wt">
        <tr><th>Inglizcha</th><th>Talaffuz</th><th>O'zbekcha</th></tr>
        <tr><td class="en">Hello <button class="spk" onclick="sp('Hello')">&#128266;</button></td><td class="pr">[heˈloʊ]</td><td class="uz">Salom</td></tr>
        <tr><td class="en">Hi <button class="spk" onclick="sp('Hi')">&#128266;</button></td><td class="pr">[haɪ]</td><td class="uz">Salom (norasmiy)</td></tr>
        <tr><td class="en">Good morning <button class="spk" onclick="sp('Good morning')">&#128266;</button></td><td class="pr">[gʊd ˈmɔːrnɪŋ]</td><td class="uz">Xayrli tong</td></tr>
        <tr><td class="en">Good afternoon <button class="spk" onclick="sp('Good afternoon')">&#128266;</button></td><td class="pr">[gʊd ˌæftərˈnuːn]</td><td class="uz">Xayrli kun</td></tr>
        <tr><td class="en">Good evening <button class="spk" onclick="sp('Good evening')">&#128266;</button></td><td class="pr">[gʊd ˈiːvnɪŋ]</td><td class="uz">Xayrli kech</td></tr>
        <tr><td class="en">Goodbye <button class="spk" onclick="sp('Goodbye')">&#128266;</button></td><td class="pr">[ˌgʊdˈbaɪ]</td><td class="uz">Xayr</td></tr>
        <tr><td class="en">How are you? <button class="spk" onclick="sp('How are you?')">&#128266;</button></td><td class="pr">[haʊ ɑːr juː]</td><td class="uz">Qandaysiz?</td></tr>
        <tr><td class="en">I'm fine, thank you <button class="spk" onclick="sp(&quot;I'm fine, thank you&quot;)">&#128266;</button></td><td class="pr">[aɪm faɪn θæŋk juː]</td><td class="uz">Yaxshi, rahmat</td></tr>
        <tr><td class="en">Nice to meet you <button class="spk" onclick="sp('Nice to meet you')">&#128266;</button></td><td class="pr">[naɪs tə miːt juː]</td><td class="uz">Tanishganimdan xursandman</td></tr>
        <tr><td class="en">See you later <button class="spk" onclick="sp('See you later')">&#128266;</button></td><td class="pr">[siː juː ˈleɪtər]</td><td class="uz">Ko'rishguncha</td></tr>
      </table>
    </div>
  </div>
  <div class="card">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(62,232,160,.15)">&#128587;</div>
      <div class="ct"><h3>O'zingni tanishtirish</h3><p>My name is... I am from...</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <table class="wt">
        <tr><th>Inglizcha</th><th>O'zbekcha</th></tr>
        <tr><td class="en">My name is Ali. <button class="spk" onclick="sp('My name is Ali.')">&#128266;</button></td><td class="uz">Mening ismim Ali.</td></tr>
        <tr><td class="en">I am from Uzbekistan. <button class="spk" onclick="sp('I am from Uzbekistan.')">&#128266;</button></td><td class="uz">Men O'zbekistondan.</td></tr>
        <tr><td class="en">I am 20 years old. <button class="spk" onclick="sp('I am 20 years old.')">&#128266;</button></td><td class="uz">Men 20 yoshdaman.</td></tr>
        <tr><td class="en">I am a student. <button class="spk" onclick="sp('I am a student.')">&#128266;</button></td><td class="uz">Men talabaman.</td></tr>
        <tr><td class="en">I live in Tashkent. <button class="spk" onclick="sp('I live in Tashkent.')">&#128266;</button></td><td class="uz">Men Toshkentda yashayman.</td></tr>
        <tr><td class="en">What is your name? <button class="spk" onclick="sp('What is your name?')">&#128266;</button></td><td class="uz">Ismingiz nima?</td></tr>
        <tr><td class="en">Where are you from? <button class="spk" onclick="sp('Where are you from?')">&#128266;</button></td><td class="uz">Qayerdansiz?</td></tr>
        <tr><td class="en">How old are you? <button class="spk" onclick="sp('How old are you?')">&#128266;</button></td><td class="uz">Nechanchi yoshdasiz?</td></tr>
      </table>
      <div class="sl">Namuna suhbat</div>
      <div class="dlg">
        <div class="bbl a"><div class="wh">A</div><div class="eg">Hello! My name is Sarah. What is your name?</div><div class="uz3">Salom! Mening ismim Sarah. Ismingiz nima?</div></div>
        <div class="bbl b"><div class="wh">B</div><div class="eg">Hi! My name is Ali. Nice to meet you!</div><div class="uz3">Salom! Mening ismim Ali. Tanishganimdan xursandman!</div></div>
        <div class="bbl a"><div class="wh">A</div><div class="eg">Where are you from?</div><div class="uz3">Qayerdansiz?</div></div>
        <div class="bbl b"><div class="wh">B</div><div class="eg">I am from Uzbekistan. And you?</div><div class="uz3">Men O'zbekistondan. Siz-chi?</div></div>
      </div>
    </div>
  </div>
</div>

<!-- S2 WORDS -->
<div class="sec" id="s2">
  <div class="card op">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(255,179,71,.15)">&#128290;</div>
      <div class="ct"><h3>Sonlar (1&ndash;100)</h3><p>Bosing va eshiting</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <div class="sl">1&ndash;20</div><div class="ngrid" id="ng1"></div>
      <div class="sl">O'nlar</div><div class="ngrid" id="ng2"></div>
    </div>
  </div>
  <div class="card">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(255,107,138,.15)">&#127912;</div>
      <div class="ct"><h3>Ranglar (Colors)</h3><p>Bosing va eshiting</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb"><div class="cgrid" id="clrg"></div></div>
  </div>
  <div class="card">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(124,111,255,.15)">&#128197;</div>
      <div class="ct"><h3>Hafta kunlari &amp; Oylar</h3><p>Days &amp; Months</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <div class="sl">Hafta kunlari</div>
      <table class="wt">
        <tr><th>Inglizcha</th><th>Talaffuz</th><th>O'zbekcha</th></tr>
        <tr><td class="en">Monday <button class="spk" onclick="sp('Monday')">&#128266;</button></td><td class="pr">[ˈmʌndeɪ]</td><td class="uz">Dushanba</td></tr>
        <tr><td class="en">Tuesday <button class="spk" onclick="sp('Tuesday')">&#128266;</button></td><td class="pr">[ˈtjuːzdeɪ]</td><td class="uz">Seshanba</td></tr>
        <tr><td class="en">Wednesday <button class="spk" onclick="sp('Wednesday')">&#128266;</button></td><td class="pr">[ˈwenzdeɪ]</td><td class="uz">Chorshanba</td></tr>
        <tr><td class="en">Thursday <button class="spk" onclick="sp('Thursday')">&#128266;</button></td><td class="pr">[ˈθɜːrzdeɪ]</td><td class="uz">Payshanba</td></tr>
        <tr><td class="en">Friday <button class="spk" onclick="sp('Friday')">&#128266;</button></td><td class="pr">[ˈfraɪdeɪ]</td><td class="uz">Juma</td></tr>
        <tr><td class="en">Saturday <button class="spk" onclick="sp('Saturday')">&#128266;</button></td><td class="pr">[ˈsætərdeɪ]</td><td class="uz">Shanba</td></tr>
        <tr><td class="en">Sunday <button class="spk" onclick="sp('Sunday')">&#128266;</button></td><td class="pr">[ˈsʌndeɪ]</td><td class="uz">Yakshanba</td></tr>
      </table>
      <div class="sl">Oylar</div>
      <table class="wt">
        <tr><th>Inglizcha</th><th>O'zbek</th><th>Inglizcha</th><th>O'zbek</th></tr>
        <tr><td class="en">January</td><td class="uz">Yanvar</td><td class="en">July</td><td class="uz">Iyul</td></tr>
        <tr><td class="en">February</td><td class="uz">Fevral</td><td class="en">August</td><td class="uz">Avgust</td></tr>
        <tr><td class="en">March</td><td class="uz">Mart</td><td class="en">September</td><td class="uz">Sentyabr</td></tr>
        <tr><td class="en">April</td><td class="uz">Aprel</td><td class="en">October</td><td class="uz">Oktyabr</td></tr>
        <tr><td class="en">May</td><td class="uz">May</td><td class="en">November</td><td class="uz">Noyabr</td></tr>
        <tr><td class="en">June</td><td class="uz">Iyun</td><td class="en">December</td><td class="uz">Dekabr</td></tr>
      </table>
    </div>
  </div>
  <div class="card">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(62,232,160,.15)">&#128106;</div>
      <div class="ct"><h3>Oila a'zolari</h3><p>Family members</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <table class="wt">
        <tr><th>Inglizcha</th><th>Talaffuz</th><th>O'zbekcha</th></tr>
        <tr><td class="en">Mother / Mom <button class="spk" onclick="sp('Mother')">&#128266;</button></td><td class="pr">[ˈmʌðər]</td><td class="uz">Ona</td></tr>
        <tr><td class="en">Father / Dad <button class="spk" onclick="sp('Father')">&#128266;</button></td><td class="pr">[ˈfɑːðər]</td><td class="uz">Ota</td></tr>
        <tr><td class="en">Brother <button class="spk" onclick="sp('Brother')">&#128266;</button></td><td class="pr">[ˈbrʌðər]</td><td class="uz">Aka / Uka</td></tr>
        <tr><td class="en">Sister <button class="spk" onclick="sp('Sister')">&#128266;</button></td><td class="pr">[ˈsɪstər]</td><td class="uz">Opa / Singil</td></tr>
        <tr><td class="en">Son <button class="spk" onclick="sp('Son')">&#128266;</button></td><td class="pr">[sʌn]</td><td class="uz">O'g'il</td></tr>
        <tr><td class="en">Daughter <button class="spk" onclick="sp('Daughter')">&#128266;</button></td><td class="pr">[ˈdɔːtər]</td><td class="uz">Qiz</td></tr>
        <tr><td class="en">Grandfather <button class="spk" onclick="sp('Grandfather')">&#128266;</button></td><td class="pr">[ˈɡrændˌfɑːðər]</td><td class="uz">Bobo</td></tr>
        <tr><td class="en">Grandmother <button class="spk" onclick="sp('Grandmother')">&#128266;</button></td><td class="pr">[ˈɡrændˌmʌðər]</td><td class="uz">Buvi</td></tr>
        <tr><td class="en">Husband <button class="spk" onclick="sp('Husband')">&#128266;</button></td><td class="pr">[ˈhʌzbənd]</td><td class="uz">Er</td></tr>
        <tr><td class="en">Wife <button class="spk" onclick="sp('Wife')">&#128266;</button></td><td class="pr">[waɪf]</td><td class="uz">Xotin</td></tr>
      </table>
    </div>
  </div>
  <div class="card">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(255,107,138,.15)">&#128188;</div>
      <div class="ct"><h3>Kasblar (Jobs)</h3><p>Mini test bilan!</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <table class="wt">
        <tr><th>Inglizcha</th><th>Talaffuz</th><th>O'zbekcha</th></tr>
        <tr><td class="en">Doctor <button class="spk" onclick="sp('Doctor')">&#128266;</button></td><td class="pr">[ˈdɒktər]</td><td class="uz">Shifokor</td></tr>
        <tr><td class="en">Teacher <button class="spk" onclick="sp('Teacher')">&#128266;</button></td><td class="pr">[ˈtiːtʃər]</td><td class="uz">O'qituvchi</td></tr>
        <tr><td class="en">Student <button class="spk" onclick="sp('Student')">&#128266;</button></td><td class="pr">[ˈstjuːdənt]</td><td class="uz">Talaba</td></tr>
        <tr><td class="en">Engineer <button class="spk" onclick="sp('Engineer')">&#128266;</button></td><td class="pr">[ˌendʒɪˈnɪər]</td><td class="uz">Muhandis</td></tr>
        <tr><td class="en">Lawyer <button class="spk" onclick="sp('Lawyer')">&#128266;</button></td><td class="pr">[ˈlɔːjər]</td><td class="uz">Huquqshunos</td></tr>
        <tr><td class="en">Driver <button class="spk" onclick="sp('Driver')">&#128266;</button></td><td class="pr">[ˈdraɪvər]</td><td class="uz">Haydovchi</td></tr>
        <tr><td class="en">Chef <button class="spk" onclick="sp('Chef')">&#128266;</button></td><td class="pr">[ʃef]</td><td class="uz">Oshpaz</td></tr>
        <tr><td class="en">Programmer <button class="spk" onclick="sp('Programmer')">&#128266;</button></td><td class="pr">[ˈproʊɡræmər]</td><td class="uz">Dasturchi</td></tr>
        <tr><td class="en">Police officer <button class="spk" onclick="sp('Police officer')">&#128266;</button></td><td class="pr">[pəˈliːs ˈɒfɪsər]</td><td class="uz">Politsiyachi</td></tr>
        <tr><td class="en">Nurse <button class="spk" onclick="sp('Nurse')">&#128266;</button></td><td class="pr">[nɜːrs]</td><td class="uz">Hamshira</td></tr>
      </table>
      <div class="qa">
        <div class="qq">&#129513; MINI TEST &mdash; Kasblar</div>
        <div class="qqt" id="qjq">...</div>
        <div class="qo" id="qjo"></div>
        <button class="qnxt" id="qjn" onclick="nxtQ()">Keyingi &#9654;</button>
        <div class="qsc" id="qjs"></div>
      </div>
    </div>
  </div>
</div>

<!-- S3 GRAMMAR — ENHANCED -->
<div class="sec" id="s3">

  <div class="gram-hero" id="gram-hero-wrap">
    <div class="gram-hero-inner">
      <div class="gram-title-row">
        <span class="gram-badge">🎮 GRAMMAR QUEST</span>
        <button class="lb-open-btn" onclick="openLeaderboard()">🏆 Reyting</button>
      </div>
      <h2 class="gram-h2">Grammatika <span>bosqichlari</span></h2>
      <p class="gram-sub">Har bir darsni o'rgan → test topshir → keyingi darajani oching</p>
      <div class="xp-bar-wrap"><div class="xp-bar-inner" id="xpBar" style="width:0%"></div></div>
      <div class="xp-label" id="xpLabel">XP: 0 / 700</div>
    </div>
  </div>

  <div class="lesson-road" id="lessonRoad"></div>
  <div id="lessonPanel" style="display:none">
    <div class="lp-header">
      <button class="lp-back" onclick="closeLessonPanel()">← Orqaga</button>
      <div class="lp-title-wrap">
        <span class="lp-icon" id="lpIcon">📘</span>
        <div><div class="lp-title" id="lpTitle">Dars</div><div class="lp-sub" id="lpSub">Easy</div></div>
      </div>
      <div class="lp-diff" id="lpDiff">A1</div>
    </div>
    <div id="lpContent"></div>
    <div id="startTestWrap" style="text-align:center;margin:28px 0 8px">
      <div class="start-test-note" id="startTestNote"></div>
      <button class="start-test-btn" id="startTestBtn" onclick="startTest()">✏️ Testni boshlash</button>
    </div>
  </div>

  <div id="testPanel" style="display:none">
    <div class="lp-header">
      <button class="lp-back" onclick="backToLesson()">← Darsga qaytish</button>
      <div class="lp-title-wrap">
        <span class="lp-icon">✏️</span>
        <div><div class="lp-title" id="tpTitle">Test</div><div class="lp-sub" id="tpSub">Savollar</div></div>
      </div>
      <div class="tp-score-chip" id="tpChip">0/0</div>
    </div>
    <div class="tp-progress-wrap"><div class="tp-progress-bar" id="tpBar" style="width:0%"></div></div>
    <div id="tpContent"></div>
  </div>

  <div id="resultPanel" style="display:none">
    <div class="result-card" id="resultCard">
      <div class="result-icon" id="resultIcon">🎉</div>
      <div class="result-score" id="resultScore">85/100</div>
      <div class="result-msg" id="resultMsg">Ajoyib!</div>
      <div class="result-detail" id="resultDetail"></div>
      <div id="unlockAnim" class="unlock-anim" style="display:none">
        <div class="unlock-glow"></div>
        <div class="unlock-text">🔓 Yangi dars ochildi!</div>
      </div>
      <div class="result-btns">
        <button class="rbtn retry" onclick="retryTest()">🔁 Qayta urinish</button>
        <button class="rbtn next" id="rNextBtn" onclick="goNextLesson()" style="display:none">▶ Keyingi dars →</button>
        <button class="rbtn back" onclick="closeLessonPanel()">🏠 Xaritaga</button>
      </div>
    </div>
  </div>

</div>

<!-- S4 CONVERSATION -->
<div class="sec" id="s4">
  <div class="card op">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(255,179,71,.15)">&#128717;</div>
      <div class="ct"><h3>Do'konda suhbat</h3><p>Shopping conversation</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <div class="dlg">
        <div class="bbl a"><div class="wh">Sotuvchi</div><div class="eg">Can I help you? <button class="spk" onclick="sp('Can I help you?')">&#128266;</button></div><div class="uz3">Sizga yordam bera olamanmi?</div></div>
        <div class="bbl b"><div class="wh">Mijoz</div><div class="eg">Yes, I'm looking for a jacket.</div><div class="uz3">Ha, men kurtka qidirmoqdaman.</div></div>
        <div class="bbl a"><div class="wh">Sotuvchi</div><div class="eg">What size do you need?</div><div class="uz3">Qanday o'lcham kerak?</div></div>
        <div class="bbl b"><div class="wh">Mijoz</div><div class="eg">Medium, please. How much is it?</div><div class="uz3">O'rta. Narxi necha?</div></div>
        <div class="bbl a"><div class="wh">Sotuvchi</div><div class="eg">It's fifty dollars.</div><div class="uz3">Ellik dollar.</div></div>
        <div class="bbl b"><div class="wh">Mijoz</div><div class="eg">I'll take it. Thank you!</div><div class="uz3">Olaman. Rahmat!</div></div>
      </div>
      <div class="sl">Foydali so'zlar</div>
      <table class="wt">
        <tr><th>Inglizcha</th><th>O'zbekcha</th></tr>
        <tr><td class="en">How much is this? <button class="spk" onclick="sp('How much is this?')">&#128266;</button></td><td class="uz">Bu qancha turadi?</td></tr>
        <tr><td class="en">That's too expensive.</td><td class="uz">Bu juda qimmat.</td></tr>
        <tr><td class="en">Do you have a discount?</td><td class="uz">Chegirma bormi?</td></tr>
        <tr><td class="en">I'll pay by card.</td><td class="uz">Karta bilan to'layman.</td></tr>
        <tr><td class="en">Can I try this on?</td><td class="uz">Kiyib ko'rsam bo'ladimi?</td></tr>
      </table>
    </div>
  </div>
  <div class="card">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(255,107,138,.15)">&#127869;</div>
      <div class="ct"><h3>Restoranda suhbat</h3><p>At a restaurant</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <div class="dlg">
        <div class="bbl a"><div class="wh">Ofitsiant</div><div class="eg">Good evening! Do you have a reservation?</div><div class="uz3">Xayrli kech! Buyurtmangiz bormi?</div></div>
        <div class="bbl b"><div class="wh">Mehmon</div><div class="eg">No, but we'd like a table for two.</div><div class="uz3">Yo'q, lekin ikki kishilik stol kerak.</div></div>
        <div class="bbl a"><div class="wh">Ofitsiant</div><div class="eg">Of course! Here is the menu.</div><div class="uz3">Albatta! Mana menyu.</div></div>
        <div class="bbl b"><div class="wh">Mehmon</div><div class="eg">I'd like chicken soup and rice, please.</div><div class="uz3">Menga tovuq sho'rva va guruch bering.</div></div>
        <div class="bbl a"><div class="wh">Ofitsiant</div><div class="eg">And to drink?</div><div class="uz3">Ichimlik-chi?</div></div>
        <div class="bbl b"><div class="wh">Mehmon</div><div class="eg">Water, please. And the bill at the end.</div><div class="uz3">Suv iltimos. Va oxirida hisob-kitob.</div></div>
      </div>
    </div>
  </div>
  <div class="card">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(62,232,160,.15)">&#128506;</div>
      <div class="ct"><h3>Yo'l so'rash</h3><p>Asking for directions</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <table class="wt">
        <tr><th>Inglizcha</th><th>O'zbekcha</th></tr>
        <tr><td class="en">Excuse me, where is the hospital? <button class="spk" onclick="sp('Excuse me, where is the hospital?')">&#128266;</button></td><td class="uz">Kechirasiz, kasalxona qayerda?</td></tr>
        <tr><td class="en">Go straight. <button class="spk" onclick="sp('Go straight.')">&#128266;</button></td><td class="uz">To'g'ri boring.</td></tr>
        <tr><td class="en">Turn left. <button class="spk" onclick="sp('Turn left.')">&#128266;</button></td><td class="uz">Chapga buriling.</td></tr>
        <tr><td class="en">Turn right. <button class="spk" onclick="sp('Turn right.')">&#128266;</button></td><td class="uz">O'ngga buriling.</td></tr>
        <tr><td class="en">It's near / far.</td><td class="uz">U yaqin / uzoq.</td></tr>
        <tr><td class="en">About 5 minutes on foot.</td><td class="uz">Piyoda taxminan 5 daqiqa.</td></tr>
      </table>
    </div>
  </div>
  <div class="card">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(124,111,255,.15)">&#128222;</div>
      <div class="ct"><h3>Telefon suhbatlari</h3><p>Phone conversations</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <table class="wt">
        <tr><th>Inglizcha</th><th>O'zbekcha</th></tr>
        <tr><td class="en">Hello, this is Ali speaking. <button class="spk" onclick="sp('Hello, this is Ali speaking.')">&#128266;</button></td><td class="uz">Allo, bu Ali gapiryapti.</td></tr>
        <tr><td class="en">Can I speak to Sara, please?</td><td class="uz">Sara bilan gaplashsam bo'ladimi?</td></tr>
        <tr><td class="en">Hold on, please.</td><td class="uz">Bir daqiqa kuting.</td></tr>
        <tr><td class="en">I'll call back later.</td><td class="uz">Keyinroq qayta qo'ng'iroq qilaman.</td></tr>
        <tr><td class="en">Wrong number, sorry!</td><td class="uz">Noto'g'ri raqam, kechirasiz!</td></tr>
      </table>
    </div>
  </div>
  <div class="card">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(255,107,138,.15)">&#10067;</div>
      <div class="ct"><h3>Savol so'zlari</h3><p>What, Where, When, Why, How...</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <table class="wt">
        <tr><th>So'z</th><th>Tarjima</th><th>Misol</th></tr>
        <tr><td class="en">What?</td><td class="uz">Nima?</td><td class="en">What is your job?</td></tr>
        <tr><td class="en">Where?</td><td class="uz">Qayerda?</td><td class="en">Where do you live?</td></tr>
        <tr><td class="en">When?</td><td class="uz">Qachon?</td><td class="en">When is your birthday?</td></tr>
        <tr><td class="en">Why?</td><td class="uz">Nima uchun?</td><td class="en">Why are you sad?</td></tr>
        <tr><td class="en">Who?</td><td class="uz">Kim?</td><td class="en">Who is that man?</td></tr>
        <tr><td class="en">How?</td><td class="uz">Qanday?</td><td class="en">How do you feel?</td></tr>
        <tr><td class="en">How much?</td><td class="uz">Qancha?</td><td class="en">How much does it cost?</td></tr>
        <tr><td class="en">How many?</td><td class="uz">Nechta?</td><td class="en">How many students?</td></tr>
      </table>
    </div>
  </div>
</div>

<!-- S5 NEXT LEVEL -->
<div class="sec" id="s5">
  <div class="card op">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(124,111,255,.15)">&#9194;</div>
      <div class="ct"><h3>Past Simple &mdash; O'tgan zamon</h3><p>Tugagan harakatlar</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <div class="gb"><strong>Tuzilishi:</strong> Subject + fe'l<strong>-ed</strong> yoki irregular 2-shakl</div>
      <table class="wt">
        <tr><th>Shakl</th><th>Misol</th><th>Tarjima</th></tr>
        <tr><td><span class="tag">&#9989;</span></td><td class="en">I worked yesterday.</td><td class="uz">Men kecha ishladim.</td></tr>
        <tr><td><span class="tag r">&#10060;</span></td><td class="en">I didn't work yesterday.</td><td class="uz">Men kecha ishlamadim.</td></tr>
        <tr><td><span class="tag g">&#10067;</span></td><td class="en">Did you work yesterday?</td><td class="uz">Kecha ishladingizmi?</td></tr>
      </table>
      <div class="sl">Notartibli fe'llar (Irregular verbs)</div>
      <table class="wt">
        <tr><th>Hozirgi</th><th>O'tgani</th><th>Tarjima</th></tr>
        <tr><td class="en">go</td><td class="en">went</td><td class="uz">bormoq</td></tr>
        <tr><td class="en">come</td><td class="en">came</td><td class="uz">kelmoq</td></tr>
        <tr><td class="en">see</td><td class="en">saw</td><td class="uz">ko'rmoq</td></tr>
        <tr><td class="en">eat</td><td class="en">ate</td><td class="uz">yemoq</td></tr>
        <tr><td class="en">drink</td><td class="en">drank</td><td class="uz">ichmoq</td></tr>
        <tr><td class="en">buy</td><td class="en">bought</td><td class="uz">sotib olmoq</td></tr>
        <tr><td class="en">say</td><td class="en">said</td><td class="uz">demoq</td></tr>
        <tr><td class="en">make</td><td class="en">made</td><td class="uz">yasamoq</td></tr>
        <tr><td class="en">take</td><td class="en">took</td><td class="uz">olmoq</td></tr>
        <tr><td class="en">get</td><td class="en">got</td><td class="uz">olmoq / bo'lmoq</td></tr>
      </table>
    </div>
  </div>
  <div class="card">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(62,232,160,.15)">&#9193;</div>
      <div class="ct"><h3>Future Simple &mdash; Kelasi zamon</h3><p>will bilan kelajak</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <div class="gb g"><strong>Tuzilishi:</strong> Subject + <strong>will</strong> + fe'l &mdash; Barcha shaxslar uchun bir xil!</div>
      <table class="wt">
        <tr><th>Shakl</th><th>Misol</th><th>Tarjima</th></tr>
        <tr><td><span class="tag">&#9989;</span></td><td class="en">I will call you tomorrow.</td><td class="uz">Ertaga qo'ng'iroq qilaman.</td></tr>
        <tr><td><span class="tag r">&#10060;</span></td><td class="en">She won't come today.</td><td class="uz">U bugun kelmaydi.</td></tr>
        <tr><td><span class="tag g">&#10067;</span></td><td class="en">Will you help me?</td><td class="uz">Menga yordam berasizmi?</td></tr>
      </table>
      <div class="gb o"><strong>will not = won't</strong> &nbsp;|&nbsp; I will = I'll &nbsp;|&nbsp; She will = She'll</div>
    </div>
  </div>
  <div class="card">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(255,107,138,.15)">&#127919;</div>
      <div class="ct"><h3>Modal Verbs</h3><p>can &middot; should &middot; must</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <table class="wt">
        <tr><th>Modal</th><th>Ma'no</th><th>Misol</th><th>Tarjima</th></tr>
        <tr><td class="en">can</td><td class="uz">imkoniyat</td><td class="en">I can swim.</td><td class="uz">Men suza olaman.</td></tr>
        <tr><td class="en">can't</td><td class="uz">imkonsizlik</td><td class="en">He can't drive.</td><td class="uz">U hayday olmaydi.</td></tr>
        <tr><td class="en">should</td><td class="uz">maslahat</td><td class="en">You should sleep early.</td><td class="uz">Erta uxlashingiz kerak.</td></tr>
        <tr><td class="en">shouldn't</td><td class="uz">kerak emas</td><td class="en">You shouldn't smoke.</td><td class="uz">Chekmasligingiz kerak.</td></tr>
        <tr><td class="en">must</td><td class="uz">majburiyat</td><td class="en">You must wear a seatbelt.</td><td class="uz">Kamar taqish shart.</td></tr>
        <tr><td class="en">mustn't</td><td class="uz">man etilgan</td><td class="en">You mustn't smoke here.</td><td class="uz">Bu yerda chekish mumkin emas.</td></tr>
      </table>
    </div>
  </div>
  <div class="card">
    <div class="ch" onclick="tc(this)">
      <div class="ci" style="background:rgba(255,179,71,.15)">&#128202;</div>
      <div class="ct"><h3>Comparison &mdash; Taqqoslash</h3><p>big &rarr; bigger &rarr; biggest</p></div>
      <span class="ti">&#9660;</span>
    </div>
    <div class="cb">
      <table class="wt">
        <tr><th>Asl</th><th>Qiyosiy</th><th>Orttirma</th><th>Tarjima</th></tr>
        <tr><td class="en">big</td><td class="en">bigger</td><td class="en">the biggest</td><td class="uz">katta / kattaroq / eng katta</td></tr>
        <tr><td class="en">small</td><td class="en">smaller</td><td class="en">the smallest</td><td class="uz">kichik / kichikroq / eng kichik</td></tr>
        <tr><td class="en">fast</td><td class="en">faster</td><td class="en">the fastest</td><td class="uz">tez / tezroq / eng tez</td></tr>
        <tr><td class="en">good</td><td class="en">better</td><td class="en">the best</td><td class="uz">yaxshi / yaxshiroq / eng yaxshi</td></tr>
        <tr><td class="en">bad</td><td class="en">worse</td><td class="en">the worst</td><td class="uz">yomon / yomonroq / eng yomon</td></tr>
        <tr><td class="en">beautiful</td><td class="en">more beautiful</td><td class="en">the most beautiful</td><td class="uz">chiroyli / chiroliroq / eng chiroyli</td></tr>
        <tr><td class="en">expensive</td><td class="en">more expensive</td><td class="en">the most expensive</td><td class="uz">qimmat / qimmatroq / eng qimmat</td></tr>
      </table>
      <div class="gb">&#128207; <strong>Qisqa (1 bo'g'in):</strong> + er/est &rarr; big<strong>ger</strong>, bigg<strong>est</strong></div>
      <div class="gb g">&#128208; <strong>Uzun (2+ bo'g'in):</strong> more/most + sifat &rarr; <strong>more</strong> beautiful</div>
      <div class="ex"><div class="eg">My car is <strong>faster than</strong> your car.</div><div class="uz2">Mening mashinam siznikidan tezroq.</div></div>
      <div class="ex"><div class="eg">This is <strong>the best</strong> restaurant in the city.</div><div class="uz2">Bu shahardagi eng yaxshi restoran.</div></div>
    </div>
  </div>
</div>

</div><!-- /wrap -->

<!-- LETTER MODAL -->
<div class="mo" id="lmo" onclick="closeMo(event)">
  <div class="mi" id="lmi">
    <div class="cw"><canvas id="lc" width="480" height="480"></canvas></div>
    <div class="pbw"><div class="pbi" id="pb"></div></div>
    <div class="cc2">
      <button class="cb2" id="pbtn" onclick="togAnim()">&#9654; Ijro</button>
      <button class="cb2" onclick="reAnim()">&#8635; Qayta</button>
    </div>
    <div class="ml" id="mlt">A a</div>
    <div class="mp" id="mpr">[eɪ]</div>
    <div class="me" id="mex">Apple, Ant, Air</div>
    <div class="wr" id="mwr"></div>
    <button class="spkb" onclick="spkNow()">&#128266; Ovozini eshitish</button>
    <button class="cls" onclick="closeMo()">&#10005; Yopish</button>
  </div>
</div>


<!-- LEADERBOARD MODAL -->
<div class="lb-modal" id="lbModal" onclick="if(event.target===this)closeLeaderboard()">
  <div class="lb-inner">
    <div class="lb-top">
      <div class="lb-heading">🏆 Global Reyting</div>
      <button class="lb-close" onclick="closeLeaderboard()">✕ Yopish</button>
    </div>
    <div style="font-size:12px;color:var(--mt);margin-bottom:10px">Ismingizni kiriting va natijangizni global reytingga saqlang!</div>
    <div class="lb-name-row">
      <input class="lb-name-in" id="lbNameIn" placeholder="Ismingizni kiriting..." maxlength="20">
      <button class="lb-save-btn" onclick="saveToLeaderboard()">Saqlash</button>
    </div>
    <div id="lbList"></div>
  </div>
</div>
<script>

/* ===================== DATA ===================== */
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

/* ===================== SPEECH ===================== */
var synth = window.speechSynthesis;
var voices = [];

function loadVoices(){
  voices = synth.getVoices();
}
if(synth){
  loadVoices();
  synth.onvoiceschanged = loadVoices;
}

function sp(txt){
  if(!synth) return;
  synth.cancel();
  var u = new SpeechSynthesisUtterance(txt);
  u.lang = 'en-US';
  u.rate = 0.82;
  u.pitch = 1.05;
  u.volume = 1.0;
  // Pick best English voice
  var enVoice = voices.find(function(v){ return v.lang === 'en-US' && v.localService; }) ||
                voices.find(function(v){ return v.lang.startsWith('en'); });
  if(enVoice) u.voice = enVoice;
  synth.speak(u);
}

function spkNow(){
  if(curD) sp(curD.l);
}

/* ===================== CANVAS ANIMATION ===================== */
var cvs = document.getElementById('lc');
var cx = cvs.getContext('2d');
var W=480, H=480;
var animT=0, animDur=150, animRaf=null, animOn=false;
var curD=null;

function drawFrame(t,d){
  cx.clearRect(0,0,W,H);
  // Dark bg
  cx.fillStyle='#0f0f1e';
  cx.fillRect(0,0,W,H);
  // Pulsing rings
  for(var i=0;i<4;i++){
    var ph=((t/animDur)+i*0.25)%1;
    var r=60+ph*200;
    var al=(1-ph)*0.3;
    cx.beginPath();
    cx.arc(W/2,H/2,r,0,Math.PI*2);
    var hexA=Math.floor(al*255).toString(16).padStart(2,'0');
    cx.strokeStyle=d.c+hexA;
    cx.lineWidth=2;
    cx.stroke();
  }
  // Orbiting dots
  for(var j=0;j<8;j++){
    var ang=(j/8)*Math.PI*2 + t*0.05;
    var or=160+Math.sin(t*0.07+j)*15;
    var px=W/2+Math.cos(ang)*or;
    var py=H/2+Math.sin(ang)*or;
    cx.beginPath();
    cx.arc(px,py,3+Math.sin(t*0.1+j)*1.5,0,Math.PI*2);
    cx.fillStyle=d.c;
    cx.globalAlpha=0.65;
    cx.fill();
    cx.globalAlpha=1;
  }
  // Glow
  var g=cx.createRadialGradient(W/2,H/2,0,W/2,H/2,140);
  g.addColorStop(0,d.c+'44');
  g.addColorStop(1,'transparent');
  cx.fillStyle=g;
  cx.fillRect(0,0,W,H);
  // Letter scale-in
  var prog=Math.min(t/20,1);
  var ease=1-Math.pow(1-prog,3);
  var sc=(0.2+ease*0.8)*(1+Math.sin(t*0.07)*0.025);
  cx.save();
  cx.translate(W/2,H/2+10);
  cx.scale(sc,sc);
  cx.shadowColor=d.c;
  cx.shadowBlur=25+Math.sin(t*0.05)*8;
  // Gradient fill
  var lg=cx.createLinearGradient(-80,-100,80,100);
  lg.addColorStop(0,'#ffffff');
  lg.addColorStop(0.5,d.c);
  lg.addColorStop(1,'#ffffffaa');
  cx.font='900 190px Unbounded,sans-serif';
  cx.textAlign='center';
  cx.textBaseline='middle';
  cx.fillStyle=lg;
  cx.fillText(d.l,0,0);
  cx.shadowBlur=0;
  cx.restore();
  // Small lowercase
  var sp2=Math.min(Math.max(t-10,0)/18,1);
  cx.globalAlpha=sp2;
  cx.font='500 46px Unbounded,sans-serif';
  cx.textAlign='center';
  cx.fillStyle='#ffffff55';
  cx.fillText(d.l.toLowerCase(),W/2,H/2+118);
  cx.globalAlpha=1;
  // Spark burst at start
  if(t<25){
    for(var k=0;k<8;k++){
      var sa=(k/8)*Math.PI*2;
      var sr=t*6;
      cx.beginPath();
      cx.arc(W/2+Math.cos(sa)*sr,H/2+Math.sin(sa)*sr,3,0,Math.PI*2);
      cx.fillStyle=d.c;
      cx.globalAlpha=(1-t/25)*0.9;
      cx.fill();
      cx.globalAlpha=1;
    }
  }
  // Progress bar
  document.getElementById('pb').style.width=Math.min((t/animDur)*100,100)+'%';
}

function animLoop(){
  if(!animOn) return;
  animT++;
  drawFrame(animT,curD);
  if(animT<animDur){
    animRaf=requestAnimationFrame(animLoop);
  } else {
    animOn=false;
    var pb=document.getElementById('pbtn');
    pb.textContent='\u25B6 Ijro';
    pb.classList.remove('pl');
  }
}

function startAnim(){
  if(animRaf) cancelAnimationFrame(animRaf);
  animT=0; animOn=true;
  var pb=document.getElementById('pbtn');
  pb.textContent='\u23F8 To\'xtat';
  pb.classList.add('pl');
  animLoop();
  setTimeout(function(){ sp(curD.l); }, 350);
}

function togAnim(){
  if(animOn){
    animOn=false;
    if(animRaf) cancelAnimationFrame(animRaf);
    var pb=document.getElementById('pbtn');
    pb.textContent='\u25B6 Ijro';
    pb.classList.remove('pl');
  } else {
    if(animT>=animDur) animT=0;
    animOn=true;
    var pb=document.getElementById('pbtn');
    pb.textContent='\u23F8 To\'xtat';
    pb.classList.add('pl');
    animLoop();
  }
}

function reAnim(){ startAnim(); }

/* ===================== MODAL ===================== */
function openMo(d){
  curD=d;
  document.getElementById('mlt').textContent=d.l+' '+d.l.toLowerCase();
  document.getElementById('mpr').textContent=d.p;
  document.getElementById('mex').textContent='Misollar: '+d.ex;
  var wr=document.getElementById('mwr');
  wr.innerHTML='';
  d.w.forEach(function(word){
    var pill=document.createElement('div');
    pill.className='wp';
    pill.textContent=word;
    pill.onclick=function(){ sp(word); };
    wr.appendChild(pill);
  });
  document.getElementById('lmo').classList.add('on');
  document.body.style.overflow='hidden';
  drawFrame(0,d);
  setTimeout(startAnim,150);
}

function closeMo(e){
  if(e && e.target!==document.getElementById('lmo')) return;
  document.getElementById('lmo').classList.remove('on');
  document.body.style.overflow='';
  animOn=false;
  if(animRaf) cancelAnimationFrame(animRaf);
  synth && synth.cancel();
}

/* ===================== BUILD ALPHABET ===================== */
function buildAlpha(){
  var g=document.getElementById('agrid');
  AD.forEach(function(d){
    var c=document.createElement('div');
    c.className='alc';
    c.style.borderColor=d.c+'44';
    c.innerHTML='<div class="bl" style="color:'+d.c+'">'+d.l+'</div>'
               +'<div class="sl">'+d.p+'</div>'
               +'<div class="hl">&#9654; bosing</div>';
    c.onclick=function(){ openMo(d); };
    g.appendChild(c);
  });
}

/* ===================== NUMBERS ===================== */
var N20=[[1,'one'],[2,'two'],[3,'three'],[4,'four'],[5,'five'],[6,'six'],[7,'seven'],[8,'eight'],[9,'nine'],[10,'ten'],[11,'eleven'],[12,'twelve'],[13,'thirteen'],[14,'fourteen'],[15,'fifteen'],[16,'sixteen'],[17,'seventeen'],[18,'eighteen'],[19,'nineteen'],[20,'twenty']];
var N10=[[20,'twenty'],[30,'thirty'],[40,'forty'],[50,'fifty'],[60,'sixty'],[70,'seventy'],[80,'eighty'],[90,'ninety'],[100,'one hundred']];
function buildNums(){
  var g1=document.getElementById('ng1');
  var g2=document.getElementById('ng2');
  N20.forEach(function(x){
    var c=document.createElement('div');c.className='nc';
    c.innerHTML='<span class="n">'+x[0]+'</span><span>'+x[1]+'</span>';
    c.onclick=function(){ sp(x[1]); };
    g1.appendChild(c);
  });
  N10.forEach(function(x){
    var c=document.createElement('div');c.className='nc';
    c.innerHTML='<span class="n">'+x[0]+'</span><span>'+x[1]+'</span>';
    c.onclick=function(){ sp(x[1]); };
    g2.appendChild(c);
  });
}

/* ===================== COLORS ===================== */
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
function buildColors(){
  var g=document.getElementById('clrg');
  CLR.forEach(function(c){
    var el=document.createElement('div');
    el.className='cc';
    el.style.background=c.bg;
    el.style.display='flex';
    el.style.flexDirection='column';
    el.style.gap='3px';
    el.innerHTML='<span style="font-weight:700;color:'+c.fg+';font-size:14px">'+c.en+'</span>'
                +'<span style="font-size:11px;opacity:.75;color:'+c.fg+'">'+c.uz+'</span>';
    el.onclick=function(){ sp(c.en); };
    g.appendChild(el);
  });
}

/* ===================== QUIZ ===================== */
var QD=[
  {q:'Who treats sick people?',o:['Teacher','Doctor','Driver','Cook'],a:1},
  {q:'Who drives a car for work?',o:['Nurse','Lawyer','Driver','Engineer'],a:2},
  {q:'Who teaches students?',o:['Teacher','Doctor','Chef','Programmer'],a:0},
  {q:'Who writes code?',o:['Lawyer','Police officer','Chef','Programmer'],a:3},
  {q:'"Hamshira" inglizcha nima?',o:['Doctor','Nurse','Cook','Teacher'],a:1},
  {q:'"Oshpaz" inglizcha nima?',o:['Driver','Engineer','Chef','Lawyer'],a:2},
  {q:'Who builds machines?',o:['Nurse','Engineer','Student','Cook'],a:1}
];
var qi=0,qs=0,qan=false;

function buildQuiz(){ showQ(); }
function showQ(){
  qan=false;
  var q=QD[qi];
  document.getElementById('qjq').textContent=q.q;
  document.getElementById('qjn').style.display='none';
  var c=document.getElementById('qjo');c.innerHTML='';
  q.o.forEach(function(opt,i){
    var b=document.createElement('div');b.className='qb';b.textContent=opt;
    b.onclick=function(){ chkQ(i,b); };
    c.appendChild(b);
  });
  document.getElementById('qjs').textContent='Savol '+(qi+1)+'/'+QD.length+' | To\'g\'ri: '+qs;
}
function chkQ(idx,btn){
  if(qan) return; qan=true;
  var a=QD[qi].a;
  document.querySelectorAll('#qjo .qb')[a].classList.add('ok');
  if(idx!==a) btn.classList.add('no'); else qs++;
  sp(QD[qi].o[a]);
  document.getElementById('qjs').textContent='Savol '+(qi+1)+'/'+QD.length+' | To\'g\'ri: '+qs;
  if(qi<QD.length-1) document.getElementById('qjn').style.display='inline-block';
  else document.getElementById('qjs').textContent='Natija: '+qs+'/'+QD.length+' to\'g\'ri!';
}
function nxtQ(){ qi++; if(qi<QD.length) showQ(); }

/* ===================== UI ===================== */
function tc(hdr){
  hdr.closest('.card').classList.toggle('op');
}
function goS(n){
  document.querySelectorAll('.sec').forEach(function(s){ s.classList.remove('on'); });
  document.querySelectorAll('.sbtn').forEach(function(b){ b.classList.remove('on'); });
  document.getElementById('s'+n).classList.add('on');
  document.querySelectorAll('.sbtn')[n].classList.add('on');
  window.scrollTo({top:0,behavior:'smooth'});
}

/* ===================== INIT ===================== */
buildAlpha();
buildNums();
buildColors();
buildQuiz();
// Pre-load voices
if(synth){ loadVoices(); setTimeout(loadVoices,500); setTimeout(loadVoices,1500); }
drawFrame(0,AD[0]);


/* ===== GRAMMAR QUEST ENGINE ===== */
var LESSONS=[
  {id:0,icon:'🔵',title:'To Be: am / is / are',sub:"Ingliz tilining asosiy fe'li",diff:'A1',tag:'a1',xp:100,content:buildToBeLesson,questions:buildToBeQuestions},
  {id:1,icon:'💚',title:'Olmoshlar (Pronouns)',sub:'I, You, He, She, It, We, They',diff:'A1',tag:'a1',xp:100,content:buildPronounLesson,questions:buildPronounQuestions},
  {id:2,icon:'⏰',title:'Simple Present Tense',sub:'Hozirgi oddiy zamon',diff:'A1',tag:'a1',xp:100,content:buildSPTLesson,questions:buildSPTQuestions},
  {id:3,icon:'📦',title:"Have / Has & There is/are",sub:'Egalik va mavjudlik',diff:'A2',tag:'a2',xp:100,content:buildHaveLesson,questions:buildHaveQuestions},
  {id:4,icon:'👉',title:'This / That / These / Those',sub:"Ko'rsatish olmoshlari + Articles",diff:'A2',tag:'a2',xp:100,content:buildDemLesson,questions:buildDemQuestions},
  {id:5,icon:'🌀',title:'Present Continuous',sub:'Hozir bo&#x2019;layotgan harakatlar',diff:'A2',tag:'a2',xp:100,content:buildPContLesson,questions:buildPContQuestions},
  {id:6,icon:'🔮',title:'Prepositions of Time & Place',sub:'in / on / at / under / next to',diff:'B1',tag:'b1',xp:100,content:buildPrepLesson,questions:buildPrepQuestions}
];

var GS={unlocked:[true,false,false,false,false,false,false],scores:[null,null,null,null,null,null,null],xp:0};
var curLesson=-1,curQ=0,curScore=0,curAnswered=false,curQList=[];

function loadGS(){
  try{var d=localStorage.getItem('gramState');if(d){var p=JSON.parse(d);GS.unlocked=p.unlocked||GS.unlocked;GS.scores=p.scores||GS.scores;GS.xp=p.xp||0;}}catch(e){}
}
function saveGS(){try{localStorage.setItem('gramState',JSON.stringify(GS));}catch(e){}}

function initGrammar(){loadGS();renderRoad();updateXPBar();}

function renderRoad(){
  var road=document.getElementById('lessonRoad');
  if(!road) return;
  road.innerHTML='';
  LESSONS.forEach(function(l,i){
    if(i>0){var line=document.createElement('div');line.className='connector-line';road.appendChild(line);}
    var node=document.createElement('div');
    var locked=!GS.unlocked[i];
    var comp=GS.scores[i]!==null&&GS.scores[i]>=75;
    node.className='lesson-node '+(locked?'locked':(comp?'completed':'unlocked active'));
    var score=GS.scores[i];
    var stars=score===null?'&#9675;&#9675;&#9675;':(score>=90?'&#9733;&#9733;&#9733;':score>=75?'&#9733;&#9733;&#9675;':'&#9733;&#9675;&#9675;');
    var scoreDisp=score===null?(locked?'&#128274;':'-'):(score+'/100');
    var scoreColor=score===null?'var(--mt)':(score>=75?'#3ee8a0':'#ff6b8a');
    node.innerHTML='<div class="ln-icon" style="background:rgba(124,111,255,.12)">'+l.icon+(locked?'<div class="ln-lock">&#128274;</div>':'')+'</div>'
      +'<div class="ln-body"><div class="ln-title">'+l.title+'</div>'
      +'<div class="ln-meta"><span class="ln-tag '+l.tag+'">'+l.diff+'</span><span>'+l.sub+'</span></div></div>'
      +'<div class="ln-score"><div class="ln-score-num" style="color:'+scoreColor+'">'+scoreDisp+'</div>'
      +'<div class="ln-score-lbl">BALL</div><div class="ln-stars">'+stars+'</div></div>';
    if(!locked){(function(idx){node.onclick=function(){openLesson(idx);};})(i);}
    road.appendChild(node);
  });
}

function updateXPBar(){
  var total=LESSONS.length*100;
  var pct=Math.min((GS.xp/total)*100,100);
  var xb=document.getElementById('xpBar');if(xb)xb.style.width=pct+'%';
  var xl=document.getElementById('xpLabel');if(xl)xl.textContent='XP: '+GS.xp+' / '+total;
}

function showSection(id){
  var lp=document.getElementById('lessonPanel');
  var tp=document.getElementById('testPanel');
  var rp=document.getElementById('resultPanel');
  var lr=document.getElementById('lessonRoad');
  var gh=document.getElementById('gram-hero-wrap');
  if(lp)lp.style.display='none';
  if(tp)tp.style.display='none';
  if(rp)rp.style.display='none';
  if(lr)lr.style.display='none';
  if(gh)gh.style.display='none';
  var el=document.getElementById(id);
  if(el)el.style.display='block';
}

function openLesson(idx){
  curLesson=idx;
  var l=LESSONS[idx];
  var el=function(id){return document.getElementById(id);};
  if(el('lpIcon'))el('lpIcon').textContent=l.icon;
  if(el('lpTitle'))el('lpTitle').textContent=l.title;
  if(el('lpSub'))el('lpSub').textContent=l.sub;
  if(el('lpDiff'))el('lpDiff').textContent=l.diff;
  if(el('lpContent'))el('lpContent').innerHTML=l.content();
  var prev=GS.scores[idx];
  var note='';
  if(prev!==null)note="So'nggi ball: <strong style=\"color:"+(prev>=75?'#3ee8a0':'#ff6b8a')+"\">"+prev+"/100</strong>";
  if(el('startTestNote'))el('startTestNote').innerHTML=note;
  showSection('lessonPanel');
  var lp=document.getElementById('lessonPanel');
  if(lp)lp.style.display='block';
  var lr=document.getElementById('lessonRoad');
  if(lr)lr.style.display='none';
  var gh=document.getElementById('gram-hero-wrap');
  if(gh)gh.style.display='none';
  window.scrollTo({top:0,behavior:'smooth'});
}

function closeLessonPanel(){
  var ids=['lessonPanel','testPanel','resultPanel'];
  ids.forEach(function(id){var el=document.getElementById(id);if(el)el.style.display='none';});
  var lr=document.getElementById('lessonRoad');if(lr)lr.style.display='flex';
  var gh=document.getElementById('gram-hero-wrap');if(gh)gh.style.display='block';
  renderRoad();updateXPBar();
}

function startTest(){
  var l=LESSONS[curLesson];
  curQList=l.questions();curQ=0;curScore=0;curAnswered=false;
  var el=function(id){return document.getElementById(id);};
  if(el('tpTitle'))el('tpTitle').textContent=l.title+' — Test';
  if(el('tpSub'))el('tpSub').textContent='Savollar: '+curQList.length+' | 75+ ball kerak';
  var ids=['lessonPanel','resultPanel','lessonRoad','gram-hero-wrap'];
  ids.forEach(function(id){var e=document.getElementById(id);if(e)e.style.display='none';});
  var tp=document.getElementById('testPanel');if(tp)tp.style.display='block';
  showQuestion();
  window.scrollTo({top:0,behavior:'smooth'});
}

function backToLesson(){
  var tp=document.getElementById('testPanel');if(tp)tp.style.display='none';
  var lp=document.getElementById('lessonPanel');if(lp)lp.style.display='block';
}

function updateTestProgress(){
  var pct=(curQ/curQList.length)*100;
  var tb=document.getElementById('tpBar');if(tb)tb.style.width=pct+'%';
  var pts=Math.round((curScore/curQList.length)*100);
  var ch=document.getElementById('tpChip');if(ch)ch.textContent=curQ+'/'+curQList.length+' | '+pts+'%';
}

function showQuestion(){
  if(curQ>=curQList.length){endTest();return;}
  var q=curQList[curQ];
  curAnswered=false;
  updateTestProgress();
  var html='<div class="q-block"><div class="q-num">Savol '+(curQ+1)+' / '+curQList.length+'</div>';
  if(q.type==='mc'){
    html+='<div class="q-text">'+q.q+'</div><div class="q-opts" id="qOpts">';
    q.opts.forEach(function(o,i){html+='<div class="q-opt" onclick="checkMC('+i+','+q.a+')">'+o+'</div>';});
    html+='</div>';
  } else if(q.type==='fill'||q.type==='transform'){
    html+='<div class="q-text">'+q.q+'</div>';
    if(q.type==='transform')html+='<div class="rule-box" style="margin-bottom:10px;padding:10px 14px"><em style="font-size:12px;color:var(--mt)">Hint: </em><span style="font-size:12px;color:#b0a8ff">'+q.hint+'</span></div>';
    html+='<input class="q-fill-input" id="fillIn" placeholder="Javobingizni yozing..." autocomplete="off"><br><button class="q-submit-btn" onclick="checkFill()">Tekshirish &#10003;</button>';
  }
  html+='<div class="q-explain" id="qExp">'+q.exp+'</div>';
  html+='<button class="q-next-btn" id="qNext" onclick="nextQuestion()">Keyingi &#8594;</button></div>';
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
  inp.classList.add(ok?'correct':'wrong');
  inp.disabled=true;
  if(ok)curScore++;
  else{
    var hint=document.createElement('div');
    hint.style.cssText='font-size:12px;color:#ff6b8a;margin-top:6px';
    hint.textContent="To'g'ri javob: "+correct[0];
    var btn=inp.nextElementSibling;
    if(btn)btn.parentNode.insertBefore(hint,btn.nextSibling);
  }
  curAnswered=true;
  var ex=document.getElementById('qExp');if(ex)ex.style.display='block';
  var nx=document.getElementById('qNext');if(nx)nx.style.display='inline-block';
}

function nextQuestion(){curQ++;showQuestion();window.scrollTo({top:0,behavior:'smooth'});}

function endTest(){
  var pct=Math.round((curScore/curQList.length)*100);
  var pass=pct>=75;
  var wasScore=GS.scores[curLesson];
  if(wasScore===null||pct>wasScore){
    var xpGain=wasScore===null?LESSONS[curLesson].xp:Math.max(0,pct-wasScore);
    GS.xp+=xpGain;GS.scores[curLesson]=pct;
  }
  var unlockNext=false;
  if(pass&&curLesson+1<LESSONS.length&&!GS.unlocked[curLesson+1]){GS.unlocked[curLesson+1]=true;unlockNext=true;}
  saveGS();
  var tp=document.getElementById('testPanel');if(tp)tp.style.display='none';
  var rp=document.getElementById('resultPanel');if(rp)rp.style.display='block';
  var icon=pct>=90?'&#127775;':pct>=75?'&#127881;':'&#128548;';
  var msg=pct>=90?"Mukammal! Ajoyib natija!":pct>=75?"Zo'r! Siz o'tdingiz!":"Hali ozroq mashq kerak...";
  var scoreEl=document.getElementById('resultScore');
  if(scoreEl){scoreEl.textContent=pct+'/100';scoreEl.className='result-score '+(pass?'pass':'fail');}
  var ri=document.getElementById('resultIcon');if(ri)ri.innerHTML=icon;
  var rm=document.getElementById('resultMsg');if(rm)rm.textContent=msg;
  var rd=document.getElementById('resultDetail');
  if(rd)rd.innerHTML="To'g'ri: <strong>"+curScore+'/'+curQList.length+"</strong> savol"+(pass?" &nbsp;|&nbsp; &#9989; Keyingi dars uchun ruxsat!":" &nbsp;|&nbsp; &#10060; 75+ ball kerak");
  var ua=document.getElementById('unlockAnim');if(ua)ua.style.display=unlockNext?'block':'none';
  var nb=document.getElementById('rNextBtn');if(nb)nb.style.display=(pass&&curLesson+1<LESSONS.length)?'inline-block':'none';
  window.scrollTo({top:0,behavior:'smooth'});
  updateXPBar();updateLeaderboard();
}

function retryTest(){startTest();}
function goNextLesson(){openLesson(curLesson+1);}

/* ===== LEADERBOARD ===== */
var LB_KEY='gramLeaderboard2';
var myName='';
function loadLB(){try{return JSON.parse(localStorage.getItem(LB_KEY))||[];}catch(e){return[];}}
function saveLB(arr){try{localStorage.setItem(LB_KEY,JSON.stringify(arr));}catch(e){}}

function updateLeaderboard(){
  if(!myName)return;
  var arr=loadLB();
  var idx=-1;
  for(var i=0;i<arr.length;i++){if(arr[i].name===myName){idx=i;break;}}
  var entry={name:myName,xp:GS.xp,lessons:GS.scores.filter(function(s){return s!==null&&s>=75;}).length};
  if(idx>=0)arr[idx]=entry;else arr.push(entry);
  arr.sort(function(a,b){return b.xp-a.xp;});
  saveLB(arr);renderLB();
}

function saveToLeaderboard(){
  var inp=document.getElementById('lbNameIn');
  if(!inp||!inp.value.trim()){alert("Ismingizni kiriting!");return;}
  myName=inp.value.trim();
  updateLeaderboard();
}

function renderLB(){
  var arr=loadLB();
  var el=document.getElementById('lbList');if(!el)return;
  if(!arr.length){el.innerHTML='<div class="lb-empty">Hali hech kim yo\'q. Birinchi bo\'ling! &#127942;</div>';return;}
  var html='';
  arr.slice(0,20).forEach(function(e,i){
    var rank=i+1;
    var rankDisp=rank===1?'&#129351;':rank===2?'&#129352;':rank===3?'&#129353;':'#'+rank;
    var isMe=e.name===myName;
    html+='<div class="lb-entry'+(isMe?' me':'')+'">'
      +'<div class="lb-rank '+(rank===1?'gold':rank===2?'silver':rank===3?'bronze':'')+'">'+rankDisp+'</div>'
      +'<div class="lb-name">'+(isMe?'&#11088; ':'')+e.name+'</div>'
      +'<div class="lb-stars">'+(e.lessons||0)+'/'+LESSONS.length+' &#127891;</div>'
      +'<div class="lb-xp">'+e.xp+' XP</div>'
      +'</div>';
  });
  el.innerHTML=html;
}

function openLeaderboard(){
  var m=document.getElementById('lbModal');if(m)m.classList.add('on');
  renderLB();
}
function closeLeaderboard(){var m=document.getElementById('lbModal');if(m)m.classList.remove('on');}

/* ===== LESSON CONTENT ===== */
function H(s){return s;}/* passthrough — use HTML entities in strings */

function buildToBeLesson(){
  return '<div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128218; Qoida</div>'
  +'<div class="rule-box"><div class="rule-title">&#128309; To Be nima?</div>'
  +'<div class="rule-body">O&#x02BC;zbek tilidagi <strong>"bo&#x02BC;lmoq"</strong> ga to&#x02BC;g&#x02BC;ri keladi. Uch shakli bor: <strong>am, is, are</strong>.</div></div>'
  +'<div class="formula">I &rarr; am &nbsp;|&nbsp; He/She/It &rarr; is &nbsp;|&nbsp; You/We/They &rarr; are</div>'
  +'</div>'
  +'<div class="lc-section"><div class="lc-section-title">&#9989; Tasdiqlash (Positive)</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en">I <strong>am</strong> a student.</div><div class="ex-uz">Men talabaman.</div></div>'
  +'<div class="ex-card"><div class="ex-en">He <strong>is</strong> a doctor.</div><div class="ex-uz">U shifokor.</div></div>'
  +'<div class="ex-card"><div class="ex-en">She <strong>is</strong> beautiful.</div><div class="ex-uz">U chiroyli.</div></div>'
  +'<div class="ex-card"><div class="ex-en">We <strong>are</strong> friends.</div><div class="ex-uz">Biz do&#x02BC;stmiz.</div></div>'
  +'<div class="ex-card"><div class="ex-en">They <strong>are</strong> happy.</div><div class="ex-uz">Ular xursand.</div></div>'
  +'<div class="ex-card"><div class="ex-en">It <strong>is</strong> a cat.</div><div class="ex-uz">Bu mushuk.</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#10060; Inkor (Negative)</div>'
  +'<div class="formula">am/is/are + NOT</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card neg"><div class="ex-en">I <strong>am not</strong> tired.</div><div class="ex-uz">Men charchamadim.</div></div>'
  +'<div class="ex-card neg"><div class="ex-en">He <strong>is not</strong> here. (He isn&#39;t)</div><div class="ex-uz">U bu yerda emas.</div></div>'
  +'<div class="ex-card neg"><div class="ex-en">They <strong>are not</strong> ready. (aren&#39;t)</div><div class="ex-uz">Ular tayyor emas.</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#10067; Savol (Question)</div>'
  +'<div class="formula">Am/Is/Are + Subject + ...?</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card q"><div class="ex-en"><strong>Are</strong> you okay?</div><div class="ex-uz">Yaxshimisiz?</div></div>'
  +'<div class="ex-card q"><div class="ex-en"><strong>Is</strong> she a teacher?</div><div class="ex-uz">U o&#x02BC;qituvchimi?</div></div>'
  +'<div class="ex-card q"><div class="ex-en"><strong>Am</strong> I late?</div><div class="ex-uz">Kechikdimmi?</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128161; Qisqartmalar</div>'
  +'<div class="tip-box"><strong>I\'m &bull; He\'s &bull; She\'s &bull; We\'re &bull; They\'re</strong><br>'
  +'isn\'t &bull; aren\'t<br><br>'
  +'&#9888;&#65039; <strong>Am not</strong> ning qisqarmasi rasmiy yo&#x02BC;q!</div>'
  +'</div></div>';
}

function buildPronounLesson(){
  return '<div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128218; Olmoshlar turlari</div>'
  +'<div class="rule-box"><div class="rule-title">&#128100; 3 tur olmosh</div>'
  +'<div class="rule-body"><strong>Subject</strong> — gap egasi (I, You, He...)<br>'
  +'<strong>Object</strong> — to&#x02BC;ldiruvchi (me, you, him...)<br>'
  +'<strong>Possessive</strong> — egalik (my, your, his...)</div></div>'
  +'</div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128202; To&#x02BC;liq jadval</div>'
  +'<div style="overflow-x:auto"><table class="wt"><tr><th>Shaxs</th><th>Subject</th><th>Object</th><th>Possessive</th><th>O&#x02BC;zbekcha</th></tr>'
  +'<tr><td>1-shaxs</td><td class="en">I</td><td class="en">me</td><td class="en">my</td><td class="uz">Men / Mening</td></tr>'
  +'<tr><td>2-shaxs</td><td class="en">You</td><td class="en">you</td><td class="en">your</td><td class="uz">Siz / Sening</td></tr>'
  +'<tr><td>3 (erkak)</td><td class="en">He</td><td class="en">him</td><td class="en">his</td><td class="uz">U / Uning</td></tr>'
  +'<tr><td>3 (ayol)</td><td class="en">She</td><td class="en">her</td><td class="en">her</td><td class="uz">U / Uning</td></tr>'
  +'<tr><td>3 (narsa)</td><td class="en">It</td><td class="en">it</td><td class="en">its</td><td class="uz">U / Uning</td></tr>'
  +'<tr><td>Ko&#x02BC;plik 1</td><td class="en">We</td><td class="en">us</td><td class="en">our</td><td class="uz">Biz / Bizning</td></tr>'
  +'<tr><td>Ko&#x02BC;plik 2/3</td><td class="en">They</td><td class="en">them</td><td class="en">their</td><td class="uz">Ular / Ularning</td></tr>'
  +'</table></div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#9989; Misollar</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en"><strong>I</strong> love <strong>my</strong> country.</div><div class="ex-uz">Men vatanimni yaxshi ko&#x02BC;raman.</div><div class="ex-note">I = subject | my = possessive</div></div>'
  +'<div class="ex-card"><div class="ex-en">She gave <strong>him</strong> a book.</div><div class="ex-uz">U unga kitob berdi.</div><div class="ex-note">him = object (not he!)</div></div>'
  +'<div class="ex-card"><div class="ex-en">This is <strong>her</strong> bag.</div><div class="ex-uz">Bu uning sumkasi.</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>We</strong> invited <strong>them</strong> to <strong>our</strong> party.</div><div class="ex-uz">Biz ularni bizning ziyofatimizga taklif qildik.</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128161; Eslatma</div>'
  +'<div class="tip-box">&#9888;&#65039; <strong>Its</strong> (egalik) &#8800; <strong>It\'s</strong> (It is qisqartmasi)<br>'
  +'Hayvonlar uchun odatda <strong>it</strong>, sevimli hayvonlar uchun <strong>he/she</strong> ham ishlatiladi.</div>'
  +'</div></div>';
}

function buildSPTLesson(){
  return '<div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128218; Qoida</div>'
  +'<div class="rule-box"><div class="rule-title">&#9200; Simple Present nima uchun?</div>'
  +'<div class="rule-body">&#8226; Odatdagi harakatlar (every day, always)<br>&#8226; Umumiy haqiqatlar (The sun rises in the east)<br>&#8226; Doimiy holat (I live in Tashkent)</div></div>'
  +'<div class="formula">Tasdiq: Subject + verb (+s/es for he/she/it)</div>'
  +'<div class="formula">Inkor: Subject + don\'t/doesn\'t + verb</div>'
  +'<div class="formula">Savol: Do/Does + Subject + verb?</div>'
  +'</div>'
  +'<div class="lc-section"><div class="lc-section-title">&#9888;&#65039; He/She/It qoidasi</div>'
  +'<div class="rule-box warn">'
  +'<div class="rule-body">Ko&#x02BC;pchilik: + <strong>-s</strong> &rarr; work&rarr;works, eat&rarr;eats<br>'
  +'-ch/-sh/-ss/-x/-o: + <strong>-es</strong> &rarr; watch&rarr;watches, go&rarr;goes<br>'
  +'Undosh+y: y&rarr;<strong>ies</strong> &rarr; study&rarr;studies, fly&rarr;flies<br>'
  +'Unli+y: + <strong>-s</strong> &rarr; play&rarr;plays, say&rarr;says</div></div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#9989; Misollar</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en">I <strong>work</strong> every day.</div><div class="ex-uz">Men har kun ishlayman.</div></div>'
  +'<div class="ex-card"><div class="ex-en">She <strong>works</strong> at 8 AM.</div><div class="ex-uz">U soat 8 da ishlaydi.</div></div>'
  +'<div class="ex-card"><div class="ex-en">He <strong>studies</strong> English.</div><div class="ex-uz">U ingliz tilini o&#x02BC;qiydi.</div></div>'
  +'<div class="ex-card neg"><div class="ex-en">I <strong>don\'t</strong> like coffee.</div><div class="ex-uz">Men qahvani yoqtirmayman.</div></div>'
  +'<div class="ex-card neg"><div class="ex-en">She <strong>doesn\'t</strong> eat meat.</div><div class="ex-uz">U go&#x02BC;sht emaydi.</div><div class="ex-note">doesn\'t &rarr; fe\'l oddiy shaklda!</div></div>'
  +'<div class="ex-card q"><div class="ex-en"><strong>Does</strong> he live here?</div><div class="ex-uz">U bu yerda yashaydimi?</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128161; Signal so&#x02BC;zlar</div>'
  +'<div class="tip-box"><strong>always</strong> (doim) | <strong>usually</strong> (odatda) | <strong>often</strong> (ko&#x02BC;pincha)<br>'
  +'<strong>sometimes</strong> (ba&#x02BC;zan) | <strong>never</strong> (hech qachon) | <strong>every day/week</strong></div>'
  +'</div></div>';
}

function buildHaveLesson(){
  return '<div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128218; Have vs Has</div>'
  +'<div class="rule-box"><div class="rule-title">&#128230; Egalik bildiruvchi</div>'
  +'<div class="rule-body"><strong>have</strong> &rarr; I / You / We / They<br><strong>has</strong> &rarr; He / She / It</div></div>'
  +'<div class="formula">I have a book. / She has a car.</div>'
  +'</div>'
  +'<div class="lc-section"><div class="lc-section-title">&#9989; Misollar</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en">I <strong>have</strong> a dog.</div><div class="ex-uz">Mening itim bor.</div></div>'
  +'<div class="ex-card"><div class="ex-en">She <strong>has</strong> long hair.</div><div class="ex-uz">Uning uzun sochi bor.</div></div>'
  +'<div class="ex-card neg"><div class="ex-en">He <strong>doesn\'t have</strong> a phone.</div><div class="ex-uz">Uning telefoni yo&#x02BC;q.</div></div>'
  +'<div class="ex-card q"><div class="ex-en"><strong>Do</strong> you <strong>have</strong> time?</div><div class="ex-uz">Vaqtingiz bormi?</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#127968; There is / There are</div>'
  +'<div class="rule-box"><div class="rule-title">&#128205; Mavjudlikni bildiradi</div>'
  +'<div class="rule-body"><strong>There is</strong> &rarr; bitta narsa (singular)<br><strong>There are</strong> &rarr; ko&#x02BC;p narsa (plural)</div></div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en"><strong>There is</strong> a book on the table.</div><div class="ex-uz">Stolda bir kitob bor.</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>There are</strong> 20 students in class.</div><div class="ex-uz">Sinfda 20 o&#x02BC;quvchi bor.</div></div>'
  +'<div class="ex-card neg"><div class="ex-en"><strong>There isn\'t</strong> any water.</div><div class="ex-uz">Hech qanday suv yo&#x02BC;q.</div></div>'
  +'<div class="ex-card q"><div class="ex-en"><strong>Is there</strong> a bank near here?</div><div class="ex-uz">Bu yaqinda bank bormi?</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128161; Some / Any</div>'
  +'<div class="tip-box"><strong>some</strong> &mdash; tasdiq gaplarda: I have <strong>some</strong> money.<br>'
  +'<strong>any</strong> &mdash; inkor va savolda: I don\'t have <strong>any</strong> money.</div>'
  +'</div></div>';
}

function buildDemLesson(){
  return '<div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128218; Ko&#x02BC;rsatish olmoshlari</div>'
  +'<div class="rule-box"><div class="rule-title">&#128070; 4 ta shakl</div>'
  +'<div class="rule-body"><strong>This</strong> &mdash; yaqin, bitta &nbsp;|&nbsp; <strong>That</strong> &mdash; uzoq, bitta<br>'
  +'<strong>These</strong> &mdash; yaqin, ko&#x02BC;p &nbsp;|&nbsp; <strong>Those</strong> &mdash; uzoq, ko&#x02BC;p</div></div>'
  +'</div>'
  +'<div class="lc-section"><div class="lc-section-title">&#9989; Misollar</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en"><strong>This</strong> is my phone.</div><div class="ex-uz">Bu (yaqinimda) mening telefonim.</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>That</strong> is a school.</div><div class="ex-uz">U (narida) maktab.</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>These</strong> are my keys.</div><div class="ex-uz">Bular mening kalitlarim.</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>Those</strong> books are interesting.</div><div class="ex-uz">U (narida) kitoblar qiziqarli.</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128240; Articles: a / an / the</div>'
  +'<div class="rule-box"><div class="rule-title">&#128204; Artikllar</div>'
  +'<div class="rule-body"><strong>a / an</strong> &mdash; noaniq (birinchi marta)<br><strong>the</strong> &mdash; aniq (allaqachon ma&#x02BC;lum)</div></div>'
  +'<div class="formula">a + undosh: a book, a car</div>'
  +'<div class="formula">an + unli: an apple, an orange</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en">I saw <strong>a</strong> cat. <strong>The</strong> cat was black.</div><div class="ex-uz">Men bir mushuk ko&#x02BC;rdim. U mushuk qora edi.</div></div>'
  +'<div class="ex-card"><div class="ex-en">She is <strong>an</strong> engineer.</div><div class="ex-uz">U muhandis.</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128161; Artikl ishlatilmaydi</div>'
  +'<div class="tip-box">Umumiy tushunchalar: <strong>Dogs are friendly.</strong><br>'
  +'Mavhum narsalar: <strong>I like music.</strong><br>'
  +'Kasb + a: <strong>He is a doctor.</strong></div>'
  +'</div></div>';
}

function buildPContLesson(){
  return '<div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128218; Present Continuous nima?</div>'
  +'<div class="rule-box"><div class="rule-title">&#127744; Hozir davom etayotgan harakat</div>'
  +'<div class="rule-body">Hozir, shu lahzada bo&#x02BC;layotgan harakatni ifodalaydi.<br>Signal: <strong>now, right now, at the moment, look!, listen!</strong></div></div>'
  +'<div class="formula">Subject + am/is/are + verb-ING</div>'
  +'</div>'
  +'<div class="lc-section"><div class="lc-section-title">&#9888;&#65039; -ing qo&#x02BC;shish qoidalari</div>'
  +'<div class="rule-box warn">'
  +'<div class="rule-body">Ko&#x02BC;pchilik: + <strong>ing</strong> &rarr; work&rarr;working<br>'
  +'-e bilan tugasa: e o&#x02BC;chir + <strong>ing</strong> &rarr; make&rarr;making<br>'
  +'Qisqa+undosh: ikkilashtir + <strong>ing</strong> &rarr; run&rarr;running, sit&rarr;sitting<br>'
  +'-ie bilan: ie&rarr;y + <strong>ing</strong> &rarr; lie&rarr;lying</div></div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#9989; Misollar</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en">I <strong>am studying</strong> now.</div><div class="ex-uz">Men hozir o&#x02BC;qiyapman.</div></div>'
  +'<div class="ex-card"><div class="ex-en">She <strong>is cooking</strong> dinner.</div><div class="ex-uz">U kechki ovqat pishiryapti.</div></div>'
  +'<div class="ex-card neg"><div class="ex-en">He <strong>is not watching</strong> TV.</div><div class="ex-uz">U TV ko&#x02BC;rmayapti.</div></div>'
  +'<div class="ex-card q"><div class="ex-en"><strong>Are</strong> you <strong>listening</strong>?</div><div class="ex-uz">Tinglayapsizmi?</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#9889; Simple Present vs Continuous</div>'
  +'<div class="tip-box"><strong>I read every day.</strong> &rarr; Odatdagi (Simple Present)<br>'
  +'<strong>I am reading now.</strong> &rarr; Hozir (Continuous)<br><br>'
  +'&#9888;&#65039; Bu fe&#x02BC;llar Continuous bilan ishlatilmaydi:<br>'
  +'<strong>know, like, love, want, need, understand, believe</strong></div>'
  +'</div></div>';
}

function buildPrepLesson(){
  return '<div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128218; Vaqt predloglari</div>'
  +'<div class="rule-box"><div class="rule-title">&#128336; in / on / at &mdash; Vaqt</div>'
  +'<div class="rule-body">'
  +'<strong>at</strong> &mdash; aniq vaqt: at 5 PM, at noon, at midnight<br>'
  +'<strong>on</strong> &mdash; kun va sana: on Monday, on July 4th<br>'
  +'<strong>in</strong> &mdash; oy, yil, mavsim: in January, in 2025, in summer</div></div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#127968; Joy predloglari</div>'
  +'<div class="rule-box"><div class="rule-title">&#128205; in / on / at &mdash; Joy</div>'
  +'<div class="rule-body">'
  +'<strong>at</strong> &mdash; aniq nuqta: at school, at home, at the door<br>'
  +'<strong>on</strong> &mdash; yuzada: on the table, on the wall<br>'
  +'<strong>in</strong> &mdash; ichida: in the box, in Tashkent</div></div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en">The book is <strong>on</strong> the table.</div><div class="ex-uz">Kitob stolning ustida.</div></div>'
  +'<div class="ex-card"><div class="ex-en">She lives <strong>in</strong> London.</div><div class="ex-uz">U Londonda yashaydi.</div></div>'
  +'<div class="ex-card"><div class="ex-en">I\'ll meet you <strong>at</strong> the station.</div><div class="ex-uz">Stantsiyada ko&#x02BC;rishamiz.</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#8596;&#65039; Qo&#x02BC;shimcha predloglar</div>'
  +'<div class="examples-grid">'
  +'<div class="ex-card"><div class="ex-en"><strong>under</strong> the table</div><div class="ex-uz">stolning tagida</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>next to</strong> the bank</div><div class="ex-uz">bank yonida</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>between</strong> the shops</div><div class="ex-uz">do&#x02BC;konlar orasida</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>in front of</strong> the school</div><div class="ex-uz">maktab oldida</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>behind</strong> the house</div><div class="ex-uz">uy orqasida</div></div>'
  +'<div class="ex-card"><div class="ex-en"><strong>above</strong> the clouds</div><div class="ex-uz">bulutlar ustida</div></div>'
  +'</div></div>'
  +'<div class="lc-section"><div class="lc-section-title">&#128161; Eslatma</div>'
  +'<div class="tip-box"><strong>in the morning/afternoon/evening</strong> (kun qismlarida IN)<br>'
  +'<strong>at night, at noon, at midnight</strong> (maxsus vaqtlarda AT)</div>'
  +'</div></div>';
}

/* ===== QUESTIONS ===== */
function buildToBeQuestions(){return[
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

function buildPronounQuestions(){return[
  {type:'mc',q:'"Ali is my friend. ___ is a doctor." — Ali uchun',opts:['She','He','They','It'],a:1,exp:'Ali erkak ism — He.'},
  {type:'mc',q:'"Give ___ the book, please." (menga)',opts:['I','my','me','mine'],a:2,exp:'To\'ldiruvchi holda "me".'},
  {type:'fill',q:'To\'ldiring: "This is ___ bag." (Sara — unga tegishli)',a:['her'],exp:'She (3-shaxs ayol) possessive = her.'},
  {type:'mc',q:'Qaysi gapda xato?',opts:['I love my dog.','Her is a teacher.','We need your help.','They gave us a gift.'],a:1,exp:'"Her is" xato — to\'g\'risi "She is".'},
  {type:'mc',q:'"Biz ularni kutdik." — to\'g\'ri tarjima',opts:['We waited us.','We waited they.','We waited them.','Us waited them.'],a:2,exp:'them = object (ular).'},
  {type:'mc',q:'"___ book is interesting." (uning — erkak)',opts:['He','Him','His','Her'],a:2,exp:'Egalik (erkak) = His.'},
  {type:'mc',q:'"The cat licked ___ paw."',opts:['his','her','its','their'],a:2,exp:'Narsa/hayvon (neytral) = its.'},
  {type:'fill',q:'Bo\'sh joy: "___ and I went to school." (Ali)',a:['ali'],exp:'Gap egasida "Ali and I".'},
  {type:'fill',q:'"What is ___ phone number?" (Siz uchun)',a:['your'],exp:'Siz/Sening = your.'},
  {type:'mc',q:'Qaysi gap grammatik to\'g\'ri?',opts:['Me and him went there.','He and I went there.','Him and I went there.','I and him went there.'],a:1,exp:'Gap egasi: He and I (subject pronouns).'}
];}

function buildSPTQuestions(){return[
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

function buildHaveQuestions(){return[
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

function buildDemQuestions(){return[
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

function buildPContQuestions(){return[
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

function buildPrepQuestions(){return[
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

/* ===== INIT ===== */
initGrammar();

</script>
</body>
</html>
