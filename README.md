# Rene-Castillo
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>René Castillo - Portafolio Interactivo</title>
  <style>
    body {
      margin: 0;
      font-family: 'Helvetica Neue', sans-serif;
      background-color: #000; /* Fondo negro */
      color: #fff; /* Texto blanco */
    }

    header {
      position: sticky;
      top: 0;
      background-color: #111; /* Fondo del encabezado */
      padding: 1rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
      z-index: 1000;
      transition: transform 0.3s ease, opacity 0.3s ease;
    }

    header img {
      transition: transform 0.3s ease, opacity 0.3s ease;
      max-width: 150px; /* Tamaño inicial */
    }

    header.scroll img {
      transform: scale(0.6); /* Reduce al 60% del tamaño */
      opacity: 0.8; /* Transparencia ligera */
    }

    .social-icons {
      display: flex;
      gap: 1rem;
    }

    .social-icons img {
      width: 32px; /* Tamaño uniforme para los íconos */
      height: 32px;
      border-radius: 50%; /* Opcional: Forma circular */
      transition: transform 0.3s ease;
    }

    .social-icons img:hover {
      transform: scale(1.2); /* Efecto de agrandamiento al pasar el cursor */
    }

    .description {
      text-align: center;
      margin: 2rem 0;
      padding: 1rem;
    }

    .description h1 {
      font-size: 2rem;
      color: #fff;
      margin-bottom: 0.5rem;
    }

    .description p {
      font-size: 1.2rem;
      color: #ccc;
    }

    .main-content {
      display: flex;
      margin-top: 2rem;
    }

    .sidebar {
      width: 300px; /* Ancho de la barra lateral */
      background: #111; /* Fondo oscuro */
      color: #fff; /* Texto blanco */
      padding: 1rem;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
      position: sticky;
      top: 0;
      height: 100vh;
      overflow-y: auto;
    }

    .feed {
      flex-grow: 1;
      padding: 2rem;
    }

    .post {
      position: relative; /* Necesario para posicionar los íconos */
      background-color: #222; /* Fondo oscuro */
      padding: 1rem;
      margin-bottom: 1rem;
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.3);
      border-radius: 5px;
    }

    .post img {
      max-width: 100%;
      border-radius: 5px;
    }

    .post .interaction-icons {
      position: absolute;
      bottom: 10px;
      left: 10px;
      display: flex;
      gap: 10px;
      opacity: 0.6; /* Íconos sutiles */
      transition: opacity 0.3s ease;
    }

    .post .interaction-icons button {
      background: none;
      border: none;
      cursor: pointer;
      font-size: 1.5rem; /* Tamaño de íconos */
    }

    .post .interaction-icons svg {
      fill: #fff; /* Color del ícono */
      width: 24px;
      height: 24px;
      transition: fill 0.3s ease;
    }

    .post:hover .interaction-icons {
      opacity: 1; /* Destacar los íconos */
    }

    .post .interaction-icons button:hover svg {
      fill: #007BFF; /* Cambiar el color al pasar cursor */
    }

    iframe {
      width: 100%;
      border-radius: 5px;
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.3);
    }
  </style>
</head>
<body>
  <header>
    <img src="ideasmec-yt.png" alt="Logo René Castillo" class="logo">
    <div class="social-icons">
      <!-- Espacios reservados para tus íconos -->
      <a href="#"><img src="IG.png" alt="Red social 1"></a>
      <a href="#"><img src="YT.png" alt="Red social 2"></a>
      <a href="#"><img src="be.png" alt="Red social 3"></a>
    </div>
  </header>
  
  <!-- Descripción creativa -->
  <div class="description">
    <h1>"Transformando ideas en arte visual y educativo, inspirando a las nuevas generaciones con creatividad, tecnología y cultura."</h1>
    <p>Con cada diseño, René Castillo fusiona pasión y estrategia, creando espacios donde el arte cobra vida y la imaginación no tiene límites.</p>
  </div>

  <div class="main-content">
    <!-- Barra lateral derecha (Videos) -->
    <div class="sidebar">
      <h2>Videos</h2>
      <iframe src="https://www.youtube.com/embed/G2EUuoIokdA" loading="lazy" allowfullscreen></iframe>
      <iframe src="https://www.youtube.com/embed/GkGO2qSNUXY" loading="lazy" allowfullscreen></iframe>
      <iframe src="https://www.youtube.com/embed/LvIfFTpdDZY" loading="lazy" allowfullscreen></iframe>
      <iframe src="https://www.youtube.com/embed/YZ_UgPuIF8Y" loading="lazy" allowfullscreen></iframe>
      <iframe src="https://www.youtube.com/embed/Td9GKQ89rtg" loading="lazy" allowfullscreen></iframe>
      <iframe src="https://www.youtube.com/embed/IZGKC1LK1hU" loading="lazy" allowfullscreen></iframe>
      <iframe src="https://www.youtube.com/embed/GvjnMdK0uZY" loading="lazy" allowfullscreen></iframe>

    </div>

    <!-- Feed principal (Imágenes) -->

    <div class="feed" id="feed">
