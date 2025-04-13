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
      background-color: #f3f4f6;
      color: #333;
    }
    header {
      background-color: #ff5733;
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
    .lang-text {
      display: none;
    }
    .lang-active {
      display: block;
    }
  </style>
</head>
<body>
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
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3240.852879735252!2d135.26479971151667!3d43.19603527496085!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x5f0d5e731c71d54d%3A0x354a93d6cbd88ab5!2sOtaru%20Canal!5e0!3m2!1sja!2sjp!4v1713000000000!5m2!1sja!2sjp"></iframe>
          </div>
        </div>
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
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3240.2639631355995!2d140.74986501154666!3d41.77323305548739!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x5f6f9d0d3e1547a3%3A0xe4b84a1b0a987e10!2sHakodate%20Mountain!5e0!3m2!1sen!2sjp!4v1713000000000!5m2!1sen!2sjp"></iframe>
          </div>
        </div>
      </div>
    </section>

    <!-- 他の都市も追加 -->
  </div>

  <footer>
    <p>&copy; 2025 Explore Hokkaido</p>
  </footer>

  <script>
    document.getElementById('language-selector').addEventListener('change', function(event) {
      const lang = event.target.value;
      const langTexts = document.querySelectorAll('.lang-text');
      langTexts.forEach(text => {
        text.classList.remove('lang-active');
        if (text.dataset.lang === lang) {
          text.classList.add('lang-active');
        }
      });
    });
  </script>
</body>
</html>
