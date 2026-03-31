# bilgisayar-Uygulamalar-Proje
Bilgisayar uygulamaları proje ödevi
[index.html](https://github.com/user-attachments/files/26377942/index.html)
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Fiyat Tahmincisi Pro</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;600;700&display=swap" rel="stylesheet">
    <!-- Stil Dosyası -->
    <link rel="stylesheet" href="style.css">
    <!-- FontAwesome (İkonlar için, isteğe bağlı) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <div class="background-effects">
        <div class="glow-orb purple-orb"></div>
        <div class="glow-orb yellow-orb"></div>
    </div>

    <main class="app-container">
        <!-- Settings Header (API Key) -->
        <header class="settings-header">
            <details class="api-settings">
                <summary><i class="fa-solid fa-gear"></i> Yapay Zeka Ayarları (API Key)</summary>
                <div class="settings-content">
                    <p class="settings-hint">Gerçek Yapay Zeka (Google Gemini) tahminleri için ücretsiz bir API Anahtarı girin.</p>
                    <input type="password" id="api-key-input" placeholder="Gemini API Anahtarınızı Buraya Girin" autocomplete="off" />
                    <small>Anahtarınız sadece tarayıcınızda (yerel olarak) tutulur.</small>
                </div>
            </details>
        </header>

        <!-- Main Content -->
        <section class="hero-section">
            <h1 class="gradient-text">Geleceğin Fiyatını Tahmin Et.</h1>
            <p class="subtitle">Yapay Zeka ve güncel enflasyon dinamiklerini kullanarak, dilediğiniz ürünün <strong>Gelecek Ayki</strong> veya <strong>Yıl Sonundaki</strong> olası fiyatını öğrenin.</p>
        </section>

        <section class="predictor-card glass-panel">
            <form id="prediction-form">
                <div class="input-group">
                    <label for="product-name"><i class="fa-solid fa-tag"></i> Hangi ürünü tahmin edelim?</label>
                    <input type="text" id="product-name" required placeholder="Örn: iPhone 15 Pro, 1 Litre Süt, Kira..." autocomplete="off">
                </div>

                <div class="input-group">
                    <label for="current-price"><i class="fa-solid fa-wallet"></i> Mevcut Fiyatı (Opsiyonel - TL)</label>
                    <input type="number" id="current-price" placeholder="Örn: 80000" autocomplete="off" min="0" step="any">
                </div>

                <button type="submit" class="glow-button yellow-btn" id="predict-btn">
                    <span>Yapay Zekaya Sor</span>
                    <i class="fa-solid fa-wand-magic-sparkles"></i>
                </button>
            </form>
        </section>

        <!-- Result Section (Gizli olarak başlar) -->
        <section class="result-card glass-panel hidden" id="result-container">
            <div class="loading-state hidden" id="loading-spinner">
                <div class="spinner"></div>
                <p>Yapay Zeka piyasayı ve enflasyonu analiz ediyor...</p>
            </div>

            <div class="result-content hidden" id="result-data">
                <h2 class="result-title">Yapay Zeka Tahmini</h2>
                <div class="prediction-box text-glow-yellow">
                    <span id="predicted-price-value">0 TL</span>
                </div>
                <div class="ai-analysis">
                    <h3><i class="fa-solid fa-brain"></i> AI Değerlendirmesi:</h3>
                    <p id="ai-reasoning">Analiz yükleniyor...</p>
                </div>
                
                <div class="disclaimer">
                    <i class="fa-solid fa-circle-exclamation"></i> Bu tahmin yapay zeka tarafından yapılmıştır, yatırım tavsiyesi değildir.
                </div>
            </div>
        </section>
    </main>

    <!-- Script Dosyası -->
    <script src="app.js"></script>
</body>
</html>
