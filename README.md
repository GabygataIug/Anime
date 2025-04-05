
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>AnimeFlix</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      background-color: #0d0d0d;
      font-family: Arial, sans-serif;
      color: #fff;
    }
    header {
      background: #111;
      padding: 20px;
      text-align: center;
      font-size: 2rem;
      color: #f90;
    }
    .controls {
      display: flex;
      justify-content: center;
      gap: 10px;
      padding: 20px;
      flex-wrap: wrap;
    }
    input, select {
      padding: 10px;
      font-size: 1rem;
      border-radius: 5px;
      border: none;
      outline: none;
    }
    .catalogo {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
      gap: 20px;
      padding: 20px;
    }
    .anime {
      background-color: #1c1c1c;
      border-radius: 8px;
      overflow: hidden;
      transition: transform 0.2s;
    }
    .anime:hover {
      transform: scale(1.03);
    }
    .anime img {
      width: 100%;
      height: 300px;
      object-fit: cover;
    }
    .anime-info {
      padding: 10px;
    }
    .anime h3 {
      color: #f90;
      font-size: 1.1rem;
      margin-bottom: 5px;
    }
    .anime p {
      font-size: 0.9rem;
      color: #ccc;
      height: 60px;
      overflow: hidden;
    }
    .assistir-btn {
      display: block;
      margin: 10px auto;
      padding: 8px 15px;
      background-color: #f90;
      color: #000;
      text-align: center;
      border-radius: 5px;
      text-decoration: none;
    }
    .player {
      display: none;
      position: fixed;
      top: 5%;
      left: 5%;
      width: 90%;
      height: 90%;
      background: #000;
      z-index: 999;
      padding: 10px;
    }
    .player iframe {
      width: 100%;
      height: 100%;
    }
    .fechar {
      position: absolute;
      top: 10px;
      right: 20px;
      font-size: 2rem;
      color: #fff;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <header>AnimeFlix</header>

  <div class="controls">
    <input type="text" id="busca" placeholder="Buscar anime..." oninput="filtrar()">
    <select id="genero" onchange="filtrar()">
      <option value="">Todos os gêneros</option>
      <option value="Ação">Ação</option>
      <option value="Comédia">Comédia</option>
      <option value="Romance">Romance</option>
      <option value="Fantasia">Fantasia</option>
      <option value="Terror">Terror</option>
    </select>
  </div>

  <div class="catalogo" id="catalogo">
    <!-- Lista de animes será gerada aqui -->
  </div>

  <div class="player" id="playerBox">
    <span class="fechar" onclick="fecharPlayer()">×</span>
    <iframe id="playerFrame" src="" frameborder="0" allowfullscreen></iframe>
  </div>

  <script>
    const animes = [];
    const generos = ["Ação", "Comédia", "Romance", "Fantasia", "Terror"];
    for (let i = 1; i <= 50; i++) {
      animes.push({
        titulo: `Anime ${i}`,
        genero: generos[i % generos.length],
        descricao: `Sinopse do Anime ${i}: Uma aventura incrível cheia de emoção e batalhas épicas!`,
        imagem: `https://placehold.co/300x400?text=Anime+${i}`,
        link: "https://www.youtube.com/embed/dQw4w9WgXcQ"
      });
    }

    const catalogo = document.getElementById("catalogo");

    function renderizarLista(lista) {
      catalogo.innerHTML = "";
      lista.forEach(anime => {
        const div = document.createElement("div");
        div.className = "anime";
        div.innerHTML = `
          <img src="${anime.imagem}" alt="${anime.titulo}">
          <div class="anime-info">
            <h3>${anime.titulo}</h3>
            <p>${anime.descricao}</p>
            <a href="#" class="assistir-btn" onclick="abrirPlayer('${anime.link}')">Assistir</a>
          </div>
        `;
        catalogo.appendChild(div);
      });
    }

    function filtrar() {
      const termo = document.getElementById("busca").value.toLowerCase();
      const genero = document.getElementById("genero").value;
      const filtrado = animes.filter(anime => {
        return anime.titulo.toLowerCase().includes(termo) &&
               (genero === "" || anime.genero === genero);
      });
      renderizarLista(filtrado);
    }

    function abrirPlayer(link) {
      document.getElementById("playerFrame").src = link;
      document.getElementById("playerBox").style.display = "block";
    }

    function fecharPlayer() {
      document.getElementById("playerBox").style.display = "none";
      document.getElementById("playerFrame").src = "";
    }

    renderizarLista(animes);
  </script>
</body>
</html>
