<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html lang="pt-BR" dir="ltr" xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title><data:blog.pageTitle/></title>
  
  <!-- CSS Tema Escuro AnimeFlix -->
  <style type="text/css">
    :root {
      --primary: #E50914;
      --dark: #121212;
      --dark-secondary: #1E1E1E;
      --text: #FFFFFF;
      --text-secondary: #AAAAAA;
    }

    body {
      background: var(--dark);
      color: var(--text);
      font-family: 'Segoe UI', Arial, sans-serif;
      margin: 0;
      padding: 0;
    }

    /* Header */
    header {
      background: var(--dark-secondary);
      padding: 15px 5%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
    }

    .logo {
      font-size: 28px;
      font-weight: bold;
      color: var(--primary);
    }

    .menu a {
      color: var(--text);
      margin: 0 15px;
      text-decoration: none;
      font-weight: 500;
    }

    .search-bar input {
      padding: 8px 15px;
      border-radius: 20px;
      border: none;
      background: #333;
      color: white;
    }

    /* Destaque */
    .featured {
      background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://via.placeholder.com/1920x600');
      background-size: cover;
      height: 60vh;
      display: flex;
      align-items: center;
      padding: 0 5%;
    }

    .featured-info h1 {
      font-size: 3em;
      margin: 0;
    }

    .featured-info p {
      max-width: 600px;
      color: var(--text-secondary);
    }

    .btn {
      background: var(--primary);
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-weight: bold;
    }

    /* Catálogo */
    .catalog {
      padding: 30px 5%;
    }

    .section-title {
      font-size: 24px;
      margin-bottom: 20px;
      border-left: 5px solid var(--primary);
      padding-left: 10px;
    }

    .anime-list {
      display: flex;
      overflow-x: auto;
      gap: 20px;
      padding-bottom: 20px;
    }

    .anime-card {
      background: var(--dark-secondary);
      border-radius: 8px;
      min-width: 200px;
      transition: transform 0.3s;
    }

    .anime-card:hover {
      transform: scale(1.05);
    }

    .anime-card img {
      width: 100%;
      border-radius: 8px 8px 0 0;
    }

    .anime-info {
      padding: 10px;
    }

    .anime-info h3 {
      margin: 5px 0;
      font-size: 16px;
    }

    .anime-info p {
      color: var(--text-secondary);
      font-size: 14px;
      margin: 5px 0;
    }

    /* Footer */
    footer {
      background: var(--dark-secondary);
      padding: 20px 5%;
      text-align: center;
      margin-top: 40px;
    }

    .footer-links a {
      color: var(--text-secondary);
      margin: 0 10px;
      text-decoration: none;
    }

    /* Responsivo */
    @media (max-width: 768px) {
      .menu {
        display: none;
      }
      .featured-info h1 {
        font-size: 2em;
      }
    }
  </style>
</head>
<body>
  <!-- Header -->
  <header>
    <div class="logo">ANIMEFLIX</div>
    <nav class="menu">
      <a href="#">Início</a>
      <a href="#">Animes</a>
      <a href="#">Filmes</a>
      <a href="#">Lista</a>
    </nav>
    <div class="search-bar">
      <input type="text" placeholder="Buscar animes..." />
    </div>
  </header>

  <!-- Destaque -->
  <section class="featured">
    <div class="featured-info">
      <h1>Attack on Titan: Final Season</h1>
      <p>A batalha final pela humanidade chega ao fim. Assista agora ao clássico que definiu uma geração.</p>
      <button class="btn">Assistir Agora</button>
    </div>
  </section>

  <!-- Catálogo -->
  <section class="catalog">
    <h2 class="section-title">Lançamentos Recentes</h2>
    <div class="anime-list">
      <div class="anime-card">
        <img src="https://via.placeholder.com/200x300" alt="Demon Slayer" />
        <div class="anime-info">
          <h3>Demon Slayer</h3>
          <p>11 episódios</p>
        </div>
      </div>
      <div class="anime-card">
        <img src="https://via.placeholder.com/200x300" alt="Jujutsu Kaisen" />
        <div class="anime-info">
          <h3>Jujutsu Kaisen</h3>
          <p>24 episódios</p>
        </div>
      </div>
      <div class="anime-card">
        <img src="https://via.placeholder.com/200x300" alt="Chainsaw Man" />
        <div class="anime-info">
          <h3>Chainsaw Man</h3>
          <p>12 episódios</p>
        </div>
      </div>
      <div class="anime-card">
        <img src="https://via.placeholder.com/200x300" alt="Vinland Saga" />
        <div class="anime-info">
          <h3>Vinland Saga</h3>
          <p>24 episódios</p>
        </div>
      </div>
    </div>
  </section>

  <section class="catalog">
    <h2 class="section-title">Populares</h2>
    <div class="anime-list">
      <div class="anime-card">
        <img src="https://via.placeholder.com/200x300" alt="Naruto" />
        <div class="anime-info">
          <h3>Naruto Shippuden</h3>
          <p>500 episódios</p>
        </div>
      </div>
      <div class="anime-card">
        <img src="https://via.placeholder.com/200x300" alt="One Piece" />
        <div class="anime-info">
          <h3>One Piece</h3>
          <p>1000+ episódios</p>
        </div>
      </div>
      <div class="anime-card">
        <img src="https://via.placeholder.com/200x300" alt="Death Note" />
        <div class="anime-info">
          <h3>Death Note</h3>
          <p>37 episódios</p>
        </div>
      </div>
      <div class="anime-card">
        <img src="https://via.placeholder.com/200x300" alt="Tokyo Revengers" />
        <div class="anime-info">
          <h3>Tokyo Revengers</h3>
          <p>24 episódios</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="footer-links">
      <a href="#">Termos de Uso</a>
      <a href="#">Política de Privacidade</a>
      <a href="#">Contato</a>
    </div>
    <p>© 2023 AnimeFlix - Todos os direitos reservados.</p>
  </footer>
</body>
</html>
