# Gin-s-Candy

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ultraman Ginga - Candy Time</title>
  <style>
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      overflow: hidden;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background: linear-gradient(to top, #87CEFA, #ffffff);
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      flex-direction: column;
    }

    #ginga {
      position: absolute;
      bottom: 0;
      opacity: 0;
      transform: scale(0.5);
      animation: showUp 2s ease-out forwards;
      animation-delay: 1s;
    }

    @keyframes showUp {
      to {
        opacity: 1;
        transform: scale(1);
      }
    }

    #hand {
      position: absolute;
      bottom: 200px;
      left: 50%;
      transform: translateX(-50%) scale(0);
      opacity: 0;
      animation: handExtend 2s ease-out forwards;
      animation-delay: 3s;
    }

    @keyframes handExtend {
      to {
        transform: translateX(-50%) scale(1);
        opacity: 1;
      }
    }

    #text {
      position: absolute;
      bottom: 50px;
      font-size: 2em;
      color: #ff1493;
      opacity: 0;
      animation: textPop 1s ease-out forwards;
      animation-delay: 5s;
    }

    @keyframes textPop {
      to {
        opacity: 1;
        transform: scale(1.1);
      }
    }

    .button-group {
      position: absolute;
      top: 20px;
      right: 20px;
      display: flex;
      gap: 10px;
    }

    .btn {
      padding: 10px 15px;
      border: none;
      border-radius: 8px;
      background-color: #ff1493;
      color: white;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.3s;
    }

    .btn:hover {
      background-color: #ff69b4;
    }

    .candy {
      position: absolute;
      width: 80px;
      animation: dropCandy 1s ease-out;
    }

    @keyframes dropCandy {
      from { transform: translateY(-100px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }
  </style>
</head>
<body>
  <div class="button-group">
    <button class="btn" onclick="addCandy()">Tambah Permen</button>
    <button class="btn" onclick="alert('Mode malam coming soon~')">Mode Malam</button>
    <button class="btn" onclick="location.reload()">Ulang Animasi</button>
  </div>

  <img id="ginga" src="Ginga.png" alt="Ultraman Ginga" width="300">
  <img id="hand" src="Hand.png" alt="Ultraman hand with candy" width="200">
  <div id="text">It's ur candy, babe!!</div>

  <script>
    function addCandy() {
      const candy = document.createElement('img');
      candy.src = 'Candy.png'; // dipersingkat untuk placeholder
      candy.className = 'candy';
      candy.style.left = Math.random() * (window.innerWidth - 100) + 'px';
      candy.style.top = Math.random() * (window.innerHeight - 200) + 'px';
      document.body.appendChild(candy);
    }
  </script>
</body>
</html>
