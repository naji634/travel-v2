<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Hokkaido Travel Guide</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      color: #333;
      background: linear-gradient(135deg, #ffc371, #47c9e5);
      background-size: 200% 200%;
      animation: bgMove 10s infinite alternate;
    }

    @keyframes bgMove {
      from { background-position: 0% 50%; }
      to { background-position: 100% 50%; }
    }

    header {
      background-color: rgba(255, 255, 255, 0.8);
      padding: 1.5rem;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 10;
      backdrop-filter: blur(10px);
    }

    header h1 {
      margin: 0;
      font-size: 2rem;
    }

    .lang-switcher {
      margin-top: 0.5rem;
    }

    main {
      padding: 2rem;
    }

    .city {
      margin-bottom: 3rem;
    }

    .city h2 {
      color: #e74c3c;
    }

    .place {
      background-color: rgba(255, 255, 255, 0.85);
      padding: 1rem;
      border-radius: 10px;
      margin: 1rem 0;
      transition: transform 0.3s;
    }

    .place:hover {
      transform: scale(1.03);
    }

    iframe {
      width: 100%;
      height: 300px;
      border: none;
      margin-top: 0.5rem;
    }

    footer {
      text-align: center;
      padding: 1rem;
      background: rgba(255, 255, 255, 0.7);
      position: sticky;
      bottom: 0;
      backdrop-filter: blur(5px);
    }
  </style>
</head>
<body>
  <header>
    <h1 id="title">Hokkaido Travel Guide</h1>
    <div class="lang-switcher">
      <select id="langSelect">
        <option value="en">🇬🇧 English</option>
        <option value="ja">🇯🇵 日本語</option>
        <option value="zh">🇨🇳 中文</option>
        <option value="fr">🇫🇷 Français</option>
        <option value="ru">🇷🇺 Русский</option>
      </select>
    </div>
  </header>

  <main id="content"></main>

  <footer>
    <p>© 2025 Hokkaido Travel</p>
  </footer>

  <script>
    const langData = {
      title: {
        en: "Hokkaido Travel Guide",
        ja: "北海道観光ガイド",
        zh: "北海道旅游指南",
        fr: "Guide touristique de Hokkaido",
        ru: "Путеводитель по Хоккайдо"
      },
      cities: {
        "Sapporo": { ja: "札幌", zh: "札幌", fr: "Sapporo", ru: "Саппоро" },
        "Otaru": { ja: "小樽", zh: "小樽", fr: "Otaru", ru: "Отару" },
        "Hakodate": { ja: "函館", zh: "函馆", fr: "Hakodate", ru: "Хакодате" },
        "Kushiro": { ja: "釧路", zh: "钏路", fr: "Kushiro", ru: "Кусиро" },
        "Niseko": { ja: "ニセコ", zh: "二世古", fr: "Niseko", ru: "Нисеко" }
      }
    };

    const data = {
      Sapporo: [
        {
          name: "Sapporo TV Tower",
          desc: "An iconic symbol in Sapporo overlooking Odori Park.",
          map: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2914.8707824211144!2d141.35300491548312!3d43.06193637914645!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x5f0b297c9c1bb5b3%3A0x8a1dfaa9f99396c0!2sSapporo%20TV%20Tower!5e0!3m2!1sen!2sjp!4v1680920476182"
        },
        {
          name: "Odori Park",
          desc: "A long park in central Sapporo with events year-round.",
          map: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2914.8990010674823!2d141.34980611548312!3d43.06146497914692!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x5f0b297c347a6bd7%3A0xdea2138139f74ebf!2sOdori%20Park!5e0!3m2!1sen!2sjp!4v1680920600180"
        }
      ],
      Otaru: [
        {
          name: "Otaru Canal",
          desc: "Romantic walkway with gas lamps and old warehouses.",
          map: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2917.008676437959!2d141.00049341548262!3d43.19759597914107"
        }
      ],
      Hakodate: [
        {
          name: "Mount Hakodate",
          desc: "Scenic night view from the mountaintop.",
          map: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2913.739027372563!2d140.7268903154835!3d41.76083487923044"
        }
      ],
      Kushiro: [
        {
          name: "Kushiro Marsh",
          desc: "Japan's largest marshland with rich wildlife.",
          map: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2885.345654820006!2d144.3793432154936!3d43.11282797914303"
        }
      ],
      Niseko: [
        {
          name: "Niseko Village",
          desc: "A world-renowned ski and outdoor resort.",
          map: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2884.321919482021!2d140.708248615494!3d42.803168479240394"
        }
      ]
    };

    const render = (lang = 'en') => {
      document.getElementById("title").textContent = langData.title[lang];
      const content = document.getElementById("content");
      content.innerHTML = '';

      for (const [city, spots] of Object.entries(data)) {
        const cityDiv = document.createElement("div");
        cityDiv.className = "city";
        const cityName = langData.cities[city]?.[lang] || city;
        cityDiv.innerHTML = `<h2>${cityName}</h2>`;
        spots.forEach(spot => {
          cityDiv.innerHTML += `
            <div class="place">
              <h3>${spot.name}</h3>
              <p>${spot.desc}</p>
              <iframe src="${spot.map}" loading="lazy" allowfullscreen></iframe>
            </div>
          `;
        });
        content.appendChild(cityDiv);
      }
    };

    document.getElementById("langSelect").addEventListener("change", (e) => {
      render(e.target.value);
    });

    render(); // 初期表示
  </script>
</body>
</html>
