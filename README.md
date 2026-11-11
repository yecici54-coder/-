[index.html](https://github.com/user-attachments/files/34682518/index.html)
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>巷口時光｜臺中第二市場</title>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+TC:wght@400;500;600;700;900&family=Noto+Sans+TC:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
/* ==========================================
   巷口時光｜臺中第二市場 CSS 樣式表
   ========================================== */

/* 全域變數設定 */
:root {
    --primary-color: #8c2d19;      /* 磚紅 / 復古印章紅 */
    --primary-hover: #6d2212;
    --text-main: #2b2b2b;          /* 深灰墨色 */
    --text-muted: #666666;         /* 灰褐色 */
    --bg-main: #f9f7f2;            /* 溫潤米白紙質色 */
    --bg-card: #ffffff;
    --bg-dark: #1e1e1e;
    --border-color: #e2ddd3;
    --font-serif: 'Noto Serif TC', "Songti TC", "PMingLiU", serif;
    --font-sans: 'Noto Sans TC', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    --transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
}

/* 重設基本與全域樣式 */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    font-size: 16px;
}

body {
    background-color: var(--bg-main);
    color: var(--text-main);
    font-family: var(--font-sans);
    line-height: 1.8;
    letter-spacing: 0.03em;
    overflow-x: hidden;
}

img {
    max-width: 100%;
    height: auto;
    display: block;
    object-fit: cover;
}

a {
    color: inherit;
    text-decoration: none;
    transition: var(--transition);
}

/* 視覺架構控制 */
.section {
    padding: 100px 8%;
    max-width: 1400px;
    margin: 0 auto;
}

.eyebrow {
    font-family: var(--font-sans);
    font-size: 0.85rem;
    font-weight: 700;
    letter-spacing: 0.25em;
    color: var(--primary-color);
    margin-bottom: 1rem;
    text-transform: uppercase;
}

h2 {
    font-family: var(--font-serif);
    font-size: 2.5rem;
    font-weight: 700;
    line-height: 1.3;
    color: var(--text-main);
}

/* ==========================================
   1. 導覽列 Navbar
   ========================================== */
.navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 24px 8%;
    background-color: rgba(249, 247, 242, 0.92);
    backdrop-filter: blur(10px);
    z-index: 1000;
    border-bottom: 1px solid rgba(226, 221, 211, 0.6);
}

.navbar .logo {
    font-family: var(--font-serif);
    font-size: 1.6rem;
    font-weight: 900;
    letter-spacing: 0.05em;
    color: var(--text-main);
}

.navbar .logo span {
    color: var(--primary-color);
}

.navbar nav {
    display: flex;
    gap: 36px;
}

.navbar nav a {
    font-size: 0.95rem;
    font-weight: 500;
    color: var(--text-main);
    position: relative;
}

.navbar nav a::after {
    content: '';
    position: absolute;
    bottom: -6px;
    left: 0;
    width: 0;
    height: 2px;
    background-color: var(--primary-color);
    transition: var(--transition);
}

.navbar nav a:hover::after {
    width: 100%;
}

.nav-button {
    font-size: 0.9rem;
    font-weight: 500;
    padding: 10px 22px;
    border: 1px solid var(--text-main);
    border-radius: 50px;
    background: transparent;
}

.nav-button:hover {
    background-color: var(--text-main);
    color: var(--bg-main);
}

/* ==========================================
   2. 首頁主視覺 Hero Section
   ========================================== */
.hero {
    min-height: 100vh;
    padding: 140px 8% 80px 8%;
    display: grid;
    grid-template-columns: 1.2fr 1fr;
    align-items: center;
    gap: 60px;
    position: relative;
    max-width: 1400px;
    margin: 0 auto;
}

.hero-content {
    z-index: 2;
}

.small-title {
    font-size: 0.85rem;
    font-weight: 700;
    letter-spacing: 0.3em;
    color: var(--primary-color);
    margin-bottom: 1.5rem;
}

.hero h1 {
    font-family: var(--font-serif);
    font-size: 3.8rem;
    font-weight: 900;
    line-height: 1.25;
    margin-bottom: 2rem;
    letter-spacing: 0.02em;
}

.hero h1 span {
    color: var(--primary-color);
    position: relative;
}

.hero-description {
    font-size: 1.15rem;
    color: var(--text-muted);
    margin-bottom: 3rem;
    line-height: 1.9;
}

.main-button {
    display: inline-block;
    padding: 16px 36px;
    background-color: var(--primary-color);
    color: #ffffff;
    font-size: 1rem;
    font-weight: 500;
    border-radius: 4px;
    box-shadow: 0 10px 25px rgba(140, 45, 25, 0.2);
}

.main-button:hover {
    background-color: var(--primary-hover);
    transform: translateY(-3px);
    box-shadow: 0 15px 30px rgba(140, 45, 25, 0.3);
}

