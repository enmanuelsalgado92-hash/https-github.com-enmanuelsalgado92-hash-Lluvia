<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Lluvia de Amor</title>
  <style>
    body {
      background-color: #000;
      overflow: hidden;
      margin: 0;
      font-family: 'Courier New', monospace;
    }
    .frase {
      position: absolute;
      color: red;
      font-size: 1.2em;
      animation: caer 5s linear infinite;
      white-space: nowrap;
    }
    @keyframes caer {
      0% { top: -50px; opacity: 0; }
      50% { opacity: 1; }
      100% { top: 100vh; opacity: 0; }
    }
  </style>
</head>
<body>
  <script>
    const frases = [
      "Te pienso en cada silencio.",
      "Tu amor me incendia suave.",
      "Eres mi caos favorito.",
      "Nosotros, aunque el mundo arda.",
      "Tu mirada me desarma lento.",
      "Amarte fue mi revolución."
    ];

    function crearFrase() {
      const frase = document.createElement("div");
      frase.className = "frase";
      frase.textContent = frases[Math.floor(Math.random() * frases.length)];
      frase.style.left = Math.random() * window.innerWidth + "px";
      document.body.appendChild(frase);
      setTimeout(() => frase.remove(), 5000);
    }

    setInterval(crearFrase, 500);
  </script>
</body>
</html>
