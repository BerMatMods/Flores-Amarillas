
<html 
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Feliz Día de las Flores Amarillas - By AnthZz Berrocal</title>

  <!-- Fuentes -->
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Montserrat:wght@700;800;900&family=Great+Vibes&family=Pacifico&display=swap" rel="stylesheet">

  <style>
    /* === Estilo principal (igual que antes) === */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Montserrat', sans-serif;
      overflow-x: hidden;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      min-height: 100vh;
      transition: background 0.8s ease, color 0.5s ease, filter 0.3s ease;
      position: relative;
    }

    @keyframes gradientFlow {
      0%, 100% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
    }

    /* === TEMAS (sin cambios) === */
    body.theme-romantic {
      background: linear-gradient(45deg, #ff9a9e, #fad0c4, #d2b4de);
      background-size: 600% 600%;
      animation: gradientFlow 25s ease infinite;
      color: white;
    }
    body.theme-dark {
      background: #1a0020;
      color: #f8d1e8;
      animation: none;
    }
    body.theme-night {
      background: #0a0a2a;
      color: #e0b8f4;
      animation: stars 10s linear infinite;
    }
    @keyframes stars {
      0% { background-position: 0% 0%; }
      100% { background-position: 100% 100%; }
    }
    body.theme-light {
      background: #fff5fb;
      color: #8a3b8f;
      animation: none;
    }
    body.theme-neon {
      background: linear-gradient(45deg, #0f003f, #1a0b5e, #4a0080);
      background-size: 600% 600%;
      animation: gradientFlow 25s ease infinite;
      color: #ff9eca;
    }
    body.theme-gold {
      background: linear-gradient(45deg, #4d2b00, #8b5e00, #d4a744);
      background-size: 600% 600%;
      animation: gradientFlow 25s ease infinite;
      color: #fff8dc;
    }
    body.theme-sky {
      background: linear-gradient(45deg, #003b6f, #0077b6, #90e0ef);
      background-size: 600% 600%;
      animation: gradientFlow 25s ease infinite;
      color: #ffe5d9;
    }
    body.theme-purple {
      background: linear-gradient(45deg, #2e004d, #6a0ca6, #b19cd9);
      background-size: 600% 600%;
      animation: gradientFlow 25s ease infinite;
      color: #ffe6f2;
    }

    /* Brillo del texto */
    .letter p, .letter h2, .credits, .menu-link, .theme-option, .font-option {
      text-shadow: 
        0 0 10px rgba(255, 100, 180, 0.9),
        0 0 20px rgba(233, 30, 99, 0.7);
    }

    /* === BOTÓN DE MENÚ MEJORADO === */
    .menu-btn {
      position: absolute;
      top: 20px;
      left: 20px;
      font-size: 30px;
      color: #fff9c4;
      background: rgba(255, 255, 255, 0.15);
      width: 55px;
      height: 55px;
      border-radius: 50%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      z-index: 100;
      backdrop-filter: blur(8px);
      box-shadow: 0 6px 15px rgba(0,0,0,0.2), 0 0 20px rgba(255, 235, 59, 0.3);
      transition: all 0.4s cubic-bezier(0.25, 0.8, 0.25, 1);
      border: 2px solid rgba(255, 235, 59, 0.4);
    }

    .menu-btn:hover {
      transform: scale(1.15) rotate(5deg);
      box-shadow: 0 8px 25px rgba(0,0,0,0.3), 0 0 30px rgba(255, 235, 59, 0.5);
    }

    .menu-btn::before,
    .menu-btn::after {
      content: '';
      width: 60%;
      height: 2px;
      background: #fff9c4;
      border-radius: 2px;
      transition: 0.3s ease;
    }

    .menu-btn span {
      display: block;
      width: 60%;
      height: 2px;
      background: #fff9c4;
      margin: 4px 0;
      border-radius: 2px;
      transition: 0.3s ease;
    }

    /* === SIDEBAR CON ESTILO AMARILLO === */
    .sidebar {
      position: fixed;
      top: 0;
      left: -320px;
      width: 300px;
      height: 100vh;
      background: rgba(30, 0, 50, 0.98);
      backdrop-filter: blur(15px);
      box-shadow: 5px 0 40px rgba(255, 235, 59, 0.2);
      padding: 70px 20px 40px;
      transition: left 0.6s cubic-bezier(0.4, 0, 0.2, 1);
      z-index: 99;
      overflow-y: auto;
      color: #ffd1ef;
      border-right: 1px solid rgba(255, 235, 59, 0.2);
    }

    .sidebar.active {
      left: 0;
      border-left: 2px solid #ffeb3b;
    }

    .close-btn {
      position: absolute;
      top: 25px;
      right: 25px;
      font-size: 30px;
      color: #ffeb3b;
      cursor: pointer;
      transition: all 0.3s;
      text-shadow: 0 0 10px #ffeb3b;
    }

    .close-btn:hover {
      transform: rotate(90deg) scale(1.1);
      text-shadow: 0 0 20px #fdd835;
    }

    .profile img {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      border: 4px solid #ffeb3b;
      object-fit: cover;
      margin-bottom: 15px;
      box-shadow: 0 0 25px rgba(255, 235, 59, 0.5);
    }

    .profile h3 {
      font-family: 'Dancing Script', cursive;
      font-size: 2.2rem;
      color: #fff9c4;
      margin: 10px 0 5px;
      text-shadow: 0 0 10px #ffeb3b;
    }

    .profile p {
      color: #fdd835;
      font-size: 0.95rem;
    }

    .menu-link, .theme-option, .font-option {
      display: block;
      color: #fff9c4;
      padding: 12px 18px;
      border-radius: 12px;
      margin: 8px 0;
      background: rgba(255, 235, 59, 0.1);
      text-decoration: none;
      transition: all 0.3s ease;
      font-size: 1rem;
      border: 1px solid rgba(255, 235, 59, 0.2);
    }

    .menu-link:hover, .theme-option:hover, .font-option:hover {
      background: rgba(255, 235, 59, 0.25);
      transform: translateX(8px);
      box-shadow: 0 0 15px rgba(255, 235, 59, 0.4);
      border-color: #fdd835;
    }

    /* === CARTA PRINCIPAL === */
    .card {
      width: 90%;
      max-width: 720px;
      background: rgba(255, 255, 255, 0.15);
      backdrop-filter: blur(12px);
      border-radius: 30px;
      padding: 30px;
      margin-top: 60px;
      box-shadow: 0 15px 40px rgba(0,0,0,0.2), 0 0 30px rgba(255,100,180,0.25);
      position: relative;
      z-index: 10;
      text-align: center;
    }

    .letter h2 {
      font-family: 'Dancing Script', cursive;
      font-size: 4.2rem;
      font-weight: 700;
      color: #fff;
      margin: 0 0 25px 0;
      text-shadow: 0 0 10px #ffeb3b, 0 0 20px #fdd835, 0 0 30px rgba(255, 235, 59, 0.8);
    }

    .letter p {
      font-family: 'Montserrat', sans-serif;
      font-size: 1.4rem;
      font-weight: 800;
      line-height: 1.8;
      color: #fff;
      margin: 15px auto;
      max-width: 640px;
    }

    .typing-text {
      white-space: nowrap;
      overflow: hidden;
      width: 0;
      border-right: 3px solid #ffeb3b;
      animation: typing 3s steps(60) forwards, blink 0.3s step-end infinite;
    }

    @keyframes typing {
      from { width: 0; }
      to { width: 100%; }
    }

    @keyframes blink {
      from, to { border-color: transparent; }
      50% { border-color: #ffeb3b; }
    }

    .btn-long-card {
      background: linear-gradient(45deg, #ffeb3b, #ffc107);
      color: #333;
      border: none;
      padding: 12px 24px;
      border-radius: 25px;
      font-size: 1.1rem;
      font-weight: 800;
      cursor: pointer;
      margin: 15px 0;
      box-shadow: 0 0 15px rgba(255, 235, 59, 0.6);
      transition: all 0.3s;
    }

    .btn-long-card:hover {
      transform: scale(1.05);
      background: linear-gradient(45deg, #fdd835, #ffb300);
    }

    /* === FLOR AMARILLA CON ANIMACIÓN SUAVE === */
    .yellow-flower {
      width: 70%;
      max-width: 400px;
      margin: 30px auto 20px;
      filter: drop-shadow(0 15px 35px rgba(255, 200, 0, 0.4));
      animation: floatGentle 8s ease-in-out infinite, swayBreeze 7s ease-in-out infinite;
      transform-origin: bottom center;
    }

    @keyframes floatGentle {
      0%, 100% { transform: translateY(0) rotate(-1deg); }
      50% { transform: translateY(-12px) rotate(1deg); }
    }

    @keyframes swayBreeze {
      0%, 100% { transform: rotate(-2deg); }
      50% { transform: rotate(2deg); }
    }

    /* === Lluvia de palabras doradas === */
    .falling-word {
      position: absolute;
      font-family: 'Montserrat', sans-serif;
      font-size: 24px;
      font-weight: 800;
      color: white;
      background: linear-gradient(45deg, #ffeb3b, #ffc107);
      padding: 10px 16px;
      border-radius: 14px;
      box-shadow: 0 0 12px #ffeb3b, 0 0 24px #ffc107;
      top: -60px;
      opacity: 0.95;
      pointer-events: none;
      user-select: none;
      animation: fall linear forwards;
      z-index: 1;
      white-space: nowrap;
    }

    @keyframes fall {
      to { top: 100vh; opacity: 0.1; }
    }

    /* === CRÉDITOS === */
    .credits {
      font-size: 1.2rem;
      font-weight: 800;
      color: #fff;
      text-shadow: 0 0 10px rgba(255,100,180,0.8);
      margin-bottom: 20px;
      z-index: 20;
    }

    @media (max-width: 768px) {
      .letter h2 { font-size: 3.2rem; }
      .letter p { font-size: 1.2rem; }
      .credits { font-size: 1rem; }
      .yellow-flower { width: 75%; }
    }
  </style>
</head>
<body class="theme-romantic" id="body">

  <!-- === BOTÓN DE MENÚ MEJORADO === -->
  <div class="menu-btn" id="menuBtn">
    <span></span>
    <span></span>
    <span></span>
  </div>

  <!-- === SIDEBAR CON ESTILO === -->
  <div class="sidebar" id="sidebar">
    <div class="close-btn" id="closeBtn">×</div>

    <div class="profile">
      <img src="https://i.postimg.cc/HsxYhHdt/Screenshot-20250912-155228.jpg" alt="Logo AnthZz Berrocal">
      <h3>AnthZz Berrocal</h3>
      <p>BerMatMods • Artista Digital & Diseñador</p>
    </div>

    <div class="menu-section">
      <h4>📞 Contacto</h4>
      <a href="https://wa.me/51930569195" target="_blank" class="menu-link">💬 WhatsApp Oficial</a>
      <a href="mailto:anthzz.berrocal@gmail.com" class="menu-link">📧 Correo Electrónico</a>
    </div>

    <div class="menu-section">
      <h4>🎨 Temas Disponibles</h4>
      <div class="theme-option" data-theme="theme-romantic"><span class="color-preview"></span> 💖 Romántico</div>
      <div class="theme-option" data-theme="theme-dark"><span class="color-preview"></span> 🖤 Oscuro</div>
      <div class="theme-option" data-theme="theme-night"><span class="color-preview"></span> 🌙 Noche Estrellada</div>
      <div class="theme-option" data-theme="theme-light"><span class="color-preview"></span> ☀️ Claro</div>
      <div class="theme-option" data-theme="theme-neon"><span class="color-preview"></span> 🌃 Neón Azul</div>
      <div class="theme-option" data-theme="theme-gold"><span class="color-preview"></span> ✨ Dorado</div>
      <div class="theme-option" data-theme="theme-sky"><span class="color-preview"></span> 🌤 Celeste Profundo</div>
      <div class="theme-option" data-theme="theme-purple"><span class="color-preview"></span> 🟣 Morado Místico</div>
    </div>

    <div class="menu-section">
      <h4>✨ Brillo del Fondo</h4>
      <div class="brightness-control">
        <label for="brightness">Intensidad del Color</label>
        <input type="range" id="brightness" min="50" max="200" value="100">
      </div>
    </div>

    <div class="menu-section">
      <h4>🔤 Tipos de Letra</h4>
      <div class="font-option" data-font="Montserrat">Montserrat (Negrita)</div>
      <div class="font-option" data-font="Dancing Script">Dancing Script (Elegante)</div>
      <div class="font-option" data-font="Great Vibes">Great Vibes (Cursiva)</div>
      <div class="font-option" data-font="Pacifico">Pacifico (Divertida)</div>
    </div>

    <div class="menu-section">
      <h4>🎵 Música Libre</h4>
      <div class="music-item">
        <button onclick="playMusic('https://www.soundhelix.com/audio/SoundHelix-Song-1.mp3')" class="menu-link">🎧 Canción 1</button>
      </div>
      <div class="music-item">
        <button onclick="playMusic('https://www.soundhelix.com/audio/SoundHelix-Song-13.mp3')" class="menu-link">🎧 Canción 2</button>
      </div>
      <div class="music-item">
        <button onclick="playMusic('https://www.soundhelix.com/audio/SoundHelix-Song-17.mp3')" class="menu-link">🎧 Canción 3</button>
      </div>
      <div class="music-item">
        <button onclick="stopMusic()" class="menu-link">⏹️ Detener Música</button>
      </div>
    </div>

    <div class="menu-section">
      <h4>🔖 Créditos</h4>
      <p style="color:#ffd1ef; font-size:0.9rem;">
        Creado con amor por <strong>AnthZz Berrocal</strong><br>
        © BerMatMods 2025<br>
        Todos los derechos reservados.
      </p>
    </div>
  </div>

  <!-- === CARTA PRINCIPAL === -->
  <div class="card">
    <div class="letter">
      <h2>Feliz Día de las Flores Amarillas 💛</h2>
      <p class="typing-text">Hoy celebro tu luz, como una flor que ilumina mi vida… 🌼</p>
      <p style="opacity:0;" id="p2">Eres mi <strong>sol</strong> ☀️, mi risa más sincera 😄, mi paz en medio del caos 🕊️.</p>
      <p style="opacity:0;" id="p3">Gracias por tu <strong>dulzura</strong> 🍯, por tu <strong>fuerza</strong> 💪, por amarme con cada gesto 💞.</p>
      <p style="opacity:0;" id="p4">Cada día contigo es un regalo envuelto en <strong>amor amarillo</strong> 🌼, lleno de momentos eternos 📸.</p>
      <p style="opacity:0; font-style:italic;" id="p5">Te llevo en el corazón 🫀… ¡Y siempre caminaré a tu lado! 💑💛</p>
    </div>
    <button class="btn-long-card" id="showLongCard">📜 Ver Carta Especial (Larga)</button>
  </div>

  <!-- === FLOR AMARILLA === -->
  <img 
    src="https://i.postimg.cc/RVVyVM0J/1123bcf6788b414bb111a4a8ce81d15d-removebg-preview-1.png" 
    alt="Flor Amarilla - Día de las Flores Amarillas" 
    class="yellow-flower"
  />

  <!-- === CRÉDITOS === -->
  <div class="credits">🌼 Feliz Día de las Flores Amarillas • By AnthZz Berrocal BerMatMods 🌼</div>

  <!-- === AUDIO Y CHISPAS === -->
  <audio id="bgMusic" loop></audio>
  <div class="audio-controls" id="audioInfo" style="display:none;">🎶 Reproduciendo música...</div>

  <script>
    // Menú
    const menuBtn = document.getElementById('menuBtn');
    const closeBtn = document.getElementById('closeBtn');
    const sidebar = document.getElementById('sidebar');
    menuBtn.addEventListener('click', () => sidebar.classList.add('active'));
    closeBtn.addEventListener('click', () => sidebar.classList.remove('active'));

    // Temas
    document.querySelectorAll('.theme-option').forEach(option => {
      option.addEventListener('click', () => {
        document.body.className = option.dataset.theme;
        sidebar.classList.remove('active');
      });
    });

    // Brillo
    document.getElementById('brightness').addEventListener('input', (e) => {
      document.body.style.filter = `brightness(${e.target.value}%)`;
    });

    // Fuentes
    document.querySelectorAll('.font-option').forEach(font => {
      font.addEventListener('click', () => {
        const family = font.dataset.font;
        document.querySelectorAll('.letter p, .letter h2').forEach(el => {
          el.style.fontFamily = `${family}, cursive, sans-serif`;
        });
        sidebar.classList.remove('active');
      });
    });

    // Música
    const audio = document.getElementById('bgMusic');
    const audioInfo = document.getElementById('audioInfo');

    function playMusic(src) {
      audio.src = src;
      const playPromise = audio.play();
      if (playPromise !== undefined) {
        playPromise.then(() => {
          audioInfo.style.display = "block";
        }).catch(err => {
          console.warn("Reproducción bloqueada: interacción requerida.", err);
          alert("Por favor, haz clic en cualquier lado primero para activar el sonido.");
        });
      }
    }

    function stopMusic() {
      audio.pause();
      audio.src = "";
      audioInfo.style.display = "none";
    }

    // Lluvia de palabras doradas
    const words = ['Amor', 'Dulzura', 'Siempre', 'Te amo', 'Gracias', 'Eternos', 'Mi alma gemela', 'Confío en ti', 'Juntos'];
    setInterval(() => {
      const word = document.createElement('div');
      word.className = 'falling-word';
      word.textContent = words[Math.floor(Math.random() * words.length)];
      word.style.left = Math.random() * 80 + 'vw';
      word.style.animationDuration = (Math.random() * 14 + 8) + 's';
      document.body.appendChild(word);
      setTimeout(() => word.remove(), 18000);
    }, 500);

    // ✨💥 EXPLOSIÓN DE GIRASOLES AL TOCAR LA PANTALLA
    document.body.addEventListener('click', (e) => {
      // Generar entre 80 y 100 girasoles pequeños
      for (let i = 0; i < 90; i++) {
        const sunflower = document.createElement('div');
        sunflower.innerHTML = '🌻';
        sunflower.style.position = 'absolute';
        sunflower.style.left = `${e.clientX}px`;
        sunflower.style.top = `${e.clientY}px`;
        sunflower.style.fontSize = `${Math.random() * 14 + 10}px`; // Pequeños pero visibles
        sunflower.style.opacity = 0;
        sunflower.style.pointerEvents = 'none';
        sunflower.style.userSelect = 'none';

        // Brillo suave
        sunflower.style.textShadow = '0 0 5px rgba(255, 235, 59, 0.8)';

        document.body.appendChild(sunflower);

        // Animación radial
        setTimeout(() => {
          const angle = Math.random() * 360;
          const distance = Math.random() * 200 + 80;
          const x = Math.cos(angle) * distance;
          const y = Math.sin(angle) * distance;

          sunflower.style.transition = 'transform 1.8s ease-out, opacity 1.8s ease-out';
          sunflower.style.transform = `translate(${x}px, ${y}px) rotate(${Math.random()*360}deg)`;
          sunflower.style.opacity = 0.9;
        }, Math.random() * 100);

        // Eliminar después
        setTimeout(() => sunflower.remove(), 2000);
      }
    });

    // Texto automático rápido
    setTimeout(() => { document.getElementById('p2').style.opacity = 1; }, 3000);
    setTimeout(() => { document.getElementById('p3').style.opacity = 1; }, 4000);
    setTimeout(() => { document.getElementById('p4').style.opacity = 1; }, 5000);
    setTimeout(() => { document.getElementById('p5').style.opacity = 1; }, 6000);

    // === CARTA LARGA CON FIRMA ===
    document.getElementById('showLongCard').addEventListener('click', () => {
      const longText = `
        🌼 <strong>Feliz Día de las Flores Amarillas, mi amor</strong> 💛<br><br>
        Hoy no solo celebro esta fecha tan especial, 
        sino <strong>cada instante en el que decidiste quedarte a mi lado</strong>.<br><br>
        Eres como una flor amarilla entre tantas: 
        <strong>rara, hermosa, llena de luz</strong> ☀️, 
        capaz de hacer brillar incluso los días más grises 🌧️.<br><br>
        Gracias por tu paciencia 🕊️, por tu sonrisa que cura todo 😊, 
        por ser mi cómplice en cada locura 🎭.<br><br>
        Cada mensaje, cada mirada, cada silencio cómodo… 
        es un <strong>tesoro</strong> 💎 que guardo en el alma.<br><br>
        Esta historia nuestra es mágica, verdadera, eterna. 
        Y aunque pasen los años, 
        seguiré eligiéndote todos los días. ❤️‍🔥<br><br>
        Te amo con todo mi ser. 
        MI AMOR💑✨<br><br>
        Con todo mi cariño,<br>
        <em>Atte: AnthZz Berrocal</em> 💞<br><br>
        <strong style="color:#ffeb3b; text-shadow:0 0 10px #fdd835;">Atte: AnthZz Berrocal BerMatMods</strong> 🌻
      `;
      document.querySelector('.card .letter').innerHTML = `<p style="font-size:1.3rem; line-height:2; text-align:justify; color:white;">${longText}</p>`;
    });
  </script>
</body>
</html>
