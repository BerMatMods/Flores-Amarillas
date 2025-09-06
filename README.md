
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>TeAmo ❤</title>
  <!-- Fuentes -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600;700&family=Nunito:wght@600;700&family=Great+Vibes&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      width: 100vw;
      height: 100vh;
      background: #000;
      display: flex;
      justify-content: center;
      align-items: center;
      perspective: 1500px;
      overflow: hidden;
      font-family: 'Poppins', sans-serif;
      position: relative;
      cursor: default;
    }

    /* FONDO ROSADO SUAVE, BAJO EN SATURACIÓN (romántico y etéreo) */
    body::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: radial-gradient(circle at center,
        rgba(255, 180, 210, 0.2) 0%,
        rgba(240, 150, 190, 0.12) 50%,
        rgba(220, 120, 170, 0.05) 90%,
        transparent 100%);
      z-index: -2;
    }

    /* Brillo difuminado sutil */
    body::after {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(255, 150, 200, 0.08);
      backdrop-filter: blur(10px);
      z-index: -1;
    }

    /* Menú de hamburguesa animado */
    .menu-toggle {
      position: fixed;
      top: 20px;
      left: 20px;
      width: 40px;
      height: 40px;
      background: rgba(255, 100, 200, 0.3);
      border-radius: 50%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      z-index: 100;
      box-shadow: 0 0 15px rgba(255, 0, 255, 0.4);
      transition: all 0.3s ease;
    }

    .menu-toggle:hover {
      transform: scale(1.1);
      background: rgba(255, 100, 200, 0.5);
    }

    .bar {
      width: 20px;
      height: 2.5px;
      background: #ff80c4;
      margin: 3px auto;
      border-radius: 2px;
      transition: 0.3s ease;
      box-shadow: 0 0 5px rgba(255, 0, 255, 0.5);
    }

    /* Animación del menú al abrir */
    .menu-toggle.active .bar:nth-child(1) {
      transform: rotate(45deg) translate(5px, 5px);
    }
    .menu-toggle.active .bar:nth-child(2) {
      opacity: 0;
    }
    .menu-toggle.active .bar:nth-child(3) {
      transform: rotate(-45deg) translate(5px, -5px);
    }

    /* Menú desplegable */
    .menu {
      position: fixed;
      top: 80px;
      left: 20px;
      width: 250px;
      background: rgba(30, 5, 30, 0.9);
      backdrop-filter: blur(10px);
      border-radius: 15px;
      padding: 15px;
      box-shadow: 0 0 20px rgba(255, 0, 255, 0.3);
      z-index: 99;
      opacity: 0;
      visibility: hidden;
      transform: translateY(-10px);
      transition: all 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
    }

    .menu.active {
      opacity: 1;
      visibility: visible;
      transform: translateY(0);
    }

    .menu a {
      display: block;
      color: #ff80c4;
      text-decoration: none;
      font-size: 16px;
      font-weight: bold;
      padding: 12px 15px;
      border-radius: 10px;
      margin-bottom: 10px;
      background: rgba(255, 0, 255, 0.1);
      text-align: center;
      transition: all 0.3s ease;
      white-space: nowrap;
    }

    .menu a:hover {
      background: rgba(255, 0, 255, 0.3);
      transform: scale(1.05);
      color: #fff;
      box-shadow: 0 0 15px rgba(255, 0, 255, 0.5);
    }

    #canvas-container {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 1;
    }

    .instruction {
      position: absolute;
      top: 50px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 22px;
      color: #ff80ff;
      text-shadow: 0 0 15px #ff00ff, 0 0 30px #ff00ff;
      z-index: 30;
      background: rgba(0, 0, 0, 0.3);
      padding: 12px 25px;
      border-radius: 20px;
      border: 2px solid #ff00ff;
      backdrop-filter: blur(8px);
      box-shadow: 0 0 15px rgba(255, 0, 255, 0.5);
      font-weight: bold;
      letter-spacing: 1px;
    }

    .wrapper {
      position: relative;
      width: 100vw;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 5;
    }

    .card {
      position: relative;
      width: 380px;
      height: 450px;
      background: rgba(20, 5, 30, 0.85);
      border-radius: 25px;
      box-shadow: 
        0 0 25px rgba(255, 20, 147, 0.8),
        0 0 50px rgba(255, 0, 255, 0.6),
        inset 0 0 20px rgba(255, 0, 255, 0.4);
      border: 3px solid rgba(255, 0, 255, 0.7);
      transform-origin: top;
      transform-style: preserve-3d;
      transition: all 1.3s cubic-bezier(0.2, 0.8, 0.3, 1);
      z-index: 10;
      overflow: hidden;
    }

    .card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: linear-gradient(45deg, transparent 30%, rgba(255, 0, 255, 0.15) 60%, transparent 80%);
      pointer-events: none;
      opacity: 0.8;
      animation: shine 4s infinite linear;
    }

    @keyframes shine {
      0% { transform: translateX(-100%); }
      100% { transform: translateX(100%); }
    }

    .card-content {
      padding: 20px;
      opacity: 0;
      transition: opacity 0.7s;
      text-align: center;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      color: #ff80c4;
      z-index: 2;
      overflow-y: auto;
      max-height: 100%;
    }

    .card-content::-webkit-scrollbar {
      display: none;
    }

    .valentine-text h1 {
      font-size: 32px;
      color: #ff00ff;
      text-shadow: 0 0 15px #ff00ff, 0 0 25px #ff00ff;
      margin-bottom: 20px;
      font-weight: bold;
    }

    .please {
      width: 300px;
      max-width: 100%;
      border-radius: 15px;
      box-shadow: 0 0 15px rgba(255, 0, 255, 0.7);
      border: 3px solid #ff00ff;
    }

    .buttons {
      display: flex;
      gap: 20px;
      margin-top: 25px;
      z-index: 3;
    }

    .buttons button {
      padding: 14px 26px;
      font-size: 18px;
      font-weight: bold;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
      box-shadow: 0 0 12px rgba(0, 0, 0, 0.6);
    }

    .buttons button::before {
      content: '';
      position: absolute;
      top: -5px;
      left: -5px;
      right: -5px;
      bottom: -5px;
      border: 2px solid #ff00ff;
      border-radius: 14px;
      opacity: 0.7;
      z-index: -1;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0% { transform: scale(1); opacity: 0.7; }
      50% { transform: scale(1.05); opacity: 1; }
      100% { transform: scale(1); opacity: 0.7; }
    }

    .buttons button.yes {
      background: linear-gradient(145deg, #d6006c, #ff00ff);
      color: white;
      text-shadow: 0 0 5px rgba(255, 255, 255, 0.8);
    }

    .floating-no {
      position: absolute;
      padding: 14px 26px;
      font-size: 18px;
      font-weight: bold;
      border: none;
      border-radius: 12px;
      background: linear-gradient(145deg, #8b0000, #ff3366);
      color: white;
      cursor: pointer;
      z-index: 9999;
      box-shadow: 0 0 12px rgba(0, 0, 0, 0.6);
    }

    .floating-no::before {
      content: '';
      position: absolute;
      top: -5px;
      left: -5px;
      right: -5px;
      bottom: -5px;
      border: 2px solid #ff00ff;
      border-radius: 14px;
      opacity: 0.7;
      z-index: -1;
      animation: pulse 2s infinite;
    }

    .floating-no:hover {
      transform: scale(1.15);
      box-shadow: 0 0 25px rgba(255, 0, 255, 0.9);
    }

    .footer-text {
      position: absolute;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 18px;
      font-weight: bold;
      font-family: 'Great Vibes', cursive;
      background: linear-gradient(to right, #ff00ff, #00ffff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      text-shadow: 0 0 10px rgba(255, 0, 255, 0.5);
      z-index: 30;
      letter-spacing: 1px;
      white-space: nowrap;
    }

    .congrats-gif {
      width: 100%;
      max-width: 300px;
      border-radius: 15px;
      box-shadow: 0 0 30px rgba(255, 0, 255, 0.8);
      border: 4px solid #ff00ff;
      margin: 15px 0;
    }

    .love-text {
      font-family: 'Nunito', cursive;
      font-size: 20px;
      color: #ff80c4;
      text-shadow: 0 0 8px rgba(255, 0, 255, 0.3);
      margin: 20px 0;
      line-height: 1.7;
      opacity: 0;
      text-align: center;
      white-space: pre-line;
      font-weight: 600;
    }

    .cord-wrapper {
      position: absolute;
      top: -130px;
      left: 50%;
      transform: translateX(-50%);
      width: 14px;
      height: 240px;
      cursor: grab;
      z-index: 8;
    }

    .ribbon {
      position: absolute;
      top: 0;
      left: 50%;
      width: 14px;
      height: 100%;
      transform-origin: top;
      transform: translateX(-50%);
      background: #ffffff;
      box-shadow: 0 0 20px rgba(255, 255, 255, 0.9);
      z-index: 5;
    }

    .plug {
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 65px;
      height: 85px;
      cursor: grab;
      z-index: 20;
    }

    .plug svg {
      width: 100%;
      height: 100%;
    }

    .plug circle, .plug rect {
      fill: #ffffff;
      filter: drop-shadow(0 0 15px rgba(255, 255, 255, 1));
    }
  </style>
</head>
<body>
  <!-- Menú de hamburguesa -->
  <div class="menu-toggle" id="menuToggle">
    <div class="bar"></div>
    <div class="bar"></div>
    <div class="bar"></div>
  </div>

  <div class="menu" id="menu">
    <a href="https://wa.me/51930569195" target="_blank">💬 Personaliza tu versión</a>
    <a href="https://wa.me/51930569195" target="_blank">📩 Escríbeme por WhatsApp</a>
    <a href="https://wa.me/51930569195" target="_blank">❤️ Haz tu propia propuesta</a>
  </div>

  <!-- Canvas para física -->
  <div id="canvas-container"></div>

  <!-- Instrucción -->
  <div class="instruction">Baja la cuerda hasta el fondo para abrir tu regalo 💖</div>

  <!-- Contenido principal -->
  <div class="wrapper">
    <div class="card">
      <p class="text-intro">Mi Amor Baja La Cuerda.</p>
      <div class="card-content">
        <div class="valentine-text" style="display: none">
          <h1>¿Quieres ser mi novia?</h1>
          <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExM2Vna2FkeDN2NHYxenduMXVuNTJ0MmJxZjI5dG16bXhoaGJuZmoxMyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/26FLdmIp6wJr91JAI/giphy.gif" alt="Por favor" class="please" />
        </div>

        <div class="buttons" style="display: none;">
          <button class="yes">SÍ ❤️</button>
        </div>

        <div class="valentine-congrats" style="display: none">
          <h1>¡Felicidades!</h1>
          <p>Ahora Somos Los Mejores Novios!</p>
          <div class="love-text" id="loveMessage"></div>
          <img src="https://media3.giphy.com/media/v1.Y2lkPTZjMDliOTUyMHQ3aHdveHYyZnkydXN6amE2aGZrZGcxNHY5eGt2d3FwNHZqcHlpZSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/CE1sk31EVmjNS/giphy.gif" alt="Felicidades" class="congrats-gif" />
        </div>
      </div>
    </div>

    <!-- Cuerda -->
    <div class="cord-wrapper">
      <div class="ribbon"></div>
      <svg class="plug" viewBox="0 0 100 100">
        <circle cx="50" cy="30" r="22" fill="#fff" />
        <rect x="39" y="50" width="22" height="55" fill="#fff" rx="10" />
      </svg>
    </div>

    <!-- Créditos -->
    <div class="footer-text">By AnthZz Berrocal BerMatMods</div>
  </div>

  <!-- Scripts -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/matter-js/0.19.0/matter.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

  <script>
    // Menú desplegable
    const menuToggle = document.getElementById("menuToggle");
    const menu = document.getElementById("menu");

    menuToggle.addEventListener("click", () => {
      menuToggle.classList.toggle("active");
      menu.classList.toggle("active");
    });

    // --- Todo el código original a partir de aquí (física, botones, etc) ---
    const engine = Matter.Engine.create();
    const world = engine.world;

    const render = Matter.Render.create({
      element: document.getElementById("canvas-container"),
      engine: engine,
      options: {
        width: window.innerWidth,
        height: window.innerHeight,
        wireframes: false,
        background: "transparent"
      }
    });

    const segments = 12;
    const segmentHeight = 180 / segments;
    const points = [];
    const constraints = [];

    const card = document.querySelector(".card");
    const cardRect = card.getBoundingClientRect();
    const startX = window.innerWidth / 2;
    const startY = cardRect.top - 50;

    for (let i = 0; i <= segments; i++) {
      const point = Matter.Bodies.circle(startX, startY + i * segmentHeight, 4, {
        friction: 0.8,
        restitution: 0.3,
        isStatic: i === 0,
        render: { visible: false }
      });
      points.push(point);
      Matter.World.add(world, point);
    }

    for (let i = 0; i < points.length - 1; i++) {
      const constraint = Matter.Constraint.create({
        bodyA: points[i],
        bodyB: points[i + 1],
        stiffness: 0.25,
        damping: 0.1,
        length: segmentHeight,
        render: { visible: false }
      });
      constraints.push(constraint);
      Matter.World.add(world, constraint);
    }

    const runner = Matter.Runner.create();
    Matter.Runner.run(runner, engine);
    Matter.Render.run(render);

    let isDragging = false;
    const plug = document.querySelector(".plug");
    const ribbon = document.querySelector(".ribbon");
    const instruction = document.querySelector(".instruction");

    plug.addEventListener("mousedown", startDrag);
    plug.addEventListener("touchstart", startDrag);
    document.addEventListener("mousemove", drag);
    document.addEventListener("touchmove", drag);
    document.addEventListener("mouseup", endDrag);
    document.addEventListener("touchend", endDrag);

    function startDrag(e) {
      e.preventDefault();
      isDragging = true;
      plug.style.cursor = "grabbing";
    }

    function drag(e) {
      if (!isDragging) return;
      const clientX = e.clientX || e.touches[0].clientX;
      const clientY = e.clientY || e.touches[0].clientY;
      const lastPoint = points[points.length - 1];
      Matter.Body.setPosition(lastPoint, { x: clientX, y: clientY });
      updateRibbon();

      if (clientY > cardRect.top + 350 && !card.classList.contains("open")) {
        openCard();
      }
    }

    function updateRibbon() {
      const first = points[0];
      const last = points[points.length - 1];
      const dx = last.position.x - first.position.x;
      const dy = last.position.y - first.position.y;
      const angle = Math.atan2(dy, dx);
      const length = Math.sqrt(dx * dx + dy * dy);

      gsap.set(ribbon, {
        height: length,
        rotation: angle * (180 / Math.PI),
        x: first.position.x - startX,
        y: first.position.y - startY
      });

      gsap.set(plug, {
        x: last.position.x - startX - 32,
        y: last.position.y - startY - 75,
        rotation: angle * (180 / Math.PI) - 90,
        transformOrigin: "50% 0%"
      });
    }

    function endDrag() {
      isDragging = false;
      plug.style.cursor = "grab";
    }

    function openCard() {
      card.classList.add("open");
      instruction.style.opacity = "0";
      setTimeout(() => instruction.style.display = "none", 600);

      gsap.to(card, {
        y: "+=35",
        yoyo: true,
        repeat: 5,
        duration: 0.06,
        onComplete: () => gsap.set(card, { y: 0 })
      });

      confetti({
        particleCount: 500,
        spread: 190,
        origin: { y: 0.6 },
        colors: ['#ff00ff', '#00ffff', '#ff33cc']
      });

      gsap.to(".card-content", { opacity: 1, duration: 0.7, delay: 0.5 });
      gsap.to(".valentine-text", { display: "block", opacity: 1, duration: 0.7, delay: 0.7 });
      gsap.to(".buttons", { display: "flex", opacity: 1, duration: 0.7, delay: 0.8 });

      const yesButton = document.querySelector(".buttons .yes");
      const loveMessage = document.getElementById("loveMessage");
      const loveText = `Desde el primer momento supe que eras especial.\n\nTu sonrisa ilumina mi mundo, tu voz es mi canción favorita, y tu amor es lo que más deseo.\n\nQuiero cada mañana contigo, cada noche abrazarte, y cada segundo amarte más.\n\nEres mi todo, mi alma gemela, mi mejor amiga, mi hogar.\n\nGracias por decir SÍ.\n\nTe amo más de lo que las palabras pueden expresar.`;

      yesButton.addEventListener("click", function() {
        gsap.to(".valentine-text, .buttons", { display: "none", opacity: 0, duration: 0.6 });
        gsap.to(".valentine-congrats", { display: "block", opacity: 1, duration: 0.8, delay: 0.6 });

        const tl = gsap.timeline();
        tl.to(".card", {
          width: window.innerWidth < 420 ? window.innerWidth - 20 : 400,
          height: 600,
          duration: 1.0,
          ease: "power4.out"
        })
        .to(".congrats-gif", {
          width: "100%",
          maxWidth: "300px",
          duration: 0.8,
          ease: "elastic.out(1.1, 0.6)"
        }, "-=0.4");

        let i = 0;
        loveMessage.textContent = "";
        const typeWriter = setInterval(() => {
          if (i < loveText.length) {
            loveMessage.textContent += loveText.charAt(i);
            i++;
            document.querySelector(".card-content").scrollTop = document.querySelector(".card-content").scrollHeight;
          } else {
            clearInterval(typeWriter);
          }
        }, 60);

        gsap.to(loveMessage, { opacity: 1, duration: 1, delay: 0.5 });

        confetti({
          particleCount: 700,
          spread: 220,
          origin: { y: 0.6 },
          colors: ['#ff00ff', '#00ffff', '#ff33cc']
        });

        setInterval(() => {
          confetti({
            particleCount: 500,
            spread: 190,
            origin: { y: 0.6 },
            colors: ['#ff00ff', '#00ffff', '#ff33cc']
          });
        }, 2800);

        if (window.noButton && document.body.contains(window.noButton)) {
          document.body.removeChild(window.noButton);
        }
      });

      const noButton = document.createElement("button");
      noButton.textContent = "NO 😢";
      noButton.classList.add("floating-no");
      document.body.appendChild(noButton);
      window.noButton = noButton;

      function moveNoButton() {
        const maxX = window.innerWidth - noButton.offsetWidth - 40;
        const maxY = window.innerHeight - noButton.offsetHeight - 40;
        const x = Math.random() * maxX + 20;
        const y = Math.random() * maxY + 20;

        gsap.to(noButton, {
          x: x - noButton.getBoundingClientRect().left,
          y: y - noButton.getBoundingClientRect().top,
          duration: 0.9,
          ease: "power2.out",
          onComplete: moveNoButton
        });
      }

      gsap.set(noButton, { x: 100, y: 100 });
      moveNoButton();
    }

    function animate() {
      updateRibbon();
      requestAnimationFrame(animate);
    }
    animate();

    gsap.set(".card", { rotateX: 0, transformPerspective: 1500 });
  </script>
</body>
</html>
