# lucas-neverland
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Lucas - Neverland</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

    body {
      font-family: 'Poppins', sans-serif;
      background-color: #d9f0d9;
      color: #2a5230;
      text-align: center;
      padding: 30px;
      position: relative;
      overflow-x: hidden;
    }

    body::before {
      content: "";
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background:
        radial-gradient(2px 2px at 20% 30%, white 98%, transparent 100%),
        radial-gradient(2px 2px at 40% 60%, white 98%, transparent 100%),
        radial-gradient(2px 2px at 70% 20%, white 98%, transparent 100%),
        radial-gradient(2px 2px at 80% 80%, white 98%, transparent 100%);
      background-repeat: repeat;
      background-size: 150px 150px;
      pointer-events: none;
      z-index: 0;
    }

    #profile-pic-container {
      width: 140px;
      height: 140px;
      margin: 0 auto 20px;
      border-radius: 50%;
      overflow: hidden;
      border: 5px solid #2a5230;
      position: relative;
      z-index: 1;
    }

    #profile-pic {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    button {
      background: #2a5230;
      border: none;
      border-radius: 25px;
      padding: 10px 20px;
      margin: 5px;
      color: white;
      font-weight: 600;
      cursor: pointer;
      position: relative;
      z-index: 1;
    }

    #otherAccountsContainer {
      display: none;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
      margin-top: 20px;
      z-index: 10;
    }

    .insta-button {
      background-color: #fff;
      color: #2a5230;
      border: 2px solid #2a5230;
      padding: 12px 18px;
      border-radius: 20px;
      font-weight: bold;
      transition: transform 0.3s ease, opacity 0.3s ease;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 10px;
      text-decoration: none;
      width: max-content;
    }

    .insta-button:hover {
      transform: scale(1.05);
    }

    .insta-pic {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      object-fit: cover;
      border: 2px solid #2a5230;
    }

    #backButton {
      display: none;
      position: fixed;
      top: 20px;
      right: 20px;
      z-index: 15;
      font-size: 30px;
      background: none;
      border: none;
      color: #2a5230;
      cursor: pointer;
    }

    p {
      position: relative;
      z-index: 1;
      margin-top: 30px;
      font-style: italic;
      font-size: 20px;
    }
  </style>
</head>
<body>

<!-- Botão Voltar -->
<button id="backButton">←</button>

<!-- Foto de perfil principal -->
<div id="profile-pic-container">
  <img id="profile-pic" src="https://i.imgur.com/4AiXzf8.jpeg" alt="Sua Foto" />
</div>

<!-- Botões principais -->
<button id="btn-other-accounts">Outras Contas</button>
<button id="btn-twitter">X (Twitter)</button>
<button id="btn-pet">🐾 Petzinho</button>

<!-- Frase -->
<p>Take me to Neverland</p>

<!-- Outras contas com espaço pra foto -->
<div id="otherAccountsContainer">
  <a class="insta-button" href="https://www.instagram.com/starlucaz_" target="_blank">
    <img class="insta-pic" src="https://via.placeholder.com/60" alt="starlucaz_" />
    @starlucaz_
  </a>
  <a class="insta-button" href="https://www.instagram.com/prvd_lucas._" target="_blank">
    <img class="insta-pic" src="https://via.placeholder.com/60" alt="prvd_lucas._" />
    @prvd_lucas._
  </a>
  <a class="insta-button" href="https://www.instagram.com/lucassveyr" target="_blank">
    <img class="insta-pic" src="https://via.placeholder.com/60" alt="lucassveyr" />
    @lucassveyr
  </a>
  <a class="insta-button" href="https://www.instagram.com/ibis_lucca" target="_blank">
    <img class="insta-pic" src="https://via.placeholder.com/60" alt="ibis_lucca" />
    @ibis_lucca
  </a>
  <a class="insta-button" href="https://www.instagram.com/galerialucas_" target="_blank">
    <img class="insta-pic" src="https://via.placeholder.com/60" alt="galerialucas_" />
    @galerialucas_
  </a>
</div>

<!-- Música de fundo -->
<audio id="background-music" autoplay loop>
  <source src="https://cdn.pixabay.com/download/audio/2022/03/21/audio_b4cfcf83ee.mp3?filename=relaxing-piano-ambient-15327.mp3" type="audio/mpeg">
</audio>

<script>
  const audio = document.getElementById('background-music');
  audio.volume = 0.05;

  const otherAccountsBtn = document.getElementById('btn-other-accounts');
  const otherAccountsContainer = document.getElementById('otherAccountsContainer');
  const backButton = document.getElementById('backButton');

  otherAccountsBtn.onclick = () => {
    const isVisible = otherAccountsContainer.style.display === 'flex';
    otherAccountsContainer.style.display = isVisible ? 'none' : 'flex';
    backButton.style.display = isVisible ? 'none' : 'block';
  };

  backButton.onclick = () => {
    otherAccountsContainer.style.display = 'none';
    backButton.style.display = 'none';
  };

  document.getElementById('btn-twitter').onclick = () =>
    window.open('https://twitter.com/seu_usuario', '_blank');

  document.getElementById('btn-pet').onclick = () =>
    alert('Aqui vai aparecer o petzinho (em breve 🐶✨)');
</script>

</body>
</html 
