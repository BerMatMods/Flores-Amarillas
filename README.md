
<html lang="es">
<head>
  <!-- Meta básicos -->
  <meta charset="utf-8">
  <title>Flores Amarillas - Elige una flor, Nombre, mensaje y envía
  por WhatsApp🌻</title>
  <meta name="viewport" content=
  "width=device-width, initial-scale=1"><!-- SEO -->
  <meta name="description" content=
  "Envía flores amarillas virtuales gratis a tus seres queridos. Añade un mensaje especial y comparte a través de WhatsApp.">
  <meta name="keywords" content=
  "flores amarillas, rosa virtual, enviar rosas gratis, regalo virtual, whatsapp, flores online">
  <meta name="author" content="Yefrin Pacheco">
  <meta name="robots" content="index, follow">
  <link rel="canonical" href=
  "https://floresamarillas.yefrinpacheco.com">
  <!-- Idioma y compatibilidad -->
  <meta http-equiv="Content-Language" content="es">
  <meta name="language" content="Spanish">
  <meta name="theme-color" content="#FFD700">
  <!-- Color de tema en móviles -->
  <!-- Favicon -->
  <link rel="icon" href=
  "https://floresamarillas.yefrinpacheco.com/images/icon.png" type=
  "image/png"><!-- Open Graph para Facebook/WhatsApp -->
  <meta property="og:title" content=
  "Feliz día de las Flores Amarillas🌻">
  <meta property="og:description" content=
  "Te regalo estas flores amarillas 🌻✨">
  <meta property="og:image" content=
  "https://floresamarillas.yefrinpacheco.com/ramo.jpg">
  <meta property="og:url" content=
  "https://floresamarillas.yefrinpacheco.com">
  <meta property="og:type" content="website"><!-- Twitter Card -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content=
  "Feliz día de las Flores Amarillas🌻">
  <meta name="twitter:description" content=
  "Te regalo estas flores amarillas 🌻✨">
  <meta name="twitter:image" content=
  "https://floresamarillas.yefrinpacheco.com/icon.png">
  <script>
  // --- ROBUST CONSOLE & SHORTCUT BLOCKER ---
  (function() {
    // Block right-click context menu
    document.addEventListener('contextmenu', event => event.preventDefault());
    // Block key combinations
    document.addEventListener('keydown', function(e) {
        if (
            e.key === 'F12' ||
            (e.ctrlKey && e.shiftKey && ['I', 'J', 'C'].includes(e.key.toUpperCase())) ||
            (e.ctrlKey && ['U', 'S'].includes(e.key.toUpperCase()))
        ) {
            e.preventDefault();
        }
    });
    // --- Aggressive DevTools blocking using a debugger loop ---
    const devToolsTrap = () => {
        debugger;
    };
    // Run the trap at a high frequency
    setInterval(devToolsTrap, 50);
  })();
  </script><!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com"
  crossorigin="">
  <link href=
  "https://fonts.googleapis.com/css2?family=Sour+Gummy:ital,wght@0,100..900;1,100..900&amp;display=swap"
  rel="stylesheet"><!-- Favicon -->
  <link rel="icon" href=
  "data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>❤️</text></svg>">
  <style>
        *,
        *::after,
        *::before {
            padding: 0;
            margin: 0;
            box-sizing: border-box;
        }
        :root {
            --dark-color: #000;
            --fl-speed: 0.8s;
            --speed-leaf: 2s;
            --petal-gradient-start: #ff8c00;
            --petal-gradient-mid: #ffd700;
            --petal-gradient-end: #ffff00;
            --petal-shadow: rgba(255, 215, 0, 0.4);
            --center-color-1: #654321;
            --center-color-2: #8b4513;
            --center-color-3: #2f1b14;
            --center-shadow: rgba(139, 69, 19, 0.6);
            --stem-gradient-1: #2d5016;
            --stem-gradient-2: #4a7c23;
            --stem-gradient-3: #6b8e23;
            --leaf-gradient-1: rgba(45, 80, 22, 0.6);
            --leaf-gradient-2: #4a7c23;
            --leaf-gradient-3: #6b8e23;
            --grass-color: #4a7c23;
            --light-seeds-1: #8b4513;
            --light-seeds-2: #654321;
            --light-seeds-shadow: rgba(139, 69, 19, 0.8);
        }
        body {
            display: flex;
            align-items: flex-end;
            justify-content: center;
            min-height: 100vh;
            background-color: var(--dark-color);
            overflow: hidden;
            perspective: 1000px;
            position: relative;
            font-family: "Sour Gummy", system-ui, cursive;
        }
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url("assets/back.jpeg");
            background-size: cover;
            background-position: center;
            opacity: 0.15;
            filter: blur(15px);
            z-index: -1;
        }
        .love-title {
            position: absolute;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            color: #ffff00;
            font-family: 'Sour Gummy', cursive;
            font-size: clamp(2.5rem, 6vw, 4rem);
            font-weight: bold;
            text-align: center;
            z-index: 100;
            text-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 20px #ff0, 0 0 30px #ff0, 0 0 40px #ff0;
        }
        #particle-container {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
            pointer-events: none; z-index: 99;
        }
        .particle {
            position: absolute; background-color: rgba(255, 221, 0, 0.8);
            border-radius: 50%; opacity: 0;
            box-shadow: 0 0 8px rgba(255, 221, 0, 0.9), 0 0 12px rgba(255, 221, 0, 0.5);
            animation: particle-rise 6s ease-out infinite;
        }
        @keyframes particle-rise {
            0% { transform: translateY(0) scale(1); opacity: 1; }
            100% { transform: translateY(-30vh) scale(0); opacity: 0; }
        }
        #falling-flower-container {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
            pointer-events: none; z-index: 0; overflow: hidden;
        }
        .falling-flower-wrapper {
            position: absolute; top: -50px;
            animation: fallDown linear forwards;
            will-change: transform;
        }
        .falling-flower {
            position: relative;
            background-image: url('data:image/svg+xml;utf8,<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><path fill="%23FFD700" d="M50 0 L58.7 34.5 L90.5 25 L65.5 41.3 L99 61.8 L61.8 61.8 L75 90.5 L50 67 L25 90.5 L38.2 61.8 L1 61.8 L34.5 41.3 L9.5 25 L41.3 34.5 Z"/><circle cx="50" cy="50" r="20" fill="%23654321"/></svg>');
            background-size: contain; background-repeat: no-repeat;
            animation: sway ease-in-out infinite alternate;
            will-change: transform;
        }
        @keyframes fallDown {
            from { transform: translateY(0); opacity: 1; }
            to { transform: translateY(110vh); opacity: 0; }
        }
        @keyframes sway {
            from { transform: translateX(-25px) rotate(-45deg); }
            to { transform: translateX(25px) rotate(45deg); }
        }
        .night{display:none;}
        .flowers { position: relative; transform: scale(0.7); z-index: 2; }
        .flower { position: absolute; bottom: 10vmin; transform-origin: bottom center; z-index: 50; will-change: transform; }
        .flower--1 { animation: moving-flower-1 4s linear infinite; }
        .flower--1 .flower__line { height: 70vmin; animation-delay: 0.3s; }
        .flower--1 .flower__line__leaf--1 { animation: blooming-leaf-right var(--fl-speed) 1.6s backwards; }
        .flower--1 .flower__line__leaf--2 { animation: blooming-leaf-right var(--fl-speed) 1.4s backwards; }
        .flower--1 .flower__line__leaf--3 { animation: blooming-leaf-left var(--fl-speed) 1.2s backwards; }
        .flower--1 .flower__line__leaf--4 { animation: blooming-leaf-left var(--fl-speed) 1s backwards; }
        .flower--2 { left: 50%; transform: rotate(20deg); animation: moving-flower-2 4s linear infinite; }
        .flower--2 .flower__line { height: 50vmin; animation-delay: 0.6s; }
        .flower--2 .flower__line__leaf--1 { animation: blooming-leaf-right var(--fl-speed) 1.9s backwards; }
        .flower--2 .flower__line__leaf--2 { animation: blooming-leaf-right var(--fl-speed) 1.7s backwards; }
        .flower--2 .flower__line__leaf--3 { animation: blooming-leaf-left var(--fl-speed) 1.5s backwards; }
        .flower--2 .flower__line__leaf--4 { animation: blooming-leaf-left var(--fl-speed) 1.3s backwards; }
        .flower--3 { left: 50%; transform: rotate(-15deg); animation: moving-flower-3 4s linear infinite; }
        .flower--3 .flower__line { animation-delay: 0.9s; }
        .flower--3 .flower__line__leaf--1 { animation: blooming-leaf-right var(--fl-speed) 2.5s backwards; }
        .flower--3 .flower__line__leaf--2 { animation: blooming-leaf-right var(--fl-speed) 2.3s backwards; }
        .flower--3 .flower__line__leaf--3 { animation: blooming-leaf-left var(--fl-speed) 2.1s backwards; }
        .flower--3 .flower__line__leaf--4 { animation: blooming-leaf-left var(--fl-speed) 1.9s backwards; }
        .flower--4 { left: -25%; z-index: -6; transform: rotate(10deg); animation: moving-flower-4 3.5s linear infinite; }
        .flower--4 .flower__line { height: 95vmin; animation-delay: 1.2s; }
        .flower--4 .flower__line__leaf--1 { animation: blooming-leaf-right var(--fl-speed) 2.8s backwards; }
        .flower--4 .flower__line__leaf--2 { animation: blooming-leaf-right var(--fl-speed) 2.6s backwards; }
        .flower--4 .flower__line__leaf--3 { animation: blooming-leaf-left var(--fl-speed) 2.4s backwards; }
        .flower--4 .flower__line__leaf--4 { animation: blooming-leaf-left var(--fl-speed) 2.2s backwards; }
        .flower--5 { left: 75%; z-index: -7; transform: rotate(-25deg); animation: moving-flower-5 4.5s linear infinite; }
        .flower--5 .flower__line { height: 93vmin; animation-delay: 1.9s; }
        .flower--5 .flower__line__leaf--1 { animation: blooming-leaf-right var(--fl-speed) 2.7s backwards; }
        .flower--5 .flower__line__leaf--2 { animation: blooming-leaf-right var(--fl-speed) 2.5s backwards; }
        .flower--5 .flower__line__leaf--3 { animation: blooming-leaf-left var(--fl-speed) 2.3s backwards; }
        .flower--5 .flower__line__leaf--4 { animation: blooming-leaf-left var(--fl-speed) 2.1s backwards; }
        .flower--6 { left: -40%; z-index: -8; transform: rotate(-30deg); animation: moving-flower-6 5s linear infinite; }
        .flower--6 .flower__line { height: 80vmin; animation-delay: 2.2s; }
        .flower--6 .flower__leafs { animation-delay: 2.3s; }
        .flower--6 .flower__line__leaf--1 { animation: blooming-leaf-right var(--fl-speed) 2.9s backwards; }
        .flower--6 .flower__line__leaf--2 { animation: blooming-leaf-right var(--fl-speed) 2.7s backwards; }
        .flower--6 .flower__line__leaf--3 { animation: blooming-leaf-left var(--fl-speed) 2.5s backwards; }
        .flower--6 .flower__line__leaf--4 { animation: blooming-leaf-left var(--fl-speed) 2.4s backwards; }
        .flower--7 { left: 90%; z-index: -9; transform: rotate(15deg); animation: moving-flower-7 4.8s linear infinite; }
        .flower--7 .flower__line { height: 80vmin; animation-delay: 2.5s; }
        .flower--7 .flower__leafs { animation-delay: 2.6s; }
        .flower--7 .flower__line__leaf--1 { animation: blooming-leaf-right var(--fl-speed) 3.2s backwards; }
        .flower--7 .flower__line__leaf--2 { animation: blooming-leaf-right var(--fl-speed) 3.0s backwards; }
        .flower--7 .flower__line__leaf--3 { animation: blooming-leaf-left var(--fl-speed) 2.8s backwards; }
        .flower--7 .flower__line__leaf--4 { animation: blooming-leaf-left var(--fl-speed) 2.7s backwards; }
        .flower__leafs { position: relative; animation: blooming-flower 2s backwards; }
        .flower__leafs--1 { animation-delay: 1.1s; }
        .flower__leafs--2 { animation-delay: 1.4s; }
        .flower__leafs--3 { animation-delay: 1.7s; }
        .flower__leafs--4 { animation-delay: 2.0s; }
        .flower__leafs--5 { animation-delay: 2.0s; }
        .flower__leafs::after { content: ""; position: absolute; left: 0; top: 0; transform: translate(-50%, -100%); width: 8vmin; height: 8vmin; background-color: #6bf0ff; filter: blur(10vmin); }
        .flower__leaf {
            position: absolute; bottom: 0; left: 50%; width: 23vmin; height: 6vmin;  border-radius: 10% 100% 10% 100%; 
            background-color: var(--petal-gradient-mid);
            background-image: linear-gradient(to top, var(--petal-gradient-start), var(--petal-gradient-mid), var(--petal-gradient-end));
            transform-origin: bottom center; opacity: 0.95;
            box-shadow: inset 0 0 1vmin rgba(255, 255, 255, 0.7), 0 0 3vmin var(--petal-shadow); z-index: 2;
        }
        .flower__white-circle {
            position: absolute; left: -4vmin; top: -4vmin; width: 10vmin; height: 10vmin; border-radius: 50%;
            background-color: var(--center-color-2);
            background-image: radial-gradient(circle at 30% 30%, var(--center-color-1), var(--center-color-2), var(--center-color-3));
            box-shadow: inset 0 0 2vmin rgba(0, 0, 0, 0.8), 0 0 1vmin var(--center-shadow);
        }
        .flower__white-circle::after {
            content: ""; position: absolute; left: 46%; top: 31%; transform: translate(-50%, -50%); width: 80%; height: 80%;
            z-index: 3; border-radius: inherit;
            background-image: repeating-conic-gradient(from 0deg, var(--center-color-3) 0deg 15deg, var(--center-color-1) 15deg 30deg),
                              radial-gradient(circle at center, var(--center-color-2), var(--center-color-1));
        }
        .flower__line {
            height: 55vmin; width: 2vmin;
            background-image: linear-gradient(to left, rgb(0, 0, 0, 0.3), transparent, rgba(255, 255, 255, 0.2)),
                              linear-gradient(to top, transparent 10%, var(--stem-gradient-1), var(--stem-gradient-2), var(--stem-gradient-3));
            box-shadow: inset 0 0 2px rgba(0, 0, 0, 0.7); animation: grow-flower-tree 4s backwards;
        }
        .flower__line__leaf {
            --w: 8vmin; --h: calc(var(--w) + 3vmin); position: absolute; top: 20%; left: 90%; width: var(--w); height: var(--h);
            border-top-right-radius: var(--h); border-bottom-left-radius: var(--h);
            background-image: linear-gradient(to top, var(--leaf-gradient-1), var(--leaf-gradient-2), var(--leaf-gradient-3));
            box-shadow: inset 0 0 1vmin rgba(0, 0, 0, 0.3);
        }
        .flower__line__leaf--1 { transform: rotate(70deg) rotateY(30deg); }
        .flower__line__leaf--2 { top: 45%; transform: rotate(70deg) rotateY(30deg); }
        .flower__line__leaf--3, .flower__line__leaf--4 {
            border-top-right-radius: 0; border-bottom-left-radius: 0; border-top-left-radius: var(--h);
            border-bottom-right-radius: var(--h); left: -460%; top: 12%; transform: rotate(-70deg) rotateY(30deg);
        }
        .flower__line__leaf--4 { top: 40%; }
        .flower__light {
            position: absolute; bottom: 0vmin; width: 0.8vmin; height: 0.8vmin;
            background-color: var(--light-seeds-1); border-radius: 50%; filter: blur(0.1vmin);
            animation: sunflower-seeds 6s linear infinite backwards; box-shadow: 0 0 1vmin var(--light-seeds-shadow);
        }
        .flower__light:nth-child(odd) { background-color: var(--light-seeds-2); }
        .flower__light--1 { left: -2vmin; animation-delay: 1s; } .flower__light--2 { left: 3vmin; animation-delay: 0.5s; }
        .flower__light--3 { left: -6vmin; animation-delay: 0.3s; } .flower__light--4 { left: 6vmin; animation-delay: 0.9s; }
        .flower__light--5 { left: -1vmin; animation-delay: 1.5s; } .flower__light--6 { left: -4vmin; animation-delay: 3s; }
        .flower__light--7 { left: 3vmin; animation-delay: 2s; } .flower__light--8 { left: -6vmin; animation-delay: 3.5s; }
        .flower__grass {
            --c: var(--grass-color); 
            --line-w: 2.5vmin;
            position: absolute; 
            bottom: 10vmin;
            left: 0;
            display: flex; 
            flex-direction: column; 
            align-items: flex-end; 
            z-index: 20;
            transform-origin: bottom center; 
            transform: rotate(-48deg) rotateY(40deg);
            will-change: transform;
        }
        .flower__grass--1 { animation: moving-grass 2s linear infinite; }
        .flower__grass--2 { transform: scale(0.9) rotate(75deg) rotateX(10deg) rotateY(-200deg); opacity: 0.8; z-index: 0; animation: moving-grass--2 1.5s linear infinite; }
        .flower__grass--3 { transform: scale(1.1) rotate(-30deg) rotateY(45deg); opacity: 0.9; z-index: 15; animation: moving-grass--3 2.2s linear infinite; }
        .flower__grass--4 { transform: scale(1.0) rotate(60deg) rotateX(15deg) rotateY(-180deg); opacity: 0.7; z-index: 5; animation: moving-grass--4 1.8s linear infinite; }
        .flower__grass--5 { transform: scale(1.1) rotate(-60deg) rotateY(60deg); opacity: 0.85; z-index: 12; animation: moving-grass--5 2.5s linear infinite; }
        .flower__grass--6 { transform: scale(0.95) rotate(35deg) rotateY(-45deg); opacity: 0.9; z-index: 15; animation: moving-grass--6 2.3s linear infinite; }
        .flower__grass--7 { transform: scale(0.85) rotate(-70deg) rotateX(20deg) rotateY(170deg); opacity: 0.75; z-index: 8; animation: moving-grass--7 1.9s linear infinite; }
        .flower__grass--8 { transform: scale(0.9) rotate(50deg) rotateY(-70deg); opacity: 0.8; z-index: 10; animation: moving-grass--8 2.1s linear infinite; }
        .flower__grass--9 { transform: scale(1.2) rotate(20deg) rotateY(90deg); opacity: 0.6; z-index: 2; animation: moving-grass--9 1.6s linear infinite; }
        .flower__grass--10 { transform: scale(0.8) rotate(-45deg) rotateY(-120deg); opacity: 0.65; z-index: 3; animation: moving-grass--10 2.0s linear infinite; }
        .flower__grass--top { 
            width: 10vmin; 
            height: 14vmin; 
            border-top-right-radius: 100%; 
            border-right: var(--line-w) solid var(--c); 
            transform-origin: bottom center; 
            transform: rotate(-2deg); 
        }
        .flower__grass--bottom { 
            margin-top: -2px; 
            width: var(--line-w); 
            height: 35vmin;
            background-image: linear-gradient(to top, transparent, var(--c)); 
        }
        .flower__grass__leaf {
            --size: 10vmin; 
            position: absolute; 
            width: calc(var(--size) * 2.1); 
            height: var(--size);
            border-top-left-radius: var(--size); 
            border-top-right-radius: var(--size);
            background-image: linear-gradient(to top, transparent, transparent 30%, var(--c)); 
            z-index: 100;
        }
        .flower__grass__leaf--1 { top: -6%; left: 20%; --size: 8vmin; transform: rotate(-20deg); animation: growing-grass-ans--1 var(--speed-leaf) 2.6s backwards; }
        .flower__grass__leaf--2 { top: -5%; left: -75%; --size: 9vmin; transform: rotate(10deg); animation: growing-grass-ans--2 var(--speed-leaf) 2.4s linear backwards; }
        .flower__grass__leaf--3 { top: 5%; left: 40%; --size: 10vmin; transform: rotate(-18deg) rotateX(-20deg); animation: growing-grass-ans--3 var(--speed-leaf) 2.2s linear backwards; }
        .flower__grass__leaf--4 { top: 6%; left: -95%; --size: 12vmin; transform: rotate(2deg); animation: growing-grass-ans--4 var(--speed-leaf) 2s linear backwards; }
        .flower__grass__leaf--5 { top: 20%; left: 40%; --size: 12vmin; transform: rotate(-24deg) rotateX(-20deg); animation: growing-grass-ans--5 var(--speed-leaf) 1.8s linear backwards; }
        .flower__grass__leaf--6 { top: 22%; left: -130%; --size: 15vmin; transform: rotate(10deg); animation: growing-grass-ans--6 var(--speed-leaf) 1.6s linear backwards; }
        .flower__grass__leaf--7 { top: 39%; left: 50%; --size: 12vmin; transform: rotate(-10deg); animation: growing-grass-ans--7 var(--speed-leaf) 1.4s linear backwards; }
        .flower__grass__leaf--8 { top: 40%; left: -160%; --size: 16vmin; transform: rotate(10deg); animation: growing-grass-ans--8 var(--speed-leaf) 1.2s linear backwards; }
        .flower__grass__overlay { 
            position: absolute; 
            top: -10%; 
            right: 0%; 
            width: 100%; 
            height: 100%; 
            background-color: rgba(0, 0, 0, 0.193); 
            filter: blur(1.5vmin); 
            z-index: 100; 
        }
        .special-text{display: none;}
        .grow-ans { animation: grow-ans 2s var(--d) backwards; }
        .growing-grass { animation: growing-grass-ans 1s 2s backwards; }
        .not-loaded * { animation-play-state: paused !important; }
        @keyframes grow-ans { from { transform: scale(0); opacity: 0; } }
        @keyframes growing-grass-ans { from { transform: scale(0); } }
        @keyframes growing-grass-ans--1 { from { transform-origin: bottom left; transform: rotate(-20deg) scale(0); } }
        @keyframes growing-grass-ans--2 { from { transform-origin: bottom right; transform: rotate(10deg) scale(0); } }
        @keyframes growing-grass-ans--3 { from { transform-origin: bottom left; transform: rotate(-18deg) rotateX(-20deg) scale(0); } }
        @keyframes growing-grass-ans--4 { from { transform-origin: bottom right; transform: rotate(2deg) scale(0); } }
        @keyframes growing-grass-ans--5 { from { transform-origin: bottom left; transform: rotate(-24deg) rotateX(-20deg) scale(0); } }
        @keyframes growing-grass-ans--6 { from { transform-origin: bottom right; transform: rotate(10deg) scale(0); } }
        @keyframes growing-grass-ans--7 { from { transform-origin: bottom left; transform: rotate(-10deg) scale(0); } }
        @keyframes growing-grass-ans--8 { from { transform-origin: bottom right; transform: rotate(10deg) scale(0); } }
        @keyframes sunflower-seeds { from { opacity: 0; transform: translateY(0vmin) rotate(0deg); } 20% { opacity: 1; transform: translateY(-3vmin) translateX(-1vmin) rotate(45deg); } 40% { opacity: 1; transform: translateY(-8vmin) translateX(1vmin) rotate(90deg); } 60% { transform: translateY(-12vmin) translateX(-1vmin) rotate(135deg); } 80% { transform: translateY(-16vmin) translateX(2vmin) rotate(180deg); opacity: 0.5; } to { transform: translateY(-25vmin) rotate(225deg); opacity: 0; } }
        @keyframes moving-flower-1 { from, to { transform: rotate(2deg); } 50% { transform: rotate(-2deg); } }
        @keyframes moving-flower-2 { from, to { transform: rotate(18deg); } 50% { transform: rotate(14deg); } }
        @keyframes moving-flower-3 { from, to { transform: rotate(-18deg); } 50% { transform: rotate(-20deg) rotateY(-10deg); } }
        @keyframes moving-flower-4 { from, to { transform: rotate(9deg); } 50% { transform: rotate(12deg) rotateY(9deg); } }
        @keyframes moving-flower-5 { from, to { transform: rotate(-5deg); } 50% { transform: rotate(-8deg) rotateY(5deg); } }
        @keyframes moving-flower-6 { from, to { transform: rotate(-20deg); } 50% { transform: rotate(-24deg) rotateY(-8deg); } }
        @keyframes moving-flower-7 { from, to { transform: rotate(22deg); } 50% { transform: rotate(25deg) rotateY(10deg); } }
        @keyframes blooming-leaf-right { from { transform-origin: left; transform: rotate(70deg) rotateY(30deg) scale(0); } }
        @keyframes blooming-leaf-left { from { transform-origin: right; transform: rotate(-70deg) rotateY(30deg) scale(0); } }
        @keyframes grow-flower-tree { from { height: 0; border-radius: 1vmin; } }
        @keyframes blooming-flower { from { transform: scale(0); } }
        @keyframes moving-grass { from, to { transform: rotate(-48deg) rotateY(40deg); } 50% { transform: rotate(-50deg) rotateY(40deg); } }
        @keyframes moving-grass--2 { from, to { transform: scale(0.5) rotate(75deg) rotateX(10deg) rotateY(-200deg); } 50% { transform: scale(0.5) rotate(79deg) rotateX(10deg) rotateY(-200deg); } }
        @keyframes moving-grass--3 { from, to { transform: scale(0.7) rotate(-30deg) rotateY(45deg); } 50% { transform: scale(0.7) rotate(-33deg) rotateY(50deg); } }
        @keyframes moving-grass--4 { from, to { transform: scale(0.4) rotate(60deg) rotateX(15deg) rotateY(-180deg); } 50% { transform: scale(0.4) rotate(63deg) rotateX(18deg) rotateY(-175deg); } }
        @keyframes moving-grass--5 { from, to { transform: scale(0.6) rotate(-60deg) rotateY(60deg); } 50% { transform: scale(0.6) rotate(-57deg) rotateY(65deg); } }
        @keyframes moving-grass--6 { from, to { transform: scale(0.65) rotate(35deg) rotateY(-45deg); } 50% { transform: scale(0.65) rotate(38deg) rotateY(-40deg); } }
        @keyframes moving-grass--7 { from, to { transform: scale(0.45) rotate(-70deg) rotateX(20deg) rotateY(170deg); } 50% { transform: scale(0.45) rotate(-67deg) rotateX(23deg) rotateY(175deg); } }
        @keyframes moving-grass--8 { from, to { transform: scale(0.55) rotate(50deg) rotateY(-70deg); } 50% { transform: scale(0.55) rotate(53deg) rotateY(-65deg); } }
        @keyframes moving-grass--9 { from, to { transform: scale(0.3) rotate(20deg) rotateY(90deg); } 50% { transform: scale(0.3) rotate(23deg) rotateY(95deg); } }
        @keyframes moving-grass--10 { from, to { transform: scale(0.35) rotate(-45deg) rotateY(-120deg); } 50% { transform: scale(0.35) rotate(-42deg) rotateY(-115deg); } }
        @media (max-width: 768px) { .flowers { transform: scale(1.2); bottom: 35vmin} .love-title { font-size: 8vw; top: 15px;} }
        @media (max-width: 480px) { .flowers { transform: scale(0.9); bottom: 35vmin} .love-title { font-size: 10vw; top: 10px; } }
  </style>
</head>
<body class="not-loaded">
  <div id="falling-flower-container"></div>
  <div id="particle-container"></div>
  <h1 class="love-title">Estás Flores son para ti mi Mi Amor BRIYITH❤️</h1>
  <div class="flowers">
    <!-- El contenido HTML de las flores no ha cambiado -->
    <div class="flower flower--1">
      <div class="flower__leafs flower__leafs--1">
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(0deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(30deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(60deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(90deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(120deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(150deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(180deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(210deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(240deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(270deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(300deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(330deg);"></div>
        <div class="flower__white-circle"></div>
        <div class="flower__light flower__light--1"></div>
        <div class="flower__light flower__light--2"></div>
        <div class="flower__light flower__light--3"></div>
        <div class="flower__light flower__light--4"></div>
        <div class="flower__light flower__light--5"></div>
        <div class="flower__light flower__light--6"></div>
        <div class="flower__light flower__light--7"></div>
        <div class="flower__light flower__light--8"></div>
      </div>
      <div class="flower__line">
        <div class="flower__line__leaf flower__line__leaf--1">
        </div>
        <div class="flower__line__leaf flower__line__leaf--2">
        </div>
        <div class="flower__line__leaf flower__line__leaf--3">
        </div>
        <div class="flower__line__leaf flower__line__leaf--4">
        </div>
      </div>
    </div>
    <div class="flower flower--2">
      <div class="flower__leafs flower__leafs--2">
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(0deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(30deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(60deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(90deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(120deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(150deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(180deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(210deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(240deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(270deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(300deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(330deg);"></div>
        <div class="flower__white-circle"></div>
        <div class="flower__light flower__light--1"></div>
        <div class="flower__light flower__light--2"></div>
        <div class="flower__light flower__light--3"></div>
        <div class="flower__light flower__light--4"></div>
        <div class="flower__light flower__light--5"></div>
        <div class="flower__light flower__light--6"></div>
        <div class="flower__light flower__light--7"></div>
        <div class="flower__light flower__light--8"></div>
      </div>
      <div class="flower__line">
        <div class="flower__line__leaf flower__line__leaf--1">
        </div>
        <div class="flower__line__leaf flower__line__leaf--2">
        </div>
        <div class="flower__line__leaf flower__line__leaf--3">
        </div>
        <div class="flower__line__leaf flower__line__leaf--4">
        </div>
      </div>
    </div>
    <div class="flower flower--3">
      <div class="flower__leafs flower__leafs--3">
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(0deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(30deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(60deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(90deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(120deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(150deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(180deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(210deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(240deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(270deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(300deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(330deg);"></div>
        <div class="flower__white-circle"></div>
        <div class="flower__light flower__light--1"></div>
        <div class="flower__light flower__light--2"></div>
        <div class="flower__light flower__light--3"></div>
        <div class="flower__light flower__light--4"></div>
        <div class="flower__light flower__light--5"></div>
        <div class="flower__light flower__light--6"></div>
        <div class="flower__light flower__light--7"></div>
        <div class="flower__light flower__light--8"></div>
      </div>
      <div class="flower__line">
        <div class="flower__line__leaf flower__line__leaf--1">
        </div>
        <div class="flower__line__leaf flower__line__leaf--2">
        </div>
        <div class="flower__line__leaf flower__line__leaf--3">
        </div>
        <div class="flower__line__leaf flower__line__leaf--4">
        </div>
      </div>
    </div>
    <div class="flower flower--4">
      <div class="flower__leafs flower__leafs--4">
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(0deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(30deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(60deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(90deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(120deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(150deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(180deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(210deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(240deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(270deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(300deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(330deg);"></div>
        <div class="flower__white-circle"></div>
        <div class="flower__light flower__light--1"></div>
        <div class="flower__light flower__light--2"></div>
        <div class="flower__light flower__light--3"></div>
        <div class="flower__light flower__light--4"></div>
        <div class="flower__light flower__light--5"></div>
        <div class="flower__light flower__light--6"></div>
        <div class="flower__light flower__light--7"></div>
        <div class="flower__light flower__light--8"></div>
      </div>
      <div class="flower__line">
        <div class="flower__line__leaf flower__line__leaf--1">
        </div>
        <div class="flower__line__leaf flower__line__leaf--2">
        </div>
        <div class="flower__line__leaf flower__line__leaf--3">
        </div>
        <div class="flower__line__leaf flower__line__leaf--4">
        </div>
      </div>
    </div>
    <div class="flower flower--5">
      <div class="flower__leafs flower__leafs--5">
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(0deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(30deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(60deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(90deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(120deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(150deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(180deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(210deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(240deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(270deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(300deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(330deg);"></div>
        <div class="flower__white-circle"></div>
        <div class="flower__light flower__light--1"></div>
        <div class="flower__light flower__light--2"></div>
        <div class="flower__light flower__light--3"></div>
        <div class="flower__light flower__light--4"></div>
        <div class="flower__light flower__light--5"></div>
        <div class="flower__light flower__light--6"></div>
        <div class="flower__light flower__light--7"></div>
        <div class="flower__light flower__light--8"></div>
      </div>
      <div class="flower__line">
        <div class="flower__line__leaf flower__line__leaf--1">
        </div>
        <div class="flower__line__leaf flower__line__leaf--2">
        </div>
        <div class="flower__line__leaf flower__line__leaf--3">
        </div>
        <div class="flower__line__leaf flower__line__leaf--4">
        </div>
      </div>
    </div>
    <div class="flower flower--6">
      <div class="flower__leafs">
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(0deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(30deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(60deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(90deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(120deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(150deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(180deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(210deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(240deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(270deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(300deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(330deg);"></div>
        <div class="flower__white-circle"></div>
        <div class="flower__light flower__light--1"></div>
        <div class="flower__light flower__light--2"></div>
        <div class="flower__light flower__light--3"></div>
        <div class="flower__light flower__light--4"></div>
      </div>
      <div class="flower__line">
        <div class="flower__line__leaf flower__line__leaf--1">
        </div>
        <div class="flower__line__leaf flower__line__leaf--2">
        </div>
        <div class="flower__line__leaf flower__line__leaf--3">
        </div>
        <div class="flower__line__leaf flower__line__leaf--4">
        </div>
      </div>
    </div>
    <div class="flower flower--7">
      <div class="flower__leafs">
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(0deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(30deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(60deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(90deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(120deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(150deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(180deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(210deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(240deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(270deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(300deg);"></div>
        <div class="flower__leaf" style=
        "transform: translate(-50%, -10%) rotate(330deg);"></div>
        <div class="flower__white-circle"></div>
        <div class="flower__light flower__light--1"></div>
        <div class="flower__light flower__light--2"></div>
        <div class="flower__light flower__light--3"></div>
        <div class="flower__light flower__light--4"></div>
      </div>
      <div class="flower__line">
        <div class="flower__line__leaf flower__line__leaf--1">
        </div>
        <div class="flower__line__leaf flower__line__leaf--2">
        </div>
        <div class="flower__line__leaf flower__line__leaf--3">
        </div>
        <div class="flower__line__leaf flower__line__leaf--4">
        </div>
      </div>
    </div>
    <div class="grow-ans" style="--d:1.2s">
      <div class="flower__g-long">
        <div class="flower__g-long__top"></div>
        <div class="flower__g-long__bottom"></div>
      </div>
    </div>
    <div class="growing-grass">
      <div class="flower__grass flower__grass--1">
        <div class="flower__grass--top"></div>
        <div class="flower__grass--bottom"></div>
        <div class="flower__grass__leaf flower__grass__leaf--1">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--2">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--3">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--4">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--5">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--6">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--7">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--8">
        </div>
        <div class="flower__grass__overlay"></div>
      </div>
    </div>
    <div class="growing-grass">
      <div class="flower__grass flower__grass--2">
        <div class="flower__grass--top"></div>
        <div class="flower__grass--bottom"></div>
        <div class="flower__grass__leaf flower__grass__leaf--1">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--2">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--3">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--4">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--5">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--6">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--7">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--8">
        </div>
        <div class="flower__grass__overlay"></div>
      </div>
    </div>
    <div class="growing-grass">
      <div class="flower__grass flower__grass--3">
        <div class="flower__grass--top"></div>
        <div class="flower__grass--bottom"></div>
        <div class="flower__grass__leaf flower__grass__leaf--1">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--2">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--3">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--4">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--5">
        </div>
        <div class="flower__grass__overlay"></div>
      </div>
    </div>
    <div class="growing-grass">
      <div class="flower__grass flower__grass--4">
        <div class="flower__grass--top"></div>
        <div class="flower__grass--bottom"></div>
        <div class="flower__grass__leaf flower__grass__leaf--1">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--2">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--3">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--4">
        </div>
        <div class="flower__grass__overlay"></div>
      </div>
    </div>
    <div class="growing-grass">
      <div class="flower__grass flower__grass--5">
        <div class="flower__grass--top"></div>
        <div class="flower__grass--bottom"></div>
        <div class="flower__grass__leaf flower__grass__leaf--1">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--2">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--3">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--4">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--5">
        </div>
        <div class="flower__grass__overlay"></div>
      </div>
    </div>
    <div class="growing-grass">
      <div class="flower__grass flower__grass--6">
        <div class="flower__grass--top"></div>
        <div class="flower__grass--bottom"></div>
        <div class="flower__grass__leaf flower__grass__leaf--1">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--2">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--3">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--4">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--5">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--6">
        </div>
        <div class="flower__grass__overlay"></div>
      </div>
    </div>
    <div class="growing-grass">
      <div class="flower__grass flower__grass--7">
        <div class="flower__grass--top"></div>
        <div class="flower__grass--bottom"></div>
        <div class="flower__grass__leaf flower__grass__leaf--1">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--2">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--3">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--4">
        </div>
        <div class="flower__grass__overlay"></div>
      </div>
    </div>
    <div class="growing-grass">
      <div class="flower__grass flower__grass--8">
        <div class="flower__grass--top"></div>
        <div class="flower__grass--bottom"></div>
        <div class="flower__grass__leaf flower__grass__leaf--1">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--2">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--3">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--4">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--5">
        </div>
        <div class="flower__grass__overlay"></div>
      </div>
    </div>
    <div class="growing-grass">
      <div class="flower__grass flower__grass--9">
        <div class="flower__grass--top"></div>
        <div class="flower__grass--bottom"></div>
        <div class="flower__grass__leaf flower__grass__leaf--1">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--2">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--3">
        </div>
        <div class="flower__grass__overlay"></div>
      </div>
    </div>
    <div class="growing-grass">
      <div class="flower__grass flower__grass--10">
        <div class="flower__grass--top"></div>
        <div class="flower__grass--bottom"></div>
        <div class="flower__grass__leaf flower__grass__leaf--1">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--2">
        </div>
        <div class="flower__grass__leaf flower__grass__leaf--3">
        </div>
        <div class="flower__grass__overlay"></div>
      </div>
    </div>
  </div>
  <script>
  // --- ROBUST CONSOLE & SHORTCUT BLOCKER ---
  (function() {
      // Block right-click context menu
      document.addEventListener('contextmenu', event => event.preventDefault());
      // Block key combinations
      document.addEventListener('keydown', function(e) {
          if (
              e.key === 'F12' ||
              (e.ctrlKey && e.shiftKey && ['I', 'J', 'C'].includes(e.key.toUpperCase())) ||
              (e.ctrlKey && ['U', 'S'].includes(e.key.toUpperCase()))
          ) {
              e.preventDefault();
          }
      });
      // --- Aggressive DevTools blocking using a debugger loop ---
      const devToolsTrap = () => {
          debugger;
      };
      // Run the trap at a high frequency
      setInterval(devToolsTrap, 50);
  })();
  // --- MAIN APPLICATION LOGIC (Music Player Removed) ---
  document.addEventListener('DOMContentLoaded', function() {
      // Initial load animation
      setTimeout(() => {
          document.body.classList.remove("not-loaded");
      }, 1000);
      // --- ANIMATION OPTIMIZATION ---
      const particleContainer = document.getElementById('particle-container');
      const fallingContainer = document.getElementById('falling-flower-container');
      let lastParticleTime = 0;
      let lastFlowerTime = 0;
      const particleInterval = 100;
      const flowerInterval = 250;
      function animationLoop(timestamp) {
          if (timestamp - lastParticleTime > particleInterval) {
              createParticle(Math.random() * window.innerWidth, Math.random() * window.innerHeight);
              createParticle((window.innerWidth / 2) + (Math.random() - 0.5) * 400, (window.innerHeight / 3) + (Math.random() - 0.5) * 300);
              lastParticleTime = timestamp;
          }
          if (timestamp - lastFlowerTime > flowerInterval) {
              createFallingFlower();
              lastFlowerTime = timestamp;
          }
          requestAnimationFrame(animationLoop);
      }
      function createParticle(x, y) {
          if (!particleContainer) return;
          const particle = document.createElement('div');
          particle.className = 'particle';
          const size = Math.random() * 6 + 2;
          particle.style.cssText = `width: ${size}px; height: ${size}px; left: ${x}px; top: ${y}px; animation-delay: ${Math.random() * 6}s;`;
          particleContainer.appendChild(particle);
          setTimeout(() => particle.remove(), (6 + parseFloat(particle.style.animationDelay)) * 1000);
      }
      function createFallingFlower() {
          if (!fallingContainer) return;
          const flowerWrapper = document.createElement('div');
          flowerWrapper.className = 'falling-flower-wrapper';
          const flower = document.createElement('div');
          flower.className = 'falling-flower';
          const animDuration = Math.random() * 8 + 7;
          const size = Math.random() * 30 + 10;
          flowerWrapper.style.left = Math.random() * 95 + 'vw';
          flowerWrapper.style.animationDuration = animDuration + 's';
          flower.style.animationDuration = (Math.random() * 2 + 3) + 's';
          flower.style.width = size + 'px';
          flower.style.height = size + 'px';
          flower.style.filter = `blur(${Math.random() * 2}px)`;
          flower.style.opacity = Math.random() * 0.5 + 0.5;
          flowerWrapper.appendChild(flower);
          fallingContainer.appendChild(flowerWrapper);
          setTimeout(() => flowerWrapper.remove(), animDuration * 1000 + 500);
      }
      // Start the optimized animation loop
      requestAnimationFrame(animationLoop);
  });
  </script>
</body>
</html>
