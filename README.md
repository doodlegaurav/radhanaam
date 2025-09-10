<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Radha Naam Jap Counter</title>
  <style>
    body {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      margin: 0;
      font-family: "Segoe UI", sans-serif;
      background: #fff8f9;
      padding: 20px;
      text-align: center;
    }

    #counter {
      font-size: clamp(2rem, 8vw, 4rem); /* responsive but safe */
      margin-bottom: 15px;
      color: #c2185b;
      font-weight: bold;
    }

    #chant {
      font-size: clamp(1.5rem, 6vw, 3rem);
      margin-bottom: 25px;
      color: #6a1b9a;
      font-weight: bold;
      min-height: 2rem;
      transition: opacity 0.3s ease-in-out;
    }

    button {
      width: 80%;
      max-width: 280px;
      padding: 16px;
      font-size: clamp(1.5rem, 5vw, 2.2rem); /* safe scaling */
      cursor: pointer;
      border: none;
      border-radius: 16px;
      background: linear-gradient(135deg, #ec407a, #d81b60);
      color: white;
      font-weight: bold;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
      transition: transform 0.15s;
      white-space: nowrap; /* prevents breaking */
    }

    button:active {
      transform: scale(0.95);
    }
  </style>
</head>
<body>
  <div id="counter">0</div>
  <div id="chant"></div>
  <button onclick="chantRadha()">Radha</button>

  <script>
    let count = 0;
    function chantRadha() {
      count++;
      document.getElementById("counter").innerText = count;
      const chantDiv = document.getElementById("chant");
      chantDiv.style.opacity = 0;
      setTimeout(() => {
        chantDiv.innerText = "Radha ✨";
        chantDiv.style.opacity = 1;
      }, 150);
    }
  </script>
</body>
</html>
