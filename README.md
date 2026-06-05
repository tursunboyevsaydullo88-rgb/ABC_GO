    <!DOCTYPE html>
<html lang="uz">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ABC_GO - Ingliz Tili Kursi</title>
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
.cc{border-radius:11px;padding:12px;cursor:pointer;transition:transform .2s;text-align:center;font-weight:bold;}
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
.sl{font-family:'Unbounded',sans-serif;font-size:9px;letter-spacing:2px;text-transform:uppercase;color:var(--mt);margin:22px 0 9px;}
.ov{display:grid;grid-template-columns:repeat(auto-fill,minmax(145px,1fr));gap:9px;margin-bottom:24px;}
.ovc{background:var(--s1);border:1px solid var(--bd);border-radius:15px;padding:16px 13px;cursor:pointer;transition:all .22s;text-align:center;}
.ovc:hover{border-color:var(--ac);transform:translateY(-3px);}
.ovc .on2{font-family:'Unbounded',sans-serif;font-size:24px;font-weight:900;margin-bottom:5px;}
.ovc .ot{font-size:11px;font-weight:600;margin-bottom:2px;}
.ovc .os{font-size:10px;color:var(--mt);}
@media(max-width:460px){.ov{grid-template-columns:repeat(2,1fr);}.agrid{grid-template-columns:repeat(auto-fill,minmax(62px,1fr));}}
</style>
</head>
<body>

