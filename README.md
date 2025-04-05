
<?xml version="1.0" encoding="UTF-8" ?>
<b:template xmlns:b="http://www.google.com/2005/gml/b">
  <b:skin><![CDATA[
    body {
      background-color: #141414;
      color: #fff;
      font-family: Arial, sans-serif;
      margin: 0;
    }
    .header {
      height: 300px;
      background: url('https://i.imgur.com/x8vXgqg.jpg') center/cover no-repeat;
    }
    .content {
      padding: 20px;
    }
    .grid {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }
    .anime {
      background: #222;
      border-radius: 8px;
      width: 160px;
      overflow: hidden;
      text-align: center;
      padding-bottom: 10px;
    }
    .anime img {
      width: 100%;
      height: auto;
    }
    .anime-title {
      padding: 10px;
      font-size: 14px;
    }
    .anime-title a {
      display: inline-block;
      margin-top: 5px;
      color: #00f;
      text-decoration: underline;
    }
  ]]></b:skin>

  <b:section id='main' class='main' maxwidgets='1' showaddelement='yes'>
    <b:widget id='AnimeWidget' locked='false' title='AnimeFlix' type='HTML'>
      <b:widget-settings>
        <b:widget-setting name='content'>
          <![CDATA[
            <div class="header"></div>
            <div class="content">
              <h2>Populares</h2>
              <div class="grid">

                <div class="anime">
                  <img src="https://i.imgur.com/Uz4FZ7b.jpeg" alt="Konosuba">
                  <div class="anime-title">
                    <strong>Konosuba</strong><br>
                    <small>2024 • Comédia, Fantasia</small><br>
                    <a href="https://exemplo.com/konosuba">Assistir</a>
                  </div>
                </div>

                <div class="anime">
                  <img src="https://i.imgur.com/ye3Z1lQ.jpeg" alt="Kanojo, Okarishimasu">
                  <div class="anime-title">
                    <strong>Kanojo, Okarishimasu</strong><br>
                    <small>2023 • Romance, Comédia</small><br>
                    <a href="https://exemplo.com/kanojo">Assistir</a>
                  </div>
                </div>

                <div class="anime">
                  <img src="https://i.imgur.com/mMuZ3HG.jpeg" alt="Blue Box">
                  <div class="anime-title">
                    <strong>Blue Box</strong><br>
                    <small>2023 • Esporte, Romance</small><br>
                    <a href="https://exemplo.com/bluebox">Assistir</a>
                  </div>
                </div>

                <div class="anime">
                  <img src="https://i.imgur.com/yGC8c5P.jpeg" alt="Hunter × Hunter">
                  <div class="anime-title">
                    <strong>Hunter × Hunter</strong><br>
                    <small>2011 • Ação, Aventura</small><br>
                    <a href="https://exemplo.com/hunter">Assistir</a>
                  </div>
                </div>

              </div>
            </div>
          ]]>
        </b:widget-setting>
      </b:widget-settings>
    </b:widget>
  </b:section>
</b:template>
