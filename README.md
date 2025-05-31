<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gin's Candy</title>
  <style>
    body {
      margin: 0;
      font-family: 'Courier New', monospace;
      background: url('background1.jpg') no-repeat center center fixed;
      background-size: cover;
      color: cyan;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    #start-screen, #candy-screen {
      position: absolute;
      text-align: center;
    }
    h1 {
      font-size: 3rem;
      text-shadow: 2px 2px 4px black;
    }
    button {
      padding: 1rem 2rem;
      font-size: 1.5rem;
      background: cyan;
      border: none;
      color: black;
      cursor: pointer;
      margin-top: 20px;
    }
    #ultraman {
      max-height: 70vh;
      display: none;
    }
    #text-reveal {
      font-size: 2rem;
      margin-top: 20px;
      color: #fff;
      display: none;
      text-shadow: 1px 1px 3px #000;
    }
  </style>
</head>
<body>
  <div id="start-screen">
    <h1>GIN'S CANDY</h1>
    <button onclick="startGame()">PLAY</button>
  </div>  <div id="candy-screen" style="display:none">
    <img id="ultraman" src="ginga1.png" alt="Ultraman Ginga">
    <div id="text-reveal">It's ur candy, babe!!</div>
  </div>  <script>
    function startGame() {
      document.getElementById('start-screen').style.display = 'none';
      document.body.style.backgroundImage = "url('background2.jpg')";
      document.getElementById('candy-screen').style.display = 'block';
      const ultraman = document.getElementById('ultraman');
      ultraman.style.display = 'block';

      // Delay buat ngeluarin teks dan ganti gambar
      setTimeout(() => {
        ultraman.src = 'ginga2.png'; // pose kasih permen
        document.getElementById('text-reveal').style.display = 'block';
      }, 1000);
    }
  </script></body>
</html>