<div class="hero">
  <div class="badge">&#127468;&#127463; Ingliz tili kursi &mdash; Offline</div>
  <h1>Inglizchani<br><span>bosqichma-bosqich</span><br>o'rgan</h1>
  <p>A1 &rarr; B1 &middot; O'zbek tilida &middot; Internetisiz ishlaydi</p>
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
      <div class="cb" style="display:block;">
        <div class="gb">&#9989; <strong>Ketma-ket o'rganing</strong> &mdash; 1-bosqichdan boshlang</div>
        <div class="gb g">&#128266; <strong>Har bir so'zni bosing</strong> &mdash; ovozli talaffuz chiqadi</div>
        <div class="gb o">&#128241; <strong>Internetisiz ishlaydi</strong> &mdash; Istalgan vaqtda foydalaning</div>
      </div>
    </div>
  </div>

  <!-- S1 ALPHABET -->
  <div class="sec" id="s1">
    <div class="card op">
      <div class="ch" onclick="tc(this)">
        <div class="ci" style="background:rgba(124,111,255,.15)">&#128292;</div>
        <div class="ct"><h3>Ingliz Alifbosi (A&ndash;Z)</h3><p>Har bir harfni bosing &rarr; ovozli talaffuz</p></div>
        <span class="ti">&#9660;</span>
      </div>
      <div class="cb" style="display:block;"><div class="agrid" id="agrid"></div></div>
    </div>
    
    <div class="card op">
      <div class="ch" onclick="tc(this)">
        <div class="ci" style="background:rgba(255,107,138,.15)">&#12075;</div>
        <div class="ct"><h3>Salomlashish</h3><p>Birinchi iboralar</p></div>
        <span class="ti">&#9660;</span>
      </div>
      <div class="cb" style="display:block;">
        <table class="wt">
          <tr><th>Inglizcha</th><th>Talaffuz</th><th>O'zbekcha</th></tr>
          <tr><td class="en">Hello <button class="spk" onclick="sp('Hello')">&#128266;</button></td><td class="pr">[heˈloʊ]</td><td class="uz">Salom</td></tr>
          <tr><td class="en">Hi <button class="spk" onclick="sp('Hi')">&#128266;</button></td><td class="pr">[haɪ]</td><td class="uz">Salom (norasmiy)</td></tr>
          <tr><td class="en">Good morning <button class="spk" onclick="sp('Good morning')">&#128266;</button></td><td class="pr">[gʊd ˈmɔːrnɪŋ]</td><td class="uz">Xayrli tong</td></tr>
          <tr><td class="en">Good afternoon <button class="spk" onclick="sp('Good afternoon')">&#128266;</button></td><td class="pr">[gʊd ˌæftərˈnuːn]</td><td class="uz">Xayrli kun</td></tr>
          <tr><td class="en">Goodbye <button class="spk" onclick="sp('Goodbye')">&#128266;</button></td><td class="pr">[ˌgʊdˈbaɪ]</td><td class="uz">Xayr</td></tr>
        </table>
      </div>
    </div>
  </div>

  <!-- S2 WORDS -->
  <div class="sec" id="s2">
    <div class="card op">
      <div class="ch" onclick="tc(this)">
        <div class="ci" style="background:rgba(255,179,71,.15)">&#128290;</div>
        <div class="ct"><h3>Sonlar (1&ndash;20)</h3><p>Bosing va eshiting</p></div>
        <span class="ti">&#9660;</span>
      </div>
      <div class="cb" style="display:block;">
        <div class="ngrid" id="ng1"></div>
      </div>
    </div>
    <div class="card op">
      <div class="ch" onclick="tc(this)">
        <div class="ci" style="background:rgba(255,107,138,.15)">&#127912;</div>
        <div class="ct"><h3>Ranglar (Colors)</h3><p>Bosing va eshiting</p></div>
        <span class="ti">&#9660;</span>
      </div>
      <div class="cb" style="display:block;">
        <div class="cgrid" id="clrg"></div>
      </div>
    </div>
  </div>

  <!-- S3 GRAMMAR -->
  <div class="sec" id="s3">
    <div class="card op">
      <div class="ch" onclick="tc(this)">
        <div class="ci" style="background:rgba(62,232,160,.15)">&#128214;</div>
        <div class="ct"><h3>To Be fe'li</h3><p>Asosiy grammatika</p></div>
        <span class="ti">&#9660;</span>
      </div>
      <div class="cb" style="display:block;">
        <div class="gb">Ingliz tilida gap tuzish uchun eng muhim fe'l <strong>To be (bo'lmoq)</strong> fe'lidir. U hozirgi zamonda 3 ga bo'linadi: <strong>am, is, are</strong>.</div>
        <div class="ex"><div class="eg">I am a teacher. <button class="spk" onclick="sp('I am a teacher')">&#128266;</button></div><div class="uz2">Men o'qituvchiman.</div></div>
        <div class="ex"><div class="eg">He is happy. <button class="spk" onclick="sp('He is happy')">&#128266;</button></div><div class="uz2">U baxtli.</div></div>
        <div class="ex"><div class="eg">They are friends. <button class="spk" onclick="sp('They are friends')">&#128266;</button></div><div class="uz2">Ular do'stlar.</div></div>
      </div>
    </div>
  </div>

  <!-- S4 DIALOGUE -->
  <div class="sec" id="s4">
    <div class="card op">
      <div class="ch" onclick="tc(this)">
        <div class="ci" style="background:rgba(255,179,71,.15)">&#128172;</div>
        <div class="ct"><h3>Kundalik Suhbat</h3><p>Namuna muloqot</p></div>
        <span class="ti">&#9660;</span>
      </div>
      <div class="cb" style="display:block;">
        <div class="dlg">
          <div class="bbl a"><div class="wh">Sarah <button class="spk" onclick="sp('Hello! My name is Sarah. What is your name?')">&#128266;</button></div><div class="eg">Hello! My name is Sarah. What is your name?</div><div class="uz3">Salom! Mening ismim Sarah. Ismingiz nima?</div></div>
          <div class="bbl b"><div class="wh">Ali <button class="spk" onclick="sp('Hi! My name is Ali. Nice to meet you!')">&#128266;</button></div><div class="eg">Hi! My name is Ali. Nice to meet you!</div><div class="uz3">Salom! Mening ismim Ali. Tanishganimdan xursandman!</div></div>
        </div>
      </div>
    </div>
  </div>

  <!-- S5 NEXT -->
  <div class="sec" id="s5">
    <div class="card op">
      <div class="ch">
        <div class="ci" style="background:rgba(176,168,255,.15)">&#128640;</div>
        <div class="ct"><h3>Keyingi Bosqichlar</h3><p>Tez kunda qo'shiladi</p></div>
      </div>
      <div class="cb" style="display:block;">
        <div class="gb o">B1 va B2 darajadagi darslar hamda yangi audio lug'atlar tez orada shu bo'limda paydo bo'ladi!</div>
      </div>
    </div>
  </div>

</div>

