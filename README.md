<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Explore Hokkaido</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, rgba(255, 200, 0, 0.3), rgba(0, 200, 255, 0.3));
      color: #333;
    }

    header {
      background-color: #ff6f61;
      color: white;
      padding: 1.5rem;
      text-align: center;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

    h1 {
      margin: 0;
      font-size: 2.5rem;
    }

    main {
      padding: 2rem;
      max-width: 1200px;
      margin: auto;
    }

    .city-section {
      margin-bottom: 3rem;
    }

    .city-header {
      font-size: 2rem;
      margin-bottom: 1.5rem;
      border-left: 8px solid #ff6f61;
      padding-left: 0.5rem;
    }

    .spot {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
    }

    .spot-card {
      background-color: #fff;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
      width: calc(50% - 1rem);
      min-width: 300px;
      position: relative;
      z-index: 10;
    }

    .spot-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }

    .spot-card-content {
      padding: 1rem;
    }

    .spot-card-content h3 {
      margin: 0.5rem 0;
      color: #ff6f61;
    }

    .spot-card-content p {
      font-size: 0.95rem;
      margin-bottom: 0.5rem;
    }

    .spot-card iframe {
      width: 100%;
      height: 200px;
      border: 0;
    }

    footer {
      background-color: #f1f1f1;
      text-align: center;
      padding: 1rem;
      font-size: 0.9rem;
    }

    @media (max-width: 768px) {
      .spot-card {
        width: 100%;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Explore Hokkaido</h1>
    <p>北海道の人気観光スポットを世界へ</p>
  </header>

  <main>
    <!-- 札幌 -->
    <section class="city-section">
      <div class="city-header">札幌 / Sapporo</div>
      <div class="spot">
        <div class="spot-card">
          <img src="https://upload.wikimedia.org/wikipedia/commons/e/e7/Sapporo_TV_Tower_2015.jpg" alt="Sapporo TV Tower" />
          <div class="spot-card-content">
            <h3>Sapporo TV Tower</h3>
            <p>大通公園の東端にあるランドマーク。夜景も人気。</p>
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2913.421061601231!2d141.35444947635593!3d43.06121497113637!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x5f0b29955df29a71%3A0xc20df0ac44c55a69!2zU2FwcG9ybyBUViBUb3dlcg!5e0!3m2!1sen!2sjp!4v1700000000000" allowfullscreen loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
          </div>
        </div>

        <!-- 他の札幌スポットもここに追加可能（Odori Park, Moerenuma Park など） -->
      </div>
    </section>

    <!-- 小樽 -->
    <section class="city-section">
      <div class="city-header">小樽 / Otaru</div>
      <div class="spot">
        <div class="spot-card">
          <img src="https://upload.wikimedia.org/wikipedia/commons/8/8e/Otaru_Canal.jpg" alt="Otaru Canal" />
          <div class="spot-card-content">
            <h3>Otaru Canal</h3>
            <p>ロマンチックな雰囲気漂う石造倉庫群と運河の景観。</p>
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2906.3903687685463!2d141.0009974!3d43.199218!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x5f0b1c6bfff105f3%3A0x4ecdb1ac6746bc09!2zT3RhcnUgQ2FuYWw!5e0!3m2!1sen!2sjp!4v1700000000000" allowfullscreen loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
          </div>
        </div>
        <!-- 他の小樽スポットもここに追加 -->
      </div>
    </section>

    <!-- 他都市（函館、釧路、ニセコ）も同じ構造で追加可能 -->
  </main>

  <footer>
    <p>&copy; 2025 Explore Hokkaido | 多言語対応・Responsive Layout</p>
  </footer>
</body>
</html>