<div class="post">
  <img src="mini9.png" alt="Descripción de la imagen">
  <div class="interaction-icons">
    <button onclick="likePost(this)">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5c0-2.41 1.72-4.5 4.5-4.5 1.54 0 3.04.77 3.96 2.09C11.46 4.77 12.96 4 14.5 4c2.78 0 4.5 2.09 4.5 4.5 0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
    </button>
    <button onclick="sharePost()">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18 16.08c-.76 0-1.44.3-1.96.77l-7.13-4.18a3.02 3.02 0 0 0 0-1.34l7.13-4.18a2.494 2.494 0 0 0 1.96.76c1.38 0 2.5-1.12 2.5-2.5S19.38 3 18 3s-2.5 1.12-2.5 2.5c0 .24.04.46.09.68L8.41 10.36C7.79 9.93 7 9.99 6.38 10.42c-.36.26-.62.63-.75 1.05-.14.47-.15.98 0 1.43.13.41.39.79.75 1.05.62.43 1.41.49 2.03.06l7.09 4.15a2.44 2.44 0 0 0-.09.68c0 1.38 1.12 2.5 2.5 2.5s2.5-1.12 2.5-2.5-1.12-2.5-2.5-2.5z"/></svg>
    </button>
  </div>
</div>
<div class="post">
  <img src="mini10.png" alt="Descripción de la imagen">
  <div class="interaction-icons">
    <button onclick="likePost(this)">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5c0-2.41 1.72-4.5 4.5-4.5 1.54 0 3.04.77 3.96 2.09C11.46 4.77 12.96 4 14.5 4c2.78 0 4.5 2.09 4.5 4.5 0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
    </button>
    <button onclick="sharePost()">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18 16.08c-.76 0-1.44.3-1.96.77l-7.13-4.18a3.02 3.02 0 0 0 0-1.34l7.13-4.18a2.494 2.494 0 0 0 1.96.76c1.38 0 2.5-1.12 2.5-2.5S19.38 3 18 3s-2.5 1.12-2.5 2.5c0 .24.04.46.09.68L8.41 10.36C7.79 9.93 7 9.99 6.38 10.42c-.36.26-.62.63-.75 1.05-.14.47-.15.98 0 1.43.13.41.39.79.75 1.05.62.43 1.41.49 2.03.06l7.09 4.15a2.44 2.44 0 0 0-.09.68c0 1.38 1.12 2.5 2.5 2.5s2.5-1.12 2.5-2.5-1.12-2.5-2.5-2.5z"/></svg>
    </button>
  </div>
</div>
<div class="post">
  <img src="mini5.png" alt="Descripción de la imagen">
  <div class="interaction-icons">
    <button onclick="likePost(this)">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5c0-2.41 1.72-4.5 4.5-4.5 1.54 0 3.04.77 3.96 2.09C11.46 4.77 12.96 4 14.5 4c2.78 0 4.5 2.09 4.5 4.5 0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
    </button>
    <button onclick="sharePost()">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18 16.08c-.76 0-1.44.3-1.96.77l-7.13-4.18a3.02 3.02 0 0 0 0-1.34l7.13-4.18a2.494 2.494 0 0 0 1.96.76c1.38 0 2.5-1.12 2.5-2.5S19.38 3 18 3s-2.5 1.12-2.5 2.5c0 .24.04.46.09.68L8.41 10.36C7.79 9.93 7 9.99 6.38 10.42c-.36.26-.62.63-.75 1.05-.14.47-.15.98 0 1.43.13.41.39.79.75 1.05.62.43 1.41.49 2.03.06l7.09 4.15a2.44 2.44 0 0 0-.09.68c0 1.38 1.12 2.5 2.5 2.5s2.5-1.12 2.5-2.5-1.12-2.5-2.5-2.5z"/></svg>
    </button>
  </div>
