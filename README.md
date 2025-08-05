<!DOCTYPE html><html lang="bn">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Shohoj World Giga Pub</title>  <!-- Telegram WebApp SDK -->  <script src="https://telegram.org/js/telegram-web-app.js"></script>  <!-- Giga.pub Script -->  <script src="https://ad.gigapub.tech/script?id=1292" defer></script>  <style>
    body {
      font-family: 'Arial', sans-serif;
      background-color: #f9f9f9;
      margin: 0;
      padding: 0;
      color: #333;
    }

    .container {
      padding: 20px;
      max-width: 500px;
      margin: auto;
    }

    .card {
      background: #fff;
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
      margin-bottom: 20px;
    }

    .title {
      font-size: 18px;
      font-weight: bold;
      margin-bottom: 10px;
    }

    .amount {
      font-size: 30px;
      color: #00795a;
      margin: 10px 0;
    }

    .stat-grid {
      display: flex;
      justify-content: space-between;
      text-align: center;
    }

    .stat {
      flex: 1;
    }

    .graph {
      height: 100px;
      background: #eef4f1;
      border-radius: 8px;
      margin-top: 10px;
    }

    .btn-ad {
      background-color: #009a5e;
      color: white;
      padding: 12px;
      border: none;
      border-radius: 8px;
      font-size: 16px;
      width: 100%;
      cursor: pointer;
    }

    .btn-ad:hover {
      background-color: #007d4b;
    }

    .footer-buttons {
      display: flex;
      justify-content: space-between;
      margin-top: 20px;
    }

    .footer-buttons button {
      flex: 1;
      padding: 10px;
      margin: 0 5px;
      border: none;
      border-radius: 6px;
      font-size: 14px;
      cursor: pointer;
    }

    .reset { background-color: #ffdddd; }
    .dev { background-color: #eee; }
  </style></head>
<body>
  <div class="container">
    <div class="card">
      <div class="title">Giga Pub</div>
      <div class="amount">0.01 ৳</div>
    </div><div class="card stat-grid">
  <div class="stat">
    <div>1</div>
    <small>মোট বিজ্ঞাপন</small>
  </div>
  <div class="stat">
    <div>0.01 ৳</div>
    <small>মোট আয়</small>
  </div>
</div>

<div class="card">
  <div class="title">সাপ্তাহিক কার্যকলাপ</div>
  <div class="graph"></div>
</div>

<div class="card">
  <div class="title">আজকের কাজ</div>
  <button class="btn-ad" onclick="showAd()">বিজ্ঞাপন দেখুন</button>
</div>

<div class="footer-buttons">
  <button class="reset">রিসেট</button>
  <button class="dev">&lt;/&gt; ডেভেলপার</button>
</div>

  </div>  <script>
    const tg = window.Telegram.WebApp;
    tg.ready();
    tg.expand();

    function showAd() {
      if (typeof window.showGiga === 'function') {
        window.showGiga()
          .then(() => alert('✅ বিজ্ঞাপন শেষ, আপনি পুরস্কার পেয়েছেন!'))
          .catch(() => alert('❌ বিজ্ঞাপন দেখানো যায়নি'));
      } else {
        alert('⚠️ বিজ্ঞাপন এখনো লোড হয়নি, একটু অপেক্ষা করুন');
      }
    }
  </script></body>
</html>
