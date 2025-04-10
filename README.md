<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:version='2' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
<head>
    <meta charset='utf-8'/>
    <meta content='width=device-width, initial-scale=1' name='viewport'/>
    <title><data:blog.pageTitle/></title>
    
    <b:skin><![CDATA[
    /* INÍCIO DO CSS */
    :root {
        --primary-color: #e50914;
        --dark-color: #141414;
        --light-color: #f4f4f4;
        --gray-color: #999;
    }
    
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    
    body {
        font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
        background-color: var(--dark-color);
        color: var(--light-color);
    }
    
    /* Header */
    .header {
        padding: 20px 50px;
        position: relative;
        z-index: 10;
        background: linear-gradient(to bottom, rgba(0,0,0,0.7) 10%, rgba(0,0,0,0));
    }
    
    /* [CONTINUE COM TODO O CSS ANTERIOR...] */
    ]]></b:skin>
</head>
<body>
    <!-- Header -->
    <header class='header'>
        <nav class='header__nav'>
            <h1 class='header__logo'><a href='/'><data:blog.title/></a></h1>
            <ul class='header__menu'>
                <li><a href='/'>Início</a></li>
                <li><a href='/search/label/Series'>Séries</a></li>
                <li><a href='/search/label/Filmes'>Filmes</a></li>
                <b:if cond='data:blog.pageType != "static_page"'>
                    <li><a expr:href='data:blog.homepageUrl + "?m=1"'>Bombando</a></li>
                </b:if>
            </ul>
        </nav>
    </header>

    <!-- Conteúdo Principal -->
    <div class='content'>
        <b:section id='main' showaddelement='yes'>
            <b:widget id='Blog1' locked='false' title='Postagens do Blog' type='Blog'>
                <b:includable id='main' var='top'>
                    <!-- Posts -->
                    <b:loop values='data:posts' var='post'>
                        <article class='post'>
                            <h2 class='post-title'><a expr:href='data:post.url'><data:post.title/></a></h2>
                            <div class='post-content'><data:post.body/></div>
                        </article>
                    </b:loop>
                </b:includable>
            </b:widget>
        </b:section>
    </div>

    <!-- Footer -->
    <footer class='footer'>
        <p>© <data:blog.title/> - Todos os direitos reservados</p>
    </footer>

    <!-- Scripts -->
    <script type='text/javascript'>
    //<![CDATA[
    document.querySelectorAll('.category__item').forEach(item => {
        item.addEventListener('mouseenter', () => {
            item.style.transform = 'scale(1.05)';
        });
        
        item.addEventListener('mouseleave', () => {
            item.style.transform = 'scale(1)';
        });
    });
    //]]>
    </script>
</body>
</html>