</div>
<div class="post">
  <img src="mini3.png" alt="Descripción de la imagen">
  <div class="interaction-icons">
    <button onclick="likePost(this)">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5c0-2.41 1.72-4.5 4.5-4.5 1.54 0 3.04.77 3.96 2.09C11.46 4.77 12.96 4 14.5 4c2.78 0 4.5 2.09 4.5 4.5 0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
    </button>
    <button onclick="sharePost()">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18 16.08c-.76 0-1.44.3-1.96.77l-7.13-4.18a3.02 3.02 0 0 0 0-1.34l7.13-4.18a2.494 2.494 0 0 0 1.96.76c1.38 0 2.5-1.12 2.5-2.5S19.38 3 18 3s-2.5 1.12-2.5 2.5c0 .24.04.46.09.68L8.41 10.36C7.79 9.93 7 9.99 6.38 10.42c-.36.26-.62.63-.75 1.05-.14.47-.15.98 0 1.43.13.41.39.79.75 1.05.62.43 1.41.49 2.03.06l7.09 4.15a2.44 2.44 0 0 0-.09.68c0 1.38 1.12 2.5 2.5 2.5s2.5-1.12 2.5-2.5-1.12-2.5-2.5-2.5z"/></svg>
    </button>
  </div>
</div>
<div class="post">
  <img src="mini4.png" alt="Descripción de la imagen">
  <div class="interaction-icons">
    <button onclick="likePost(this)">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5c0-2.41 1.72-4.5 4.5-4.5 1.54 0 3.04.77 3.96 2.09C11.46 4.77 12.96 4 14.5 4c2.78 0 4.5 2.09 4.5 4.5 0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
    </button>
    <button onclick="sharePost()">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18 16.08c-.76 0-1.44.3-1.96.77l-7.13-4.18a3.02 3.02 0 0 0 0-1.34l7.13-4.18a2.494 2.494 0 0 0 1.96.76c1.38 0 2.5-1.12 2.5-2.5S19.38 3 18 3s-2.5 1.12-2.5 2.5c0 .24.04.46.09.68L8.41 10.36C7.79 9.93 7 9.99 6.38 10.42c-.36.26-.62.63-.75 1.05-.14.47-.15.98 0 1.43.13.41.39.79.75 1.05.62.43 1.41.49 2.03.06l7.09 4.15a2.44 2.44 0 0 0-.09.68c0 1.38 1.12 2.5 2.5 2.5s2.5-1.12 2.5-2.5-1.12-2.5-2.5-2.5z"/></svg>
    </button>
  </div>
</div>
<div class="post">
  <img src="mini5.png" alt="Descripción de la imagen">
  <div class="interaction-icons">
    <button onclick="likePost(this)">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5c0-2.41 1.72-4.5 4.5-4.5 1.54 0 3.04.77 3.96 2.09C11.46 4.77 12.96 4 14.5 4c2.78 0 4.5 2.09 4.5 4.5 0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
    </button>
    <button onclick="sharePost()">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18 16.08c-.76 0-1.44.3-1.96.77l-7.13-4.18a3.02 3.02 0 0 0 0-1.34l7.13-4.18a2.494 2.494 0 0 0 1.96.76c1.38 0 2.5-1.12 2.5-2.5S19.38 3 18 3s-2.5 1.12-2.5 2.5c0 .24.04.46.09.68L8.41 10.36C7.79 9.93 7 9.99 6.38 10.42c-.36.26-.62.63-.75 1.05-.14.47-.15.98 0 1.43.13.41.39.79.75 1.05.62.43 1.41.49 2.03.06l7.09 4.15a2.44 2.44 0 0 0-.09.68c0 1.38 1.12 2.5 2.5 2.5s2.5-1.12 2.5-2.5-1.12-2.5-2.5-2.5z"/></svg>
    </button>
  </div>
