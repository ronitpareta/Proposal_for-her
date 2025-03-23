# Proposal_for-her
My Dear Love..
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>For the Love of My Life</title>
  <style>
    /* General Styles */
    body {
      margin: 0;
      padding: 0;
      font-family: 'Arial', sans-serif;
      background: linear-gradient(to bottom right, #ff9a9e, #fad0c4);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
      text-align: center;
      color: #fff;
      position: relative;
    }
    .container {
      position: relative;
      z-index: 2;
    }
    h1 {
      font-size: 48px;
      margin-bottom: 20px;
    }
    #startButton {
      padding: 15px 30px;
      font-size: 24px;
      border: none;
      border-radius: 8px;
      background-color: #e91e63;
      color: #fff;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    #startButton:hover {
      background-color: #d81b60;
    }
    #proposalText {
      display: none;
      font-size: 24px;
      margin-top: 20px;
      line-height: 1.5;
      animation: fadeIn 3s ease;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    /* Heart Animation */
    .heart {
      position: absolute;
      bottom: -50px;
      width: 30px;
      height: 30px;
      background-color: #ff69b4;
      clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);
      animation: floatHearts 5s infinite;
    }
    @keyframes floatHearts {
      0% { transform: translateY(0) scale(0.5); opacity: 0.8; }
      50% { opacity: 1; }
      100% { transform: translateY(-100vh) scale(1); opacity: 0; }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Welcome, My Love</h1>
    <button id="startButton" onclick="startProposal()">Start</button>
    <div id="proposalText">
      <p>
        My heart beats in binary, but our love is infinite.<br>
        Every line of code and every algorithm reminds me how perfectly we fit together.<br>
        Today, I want to merge our lives forever. Will you marry me?
      </p>
    </div>
  </div>
  
  <!-- Background Music: Replace the src with your romantic song file -->
  <audio id="bgMusic" src="Dil Meri Na Sune Genius 128 Kbps.mp3"></audio>
  
  <script>
    function startProposal() {
      // Hide the start button and show the proposal text
      document.getElementById('startButton').style.display = 'none';
      document.getElementById('proposalText').style.display = 'block';
      
      // Play the background music (triggered by user interaction)
      var music = document.getElementById('bgMusic');
      music.play();
      
      // Start heart animations
      startHeartAnimation();
    }
    
    function startHeartAnimation() {
      // Create heart elements periodically
      setInterval(function() {
        var heart = document.createElement('div');
        heart.classList.add('heart');
        // Random horizontal placement
        heart.style.left = Math.random() * 100 + 'vw';
        // Random animation delay for variety
        heart.style.animationDelay = Math.random() * 5 + 's';
        document.body.appendChild(heart);
        // Remove heart after its animation duration
        setTimeout(() => {
          heart.remove();
        }, 5000);
      }, 300);
    }
  </script>
</body>
</html>
