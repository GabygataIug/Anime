<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anime Finder</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        h1 {
            text-align: center;
            color: #333;
        }

        .anime-list {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
        }

        .anime-card {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .anime-card h3 {
            color: #333;
        }

        .episodes-list {
            margin-top: 20px;
            list-style-type: none;
            padding: 0;
        }

        .episode-item {
            margin-bottom: 10px;
        }

        button {
            background-color: #333;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
        }

        button:hover {
            background-color: #555;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Anime Finder</h1>
    <div id="anime-list" class="anime-list"></div>
</div>

<script>
// Dados simulados em JSON (animes e episódios)
const animesData = [
    {
        "title": "Naruto",
        "description": "Um jovem ninja busca reconhecimento e sonha em se tornar o Hokage, o líder de sua aldeia.",
        "episodes": [
            {
                "title": "Episódio 1",
                "videoUrl": "https://linkdoanime.com/episodio1.mp4"
            },
            {
                "title": "Episódio 2",
                "videoUrl": "https://linkdoanime.com/episodio2.mp4"
            }
        ]
    },
    {
        "title": "One Piece",
        "description": "Luffy e sua tripulação de piratas buscam o One Piece, o maior tesouro do mundo.",
        "episodes": [
            {
                "title": "Episódio 1",
                "videoUrl": "https://linkdoanime.com/episodio1.mp4"
            },
            {
                "title": "Episódio 2",
                "videoUrl": "https://linkdoanime.com/episodio2.mp4"
            }
        ]
    }
];

// Função para exibir os animes
function fetchAnimes() {
    const animeListElement = document.getElementById('anime-list');
    animeListElement.innerHTML = ''; // Limpa o conteúdo

    animesData.forEach(anime => {
        const animeCard = document.createElement('div');
        animeCard.classList.add('anime-card');

        // Exibe o título e descrição
        animeCard.innerHTML = `
            <h3>${anime.title}</h3>
            <p>${anime.description}</p>
            <button onclick="showEpisodes('${anime.title}')">Ver Episódios</button>
            <ul id="episodes-${anime.title}" class="episodes-list"></ul>
        `;
        animeListElement.appendChild(animeCard);
    });
}

// Função para exibir os episódios de um anime
function showEpisodes(title) {
    const anime = animesData.find(anime => anime.title === title);
    const episodesList = document.getElementById(`episodes-${title}`);
    episodesList.innerHTML = ''; // Limpa a lista de episódios

    anime.episodes.forEach(episode => {
        const episodeItem = document.createElement('li');
        episodeItem.classList.add('episode-item');
        episodeItem.innerHTML = `<a href="${episode.videoUrl}" target="_blank">${episode.title}</a>`;
        episodesList.appendChild(episodeItem);
    });
}

// Carrega os animes assim que a página carregar
window.onload = fetchAnimes;
</script>

</body>
</html>