.hero-image {
    position: relative;
    width: 100%;
    height: 540px;
}

.hero-image img {
    width: 100%;
    height: 100%;
    border-radius: 8px;
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.08);
}

.image-label {
    position: absolute;
    bottom: -25px;
    left: -25px;
    background-color: var(--bg-card);
    padding: 20px 30px;
    border-radius: 6px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.06);
    border: 1px solid var(--border-color);
}

.image-label span {
    font-size: 0.8rem;
    font-weight: 700;
    color: var(--primary-color);
    letter-spacing: 0.1em;
}

.image-label p {
    font-family: var(--font-serif);
    font-size: 1rem;
    font-weight: 600;
    margin-top: 4px;
}

.hero-side-text {
    position: absolute;
    right: -80px;
    top: 50%;
    transform: rotate(90deg) translateY(-50%);
    font-size: 0.75rem;
    letter-spacing: 0.4em;
    color: #c5c0b6;
    white-space: nowrap;
}

/* ==========================================
   3. 市場介紹 About Section
   ========================================== */
.about-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    margin-top: 60px;
    align-items: center;
}

.about-image {
    position: relative;
}

.about-image img {
    width: 100%;
    height: 480px;
    border-radius: 8px;
    filter: sepia(15%);
}

.photo-number {
    position: absolute;
    top: 20px;
    left: 20px;
    background: rgba(0, 0, 0, 0.6);
    color: #fff;
    padding: 6px 14px;
    font-size: 0.75rem;
    letter-spacing: 0.2em;
    border-radius: 4px;
}

.about-text {
    padding-right: 20px;
}

.text-tag {
    font-size: 0.8rem;
    font-weight: 700;
    letter-spacing: 0.2em;
    color: var(--text-muted);
    margin-bottom: 10px;
}

.about-text h3 {
    font-family: var(--font-serif);
    font-size: 2rem;
    line-height: 1.4;
    margin-bottom: 24px;
}

.about-text p {
    color: var(--text-muted);
    margin-bottom: 20px;
    font-size: 1.05rem;
}

.text-link {
    display: inline-block;
    margin-top: 15px;
    font-weight: 700;
    color: var(--primary-color);
    border-bottom: 2px solid var(--primary-color);
    padding-bottom: 4px;
}

.text-link:hover {
    color: var(--primary-hover);
    border-color: var(--primary-hover);
    padding-left: 6px;
}

/* ==========================================
   4. 六角樓 Architecture Section
   ========================================== */
.architecture-top {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    margin-bottom: 60px;
    align-items: flex-end;
}

.architecture-intro {
    color: var(--text-muted);
    font-size: 1.1rem;
    line-height: 1.9;
}

.architecture-image {
    position: relative;
    width: 100%;
    height: 500px;
    border-radius: 8px;
    overflow: hidden;
}

.architecture-image img {
    width: 100%;
    height: 100%;
    transition: var(--transition);
}

.architecture-image:hover img {
    transform: scale(1.03);
}

.architecture-caption {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 40px;
    background: linear-gradient(transparent, rgba(0,0,0,0.75));
    color: #ffffff;
}

.architecture-caption span {
    font-size: 0.8rem;
    letter-spacing: 0.2em;
    opacity: 0.8;
}

.architecture-caption h3 {
    font-family: var(--font-serif);
    font-size: 1.8rem;
    margin-top: 6px;
}

/* ==========================================
   5. 在地美食 Food Section
   ========================================== */
.food-heading {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    margin-bottom: 70px;
    align-items: flex-end;
}

.food-heading p {
    color: var(--text-muted);
    font-size: 1.1rem;
}

.food-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 40px;
}

.food-card {
    background: var(--bg-card);
    border-radius: 8px;
    overflow: hidden;
    border: 1px solid var(--border-color);
    transition: var(--transition);
}

.food-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 40px rgba(0,0,0,0.06);
}

.food-card-down {
    margin-top: 40px;
}

.food-photo {
    position: relative;
    height: 260px;
}

.food-photo img {
    width: 100%;
    height: 100%;
}

.food-photo span {
    position: absolute;
    top: 15px;
    right: 15px;
    background: var(--bg-card);
    width: 36px;
    height: 36px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.85rem;
    font-weight: 700;
    color: var(--primary-color);
}

.food-info {
    padding: 30px;
}

.food-info p:first-child {
    font-size: 0.75rem;
    font-weight: 700;
    letter-spacing: 0.2em;
    color: var(--primary-color);
    margin-bottom: 8px;
}

.food-info h3 {
    font-family: var(--font-serif);
    font-size: 1.4rem;
    margin-bottom: 12px;
}

.food-info p:last-child {
    color: var(--text-muted);
    font-size: 0.95rem;
}

