<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Hokkaido Travel Guide</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1 data-i18n="title">Hokkaido Travel Guide</h1>
    <select id="languageSelector">
      <option value="en">English</option>
      <option value="ja">日本語</option>
      <option value="zh">中文</option>
      <option value="fr">Français</option>
      <option value="ru">Русский</option>
    </select>
  </header>

  <main id="content"></main>

  <footer>
    <p>&copy; 2025 Hokkaido Travel</p>
  </footer>

  <script src="lang.js"></script>
  <script src="data.js"></script>
  <script src="main.js"></script>
</body>
</html>
body {
  font-family: 'Arial', sans-serif;
  margin: 0;
  padding: 0;
  background: linear-gradient(135deg, #ffecb3, #b3e5fc);
  min-height: 100vh;
  overflow-x: hidden;
  color: #333;
}

header {
  background: rgba(255, 255, 255, 0.8);
  text-align: center;
  padding: 1.5rem;
  box-shadow: 0 0 10px rgba(0,0,0,0.2);
}

h1 {
  font-size: 2rem;
  margin: 0;
}

#languageSelector {
  margin-top: 1rem;
  padding: 0.5rem;
  font-size: 1rem;
}

main {
  padding: 2rem;
}

.city {
  margin-bottom: 3rem;
  animation: fadeIn 1s ease-in-out;
}

.city h2 {
  color: #f06292;
}

.spot {
  margin-top: 1rem;
  padding: 1rem;
  border-left: 5px solid #29b6f6;
  background: #ffffffcc;
  backdrop-filter: blur(10px);
  margin-bottom: 1rem;
  animation: slideUp 0.8s ease;
}

iframe {
  width: 100%;
  height: 300px;
  border: none;
  margin-top: 0.5rem;
}

footer {
  background: rgba(255,255,255,0.8);
  padding: 1rem;
  text-align: center;
  font-size: 0.9rem;
  position: relative;
  bottom: 0;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-20px); }
  to   { opacity: 1; transform: translateY(0); }
}

@keyframes slideUp {
  from { opacity: 0; transform: translateY(30px); }
  to   { opacity: 1; transform: translateY(0); }
}
const translations = {
  en: {
    title: "Hokkaido Travel Guide",
    cities: {
      sapporo: "Sapporo",
      otaru: "Otaru",
      hakodate: "Hakodate",
      kushiro: "Kushiro",
      niseko: "Niseko"
    }
  },
  ja: {
    title: "北海道観光ガイド",
    cities: {
      sapporo: "札幌",
      otaru: "小樽",
      hakodate: "函館",
      kushiro: "釧路",
      niseko: "ニセコ"
    }
  },
  zh: {
    title: "北海道旅游指南",
    cities: {
      sapporo: "札幌",
      otaru: "小樽",
      hakodate: "函馆",
      kushiro: "钏路",
      niseko: "二世古"
    }
  },
  fr: {
    title: "Guide touristique de Hokkaido",
    cities: {
      sapporo: "Sapporo",
      otaru: "Otaru",
      hakodate: "Hakodate",
      kushiro: "Kushiro",
      niseko: "Niseko"
    }
  },
  ru: {
    title: "Путеводитель по Хоккайдо",
    cities: {
      sapporo: "Саппоро",
      otaru: "Отару",
      hakodate: "Хакодате",
      kushiro: "Кусиро",
      niseko: "Нисеко"
    }
  }
};
const spots = {
  sapporo: [
    { name: "Sapporo TV Tower", description: "Iconic TV tower with city views", map: "https://..." },
    { name: "Odori Park", description: "Scenic park in city center", map: "https://..." },
    { name: "Shiroi Koibito Park", description: "Chocolate theme park", map: "https://..." },
    { name: "Mount Moiwa", description: "Great city view", map: "https://..." },
    { name: "Historic Village", description: "Reconstruction of historic buildings", map: "https://..." }
  ],
  otaru: [
    { name: "Otaru Canal", description: "Romantic canal walk", map: "https://..." },
    { name: "Music Box Museum", description: "Old-world charm and music", map: "https://..." },
    { name: "Otaru Aquarium", description: "Aquatic wildlife", map: "https://..." },
    { name: "Sakaimachi Street", description: "Shopping and snacks", map: "https://..." },
    { name: "Mount Tengu", description: "Night view spot", map: "https://..." }
  ],
  // 同様に hakodate, kushiro, niseko を追加（省略）
};
function renderContent(language) {
  const cityNames = translations[language].cities;
  document.querySelector('[data-i18n="title"]').textContent = translations[language].title;

  const container = document.getElementById("content");
  container.innerHTML = "";

  for (const [city, places] of Object.entries(spots)) {
    const section = document.createElement("section");
    section.className = "city";
    section.innerHTML = `<h2>${cityNames[city]}</h2>`;
    places.forEach(spot => {
      section.innerHTML += `
        <div class="spot">
          <h3>${spot.name}</h3>
          <p>${spot.description}</p>
          <iframe src="${spot.map}" loading="lazy"></iframe>
        </div>
      `;
    });
    container.appendChild(section);
  }
}

document.getElementById("languageSelector").addEventListener("change", e => {
  renderContent(e.target.value);
});

window.addEventListener("DOMContentLoaded", () => {
  renderContent("en"); // default language
});
