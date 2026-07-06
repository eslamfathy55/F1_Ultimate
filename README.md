# F1_Ultimate
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>F1 ULTRA 8K PRO MAX</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Titillium+Web:wght@400;700;900&display=swap');
    
    :root { --f1-red: #e10600; --f1-black: #000; }
    * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
    body { 
      font-family: 'Titillium Web', sans-serif;
      background: var(--f1-black); 
      color: #fff;
      overflow-x: hidden;
    }

    /* PRO MAX Header */
    header {
      position: fixed; width: 100%;
      background: rgba(0,0,0,0.98); backdrop-filter: blur(25px);
      padding: 15px 3%; z-index: 99999; 
      border-bottom: 4px solid var(--f1-red);
      display: flex; justify-content: space-between; align-items: center;
    }
    .logo { font-size: 2.5rem; font-weight: 900; color: var(--f1-red); text-shadow: 0 0 20px var(--f1-red); }
    nav a { color: #fff; text-decoration: none; margin: 0 10px; font-weight: 700; transition: 0.3s; }
    nav a:hover { color: var(--f1-red); }

    /* 8K Hero Video */
    .hero {
      height: 100vh; position: relative; display: flex; align-items: center; justify-content: center;
    }
    .hero video {
      position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; z-index: -1;
      filter: brightness(0.6);
    }
    .hero h1 { font-size: 10vw; font-weight: 900; text-shadow: 0 0 100px var(--f1-red); animation: pulse 2s infinite; }
    @keyframes pulse { 0%,100%{transform:scale(1);} 50%{transform:scale(1.05);} }

    /* Live Telemetry */
    .telemetry {
      background: linear-gradient(90deg, var(--f1-red), #ff0033);
      padding: 20px; display: flex; justify-content: space-around; font-weight: 900;
      position: sticky; top: 85px; z-index: 9999;
    }

    section { padding: 120px 3%; }
    h2 { font-size: 3.5rem; color: var(--f1-red); text-align: center; margin-bottom: 70px; }

    /* AI Chat Box */
    .ai-chat {
      background: rgba(255,255,255,0.05); border: 2px solid var(--f1-red); border-radius: 20px;
      padding: 30px; max-width: 800px; margin: 0 auto;
    }
    .ai-chat input {
      width: 100%; padding: 15px; background: #111; border: 1px solid var(--f1-red);
      color: #fff; border-radius: 10px; margin-top: 15px;
    }

    /* 3D Cards */
    .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 35px; }
    .card-3d {
      background: rgba(255,255,255,0.03); backdrop-filter: blur(20px);
      border: 2px solid rgba(225,6,0,0.5); border-radius: 25px; padding: 35px;
      transform-style: preserve-3d; transition: 0.5s;
    }
    .card-3d:hover { transform: rotateX(5deg) translateY(-20px); box-shadow: 0 30px 70px rgba(225,6,0,0.7); }

    /* Circuit 3D Map */
    .circuit-3d {
      background: rgba(255,255,255,0.04); border: 3px solid var(--f1-red);
      padding: 50px; margin: 40px 0; border-radius: 25px;
    }

    /* Pro Table */
    table { width: 100%; background: rgba(255,255,255,0.05); border-radius: 25px; overflow: hidden; border: 3px solid var(--f1-red); }
    th { background: linear-gradient(90deg, var(--f1-red), #ff2a00); padding: 22px; font-size: 1.2rem; }
    td { padding: 20px; text-align: center; border-bottom: 1px solid rgba(255,255,255,0.1); }

    /* Login System */
    .login-box {
      background: rgba(255,255,255,0.05); padding: 50px; border-radius: 25px;
      max-width: 500px; margin: 0 auto; border: 2px solid var(--f1-red);
    }
    .login-box input, .login-box button {
      width: 100%; padding: 15px; margin: 10px 0; border-radius: 10px; border: none;
    }
    .login-box button { background: var(--f1-red); color: #fff; font-weight: 900; font-size: 1.1rem; cursor: pointer; }

    footer { text-align: center; padding: 80px; background: #000; border-top: 4px solid var(--f1-red); }
  </style>
</head>
<body>

  <header>
    <div class="logo">F1 PRO MAX</div>
    <nav>
      <a href="#home">الرئيسية</a>
      <a href="#ai">AI</a>
      <a href="#telemetry">لايف</a>
      <a href="#teams">الفرق</a>
      <a href="#3d">3D</a>
      <a href="#shop">المتجر</a>
      <a href="#login">الحساب</a>
    </nav>
  </header>

  <div class="telemetry">
    <span>🏎️ Verstappen: 312.5 كم/س</span>
    <span>⏱️ أفضل لفة: 1:21.345</span>
    <span>🔴 LIVE: FP3 Egypt GP</span>
  </div>

  <section class="hero" id="home">
    <video autoplay muted loop>
      <source src="https://videos.pexels.com/video-files/1203463/1203463-hd_1920_1080_30fps.mp4" type="video/mp4">
    </video>
    <div>
      <h1>PRO MAX</h1>
      <p style="font-size: 2.2rem;">8K + AI + 3D + كل شي</p>
    </div>
  </section>

  <!-- AI SECTION -->
  <section id="ai">
    <h2>F1 AI ASSISTANT</h2>
    <div class="ai-chat">
      <h3>اسأل الـ AI عن أي شي في F1</h3>
      <input type="text" placeholder="مثال: من سيفوز في سباق مصر؟">
      <p style="margin-top: 15px; color: #888;">الـ AI يحلل البيانات ويعطيك توقعات 8K</p>
    </div>
  </section>

  <!-- 3D TEAMS -->
  <section id="3d">
    <h2>الفرق بتقنية 3D</h2>
    <div class="grid">
      <div class="card-3d">
        <h3>Red Bull RB21</h3>
        <p><b>المحرك:</b> 1000 حصان هايبرد</p>
        <p><b>الوزن:</b> 798 كجم</p>
        <p><b>التسارع:</b> 0-100 في 2.4 ثانية</p>
      </div>
      <div class="card-3d">
        <h3>Ferrari SF-26</h3>
        <p><b>المحرك:</b> 1000 حصان هايبرد</p>
        <p><b>الوزن:</b> 798 كجم</p>
        <p><b>السرعة القصوى:</b> 375 كم/س</p>
      </div>
    </div>
  </section>

  <!-- CIRCUIT 3D -->
  <section id="circuits">
    <h2>حلبة مصر 3D</h2>
    <div class="circuit-3d">
      <h3>🇪🇬 El Alamein Circuit - 8K 3D</h3>
      <p><b>عدد المنعطفات:</b> 18 منعطف</p>
      <p><b>أطول مستقيم:</b> 1.2 كم</p>
      <p><b>DRS Zones:</b> 3 مناطق</p>
      <p><b>الوصف:</b> أول حلبة ساحلية في أفريقيا. تصميم 3D تفاعلي</p>
    </div>
  </section>

  <!-- SHOP PRO -->
  <section id="shop">
    <h2>متجر PRO MAX</h2>
    <div class="grid">
      <div class="card-3d">
        <h3>نظارة VR للسباقات</h3>
        <p>$499</p>
        <button style="background:var(--f1-red); padding:12px 30px; border:none; border-radius:10px; color:#fff; font-weight:900;">اشتري</button>
      </div>
      <div class="card-3d">
        <h3>مقود F1 Pro</h3>
        <p>$899</p>
        <button style="background:var(--f1-red); padding:12px 30px; border:none; border-radius:10px; color:#fff; font-weight:900;">اشتري</button>
      </div>
    </div>
  </section>

  <!-- LOGIN SYSTEM -->
  <section id="login">
    <h2>حساب F1 PRO MAX</h2>
    <div class="login-box">
      <h3>سجل دخولك</h3>
      <input type="email" placeholder="الإيميل">
      <input type="password" placeholder="كلمة السر">
      <button>دخول</button>
      <p style="text-align:center; margin-top:15px;">احصل على بث 8K حصري</p>
    </div>
  </section>

  <footer>
    <p>© 2026 F1 ULTRA 8K PRO MAX | AI Powered | 3D Racing | صنع في Shebin Al-Kom 👑</p>
  </footer>

</body>
</html><!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>F1 ULTRA 8K PRO MAX</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Titillium+Web:wght@400;700;900&display=swap');
    
    :root { --f1-red: #e10600; --f1-black: #000; }
    * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
    body { 
      font-family: 'Titillium Web', sans-serif;
      background: var(--f1-black); 
      color: #fff;
      overflow-x: hidden;
    }

    /* PRO MAX Header */
    header {
      position: fixed; width: 100%;
      background: rgba(0,0,0,0.98); backdrop-filter: blur(25px);
      padding: 15px 3%; z-index: 99999; 
      border-bottom: 4px solid var(--f1-red);
      display: flex; justify-content: space-between; align-items: center;
    }
    .logo { font-size: 2.5rem; font-weight: 900; color: var(--f1-red); text-shadow: 0 0 20px var(--f1-red); }
    nav a { color: #fff; text-decoration: none; margin: 0 10px; font-weight: 700; transition: 0.3s; }
    nav a:hover { color: var(--f1-red); }

    /* 8K Hero Video */
    .hero {
      height: 100vh; position: relative; display: flex; align-items: center; justify-content: center;
    }
    .hero video {
      position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; z-index: -1;
      filter: brightness(0.6);
    }
    .hero h1 { font-size: 10vw; font-weight: 900; text-shadow: 0 0 100px var(--f1-red); animation: pulse 2s infinite; }
    @keyframes pulse { 0%,100%{transform:scale(1);} 50%{transform:scale(1.05);} }

    /* Live Telemetry */
    .telemetry {
      background: linear-gradient(90deg, var(--f1-red), #ff0033);
      padding: 20px; display: flex; justify-content: space-around; font-weight: 900;
      position: sticky; top: 85px; z-index: 9999;
    }

    section { padding: 120px 3%; }
    h2 { font-size: 3.5rem; color: var(--f1-red); text-align: center; margin-bottom: 70px; }

    /* AI Chat Box */
    .ai-chat {
      background: rgba(255,255,255,0.05); border: 2px solid var(--f1-red); border-radius: 20px;
      padding: 30px; max-width: 800px; margin: 0 auto;
    }
    .ai-chat input {
      width: 100%; padding: 15px; background: #111; border: 1px solid var(--f1-red);
      color: #fff; border-radius: 10px; margin-top: 15px;
    }

    /* 3D Cards */
    .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 35px; }
    .card-3d {
      background: rgba(255,255,255,0.03); backdrop-filter: blur(20px);
      border: 2px solid rgba(225,6,0,0.5); border-radius: 25px; padding: 35px;
      transform-style: preserve-3d; transition: 0.5s;
    }
    .card-3d:hover { transform: rotateX(5deg) translateY(-20px); box-shadow: 0 30px 70px rgba(225,6,0,0.7); }

    /* Circuit 3D Map */
    .circuit-3d {
      background: rgba(255,255,255,0.04); border: 3px solid var(--f1-red);
      padding: 50px; margin: 40px 0; border-radius: 25px;
    }

    /* Pro Table */
    table { width: 100%; background: rgba(255,255,255,0.05); border-radius: 25px; overflow: hidden; border: 3px solid var(--f1-red); }
    th { background: linear-gradient(90deg, var(--f1-red), #ff2a00); padding: 22px; font-size: 1.2rem; }
    td { padding: 20px; text-align: center; border-bottom: 1px solid rgba(255,255,255,0.1); }

    /* Login System */
    .login-box {
      background: rgba(255,255,255,0.05); padding: 50px; border-radius: 25px;
      max-width: 500px; margin: 0 auto; border: 2px solid var(--f1-red);
    }
    .login-box input, .login-box button {
      width: 100%; padding: 15px; margin: 10px 0; border-radius: 10px; border: none;
    }
    .login-box button { background: var(--f1-red); color: #fff; font-weight: 900; font-size: 1.1rem; cursor: pointer; }

    footer { text-align: center; padding: 80px; background: #000; border-top: 4px solid var(--f1-red); }
  </style>
</head>
<body>

  <header>
    <div class="logo">F1 PRO MAX</div>
    <nav>
      <a href="#home">الرئيسية</a>
      <a href="#ai">AI</a>
      <a href="#telemetry">لايف</a>
      <a href="#teams">الفرق</a>
      <a href="#3d">3D</a>
      <a href="#shop">المتجر</a>
      <a href="#login">الحساب</a>
    </nav>
  </header>

  <div class="telemetry">
    <span>🏎️ Verstappen: 312.5 كم/س</span>
    <span>⏱️ أفضل لفة: 1:21.345</span>
    <span>🔴 LIVE: FP3 Egypt GP</span>
  </div>

  <section class="hero" id="home">
    <video autoplay muted loop>
      <source src="https://videos.pexels.com/video-files/1203463/1203463-hd_1920_1080_30fps.mp4" type="video/mp4">
    </video>
    <div>
      <h1>PRO MAX</h1>
      <p style="font-size: 2.2rem;">8K + AI + 3D + كل شي</p>
    </div>
  </section>

  <!-- AI SECTION -->
  <section id="ai">
    <h2>F1 AI ASSISTANT</h2>
    <div class="ai-chat">
      <h3>اسأل الـ AI عن أي شي في F1</h3>
      <input type="text" placeholder="مثال: من سيفوز في سباق مصر؟">
      <p style="margin-top: 15px; color: #888;">الـ AI يحلل البيانات ويعطيك توقعات 8K</p>
    </div>
  </section>

  <!-- 3D TEAMS -->
  <section id="3d">
    <h2>الفرق بتقنية 3D</h2>
    <div class="grid">
      <div class="card-3d">
        <h3>Red Bull RB21</h3>
        <p><b>المحرك:</b> 1000 حصان هايبرد</p>
        <p><b>الوزن:</b> 798 كجم</p>
        <p><b>التسارع:</b> 0-100 في 2.4 ثانية</p>
      </div>
      <div class="card-3d">
        <h3>Ferrari SF-26</h3>
        <p><b>المحرك:</b> 1000 حصان هايبرد</p>
        <p><b>الوزن:</b> 798 كجم</p>
        <p><b>السرعة القصوى:</b> 375 كم/س</p>
      </div>
    </div>
  </section>

  <!-- CIRCUIT 3D -->
  <section id="circuits">
    <h2>حلبة مصر 3D</h2>
    <div class="circuit-3d">
      <h3>🇪🇬 El Alamein Circuit - 8K 3D</h3>
      <p><b>عدد المنعطفات:</b> 18 منعطف</p>
      <p><b>أطول مستقيم:</b> 1.2 كم</p>
      <p><b>DRS Zones:</b> 3 مناطق</p>
      <p><b>الوصف:</b> أول حلبة ساحلية في أفريقيا. تصميم 3D تفاعلي</p>
    </div>
  </section>

  <!-- SHOP PRO -->
  <section id="shop">
    <h2>متجر PRO MAX</h2>
    <div class="grid">
      <div class="card-3d">
        <h3>نظارة VR للسباقات</h3>
        <p>$499</p>
        <button style="background:var(--f1-red); padding:12px 30px; border:none; border-radius:10px; color:#fff; font-weight:900;">اشتري</button>
      </div>
      <div class="card-3d">
        <h3>مقود F1 Pro</h3>
        <p>$899</p>
        <button style="background:var(--f1-red); padding:12px 30px; border:none; border-radius:10px; color:#fff; font-weight:900;">اشتري</button>
      </div>
    </div>
  </section>

  <!-- LOGIN SYSTEM -->
  <section id="login">
    <h2>حساب F1 PRO MAX</h2>
    <div class="login-box">
      <h3>سجل دخولك</h3>
      <input type="email" placeholder="الإيميل">
      <input type="password" placeholder="كلمة السر">
      <button>دخول</button>
      <p style="text-align:center; margin-top:15px;">احصل على بث 8K حصري</p>
    </div>
  </section>

  <footer>
    <p>© 2026 F1 ULTRA 8K PRO MAX | AI Powered | 3D Racing | صنع في Shebin Al-Kom 👑</p>
  </footer>

</body>
</html><!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>F1 ULTRA 8K PRO MAX</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Titillium+Web:wght@400;700;900&display=swap');
    
    :root { --f1-red: #e10600; --f1-black: #000; }
    * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
    body { 
      font-family: 'Titillium Web', sans-serif;
      background: var(--f1-black); 
      color: #fff;
      overflow-x: hidden;
    }

    /* PRO MAX Header */
    header {
      position: fixed; width: 100%;
      background: rgba(0,0,0,0.98); backdrop-filter: blur(25px);
      padding: 15px 3%; z-index: 99999; 
      border-bottom: 4px solid var(--f1-red);
      display: flex; justify-content: space-between; align-items: center;
    }
    .logo { font-size: 2.5rem; font-weight: 900; color: var(--f1-red); text-shadow: 0 0 20px var(--f1-red); }
    nav a { color: #fff; text-decoration: none; margin: 0 10px; font-weight: 700; transition: 0.3s; }
    nav a:hover { color: var(--f1-red); }

    /* 8K Hero Video */
    .hero {
      height: 100vh; position: relative; display: flex; align-items: center; justify-content: center;
    }
    .hero video {
      position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; z-index: -1;
      filter: brightness(0.6);
    }
    .hero h1 { font-size: 10vw; font-weight: 900; text-shadow: 0 0 100px var(--f1-red); animation: pulse 2s infinite; }
    @keyframes pulse { 0%,100%{transform:scale(1);} 50%{transform:scale(1.05);} }

    /* Live Telemetry */
    .telemetry {
      background: linear-gradient(90deg, var(--f1-red), #ff0033);
      padding: 20px; display: flex; justify-content: space-around; font-weight: 900;
      position: sticky; top: 85px; z-index: 9999;
    }

    section { padding: 120px 3%; }
    h2 { font-size: 3.5rem; color: var(--f1-red); text-align: center; margin-bottom: 70px; }

    /* AI Chat Box */
    .ai-chat {
      background: rgba(255,255,255,0.05); border: 2px solid var(--f1-red); border-radius: 20px;
      padding: 30px; max-width: 800px; margin: 0 auto;
    }
    .ai-chat input {
      width: 100%; padding: 15px; background: #111; border: 1px solid var(--f1-red);
      color: #fff; border-radius: 10px; margin-top: 15px;
    }

    /* 3D Cards */
    .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 35px; }
    .card-3d {
      background: rgba(255,255,255,0.03); backdrop-filter: blur(20px);
      border: 2px solid rgba(225,6,0,0.5); border-radius: 25px; padding: 35px;
      transform-style: preserve-3d; transition: 0.5s;
    }
    .card-3d:hover { transform: rotateX(5deg) translateY(-20px); box-shadow: 0 30px 70px rgba(225,6,0,0.7); }

    /* Circuit 3D Map */
    .circuit-3d {
      background: rgba(255,255,255,0.04); border: 3px solid var(--f1-red);
      padding: 50px; margin: 40px 0; border-radius: 25px;
    }

    /* Pro Table */
    table { width: 100%; background: rgba(255,255,255,0.05); border-radius: 25px; overflow: hidden; border: 3px solid var(--f1-red); }
    th { background: linear-gradient(90deg, var(--f1-red), #ff2a00); padding: 22px; font-size: 1.2rem; }
    td { padding: 20px; text-align: center; border-bottom: 1px solid rgba(255,255,255,0.1); }

    /* Login System */
    .login-box {
      background: rgba(255,255,255,0.05); padding: 50px; border-radius: 25px;
      max-width: 500px; margin: 0 auto; border: 2px solid var(--f1-red);
    }
    .login-box input, .login-box button {
      width: 100%; padding: 15px; margin: 10px 0; border-radius: 10px; border: none;
    }
    .login-box button { background: var(--f1-red); color: #fff; font-weight: 900; font-size: 1.1rem; cursor: pointer; }

    footer { text-align: center; padding: 80px; background: #000; border-top: 4px solid var(--f1-red); }
  </style>
</head>
<body>

  <header>
    <div class="logo">F1 PRO MAX</div>
    <nav>
      <a href="#home">الرئيسية</a>
      <a href="#ai">AI</a>
      <a href="#telemetry">لايف</a>
      <a href="#teams">الفرق</a>
      <a href="#3d">3D</a>
      <a href="#shop">المتجر</a>
      <a href="#login">الحساب</a>
    </nav>
  </header>

  <div class="telemetry">
    <span>🏎️ Verstappen: 312.5 كم/س</span>
    <span>⏱️ أفضل لفة: 1:21.345</span>
    <span>🔴 LIVE: FP3 Egypt GP</span>
  </div>

  <section class="hero" id="home">
    <video autoplay muted loop>
      <source src="https://videos.pexels.com/video-files/1203463/1203463-hd_1920_1080_30fps.mp4" type="video/mp4">
    </video>
    <div>
      <h1>PRO MAX</h1>
      <p style="font-size: 2.2rem;">8K + AI + 3D + كل شي</p>
    </div>
  </section>

  <!-- AI SECTION -->
  <section id="ai">
    <h2>F1 AI ASSISTANT</h2>
    <div class="ai-chat">
      <h3>اسأل الـ AI عن أي شي في F1</h3>
      <input type="text" placeholder="مثال: من سيفوز في سباق مصر؟">
      <p style="margin-top: 15px; color: #888;">الـ AI يحلل البيانات ويعطيك توقعات 8K</p>
    </div>
  </section>

  <!-- 3D TEAMS -->
  <section id="3d">
    <h2>الفرق بتقنية 3D</h2>
    <div class="grid">
      <div class="card-3d">
        <h3>Red Bull RB21</h3>
        <p><b>المحرك:</b> 1000 حصان هايبرد</p>
        <p><b>الوزن:</b> 798 كجم</p>
        <p><b>التسارع:</b> 0-100 في 2.4 ثانية</p>
      </div>
      <div class="card-3d">
        <h3>Ferrari SF-26</h3>
        <p><b>المحرك:</b> 1000 حصان هايبرد</p>
        <p><b>الوزن:</b> 798 كجم</p>
        <p><b>السرعة القصوى:</b> 375 كم/س</p>
      </div>
    </div>
  </section>

  <!-- CIRCUIT 3D -->
  <section id="circuits">
    <h2>حلبة مصر 3D</h2>
    <div class="circuit-3d">
      <h3>🇪🇬 El Alamein Circuit - 8K 3D</h3>
      <p><b>عدد المنعطفات:</b> 18 منعطف</p>
      <p><b>أطول مستقيم:</b> 1.2 كم</p>
      <p><b>DRS Zones:</b> 3 مناطق</p>
      <p><b>الوصف:</b> أول حلبة ساحلية في أفريقيا. تصميم 3D تفاعلي</p>
    </div>
  </section>

  <!-- SHOP PRO -->
  <section id="shop">
    <h2>متجر PRO MAX</h2>
    <div class="grid">
      <div class="card-3d">
        <h3>نظارة VR للسباقات</h3>
        <p>$499</p>
        <button style="background:var(--f1-red); padding:12px 30px; border:none; border-radius:10px; color:#fff; font-weight:900;">اشتري</button>
      </div>
      <div class="card-3d">
        <h3>مقود F1 Pro</h3>
        <p>$899</p>
        <button style="background:var(--f1-red); padding:12px 30px; border:none; border-radius:10px; color:#fff; font-weight:900;">اشتري</button>
      </div>
    </div>
  </section>

  <!-- LOGIN SYSTEM -->
  <section id="login">
    <h2>حساب F1 PRO MAX</h2>
    <div class="login-box">
      <h3>سجل دخولك</h3>
      <input type="email" placeholder="الإيميل">
      <input type="password" placeholder="كلمة السر">
      <button>دخول</button>
      <p style="text-align:center; margin-top:15px;">احصل على بث 8K حصري</p>
    </div>
  </section>

  <footer>
    <p>© 2026 F1 ULTRA 8K PRO MAX | AI Powered | 3D Racing | صنع في Shebin Al-Kom 👑</p>
  </footer>

</body>
</html>