/* ==========================================
   6. 日常風景 Daily Section
   ========================================== */
.daily {
    display: grid;
    grid-template-columns: 1.1fr 1fr;
    gap: 80px;
    align-items: center;
    background-color: #f2ede4;
    border-radius: 12px;
    padding: 80px 8%;
}

.daily-image img {
    border-radius: 8px;
    height: 450px;
    width: 100%;
    box-shadow: 0 15px 35px rgba(0,0,0,0.08);
}

.daily-content p {
    color: var(--text-muted);
    margin-bottom: 18px;
    font-size: 1.05rem;
}

.daily-note {
    display: inline-block;
    margin-top: 24px;
    font-size: 0.8rem;
    font-weight: 700;
    letter-spacing: 0.25em;
    color: var(--primary-color);
}

/* ==========================================
   7. 結尾 Call to Action (Visit)
   ========================================== */
.visit {
    text-align: center;
    padding: 140px 8%;
    background-color: var(--bg-main);
    border-top: 1px solid var(--border-color);
}

.visit h2 {
    font-size: 3.2rem;
    margin: 20px 0;
}

.visit p:nth-child(3) {
    color: var(--text-muted);
    font-size: 1.2rem;
    margin-bottom: 40px;
}

.visit a {
    display: inline-block;
    padding: 18px 48px;
    background-color: var(--text-main);
    color: var(--bg-main);
    font-size: 1.05rem;
    font-weight: 500;
    border-radius: 50px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.15);
}

.visit a:hover {
    background-color: var(--primary-color);
    transform: translateY(-4px);
    box-shadow: 0 15px 30px rgba(140, 45, 25, 0.3);
}

/* ==========================================
   8. 頁尾 Footer
   ========================================== */
footer {
    background-color: var(--bg-dark);
    color: #a0a0a0;
    padding: 60px 8%;
    text-align: center;
}

.footer-logo {
    font-family: var(--font-serif);
    font-size: 1.8rem;
    font-weight: 900;
    color: #ffffff;
    margin-bottom: 10px;
}

.footer-logo span {
    color: var(--primary-color);
}

footer p {
    font-size: 0.85rem;
    letter-spacing: 0.15em;
    margin-bottom: 6px;
}

.copyright {
    margin-top: 30px;
    font-size: 0.75rem;
    color: #666666;
}

/* ==========================================
   RWD 響應式適應 (RWD)
   ========================================== */
@media (max-width: 1024px) {
    .hero {
        grid-template-columns: 1fr;
        padding-top: 120px;
        text-align: center;
    }

    .hero-side-text {
        display: none;
    }

    .hero-image {
        height: 400px;
    }

    .image-label {
        left: 50%;
        transform: translateX(-50%);
        bottom: -20px;
        width: 80%;
    }

    .about-content,
    .architecture-top,
    .food-heading,
    .daily {
        grid-template-columns: 1fr;
        gap: 40px;
    }

    .food-grid {
        grid-template-columns: 1fr;
    }

    .food-card-down {
        margin-top: 0;
    }
}

@media (max-width: 768px) {
    .navbar nav {
        display: none;
    }

    .hero h1 {
        font-size: 2.8rem;
    }

    .visit h2 {
        font-size: 2.2rem;
    }
}
    </style>
</head>

