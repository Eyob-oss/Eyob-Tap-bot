<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tap the Birr</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #282c34;
            color: white;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
        }
        #game-area {
            width: 150px;
            height: 150px;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            margin-bottom: 20px;
        }
        #coin {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
        #start-btn {
            padding: 10px 20px;
            font-size: 18px;
            border: none;
            background-color: #ff9800;
            color: white;
            cursor: pointer;
            border-radius: 5px;
        }
        #start-btn:hover {
            background-color: #e68900;
        }
    </style>
</head>
<body>

    <h1>Tap the Ethiopian 1 Birr Coin</h1>
    <div id="game-area" onclick="tap()">
        <img id="coin" src="ei_1738424160057-removebg-preview (1).png" alt="1 Birr Coin">
    </div>
    <button id="start-btn" onclick="startGame()">Start Game</button>
    <h2 id="score">Score: 0</h2>
    <h3 id="timer">Time Left: 10s</h3>

    <script>
        let score = 0;
        let timeLeft = 10;
        let gameActive = false;
        let timerInterval;

        function startGame() {
            score = 0;
            timeLeft = 10;
            gameActive = true;
            document.getElementById("score").innerText = "Score: " + score;
            document.getElementById("timer").innerText = "Time Left: " + timeLeft + "s";
            
            timerInterval = setInterval(() => {
                timeLeft--;
                document.getElementById("timer").innerText = "Time Left: " + timeLeft + "s";
                if (timeLeft <= 0) {
                    endGame();
                }
            }, 1000);
        }

        function tap() {
            if (gameActive) {
                score++;
                document.getElementById("score").innerText = "Score: " + score;
            }
        }

        function endGame() {
            gameActive = false;
            clearInterval(timerInterval);
            alert("Game Over! Your final score is: " + score);
        }
    </script>

</body>
</html>
let do this don't count second  and score how many it taps 
