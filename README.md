<!DOCTYPE html><html lang="uz">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fargona Gap Sayt</title>
  <style>
    body {
      font-family: sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      background: #f0f8ff;
    }
    h1 {
      color: #333;
    }
    .buttons {
      display: grid;
      grid-template-columns: repeat(2, 120px);
      gap: 10px;
      margin-top: 20px;
    }
    button {
      padding: 20px;
      font-size: 24px;
      border: none;
      background-color: #87cefa;
      border-radius: 10px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    button:hover {
      background-color: #4682b4;
      color: white;
    }
    #result {
      margin-top: 20px;
      font-size: 20px;
      font-weight: bold;
      color: #006400;
    }
  </style>
</head>
<body>
  <h1>Raqamni tanlang</h1>
  <div class="buttons" id="buttonContainer"></div>
  <div id="result"></div>  <script>
    const buttonContainer = document.getElementById('buttonContainer');
    const resultDiv = document.getElementById('result');

    // Tasodifiy to'g'ri tugmani tanlaymiz
    const correctButton = Math.floor(Math.random() * 10) + 1;

    for (let i = 1; i <= 10; i++) {
      const btn = document.createElement('button');
      btn.textContent = i;
      btn.onclick = () => {
        if (i === correctButton) {
          resultDiv.textContent = "To'g'ri topdingiz!";
          resultDiv.style.color = '#008000';
        } else {
          resultDiv.textContent = "Xato! Yana urinib ko'ring.";
          resultDiv.style.color = '#b22222';
        }
      };
      buttonContainer.appendChild(btn);
    }
  </script></body>
</html>
