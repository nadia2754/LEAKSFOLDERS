<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes, viewport-fit=cover">
  <title>🔥 Exclusive Vault · Mobile Collectibles</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
      background: linear-gradient(145deg, #0a0a0a 0%, #1a0b1e 100%);
      min-height: 100vh;
      padding: 1rem 0.9rem 2rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      scroll-behavior: smooth;
    }

    .store {
      width: 100%;
      max-width: 450px;
      display: flex;
      flex-direction: column;
      gap: 1.2rem;
    }

    .header {
      text-align: center;
      margin-bottom: 0.5rem;
    }
    .header h1 {
      font-size: 2.2rem;
      font-weight: 800;
      letter-spacing: 1px;
      background: linear-gradient(to right, #c084fc, #38bdf8, #ef4444);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      filter: drop-shadow(0 0 6px #7e22ce55);
    }
    .header p {
      color: #cbd5e1;
      font-size: 0.9rem;
      margin-top: 0.2rem;
    }

    .card {
      background: rgba(15, 10, 20, 0.9);
      backdrop-filter: blur(18px);
      border-radius: 2rem;
      padding: 0.9rem;
      display: flex;
      align-items: center;
      gap: 0.8rem;
      box-shadow: 0 20px 30px -10px rgba(0,0,0,0.7), 0 0 0 1px rgba(168,85,247,0.25);
      border: 1px solid rgba(255,255,255,0.07);
      transition: transform 0.2s ease, box-shadow 0.2s;
      position: relative;
      overflow: hidden;
    }
    .card:hover {
      transform: scale(1.01);
      box-shadow: 0 25px 35px -12px #7e22ce88;
    }

    .media-box {
      width: 85px;
      height: 85px;
      border-radius: 1.5rem;
      background: #1e1b2b;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      position: relative;
      overflow: hidden;
      box-shadow: 0 8px 14px rgba(0,0,0,0.6);
      border: 1px solid rgba(192,132,252,0.5);
    }
    .media-box img,
    .media-box video {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .info {
      flex: 1;
      display: flex;
      flex-direction: column;
      gap: 0.4rem;
    }
    .model-name {
      font-weight: 700;
      font-size: 1.25rem;
      color: #f8fafc;
      letter-spacing: 0.3px;
      text-shadow: 0 2px 5px black;
    }
    .description {
      font-size: 0.8rem;
      color: #a5b4fc;
      line-height: 1.3;
      display: flex;
      align-items: center;
      gap: 0.3rem;
      flex-wrap: wrap;
    }
    .badge-popular {
      background: #dc2626;
      color: white;
      font-size: 0.65rem;
      font-weight: 700;
      padding: 0.2rem 0.5rem;
      border-radius: 20px;
      letter-spacing: 0.4px;
      background: linear-gradient(135deg, #ef4444, #b91c1c);
    }

    .buy-btn {
      background: linear-gradient(135deg, #25D366, #0f9d4a);
      border: none;
      width: 52px;
      height: 52px;
      border-radius: 28px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.8rem;
      font-weight: 700;
      color: white;
      box-shadow: 0 8px 16px rgba(37,211,102,0.45);
      cursor: pointer;
      transition: all 0.2s ease;
      flex-shrink: 0;
      text-decoration: none;
      touch-action: manipulation;
      border: 1px solid #25D366;
      background: #0d3320;
    }
    .buy-btn:active {
      transform: scale(0.92);
      background: #25D366;
      box-shadow: 0 0 22px #25D366cc;
    }

    .full-access {
      background: linear-gradient(135deg, #2d1a2c, #0f0b14);
      border: 2px solid #fbbf24;
      box-shadow: 0 0 28px #f59e0b88, 0 10px 20px black;
      position: relative;
    }
    .full-access .media-box {
      border-color: #fbbf24;
      background: #241f0f;
    }
    .full-access .buy-btn {
      background: #b45309;
      border: 1px solid #fbbf24;
      width: 62px;
      height: 62px;
      font-size: 2rem;
      background: linear-gradient(145deg, #f59e0b, #b45309);
      box-shadow: 0 0 28px #fbbf24;
    }
    .hot-label {
      position: absolute;
      top: 8px;
      right: 12px;
      background: #dc2626;
      color: white;
      font-weight: 800;
      font-size: 0.7rem;
      padding: 0.25rem 0.8rem;
      border-radius: 30px;
      letter-spacing: 0.5px;
      background: linear-gradient(to right, #ef4444, #7f1d1d);
      animation: pulse 1.4s infinite;
    }
    @keyframes pulse {
      0% { opacity: 0.9; transform: scale(1); }
      50% { opacity: 1; transform: scale(1.07); background: #f87171; }
      100% { opacity: 0.9; transform: scale(1); }
    }
    .social-proof {
      background: #1e1030;
      border-radius: 30px;
      padding: 0.3rem 1rem;
      font-weight: 700;
      color: #fcd34d;
      font-size: 0.75rem;
      display: inline-flex;
      align-items: center;
      gap: 0.2rem;
      margin-top: 0.2rem;
    }

    .notification-container {
      position: fixed;
      bottom: 18px;
      left: 50%;
      transform: translateX(-50%);
      z-index: 999;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.5rem;
      width: 90%;
      max-width: 400px;
      pointer-events: none;
    }
    .toast {
      background: rgba(20, 10, 30, 0.9);
      backdrop-filter: blur(18px);
      border-left: 5px solid #c084fc;
      border-radius: 2rem;
      padding: 0.7rem 1.3rem;
      color: #f1f5f9;
      font-weight: 600;
      font-size: 0.9rem;
      box-shadow: 0 10px 25px #000000cc;
      animation: slideUp 0.4s ease, fadeOut 0.5s 3.5s forwards;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      width: fit-content;
      max-width: 100%;
      border: 1px solid #7e22ce;
    }
    @keyframes slideUp {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes fadeOut {
      to { opacity: 0; transform: translateY(-10px); }
    }
    .toast span {
      color: #facc15;
      font-weight: 700;
    }
  </style>
</head>
<body>

  <!-- ==================== NOTIFICATION CONTAINER ==================== -->
  <div class="notification-container" id="notificationContainer"></div>

  <div class="store">
    <div class="header">
      <h1>✦ EXCLUSIVE VAULT ✦</h1>
      <p>🔮 Tap 💲 to buy on Telegram</p>
    </div>

    <!-- ============================================ -->
    <!-- CARD 1: cp1-4 PHOTO                         -->
    <!-- ============================================ -->
    <div class="card">
      <div class="media-box">
        <!-- 👀👀👀👀 COLA AQUI O LINK DA IMAGEM DA cp1-4 👀👀👀👀 -->
        <!-- EXEMPLO: <img src="https://i.imgur.com/EXEMPLO123.jpg" alt="cp1-4"> -->
        <img src="👀👀👀👀" alt="cp1-4" onerror="this.style.display='none'; this.parentNode.innerHTML='<span style=font-size:2.4rem;color:#d8b4fe;opacity:0.7>🌸</span>'">
      </div>
      <div class="info">
        <div class="model-name">cp1-4</div>
        <div class="description">✨ Exclusive set</div>
      </div>
      <button class="buy-btn" onclick="buyProduct('cp1-4', 'photo')" aria-label="Buy cp1-4">💲</button>
    </div>

    <!-- ============================================ -->
    <!-- CARD 2: all ©🅿 PHOTO                       -->
    <!-- ============================================ -->
    <div class="card">
      <div class="media-box">
        <!-- 👀👀👀👀 COLA AQUI O LINK DA IMAGEM DA all ©🅿 👀👀👀👀 -->
        <!-- EXEMPLO: <img src="https://i.imgur.com/EXEMPLO456.jpg" alt="all ©🅿"> -->
        <img src="👀👀👀👀" alt="all ©🅿" onerror="this.style.display='none'; this.parentNode.innerHTML='<span style=font-size:2.4rem;color:#d8b4fe;opacity:0.7>🎴</span>'">
      </div>
      <div class="info">
        <div class="model-name">all ©🅿</div>
        <div class="description">Rare collection</div>
      </div>
      <button class="buy-btn" onclick="buyProduct('all ©🅿', 'photo')">💲</button>
    </div>

    <!-- ============================================ -->
    <!-- CARD 3: black ©🅿 PHOTO                     -->
    <!-- ============================================ -->
    <div class="card">
      <div class="media-box">
        <!-- 👀👀👀👀 COLA AQUI O LINK DA IMAGEM DA black ©🅿 👀👀👀👀 -->
        <img src="👀👀👀👀" alt="black ©🅿" onerror="this.style.display='none'; this.parentNode.innerHTML='<span style=font-size:2.4rem;color:#d8b4fe;opacity:0.7>🖤</span>'">
      </div>
      <div class="info">
        <div class="model-name">black ©🅿</div>
        <div class="description">Dark elegance</div>
      </div>
      <button class="buy-btn" onclick="buyProduct('black ©🅿', 'photo')">💲</button>
    </div>

    <!-- ============================================ -->
    <!-- CARD 4: high school PHOTO                   -->
    <!-- ============================================ -->
    <div class="card">
      <div class="media-box">
        <!-- 👀👀👀👀 COLA AQUI O LINK DA IMAGEM DA high school 👀👀👀👀 -->
        <img src="👀👀👀👀" alt="high school" onerror="this.style.display='none'; this.parentNode.innerHTML='<span style=font-size:2.4rem;color:#d8b4fe;opacity:0.7>📚</span>'">
      </div>
      <div class="info">
        <div class="model-name">high school</div>
        <div class="description">Sweet memories</div>
      </div>
      <button class="buy-btn" onclick="buyProduct('high school', 'photo')">💲</button>
    </div>

    <!-- ============================================ -->
    <!-- CARD 5: amelia PHOTO                        -->
    <!-- ============================================ -->
    <div class="card">
      <div class="media-box">
        <!-- 👀👀👀👀 COLA AQUI O LINK DA IMAGEM DA amelia 👀👀👀👀 -->
        <img src="👀👀👀👀" alt="amelia" onerror="this.style.display='none'; this.parentNode.innerHTML='<span style=font-size:2.4rem;color:#d8b4fe;opacity:0.7>🌙</span>'">
      </div>
      <div class="info">
        <div class="model-name">amelia</div>
        <div class="description">Soft glow</div>
      </div>
      <button class="buy-btn" onclick="buyProduct('amelia', 'photo')">💲</button>
    </div>

    <!-- ============================================ -->
    <!-- CARD 6: 💲n🅰pg🅾d PHOTO                    -->
    <!-- ============================================ -->
    <div class="card">
      <div class="media-box">
        <!-- 👀👀👀👀 COLA AQUI O LINK DA IMAGEM DA 💲n🅰pg🅾d 👀👀👀👀 -->
        <img src="👀👀👀👀" alt="💲n🅰pg🅾d" onerror="this.style.display='none'; this.parentNode.innerHTML='<span style=font-size:2.4rem;color:#d8b4fe;opacity:0.7>💎</span>'">
      </div>
      <div class="info">
        <div class="model-name">💲n🅰pg🅾d</div>
        <div class="description">Gold edition</div>
      </div>
      <button class="buy-btn" onclick="buyProduct('💲n🅰pg🅾d', 'photo')">💲</button>
    </div>

    <!-- ============================================ -->
    <!-- CARD 7: LIZZY PHOTO (Most Purchased)        -->
    <!-- ============================================ -->
    <div class="card" style="border-color: #f472b6;">
      <div class="media-box">
        <!-- 👀👀👀👀 COLA AQUI O LINK DA IMAGEM DA LIZZY 👀👀👀👀 -->
        <img src="👀👀👀👀" alt="LIZZY" onerror="this.style.display='none'; this.parentNode.innerHTML='<span style=font-size:2.4rem;color:#d8b4fe;opacity:0.7>👑</span>'">
      </div>
      <div class="info">
        <div class="model-name">LIZZY</div>
        <div class="description">
          🔥 Most purchased 
          <span class="badge-popular">370 purchased this week</span>
        </div>
      </div>
      <button class="buy-btn" onclick="buyProduct('LIZZY', 'photo')">💲</button>
    </div>

    <!-- ============================================ -->
    <!-- CARD 8: mae e filho PHOTO                   -->
    <!-- ============================================ -->
    <div class="card">
      <div class="media-box">
        <!-- 👀👀👀👀 COLA AQUI O LINK DA IMAGEM DA mae e filho 👀👀👀👀 -->
        <img src="👀👀👀👀" alt="mae e filho" onerror="this.style.display='none'; this.parentNode.innerHTML='<span style=font-size:2.4rem;color:#d8b4fe;opacity:0.7>👩‍👦</span>'">
      </div>
      <div class="info">
        <div class="model-name">mae e filho</div>
        <div class="description">Mom & Son</div>
      </div>
      <button class="buy-btn" onclick="buyProduct('mae e filho', 'photo')">💲</button>
    </div>

    <!-- ============================================ -->
    <!-- CARD 9: pai e filha PHOTO                   -->
    <!-- ============================================ -->
    <div class="card">
      <div class="media-box">
        <!-- 👀👀👀👀 COLA AQUI O LINK DA IMAGEM DA pai e filha 👀👀👀👀 -->
        <img src="👀👀👀👀" alt="pai e filha" onerror="this.style.display='none'; this.parentNode.innerHTML='<span style=font-size:2.4rem;color:#d8b4fe;opacity:0.7>👨‍👧</span>'">
      </div>
      <div class="info">
        <div class="model-name">pai e filha</div>
        <div class="description">Dad & Daughter</div>
      </div>
      <button class="buy-btn" onclick="buyProduct('pai e filha', 'photo')">💲</button>
    </div>

    <!-- ============================================ -->
    <!-- CARD 10: FULL ACCESS PACK [all]             -->
    <!-- ============================================ -->
    <div class="card full-access">
      <div class="hot-label">🔥 HOT</div>
      <div class="media-box">
        <!-- <img width="1280" height="675" alt="FULL ACCESS" src="https://github.com/user-attachments/assets/9c8773fc-277f-4b0d-b7b5-d66f49110693" /> COLA AQUI O LINK DA IMAGEM/VIDEO DO FULL ACCESS <img width="1280" height="675" alt="FULL ACCESS" src="https://github.com/user-attachments/assets/9c8773fc-277f-4b0d-b7b5-d66f49110693" /> -->
        <!-- Para IMAGEM: <img src="COLA-LINK-AQUI" alt="Full Access"> -->
        <!-- Para VIDEO: <video src="COLA-LINK-AQUI" autoplay muted loop playsinline></video> -->
        <img src="<img width="1280" height="675" alt="FULL ACCESS" src="https://github.com/user-attachments/assets/9c8773fc-277f-4b0d-b7b5-d66f49110693" />" alt="Full Access" onerror="this.style.display='none'; this.parentNode.innerHTML='<span style=font-size:2.4rem;color:#d8b4fe;opacity:0.7>🌟</span>'">
      </div>
      <div class="info">
        <div class="model-name" style="color: #fcd34d;">FULL ACCESS [all]</div>
        <div class="description">All content unlocked</div>
        <div class="social-proof">
          <span>⚡ Acquired by over 300 people just today!</span>
        </div>
      </div>
      <button class="buy-btn" onclick="buyProduct('FULL ACCESS all', 'pack')">💲</button>
    </div>

  </div>

  <script>
    (function() {
      const TELEGRAM_USER = "douglasbowman88217";
      
      function buildTelegramUrl(modelName, type) {
        let message = "";
        if (modelName === 'FULL ACCESS all') {
          message = "I want to buy the Full Access Pack";
        } else {
          message = `I want to buy ${modelName}'s photo`;
        }
        return `https://t.me/${TELEGRAM_USER}?text=${encodeURIComponent(message)}`;
      }

      window.buyProduct = function(modelName, type) {
        const url = buildTelegramUrl(modelName, type);
        showPurchaseNotification(modelName);
        window.open(url, '_blank');
      };

      function showPurchaseNotification(modelName) {
        const container = document.getElementById('notificationContainer');
        if (!container) return;
        const toast = document.createElement('div');
        toast.className = 'toast';
        const displayName = modelName === 'FULL ACCESS all' ? 'Full Access Pack' : modelName;
        toast.innerHTML = `🛒 <span>${displayName}</span> was purchased`;
        container.appendChild(toast);
        setTimeout(() => {
          if (toast && toast.parentNode === container) {
            container.removeChild(toast);
          }
        }, 4200);
      }

      const modelNames = [
        "cp1-4", "all ©🅿", "black ©🅿", "high school", "amelia",
        "💲n🅰pg🅾d", "LIZZY", "mae e filho", "pai e filha", "FULL ACCESS all"
      ];

      function randomNotification() {
        const randomModel = modelNames[Math.floor(Math.random() * modelNames.length)];
        showPurchaseNotification(randomModel);
      }

      function scheduleNext() {
        const delay = Math.floor(Math.random() * 8000) + 10000;
        setTimeout(() => {
          randomNotification();
          scheduleNext();
        }, delay);
      }
      scheduleNext();

      setTimeout(() => showPurchaseNotification("LIZZY"), 8000);
      setTimeout(() => showPurchaseNotification("💲n🅰pg🅾d"), 18000);
      setTimeout(() => showPurchaseNotification("FULL ACCESS all"), 25000);
    })();
  </script>
</body>
</html>





