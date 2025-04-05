
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>AnimeFlix</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #141414;
      color: white;
    }
    header {
      background: #000;
      padding: 20px;
      text-align: center;
      font-size: 24px;
      font-weight: bold;
      color: #e50914;
    }
    .catalogo {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
      padding: 20px;
    }
    .anime-card {
      background: #1f1f1f;
      width: 200px;
      border-radius: 10px;
      padding: 10px;
    }
    .anime-card img {
      width: 100%;
      border-radius: 10px;
    }
    .anime-card h3 {
      font-size: 16px;
      margin: 10px 0 5px;
    }
    .anime-card p {
      color: #bbb;
      font-size: 14px;
      margin: 0 0 10px;
    }
    .anime-card a {
      background: #e50914;
      color: white;
      padding: 5px 10px;
      text-decoration: none;
      border-radius: 5px;
      display: inline-block;
    }
  </style>
</head>
<body>

<header>AnimeFlix</header>

<div class="catalogo" id="catalogo">
  <!-- Animes vão aparecer aqui -->
</div>

<script>
  const animes = [
    {
      titulo: "Konosuba",
      imagem: "https://upload.wikimedia.org/wikipedia/en/2/2d/KonoSuba_light_novel_vol_1_cover.jpg",
      genero: "Comédia, Fantasia",
      ano: "2016",
      link: "https://www.example.com/konosuba"
    },
    {
      titulo: "Kanojo, Okarishimasu",
      imagem: "https://upload.wikimedia.org/wikipedia/en/5/5b/Rent-A-Girlfriend_volume_1_cover.jpg",
      genero: "Romance, Comédia",
      ano: "2020",
      link: "https://www.example.com/kanojo"
    },
    {
      titulo: "Blue Box",
      imagem: "https://upload.wikimedia.org/wikipedia/en/2/22/Blue_Box_manga_volume_1_cover.jpg",
      genero: "Esporte, Romance",
      ano: "2021",
      link: "https://www.example.com/bluebox"
    },
    {
      titulo: "Hunter × Hunter",
      imagem: "https://upload.wikimedia.org/wikipedia/en/9/9b/Hunter_Hunter_cover.gif",
      genero: "Ação, Aventura",
      ano: "1999",
      link: "https://www.example.com/hunterxhunter"
    }
  ];

  let html = "";
  animes.forEach(a => {
    html += `
      <div class="anime-card">
        <img src="${a.imagem}" alt="${a.titulo}">
        <h3>${a.titulo}</h3>
        <p>${a.genero} - ${a.ano}</p>
        <a href="${a.link}" target="_blank">Assistir</a>
      </div>
    `;
  });
  document.getElementById("catalogo").innerHTML = html;
</script>

</body>
</html>
