<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Valentine's Message for Loraine</title>
<style>
  body {
    margin: 0;
    height: 100vh;
    background: #ffdde1;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    font-family: 'Arial', sans-serif;
  }

  .container {
    text-align: center;
  }

  h1 {
    font-size: 3em;
    color: #e60073;
    margin-bottom: 20px;
    animation: pulse 1s infinite;
  }

  h2 {
    font-size: 2em;
    color: #ff3399;
    animation: floatText 2s ease-in-out infinite;
  }

  @keyframes pulse {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.2); }
  }

  @keyframes floatText {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-10px); }
  }

  .heart {
    position: absolute;
    width: 20px;
    height: 20px;
    background: #ff3399;
    transform: rotate(-45deg);
    animation: floatHeart 5s linear infinite;
  }

  .heart::before,
  .heart::after {
    content: "";
    position: absolute;
    width: 20px;
    height: 20px;
    background: #ff3399;
    border-radius: 50%;
  }

  .heart::before {
    top: -10px;
    left: 0;
  }

  .heart::after {
    top: 0;
    left: 10px;
  }

  @keyframes floatHeart {
    0% {
      transform: translateY(0) rotate(-45deg);
      opacity: 1;
    }
    100% {
      transform: translateY(-800px) rotate(-45deg);
      opacity: 0;
    }
  }
</style>
</head>
<body>

<div class="container">
  <h1>I Love You, Loraine 💖</h1>
  <h2>Happy Valentine's Day! 🌹</h2>
</div>

<script>
  // Create floating hearts
  function createHeart() {
    const heart = document.createElement('div');
    heart.classList.add('heart');
    heart.style.left = Math.random() * window.innerWidth + 'px';
    heart.style.width = heart.style.height = (10 + Math.random() * 30) + 'px';
    document.body.appendChild(heart);

    setTimeout(() => {
      heart.remove();
    }, 5000);
  }

  setInterval(createHeart, 300);
</script>

</body>
</html>