</div>
<div class="post">
  <img src="mini12.png" alt="Descripción de la imagen">
  <div class="interaction-icons">
    <button onclick="likePost(this)">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5c0-2.41 1.72-4.5 4.5-4.5 1.54 0 3.04.77 3.96 2.09C11.46 4.77 12.96 4 14.5 4c2.78 0 4.5 2.09 4.5 4.5 0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
    </button>
    <button onclick="sharePost()">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18 16.08c-.76 0-1.44.3-1.96.77l-7.13-4.18a3.02 3.02 0 0 0 0-1.34l7.13-4.18a2.494 2.494 0 0 0 1.96.76c1.38 0 2.5-1.12 2.5-2.5S19.38 3 18 3s-2.5 1.12-2.5 2.5c0 .24.04.46.09.68L8.41 10.36C7.79 9.93 7 9.99 6.38 10.42c-.36.26-.62.63-.75 1.05-.14.47-.15.98 0 1.43.13.41.39.79.75 1.05.62.43 1.41.49 2.03.06l7.09 4.15a2.44 2.44 0 0 0-.09.68c0 1.38 1.12 2.5 2.5 2.5s2.5-1.12 2.5-2.5-1.12-2.5-2.5-2.5z"/></svg>
    </button>
  </div>
</div>
<div class="post">
  <img src="mini13.png" alt="Descripción de la imagen">
  <div class="interaction-icons">
    <button onclick="likePost(this)">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5c0-2.41 1.72-4.5 4.5-4.5 1.54 0 3.04.77 3.96 2.09C11.46 4.77 12.96 4 14.5 4c2.78 0 4.5 2.09 4.5 4.5 0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
    </button>
    <button onclick="sharePost()">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18 16.08c-.76 0-1.44.3-1.96.77l-7.13-4.18a3.02 3.02 0 0 0 0-1.34l7.13-4.18a2.494 2.494 0 0 0 1.96.76c1.38 0 2.5-1.12 2.5-2.5S19.38 3 18 3s-2.5 1.12-2.5 2.5c0 .24.04.46.09.68L8.41 10.36C7.79 9.93 7 9.99 6.38 10.42c-.36.26-.62.63-.75 1.05-.14.47-.15.98 0 1.43.13.41.39.79.75 1.05.62.43 1.41.49 2.03.06l7.09 4.15a2.44 2.44 0 0 0-.09.68c0 1.38 1.12 2.5 2.5 2.5s2.5-1.12 2.5-2.5-1.12-2.5-2.5-2.5z"/></svg>
    </button>
  </div>
</div>
<div class="post">
  <img src="mini14.png" alt="Descripción de la imagen">
  <div class="interaction-icons">
    <button onclick="likePost(this)">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5c0-2.41 1.72-4.5 4.5-4.5 1.54 0 3.04.77 3.96 2.09C11.46 4.77 12.96 4 14.5 4c2.78 0 4.5 2.09 4.5 4.5 0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
    </button>
    <button onclick="sharePost()">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18 16.08c-.76 0-1.44.3-1.96.77l-7.13-4.18a3.02 3.02 0 0 0 0-1.34l7.13-4.18a2.494 2.494 0 0 0 1.96.76c1.38 0 2.5-1.12 2.5-2.5S19.38 3 18 3s-2.5 1.12-2.5 2.5c0 .24.04.46.09.68L8.41 10.36C7.79 9.93 7 9.99 6.38 10.42c-.36.26-.62.63-.75 1.05-.14.47-.15.98 0 1.43.13.41.39.79.75 1.05.62.43 1.41.49 2.03.06l7.09 4.15a2.44 2.44 0 0 0-.09.68c0 1.38 1.12 2.5 2.5 2.5s2.5-1.12 2.5-2.5-1.12-2.5-2.5-2.5z"/></svg>
    </button>
  </div>
</div>
<div class="post">
  <img src="mini15.png" alt="Descripción de la imagen">
  <div class="interaction-icons">
    <button onclick="likePost(this)">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5c0-2.41 1.72-4.5 4.5-4.5 1.54 0 3.04.77 3.96 2.09C11.46 4.77 12.96 4 14.5 4c2.78 0 4.5 2.09 4.5 4.5 0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
    </button>
    <button onclick="sharePost()">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18 16.08c-.76 0-1.44.3-1.96.77l-7.13-4.18a3.02 3.02 0 0 0 0-1.34l7.13-4.18a2.494 2.494 0 0 0 1.96.76c1.38 0 2.5-1.12 2.5-2.5S19.38 3 18 3s-2.5 1.12-2.5 2.5c0 .24.04.46.09.68L8.41 10.36C7.79 9.93 7 9.99 6.38 10.42c-.36.26-.62.63-.75 1.05-.14.47-.15.98 0 1.43.13.41.39.79.75 1.05.62.43 1.41.49 2.03.06l7.09 4.15a2.44 2.44 0 0 0-.09.68c0 1.38 1.12 2.5 2.5 2.5s2.5-1.12 2.5-2.5-1.12-2.5-2.5-2.5z"/></svg>
    </button>
  </div>
