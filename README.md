<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Explore Hokkaido</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      padding: 0;
      overflow: hidden;
    }

    /* スプレー背景 */
    .spray-background {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(135deg, #ff5733, #ffbb33, #33ccff, #ff3399);
      background-size: 200% 200%;
      animation: spray 8s infinite;
      filter: blur(30px);
    }
    
    @keyframes spray {
      0% { background-position: 100% 0%; }
      50% { background-position: 0% 100%; }
      100% { background-position: 100% 0%; }
    }

    header {
      background-color: rgba(255, 87, 51, 0.8);
      color: white;
      text-align: center;
      padding: 3rem 0;
      font-size: 2.5rem;
      font-weight: 600;
    }

    select {
      padding: 0.8rem 1rem;
      font-size: 1rem;
      margin-top: 1rem;
      background-color: #fff;
      border-radius: 5px;
      border: 2px solid #ccc;
    }

    .container {
      width: 90%;
      max-width: 1200px;
      margin: 2rem auto;
    }

    .city-section {
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      overflow: hidden;
      margin-bottom: 2rem;
      transition: transform 0.3s ease-in-out;
    }

    .city-section:hover {
      transform: translateY(-10px);
    }

    .city-header {
      background-color: #ffbb33;
      color: white;
      padding: 1.5rem;
      text-align: center;
      font-size: 2rem;
      font-weight: 600;
    }

    .spot {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      justify-content: center;
      padding: 2rem;
    }

    .spot-card {
      background-color: #f9f9f9;
      width: 250px;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s;
    }

    .spot-card:hover {
      transform: scale(1.05);
    }

    .spot-card img {
      width: 100%;
      height: 160px;
      object-fit: cover;
      border-radius: 8px 8px 0 0;
    }

    .spot-card-content {
      padding: 1rem;
    }

    .spot-card-content h3 {
      font-size: 1.5rem;
      color: #ff5733;
      margin: 0.5rem 0;
    }

    .spot-card-content p {
      font-size: 1rem;
      color: #555;
    }

    .spot-card iframe {
      width: 100%;
      height: 250px;
      border: none;
      border-radius: 8px;
      margin-top: 1rem;
    }

    footer {
      background-color: #ff5733;
      color: white;
      text-align: center;
      padding: 1.5rem;
      font-size: 1.2rem;
    }

    footer p {
      margin: 0;
    }
  </style>
</head>
<body>
  <!-- スプレー背景 -->
  <div class="spray-background"></div>

  <header>
    <h1>Explore Hokkaido</h1>
    <select id="language-selector">
      <option value="en">English</option>
      <option value="ja">日本語</option>
      <option value="zh">中文</option>
      <option value="fr">Français</option>
      <option value="ru">Русский</option>
    </select>
  </header>

  <div class="container">
    <!-- 札幌 -->
    <section class="city-section">
      <div class="city-header">
        <h2>Sapporo</h2>
      </div>
      <div class="spot">
        <div class="spot-card">
          <img src="https://upload.wikimedia.org/wikipedia/commons/e/ec/Sapporo_Tower_Night_View.jpg" alt="Sapporo TV Tower">
          <div class="spot-card-content">
            <h3>Sapporo TV Tower</h3>
            <p>A symbol of Sapporo, offering great city views.</p>
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3240.648690870986!2d141.35011861151616!3d43.06208717903602!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x5f6c36a604ffbce1%3A0x957dc835d19a7f9a!2sSapporo%20TV%20Tower!5e0!3m2!1sen!2sjp!4v1700000000000!5m2!1sen!2sjp"></iframe>
          </div>
        </div>
        <div class="spot-card">
          <img src="https://upload.wikimedia.org/wikipedia/commons/d/d7/Sapporo_Odori_Park_snow.jpg" alt="Odori Park">
          <div class="spot-card-content">
            <h3>Odori Park</h3>
            <p>A beautiful park in the center of Sapporo, famous for its seasonal flowers.</p>
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3240.6233633942955!2d141.35235171151624!3d43.06336588163477!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x5f6c36e9821fcf0b%3A0xb73962e80119e0b8!2sOdori%20Park!5e0!3m2!1sen!2sjp!4v1700000000000!5m2!1sen!2sjp"></iframe>
          </div>
        </div>
        <!-- 他の札幌観光地も同様に追加 -->
      </div>
    </section>

    <!-- 小樽 -->
    <section class="city-section">
      <div class="city-header">
        <h2>Otaru</h2>
      </div>
      <div class="spot">
        <div class="spot-card">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/39/Otaru_Canal_at_Night.jpg/800px-Otaru_Canal_at_Night.jpg" alt="Otaru Canal">
          <div class="spot-card-content">
            <h3>Otaru Canal</h3>
            <p>A scenic canal in Otaru, known for its historical stone warehouses and picturesque views.</p>
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3240.852879735252!2d135.26479971151667!3d43.19603527496085!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x5f0d5e731c71d54d%3A0x354a93d6cbd88ab5!2sOtaru%20Canal!5e0!3m2!1sja!2sjp!4v1700000000000!5m2!1sja!2sjp"></iframe>
          </div>
        </div>
        <!-- 他の小樽観光地も同様に追加 -->
      </div>
    </section>

    <!-- 函館 -->
    <section class="city-section">
      <div class="city-header">
        <h2>Hakodate</h2>
      </div>
      <div class="spot">
        <div class="spot-card">
          <img src="https://upload.wikimedia.org/wikipedia/commons/e/e4/Hakodate_Mountain_View.jpg" alt="Hakodate View">
          <div class="spot-card-content">
            <h3>Hakodate Mountain</h3>
            <p>Famous for its breathtaking night views of the city and the bay.</p>
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3240.2639631355995!2d140.74986501154666!3d41.77323305548739!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x5f29007cb0396d6f%3A0xe8e83e98b2f1d1d2!2sMount%20Hakodate!5e0!3m2!1sen!2sjp!4v1700000000000!5m2!1sen!2sjp"></iframe>
          </div>
        </div>
        <!-- 他の函館観光地も同様に追加 -->
      </div>
    </section>

    <!-- 釧路 -->
    <section class="city-section">
      <div class="city-header">
        <h2>Kushiro</h2>
      </div>
      <div class="spot">
        <div class="spot-card">
          <img src="https://upload.wikimedia.org/wikipedia/commons/a/a4/Kushiro_Swamp.jpg" alt="Kushiro Wetland">
          <div class="spot-card-content">
            <h3>Kushiro Wetland</h3>
            <p>The largest wetland in Japan, home to diverse wildlife and beautiful nature.</p>
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3240.300682124817!2d144.3314627115463!3d43.01855013557752!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x5f6c5d767b6fd3cf%3A0x6ec1f9c5440ed01e!2sKushiro%20Swamp!5e0!3m2!1sen!2sjp!4v1700000000000!5m2!1sen!2sjp"></iframe>
          </div>
        </div>
        <!-- 他の釧路観光地も同様に追加 -->
      </div>
    </section>

    <!-- ニセコ -->
    <section class="city-section">
      <div class="city-header">
        <h2>Niseko</h2>
      </div>
      <div class="spot">
        <div class="spot-card">
          <img src="https://upload.wikimedia.org/wikipedia/commons/e/e6/Niseko.jpg" alt="Niseko Ski">
          <div class="spot-card-content">
            <h3>Niseko Ski Resort</h3>
            <p>World-famous for its powder snow and excellent skiing conditions.</p>
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3240.694832689899!2d140.6782620115481!3d42.96102347859793!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x5f6c5a9b0629291d%3A0x82a70dfbfa02e015!2sNiseko%20Resort!5e0!3m2!1sen!2sjp!4v1700000000000!5m2!1sen!2sjp"></iframe>
          </div>
        </div>
        <!-- 他のニセコ観光地も同様に追加 -->
      </div>
    </section>
  </div>

  <footer>
    <p>&copy; 2025 Explore Hokkaido</p>
  </footer>
</body>
</html>
