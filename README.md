
<?xml version="1.0" encoding="UTF-8" ?>
<html xmlns='http://www.w3.org/1999/xhtml'>
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1"/>
  <meta name="description" content="AnimeFlix - O melhor streaming de animes do Brasil com centenas de títulos em diversos gêneros"/>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&amp;display=swap"/>
  <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons"/>
  <title>AnimeFlix - Seu Streaming de Anime</title>
  
  <style>
    <![CDATA[
    :root {
      --primary-color: #e50914;
      --primary-hover: #f40612;
      --bg-dark: #141414;
      --bg-darker: #0f0f0f;
      --text-light: #ffffff;
      --text-muted: rgba(255, 255, 255, 0.7);
      --success-color: #46d369;
    }
    
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    
    body {
      font-family: 'Roboto', sans-serif;
      background-color: var(--bg-dark);
      color: var(--text-light);
      line-height: 1.5;
    }
    
    /* Navbar */
    .navbar {
      background-color: rgba(20, 20, 20, 0.9);
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      z-index: 1000;
      padding: 0.75rem 2rem;
      transition: background-color 0.3s ease;
    }
    
    .navbar-content {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    
    .navbar-brand {
      font-size: 1.75rem;
      font-weight: 700;
      color: var(--primary-color);
      text-decoration: none;
    }
    
    .navbar-menu {
      display: flex;
      list-style: none;
    }
    
    .navbar-item {
      margin-left: 1.5rem;
    }
    
    .navbar-link {
      color: var(--text-light);
      text-decoration: none;
      font-size: 0.9rem;
      transition: color 0.3s ease;
    }
    
    .navbar-link:hover {
      color: var(--primary-color);
    }
    
    /* Hero Banner */
    .hero-banner {
      height: 80vh;
      background-size: cover;
      background-position: center;
      position: relative;
      margin-top: 4rem;
    }
    
    .hero-overlay {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: linear-gradient(to bottom, rgba(20,20,20,0.2), rgba(20,20,20,1));
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      padding: 3rem;
    }
    
    .hero-title {
      font-size: 3rem;
      font-weight: 700;
      margin-bottom: 1rem;
    }
    
    .hero-description {
      font-size: 1.25rem;
      max-width: 50%;
      margin-bottom: 1.5rem;
      color: var(--text-muted);
    }
    
    .hero-actions {
      display: flex;
      gap: 1rem;
    }
    
    .btn {
      display: inline-flex;
      align-items: center;
      padding: 0.75rem 1.5rem;
      border-radius: 4px;
      font-weight: 500;
      cursor: pointer;
      transition: all 0.3s ease;
      text-decoration: none;
    }
    
    .btn-primary {
      background-color: var(--primary-color);
      color: white;
      border: none;
    }
    
    .btn-primary:hover {
      background-color: var(--primary-hover);
    }
    
    .btn-secondary {
      background-color: rgba(109, 109, 110, 0.7);
      color: white;
      border: none;
    }
    
    .btn-secondary:hover {
      background-color: rgba(109, 109, 110, 0.9);
    }
    
    .btn-icon {
      margin-right: 0.5rem;
    }
    
    /* Anime Sections */
    .section {
      padding: 2rem 3rem;
    }
    
    .section-title {
      font-size: 1.5rem;
      font-weight: 700;
      margin-bottom: 1rem;
    }
    
    .anime-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 1.5rem;
    }
    
    /* Anime Cards */
    .anime-card {
      position: relative;
      overflow: hidden;
      border-radius: 4px;
      transition: transform 0.3s ease;
    }
    
    .anime-card:hover {
      transform: scale(1.05);
    }
    
    .anime-poster {
      width: 100%;
      aspect-ratio: 2/3;
      object-fit: cover;
    }
    
    .anime-overlay {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      background: linear-gradient(to top, rgba(0,0,0,0.9), transparent);
      padding: 1rem;
      opacity: 0;
      transition: opacity 0.3s ease;
    }
    
    .anime-card:hover .anime-overlay {
      opacity: 1;
    }
    
    .anime-title {
      font-size: 1rem;
      font-weight: 500;
      margin-bottom: 0.25rem;
    }
    
    .anime-match {
      color: var(--success-color);
      font-size: 0.875rem;
      margin-bottom: 0.5rem;
    }
    
    .anime-categories {
      font-size: 0.75rem;
      color: var(--text-muted);
    }
    
    /* Footer */
    .footer {
      background-color: var(--bg-darker);
      padding: 3rem;
      margin-top: 2rem;
    }
    
    .footer-content {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    
    .footer-logo {
      font-size: 1.75rem;
      font-weight: 700;
      color: var(--primary-color);
      margin-bottom: 1.5rem;
    }
    
    .footer-links {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2rem;
      margin-bottom: 2rem;
    }
    
    .footer-column {
      min-width: 160px;
    }
    
    .footer-title {
      font-size: 1rem;
      font-weight: 500;
      margin-bottom: 1rem;
    }
    
    .footer-items {
      list-style: none;
    }
    
    .footer-item {
      margin-bottom: 0.5rem;
    }
    
    .footer-link {
      color: var(--text-muted);
      text-decoration: none;
      font-size: 0.875rem;
      transition: color 0.3s ease;
    }
    
    .footer-link:hover {
      color: var(--text-light);
    }
    
    .footer-social {
      display: flex;
      gap: 1rem;
      margin-bottom: 1.5rem;
    }
    
    .social-icon {
      width: 40px;
      height: 40px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 50%;
      background-color: #333;
      transition: all 0.3s ease;
    }
    
    .social-icon:hover {
      background-color: var(--primary-color);
    }
    
    .footer-copyright {
      font-size: 0.875rem;
      color: rgba(255, 255, 255, 0.5);
    }
    
    /* Responsivity */
    @media (max-width: 768px) {
      .navbar {
        padding: 0.75rem 1rem;
      }
      
      .hero-title {
        font-size: 2rem;
      }
      
      .hero-description {
        max-width: 100%;
        font-size: 1rem;
      }
      
      .section {
        padding: 1.5rem;
      }
      
      .anime-grid {
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
      }
    }
    ]]>
  </style>
</head>
<body>
  <div class="animeflix-container">
    <!-- Navbar -->
    <nav class="navbar">
      <div class="navbar-content">
        <a href="#" class="navbar-brand">AnimeFlix</a>
        <ul class="navbar-menu">
          <li class="navbar-item"><a href="#" class="navbar-link">Início</a></li>
          <li class="navbar-item"><a href="#" class="navbar-link">Séries</a></li>
          <li class="navbar-item"><a href="#" class="navbar-link">Filmes</a></li>
          <li class="navbar-item"><a href="#" class="navbar-link">Categorias</a></li>
          <li class="navbar-item"><a href="#" class="navbar-link">Minha Lista</a></li>
        </ul>
      </div>
    </nav>
    
    <!-- Hero Banner -->
    <div class="hero-banner" style="background-image: url('https://cdn.myanimelist.net/images/anime/1286/99889l.jpg')">
      <div class="hero-overlay">
        <h1 class="hero-title">Demon Slayer</h1>
        <p class="hero-description">Tanjiro Kamado, um jovem que vende carvão, encontra sua família massacrada por um demônio. Para piorar, sua irmã mais nova, Nezuko, foi transformada em um demônio. Assim, os dois embarcam em uma jornada a fim de encontrar a cura para Nezuko e vingar sua família.</p>
        <div class="hero-actions">
          <a href="#" class="btn btn-primary">
            <span class="material-icons btn-icon">play_arrow</span>
            Assistir
          </a>
          <a href="#" class="btn btn-secondary">
            <span class="material-icons btn-icon">add</span>
            Minha Lista
          </a>
        </div>
      </div>
    </div>
    
    <!-- Populares Section -->
    <section class="section">
      <h2 class="section-title">Populares na AnimeFlix</h2>
      <div class="anime-grid">
        <!-- Anime 1 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/1223/96541l.jpg" alt="Fullmetal Alchemist" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Fullmetal Alchemist</h3>
            <div class="anime-match">98% Match</div>
            <div class="anime-categories">Ação, Aventura, Fantasia</div>
          </div>
        </div>
        
        <!-- Anime 2 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/9/9453l.jpg" alt="Death Note" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Death Note</h3>
            <div class="anime-match">96% Match</div>
            <div class="anime-categories">Mistério, Suspense, Sobrenatural</div>
          </div>
        </div>
        
        <!-- Anime 3 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/10/47347l.jpg" alt="Attack on Titan" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Attack on Titan</h3>
            <div class="anime-match">95% Match</div>
            <div class="anime-categories">Ação, Drama, Fantasia</div>
          </div>
        </div>
        
        <!-- Anime 4 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/10/78745l.jpg" alt="My Hero Academia" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">My Hero Academia</h3>
            <div class="anime-match">89% Match</div>
            <div class="anime-categories">Ação, Comédia, Super Poderes</div>
          </div>
        </div>
        
        <!-- Anime 5 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/12/76049l.jpg" alt="One Punch Man" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">One Punch Man</h3>
            <div class="anime-match">97% Match</div>
            <div class="anime-categories">Ação, Comédia, Super Poderes</div>
          </div>
        </div>
      </div>
    </section>
    
    <!-- Romance Section -->
    <section class="section">
      <h2 class="section-title">Romance</h2>
      <div class="anime-grid">
        <!-- Anime 1 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/5/87048l.jpg" alt="Your Name" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Your Name</h3>
            <div class="anime-match">96% Match</div>
            <div class="anime-categories">Romance, Sobrenatural, Drama</div>
          </div>
        </div>
        
        <!-- Anime 2 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/1295/106551l.jpg" alt="Kaguya-sama: Love is War" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Kaguya-sama: Love is War</h3>
            <div class="anime-match">94% Match</div>
            <div class="anime-categories">Romance, Comédia</div>
          </div>
        </div>
        
        <!-- Anime 3 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/1795/95088l.jpg" alt="Violet Evergarden" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Violet Evergarden</h3>
            <div class="anime-match">93% Match</div>
            <div class="anime-categories">Drama, Romance, Fantasia</div>
          </div>
        </div>
        
        <!-- Anime 4 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/1447/99827l.jpg" alt="Fruits Basket" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Fruits Basket</h3>
            <div class="anime-match">93% Match</div>
            <div class="anime-categories">Romance, Slice of Life, Sobrenatural</div>
          </div>
        </div>
      </div>
    </section>
    
    <!-- Ação Section -->
    <section class="section">
      <h2 class="section-title">Ação</h2>
      <div class="anime-grid">
        <!-- Anime 1 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/1286/99889l.jpg" alt="Demon Slayer" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Demon Slayer</h3>
            <div class="anime-match">98% Match</div>
            <div class="anime-categories">Ação, Aventura, Sobrenatural</div>
          </div>
        </div>
        
        <!-- Anime 2 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/1171/109222l.jpg" alt="Jujutsu Kaisen" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Jujutsu Kaisen</h3>
            <div class="anime-match">95% Match</div>
            <div class="anime-categories">Ação, Sobrenatural, Horror</div>
          </div>
        </div>
        
        <!-- Anime 3 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/13/17405l.jpg" alt="Naruto" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Naruto</h3>
            <div class="anime-match">97% Match</div>
            <div class="anime-categories">Ação, Aventura, Fantasia</div>
          </div>
        </div>
        
        <!-- Anime 4 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/6/73245l.jpg" alt="One Piece" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">One Piece</h3>
            <div class="anime-match">91% Match</div>
            <div class="anime-categories">Ação, Aventura, Comédia</div>
          </div>
        </div>
        
        <!-- Anime 5 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/1887/92364l.jpg" alt="Dragon Ball" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Dragon Ball</h3>
            <div class="anime-match">95% Match</div>
            <div class="anime-categories">Ação, Aventura, Fantasia</div>
          </div>
        </div>
      </div>
    </section>
    
    <!-- Comédia Section -->
    <section class="section">
      <h2 class="section-title">Comédia</h2>
      <div class="anime-grid">
        <!-- Anime 1 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/1295/106551l.jpg" alt="Kaguya-sama: Love is War" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Kaguya-sama: Love is War</h3>
            <div class="anime-match">94% Match</div>
            <div class="anime-categories">Comédia, Romance, Psicológico</div>
          </div>
        </div>
        
        <!-- Anime 2 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/8/77831l.jpg" alt="Konosuba" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Konosuba</h3>
            <div class="anime-match">95% Match</div>
            <div class="anime-categories">Comédia, Aventura, Fantasia</div>
          </div>
        </div>
        
        <!-- Anime 3 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/10/73274l.jpg" alt="Gintama" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">Gintama</h3>
            <div class="anime-match">94% Match</div>
            <div class="anime-categories">Comédia, Ação, Sci-Fi</div>
          </div>
        </div>
        
        <!-- Anime 4 -->
        <div class="anime-card">
          <img src="https://cdn.myanimelist.net/images/anime/6/73245l.jpg" alt="One Piece" class="anime-poster" />
          <div class="anime-overlay">
            <h3 class="anime-title">One Piece</h3>
            <div class="anime-match">91% Match</div>
            <div class="anime-categories">Comédia, Ação, Aventura</div>
          </div>
        </div>
      </div>
    </section>
    
    <!-- Footer -->
    <footer class="footer">
      <div class="footer-content">
        <div class="footer-logo">AnimeFlix</div>
        
        <div class="footer-links">
          <div class="footer-column">
            <h3 class="footer-title">AnimeFlix</h3>
            <ul class="footer-items">
              <li class="footer-item"><a href="#" class="footer-link">Sobre nós</a></li>
              <li class="footer-item"><a href="#" class="footer-link">Contato</a></li>
              <li class="footer-item"><a href="#" class="footer-link">Carreiras</a></li>
              <li class="footer-item"><a href="#" class="footer-link">Centro de ajuda</a></li>
            </ul>
          </div>
          
          <div class="footer-column">
            <h3 class="footer-title">Categorias</h3>
            <ul class="footer-items">
              <li class="footer-item"><a href="#" class="footer-link">Ação</a></li>
              <li class="footer-item"><a href="#" class="footer-link">Comédia</a></li>
              <li class="footer-item"><a href="#" class="footer-link">Romance</a></li>
              <li class="footer-item"><a href="#" class="footer-link">Drama</a></li>
              <li class="footer-item"><a href="#" class="footer-link">Fantasia</a></li>
            </ul>
          </div>
          
          <div class="footer-column">
            <h3 class="footer-title">Termos</h3>
            <ul class="footer-items">
              <li class="footer-item"><a href="#" class="footer-link">Termos de uso</a></li>
              <li class="footer-item"><a href="#" class="footer-link">Privacidade</a></li>
              <li class="footer-item"><a href="#" class="footer-link">Cookies</a></li>
              <li class="footer-item"><a href="#" class="footer-link">Informações corporativas</a></li>
            </ul>
          </div>
        </div>
        
        <div class="footer-social">
          <a href="#" class="social-icon">
            <span class="material-icons">facebook</span>
          </a>
          <a href="#" class="social-icon">
            <span class="material-icons">twitter</span>
          </a>
          <a href="#" class="social-icon">
            <span class="material-icons">instagram</span>
          </a>
          <a href="#" class="social-icon">
            <span class="material-icons">youtube_activity</span>
          </a>
        </div>
        
        <div class="footer-copyright">
          &copy; 2025 AnimeFlix. Todos os direitos reservados.
        </div>
      </div>
    </footer>
  </div>
</body>
</html>
