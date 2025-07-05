<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>About Me - Jayson</title>
  <style>
    body {
      background: #0d1117;
      color: #c9d1d9;
      font-family: 'Fira Code', monospace;
      padding: 2rem;
      line-height: 1.6;
    }

    h1 {
      font-size: 2.5rem;
      color: #58a6ff;
    }

    .typewriter {
      font-size: 1.2rem;
      white-space: pre-line;
      border-right: 2px solid #58a6ff;
      width: 100%;
      max-width: 60ch;
      animation: blink 0.8s infinite;
    }

    @keyframes blink {
      50% { border-color: transparent; }
    }
  </style>
</head>
<body>
  <h1>👋 Hey, I'm Jayson</h1>
  <pre class="typewriter" id="type"></pre>

  <script>
    const lines = [
      "I'm a high school student with a love for robotics and coding.",
      "🛠️ I build robots using Java, WPILib, and real hardware.",
      "💡 I design circuits and 3D print parts for my projects.",
      "🧠 Currently exploring: simulation, VS Code workflows, and CAD.",
      "🔌 Future Master Electrician? You bet.",
      "📂 Check out my repos and feel free to reach out!"
    ];

    let i = 0, j = 0;
    const speed = 30;
    const el = document.getElementById("type");

    function typeLine() {
      if (i < lines.length) {
        if (j <= lines[i].length) {
          el.textContent = lines.slice(0, i).join('\n') + '\n' + lines[i].slice(0, j);
          j++;
          setTimeout(typeLine, speed);
        } else {
          i++;
          j = 0;
          setTimeout(typeLine, 500);
        }
      }
    }

    typeLine();
  </script>
</body>
</html>