<body>

    <!-- 導覽列 -->
    <header class="navbar">
        <a href="#" class="logo">巷口時光<span>.</span></a>

        <nav>
            <a href="#about">市場故事</a>
            <a href="#architecture">歷史建築</a>
            <a href="#food">在地美食</a>
            <a href="#life">日常風景</a>
        </nav>

        <a href="#visit" class="nav-button">探索市場 ↗</a>
    </header>


    <!-- 首頁主視覺 -->
    <section class="hero">

        <div class="hero-content">
            <p class="small-title">TAICHUNG SECOND MARKET · EST. 1917</p>

            <h1>
                在城市的日常裡，<br>
                遇見<span>老時光。</span>
            </h1>

            <p class="hero-description">
                有些地方，不需要刻意尋找。<br>
                走進臺中第二市場，感受老市場裡的生活溫度。
            </p>

            <a href="#about" class="main-button">開始探索　↓</a>
        </div>

        <div class="hero-image">
            <img src="images/market-main.jpg" alt="臺中第二市場">
            <div class="image-label">
                <span>01 / 04</span>
                <p>藏在城市裡的日常風景</p>
            </div>
        </div>

        <div class="hero-side-text">A LITTLE JOURNEY THROUGH TIME</div>

    </section>


    <!-- 市場介紹 -->
    <section class="about section" id="about">

        <div class="section-heading">
            <p class="eyebrow">01 — THE STORY</p>
            <h2>一座市場，<br>收藏一座城市的故事。</h2>
        </div>

        <div class="about-content">
            <div class="about-image">
                <img src="images/market-history.jpg" alt="第二市場歷史街景">
                <span class="photo-number">FIG. 01</span>
            </div>

            <div class="about-text">
                <p class="text-tag">ABOUT SECOND MARKET</p>
                <h3>從過去走到現在，<br>生活始終在這裡發生。</h3>

                <p>
                    臺中第二市場位於臺中市中區，是一座承載城市歷史與生活記憶的老市場。
                    從早期的商業聚集，到今日融合美食、文化與觀光的特色場域，
                    這裡不只是購買食材的地方，更記錄著臺中人的日常。
                </p>

                <p>
                    穿梭在市場巷弄之間，可以看見老店的堅持、熟悉的人情味，
                    也能發現傳統市場與現代生活交織出的新風景。
                </p>

                <a href="#architecture" class="text-link">繼續認識第二市場　↗</a>
            </div>
        </div>

    </section>


    <!-- 六角樓 -->
    <section class="architecture section" id="architecture">

        <div class="architecture-top">
            <div>
                <p class="eyebrow">02 — ARCHITECTURE</p>
                <h2>不只是建築，<br>也是市場的記憶。</h2>
            </div>

            <p class="architecture-intro">
                走進第二市場，抬頭看看這座充滿特色的建築。
                六角樓的空間設計，讓市場形成獨特的放射狀格局，
                成為第二市場最具代表性的風景之一。
            </p>
        </div>

        <div class="architecture-image">
            <img src="images/market-hexagon.jpg" alt="第二市場六角樓">
            <div class="architecture-caption">
                <span>THE HEXAGONAL BUILDING</span>
                <h3>六角樓・市場的中心</h3>
            </div>
        </div>

    </section>


    <!-- 美食 -->
    <section class="food section" id="food">

        <div class="food-heading">
            <div>
                <p class="eyebrow">03 — LOCAL TASTE</p>
                <h2>老市場裡的，<br>在地好味道。</h2>
            </div>

            <p>
                從熟悉的傳統小吃，到飄香多年的老店，
                每一道料理都藏著屬於臺中的味道。
            </p>
        </div>

        <div class="food-grid">

            <article class="food-card">
                <div class="food-photo">
                    <img src="images/food-01.jpg" alt="市場在地美食">
                    <span>01</span>
                </div>
                <div class="food-info">
                    <p>LOCAL FOOD</p>
                    <h3>傳承多年的老味道</h3>
                    <p>熟悉的香氣，是市場最迷人的日常。</p>
                </div>
            </article>

            <article class="food-card food-card-down">
                <div class="food-photo">
                    <img src="images/food-02.jpg" alt="市場特色小吃">
                    <span>02</span>
                </div>
                <div class="food-info">
                    <p>LOCAL FLAVOR</p>
                    <h3>巷弄裡的美食風景</h3>
                    <p>每個轉角，都可能遇見意想不到的美味。</p>
                </div>
            </article>

            <article class="food-card">
                <div class="food-photo">
                    <img src="images/food-03.jpg" alt="市場特色料理">
                    <span>03</span>
                </div>
                <div class="food-info">
                    <p>OLD & NEW</p>
                    <h3>傳統與新意的交會</h3>
                    <p>老市場裡，也有屬於現在的生活風格。</p>
                </div>
            </article>

        </div>

    </section>


    <!-- 日常風景 -->
    <section class="daily section" id="life">

        <div class="daily-image">
            <img src="images/market-daily.jpg" alt="第二市場日常生活">
        </div>

        <div class="daily-content">
            <p class="eyebrow">04 — DAILY MOMENTS</p>
            <h2>市場的魅力，<br>藏在每個平凡瞬間。</h2>

            <p>
                老闆招呼客人的聲音、攤位飄出的香氣、
                人們來來去去的身影，構成了第二市場最真實的樣子。
            </p>

            <p>
                這裡的故事不只存在於歷史裡，
                而是每天都在發生。
            </p>

            <span class="daily-note">THE BEAUTY OF EVERYDAY LIFE.</span>
        </div>

    </section>


    <!-- 結尾 -->
    <section class="visit" id="visit">
        <p class="eyebrow">A PLACE WORTH DISCOVERING</p>
        <h2>下一次，換你走進<br>第二市場的故事。</h2>
        <p>在臺中的城市角落，重新認識那些熟悉又陌生的風景。</p>
        <a href="https://www.google.com/maps/search/?api=1&query=台中第二市場" target="_blank">
            前往第二市場　↗
        </a>
    </section>


    <!-- 頁尾 -->
    <footer>
        <div class="footer-logo">巷口時光<span>.</span></div>
        <p>TAICHUNG SECOND MARKET</p>
        <p class="copyright">© 2026 SECOND MARKET JOURNEY. ALL RIGHTS RESERVED.</p>
    </footer>

</body>
</html>
