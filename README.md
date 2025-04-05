<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>AnimeFlix</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: #121212;
      color: white;
    }
    header {
      background: #000;
      padding: 20px;
      text-align: center;
      font-size: 2rem;
      font-weight: bold;
      color: #f97316;
      letter-spacing: 1px;
    }
    #search {
      display: block;
      margin: 20px auto;
      padding: 12px 15px;
      font-size: 16px;
      width: 90%;
      max-width: 500px;
      border: none;
      border-radius: 8px;
      background: #222;
      color: white;
    }
    #anime-list {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 16px;
      padding: 20px;
    }
    .anime-card {
      background: #1e1e1e;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 2px 10px rgba(0,0,0,0.6);
      transition: transform 0.2s;
    }
    .anime-card:hover {
      transform: scale(1.05);
    }
    .anime-card img {
      width: 100%;
      height: 280px;
      object-fit: cover;
    }
    .info {
      padding: 10px;
    }
    .info h3 {
      margin: 0 0 8px;
      font-size: 1.1rem;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }
    .episodes {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
    }
    .episodes button {
      flex: 1;
      background: #f97316;
      border: none;
      padding: 6px 10px;
      color: white;
      border-radius: 4px;
      cursor: pointer;
      font-size: 0.85rem;
    }
    .episodes button:hover {
      background: #fb923c;
    }
    @media (max-width: 600px) {
      .anime-card img {
        height: 200px;
      }
    }
  </style>
</head>
<body>

  <header>AnimeFlix</header>
  <input type="text" id="search" placeholder="Buscar anime..." oninput="filtrarAnimes()" />
  <section id="anime-list"></section>

  <script>
    const animes = [
      {
        nome: "Attack on Titan",
        imagem: "https://cdn.myanimelist.net/images/anime/10/47347.jpg",
        episodios: [
          "https://www.youtube.com/embed/MGRm4IzK1SQ",
          "https://www.youtube.com/embed/8OkpRK2_gVs"
        ]
      },
      {
        nome: "Demon Slayer",
        imagem: "https://cdn.myanimelist.net/images/anime/1286/99889.jpg",
        episodios: [
          "https://www.youtube.com/embed/VQGCKyvzIM4",
          "https://www.youtube.com/embed/OL8HyJekyCU"
        ]
      },
      {
        nome: "Jujutsu Kaisen",
        imagem: "https://cdn.myanimelist.net/images/anime/1171/109222.jpg",
        episodios: [
          "https://www.youtube.com/embed/aPz5FWWtLOI",
          "https://www.youtube.com/embed/kY7Z9NgnxJU"
        ]
      },
      {
        nome: "Naruto Shippuden",
        imagem: "https://cdn.myanimelist.net/images/anime/5/17407.jpg",
        episodios: [
          "https://www.youtube.com/embed/dnYweLzQdMM",
          "https://www.youtube.com/embed/NDjC8jJ8-hE"
        ]
      }
    ];

    const container = document.getElementById("anime-list");

    function renderizarAnimes(lista) {
      container.innerHTML = "";
      lista.forEach(anime => {
        const card = document.createElement("div");
        card.className = "anime-card";
        card.innerHTML = `
          <img src="${anime.imagem}" alt="${anime.nome}">
          <div class="info">
            <h3>${anime.nome}</h3>
            <div class="episodes">
              ${anime.episodios.map((ep, i) => `<button onclick="assistir('${ep}')">Ep ${i + 1}</button>`).join("")}
            </div>
          </div>
        `;
        container.appendChild(card);
      });
    }

    function assistir(link) {
      const player = window.open("", "_blank");
      player.document.write(`
        <html><head><title>Assistir</title></head>
        <body style="margin:0;background:#000;">
          <iframe width="100%" height="100%" src="${link}" frameborder="0" allowfullscreen></iframe>
        </body></html>
      `);
    }

    function filtrarAnimes() {
      const termo = document.getElementById("search").value.toLowerCase();
      const filtrados = animes.filter(anime => anime.nome.toLowerCase().includes(termo));
      renderizarAnimes(filtrados);
    }

    renderizarAnimes(animes);
  </script>

</body>
</html>

