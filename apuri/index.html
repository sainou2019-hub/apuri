<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover" />
  <meta name="apple-mobile-web-app-capable" content="yes" />
  <meta name="mobile-web-app-capable" content="yes" />
  <title>NEON DODGE OVERDRIVE - オンラインランキング対応アクション</title>
  <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>⚡</text></svg>">
  <link rel="manifest" href="./manifest.json" />
  <link rel="apple-touch-icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 512 512'><rect width='512' height='512' fill='%2307080d'/><circle cx='256' cy='256' r='160' fill='none' stroke='%2300f2fe' stroke-width='28'/><text x='256' y='320' font-size='210' text-anchor='middle'>⚡</text></svg>" />
   <style>
    :root {
      --bg-color: #07080d;
      --panel-bg: rgba(16, 20, 34, 0.94);
      --primary: #00f2fe;
      --secondary: #4facfe;
      --accent: #ff007f;
      --gold: #ffd700;
      --purple: #b537f2;
      --orange: #ff7b00;
      --text: #ffffff;
      --safe-top: env(safe-area-inset-top, 0px);
      --safe-bottom: env(safe-area-inset-bottom, 0px);
      --safe-left: env(safe-area-inset-left, 0px);
      --safe-right: env(safe-area-inset-right, 0px);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      user-select: none;
      -webkit-user-select: none;
      -webkit-touch-callout: none;
    }

    html, body {
      background-color: var(--bg-color);
      color: var(--text);
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
      overflow: hidden;
      overscroll-behavior: none;
      width: 100%;
      height: 100dvh;
      position: fixed;
      top: 0;
      left: 0;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    #gameCanvas {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100dvh;
      z-index: 1;
      touch-action: none;
      display: block;
    }

    /* HUD (Safe Area対応) */
    #hud {
      position: fixed;
      top: calc(12px + var(--safe-top));
      left: calc(12px + var(--safe-left));
      right: calc(12px + var(--safe-right));
      z-index: 5;
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 8px;
      pointer-events: none;
    }

    .hud-box {
      background: rgba(0, 0, 0, 0.62);
      border: 1px solid rgba(0, 242, 254, 0.35);
      padding: 8px 12px;
      border-radius: 12px;
      backdrop-filter: blur(4px);
      -webkit-backdrop-filter: blur(4px);
      min-width: 105px;
    }

    .score-label {
      font-size: 10px;
      color: var(--primary);
      letter-spacing: 1px;
    }

    .score-value {
      font-size: clamp(20px, 5vw, 26px);
      font-weight: bold;
      line-height: 1.15;
      text-shadow: 0 0 10px var(--primary);
    }

    #comboDisplay {
      font-size: 12px;
      color: var(--gold);
      font-weight: bold;
      margin-top: 2px;
      opacity: 0;
      transition: opacity 0.2s;
    }

    .status-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 4px;
      margin-top: 4px;
      justify-content: flex-end;
    }

    .badge {
      font-size: 10px;
      font-weight: bold;
      padding: 2px 6px;
      border-radius: 6px;
      display: none;
    }

    .badge-shield { background: rgba(0, 242, 254, 0.25); border: 1px solid var(--primary); color: var(--primary); }
    .badge-slow { background: rgba(181, 55, 242, 0.25); border: 1px solid var(--purple); color: #e0aaff; }

    /* ボス警告バナー */
    #bossBanner {
      position: fixed;
      top: calc(76px + var(--safe-top));
      left: 50%;
      transform: translateX(-50%);
      z-index: 6;
      width: 90%;
      max-width: 420px;
      text-align: center;
      background: rgba(255, 0, 85, 0.28);
      border: 1px solid #ff0055;
      color: #ff80aa;
      padding: 6px 12px;
      border-radius: 20px;
      font-size: clamp(11px, 3vw, 13px);
      font-weight: bold;
      letter-spacing: 1px;
      pointer-events: none;
      display: none;
      animation: pulseWarn 0.6s infinite alternate;
    }

    @keyframes pulseWarn {
      from { transform: translateX(-50%) scale(0.97); box-shadow: 0 0 10px rgba(255, 0, 85, 0.4); }
      to { transform: translateX(-50%) scale(1.03); box-shadow: 0 0 22px rgba(255, 0, 85, 0.9); }
    }

    /* 実績解除トースト */
    #toast {
      position: fixed;
      top: calc(14px + var(--safe-top));
      left: 50%;
      transform: translate(-50%, -150px);
      z-index: 20;
      width: max-content;
      max-width: 90vw;
      background: linear-gradient(90deg, rgba(25, 30, 50, 0.96), rgba(50, 38, 20, 0.96));
      border: 1px solid var(--gold);
      box-shadow: 0 0 25px rgba(255, 215, 0, 0.45);
      padding: 10px 16px;
      border-radius: 14px;
      display: flex;
      align-items: center;
      gap: 10px;
      transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      pointer-events: none;
    }

    #toast.show { transform: translate(-50%, 0); }

    /* オーバーレイメニュー (レスポンシブ) */
    #overlay {
      position: relative;
      z-index: 10;
      width: calc(100% - 24px);
      max-width: 480px;
      max-height: calc(100dvh - 24px - var(--safe-top) - var(--safe-bottom));
      overflow-y: auto;
      -webkit-overflow-scrolling: touch;
      background: var(--panel-bg);
      border: 1px solid rgba(255, 255, 255, 0.16);
      border-radius: 20px;
      padding: clamp(14px, 4vw, 22px);
      text-align: center;
      backdrop-filter: blur(14px);
      -webkit-backdrop-filter: blur(14px);
      box-shadow: 0 0 45px rgba(0, 242, 254, 0.25);
    }

    .top-bar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 4px;
      gap: 8px;
    }

    h1 {
      font-size: clamp(17px, 4.8vw, 23px);
      background: linear-gradient(90deg, var(--primary), var(--accent));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      letter-spacing: 0.5px;
      text-align: left;
      line-height: 1.2;
    }

    .audio-controls {
      display: flex;
      gap: 4px;
      flex-shrink: 0;
    }

    .sound-btn {
      background: rgba(255, 255, 255, 0.12);
      color: #fff;
      padding: 6px 8px;
      font-size: 11px;
      border-radius: 8px;
      white-space: nowrap;
    }

    .subtitle {
      font-size: clamp(11px, 3vw, 12px);
      color: #aaa;
      margin-bottom: 12px;
      text-align: left;
    }

    .auth-section {
      background: rgba(0, 0, 0, 0.38);
      padding: 9px 10px;
      border-radius: 12px;
      margin-bottom: 12px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 8px;
    }

    .user-info {
      display: flex;
      align-items: center;
      gap: 8px;
      text-align: left;
      min-width: 0;
      flex: 1;
    }

    .user-avatar {
      width: 32px;
      height: 32px;
      border-radius: 50%;
      border: 2px solid var(--primary);
      display: none;
      flex-shrink: 0;
    }

    .user-text-wrap {
      min-width: 0;
      flex: 1;
    }

    .user-name {
      font-size: 13px;
      font-weight: bold;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }

    .user-best {
      font-size: 11px;
      color: var(--gold);
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }

    button {
      cursor: pointer;
      border: none;
      border-radius: 10px;
      font-weight: bold;
      transition: transform 0.1s, box-shadow 0.2s;
      touch-action: manipulation;
    }

    button:active { transform: scale(0.96); }

    .btn-google {
      background: #ffffff;
      color: #333;
      padding: 8px 11px;
      font-size: 11px;
      white-space: nowrap;
      flex-shrink: 0;
    }

    .btn-logout {
      background: rgba(255, 255, 255, 0.15);
      color: #fff;
      padding: 6px 9px;
      font-size: 11px;
      white-space: nowrap;
      flex-shrink: 0;
    }

    .btn-play {
      width: 100%;
      padding: 13px;
      font-size: clamp(16px, 4.5vw, 18px);
      color: #000;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      box-shadow: 0 0 22px rgba(0, 242, 254, 0.5);
      margin-bottom: 12px;
    }

    .tabs {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 4px;
      margin-bottom: 10px;
      background: rgba(0, 0, 0, 0.45);
      padding: 4px;
      border-radius: 12px;
    }

    .tab-btn {
      padding: 7px 2px;
      font-size: clamp(10px, 2.7vw, 11px);
      background: transparent;
      color: #aaa;
      border-radius: 8px;
      white-space: nowrap;
    }

    .tab-btn.active {
      background: rgba(0, 242, 254, 0.2);
      color: var(--primary);
      box-shadow: inset 0 0 0 1px rgba(0, 242, 254, 0.4);
    }

    .tab-content {
      text-align: left;
      background: rgba(0, 0, 0, 0.42);
      border-radius: 12px;
      padding: 10px;
      height: clamp(165px, 28dvh, 215px);
      overflow-y: auto;
      -webkit-overflow-scrolling: touch;
    }

    .rank-list { list-style: none; }
    .rank-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 6px 6px;
      border-bottom: 1px solid rgba(255, 255, 255, 0.06);
      font-size: 13px;
    }
    .rank-item:last-child { border-bottom: none; }
    .rank-num { width: 26px; font-weight: bold; color: #888; flex-shrink: 0; }
    .rank-1 .rank-num { color: var(--gold); }
    .rank-2 .rank-num { color: #c0c0c0; }
    .rank-3 .rank-num { color: #cd7f32; }
    .rank-name { flex: 1; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; padding-right: 8px; }
    .rank-score { font-weight: bold; color: var(--primary); flex-shrink: 0; }

    .skin-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 8px;
    }

    @media (max-width: 360px) {
      .skin-grid { grid-template-columns: 1fr; }
    }

    .skin-card {
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 10px;
      padding: 9px;
      display: flex;
      align-items: center;
      gap: 8px;
      cursor: pointer;
    }

    .skin-card.selected { border-color: var(--primary); background: rgba(0, 242, 254, 0.16); }
    .skin-card.locked { opacity: 0.45; cursor: not-allowed; }
    .skin-preview { width: 22px; height: 22px; border-radius: 50%; flex-shrink: 0; }
    .skin-meta { flex: 1; min-width: 0; }
    .skin-title { font-size: 11px; font-weight: bold; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
    .skin-req { font-size: 10px; color: #aaa; }

    .ach-item {
      display: flex;
      align-items: center;
      gap: 10px;
      padding: 7px 4px;
      border-bottom: 1px solid rgba(255, 255, 255, 0.06);
    }
    .ach-item:last-child { border-bottom: none; }
    .ach-icon {
      font-size: 18px;
      width: 30px;
      height: 30px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: rgba(255, 255, 255, 0.08);
      border-radius: 8px;
      flex-shrink: 0;
    }
    .ach-item.unlocked .ach-icon { background: rgba(255, 215, 0, 0.2); border: 1px solid var(--gold); }
    .ach-info { flex: 1; min-width: 0; }
    .ach-title { font-size: 12px; font-weight: bold; color: #ddd; }
    .ach-item.unlocked .ach-title { color: var(--gold); }
    .ach-desc { font-size: 11px; color: #888; }

    .guide-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
      font-size: 11px;
      line-height: 1.4;
    }
    @media (max-width: 380px) {
      .guide-grid { grid-template-columns: 1fr; }
    }
    .guide-card { background: rgba(255, 255, 255, 0.05); padding: 8px; border-radius: 8px; }

    .hidden { display: none !important; }
    #resultBanner {
      margin-bottom: 10px;
      padding: 8px;
      background: rgba(255, 0, 127, 0.22);
      border: 1px solid var(--accent);
      border-radius: 10px;
    }
  </style>
</head>
<body>

  <!-- 実績解除通知 -->
  <div id="toast">
    <span style="font-size: 22px;" id="toastIcon">🏆</span>
    <div style="text-align: left;">
      <div style="font-size: 10px; color: var(--gold); font-weight: bold;">ACHIEVEMENT UNLOCKED!</div>
      <div style="font-size: 13px; font-weight: bold;" id="toastTitle">実績名</div>
    </div>
  </div>

  <canvas id="gameCanvas"></canvas>

  <!-- ボス出現警告 -->
  <div id="bossBanner">⚠️ BOSS出現！コアスターを3つ集めて撃破せよ！</div>

  <!-- プレイ中HUD -->
  <div id="hud" class="hidden">
    <div class="hud-box">
      <div class="score-label">SCORE</div>
      <div class="score-value" id="hudScore">0</div>
      <div id="comboDisplay">COMBO x1</div>
    </div>
    <div class="hud-box" style="text-align: right;">
      <div class="score-label">FEVER GAUGE</div>
      <div class="score-value" id="hudFever" style="color: var(--accent);">0%</div>
      <div class="status-badges">
        <span id="badgeShield" class="badge badge-shield">🛡️ SHIELD</span>
        <span id="badgeSlow" class="badge badge-slow">⏳ SLOW</span>
      </div>
    </div>
  </div>

  <!-- メニューオーバーレイ -->
  <div id="overlay">
    <div class="top-bar">
      <h1>NEON DODGE OVERDRIVE</h1>
      <div class="audio-controls">
        <button id="bgmToggleBtn" class="sound-btn">🎵 BGM</button>
        <button id="soundToggleBtn" class="sound-btn">🔊 SE</button>
      </div>
    </div>
    <p class="subtitle">指ドラッグ / マウス操作で回避！カスり(GRAZE)でゲージ急上昇！</p>

    <div id="resultBanner" class="hidden">
      <div style="font-size: 11px; color: #ff80bf;">GAME OVER</div>
      <div style="font-size: 22px; font-weight: bold;" id="finalScore">0</div>
      <div style="font-size: 11px; color: var(--gold);" id="newRecordMsg" class="hidden">🎉 NEW RECORD! ランキング更新！</div>
    </div>

    <div class="auth-section">
      <div class="user-info">
        <img id="userAvatar" class="user-avatar" src="" alt="avatar" />
        <div class="user-text-wrap">
          <div class="user-name" id="userName">ゲストプレイヤー</div>
          <div class="user-best" id="userBest">ログインするとランキング＆実績を保存</div>
        </div>
      </div>
      <button id="loginBtn" class="btn-google">Googleログイン</button>
      <button id="logoutBtn" class="btn-logout hidden">ログアウト</button>
    </div>

    <button id="startBtn" class="btn-play">PLAY START</button>

    <div class="tabs">
      <button class="tab-btn active" data-tab="tabRank">🏆 順位</button>
      <button class="tab-btn" data-tab="tabSkins">🎨 スキン (<span id="skinCount">1/8</span>)</button>
      <button class="tab-btn" data-tab="tabAch">🎖️ 実績 (<span id="achCount">0/8</span>)</button>
      <button class="tab-btn" data-tab="tabGuide">📖 遊び方</button>
    </div>

    <div id="tabRank" class="tab-content">
      <ul class="rank-list" id="rankList">
        <li class="rank-item" style="justify-content: center; color: #888;">読み込み中...</li>
      </ul>
    </div>

    <div id="tabSkins" class="tab-content hidden">
      <div class="skin-grid" id="skinGrid"></div>
    </div>

    <div id="tabAch" class="tab-content hidden">
      <div id="achList"></div>
    </div>

    <div id="tabGuide" class="tab-content hidden">
      <div class="guide-grid">
        <div class="guide-card"><strong style="color:#00f2fe;">📱 スマホ操作</strong><br>画面をタッチ＆スライド！自機は指の少し上に表示されるので見やすいです。</div>
        <div class="guide-card"><strong style="color:#ffd700;">⚡ GRAZE（カスり）</strong><br>敵のすぐ横をすり抜けるとボーナス＋フィーバー急速チャージ！</div>
        <div class="guide-card"><strong style="color:#ff0055;">👾 BOSS戦</strong><br>3000点毎に出現。周りのスター3個獲得で大爆発撃破！</div>
        <div class="guide-card"><strong style="color:#ff7b00;">🛡️ ⏳ 💥 アイテム</strong><br>シールド(1回防御)・スロー(敵減速)・ボム(敵全消去)</div>
      </div>
    </div>
  </div>

  <!-- Firebase & ゲームロジック -->
  <script type="module">
    import { initializeApp } from "https://www.gstatic.com/firebasejs/11.0.2/firebase-app.js";
    import { getAuth, GoogleAuthProvider, signInWithPopup, signInWithRedirect, getRedirectResult, signOut, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/11.0.2/firebase-auth.js";
    import { getFirestore, doc, getDoc, setDoc, collection, query, orderBy, limit, onSnapshot, serverTimestamp } from "https://www.gstatic.com/firebasejs/11.0.2/firebase-firestore.js";

    const firebaseConfig = {
      apiKey: "AIzaSyDnlfnMpZZVxPHLR87unzwLH13Vovx6Qqk",
      authDomain: "apuri-b4d56.firebaseapp.com",
      projectId: "apuri-b4d56",
      storageBucket: "apuri-b4d56.firebasestorage.app",
      messagingSenderId: "366055633446",
      appId: "1:366055633446:web:f686e28a3ce84acea3ece7"
    };

    const app = initializeApp(firebaseConfig);
    const auth = getAuth(app);
    const db = getFirestore(app);
    const provider = new GoogleAuthProvider();

    // --- サウンド & シンセBGMエンジン ---
    let soundEnabled = true;
    let bgmEnabled = true;
    let audioCtx = null;
    let bgmInterval = null;
    let bgmStep = 0;

    function initAudio() {
      if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
      if (audioCtx.state === "suspended") audioCtx.resume();
    }

    function playTone(freq, type, duration, vol = 0.12, slideFreq = null) {
      if (!soundEnabled) return;
      initAudio();
      const osc = audioCtx.createOscillator();
      const gain = audioCtx.createGain();
      osc.type = type;
      osc.frequency.setValueAtTime(freq, audioCtx.currentTime);
      if (slideFreq) osc.frequency.exponentialRampToValueAtTime(slideFreq, audioCtx.currentTime + duration);
      gain.gain.setValueAtTime(vol, audioCtx.currentTime);
      gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + duration);
      osc.connect(gain);
      gain.connect(audioCtx.destination);
      osc.start();
      osc.stop(audioCtx.currentTime + duration);
    }

    function startBgm() {
      stopBgm();
      if (!bgmEnabled) return;
      initAudio();
      const bassNotes = [110, 110, 130.81, 146.83, 110, 110, 164.81, 146.83];
      const leadNotes = [440, 523.25, 659.25, 587.33, 440, 659.25, 783.99, 659.25];
      bgmInterval = setInterval(() => {
        if (!isPlaying || !bgmEnabled) return;
        const mult = isFever ? 1.25 : 1.0;
        const bFreq = bassNotes[bgmStep % bassNotes.length] * mult;
        const lFreq = leadNotes[bgmStep % leadNotes.length] * mult;

        const osc1 = audioCtx.createOscillator();
        const g1 = audioCtx.createGain();
        osc1.type = "triangle";
        osc1.frequency.setValueAtTime(bFreq, audioCtx.currentTime);
        g1.gain.setValueAtTime(0.055, audioCtx.currentTime);
        g1.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + 0.16);
        osc1.connect(g1); g1.connect(audioCtx.destination);
        osc1.start(); osc1.stop(audioCtx.currentTime + 0.16);

        if (bgmStep % 2 === 0 || isFever) {
          const osc2 = audioCtx.createOscillator();
          const g2 = audioCtx.createGain();
          osc2.type = "sine";
          osc2.frequency.setValueAtTime(lFreq, audioCtx.currentTime);
          g2.gain.setValueAtTime(0.032, audioCtx.currentTime);
          g2.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + 0.14);
          osc2.connect(g2); g2.connect(audioCtx.destination);
          osc2.start(); osc2.stop(audioCtx.currentTime + 0.14);
        }
        bgmStep++;
      }, 175);
    }

    function stopBgm() {
      if (bgmInterval) { clearInterval(bgmInterval); bgmInterval = null; }
    }

    const sfx = {
      star: (combo) => playTone(520 + Math.min(combo * 40, 600), "sine", 0.14, 0.12, 880 + Math.min(combo * 45, 700)),
      graze: () => playTone(980, "sine", 0.07, 0.08, 1450),
      item: () => { playTone(440, "triangle", 0.12, 0.15, 880); setTimeout(() => playTone(660, "triangle", 0.2, 0.15, 1320), 80); },
      shieldBreak: () => playTone(300, "sawtooth", 0.25, 0.15, 90),
      bomb: () => playTone(150, "sawtooth", 0.45, 0.2, 35),
      bossDown: () => { [330, 440, 554, 659, 880].forEach((f, i) => setTimeout(() => playTone(f, "sawtooth", 0.25, 0.14), i * 65)); },
      fever: () => { [523, 659, 784, 1046].forEach((f, i) => setTimeout(() => playTone(f, "square", 0.18, 0.1), i * 60)); },
      achievement: () => { [587, 880, 1174].forEach((f, i) => setTimeout(() => playTone(f, "sine", 0.25, 0.15), i * 90)); },
      gameover: () => playTone(260, "sawtooth", 0.5, 0.18, 55)
    };

    document.getElementById("soundToggleBtn").addEventListener("click", (e) => {
      soundEnabled = !soundEnabled;
      e.target.textContent = soundEnabled ? "🔊 SE" : "🔇 SE";
      e.target.style.opacity = soundEnabled ? "1" : "0.5";
    });

    document.getElementById("bgmToggleBtn").addEventListener("click", (e) => {
      bgmEnabled = !bgmEnabled;
      e.target.textContent = bgmEnabled ? "🎵 BGM" : "🔇 BGM";
      e.target.style.opacity = bgmEnabled ? "1" : "0.5";
      if (!bgmEnabled) stopBgm();
      else if (isPlaying) startBgm();
    });

    // --- 実績 & スキンマスターデータ ---
    const ACHIEVEMENTS = [
      { id: "first_play", icon: "🚀", title: "初陣", desc: "初めてゲームをプレイする" },
      { id: "graze_20", icon: "⚡", title: "スリルジャンキー", desc: "1プレイで20回GRAZE(カスり回避)を達成" },
      { id: "score_3000", icon: "⭐", title: "ライジングスター", desc: "スコア 3,000 pts を達成" },
      { id: "boss_kill", icon: "👾", title: "ジャイアントキラー", desc: "ボス「ネオン・ガーディアン」を撃破" },
      { id: "combo_10", icon: "🔥", title: "コンボマスター", desc: "10コンボ以上を達成" },
      { id: "fever_once", icon: "🌈", title: "フィーバータイム", desc: "フィーバーモードに突入する" },
      { id: "item_5", icon: "🎒", title: "アイテムハンター", desc: "累計5個の特殊アイテムを取得" },
      { id: "score_10000", icon: "👑", title: "ネオンの覇者", desc: "スコア 10,000 pts を達成" }
    ];

    const SKINS = [
      { id: "cyan", name: "デフォルトシアン", color: "#00f2fe", shape: "circle", reqText: "初期装備", unlockAch: null },
      { id: "volt", name: "ボルトイエロー", color: "#f9ff00", shape: "circle", reqText: "実績「スリルジャンキー」", unlockAch: "graze_20" },
      { id: "emerald", name: "エメラルドパルス", color: "#00ff88", shape: "circle", reqText: "実績「ライジングスター」", unlockAch: "score_3000" },
      { id: "crimson", name: "クリムゾンファング", color: "#ff2a55", shape: "diamond", reqText: "実績「ジャイアントキラー」", unlockAch: "boss_kill" },
      { id: "solar", name: "ソーラーフレア", color: "#ff9900", shape: "circle", reqText: "実績「コンボマスター」", unlockAch: "combo_10" },
      { id: "magenta", name: "サイバーピンク", color: "#ff007f", shape: "circle", reqText: "実績「フィーバータイム」", unlockAch: "fever_once" },
      { id: "diamond", name: "クリスタルダイヤ", color: "#70d6ff", shape: "diamond", reqText: "実績「アイテムハンター」", unlockAch: "item_5" },
      { id: "royal_star", name: "ロイヤルスター", color: "#ffd700", shape: "star", reqText: "実績「ネオンの覇者」", unlockAch: "score_10000" }
    ];

    let userData = {
      bestScore: 0,
      unlockedAchievements: [],
      selectedSkin: "cyan",
      totalItemsCollected: 0
    };

    try {
      const savedLocal = localStorage.getItem("neon_dodge_dx_save");
      if (savedLocal) userData = { ...userData, ...JSON.parse(savedLocal) };
    } catch (e) {}

    function renderSkinsAndAchievements() {
      const skinGrid = document.getElementById("skinGrid");
      const achList = document.getElementById("achList");
      skinGrid.innerHTML = "";
      achList.innerHTML = "";

      let unlockedSkinCount = 0;
      SKINS.forEach((skin) => {
        const isUnlocked = !skin.unlockAch || userData.unlockedAchievements.includes(skin.unlockAch);
        if (isUnlocked) unlockedSkinCount++;
        const isSelected = userData.selectedSkin === skin.id;

        const card = document.createElement("div");
        card.className = `skin-card ${isSelected ? "selected" : ""} ${!isUnlocked ? "locked" : ""}`;
        const borderRadius = skin.shape === "diamond" ? "4px" : "50%";
        const transform = skin.shape === "diamond" ? "rotate(45deg) scale(0.8)" : "none";

        card.innerHTML = `
          <div class="skin-preview" style="background:${skin.color}; box-shadow:0 0 10px ${skin.color}; border-radius:${borderRadius}; transform:${transform};"></div>
          <div class="skin-meta">
            <div class="skin-title">${skin.name} ${isSelected ? "✓" : ""}</div>
            <div class="skin-req">${isUnlocked ? "使用可能" : skin.reqText}</div>
          </div>
        `;
        if (isUnlocked) {
          card.addEventListener("click", () => {
            userData.selectedSkin = skin.id;
            saveUserProgress();
            renderSkinsAndAchievements();
          });
        }
        skinGrid.appendChild(card);
      });

      document.getElementById("skinCount").textContent = `${unlockedSkinCount}/${SKINS.length}`;
      document.getElementById("achCount").textContent = `${userData.unlockedAchievements.length}/${ACHIEVEMENTS.length}`;

      ACHIEVEMENTS.forEach((ach) => {
        const unlocked = userData.unlockedAchievements.includes(ach.id);
        const div = document.createElement("div");
        div.className = `ach-item ${unlocked ? "unlocked" : ""}`;
        div.innerHTML = `
          <div class="ach-icon">${unlocked ? ach.icon : "🔒"}</div>
          <div class="ach-info">
            <div class="ach-title">${ach.title}</div>
            <div class="ach-desc">${ach.desc}</div>
          </div>
        `;
        achList.appendChild(div);
      });
    }

    let toastTimeout = null;
    function unlockAchievement(achId) {
      if (userData.unlockedAchievements.includes(achId)) return;
      const ach = ACHIEVEMENTS.find((a) => a.id === achId);
      if (!ach) return;

      userData.unlockedAchievements.push(achId);
      sfx.achievement();
      renderSkinsAndAchievements();
      saveUserProgress();

      const toast = document.getElementById("toast");
      document.getElementById("toastIcon").textContent = ach.icon;
      document.getElementById("toastTitle").textContent = ach.title;
      toast.classList.add("show");
      clearTimeout(toastTimeout);
      toastTimeout = setTimeout(() => toast.classList.remove("show"), 3200);
    }

    document.querySelectorAll(".tab-btn").forEach((btn) => {
      btn.addEventListener("click", () => {
        document.querySelectorAll(".tab-btn").forEach((b) => b.classList.remove("active"));
        document.querySelectorAll(".tab-content").forEach((c) => c.classList.add("hidden"));
        btn.classList.add("active");
        document.getElementById(btn.dataset.tab).classList.remove("hidden");
      });
    });

    // --- Firebase 認証 & 同期 ---
    const loginBtn = document.getElementById("loginBtn");
    const logoutBtn = document.getElementById("logoutBtn");
    const userNameEl = document.getElementById("userName");
    const userBestEl = document.getElementById("userBest");
    const userAvatarEl = document.getElementById("userAvatar");
    const rankListEl = document.getElementById("rankList");
    let currentUser = null;

    getRedirectResult(auth).catch((e) => console.error(e));

    loginBtn.addEventListener("click", async () => {
      try {
        await signInWithPopup(auth, provider);
      } catch (error) {
        if (error.code === "auth/popup-blocked" || error.code === "auth/cancelled-popup-request") {
          await signInWithRedirect(auth, provider);
        } else if (error.code !== "auth/popup-closed-by-user") {
          alert("ログインエラー: " + error.message);
        }
      }
    });

    logoutBtn.addEventListener("click", () => signOut(auth));

    async function saveUserProgress(newScore = null) {
      if (newScore !== null && newScore > userData.bestScore) userData.bestScore = newScore;
      localStorage.setItem("neon_dodge_dx_save", JSON.stringify(userData));

      if (!currentUser) return;
      userBestEl.textContent = `自己ベスト: ${userData.bestScore.toLocaleString()} pts`;

      try {
        await setDoc(doc(db, "leaderboard", currentUser.uid), {
          name: currentUser.displayName || "プレイヤー",
          score: userData.bestScore,
          unlockedAchievements: userData.unlockedAchievements,
          selectedSkin: userData.selectedSkin,
          totalItemsCollected: userData.totalItemsCollected,
          updatedAt: serverTimestamp()
        }, { merge: true });
      } catch (e) { console.error(e); }
    }

    onAuthStateChanged(auth, async (user) => {
      currentUser = user;
      if (user) {
        loginBtn.classList.add("hidden");
        logoutBtn.classList.remove("hidden");
        userNameEl.textContent = user.displayName || "プレイヤー";
        if (user.photoURL) { userAvatarEl.src = user.photoURL; userAvatarEl.style.display = "block"; }

        const snap = await getDoc(doc(db, "leaderboard", user.uid));
        if (snap.exists()) {
          const d = snap.data();
          userData.bestScore = Math.max(userData.bestScore, d.score || 0);
          userData.unlockedAchievements = Array.from(new Set([...userData.unlockedAchievements, ...(d.unlockedAchievements || [])]));
          if (d.selectedSkin) userData.selectedSkin = d.selectedSkin;
          userData.totalItemsCollected = Math.max(userData.totalItemsCollected, d.totalItemsCollected || 0);
        }
        userBestEl.textContent = `自己ベスト: ${userData.bestScore.toLocaleString()} pts`;
        renderSkinsAndAchievements();
        saveUserProgress();
      } else {
        loginBtn.classList.remove("hidden");
        logoutBtn.classList.add("hidden");
        userAvatarEl.style.display = "none";
        userNameEl.textContent = "ゲストプレイヤー";
        userBestEl.textContent = "ログインするとランキング＆実績を保存";
      }
    });

    const q = query(collection(db, "leaderboard"), orderBy("score", "desc"), limit(10));
    onSnapshot(q, (snapshot) => {
      rankListEl.innerHTML = "";
      if (snapshot.empty) {
        rankListEl.innerHTML = `<li class="rank-item" style="justify-content:center; color:#888;">まだ記録がありません！</li>`;
        return;
      }
      let rank = 1;
      snapshot.forEach((docSnap) => {
        const data = docSnap.data();
        const li = document.createElement("li");
        li.className = `rank-item rank-${rank}`;
        li.innerHTML = `
          <span class="rank-num">#${rank}</span>
          <span class="rank-name">${escapeHtml(data.name || "名無し")}</span>
          <span class="rank-score">${Number(data.score).toLocaleString()}</span>
        `;
        rankListEl.appendChild(li);
        rank++;
      });
    });

    function escapeHtml(str) {
      return str.replace(/[&<>"']/g, m => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[m]));
    }

    renderSkinsAndAchievements();

    // --- ゲームエンジン (レスポンシブ & タッチ最適化) ---
    const canvas = document.getElementById("gameCanvas");
    const ctx = canvas.getContext("2d");

    let width, height, gameScale = 1;
    function resize() {
      width = canvas.width = window.innerWidth;
      height = canvas.height = window.innerHeight;
      // スマホ縦画面では要素サイズと速度を画面幅に合わせて最適化
      gameScale = width < 520 ? Math.max(0.78, width / 480) : 1.0;
    }
    window.addEventListener("resize", resize);
    resize();

    let isPlaying = false;
    let score = 0;
    let combo = 0;
    let comboTimer = 0;
    let feverGauge = 0;
    let isFever = false;
    let feverTimer = 0;
    let hasShield = false;
    let slowTimer = 0;
    let frameCount = 0;
    let grazeCountInRun = 0;
    let shakeTime = 0;
    let hitstopFrames = 0;
    let nextBossScore = 3000;

    const player = { x: width / 2, y: height / 2, r: 12, targetX: width / 2, targetY: height / 2, trail: [] };
    let enemies = [];
    let stars = [];
    let powerups = [];
    let particles = [];
    let floatingTexts = [];
    let boss = null;

    // PCはカーソル位置、スマホは指で隠れないよう45px上にオフセット
    function updateTarget(x, y, isTouch = false) {
      const offsetY = isTouch ? -45 : 0;
      const pad = 20;
      player.targetX = Math.max(pad, Math.min(width - pad, x));
      player.targetY = Math.max(pad + 50, Math.min(height - pad, y + offsetY));
    }

    window.addEventListener("mousemove", (e) => updateTarget(e.clientX, e.clientY, false));
    window.addEventListener("touchmove", (e) => {
      if (e.touches.length > 0) updateTarget(e.touches[0].clientX, e.touches[0].clientY, true);
    }, { passive: true });
    window.addEventListener("touchstart", (e) => {
      if (e.touches.length > 0) updateTarget(e.touches[0].clientX, e.touches[0].clientY, true);
    }, { passive: true });

    function addFloatingText(x, y, text, color = "#fff") {
      floatingTexts.push({ x, y, text, color, life: 1.0 });
    }

    function triggerShake(frames = 10) {
      shakeTime = Math.max(shakeTime, frames);
    }

    function spawnEnemy() {
      const edge = Math.floor(Math.random() * 4);
      let x, y;
      if (edge === 0) { x = Math.random() * width; y = -20; }
      else if (edge === 1) { x = width + 20; y = Math.random() * height; }
      else if (edge === 2) { x = Math.random() * width; y = height + 20; }
      else { x = -20; y = Math.random() * height; }

      const rand = Math.random();
      let type = "normal";
      if (score > 800 && rand < 0.22) type = "homing";
      else if (score > 1500 && rand < 0.38) type = "sniper";
      else if (score > 2200 && rand < 0.50) type = "bomber";

      const angle = Math.atan2(player.y - y, player.x - x) + (Math.random() - 0.5) * 0.45;
      const baseSpeed = (2.6 + Math.min(score / 2800, 5.0)) * (width < 520 ? 0.88 : 1.0);

      if (type === "sniper") {
        const sx = Math.max(30, Math.min(width - 30, x));
        const sy = Math.max(85, Math.min(height - 30, y));
        enemies.push({ x: sx, y: sy, vx: 0, vy: 0, r: 11 * gameScale, type: "sniper", aimTimer: 58, aimAngle: Math.atan2(player.y - sy, player.x - sx), grazed: false });
      } else if (type === "bomber") {
        enemies.push({ x, y, vx: Math.cos(angle) * (baseSpeed * 0.75), vy: Math.sin(angle) * (baseSpeed * 0.75), r: 15 * gameScale, type: "bomber", fuse: 110 + Math.random() * 50, grazed: false });
      } else if (type === "homing") {
        enemies.push({ x, y, vx: Math.cos(angle) * (baseSpeed * 0.85), vy: Math.sin(angle) * (baseSpeed * 0.85), r: 10.5 * gameScale, type: "homing", life: 320, grazed: false });
      } else {
        enemies.push({ x, y, vx: Math.cos(angle) * baseSpeed, vy: Math.sin(angle) * baseSpeed, r: (9.5 + Math.random() * 5.5) * gameScale, type: "normal", grazed: false });
      }
    }

    function spawnBoss() {
      boss = {
        x: width / 2,
        y: -60,
        targetY: 115,
        r: 34 * gameScale,
        coresLeft: 3,
        shootTimer: 0,
        angle: 0
      };
      document.getElementById("bossBanner").style.display = "block";
      triggerShake(18);
      stars = [];
      for (let i = 0; i < 3; i++) spawnStar(true);
    }

    function spawnStar(isBossCore = false) {
      const marginX = Math.max(40, width * 0.1);
      const topSafe = 110;
      const bottomSafe = 60;
      stars.push({
        x: marginX + Math.random() * (width - marginX * 2),
        y: topSafe + Math.random() * Math.max(120, height - topSafe - bottomSafe),
        r: (isBossCore ? 13 : 10) * gameScale,
        pulse: 0,
        isBossCore
      });
    }

    function spawnPowerup() {
      const types = ["shield", "slow", "bomb"];
      const type = types[Math.floor(Math.random() * types.length)];
      const marginX = Math.max(45, width * 0.12);
      const topSafe = 115;
      const bottomSafe = 65;
      powerups.push({
        x: marginX + Math.random() * (width - marginX * 2),
        y: topSafe + Math.random() * Math.max(120, height - topSafe - bottomSafe),
        type,
        r: 14 * gameScale,
        life: 480
      });
    }

    function createParticles(x, y, color, count = 12) {
      for (let i = 0; i < count; i++) {
        const angle = Math.random() * Math.PI * 2;
        const speed = 1.5 + Math.random() * 5.5;
        particles.push({ x, y, vx: Math.cos(angle) * speed, vy: Math.sin(angle) * speed, life: 1.0, color });
      }
    }

    function drawPlayerShape(x, y, r, shape, color) {
      ctx.fillStyle = "#ffffff";
      ctx.strokeStyle = color;
      ctx.lineWidth = 3;

      if (shape === "diamond") {
        ctx.beginPath();
        ctx.moveTo(x, y - r - 3); ctx.lineTo(x + r + 3, y); ctx.lineTo(x, y + r + 3); ctx.lineTo(x - r - 3, y);
        ctx.closePath(); ctx.fill(); ctx.stroke();
      } else if (shape === "star") {
        ctx.beginPath();
        for (let i = 0; i < 5; i++) {
          const outerAngle = (i * 2 * Math.PI) / 5 - Math.PI / 2;
          const innerAngle = outerAngle + Math.PI / 5;
          ctx.lineTo(x + Math.cos(outerAngle) * (r + 4), y + Math.sin(outerAngle) * (r + 4));
          ctx.lineTo(x + Math.cos(innerAngle) * (r * 0.5), y + Math.sin(innerAngle) * (r * 0.5));
        }
        ctx.closePath(); ctx.fill(); ctx.stroke();
      } else {
        ctx.beginPath(); ctx.arc(x, y, r, 0, Math.PI * 2); ctx.fill();
        ctx.beginPath(); ctx.arc(x, y, r + 3, 0, Math.PI * 2); ctx.stroke();
      }
    }

    function startGame() {
      isPlaying = true;
      score = 0;
      combo = 0;
      comboTimer = 0;
      feverGauge = 0;
      isFever = false;
      hasShield = false;
      slowTimer = 0;
      frameCount = 0;
      grazeCountInRun = 0;
      nextBossScore = 3000;
      boss = null;
      enemies = [];
      stars = [];
      powerups = [];
      particles = [];
      floatingTexts = [];
      player.r = 12 * gameScale;
      player.x = player.targetX = width / 2;
      player.y = player.targetY = height * 0.55;
      player.trail = [];

      for (let i = 0; i < 3; i++) spawnStar(false);
      unlockAchievement("first_play");
      startBgm();

      document.getElementById("overlay").classList.add("hidden");
      document.getElementById("hud").classList.remove("hidden");
      document.getElementById("newRecordMsg").classList.add("hidden");
      document.getElementById("bossBanner").style.display = "none";
    }

    async function gameOver() {
      isPlaying = false;
      stopBgm();
      sfx.gameover();
      triggerShake(20);
      createParticles(player.x, player.y, "#00f2fe", 45);
      document.getElementById("hud").classList.add("hidden");
      document.getElementById("bossBanner").style.display = "none";
      document.getElementById("overlay").classList.remove("hidden");
      document.getElementById("resultBanner").classList.remove("hidden");
      document.getElementById("finalScore").textContent = `${score.toLocaleString()} pts`;
      document.getElementById("startBtn").textContent = "PLAY AGAIN";

      const isNewRecord = score > userData.bestScore;
      await saveUserProgress(score);
      if (isNewRecord && currentUser) document.getElementById("newRecordMsg").classList.remove("hidden");
    }

    document.getElementById("startBtn").addEventListener("click", startGame);

    function loop() {
      requestAnimationFrame(loop);

      if (hitstopFrames > 0) {
        hitstopFrames--;
        return;
      }

      ctx.save();
      if (shakeTime > 0) {
        shakeTime--;
        const mag = shakeTime * 0.6;
        ctx.translate((Math.random() - 0.5) * mag, (Math.random() - 0.5) * mag);
      }

      ctx.fillStyle = "rgba(7, 8, 13, 0.28)";
      ctx.fillRect(0, 0, width, height);

      // 背景グリッド
      ctx.strokeStyle = isFever ? "rgba(255, 0, 127, 0.08)" : "rgba(0, 242, 254, 0.04)";
      ctx.lineWidth = 1;
      const gridSize = 55;
      const offset = (frameCount * (isFever ? 2.5 : 0.8)) % gridSize;
      for (let gx = 0; gx < width; gx += gridSize) {
        ctx.beginPath(); ctx.moveTo(gx, 0); ctx.lineTo(gx, height); ctx.stroke();
      }
      for (let gy = offset; gy < height; gy += gridSize) {
        ctx.beginPath(); ctx.moveTo(0, gy); ctx.lineTo(width, gy); ctx.stroke();
      }

      // パーティクル
      for (let i = particles.length - 1; i >= 0; i--) {
        const p = particles[i];
        p.x += p.vx; p.y += p.vy; p.life -= 0.03;
        if (p.life <= 0) { particles.splice(i, 1); continue; }
        ctx.globalAlpha = p.life;
        ctx.fillStyle = p.color;
        ctx.beginPath(); ctx.arc(p.x, p.y, 3, 0, Math.PI * 2); ctx.fill();
      }
      ctx.globalAlpha = 1.0;

      // フローティングテキスト
      for (let i = floatingTexts.length - 1; i >= 0; i--) {
        const ft = floatingTexts[i];
        ft.y -= 1.2; ft.life -= 0.025;
        if (ft.life <= 0) { floatingTexts.splice(i, 1); continue; }
        ctx.globalAlpha = ft.life;
        ctx.font = `bold ${Math.round(14 * gameScale)}px sans-serif`;
        ctx.textAlign = "center";
        ctx.fillStyle = ft.color;
        ctx.fillText(ft.text, ft.x, ft.y);
      }
      ctx.globalAlpha = 1.0;

      if (!isPlaying) { ctx.restore(); return; }

      frameCount++;
      score += 1;

      if (score >= 3000) unlockAchievement("score_3000");
      if (score >= 10000) unlockAchievement("score_10000");

      if (!boss && score >= nextBossScore) {
        spawnBoss();
        nextBossScore += 4500;
      }

      player.x += (player.targetX - player.x) * 0.22;
      player.y += (player.targetY - player.y) * 0.22;
      player.trail.push({ x: player.x, y: player.y });
      if (player.trail.length > 10) player.trail.shift();

      if (combo > 0) {
        comboTimer--;
        if (comboTimer <= 0) { combo = 0; document.getElementById("comboDisplay").style.opacity = 0; }
      }

      if (isFever) {
        feverTimer--;
        feverGauge = Math.max(0, Math.ceil((feverTimer / 300) * 100));
        if (feverTimer <= 0) isFever = false;
      }

      if (slowTimer > 0) slowTimer--;

      const spawnRate = boss ? 38 : Math.max(14, 42 - Math.floor(score / 450));
      if (frameCount % spawnRate === 0) spawnEnemy();
      if (!boss && stars.length < 3) spawnStar(false);
      if (frameCount % 450 === 0 && powerups.length < 2) spawnPowerup();

      // --- ボス処理 ---
      if (boss) {
        boss.y += (boss.targetY - boss.y) * 0.05;
        boss.x = width / 2 + Math.sin(frameCount * 0.025) * (width * 0.3);
        boss.angle += 0.04;
        boss.shootTimer++;

        if (boss.shootTimer % 52 === 0) {
          for (let k = -1; k <= 1; k++) {
            const a = Math.atan2(player.y - boss.y, player.x - boss.x) + k * 0.28;
            enemies.push({ x: boss.x, y: boss.y, vx: Math.cos(a) * 3.5, vy: Math.sin(a) * 3.5, r: 8.5 * gameScale, type: "normal", grazed: false });
          }
        }

        ctx.save();
        ctx.translate(boss.x, boss.y);
        ctx.rotate(boss.angle);
        ctx.shadowBlur = 22;
        ctx.shadowColor = "#ff0055";
        ctx.strokeStyle = "#ff0055";
        ctx.lineWidth = 4;
        ctx.strokeRect(-boss.r, -boss.r, boss.r * 2, boss.r * 2);
        ctx.rotate(-boss.angle * 2);
        ctx.strokeStyle = "#ffd700";
        ctx.strokeRect(-boss.r * 0.65, -boss.r * 0.65, boss.r * 1.3, boss.r * 1.3);
        ctx.restore();

        if (!isFever && Math.hypot(player.x - boss.x, player.y - boss.y) < player.r + boss.r) {
          if (hasShield) { hasShield = false; sfx.shieldBreak(); triggerShake(12); player.targetY += 70; }
          else { ctx.restore(); gameOver(); return; }
        }
      }

      // --- 特殊アイテム ---
      for (let i = powerups.length - 1; i >= 0; i--) {
        const pw = powerups[i];
        pw.life--;
        if (pw.life <= 0) { powerups.splice(i, 1); continue; }

        const colorMap = { shield: "#00f2fe", slow: "#b537f2", bomb: "#ff7b00" };
        const iconMap = { shield: "🛡️", slow: "⏳", bomb: "💥" };
        const c = colorMap[pw.type];

        ctx.shadowBlur = 15; ctx.shadowColor = c; ctx.strokeStyle = c; ctx.lineWidth = 2.5;
        ctx.beginPath(); ctx.arc(pw.x, pw.y, pw.r + Math.sin(frameCount * 0.15) * 2, 0, Math.PI * 2); ctx.stroke();
        ctx.shadowBlur = 0;

        ctx.font = `${Math.round(15 * gameScale)}px sans-serif`; ctx.textAlign = "center"; ctx.textBaseline = "middle";
        ctx.fillText(iconMap[pw.type], pw.x, pw.y);

        if (Math.hypot(player.x - pw.x, player.y - pw.y) < player.r + pw.r + 8) {
          powerups.splice(i, 1);
          userData.totalItemsCollected++;
          if (userData.totalItemsCollected >= 5) unlockAchievement("item_5");

          if (pw.type === "shield") {
            hasShield = true; sfx.item(); addFloatingText(pw.x, pw.y - 15, "SHIELD UP!", "#00f2fe");
            createParticles(pw.x, pw.y, "#00f2fe", 20);
          } else if (pw.type === "slow") {
            slowTimer = 300; sfx.item(); addFloatingText(pw.x, pw.y - 15, "SLOW MOTION!", "#e0aaff");
            createParticles(pw.x, pw.y, "#b537f2", 20);
          } else if (pw.type === "bomb") {
            sfx.bomb(); triggerShake(16); hitstopFrames = 3;
            const bonus = enemies.length * 120;
            score += bonus;
            addFloatingText(pw.x, pw.y - 15, `MEGA BOMB! +${bonus}`, "#ff7b00");
            enemies.forEach((e) => createParticles(e.x, e.y, "#ff7b00", 10));
            enemies = [];
            createParticles(pw.x, pw.y, "#ff7b00", 35);
          }
        }
      }

      // --- スター ---
      for (let i = stars.length - 1; i >= 0; i--) {
        const s = stars[i];
        s.pulse += 0.12;
        const radius = s.r + Math.sin(s.pulse) * 2.5;

        ctx.shadowBlur = 16; ctx.shadowColor = s.isBossCore ? "#ff0055" : "#ffd700";
        ctx.fillStyle = s.isBossCore ? "#fff" : "#ffd700";
        ctx.beginPath(); ctx.arc(s.x, s.y, radius, 0, Math.PI * 2); ctx.fill();
        if (s.isBossCore) {
          ctx.strokeStyle = "#ffd700"; ctx.lineWidth = 3;
          ctx.beginPath(); ctx.arc(s.x, s.y, radius + 5, 0, Math.PI * 2); ctx.stroke();
        }
        ctx.shadowBlur = 0;

        if (Math.hypot(player.x - s.x, player.y - s.y) < player.r + s.r + 8) {
          stars.splice(i, 1);
          combo++; comboTimer = 185;
          if (combo >= 10) unlockAchievement("combo_10");

          const bonus = 100 * combo;
          score += bonus;
          sfx.star(combo);
          addFloatingText(s.x, s.y - 12, `+${bonus}`, "#ffd700");

          const comboEl = document.getElementById("comboDisplay");
          comboEl.textContent = `COMBO x${combo} (+${bonus})`;
          comboEl.style.opacity = 1;
          createParticles(s.x, s.y, "#ffd700", 16);

          if (s.isBossCore && boss) {
            boss.coresLeft--;
            triggerShake(10);
            if (boss.coresLeft <= 0) {
              sfx.bossDown();
              triggerShake(25);
              hitstopFrames = 5;
              score += 2000;
              addFloatingText(boss.x, boss.y, "BOSS DESTROYED! +2000", "#ffd700");
              createParticles(boss.x, boss.y, "#ffd700", 50);
              createParticles(boss.x, boss.y, "#ff0055", 40);
              enemies = [];
              boss = null;
              document.getElementById("bossBanner").style.display = "none";
              unlockAchievement("boss_kill");
            }
          }

          if (!isFever) {
            feverGauge = Math.min(100, feverGauge + 20);
            if (feverGauge >= 100) {
              isFever = true; feverTimer = 300; sfx.fever(); triggerShake(12);
              unlockAchievement("fever_once");
              addFloatingText(player.x, player.y - 25, "FEVER OVERDRIVE!!", "#ff007f");
              createParticles(player.x, player.y, "#ff007f", 35);
            }
          }
        }
      }

      // --- 敵の更新・描画・GRAZE判定 ---
      const speedMult = slowTimer > 0 ? 0.38 : 1.0;
      for (let i = enemies.length - 1; i >= 0; i--) {
        const e = enemies[i];

        if (e.type === "homing") {
          const desiredAngle = Math.atan2(player.y - e.y, player.x - e.x);
          const curAngle = Math.atan2(e.vy, e.vx);
          const speed = Math.hypot(e.vx, e.vy);
          let diff = desiredAngle - curAngle;
          while (diff > Math.PI) diff -= Math.PI * 2;
          while (diff < -Math.PI) diff += Math.PI * 2;
          const nextAngle = curAngle + Math.sign(diff) * Math.min(Math.abs(diff), 0.045);
          e.vx = Math.cos(nextAngle) * speed;
          e.vy = Math.sin(nextAngle) * speed;
          e.life--;
          if (e.life <= 0) { createParticles(e.x, e.y, "#b537f2", 8); enemies.splice(i, 1); continue; }
        } else if (e.type === "sniper") {
          if (e.aimTimer > 0) {
            e.aimTimer--;
            e.aimAngle = Math.atan2(player.y - e.y, player.x - e.x);
            ctx.strokeStyle = "rgba(249, 255, 0, 0.35)";
            ctx.lineWidth = 1.5;
            ctx.setLineDash([5, 5]);
            ctx.beginPath(); ctx.moveTo(e.x, e.y); ctx.lineTo(e.x + Math.cos(e.aimAngle) * 900, e.y + Math.sin(e.aimAngle) * 900); ctx.stroke();
            ctx.setLineDash([]);
            if (e.aimTimer === 0) {
              const dashSpeed = width < 520 ? 9.2 : 10.5;
              e.vx = Math.cos(e.aimAngle) * dashSpeed;
              e.vy = Math.sin(e.aimAngle) * dashSpeed;
            }
          }
        } else if (e.type === "bomber") {
          e.fuse--;
          if (e.fuse <= 0) {
            createParticles(e.x, e.y, "#ff7b00", 15);
            for (let b = 0; b < 6; b++) {
              const ba = (b * Math.PI) / 3;
              enemies.push({ x: e.x, y: e.y, vx: Math.cos(ba) * 3.3, vy: Math.sin(ba) * 3.3, r: 6.5 * gameScale, type: "normal", grazed: false });
            }
            enemies.splice(i, 1);
            continue;
          }
        }

        e.x += e.vx * speedMult;
        e.y += e.vy * speedMult;

        if (e.x < -70 || e.x > width + 70 || e.y < -70 || e.y > height + 70) {
          enemies.splice(i, 1);
          continue;
        }

        const enemyColorMap = { normal: "#ff0055", homing: "#b537f2", sniper: "#f9ff00", bomber: "#ff7b00" };
        const ec = slowTimer > 0 ? "#80ed99" : enemyColorMap[e.type];

        ctx.shadowBlur = 12; ctx.shadowColor = ec; ctx.fillStyle = ec;
        ctx.beginPath(); ctx.arc(e.x, e.y, e.r, 0, Math.PI * 2); ctx.fill();
        ctx.shadowBlur = 0;

        const dist = Math.hypot(player.x - e.x, player.y - e.y);

        // GRAZE判定
        if (!isFever && !e.grazed && dist >= player.r + e.r && dist < player.r + e.r + 25 * gameScale) {
          e.grazed = true;
          grazeCountInRun++;
          if (grazeCountInRun >= 20) unlockAchievement("graze_20");
          score += 50;
          feverGauge = Math.min(100, feverGauge + 5);
          sfx.graze();
          addFloatingText(player.x, player.y - 18, "⚡GRAZE +50", "#00f2fe");
          createParticles((player.x + e.x) / 2, (player.y + e.y) / 2, "#00f2fe", 5);
        }

        // 衝突判定
        if (dist < player.r + e.r - 3) {
          if (isFever) {
            enemies.splice(i, 1);
            score += 250;
            triggerShake(5);
            addFloatingText(e.x, e.y, "+250", "#ff007f");
            createParticles(e.x, e.y, ec, 18);
          } else if (hasShield) {
            hasShield = false;
            enemies.splice(i, 1);
            sfx.shieldBreak();
            triggerShake(12);
            addFloatingText(player.x, player.y - 20, "SHIELD BLOCK!", "#00f2fe");
            createParticles(player.x, player.y, "#00f2fe", 25);
          } else {
            ctx.restore();
            gameOver();
            return;
          }
        }
      }

      // --- プレイヤー描画 ---
      const activeSkin = SKINS.find((s) => s.id === userData.selectedSkin) || SKINS[0];
      const playerColor = isFever ? "#ff007f" : activeSkin.color;

      player.trail.forEach((pt, idx) => {
        ctx.globalAlpha = (idx / player.trail.length) * 0.35;
        ctx.fillStyle = playerColor;
        ctx.beginPath(); ctx.arc(pt.x, pt.y, player.r * (idx / player.trail.length), 0, Math.PI * 2); ctx.fill();
      });
      ctx.globalAlpha = 1.0;

      ctx.shadowBlur = isFever ? 26 : 18;
      ctx.shadowColor = playerColor;
      drawPlayerShape(player.x, player.y, player.r + (isFever ? 3 : 0), activeSkin.shape, playerColor);
      ctx.shadowBlur = 0;

      if (hasShield) {
        ctx.strokeStyle = "#00f2fe"; ctx.lineWidth = 2; ctx.setLineDash([6, 4]);
        ctx.beginPath(); ctx.arc(player.x, player.y, player.r + 10, frameCount * 0.05, frameCount * 0.05 + Math.PI * 2); ctx.stroke();
        ctx.setLineDash([]);
      }

      ctx.restore();

      document.getElementById("hudScore").textContent = score.toLocaleString();
      const hudFever = document.getElementById("hudFever");
      hudFever.textContent = isFever ? "FEVER!!" : `${feverGauge}%`;
      hudFever.style.color = isFever ? "#ffd700" : "#ff007f";

      document.getElementById("badgeShield").style.display = hasShield ? "inline-block" : "none";
      document.getElementById("badgeSlow").style.display = slowTimer > 0 ? "inline-block" : "none";
    }

    loop();
  </script>
     <script>
    if ("serviceWorker" in navigator) {
      window.addEventListener("load", () => {
        navigator.serviceWorker.register("./sw.js").catch((err) => {
          console.log("SW registration failed:", err);
        });
      });
    }
  </script>
</body>
</html>
   
{
  "name": "NEON DODGE OVERDRIVE",
  "short_name": "NEON DODGE",
  "description": "オンラインランキング対応のネオン回避アクションゲーム",
  "start_url": "./index.html",
  "scope": "./",
  "display": "standalone",
  "orientation": "portrait",
  "background_color": "#07080d",
  "theme_color": "#07080d",
  "icons": [
    {
      "src": "data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 512 512'><rect width='512' height='512' rx='110' fill='%2307080d'/><circle cx='256' cy='256' r='160' fill='none' stroke='%2300f2fe' stroke-width='28'/><text x='256' y='320' font-size='210' text-anchor='middle'>⚡</text></svg>",
      "sizes": "192x192 512x512",
      "type": "image/svg+xml",
      "purpose": "any maskable"
    }
  ]
}
// PWAインストール要件を満たすための最小構成Service Worker
self.addEventListener("install", (event) => {
  self.skipWaiting();
});

self.addEventListener("activate", (event) => {
  event.waitUntil(clients.claim());
});

self.addEventListener("fetch", (event) => {
  // Firebase通信やランキングを常に最新に保つためネットワーク優先で処理
  event.respondWith(fetch(event.request));
});
