body_html = """
<body>

<!-- TOP BAR -->
<div id="topbar">
  <div class="topbar-left">
    <div class="topbar-item">📞 <a href="tel:+998901234567">+998 90 123-45-67</a></div>
    <div class="topbar-item">✉️ info@linguauz.uz</div>
    <div class="topbar-item">🏛️ O'zbekiston &mdash; Ingliz Tili Platformasi</div>
  </div>
  <div class="topbar-right">
    <div class="topbar-stat">🔥 <span id="topStreak">0</span></div>
    <div class="topbar-stat">⚡ <span id="topXP">0 XP</span></div>
    <div class="topbar-stat">🎯 <span id="topLevel">A1</span></div>
  </div>
</div>

<!-- NAVBAR -->
<nav id="navbar">
  <button class="hamburger" onclick="openSidebar()" aria-label="Menu">
    <span></span><span></span><span></span>
  </button>
  <div class="navbar-logo" onclick="navTo('home')" style="cursor:pointer">
    <div class="navbar-logo-icon">🌐</div>
    <div class="navbar-logo-text">
      <div class="navbar-logo-title">LinguaUz</div>
      <div class="navbar-logo-sub">Ingliz tili platformasi</div>
    </div>
  </div>
  <div class="navbar-nav">
    <button class="nav-link active" onclick="navTo('home')" id="nl-home">🏠 Bosh sahifa</button>
    <button class="nav-link" onclick="navTo('alphabet')" id="nl-alphabet">🔤 Alifbo</button>
    <button class="nav-link" onclick="navTo('vocabulary')" id="nl-vocabulary">📚 So'z boyligi</button>
    <button class="nav-link" onclick="navTo('grammar')" id="nl-grammar">🎮 Grammar Quest</button>
    <button class="nav-link" onclick="navTo('advanced')" id="nl-advanced">🚀 Ilg'or</button>
    <button class="nav-link" onclick="navTo('conversation')" id="nl-conversation">💬 Suhbat</button>
    <button class="nav-link" onclick="navTo('game')" id="nl-game">⚡ O'yin</button>
    <button class="nav-link" onclick="navTo('progress')" id="nl-progress">📊 Progress</button>
  </div>
  <div class="navbar-right">
    <button class="nav-btn nav-btn-outline" onclick="openLB()">🏆 Reyting</button>
  </div>
</nav>

<!-- MOBILE SIDEBAR -->
<div id="sideOverlay" onclick="closeSidebar()"></div>
<div id="mobileSidebar">
  <div class="sidebar-header">
    <div style="font-family:'Unbounded',sans-serif;font-weight:900;font-size:16px">🌐 LinguaUz</div>
    <button class="sidebar-close" onclick="closeSidebar()">✕</button>
  </div>
  <button class="sidebar-nav-item active" onclick="navTo('home')" id="sn-home"><span class="sidebar-nav-icon">🏠</span>Bosh sahifa</button>
  <button class="sidebar-nav-item" onclick="navTo('alphabet')" id="sn-alphabet"><span class="sidebar-nav-icon">🔤</span>Alifbo va Salomlashish</button>
  <button class="sidebar-nav-item" onclick="navTo('vocabulary')" id="sn-vocabulary"><span class="sidebar-nav-icon">📚</span>So'z boyligi</button>
  <button class="sidebar-nav-item" onclick="navTo('grammar')" id="sn-grammar"><span class="sidebar-nav-icon">🎮</span>Grammar Quest</button>
  <button class="sidebar-nav-item" onclick="navTo('advanced')" id="sn-advanced"><span class="sidebar-nav-icon">🚀</span>Ilg'or daraja</button>
  <button class="sidebar-nav-item" onclick="navTo('conversation')" id="sn-conversation"><span class="sidebar-nav-icon">💬</span>Suhbat</button>
  <button class="sidebar-nav-item" onclick="navTo('game')" id="sn-game"><span class="sidebar-nav-icon">⚡</span>So'z O'yini</button>
  <button class="sidebar-nav-item" onclick="navTo('progress')" id="sn-progress"><span class="sidebar-nav-icon">📊</span>Progress</button>
  <button class="sidebar-nav-item" onclick="openLB()"><span class="sidebar-nav-icon">🏆</span>Global Reyting</button>
</div>

<!-- HERO (shown on home page) -->
<div id="hero">
  <div class="hero-inner">
    <div class="hero-tag">✦ O'zbek tilida ingliz tili</div>
    <div class="hero-title">Ingliz tilini o'rganishning<br>eng qulay usuli</div>
    <p class="hero-sub">7 ta grammatika darsi · So'z o'yinlari · Kunlik vazifalar · Global reyting tizimi</p>
    <div class="hero-btns">
      <button class="hero-btn hero-btn-white" onclick="navTo('grammar')">🎮 Grammar Quest</button>
      <button class="hero-btn hero-btn-outline" onclick="navTo('game')">⚡ So'z O'yini</button>
    </div>
    <div class="hero-stats">
      <div class="hero-stat"><div class="hero-stat-num">7</div><div class="hero-stat-lbl">Grammatika darsi</div></div>
      <div class="hero-stat"><div class="hero-stat-num">26</div><div class="hero-stat-lbl">Alifbo harflari</div></div>
      <div class="hero-stat"><div class="hero-stat-num">70+</div><div class="hero-stat-lbl">Test savollari</div></div>
      <div class="hero-stat"><div class="hero-stat-num">∞</div><div class="hero-stat-lbl">So'z o'yinlari</div></div>
    </div>
  </div>
</div>

<!-- MAIN CONTENT -->
<div id="content">

  <!-- ========== HOME PAGE ========== -->
  <div class="page active" id="page-home">
    <!-- Streak banner -->
    <div class="streak-banner">
      <div class="streak-fire">🔥</div>
      <div class="streak-info">
        <div class="streak-num" id="homeStreak">0</div>
        <div class="streak-label">kunlik streak</div>
      </div>
      <div style="flex:1"></div>
      <div>
        <div style="font-size:11px;color:var(--gray-500);margin-bottom:6px;font-weight:600">Bu hafta:</div>
        <div class="streak-days" id="streakCal"></div>
      </div>
    </div>

    <!-- Stats -->
    <div class="stats-grid">
      <div class="stat-card blue"><div class="stat-icon">⚡</div><div class="stat-val blue" id="homeXP">0</div><div class="stat-label">Jami XP</div></div>
      <div class="stat-card green"><div class="stat-icon">✅</div><div class="stat-val green" id="homeLessons">0/7</div><div class="stat-label">Yakunlandi</div></div>
      <div class="stat-card amber"><div class="stat-icon">🎯</div><div class="stat-val amber" id="homeAccuracy">—</div><div class="stat-label">O'rtacha ball</div></div>
      <div class="stat-card purple"><div class="stat-icon">📈</div><div class="stat-val purple" id="homeLvl">A1</div><div class="stat-label">Daraja</div></div>
    </div>

    <!-- Daily Challenge -->
    <div class="sec-head">
      <div class="sec-head-title"><div class="dot"></div>⚡ Kunlik vazifa <span style="font-size:11px;font-weight:500;color:var(--green);margin-left:6px">+50 XP</span></div>
    </div>
    <div class="daily-challenge">
      <div class="daily-tag">📅 Bugungi savol</div>
      <div class="daily-q" id="dailyQ">Yuklanmoqda...</div>
      <div class="daily-opts" id="dailyOpts"></div>
      <div class="daily-reward" id="dailyReward" style="display:none">🎉 Ajoyib! +50 XP oldiniz!</div>
    </div>

    <!-- Courses -->
    <div class="sec-head">
      <div class="sec-head-title"><div class="dot"></div>📖 Darslar</div>
      <button class="nav-btn nav-btn-outline" style="font-size:12px;padding:6px 12px" onclick="navTo('progress')">Barchasini ko'rish →</button>
    </div>
    <div class="course-grid">
      <div class="course-card" onclick="navTo('alphabet')">
        <div class="course-card-img" style="background:#eff6ff">🔤</div>
        <div class="course-card-body">
          <div class="course-card-badge badge-a1">A1</div>
          <div class="course-card-title">Alifbo</div>
          <div class="course-card-sub">26 harf · Animatsiya</div>
          <div class="course-progress-bar"><div class="course-progress-fill" style="width:100%"></div></div>
        </div>
      </div>
      <div class="course-card" onclick="navTo('vocabulary')">
        <div class="course-card-img" style="background:#fff7ed">📚</div>
        <div class="course-card-body">
          <div class="course-card-badge badge-a1">A1</div>
          <div class="course-card-title">So'z boyligi</div>
          <div class="course-card-sub">Sonlar · Ranglar · Kasblar</div>
          <div class="course-progress-bar"><div class="course-progress-fill" style="width:80%"></div></div>
        </div>
      </div>
      <div class="course-card" onclick="navTo('grammar')">
        <div class="course-card-img" style="background:#eff6ff">🎮</div>
        <div class="course-card-body">
          <div class="course-card-badge badge-a2">A1-B1</div>
          <div class="course-card-title">Grammar Quest</div>
          <div class="course-card-sub">7 bosqich · Unlock tizimi</div>
          <div class="course-progress-bar"><div class="course-progress-fill" id="gramProgBar" style="width:0%"></div></div>
        </div>
      </div>
      <div class="course-card" onclick="navTo('advanced')">
        <div class="course-card-img" style="background:#fef2f2">🚀</div>
        <div class="course-card-body">
          <div class="course-card-badge badge-b1">B1</div>
          <div class="course-card-title">Ilg'or daraja</div>
          <div class="course-card-sub">Past · Future · Modal</div>
          <div class="course-progress-bar"><div class="course-progress-fill" style="width:60%"></div></div>
        </div>
      </div>
      <div class="course-card" onclick="navTo('conversation')">
        <div class="course-card-img" style="background:#f0fdf4">💬</div>
        <div class="course-card-body">
          <div class="course-card-badge badge-a2">A2</div>
          <div class="course-card-title">Suhbat</div>
          <div class="course-card-sub">Do'kon · Restoran</div>
          <div class="course-progress-bar"><div class="course-progress-fill" style="width:75%"></div></div>
        </div>
      </div>
      <div class="course-card" onclick="navTo('game')">
        <div class="course-card-img" style="background:#faf5ff">⚡</div>
        <div class="course-card-body">
          <div class="course-card-badge badge-game">O'yin</div>
          <div class="course-card-title">So'z O'yini</div>
          <div class="course-card-sub">Tezkor savol-javob</div>
          <div class="course-progress-bar"><div class="course-progress-fill" style="width:50%;background:var(--purple)"></div></div>
        </div>
      </div>
    </div>

    <!-- Achievements -->
    <div class="sec-head">
      <div class="sec-head-title"><div class="dot"></div>🏅 Yutuqlar</div>
    </div>
    <div class="ach-grid" id="homeAch"></div>
  </div>

  <!-- ========== ALPHABET PAGE ========== -->
  <div class="page" id="page-alphabet">
    <div class="breadcrumb"><span onclick="navTo('home')" style="cursor:pointer">🏠 Bosh sahifa</span><span class="breadcrumb-sep">›</span><span class="breadcrumb-current">Alifbo</span></div>
    <div class="sec-head"><div class="sec-head-title"><div class="dot"></div>🔤 Ingliz Alifbosi (A–Z)</div><span class="course-card-badge badge-a1" style="font-size:10px;padding:4px 10px">A1</span></div>
    <div class="alphabet-grid" id="alphaGrid"></div>

    <div class="sec-sub-label" style="margin-top:24px">Salomlashish iboralari</div>
    <div class="coll-card open">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#fef2f2">👋</div>
        <div class="coll-body"><div class="coll-title">Salomlashish</div><div class="coll-sub">Birinchi iboralar</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
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
    <div class="coll-card">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#f0fdf4">🙋</div>
        <div class="coll-body"><div class="coll-title">O'zingni tanishtirish</div><div class="coll-sub">My name is... I am from...</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
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
        <div class="sec-sub-label" style="margin-top:14px">Namuna suhbat</div>
        <div class="dialogue">
          <div class="bubble bubble-a"><div class="bubble-who">A</div><div class="bubble-en">Hello! My name is Sarah. What is your name?</div><div class="bubble-uz">Salom! Mening ismim Sarah. Ismingiz nima?</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">B</div><div class="bubble-en">Hi! My name is Ali. Nice to meet you!</div><div class="bubble-uz">Salom! Mening ismim Ali. Tanishganimdan xursandman!</div></div>
          <div class="bubble bubble-a"><div class="bubble-who">A</div><div class="bubble-en">Where are you from?</div><div class="bubble-uz">Qayerdansiz?</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">B</div><div class="bubble-en">I am from Uzbekistan. And you?</div><div class="bubble-uz">Men O'zbekistondan. Siz-chi?</div></div>
        </div>
      </div>
    </div>
  </div>

  <!-- ========== VOCABULARY PAGE ========== -->
  <div class="page" id="page-vocabulary">
    <div class="breadcrumb"><span onclick="navTo('home')" style="cursor:pointer">🏠 Bosh sahifa</span><span class="breadcrumb-sep">›</span><span class="breadcrumb-current">So'z boyligi</span></div>
    <div class="sec-head"><div class="sec-head-title"><div class="dot"></div>📚 So'z boyligi</div><span class="course-card-badge badge-a1" style="font-size:10px;padding:4px 10px">A1</span></div>
    <div class="coll-card open">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#fffbeb">🔢</div>
        <div class="coll-body"><div class="coll-title">Sonlar (1–100)</div><div class="coll-sub">Bosing va eshiting</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
        <div class="sec-sub-label">1–20</div><div class="num-grid" id="numGrid1"></div>
        <div class="sec-sub-label">O'nlar</div><div class="num-grid" id="numGrid2"></div>
      </div>
    </div>
    <div class="coll-card">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#fef2f2">🎨</div>
        <div class="coll-body"><div class="coll-title">Ranglar (Colors)</div><div class="coll-sub">Bosing va eshiting</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content"><div class="color-grid" id="colorGrid"></div></div>
    </div>
    <div class="coll-card">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#eff6ff">📅</div>
        <div class="coll-body"><div class="coll-title">Hafta kunlari &amp; Oylar</div><div class="coll-sub">Days &amp; Months</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
        <div class="sec-sub-label">Hafta kunlari</div>
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
        <div class="sec-sub-label">Oylar</div>
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
    <div class="coll-card">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#f0fdf4">👨‍👩‍👧‍👦</div>
        <div class="coll-body"><div class="coll-title">Oila a'zolari</div><div class="coll-sub">Family members</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
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
    <div class="coll-card">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#fef2f2">💼</div>
        <div class="coll-body"><div class="coll-title">Kasblar (Jobs)</div><div class="coll-sub">Mini test bilan!</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
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
        <div class="mini-quiz">
          <div class="mq-label">&#129513; MINI TEST — Kasblar</div>
          <div class="mq-q" id="mqqt">...</div>
          <div class="mq-opts" id="mqqo"></div>
          <button class="mq-next" id="mqqn" onclick="mqNext()">Keyingi &#9654;</button>
          <div class="mq-score" id="mqqs"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- ========== GRAMMAR QUEST PAGE ========== -->
  <div class="page" id="page-grammar">
    <div class="breadcrumb"><span onclick="navTo('home')" style="cursor:pointer">🏠 Bosh sahifa</span><span class="breadcrumb-sep">›</span><span class="breadcrumb-current">Grammar Quest</span></div>
    <div class="gram-quest-hero" id="gramHero">
      <div class="gqh-inner">
        <div class="gqh-top">
          <div class="gqh-badge">🎮 Grammar Quest</div>
          <button class="gqh-lb-btn" onclick="openLB()">🏆 Reyting</button>
        </div>
        <div class="gqh-title">Grammatika bosqichlari</div>
        <div class="gqh-sub">Har bir darsni o'rgan → Test topshir → Keyingi darajani oching</div>
        <div class="xp-track"><div class="xp-fill" id="gramXpFill" style="width:0%"></div></div>
        <div class="xp-label" id="gramXpLabel">XP: 0 / 700</div>
      </div>
    </div>
    <div id="lessonRoad" class="lesson-road"></div>
    <div id="lessonPanel" style="display:none">
      <div class="panel-header">
        <button class="ph-back" onclick="closeLessonPanel()">&#8592; Orqaga</button>
        <div style="flex:1;display:flex;align-items:center;gap:10px">
          <span class="ph-icon" id="lpIcon">📘</span>
          <div><div class="ph-title" id="lpTitle">Dars</div><div class="ph-sub" id="lpSub"></div></div>
        </div>
        <div class="ph-diff" id="lpDiff">A1</div>
      </div>
      <div id="lpContent"></div>
      <div style="text-align:center;margin:28px 0">
        <div class="start-test-note" id="startTestNote"></div>
        <button class="start-test-btn" onclick="startTest()">&#9999;&#65039; Testni boshlash</button>
      </div>
    </div>
    <div id="testPanel" style="display:none">
      <div class="panel-header">
        <button class="ph-back" onclick="backToLesson()">&#8592; Darsga qaytish</button>
        <div style="flex:1;display:flex;align-items:center;gap:10px">
          <span class="ph-icon">&#9999;&#65039;</span>
          <div><div class="ph-title" id="tpTitle">Test</div><div class="ph-sub" id="tpSub"></div></div>
        </div>
        <div class="ph-score" id="tpChip">0/0</div>
      </div>
      <div class="test-prog-wrap"><div class="test-prog-fill" id="tpBar" style="width:0%"></div></div>
      <div id="tpContent"></div>
    </div>
    <div id="resultPanel" style="display:none">
      <div class="result-card">
        <div class="result-icon" id="resultIcon">&#127881;</div>
        <div class="result-score" id="resultScore">85/100</div>
        <div class="result-msg" id="resultMsg">Ajoyib!</div>
        <div class="result-detail" id="resultDetail"></div>
        <div id="unlockBanner" class="unlock-banner" style="display:none">&#128275; Yangi dars ochildi!</div>
        <div class="result-btns">
          <button class="res-btn res-btn-retry" onclick="retryTest()">&#128260; Qayta</button>
          <button class="res-btn res-btn-next" id="rNextBtn" onclick="goNextLesson()" style="display:none">&#9654; Keyingi dars</button>
          <button class="res-btn res-btn-back" onclick="closeLessonPanel()">&#127968; Xaritaga</button>
        </div>
      </div>
    </div>
  </div>

  <!-- ========== ADVANCED PAGE ========== -->
  <div class="page" id="page-advanced">
    <div class="breadcrumb"><span onclick="navTo('home')" style="cursor:pointer">🏠 Bosh sahifa</span><span class="breadcrumb-sep">›</span><span class="breadcrumb-current">Ilg'or daraja</span></div>
    <div class="sec-head"><div class="sec-head-title"><div class="dot"></div>🚀 Ilg'or daraja</div><span class="course-card-badge badge-b1" style="font-size:10px;padding:4px 10px">B1</span></div>
    <div class="coll-card open">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#f0fdf4">⬆️</div>
        <div class="coll-body"><div class="coll-title">Future Simple — Kelasi zamon</div><div class="coll-sub">will bilan kelajak</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
        <div class="gram-box green"><strong>Tuzilishi:</strong> Subject + <strong>will</strong> + fe'l — Barcha shaxslar uchun bir xil!</div>
        <table class="data-table">
          <tr><th>Shakl</th><th>Misol</th><th>Tarjima</th></tr>
          <tr><td><span class="course-card-badge badge-a1">✅</span></td><td class="td-en">I will call you tomorrow.</td><td class="td-uz">Ertaga qo'ng'iroq qilaman.</td></tr>
          <tr><td><span class="course-card-badge badge-b1">❌</span></td><td class="td-en">She won't come today.</td><td class="td-uz">U bugun kelmaydi.</td></tr>
          <tr><td><span class="course-card-badge badge-a2">❓</span></td><td class="td-en">Will you help me?</td><td class="td-uz">Menga yordam berasizmi?</td></tr>
        </table>
        <div class="gram-box orange"><strong>will not = won't</strong> &nbsp;|&nbsp; I will = I'll &nbsp;|&nbsp; She will = She'll</div>
      </div>
    </div>
    <div class="coll-card">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#fef2f2">🎯</div>
        <div class="coll-body"><div class="coll-title">Modal Verbs</div><div class="coll-sub">can · should · must</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
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
    <div class="coll-card">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#fffbeb">📊</div>
        <div class="coll-body"><div class="coll-title">Comparison — Taqqoslash</div><div class="coll-sub">big → bigger → biggest</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
        <table class="data-table">
          <tr><th>Asl</th><th>Qiyosiy</th><th>Orttirma</th><th>Tarjima</th></tr>
          <tr><td class="td-en">big</td><td class="td-en">bigger</td><td class="td-en">the biggest</td><td class="td-uz">katta → kattaroq → eng katta</td></tr>
          <tr><td class="td-en">small</td><td class="td-en">smaller</td><td class="td-en">the smallest</td><td class="td-uz">kichik → kichikroq → eng kichik</td></tr>
          <tr><td class="td-en">fast</td><td class="td-en">faster</td><td class="td-en">the fastest</td><td class="td-uz">tez → tezroq → eng tez</td></tr>
          <tr><td class="td-en">good</td><td class="td-en">better</td><td class="td-en">the best</td><td class="td-uz">yaxshi → yaxshiroq → eng yaxshi</td></tr>
          <tr><td class="td-en">bad</td><td class="td-en">worse</td><td class="td-en">the worst</td><td class="td-uz">yomon → yomonroq → eng yomon</td></tr>
          <tr><td class="td-en">beautiful</td><td class="td-en">more beautiful</td><td class="td-en">the most beautiful</td><td class="td-uz">chiroyli → chiroliroq → eng chiroyli</td></tr>
        </table>
        <div class="gram-box" style="margin-top:10px">&#128207; <strong>Qisqa (1 bo'g'in):</strong> + er/est &rarr; bigger, biggest</div>
        <div class="gram-box green">&#128208; <strong>Uzun (2+ bo'g'in):</strong> more/most &rarr; more beautiful</div>
      </div>
    </div>
    <div class="coll-card">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#eff6ff">⬅️</div>
        <div class="coll-body"><div class="coll-title">Past Simple — O'tgan zamon</div><div class="coll-sub">Tugagan harakatlar</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
        <div class="gram-box"><strong>Tuzilishi:</strong> Subject + fe'l<strong>-ed</strong> yoki irregular 2-shakl</div>
        <table class="data-table">
          <tr><th>Shakl</th><th>Misol</th><th>Tarjima</th></tr>
          <tr><td><span class="course-card-badge badge-a1">✅</span></td><td class="td-en">I worked yesterday.</td><td class="td-uz">Men kecha ishladim.</td></tr>
          <tr><td><span class="course-card-badge badge-b1">❌</span></td><td class="td-en">I didn't work yesterday.</td><td class="td-uz">Men kecha ishlamadim.</td></tr>
          <tr><td><span class="course-card-badge badge-a2">❓</span></td><td class="td-en">Did you work yesterday?</td><td class="td-uz">Kecha ishladingizmi?</td></tr>
        </table>
        <div class="sec-sub-label">Notartibli fe'llar</div>
        <table class="data-table">
          <tr><th>Hozirgi</th><th>O'tgani</th><th>Tarjima</th></tr>
          <tr><td class="td-en">go</td><td class="td-en">went</td><td class="td-uz">bormoq</td></tr>
          <tr><td class="td-en">come</td><td class="td-en">came</td><td class="td-uz">kelmoq</td></tr>
          <tr><td class="td-en">see</td><td class="td-en">saw</td><td class="td-uz">ko'rmoq</td></tr>
          <tr><td class="td-en">eat</td><td class="td-en">ate</td><td class="td-uz">yemoq</td></tr>
          <tr><td class="td-en">drink</td><td class="td-en">drank</td><td class="td-uz">ichmoq</td></tr>
          <tr><td class="td-en">buy</td><td class="td-en">bought</td><td class="td-uz">sotib olmoq</td></tr>
          <tr><td class="td-en">say</td><td class="td-en">said</td><td class="td-uz">demoq</td></tr>
          <tr><td class="td-en">make</td><td class="td-en">made</td><td class="td-uz">yasamoq</td></tr>
          <tr><td class="td-en">take</td><td class="td-en">took</td><td class="td-uz">olmoq</td></tr>
          <tr><td class="td-en">get</td><td class="td-en">got</td><td class="td-uz">olmoq / bo'lmoq</td></tr>
        </table>
      </div>
    </div>
  </div>

  <!-- ========== CONVERSATION PAGE ========== -->
  <div class="page" id="page-conversation">
    <div class="breadcrumb"><span onclick="navTo('home')" style="cursor:pointer">🏠 Bosh sahifa</span><span class="breadcrumb-sep">›</span><span class="breadcrumb-current">Suhbat</span></div>
    <div class="sec-head"><div class="sec-head-title"><div class="dot"></div>💬 Suhbat</div><span class="course-card-badge badge-a2" style="font-size:10px;padding:4px 10px">A2</span></div>
    <div class="coll-card open">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#fffbeb">🛒</div>
        <div class="coll-body"><div class="coll-title">Do'konda suhbat</div><div class="coll-sub">Shopping conversation</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
        <div class="dialogue">
          <div class="bubble bubble-a"><div class="bubble-who">Sotuvchi</div><div class="bubble-en">Can I help you? <button class="spk-btn" onclick="sp('Can I help you?')">🔊</button></div><div class="bubble-uz">Sizga yordam bera olamanmi?</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">Mijoz</div><div class="bubble-en">Yes, I'm looking for a jacket.</div><div class="bubble-uz">Ha, men kurtka qidirmoqdaman.</div></div>
          <div class="bubble bubble-a"><div class="bubble-who">Sotuvchi</div><div class="bubble-en">What size do you need?</div><div class="bubble-uz">Qanday o'lcham kerak?</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">Mijoz</div><div class="bubble-en">Medium, please. How much is it?</div><div class="bubble-uz">O'rta. Narxi necha?</div></div>
          <div class="bubble bubble-a"><div class="bubble-who">Sotuvchi</div><div class="bubble-en">It's fifty dollars.</div><div class="bubble-uz">Ellik dollar.</div></div>
        </div>
        <div class="sec-sub-label" style="margin-top:14px">Foydali so'zlar</div>
        <table class="data-table">
          <tr><th>Inglizcha</th><th>O'zbekcha</th></tr>
          <tr><td class="td-en">How much is this? <button class="spk-btn" onclick="sp('How much is this?')">🔊</button></td><td class="td-uz">Bu qancha turadi?</td></tr>
          <tr><td class="td-en">That's too expensive.</td><td class="td-uz">Bu juda qimmat.</td></tr>
          <tr><td class="td-en">Do you have a discount?</td><td class="td-uz">Chegirma bormi?</td></tr>
          <tr><td class="td-en">I'll pay by card.</td><td class="td-uz">Karta bilan to'layman.</td></tr>
          <tr><td class="td-en">Can I try this on?</td><td class="td-uz">Kiyib ko'rsam bo'ladimi?</td></tr>
        </table>
      </div>
    </div>
    <div class="coll-card">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#fef2f2">🍽️</div>
        <div class="coll-body"><div class="coll-title">Restoranda suhbat</div><div class="coll-sub">At a restaurant</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
        <div class="dialogue">
          <div class="bubble bubble-a"><div class="bubble-who">Ofitsiant</div><div class="bubble-en">Good evening! Do you have a reservation?</div><div class="bubble-uz">Xayrli kech! Buyurtmangiz bormi?</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">Mehmon</div><div class="bubble-en">No, but we'd like a table for two.</div><div class="bubble-uz">Yo'q, lekin ikki kishilik stol kerak.</div></div>
          <div class="bubble bubble-a"><div class="bubble-who">Ofitsiant</div><div class="bubble-en">Of course! Here is the menu.</div><div class="bubble-uz">Albatta! Mana menyu.</div></div>
          <div class="bubble bubble-b"><div class="bubble-who">Mehmon</div><div class="bubble-en">I'd like chicken soup and rice, please.</div><div class="bubble-uz">Menga tovuq sho'rva va guruch bering.</div></div>
        </div>
      </div>
    </div>
    <div class="coll-card">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#f0fdf4">🗺️</div>
        <div class="coll-body"><div class="coll-title">Yo'l so'rash</div><div class="coll-sub">Asking for directions</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
        <table class="data-table">
          <tr><th>Inglizcha</th><th>O'zbekcha</th></tr>
          <tr><td class="td-en">Excuse me, where is the hospital? <button class="spk-btn" onclick="sp('Excuse me, where is the hospital?')">🔊</button></td><td class="td-uz">Kechirasiz, kasalxona qayerda?</td></tr>
          <tr><td class="td-en">Go straight. <button class="spk-btn" onclick="sp('Go straight.')">🔊</button></td><td class="td-uz">To'g'ri boring.</td></tr>
          <tr><td class="td-en">Turn left. <button class="spk-btn" onclick="sp('Turn left.')">🔊</button></td><td class="td-uz">Chapga buriling.</td></tr>
          <tr><td class="td-en">Turn right. <button class="spk-btn" onclick="sp('Turn right.')">🔊</button></td><td class="td-uz">O'ngga buriling.</td></tr>
          <tr><td class="td-en">It's near / far.</td><td class="td-uz">U yaqin / uzoq.</td></tr>
        </table>
      </div>
    </div>
    <div class="coll-card">
      <div class="coll-header" onclick="toggleColl(this)">
        <div class="coll-icon" style="background:#eff6ff">❓</div>
        <div class="coll-body"><div class="coll-title">Savol so'zlari</div><div class="coll-sub">What, Where, When, Why, How...</div></div>
        <span class="coll-arrow">▾</span>
      </div>
      <div class="coll-content">
        <table class="data-table">
          <tr><th>So'z</th><th>Tarjima</th><th>Misol</th></tr>
          <tr><td class="td-en">What?</td><td class="td-uz">Nima?</td><td class="td-en">What is your job?</td></tr>
          <tr><td class="td-en">Where?</td><td class="td-uz">Qayerda?</td><td class="td-en">Where do you live?</td></tr>
          <tr><td class="td-en">When?</td><td class="td-uz">Qachon?</td><td class="td-en">When is your birthday?</td></tr>
          <tr><td class="td-en">Why?</td><td class="td-uz">Nima uchun?</td><td class="td-en">Why are you sad?</td></tr>
          <tr><td class="td-en">Who?</td><td class="td-uz">Kim?</td><td class="td-en">Who is that man?</td></tr>
          <tr><td class="td-en">How?</td><td class="td-uz">Qanday?</td><td class="td-en">How do you feel?</td></tr>
          <tr><td class="td-en">How much?</td><td class="td-uz">Qancha?</td><td class="td-en">How much does it cost?</td></tr>
          <tr><td class="td-en">How many?</td><td class="td-uz">Nechta?</td><td class="td-en">How many students?</td></tr>
        </table>
      </div>
    </div>
  </div>

  <!-- ========== VOCAB GAME PAGE ========== -->
  <div class="page" id="page-game">
    <div class="breadcrumb"><span onclick="navTo('home')" style="cursor:pointer">🏠 Bosh sahifa</span><span class="breadcrumb-sep">›</span><span class="breadcrumb-current">So'z O'yini</span></div>
    <div class="sec-head"><div class="sec-head-title"><div class="dot"></div>⚡ So'z O'yini</div><span class="course-card-badge badge-game" style="font-size:10px;padding:4px 10px">O'yin</span></div>
    <div class="vocab-game-box">
      <div class="vg-scorebar">
        <div><div class="vg-pts" id="vgPts">0 pts</div><div style="font-size:11px;color:var(--gray-400)">Natija</div></div>
        <div style="text-align:center"><div class="vg-timer" id="vgTimer">15</div><div style="font-size:11px;color:var(--gray-400)">Soniya</div></div>
        <div style="text-align:right"><div class="vg-qnum" id="vgQnum">1/10</div><div style="font-size:11px;color:var(--gray-400)">Savol</div></div>
      </div>
      <div class="vg-timer-bar-wrap"><div class="vg-timer-bar" id="vgTimerBar" style="width:100%"></div></div>
      <div class="vg-word" id="vgWord">—</div>
      <div class="vg-hint">O'zbekcha tarjimasini toping:</div>
      <div class="vg-opts" id="vgOpts"></div>
      <div class="vg-result" id="vgResult">
        <div class="vg-result-icon" id="vgEndIcon">🎯</div>
        <div class="vg-result-score" id="vgEndScore">0 / 100</div>
        <div class="vg-result-msg" id="vgEndMsg">Yaxshi natija!</div>
        <button class="start-test-btn" onclick="startVG()">&#128260; Qayta o'ynash</button>
      </div>
    </div>
  </div>

  <!-- ========== PROGRESS PAGE ========== -->
  <div class="page" id="page-progress">
    <div class="breadcrumb"><span onclick="navTo('home')" style="cursor:pointer">🏠 Bosh sahifa</span><span class="breadcrumb-sep">›</span><span class="breadcrumb-current">Mening progressim</span></div>
    <div class="sec-head"><div class="sec-head-title"><div class="dot"></div>📊 Mening progressim</div></div>
    <div class="stats-grid">
      <div class="stat-card blue"><div class="stat-icon">⚡</div><div class="stat-val blue" id="progXP">0</div><div class="stat-label">Jami XP</div></div>
      <div class="stat-card green"><div class="stat-icon">🔥</div><div class="stat-val green" id="progStreak">0</div><div class="stat-label">Streak</div></div>
      <div class="stat-card amber"><div class="stat-icon">✅</div><div class="stat-val amber" id="progDone">0</div><div class="stat-label">Darslar o'tildi</div></div>
    </div>
    <div class="sec-head"><div class="sec-head-title"><div class="dot"></div>📈 Dars natijalari</div></div>
    <div id="progLessons"></div>
    <div class="sec-head" style="margin-top:24px"><div class="sec-head-title"><div class="dot"></div>🏅 Barcha yutuqlar</div></div>
    <div class="ach-grid" id="progAch"></div>
  </div>

</div><!-- /content -->

<!-- FOOTER -->
<footer id="footer">
  <div class="footer-grid">
    <div>
      <div class="footer-title">🌐 LinguaUz</div>
      <p style="font-size:12px;color:rgba(255,255,255,.5);line-height:1.7">O'zbek tilida ingliz tili o'rganish platformasi. Barcha funksiyalar bepul.</p>
    </div>
    <div>
      <div class="footer-title">📖 Darslar</div>
      <div class="footer-link" onclick="navTo('alphabet')">🔤 Alifbo</div>
      <div class="footer-link" onclick="navTo('vocabulary')">📚 So'z boyligi</div>
      <div class="footer-link" onclick="navTo('grammar')">🎮 Grammar Quest</div>
      <div class="footer-link" onclick="navTo('advanced')">🚀 Ilg'or daraja</div>
    </div>
    <div>
      <div class="footer-title">⚡ O'yinlar</div>
      <div class="footer-link" onclick="navTo('game')">So'z O'yini</div>
      <div class="footer-link" onclick="navTo('grammar')">Grammar Test</div>
      <div class="footer-link" onclick="openLB()">Global Reyting</div>
    </div>
    <div>
      <div class="footer-title">📞 Aloqa</div>
      <p style="font-size:12px;color:rgba(255,255,255,.5)">O'zbekiston</p>
      <p style="font-size:12px;color:rgba(255,255,255,.5);margin-top:4px">info@linguauz.uz</p>
    </div>
  </div>
  <div class="footer-bottom">
    <span>© 2025 LinguaUz — Barcha huquqlar himoyalangan</span>
    <span>O'zbek tilida ingliz tili platformasi</span>
  </div>
</footer>

<!-- LETTER MODAL -->
<div class="letter-modal-wrap" id="letterModal" onclick="if(event.target===this)closeLetterModal()">
  <div class="letter-modal-box">
    <div class="canvas-wrap"><canvas id="lc" width="480" height="480"></canvas></div>
    <div class="pbw"><div class="pbi" id="pb"></div></div>
    <div class="anim-ctrl">
      <button class="anim-btn" id="pbtn" onclick="togAnim()">&#9654; Ijro</button>
      <button class="anim-btn" onclick="reAnim()">&#8635; Qayta</button>
    </div>
    <div class="lm-letter" id="mlt">A a</div>
    <div class="lm-phone" id="mpr">[eɪ]</div>
    <div class="lm-examples" id="mex">Apple, Ant, Air</div>
    <div class="lm-words" id="mwr"></div>
    <button class="lm-speak" onclick="spkNow()">&#128266; Ovozini eshitish</button>
    <button class="lm-close" onclick="closeLetterModal()">&#10005; Yopish</button>
  </div>
</div>

<!-- LEADERBOARD MODAL -->
<div class="modal-wrap" id="lbModal" onclick="if(event.target===this)closeLB()">
  <div class="modal-box">
    <div class="modal-head">
      <div class="modal-title">&#127942; Global Reyting</div>
      <button class="modal-close" onclick="closeLB()">✕ Yopish</button>
    </div>
    <p style="font-size:12px;color:var(--gray-500);margin-bottom:12px">Ismingizni kiriting va natijangizni global reytingga saqlang!</p>
    <div class="lb-input-row">
      <input class="lb-input" id="lbName" placeholder="Ismingizni kiriting..." maxlength="20">
      <button class="lb-save" onclick="saveLBEntry()">Saqlash</button>
    </div>
    <div id="lbList"></div>
  </div>
</div>

<!-- TOAST CONTAINER -->
<div id="toasts"></div>
"""

with open('/home/claude/part2.html', 'w', encoding='utf-8') as f:
    f.write(body_html)
print("Part 2 written:", len(body_html))