<script>
// SAHIFALARNI ALMAASHTIRISH (NAVIGATSIYA)
function goS(num) {
  // Barcha bo'limlarni yopish
  document.querySelectorAll('.sec').forEach(s => s.classList.remove('on'));
  // Tanlangan bo'limni ochish
  document.getElementById('s' + num).classList.add('on');
  
  // Tugmalarni aktiv qilish
  document.querySelectorAll('.sbtn').forEach(b => b.classList.remove('on'));
  document.querySelectorAll('.snav .sbtn')[num].classList.add('on');
}

// AKKORDEON (CARD) OCHIB YOPISH
function tc(el) {
  el.parentElement.classList.toggle('op');
  let body = el.nextElementSibling;
  if(body.style.display === 'block') {
    body.style.display = 'none';
  } else {
    body.style.display = 'block';
  }
}

// OVOZ CHIQARISH (TEXT-TO-SPEECH)
function sp(text) {
  if ('speechSynthesis' in window) {
    let u = new SpeechSynthesisUtterance(text);
    u.lang = 'en-US';
    u.rate = 0.85; 
    window.speechSynthesis.cancel(); 
    window.speechSynthesis.speak(u);
  } else {
    alert("Kechirasiz, qurilmangizda ovoz chiqarish tizimi ishlamaydi.");
  }
}

// ALIFBONI AVTOMATIK YARATISH
const alpha = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'.split('');
const alphUz = {
  A:'Ey', B:'Bi', C:'Si', D:'Di', E:'I', F:'Ef', G:'Ji', H:'Eych', I:'Ay', J:'Jey', K:'Key', L:'El', M:'Em', 
  N:'En', O:'Ou', P:'Pi', Q:'Kyu', R:'Ar', S:'Es', T:'Ti', U:'Yu', V:'Vi', W:'Dablyu', X:'Eks', Y:'Uay', Z:'Zed'
};
let ag = document.getElementById('agrid');
if(ag) {
  alpha.forEach(l => {
    let div = document.createElement('div');
    div.className = 'alc';
    div.onclick = () => sp(l);
    div.innerHTML = `<div class="bl">${l}</div><div class="sl">[${alphUz[l]}]</div>`;
    ag.appendChild(div);
  });
}

// SONLARNI AVTOMATIK YARATISH
const nums = [
  {n:1, e:'One'}, {n:2, e:'Two'}, {n:3, e:'Three'}, {n:4, e:'Four'}, {n:5, e:'Five'},
  {n:6, e:'Six'}, {n:7, e:'Seven'}, {n:8, e:'Eight'}, {n:9, e:'Nine'}, {n:10, e:'Ten'},
  {n:11, e:'Eleven'}, {n:12, e:'Twelve'}, {n:13, e:'Thirteen'}, {n:14, e:'Fourteen'}, {n:15, e:'Fifteen'},
  {n:16, e:'Sixteen'}, {n:17, e:'Seventeen'}, {n:18, e:'Eighteen'}, {n:19, e:'Nineteen'}, {n:20, e:'Twenty'}
];
let ng1 = document.getElementById('ng1');
if(ng1) {
  nums.forEach(x => {
    let div = document.createElement('div');
    div.className = 'nc';
    div.onclick = () => sp(x.e);
    div.innerHTML = `<div class="n">${x.n}</div><div><div style="font-size:12px;font-weight:600;">${x.e}</div></div>`;
    ng1.appendChild(div);
  });
}

// RANGLARNI AVTOMATIK YARATISH
const clrs = [
  {e:'Red', u:'Qizil', c:'#ff4d4d', t:'#000'}, {e:'Blue', u:'Ko\'k', c:'#4d94ff', t:'#000'},
  {e:'Green', u:'Yashil', c:'#2ecc71', t:'#000'}, {e:'Yellow', u:'Sariq', c:'#f1c40f', t:'#000'},
  {e:'White', u:'Oq', c:'#ffffff', t:'#000'}, {e:'Black', u:'Qora', c:'#111111', t:'#fff'}
];
let cg = document.getElementById('clrg');
if(cg) {
  clrs.forEach(c => {
    let div = document.createElement('div');
    div.className = 'cc';
    div.style.background = c.c;
    div.style.color = c.t;
    div.onclick = () => sp(c.e);
    div.innerHTML = `<div>${c.e}</div><div style="font-size:11px;opacity:0.8;">${c.u}</div>`;
    cg.appendChild(div);
  });
}
</script>

</body>
</html>