</div>
<div class="post">
  <img src="F2resa25.png" alt="Descripción de la imagen">
  <div class="interaction-icons">
    <button onclick="likePost(this)">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5c0-2.41 1.72-4.5 4.5-4.5 1.54 0 3.04.77 3.96 2.09C11.46 4.77 12.96 4 14.5 4c2.78 0 4.5 2.09 4.5 4.5 0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
    </button>
    <button onclick="sharePost()">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18 16.08c-.76 0-1.44.3-1.96.77l-7.13-4.18a3.02 3.02 0 0 0 0-1.34l7.13-4.18a2.494 2.494 0 0 0 1.96.76c1.38 0 2.5-1.12 2.5-2.5S19.38 3 18 3s-2.5 1.12-2.5 2.5c0 .24.04.46.09.68L8.41 10.36C7.79 9.93 7 9.99 6.38 10.42c-.36.26-.62.63-.75 1.05-.14.47-.15.98 0 1.43.13.41.39.79.75 1.05.62.43 1.41.49 2.03.06l7.09 4.15a2.44 2.44 0 0 0-.09.68c0 1.38 1.12 2.5 2.5 2.5s2.5-1.12 2.5-2.5-1.12-2.5-2.5-2.5z"/></svg>
    </button>
  </div>
</div><div class="post">
  <img src="mini3.png" alt="Descripción de la imagen">
  <div class="interaction-icons">
    <button onclick="likePost(this)">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5c0-2.41 1.72-4.5 4.5-4.5 1.54 0 3.04.77 3.96 2.09C11.46 4.77 12.96 4 14.5 4c2.78 0 4.5 2.09 4.5 4.5 0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
    </button>
    <button onclick="sharePost()">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18 16.08c-.76 0-1.44.3-1.96.77l-7.13-4.18a3.02 3.02 0 0 0 0-1.34l7.13-4.18a2.494 2.494 0 0 0 1.96.76c1.38 0 2.5-1.12 2.5-2.5S19.38 3 18 3s-2.5 1.12-2.5 2.5c0 .24.04.46.09.68L8.41 10.36C7.79 9.93 7 9.99 6.38 10.42c-.36.26-.62.63-.75 1.05-.14.47-.15.98 0 1.43.13.41.39.79.75 1.05.62.43 1.41.49 2.03.06l7.09 4.15a2.44 2.44 0 0 0-.09.68c0 1.38 1.12 2.5 2.5 2.5s2.5-1.12 2.5-2.5-1.12-2.5-2.5-2.5z"/></svg>
    </button>
  </div>
</div>
      <div class="post">
        <img src="CalabazaOct.png" alt="Ilustración 1">
        <div class="interaction-icons">
          <button onclick="likePost(this)">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5c0-2.41 1.72-4.5 4.5-4.5 1.54 0 3.04.77 3.96 2.09C11.46 4.77 12.96 4 14.5 4c2.78 0 4.5 2.09 4.5 4.5 0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
          </button>
          <button onclick="sharePost()">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18 16.08c-.76 0-1.44.3-1.96.77l-7.13-4.18a3.02 3.02 0 0 0 0-1.34l7.13-4.18a2.494 2.494 0 0 0 1.96.76c1.38 0 2.5-1.12 2.5-2.5S19.38 3 18 3s-2.5 1.12-2.5 2.5c0 .24.04.46.09.68L8.41 10.36C7.79 9.93 7 9.99 6.38 10.42c-.36.26-.62.63-.75 1.05-.14.47-.15.98 0 1.43.13.41.39.79.75 1.05.62.43 1.41.49 2.03.06l7.09 4.15a2.44 2.44 0 0 0-.09.68c0 1.38 1.12 2.5 2.5 2.5s2.5-1.12 2.5-2.5-1.12-2.5-2.5-2.5z"/></svg>
          </button>
        </div>
      </div>
    </div>
  </div>

 <script>
  // Cambia el tamaño del logo al hacer scroll
  window.addEventListener('scroll', function() {
    const header = document.querySelector('header');
    if (window.scrollY > 0) {
      header.classList.add('scroll'); // Agregar clase 'scroll' al header
    } else {
      header.classList.remove('scroll'); // Quitar clase 'scroll' al volver al inicio
    }
  });
</script>
