<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AZAMBEK - YNGI BOZOR FRUITS</title>
    <style>
        :root {
            --bg-image: url('https://images.unsplash.com/photo-1610832958506-aa56368176cf?auto=format&fit=crop&w=1200&q=80');
            --primary-color: #d35400;
            --accent-color: #e67e22;
        }
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), var(--bg-image) no-repeat center center fixed;
            background-size: cover;
            color: #333;
        }
        .container {
            max-width: 600px;
            margin: 20px auto;
            background: rgba(255, 255, 255, 0.95);
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.3);
            position: relative;
        }
        /* Top Header & QR & Calendar */
        .top-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 13px;
            color: #555;
            border-bottom: 1px solid #ddd;
            padding-bottom: 8px;
            margin-bottom: 15px;
        }
        .qr-code {
            width: 50px;
            height: 50px;
            background: #eee;
            border: 1px solid #ccc;
            text-align: center;
            line-height: 50px;
            font-size: 10px;
            font-weight: bold;
        }
        /* Promo Banner */
        .promo-banner {
            background: #e74c3c;
            color: white;
            padding: 10px;
            border-radius: 8px;
            text-align: center;
            font-weight: bold;
            margin-bottom: 15px;
            animation: pulse 1.5s infinite;
        }
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.02); }
            100% { transform: scale(1); }
        }
        /* Header Info */
        .header-title {
            text-align: center;
        }
        .header-title h1 {
            font-size: 22px;
            color: var(--primary-color);
            margin: 5px 0;
        }
        .address-box {
            font-weight: bold;
            color: #c0392b;
            margin-bottom: 10px;
            text-align: center;
        }
        /* Live & Media Streams */
        .live-section {
            background: #2c3e50;
            color: white;
            padding: 10px;
            border-radius: 8px;
            margin-bottom: 15px;
            text-align: center;
        }
        .live-links a {
            display: inline-block;
            margin: 5px 10px;
            color: #f39c12;
            text-decoration: none;
            font-weight: bold;
        }
        /* Catalog & Grid */
        .catalog-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin-bottom: 15px;
        }
        .card {
            background: #fff;
            border: 1px solid #ddd;
            border-radius: 8px;
            padding: 10px;
            text-align: center;
        }
        .card img {
            width: 100%;
            height: 100px;
            object-fit: cover;
            border-radius: 6px;
        }
        /* Reactions */
        .reactions {
            display: flex;
            justify-content: space-around;
            margin: 15px 0;
            padding: 8px;
            background: #f9f9f9;
            border-radius: 6px;
        }
        .reaction-btn {
            background: none;
            border: none;
            cursor: pointer;
            font-size: 16px;
        }
        /* SOS Button */
        .sos-btn {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: #e74c3c;
            color: white;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            text-align: center;
            line-height: 50px;
            font-weight: bold;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
            text-decoration: none;
            font-size: 14px;
        }
        /* Admin Panel Toggle */
        .admin-panel {
            background: #f1f2f6;
            padding: 10px;
            border-radius: 8px;
            margin-top: 20px;
            border: 1px dashed #ccc;
        }
        .admin-panel input, .admin-panel select {
            width: 100%;
            padding: 6px;
            margin: 5px 0;
            box-sizing: border-box;
        }
    </style>
</head>
<body>

<div class="container">
    <!-- Top Bar: Calendar & QR Code -->
    <div class="top-bar">
        <div id="current-date">Kun, Oy, Yil</div>
        <div class="qr-code">QR-KOD</div>
    </div>

    <!-- Aksiya E'loni -->
    <div class="promo-banner" id="promo-text">
        🔥 AKSIYA: Sherobod anorlari va Sarxil olmalar 20% chegirmada!
    </div>

    <!-- Header & Address -->
    <div class="header-title">
        <h1>AZAMBEK - YAGNI BOZOR FRUITS</h1>
        <div class="address-box">📍 Surxondaryo viloyati, Denov shahri, 103-uy | Tel: +998 -- --- -- --</div>
    </div>

    <!-- Live & Media (Telegram / Instagram) -->
    <div class="live-section">
        🎥 Jonli Efir & Storylar
        <div class="live-links">
            <a href="#" target="_blank">🔴 Instagram Live</a>
            <a href="#" target="_blank">✈️ Telegram Live / Story</a>
        </div>
    </div>

    <!-- Reaksiyalar -->
    <div class="reactions">
        <button class="reaction-btn" onclick="alert('Rahmat!')">👍 Like (0)</button>
        <button class="reaction-btn" onclick="alert('Yoqimli!')">❤️ Yurak (0)</button>
        <button class="reaction-btn" onclick="alert('Super!')">🔥 Olov (0)</button>
        <button class="reaction-btn" onclick="alert('Fikringiz uchun rahmat!')">💬 Fikr</button>
    </div>

    <!-- Mevalar Katalogi (Kengaytirilgan Bloklar) -->
    <h3>🍎 Mevalar va Hamkorlik Katalogi</h3>
    <div class="catalog-grid" id="product-grid">
        <div class="card">
            <img src="https://images.unsplash.com/photo-1615485290382-441e4d049cb5?auto=format&fit=crop&w=300&q=80" alt="Anor">
            <h4>Sherobod Anori</h4>
            <p>Kelishilgan narxda</p>
        </div>
        <div class="card">
            <img src="https://images.unsplash.com/photo-1568702846914-96b305d2aaeb?auto=format&fit=crop&w=300&q=80" alt="Olma">
            <h4>Denov Olmalari (Fuji/Golden)</h4>
            <p>Ulgurji savdo</p>
        </div>
    </div>

    <!-- Admin Panel (Oson o'zgartirish uchun) -->
    <div class="admin-panel">
        <h4>⚙️ Admin Boshqaruvi</h4>
        <input type="text" id="admin-promo" placeholder="Yangi aksiya matnini kiriting...">
        <select id="admin-bg" onchange="changeBackground(this.value)">
            <option value="url('https://images.unsplash.com/photo-1610832958506-aa56368176cf?auto=format&fit=crop&w=1200&q=80')">Mevali Fon (Standard)</option>
            <option value="url('https://images.unsplash.com/photo-1513151233558-d860c5398176?auto=format&fit=crop&w=1200&q=80')">Bayramona Fon</option>
        </select>
        <button onclick="updateSite()" style="width:100%; background:#27ae60; color:white; border:none; padding:8px; border-radius:4px; cursor:pointer; font-weight:bold;">Yangilash</button>
    </div>
</div>

<!-- SOS Yordam tugmasi -->
<a href="tel:+998900000000" class="sos-btn">SOS</a>

<script>
    // Sana va Vaqtni chiqarish
    const d = new Date();
    document.getElementById("current-date").innerText = d.toLocaleDateString('uz-UZ', { year: 'numeric', month: 'long', day: 'numeric' });

    // Admin funksiyalari
    function updateSite() {
        let promo = document.getElementById('admin-promo').value;
        if(promo) {
            document.getElementById('promo-text').innerText = promo;
        }
        alert('Sayt muvaffaqiyatli yangilandi!');
    }

    function changeBackground(bgVal) {
        document.documentElement.style.setProperty('--bg-image', bgVal);
    }
</script>

</body>
</html>

