
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>FELIZ DÍA DE LAS FLORES AMARILLAS</title>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@500;600&family=Playfair+Display:wght@700&family=Pacifico&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Quicksand', sans-serif;
      background: #0a0a0a;
      color: #fff;
      min-height: 100vh;
      overflow-x: hidden;
      cursor: none;
      position: relative;
    }

    /* Fondo tenue de girasoles */
    body::before {
      content: '';
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: url('https://i.postimg.cc/MTKPqRCZ/Girasoles.jpg');
      background-size: cover;
      opacity: 0.1;
      z-index: -3;
    }

    /* Overlay cálido */
    .overlay {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: linear-gradient(135deg, rgba(30, 10, 0, 0.8), rgba(10, 5, 0, 0.9));
      z-index: -2;
    }

    /* Estrellas sutiles */
    .stars {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      pointer-events: none;
      z-index: -1;
    }

    .star {
      position: absolute;
      width: 2px; height: 2px;
      background: #fff9c4;
      border-radius: 50%;
      box-shadow: 0 0 6px #fff9c4;
      opacity: 0.6;
    }

    /* Cursor personalizado */
    .cursor {
      position: fixed;
      width: 22px;
      height: 22px;
      border: 2px solid #fff9c4;
      border-radius: 50%;
      background: rgba(255, 230, 128, 0.2);
      pointer-events: none;
      transform: translate(-50%, -50%);
      z-index: 9999;
      mix-blend-mode: difference;
      transition: transform 0.1s ease;
    }

    /* Brillo del cursor */
    .cursor-glow {
      position: fixed;
      width: 120px;
      height: 120px;
      background: radial-gradient(circle, rgba(255, 230, 128, 0.1), transparent 70%);
      transform: translate(-50%, -50%);
      pointer-events: none;
      z-index: 9998;
    }

    /* Contenedor principal */
    .container {
      padding: 2rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      min-height: 100vh;
      gap: 4rem; /* Secciones más juntas */
    }

    /* Título principal */
    .main-title {
      font-family: 'Pacifico', cursive;
      font-size: 3.8rem;
      color: #ffeb3b;
      text-align: center;
      margin-top: 1rem;
      text-shadow: 
        0 0 8px #ffeb3b,
        0 0 15px #fdd835,
        0 0 25px #fbc02d,
        0 0 35px rgba(251, 192, 45, 0.6);
      letter-spacing: 2px;
      animation: glow 2s infinite alternate, bounce 3s ease-in-out infinite;
    }

    @keyframes glow {
      0% { text-shadow: 0 0 8px #ffeb3b, 0 0 15px #fdd835; }
      100% { text-shadow: 0 0 15px #fff352, 0 0 30px #fbc02d, 0 0 40px #f9a825; }
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    /* Fases */
    .phase {
      display: flex;
      flex-direction: column;
      align-items: center;
      max-width: 800px;
      text-align: center;
      opacity: 0;
      transform: translateY(40px);
      transition: opacity 0.7s ease, transform 0.7s ease;
    }

    .phase.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .phase h1 {
      font-family: 'Pacifico', cursive;
      font-size: 3rem;
      color: #fff352;
      text-shadow: 
        0 0 6px #fff352,
        0 0 12px #fdd835,
        0 0 20px rgba(251, 192, 45, 0.5);
      margin-bottom: 1.2rem;
    }

    /* Cuadro neon */
    .frame {
      border: 3px solid #ffeb3b;
      border-radius: 12px;
      padding: 8px;
      max-width: 280px;
      box-shadow: 
        0 0 10px #ffeb3b,
        0 0 20px #fdd835,
        0 0 30px rgba(251, 192, 45, 0.4);
      animation: pulse-neon 2s infinite alternate;
      overflow: hidden;
    }

    .frame img {
      width: 100%;
      border-radius: 8px;
      transition: transform 0.3s;
    }

    .frame:hover img {
      transform: scale(1.08);
    }

    @keyframes pulse-neon {
      0% { box-shadow: 0 0 10px #ffeb3b, 0 0 20px #fdd835; }
      100% { box-shadow: 0 0 15px #fff352, 0 0 30px #fbc02d, 0 0 40px #f9a825; }
    }

    /* Texto de fase */
    .phase p {
      font-size: 1.25rem;
      line-height: 1.8;
      color: #fff9c4;
      max-width: 600px;
      margin: 1rem auto;
      font-weight: 500;
    }

    .phase p em {
      color: #fff352;
      font-weight: 600;
    }

    /* Créditos */
    .credits {
      margin-top: 3rem;
      font-size: 0.95rem;
      color: #ccc;
      text-align: center;
      opacity: 0;
      animation: fadeIn 1s ease forwards;
      animation-delay: 0.8s;
    }

    .credits strong {
      color: #ffeb3b;
    }

    .credits em {
      color: #fdd835;
    }

    .credits a {
      color: #fff352;
      text-decoration: none;
      font-weight: bold;
    }

    .credits a:hover {
      text-decoration: underline;
    }

    /* Corazones y pétalos */
    .heart, .petal {
      position: absolute;
      width: 14px;
      height: 14px;
      pointer-events: none;
      opacity: 0;
      z-index: 1000;
    }

    .heart {
      background: #ffeb3b;
      transform: rotate(-45deg) scale(0);
      clip-path: polygon(75% 0%, 75% 0%, 100% 25%, 100% 50%, 75% 75%, 75% 100%, 50% 75%, 25% 100%, 25% 75%, 0% 50%, 0% 25%, 25% 0%);
      box-shadow: 0 2px 6px rgba(255, 193, 7, 0.7);
    }

    .petal {
      background: #fff9c4;
      border-radius: 50% 50% 50% 0;
      transform: rotate(var(--rotate)) scale(0);
    }

    .petal::after {
      content: '';
      position: absolute;
      top: 50%; left: -3px;
      width: 8px; height: 8px;
      background: #fdd835;
      border-radius: 50%;
    }

    .animate {
      animation: explode 1.4s ease-out forwards;
    }

    @keyframes explode {
      0% { transform: scale(0); opacity: 0; }
      20% { opacity: 1; }
      100% {
        transform: translate(var(--x), var(--y)) scale(1.4);
        opacity: 0;
      }
    }

    /* Responsive */
    @media (max-width: 768px) {
      .main-title { font-size: 2.8rem; }
      .phase h1 { font-size: 2.3rem; }
      .phase p { font-size: 1.1rem; }
      .frame { max-width: 240px; }
      .container { gap: 3rem; }
    }
  </style>
</head>
<body>

  <!-- Fondos -->
  <div class="overlay"></div>
  <div class="stars" id="stars"></div>

  <!-- Cursor -->
  <div class="cursor" id="cursor"></div>
  <div class="cursor-glow" id="cursorGlow"></div>

  <!-- Contenido -->
  <div class="container">

    <h1 class="main-title">FELIZ DÍA DE LAS FLORES AMARILLAS</h1>

    <section class="phase" id="recuerdo">
      <h1>Recuerdo</h1>
      <div class="frame">
        <img src="https://i.postimg.cc/VNFGx4HH/ramo-proncipal.jpg" alt="Ramo de recuerdo">
      </div>
      <p>
        Hay momentos que <em>no se olvidan</em>, solo se guardan en el corazón.<br>
        Como este ramo amarillo que lleva tu nombre,<br>
        como esa sonrisa que nunca dejó de brillar.
      </p>
    </section>

    <section class="phase" id="esperanza">
      <h1>Esperanza</h1>
      <div class="frame">
        <img src="https://i.postimg.cc/MTKPqRCZ/Girasoles.jpg" alt="Campo de girasoles">
      </div>
      <p>
        Aunque el camino sea largo,<br>
        <em>el sol siempre encuentra</em> a los que siguen mirando hacia arriba.<br>
        Como estos girasoles que nunca dejan de buscar la luz.
      </p>
    </section>

    <section class="phase" id="amor">
      <h1>Amor</h1>
      <div class="frame">
        <img src="https://i.postimg.cc/VNFGx4HH/ramo-proncipal.jpg" alt="Ramo de amor">
      </div>
      <p>
        El amor no necesita palabras.<br>
        Basta con un ramo amarillo,<br>
        una mirada,<br>
        un gesto.<br>
        Porque el <em>verdadero amor</em> no se mide en tiempo,<br>
        sino en eternidad.
      </p>
    </section>

    <section class="phase" id="eternidad">
      <h1>Eternidad</h1>
      <div class="frame">
        <img src="https://i.postimg.cc/MTKPqRCZ/Girasoles.jpg" alt="Campo eterno">
      </div>
      <p>
        Algunos lazos no terminan.<br>
        Se transforman en luz,<br>
        en viento,<br>
        en flores que nacen cada primavera.<br>
        Y aunque el tiempo pase,<br>
        <em>tú sigues aquí</em>,<br>
        en cada pétalo que vuela.
      </p>
    </section>

    <div class="credits">
      🌼 Detalle virtual creado con amor por 
      <strong>AnthZz Berrocal</strong> | 
      <em>BerMatMods</em> | 
      <a href="https://github.com/tu-usuario" target="_blank">GitHub Pages</a>
    </div>

  </div>

  <!-- Audio (instrumental suave tipo "Flores Amarillas") -->
  <!-- Usa un archivo local o enlace seguro -->
  <audio id="music" loop>
    <source src="https://cdn.pixabay.com/audio/2022/01/10/audio_7f7a9b5b25.mp3" type="audio/mpeg">
    <!-- Música libre: "Acoustic Emotional Background" de Pixabay -->
  </audio>

  <script>
    // Cursor
    const cursor = document.getElementById('cursor');
    const cursorGlow = document.getElementById('cursorGlow');
    document.addEventListener('mousemove', (e) => {
      cursor.style.left = e.clientX + 'px';
      cursor.style.top = e.clientY + 'px';
      cursorGlow.style.left = e.clientX + 'px';
      cursorGlow.style.top = e.clientY + 'px';
    });

    // Música al primer clic
    const music = document.getElementById('music');
    let musicStarted = false;
    document.addEventListener('click', () => {
      if (!musicStarted) {
        music.play().catch(e => console.log("Auto-play bloqueado"));
        music.volume = 0.3;
        musicStarted = true;
      }
    }, { once: true });

    // Crear partículas: flores y corazones
    function createParticle(x, y, type) {
      const el = document.createElement('div');
      el.classList.add(type);
      el.style.left = `${x}px`;
      el.style.top = `${y}px`;

      const angle = Math.random() * 360;
      const distance = 50 + Math.random() * 100;
      const vx = Math.cos(angle * Math.PI / 180) * distance;
      const vy = Math.sin(angle * Math.PI / 180) * distance;

      if (type === 'petal') {
        el.style.setProperty('--rotate', `${angle}deg`);
      }

      document.body.appendChild(el);
      setTimeout(() => el.classList.add('animate'), 10);
      setTimeout(() => el.remove(), 1400);
    }

    // Clic → explosión de flores y corazones
    document.addEventListener('click', (e) => {
      for (let i = 0; i < 8; i++) {
        setTimeout(() => createParticle(e.clientX, e.clientY, 'petal'), i * 60);
        setTimeout(() => createParticle(e.clientX, e.clientY, 'heart'), i * 60 + 30);
      }
    });

    // Mouse move → pequeñas explosiones aleatorias
    let moveTimeout;
    document.addEventListener('mousemove', (e) => {
      clearTimeout(moveTimeout);
      moveTimeout = setTimeout(() => {
        if (Math.random() < 0.4) {
          createParticle(e.clientX, e.clientY, Math.random() > 0.5 ? 'petal' : 'heart');
        }
      }, 150);
    });

    // Estrellas
    const stars = document.getElementById('stars');
    for (let i = 0; i < 80; i++) {
      const star = document.createElement('div');
      star.classList.add('star');
      star.style.left = `${Math.random() * 100}%`;
      star.style.top = `${Math.random() * 100}%`;
      star.style.opacity = Math.random() * 0.8 + 0.2;
      stars.appendChild(star);
    }

    // Revelar fases al hacer scroll
    const phases = document.querySelectorAll('.phase');
    function checkVisibility() {
      phases.forEach(phase => {
        const rect = phase.getBoundingClientRect();
        if (rect.top < window.innerHeight * 0.85) {
          phase.classList.add('visible');
        }
      });
    }

    window.addEventListener('scroll', checkVisibility);
    window.addEventListener('load', checkVisibility);
  </script>

</body>
