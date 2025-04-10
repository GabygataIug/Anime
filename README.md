<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:version="2" xmlns="http://www.w3.org/1999/xhtml" xmlns:b="http://www.google.com/2005/gml/b" xmlns:data="http://www.google.com/2005/gml/data">
<head>
  <b:include data="blog" name="all-head-content"/>
  <title>AnimeFlix - Seu streaming de animes</title>
  
  <b:skin><![CDATA[
  :root {
    --red: #e50914;
    --dark: #141414;
    --light: #f4f4f4;
  }
  
  body {
    font-family: 'Helvetica Neue', Arial, sans-serif;
    background: var(--dark);
    color: var(--light);
    margin: 0;
  }
  
  /* CABEÇALHO NETFLIX */
  .header {
    padding: 15px 50px;
    position: fixed;
    width: 100%;
    display: flex;
    justify-content: space-between;
    z-index: 100;
    background: linear-gradient(to bottom, #000 0%, transparent 100%);
  }
  
  .logo {
    height: 45px;
  }
  
  /* DESTAQUE PRINCIPAL */
  .hero {
    height: 100vh;
    background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.7)), 
                url('https://i.imgur.com/3KLfVm3.jpg') center/cover;
    display: flex;
    align-items: center;
    padding: 0 50px;
  }
  
  /* CATEGORIAS */
  .category {
    padding: 30px 50px;
  }
  
  .anime-list {
    display: flex;
    overflow-x: auto;
    gap: 15px;
    padding: 20px 0;
  }
  
  .anime-card {
    min-width: 200px;
    cursor: pointer;
    transition: transform 0.3s;
  }
  
  .anime-card:hover {
    transform: scale(1.05);
  }
  
  .anime-cover {
    width: 100%;
    border-radius: 4px;
  }
  ]]></b:skin>
</head>

<body>
  <!-- CABEÇALHO -->
  <header class="header">
    <img class="logo" src="https://i.imgur.com/mZQyH0e.png" alt="AnimeFlix"/>
    <nav>
      <a href="#" style="color:white;margin-right:20px;text-decoration:none;">Início</a>
      <a href="#" style="color:white;margin-right:20px;text-decoration:none;">Séries</a>
      <a href="#" style="color:white;text-decoration:none;">Filmes</a>
    </nav>
  </header>

  <!-- DESTAQUE PRINCIPAL -->
  <section class="hero">
    <div style="max-width:500px;">
      <h1 style="font-size:48px;margin-bottom:20px;">Attack on Titan</h1>
      <p style="font-size:18px;margin-bottom:30px;">A humanidade vive em cidades cercadas por muralhas gigantes para se proteger dos Titãs. Eren Yeager se junta à luta após testemunhar uma tragédia pessoal.</p>
      <a href="#" style="background:var(--red);color:white;padding:10px 25px;border-radius:4px;text-decoration:none;">Assistir</a>
    </div>
  </section>

  <!-- CATEGORIAS DE ANIMES PRÉ-CADASTRADOS -->
  <section class="category">
    <h2>Animes Populares</h2>
    <div class="anime-list">
      <!-- ANIME 1 - DEMON SLAYER -->
      <div class="anime-card">
        <img class="anime-cover" src="https://i.imgur.com/VhRX9yW.jpg" alt="Demon Slayer"/>
        <h3>Demon Slayer (2019)</h3>
        <p>Ação, Fantasia</p>
        <!-- ADICIONE SEU LINK AQUI -->
        <a href="#LINK_DO_VIDEO" style="color:var(--red);">Assistir</a>
      </div>
      
      <!-- ANIME 2 - JUJUTSU KAISEN -->
      <div class="anime-card">
        <img class="anime-cover" src="https://i.imgur.com/5vdfXbB.jpg" alt="Jujutsu Kaisen"/>
        <h3>Jujutsu Kaisen (2020)</h3>
        <p>Ação, Sobrenatural</p>
        <a href="#LINK_DO_VIDEO" style="color:var(--red);">Assistir</a>
      </div>
      
      <!-- ANIME 3 - SPY x FAMILY -->
      <div class="anime-card">
        <img class="anime-cover" src="https://i.imgur.com/9Xa1VQt.jpg" alt="Spy x Family"/>
        <h3>Spy x Family (2022)</h3>
        <p>Comédia, Ação</p>
        <a href="#LINK_DO_VIDEO" style="color:var(--red);">Assistir</a>
      </div>
    </div>
  </section>

  <!-- SEÇÃO PARA SEUS POSTS (OPCIONAL) -->
  <b:section id="main" showaddelement="yes">
    <b:widget id="Blog1" locked="false" title="Postagens" type="Blog"/>
  </b:section>
</body>
</html>
