<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Convite Especial 💖</title>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: linear-gradient(135deg, #ff9a9e, #fad0c4);
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  overflow: hidden;
}

.screen { display: none; text-align: center; }
.active { display: block; }

.card {
  background: rgba(0,0,0,0.25);
  padding: 30px;
  border-radius: 20px;
  max-width: 360px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.3);
}

button {
  padding: 12px 22px;
  border: none;
  border-radius: 25px;
  font-size: 1em;
  cursor: pointer;
}

#yesBtn { background: #ff4b5c; color: white; }
#noBtn  { background: #444; color: white; position: absolute; }

.heart {
  font-size: 2.5em;
  margin: 15px 0;
  animation: pulse 1.5s infinite;
}

@keyframes pulse {
  0% { transform: scale(1); }
  50% { transform: scale(1.2); }
  100% { transform: scale(1); }
}

.photo img {
  width: 100%;
  border-radius: 15px;
  margin-top: 20px;
}

.love-text {
  margin-top: 10px;
  font-size: 1.4em;
  font-weight: bold;
}
</style>
</head>

<body>

<!-- TELA 1 -->
<div id="screen1" class="screen active">
  <div class="card">
    <h1>Você deseja acessar? 💌</h1>
    <button id="yesBtn" onclick="goNext()">Sim 😍</button>
    <button id="noBtn">Não 😶</button>
  </div>
</div>

<!-- TELA 2 -->
<div id="screen2" class="screen">
  <div class="card">
    <h1>Oi, meu amor 💕</h1>

    <p>Quero te fazer um convite especial.</p>

    <div class="heart">❤️</div>

    <p>
      Você aceita almoçar comigo neste <strong>sábado</strong>?  
      Preparei tudo com muito carinho.
    </p>

    <p>
      O <strong>cardápio é surpresa</strong> 🍽️  
      mas o amor é garantido.
    </p>

    <div class="photo">
      <img src="d

    <div class="love-text">Eu Te Amo ❤️</div>
  </div>
</div>

<script>
const noBtn = document.getElementById("noBtn");

noBtn.addEventListener("mouseover", moveButton);
noBtn.addEventListener("click", moveButton);

function moveButton() {
  const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
  const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
}

function goNext() {
  document.getElementById("screen1").classList.remove("active");
  document.getElementById("screen2").classList.add("active");
}
</script>

</body>
</html>
