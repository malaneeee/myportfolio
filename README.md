<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Portfolio | Under Construction</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background: #f5f5f5;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      text-align: center;
      color: #333;
    }
    .container {
      background: #ffffff;
      padding: 40px;
      border-radius: 20px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.1);
    }
    h1 {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }
    p {
      font-size: 1.2rem;
      margin-bottom: 20px;
    }
    .loader {
      border: 6px solid #eee;
      border-top: 6px solid #333;
      border-radius: 50%;
      width: 40px;
      height: 40px;
      animation: spin 1s linear infinite;
      margin: 0 auto;
    }
    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }
      .countdown-container {
      margin-top: 20px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }
    .bar-bg {
      width: 80%;
      max-width: 400px;
      height: 18px;
      background: repeating-linear-gradient(45deg, #000 0 10px, #fff 10px 20px);
      border-radius: 20px;
      overflow: hidden;
      box-shadow: inset 0 0 10px rgba(0,0,0,0.2);
    }
    .bar-fill {
      height: 100%;
      width: 0%;
      background: rgba(0,0,0,0.3);
      border-radius: 20px;
      transition: width 0.5s ease-in-out;
    }
    .count-text {
      margin-top: 10px;
      font-size: 1rem;
      color: #555;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Portfolio Under Construction</h1>
    <p>I'm currently working on building my GitHub portfolio. Stay tuned!</p>
    <div class="countdown-container">
    <div class="bar-bg">
      <div class="bar-fill" id="bar"></div>
    </div>
  </div>
  </div>
  <div class="countdown-container">
    <div class="bar-bg">
      <div class="bar-fill" id="bar"></div>
    </div>
    
  </div>

  <script>
    const totalDays = 30;
    const startDate = new Date();

    function updateCountdown() {
      const now = new Date();
      const diff = (now - startDate) / (1000 * 60 * 60 * 24);
      const daysPassed = Math.min(diff, totalDays);
      const percentage = (daysPassed / totalDays) * 100;

      document.getElementById('bar').style.width = percentage + '%';

      // removed countdown text;
      // removed text update;
    }

    setInterval(updateCountdown, 1000 * 60 * 60);
    updateCountdown();
  </script>
</body>
</html>
