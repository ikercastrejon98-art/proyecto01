<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>TEPIC MX</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;700&display=swap" rel="stylesheet">
<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family:'Montserrat',sans-serif;
}
body{
  background:#0b0b0b;
  color:white;
  overflow-x:hidden;
}
header{
  height:100vh;
  background:
    linear-gradient(to bottom, rgba(0,0,0,.6), #0b0b0b),
    url("https://images.unsplash.com/photo-1526401485004-2fda9f6a55d3?auto=format&fit=crop&w=1600&q=80");
  background-size:cover;
  background-position:center;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
}
header h1{
  font-size:4rem;
  letter-spacing:10px;
}
header p{
  margin-top:15px;
  opacity:.7;
}
section{
  padding:100px 10%;
}
#about{
  max-width:800px;
  margin:auto;
  text-align:center;
}
#about h2{
  margin-bottom:30px;
  letter-spacing:5px;
}
#about p{
  line-height:1.8;
  opacity:.8;
}
.gallery{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
  gap:20px;
}
.gallery img{
  width:100%;
  height:350px;
  object-fit:cover;
  filter:grayscale(20%);
  transition:.5s;
}
.gallery img:hover{
  filter:grayscale(0%);
  transform:scale(1.03);
}
footer{
  text-align:center;
  padding:40px;
  background:#000;
  font-size:.9rem;
  opacity:.6;
}
</style>
</head>
<body>

<header>
  <div>
    <h1>TEPIC MX</h1>
    <p>Nayarit, México</p>
  </div>
</header>

<section id="about">
  <h2>TEPIC</h2>
  <p>
    Tepic no es una ciudad que grite, es una ciudad que respira lento.  
    Entre montañas, calles tranquilas y cielos que se apagan en tonos naranjas,  
    aquí el tiempo parece detenerse.  
    Este proyecto es una mirada a su belleza silenciosa.
  </p>
</section>

<section>
  <div class="gallery">
    <img src="https://images.unsplash.com/photo-1610360944932-9df0b9e4f8b7?auto=format&fit=crop&w=800&q=80">
    <img src="https://images.unsplash.com/photo-1622632849984-70cf36c6b2b7?auto=format&fit=crop&w=800&q=80">
    <img src="https://images.unsplash.com/photo-1521295121783-8a321d551ad2?auto=format&fit=crop&w=800&q=80">
    <img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=800&q=80">
  </div>
</section>

<footer>
  Creado por Iker Castrejón — Tepic, Nayarit, México
</footer>

</body>
</html>
