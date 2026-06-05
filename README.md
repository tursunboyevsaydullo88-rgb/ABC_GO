<!DOCTYPE html>
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
        <tr><td class="en">Saturday <button class="spk" onclick="sp('Saturday')">&#128266;</button></td><td class="pr">[ˈsætərdeɪ]</t# english-course_saydullo_go
