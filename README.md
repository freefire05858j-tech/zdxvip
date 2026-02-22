# habib-vip-hok
habib-hok
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SHAMIM VIP TRADER</title>
<style>
/* ================= BASE ================= */
*{margin:0;padding:0;box-sizing:border-box;}
:root{--vh:100vh;}
html,body{width:100%;height:calc(var(--vh)*1);background:#000;overflow:hidden;font-family:Arial,sans-serif;}
iframe{width:100%;height:calc(var(--vh)*1);border:none;display:none;}

/* ================= FONTS ================= */
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@700;900&display=swap');

/*===== VIP PREMIUM RED RGB LOGIN ====*/

.login{position:fixed;inset:0;display:flex;align-items:center;justify-content:center;background:radial-gradient(circle,#111,#000);z-index:999999;backdrop-filter:blur(15px);transition:all .25s}
.login-box{position:relative;width:340px;padding:45px 35px;border-radius:35px;text-align:center;background:#0d0d0d;border:1px solid rgba(255,255,255,.05);overflow:hidden;z-index:1;animation:shadowGlowFlow 8s linear infinite}
.login-box::before{content:'';position:absolute;top:-50%;left:-50%;width:200%;height:200%;background:conic-gradient(#f00,#ff8000,#ff0,#0f0,#0ff,#00f,#8000ff,#f0f,#f00);animation:rotateBorder 6s linear infinite;z-index:-1}
.login-box::after{content:'';position:absolute;inset:3px;background:#0d0d0d;border-radius:10px;z-index:-1}
.login-box h3{color:#fff;font:900 20px 'Arial';margin-bottom:35px;text-transform:uppercase;letter-spacing:2px;white-space:nowrap;background:linear-gradient(90deg,#f00,#0f0,#0ff,#f00);background-size:300%;-webkit-background-clip:text;-webkit-text-fill-color:transparent;animation:textFlow 5s linear infinite}
.login-box input{width:100%;padding:16px;border-radius:15px;background:rgba(255,255,255,.03);color:#fff;border:1px solid rgba(255,255,255,.1);text-align:center;font-size:18px;outline:none;box-sizing:border-box}
.login-btn{width:100%;margin-top:25px;padding:14px;border-radius:50px;font:900 16px 'Arial';text-transform:uppercase;border:none;background:linear-gradient(45deg,#8b0000,#f00);color:#fff;cursor:pointer;box-shadow:0 5px 15px rgba(255,0,0,.3);transition:.4s;position:relative;overflow:hidden}
.login-btn:hover{background:linear-gradient(45deg,#f00,#ff4d4d);box-shadow:0 0 25px rgba(255,0,0,.7);transform:translateY(-2px) scale(1.02)}
@keyframes rotateBorder{to{transform:rotate(360deg)}}
@keyframes textFlow{to{background-position:300%}}
@keyframes shadowGlowFlow{0%,100%{box-shadow:0 0 25px rgba(255,0,0,.6)}25%{box-shadow:0 0 25px rgba(0,255,0,.6)}50%{box-shadow:0 0 25px rgba(0,255,255,.6)}75%{box-shadow:0 0 25px rgba(255,0,255,.6)}}



/* CHOICE PAGE COMPACT VIP */
#choicePage {
  position: fixed;
  inset: 0;
  display: none;
  flex-direction: column;
  align-items: center;
  background: radial-gradient(circle, #1a1a1a, #000);
  z-index: 999999;
  overflow-y: auto;
  padding: 129px 10px 40px;
  backdrop-filter: blur(10px);
}

.choice-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 18px;
  width: 100%;
  max-width: 420px;
}

/* NOTICE BOX */
.notice-box.glass {
  width: 95%;
  background: rgba(10, 10, 10, 0.9);
  border: 4px solid #fff;
  border-radius: 22px;
  padding: 18px 10px;
  box-sizing: border-box;
  text-align: center;
  box-shadow: 0 0 15px rgba(255, 255, 255, 0.15);
  animation: cleanSwing 5s infinite alternate ease-in-out;
}

@keyframes cleanSwing { to { transform: translateY(-8px); } }

.notice-box h2 {
  font: 900 22px 'Arial';
  color: #fff;
  margin-bottom: 12px;
  text-transform: uppercase;
  text-shadow: 0 0 8px #fff;
}

.notice-list {
  padding: 0;
  list-style: none;
  margin: 0 auto;
  display: inline-block;
  text-align: left;
}

.notice-list li {
  font: 900 18px 'Arial';
  color: #fff;
  margin-bottom: 10px;
  white-space: nowrap;
  display: block;
}

.notice-list li::before {
  content: '';
  color: #ff2b2b;
  margin-right: 10px;
  font-size: 14px;
  animation: blinkNotice 1.5s infinite;
  display: inline-block;
}

@keyframes blinkNotice { 50% { opacity: 0.4; } }

/* BUTTONS */
.admin-buttons, .engine-buttons-extra {
  display: flex;
  justify-content: center;
  gap: 10px;
  width: 100%;
  margin-top: 12px;
}

.admin-btn, .telegram-btn {
  width: 135px;
  padding: 11px 0;
  font: 900 13px 'Arial';
  border-radius: 12px;
  border: none;
  cursor: pointer;
  text-transform: uppercase;
  box-shadow: 0 4px 10px rgba(0,0,0,0.4);
}

.admin-btn { background: #4bff99; color: #000; }
.telegram-btn { background: #00acee; color: #fff; }

/* COUNTDOWN */
.countdown {
  font: 900 16px 'Arial';
  color: #f6c96b;
  border: 1.5px solid #f6c96b;
  padding: 6px 15px;
  border-radius: 10px;
  margin: 15px 0;
  display: inline-block;
  animation: glowCountdown 2s infinite alternate;
}

@keyframes glowCountdown { to { box-shadow: 0 0 12px #f6c96b; } }

/* ENGINE BOX */
.engine-box {
  width: 96%;
  background: rgba(10, 10, 10, 0.95);
  border-radius: 28px;
  padding: 22px 10px;
  border: 3.5px solid #fff;
  box-sizing: border-box;
  text-align: center;
  animation: shadowFlow 8s infinite alternate;
}

@keyframes shadowFlow {
  0% { box-shadow: 0 0 18px #ff4d4d; border-color: #ff4d4d; }
  50% { box-shadow: 0 0 18px #0ff; border-color: #0ff; }
  100% { box-shadow: 0 0 18px #f0f; border-color: #f0f; }
}

.engine-title {
  font: 900 28px 'Arial';
  color: #fff;
  margin-bottom: 18px;
  text-shadow: 0 0 10px rgba(255, 255, 255, 0.3);
}

.engine-buttons {
  display: flex;
  justify-content: center;
  gap: 12px;
  width: 100%;
}

.engine-btn {
  flex: 1;
  max-width: 140px;
  padding: 15px 0;
  font: 900 20px 'Arial';
  border-radius: 16px;
  border: none;
  animation: btnSwing 4s infinite alternate;
}

.dk-btn { background: #fff; color: #000; }
.hz-btn { background: #ff4d4d; color: #fff; }

@keyframes btnSwing { to { transform: translateY(-5px); } }

.developer-signature {
  font: 900 9px 'Arial';
  color: rgba(255, 255, 255, 0.3);
  margin-top: 15px;
  letter-spacing: 1px;
}



/* VIP Iframe */
#iframe{display:none;width:100%;height:calc(var(--vh)*1);border:none;}

/* LIVE BAR */
.live-bar{position:fixed;top:16px;left:50%;transform:translateX(-50%);background:#111;padding:7px 18px;border-radius:22px;font-size:11px;font-weight:900;color:#fff;opacity:0;display:flex;align-items:center;gap:8px;z-index:99999;animation:liveGlow 3s infinite;border:3.5px solid rgba(255,255,255,.12);}
.live-bar.show{opacity:1;}
@keyframes liveGlow{0%,100%{box-shadow:0 0 18px #ff3b3b;}50%{box-shadow:0 0 30px #ff8585;}}
.live-dot{width:8px;height:7px;border-radius:50%;background:#ff2d2d;animation:blink 1.2s infinite;}
@keyframes blink{0%,100%{opacity:.3;}50%{opacity:1;}}

/* === LOADER UPDATED === */
.realLoader{
  width:34px;                /* আগের 25px → বড় করা হয়েছে */
  height:34px;               /* আগের 25px → বড় করা হয়েছে */
  border:4px solid rgba(255,255,255,0.3); 
  border-top:4px solid #fff;
  border-radius:50%;
  margin:8px auto;           /* মার্জিন সামান্য বাড়ানো */
  animation: spin 1s linear infinite;
}

@keyframes spin{
  100%{transform: rotate(360deg);}
}

/* ================= FX BOX ================= */
.fx-box {
  position: fixed;
  top: 120px;
  left: 40px;
  width: 220px;
  padding: 14px 10px;
  border-radius: 14px;
  text-align: center;
  background: #000; /* কালো বেজ */
  border: 2px solid #fff; /* সাদা বর্ডার */
  box-shadow: 0 0 16px #fff33, 0 0 32px #fff22; /* initial soft glow, বড় এবং গাঢ় */
  animation: fxBoxSwing 8s infinite ease-in-out; /* হালকা swing */
  touch-action: none;
  z-index: 9999;
  font-family: 'Orbitron', 'Arial', sans-serif;
  transform-origin: center;
  transition: box-shadow 1s ease; /* smooth color change */
}

/* Soft Swing Animation */
@keyframes fxBoxSwing {
  0%   { transform: translateX(-8px) translateY(0px) rotate(-0.3deg) scale(1); }
  25%  { transform: translateX(6px) translateY(-2px) rotate(0.2deg) scale(1.01); }
  50%  { transform: translateX(8px) translateY(0px) rotate(0deg) scale(1.02); }
  75%  { transform: translateX(-6px) translateY(2px) rotate(-0.2deg) scale(1.01); }
  100% { transform: translateX(-8px) translateY(0px) rotate(-0.3deg) scale(1); }
}

/* RESULT TEXT */
.result {
  font-weight: 900;
  text-align: center;
  transition: color 0.5s ease, text-shadow 0.5s ease, transform 0.3s ease;
  text-shadow: 0 0 4px rgba(255,255,255,0.2); /* সফ্ট, চোখে আরামদায়ক */
}

/* BIG */
.big {
  font-size: 38px;
  font-weight: 900;
  font-family: 'Orbitron', 'Arial', sans-serif;
  color: #ff4d4d;
  text-shadow: 0 0 2px rgba(255,255,255,0.15), 0 0 6px rgba(255,255,255,0.1);
  transition: color 0.5s, text-shadow 0.5s;
}

/* SMALL */
.small {
  font-size: 34px;
  font-weight: 900;
  font-family: 'Orbitron', 'Arial', sans-serif;
  color: #38ff9c;
  text-shadow: 0 0 2px rgba(255,255,255,0.15), 0 0 6px rgba(255,255,255,0.1);
  transition: color 0.5s, text-shadow 0.5s;
}

/* FX TITLE & SUB */
.fx-title {
  font-size: 12px;
  font-weight: 900;
  color: #fff;
  cursor: pointer;
  text-shadow: 0 0 4px rgba(255,255,255,0.2);
}
.fx-sub {
  font-size: 10px;
  color: #f6c96b;
  text-shadow: 0 0 4px rgba(255,255,255,0.15);
}

/* TIMER & CLOCK */
#rt {
  font-size: 20px;
  font-weight: 900;
  color: #fff;
  text-shadow: 0 0 4px rgba(255,255,255,0.2);
}
.clock-row { display:flex; justify-content:center; gap:6px; margin-top:6px; }
#clock { font-size:14px; color:#bbb; text-shadow:0 0 4px rgba(255,255,255,0.2); 

}

/* ================= ERROR POPUP ================= */
#errorPopup {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: rgba(0,0,0,0.95); /* কালো ব্যাকগ্রাউন্ড */
  padding: 36px 48px;
  border-radius: 22px;
  border: 3px solid #3399ff; /* নীল সেডু বর্ডার */
  box-shadow: 0 0 30px rgba(51,153,255,0.4); /* subtle blue glow */
  z-index: 999999;
  text-align: left;
  font-family: 'Orbitron', sans-serif;
  max-width: 420px;
}

/* Invalid password text */
#errorPopup div {
  font-weight: 900;
  font-size: 40px;
  color: #ffffff; /* সাদা লেখা */
  margin-bottom: 40px;
  gap:50px; /* spacing between notices + engine box */
  width:100%;

}

/* OK button */
#errorPopup button {
  padding: 10px 20px;
  border: none;
  background: transparent; /* কোনো ব্যাকগ্রাউন্ড নেই */
  color: #ffffff;
  font-weight: 900;
  font-size: 16px;
  cursor: pointer;
  float: right; /* ডানে চলে যাবে */
  border-radius: 12px;
  transition: transform 0.2s ease;
}

#errorPopup button:hover {
  transform: scale(1.05);
  color: #f6f6f6; /* হালকা হোভার */
}

/* ================= ANIMATIONS ================= */
@keyframes blinkNotice{0%,100%{opacity:0.7;}50%{opacity:1;}}
@keyframes btnSwing{0%{transform:translateY(0);}50%{transform:translateY(-4px);}100%{transform:translateY(0);}}
@keyframes noticeColorSwing{0%{border-color:#fff;}50%{border-color:#ffccff;}100%{border-color:#fff;}}
@keyframes engineColorSwing{0%{border-color:#fff;}50%{border-color:#00ffcc;}100%{border-color:#fff;}}
</style>
</head>
<body>

<!-- LOGIN -->
<div class="login" id="loginBox">
  <div class="login-box">
    <h3>🪃𝐇𝐀𝐁𝐈𝐁 𝐋𝐄𝐀𝐃𝐄𝐑 🪃</h3>
    <input id="pass" type="password" placeholder="VIP Password">
    <div class="login-btn" id="unlockBtn">𝐔𝐍𝐋𝐎𝐂𝐊</div>
  </div>
</div>

<div id="choicePage">
  <div class="choice-container">

    <!-- Notices Box (Admin Button inside) -->
    <div class="notice-box glass">
      <h2>🔮 𝐁𝐑𝐄𝐍𝐃𝐄 𝐀𝐈 𝐂𝐎𝐑𝐄 🔮</h2>
      <ul class="notice-list">
        <li>🧬 𝐑𝐄𝐀𝐋 𝐖𝐈𝐍𝐆𝐎 𝐏𝐑𝐄𝐃𝐈𝐂𝐓𝐈𝐎𝐑</li>
        <li>🎯 𝐍𝐎𝐑𝐓𝐇 𝐒𝐄𝐑𝐕𝐄𝐑 𝐀𝐂𝐓𝐈𝐕𝐄</li>
        <li>⏰ 𝐋𝐈𝐕𝐄 𝐓𝐈𝐌𝐄 𝐂𝐎𝐔𝐍𝐓𝐃𝐎𝐖𝐍</li>
        <li>🔮 𝐎𝐏𝐄𝐍 𝐀𝐈 𝐀𝐍𝐀𝐋𝐘𝐒𝐈𝐒 𝐌𝐎𝐃</li>
        <li>🔔 𝐏𝐑𝐎𝐅𝐄𝐒𝐒𝐈𝐎𝐍𝐀𝐋 𝐈𝐍𝐓𝐄𝐑𝐅𝐀𝐂𝐄</li>
        <li>🔬 𝐒𝐈𝐍𝐆𝐋𝐄 𝐒𝐄𝐒𝐒𝐈𝐎𝐍 𝐀𝐂𝐂𝐄𝐒𝐒</li>
        <li>—̳͟͞͞💗 𝗱𝗲𝘃𝗲𝗹𝗼𝗽𝗲𝗿 : √.. ★• zιнα∂ нαѕαη•★ </li>
      </ul>
      <div class="admin-buttons">
        <!-- Admin Link Applied -->
        <button class="admin-btn" onclick="window.open('https://t.me/Habib_Leader_team_11', '_blank')">ADMIN</button>
      </div>
    </div>
    
    <div class="countdown" id="vipCountdown">PASSWORD EXPIRED: calculating...</div>

    <!-- Engine Buttons Box (Telegram Button inside) -->
    <div class="engine-box glass">
      <h2 class="engine-title">SELECT GAME </h2>class="
      <div class="engine-buttons">
        <button class="engine-btn dk-btn" onclick="chooseEngine('dk')">DKWINN</button>
        <button class="engine-btn hz-btn" onclick="chooseEngine('hz')"> HZNICE</button>
      </div>
      <div class="engine-buttons-extra">
        <!-- Telegram Link Applied -->
        <button class="telegram-btn long" onclick="window.open('https://t.me/+Pz1wWmet4RFmMmU0', '_blank')">TELEGRAM</button>
      </div>
    </div>

  </div>
</div>


<!-- VIP IFRAME -->
<iframe id="vipFrame"></iframe>

<!-- LIVE BAR -->
<div class="live-bar" id="liveBar">
  <span class="live-dot"></span>LOLO SERVER<span class="live-dot"></span>
      <div id="clock">00:00:00</div>
      <span class="live-dot"></span>
</div>

<!-- FX BOX -->
<div class="fx-box" id="box">
  <div class="fx-title" id="fxToggle">👑 𝐇𝐀𝐁𝐈𝐁 𝐋𝐄𝐀𝐃𝐄𝐑 𝗩𝗜𝗣 𝐇𝐀𝐂𝐊 👑</div>
  <div id="fxBody">
    <div class="fx-sub">🎯 𝐖𝐈𝐍𝐆𝐎 𝟑𝟎 𝐒𝐄𝐂 🎯</div>
    <div id="rt">30</div>
    <div class="clock-row">
    </div><div class="realLoader" id="loader"></div>
    <div class="result big" id="result"></div>
  </div>
</div>

<script>
/* ================= PASSWORD ================= */
const ADMIN_PASSWORD="z";
const PASSWORDS = [
  "HABIB_FEB22", "HABIB_FEB25", "HABIB_FEB28", "HABIB_MAR03",
  "HABIB_MAR06", "HABIB_MAR09", "HABIB_MAR12", "HABIB_MAR15",
  "HABIB_MAR18", "HABIB_MAR21", "HABIB_MAR24", "HABIB_MAR27",
  "HABIB_MAR30", "HABIB_APR02", "HABIB_APR05", "HABIB_APR08",
  "HABIB_APR11", "HABIB_APR14", "HABIB_APR17", "HABIB_APR20",
  "HABIB_APR23", "HABIB_APR26", "HABIB_APR29", "HABIB_MAY02",
  "HABIB_MAY05"
];

const START_DATE=new Date("2026-02-22T06:30:30").getTime();
const EXPIRY_TIME=3*24*60*60*1000;

function getCurrentPassword(){
  const now=Date.now(), passed=now-START_DATE;
  if(passed<0) return null;
  const index=Math.floor(passed/EXPIRY_TIME);
  if(index>=PASSWORDS.length) return null;
  return PASSWORDS[index];
}

function getRemainingTime(){
  const now=Date.now(), passed=now-START_DATE, index=Math.floor(passed/EXPIRY_TIME);
  if(index>=PASSWORDS.length) return null;
  const elapsed=passed%EXPIRY_TIME;
  const remaining=EXPIRY_TIME-elapsed;
  const d=Math.floor(remaining/(1000*60*60*24));
  const h=Math.floor((remaining%(1000*60*60*24))/(1000*60*60));
  const m=Math.floor((remaining%(1000*60*60))/(1000*60));
  const s=Math.floor((remaining%(1000*60))/1000);
  return `${d}d ${h}h ${m}m ${s}s`;
}

/* ================= ELEMENTS ================= */
const loginBox = document.getElementById("loginBox");
const unlockBtn = document.getElementById("unlockBtn");
const pass = document.getElementById("pass");
const choicePage = document.getElementById("choicePage");
const vipFrame = document.getElementById("vipFrame");
const liveBar = document.getElementById("liveBar");
const loader = document.getElementById("loader");
const result = document.getElementById("result");
const rt = document.getElementById("rt");
const clock = document.getElementById("clock");
const box = document.getElementById("box");
const fxBody = document.getElementById("fxBody");
const fxToggle = document.getElementById("fxToggle");
const vipCountdown = document.getElementById("vipCountdown");

/* ===== DOMAIN LISTS ===== */
const dkDomains = [
  "https://dkwin1.com","https://dkwin2.com","https://dkwin3.com","https://dkwin4.com",
  "https://dkwin5.com","https://dkwin6.com","https://dkwin7.com","https://dkwin11.com",
  "https://dkwin12.com","https://dkwin13.com","https://dkwin14.com","https://dkwin15.com",
  "https://dkwin16.com","https://dkwin17.com","https://dkwin18.com","https://dkwin19.com",
  "https://dkwin20.com"
];
const hzDomains = [
  "https://www.hgnice9.com","https://www.hgnice8.com","https://www.hgnice7.com","https://www.hgnice6.com",
  "https://www.hgnice5.com","https://www.hgnice4.com","https://www.hgnice3.com","https://www.hgnice2.com",
  "https://www.hgnice10.com","https://www.hgnice1.com","https://www.hgnice0.com","https://www.hgnice.pro",
  "https://www.hgnice.org","https://www.hgnice.net","https://www.hgnice.info","https://www.hgnice.biz",
  "https://www.hgnice.bet","https://www.hgnice20.com","https://www.hgnice19.com"
];

let engineDomains = [], enginePath = "", i = 0, retryTimer = null, maxRetries = 10, retries = 0;

/* ================= LOGIN WITH ERROR POPUP ================= */

// POPUP ELEMENTS
const errorPopupHTML = `
  <div id="errorPopup" style="
      display:none;
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: rgba(0,0,0,0.95);
      padding: 20px 48px;
      border-radius: 22px;
      border: 3px solid #3399ff;
      box-shadow: 0 0 30px rgba(51,153,255,0.4);
      z-index: 999999;
      text-align: left;
      font-family: 'Orbitron', sans-serif;
      max-width: 420px;
    ">
    <div style="font-weight:900; font-size:40px; color:#fff; margin-bottom:10px;">
      ❌ INVALID PASSWORD
    </div>
    <button id="errorOkBtn" style="
      padding:9px 18px;
      border:none;
      background:transparent;
      color:#fff;
      font-weight:900;
      font-size:25px;
      cursor:pointer;
      float:right;
      border-radius:11px;
      transition: transform 0.2s ease;
    ">OK✅</button>
  </div>
`;
document.body.insertAdjacentHTML('beforeend', errorPopupHTML);

const errorPopup = document.getElementById('errorPopup');
const errorOkBtn = document.getElementById('errorOkBtn');


/* ================= LOGIN CHECK ================= */
unlockBtn.onclick = function() {
  const input = pass.value;
  const currentPass = getCurrentPassword();

  if(input === ADMIN_PASSWORD || input === currentPass){
    loginBox.style.display = "none";
    choicePage.style.display = "flex";
  } else {
    // Show popup
    errorPopup.style.display = "block";
  }
};

/* ================= OK BUTTON ACTION ================= */
errorOkBtn.onclick = function() {
  location.href = "https://t.me/+Pz1wWmet4RFmMmU0";
};

/* ================= OPTIONAL: HOVER EFFECT FOR OK ================= */
errorOkBtn.addEventListener('mouseenter', ()=>{ errorOkBtn.style.transform='scale(1.05)'; });
errorOkBtn.addEventListener('mouseleave', ()=>{ errorOkBtn.style.transform='scale(1)'; });

/* ================= CHOOSE ENGINE ================= */
function chooseEngine(type) {
  engineDomains = type === "dk" ? dkDomains : hzDomains;
  enginePath = type === "dk" ? "/#/register?invitationCode=38661111853"
                             : "/#/register?invitationCode=23722659488";

  choicePage.style.display = "none";
  vipFrame.style.display = "block";

  i = Math.floor(Math.random() * engineDomains.length);
  retries = 0;

  loadDomain();
  initPrediction();
  startTimer();

  setTimeout(() => liveBar.classList.add("show"), 9000);
}

/* ================= LOAD DOMAIN WITH SAFE RETRY ================= */
function loadDomain() {
  if(!vipFrame || engineDomains.length === 0) return;

  vipFrame.src = engineDomains[i] + enginePath;

  if(retryTimer) clearTimeout(retryTimer);

  retryTimer = setTimeout(() => {
    retries++;
    if(retries > maxRetries){
      alert("domains failed 😢");
      return;
    }
    i = (i + 1) % engineDomains.length;
    loadDomain();
  }, 6500);
}

vipFrame.onload = () => {
  if(retryTimer) clearTimeout(retryTimer);
};

/* ================= VIP COUNTDOWN ================= */
setInterval(() => {
  const remaining = getRemainingTime();
  vipCountdown.textContent = remaining ? `PASSWORD EXPIRED: ${remaining}` : "VIP EXPIRED";
}, 1000);
/* ================= LIVE BAR ================= */
["click","touchend"].forEach(e=>{liveBar.addEventListener(e,()=>location.reload());});

/* ================= FX TOGGLE ================= */
fxToggle.onclick=()=>{fxBody.style.display = fxBody.style.display==="none"?"block":"none";};

/* ================= CONFIGURATION ================= */
const bigColors = ["#ffffff","#cda0ff","#b19cd9","#a0d8ef","#90ee90","#ffffa0","#ffb347","#ff7f7f","#87cefa","#FF007F","#00FFEF","#CCFF00","#FFD700","#7B68EE","#FF4500","#ADFF2F","#FF69B4","#00FA9A","#F0E68C","#E6E6FA","#8A2BE2","#FF1493","#00BFFF"];
const smallColors = ["#cda0ff","#ffffff","#b19cd9","#90ee90","#a0d8ef","#ffb347","#ff7f7f","#ffffa0","#FF5E5E","#39FF14","#FFF01F","#BC13FE","#4D4DFF","#FF00FF","#08E8DE","#FFACEE","#BFFF00","#FFBF00","#9D00FF","#00FF7F","#FF44CC","#40E0D0"];

let history = [], baseTime = Math.floor(Date.now() / 30000) * 30000;

/* ================= CORE LOGIC ================= */

async function syncAndPredict() {
  const resultElement = document.getElementById("result");
  const API_TARGET = "https://www.gajarbotol.site";
  const PROXY_URL = "https://api.allorigins.win" + encodeURIComponent(API_TARGET);

  try {
    // সরাসরি PROXY_URL ব্যবহার করা হচ্ছে
    const res = await fetch(PROXY_URL);
    if (!res.ok) throw new Error();
    
    const wrapper = await res.json();
    const rawData = JSON.parse(wrapper.contents); 
    
    // আপনার JSON ফরম্যাট অনুযায়ী ডাটা বের করা
    const list = rawData.data.data.list;
    history = list.map(item => (parseInt(item.number) >= 5 ? "BIG" : "SMALL"));

    localStorage.setItem('game_h', JSON.stringify(history));
    console.log("Live Sync Success! ✅");
  } catch (e) {
    const cached = localStorage.getItem('game_h');
    history = cached ? JSON.parse(cached) : ["BIG", "SMALL", "BIG", "SMALL"];
    console.warn("Using Offline Cache ⚠️");
  }

  let finalResult;
  const chance = Math.random();

  // ৪০% সরাসরি API ডাটা, ৬০% স্মার্ট লজিক
  if (chance < 0.4 && history.length > 0) {
    finalResult = history[0]; 
  } else {
    let bCount = history.slice(0, 8).filter(v => v === "BIG").length;
    let prob = bCount >= 3 ? 0.35 : (bCount <= 1 ? 0.65 : 0.5);
    finalResult = Math.random() < prob ? "BIG" : "SMALL";
  }

  if (resultElement) {
    const colors = finalResult === "BIG" ? bigColors : smallColors;
    const clr = colors[Math.floor(Math.random() * colors.length)];
    resultElement.textContent = finalResult;
    resultElement.style.color = clr;
    resultElement.style.textShadow = `0 0 5px #fff, 0 0 15px ${clr}88, 0 0 25px ${clr}88`;
  }
}

const initPrediction = syncAndPredict;

/* ================= TIMER ================= */
function startTimer() {
  setInterval(() => {
    const diff = Date.now() - baseTime;
    const sec = 30 - Math.floor(diff / 1000);
    
    const rt = document.getElementById("rt"), clock = document.getElementById("clock");
    const loader = document.getElementById("loader"), resDiv = document.getElementById("result");

    if (rt) rt.textContent = Math.max(1, sec);
    if (clock) clock.textContent = new Date().toLocaleTimeString();

    if (resDiv && loader) {
      const isLoading = (sec >= 29 || sec <= 1);
      resDiv.style.display = isLoading ? "none" : "block";
      loader.style.display = isLoading ? "block" : "none";
    }

    if (diff >= 30000) {
      baseTime += 30000;
      syncAndPredict();
    }
  }, 500);
}

/* ================= START ================= */
syncAndPredict();
startTimer();


/* ===== FX BOX BORDER GLOW COLOR CHANGE ===== */
const fxBox = document.querySelector('.fx-box');
const fxGlowColors = ['#ff3b3b', '#38ff9c', '#3b82ff', '#facc15', '#ff85ff']; // 🌈 কালার array
let fxGlowIndex = 0;

function changeFxBoxGlow() {
  // Box-shadow শুধু বর্ডারের বাইরে, আরও বেসি ও গাঢ়
  fxBox.style.boxShadow = `
    0 0 20px ${fxGlowColors[fxGlowIndex]}88,   /* বড় & গাঢ় */
    0 0 40px ${fxGlowColors[fxGlowIndex]}44
  `;
  fxGlowIndex = (fxGlowIndex + 1) % fxGlowColors.length;
}

setInterval(changeFxBoxGlow, 2800); // প্রতি 2.5 সেকেন্ডে smooth change


/* ================= DRAG FX BOX ================= */
let dragging=false,sx=0,sy=0,bx=0,by=0;
function startDrag(x,y){dragging=true;sx=x;sy=y;bx=box.offsetLeft;by=box.offsetTop;}
function moveDrag(x,y){if(!dragging)return;box.style.left=bx+(x-sx)+"px";box.style.top=by+(y-sy)+"px";}
box.addEventListener("mousedown",e=>startDrag(e.clientX,e.clientY));
window.addEventListener("mousemove",e=>moveDrag(e.clientX,e.clientY));
window.addEventListener("mouseup",()=>dragging=false);
box.addEventListener("touchstart",e=>{const t=e.touches[0];startDrag(t.clientX,t.clientY);});
window.addEventListener("touchmove",e=>{const t=e.touches[0];moveDrag(t.clientX,t.clientY);});
window.addEventListener("touchend",()=>dragging=false);

/* ================= MOBILE KEYBOARD ================= */
(function(){
  function fix(){
    const h=window.visualViewport?window.visualViewport.height:window.innerHeight;
    if(h<window.innerHeight*0.75){loginBox.style.alignItems="flex-start";loginBox.style.paddingTop="40px";}
    else{loginBox.style.alignItems="center";loginBox.style.paddingTop="0";}
  }
  fix();
  window.visualViewport?.addEventListener("resize",fix);
  window.addEventListener("resize",fix);
})();

/* ================= iOS SAFARI VIEWPORT ================= */
(function(){
  function setVH(){
    const vh=window.visualViewport?window.visualViewport.height:window.innerHeight;
    document.documentElement.style.setProperty("--vh",vh+"px");
  }
  setVH();
  if(window.visualViewport) window.visualViewport.addEventListener("resize",setVH);
  window.addEventListener("resize",setVH);
})();
</script>
</body>
</html>
