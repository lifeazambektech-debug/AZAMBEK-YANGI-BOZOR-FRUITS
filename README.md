
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AZAMBEK AI OPTOVIK - Denov</title>
    <style>
        :root {
            --primary-color: #f59e0b;
            --primary-dark: #d97706;
            --text-dark: #1f2937;
            --bg-light: #fffbeb;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--bg-light);
            color: var(--text-dark);
        }
        .hero {
            position: relative;
            height: 60vh;
            background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.6)), url('https://files.catbox.moe/fe5i8g.jpg') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            text-align: center;
            padding: 1rem;
        }
        .hero h1 {
            font-size: 3rem;
            margin: 0;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.5);
        }
        .hero p {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary-color);
            text-shadow: 1px 1px 5px rgba(0,0,0,0.5);
        }
        .container {
            max-width: 1100px;
            margin: -50px auto 0 auto;
            padding: 0 15px;
            position: relative;
            z-index: 10;
        }
        .stats-bar {
            background: white;
            padding: 20px;
            border-radius: 15px;
            display: flex;
            justify-content: space-around;
            align-items: center;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            margin-bottom: 30px;
        }
        .stat-item {
            text-align: center;
        }
        .stat-value {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary-dark);
        }
        .btn {
            background-color: var(--primary-color);
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s, transform 0.2s;
            text-decoration: none;
            display: inline-block;
        }
        .btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
        }
        .share-btn {
            background-color: #3b82f6;
        }
        .share-btn:hover {
            background-color: #2563eb;
        }
        .card {
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            margin-bottom: 30px;
        }
        .card h2 {
            border-bottom: 2px solid var(--primary-color);
            padding-bottom: 10px;
            margin-top: 0;
            color: var(--primary-dark);
        }
        .news-item {
            padding: 15px 0;
            border-bottom: 1px solid #e5e7eb;
        }
        .news-item:last-child {
            border-bottom: none;
        }
        .news-date {
            font-size: 0.85rem;
            color: #6b7280;
        }
        .catalog-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        .product-card {
            background: white;
            border: 1px solid #e5e7eb;
            border-radius: 10px;
            overflow: hidden;
            transition: box-shadow 0.3s;
        }
        .product-card:hover {
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        .product-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        .product-info {
            padding: 15px;
        }
        .price {
            font-weight: bold;
            color: var(--primary-dark);
            font-size: 1.2rem;
        }
        .ai-assistant {
            position: fixed;
            bottom: 30px;
            right: 30px;
            z-index: 100;
            display: flex;
            align-items: flex-end;
            gap: 15px;
        }
        .chat-bubble {
            background: white;
            padding: 15px 20px;
            border-radius: 20px 20px 4px 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
            max-width: 280px;
            border: 2px solid var(--primary-color);
            font-weight: 500;
        }
        .avatar {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, #f59e0b, #ef4444);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 2rem;
            color: white;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            border: 4px solid white;
        }
        footer {
            background-color: #1f2937;
            color: white;
            text-align: center;
            padding: 40px 20px;
            margin-top: 50px;
        }
        .contact-details {
            display: inline-block;
            text-align: left;
            margin-top: 20px;
            background: #374151;
            padding: 20px;
            border-radius: 10px;
        }
    </style>
</head>
<body>

    <div class="hero">
        <h1>AZAMBEK AI OPTOVIK</h1>
        <p>Denov shahri bo'yicha eng sarxil mevalar va islohotlar markazi</p>
    </div>

    <div class="container">
        <!-- Obunachilar va Interaktiv Panel -->
        <div class="stats-bar">
            <div class="stat-item">
                <div class="stat-value" id="subscribers">12,450</div>
                <div>Obunachilar</div>
            </div>
            <div>
                <button class="btn" onclick="handleSubscribe()">🔔 Obuna Bo'lish</button>
                <button class="btn share-btn" onclick="handleShare()">🔗 Ulashish</button>
            </div>
        </div>

        <!-- Biz Haqimizda -->
        <div class="card">
            <h2>Biz Haqimizda</h2>
            <p>AZAMBEK AI OPTOVIK — xalqimizga eng sifatli, sarxil va arzon mevalarni yetkazib berishga qaratilgan yirik loyiha. Biz mahalliy dehqonlarimiz mahsulotlarini jahon standartlariga moslab, eng qulay shartlarda taqdim etamiz.</p>
        </div>

        <!-- Yangiliklar va Islohotlar Lentasi -->
        <div class="card">
            <h2>Dunyoviy va O'zbekiston Yangiliklari</h2>
            <div class="news-item">
                <span class="news-date">Bugun, 11:00</span>
                <h3>O'zbekistonda meva-sabzavot eksporti hajmi keskin oshdi</h3>
                <p>Yangi islohotlar doirasida fermerlarga yaratilgan imkoniyatlar sharofati bilan Denovdan xorijga mevalar yetkazib berish ko'lami kengaydi.</p>
            </div>
            <div class="news-item">
                <span class="news-date">Kecha</span>
                <h3>Jahon bozorida qishloq xo'jaligi mahsulotlari narxlari tahlili</h3>
                <p>Global miqyosda tabiiy va vitaminlarga boy mahsulotlarga talab ortib bormoqda, bu esa mahalliy ishlab chiqaruvchilar uchun katta imkoniyat.</p>
            </div>
        </div>

        <!-- Mahsulotlar Katalogi -->
        <div class="card">
            <h2>Mevalar Katalogi</h2>
            <div class="catalog-grid">
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1590080875707-e38048d6168e?auto=format&fit=crop&q=80&w=500" alt="Anor">
                    <div class="product-info">
                        <h3>Sherobod Anori</h3>
                        <p>O'ta shirin va vitaminlarga boy, sarxil tanlov.</p>
                        <div class="price">Kelishilgan narxda</div>
                    </div>
                </div>
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1560806887-1e4cd0b6cbd6?auto=format&fit=crop&q=80&w=500" alt="Olma">
                    <div class="product-info">
                        <h3>Denov Olmalari (Golden, Fuji)</h3>
                        <p>Bevosita bog'dan, qadoqlangan va saralangan.</p>
                        <div class="price">Ulgurji narxda</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Kontakt va Manzil -->
        <div style="text-align: center;">
            <div class="contact-details">
                <h3>📍 Manzilimiz:</h3>
                <p>Surxondaryo viloyati, Denov tumani, Oqqo‘rg‘on mahallasi, Adolat 2-berk ko‘cha, 103A-uy.</p>
                <h3>📞 Aloqa uchun:</h3>
                <p style="font-size: 1.5rem; font-weight: bold; color: var(--primary-color);">+998 99 539 57 96</p>
            </div>
        </div>
    </div>

    <!-- AI Robot-qiz Yordamchi -->
    <div class="ai-assistant">
        <div class="chat-bubble">
            Salom! Men AZAMBEK AI Yordamchisiman. Narxlar va yetkazib berish bo'yicha savollaringizni bering!
        </div>
        <div class="avatar">
            👩‍💻
        </div>
    </div>

    <footer>
        <p>&copy; 2026 AZAMBEK AI OPTOVIK. Barcha huquqlar himoyalangan.</p>
    </footer>

    <script>
        function handleSubscribe() {
            const subElem = document.getElementById('subscribers');
            let count = parseInt(subElem.innerText.replace(/,/g, ''));
            count++;
            subElem.innerText = count.toLocaleString();
            alert("Kanalimizga obuna bo'lganingiz uchun rahmat!");
        }

        function handleShare() {
            if (navigator.share) {
                navigator.share({
                    title: 'AZAMBEK AI OPTOVIK',
                    text: 'Denovdan eng sarxil mevalar va yangiliklar!',
                    url: window.location.href
                }).catch(() => {});
            } else {
                alert("Havola nusxalandi!");
            }
        }
    </script>
</body>
</html>
