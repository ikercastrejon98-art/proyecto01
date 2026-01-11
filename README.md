<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Proyecto 01</title>

<style>
body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
  background: #050505;
  color: white;
  overflow-x: hidden;
}

/* Fondo animado */
.fondo {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at 20% 20%, #1a1a1a, #000);
  animation: mover 10s infinite alternate;
  z-index: -1;
}

@keyframes mover {
  0% { background-position: 0% 0%; }
  100% { background-position: 100% 100%; }
}

header {
  text-align: center;
  padding: 40px;
  font-size: 40px;
  letter-spacing: 3px;
}

section {
  max-width: 700px;
  margin: auto;
  padding: 30px;
}

.card {
  background: rgba(0,0,0,0.7);
  border: 1px solid #222;
  padding: 25px;
  margin: 20px 0;
  border-radius: 10px;
  animation: aparecer 2s ease;
}

@keyframes aparecer {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

button {
  padding: 15px 30px;
  background: black;
  color: white;
  border: 2px solid white;
  cursor: pointer;
  margin-top: 15px;
}

button:hover {
  background: white;
  color: black;
}
</style>
</head>

<body>

<div class="fondo"></div>

<header>PROYECTO 01</header>

<section>

<div class="card">
<h2>Sobre mí</h2>
<p>Soy Iker. Estoy construyendo mi mejor versión en silencio.</p>
</div>

<div class="card">
<h2>Mi misión</h2>
<p>A los 16 quiero ser fuerte, disciplinado y respetado.</p>
</div>

<div class="card">
<h2>Días desde que empecé</h2>
<p id="contador"></p>
</div>

<div class="card">
<h2>Recordatorio</h2>
<p id="frase">Presiona para recordar quién quieres ser.</p>
<button onclick="cambiar()">Recordar</button>
</div>

<div class="card">
<h2>Música</h2>
<button onclick="musica()">Encender / Apagar</button>
</div>

</section>

<audio id="song" loop>
<source src="https://cdn.pixabay.com/download/audio/2022/10/03/audio_41c6e8b0c5.mp3" type="audio/mpeg">
</audio>

<script>
function cambiar(){
  document.getElementById("frase").innerHTML = "No vine a ser promedio. Vine a ser fuerte.";
}

const inicio = new Date("2026-01-01");
setInterval(() => {
  const hoy = new Date();
  const dias = Math.floor((hoy - inicio) / (1000 * 60 * 60 * 24));
  document.getElementById("contador").innerHTML = dias + " días";
}, 1000);

function musica(){
  const song = document.getElementById("song");
  if(song.paused){
    song.play();
  } else {
    song.pause();
  }
}
</script>

</body>
</html>
