
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>AnimeFlix</title>
  <style>
    body {
      background-color: #121212;
      color: white;
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }
    .header {
      background-color: #1c1c1c;
      padding: 15px;
      text-align: center;
      font-size: 24px;
      color: orange;
    }
    .painel {
      background-color: #1e1e1e;
      padding: 20px;
      text-align: center;
    }
    .painel input, .painel button {
      padding: 10px;
      margin: 5px;
      width: 90%;
      max-width: 400px;
    }
    .anime-list {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      padding: 20px;
    }
    .anime-item {
      background-color: #222;
      border-radius: 8px;
      overflow: hidden;
      width: 300px;
      text-align: center;
      padding: 10px;
    }
    .anime-item img {
      width: 100%;
      border-radius: 5px;
    }
    video {
      width: 100%;
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <div class="header">AnimeFlix</div>

  <div class="painel">
    <h2>Adicionar Novo Anime</h2>
    <input type="text" id="anime-nome" placeholder="Nome do Anime" /><br>
    <input type="text" id="anime-imagem" placeholder="URL da Imagem" /><br>
    <input type="text" id="anime-video" placeholder="URL do Episódio MP4" /><br>
    <button onclick="adicionarAnime()">Adicionar</button>
  </div>

  <h2 style="text-align:center">Últimos Lançamentos</h2>
  <div class="anime-list" id="anime-list"></div>

  <script>
    async function carregarAnimes() {
      const response = await fetch('animes.json');
      const animes = await response.json();
      const lista = document.getElementById('anime-list');
      lista.innerHTML = '';
      animes.forEach(anime => {
        const item = document.createElement('div');
        item.className = 'anime-item';
        item.innerHTML = `
          <img src="${anime.imagem}" alt="${anime.nome}" />
          <h3>${anime.nome}</h3>
          <video controls>
            <source src="${anime.video}" type="video/mp4">
            Seu navegador não suporta vídeo.
          </video>
        `;
        lista.appendChild(item);
      });
    }

    async function adicionarAnime() {
      const nome = document.getElementById('anime-nome').value;
      const imagem = document.getElementById('anime-imagem').value;
      const video = document.getElementById('anime-video').value;

      const response = await fetch('animes.json');
      const animes = await response.json();
      animes.push({ nome, imagem, video });

      await fetch('salvar.php', {
        method: 'POST',
        headers: {'Content-Type': 'application/json'},
        body: JSON.stringify(animes)
      });

      carregarAnimes();
    }

    window.onload = carregarAnimes;
  </script>
</body>
</html>
