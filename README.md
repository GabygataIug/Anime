
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
      height: 280px;
      object-fit: cover;
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

<div class="catalogo" id="catalogo"></div>

<script>
  const animes = [
    {
      titulo: "Konosuba",
      imagem: "https://upload.wikimedia.org/wikipedia/en/4/4d/Konosuba_Anime_Season_1_Poster.jpg",
      genero: "Comédia, Fantasia",
      ano: "2016",
      link: "https://www.crunchyroll.com/pt-br/series/GYEXQKJG6/konosuba-gods-blessing-on-this-wonderful-world"
    },
    {
      titulo: "Kanojo, Okarishimasu",
      imagem: "https://upload.wikimedia.org/wikipedia/en/f/f4/Rent-A-Girlfriend_2020_Anime_Key_Visual.jpg",
      genero: "Romance, Comédia",
      ano: "2020",
      link: "https://www.crunchyroll.com/pt-br/series/GYUG7X1VY/rent-a-girlfriend"
    },
    {
      titulo: "Blue Box",
      imagem: "https://cdn.myanimelist.net/images/manga/3/259892.jpg",
      genero: "Esporte, Romance",
      ano: "2021",
      link: "https://www.viz.com/blue-box"
    },
    {
      titulo: "Hunter × Hunter",
      imagem: "https://upload.wikimedia.org/wikipedia/en/3/3f/Hunter_Hunter_2011_key_visual.png",
      genero: "Ação, Aventura",
      ano: "2011",
      link: "https://www.crunchyroll.com/pt-br/series/G6NQ5DWZ6/hunter-x-hunter"
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
