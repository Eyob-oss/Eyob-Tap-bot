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
        #reset-btn {
            padding: 10px 20px;
            font-size: 18px;
            border: none;
            background-color: #ff9800;
            color: white;
            cursor: pointer;
            border-radius: 5px;
            margin-top: 20px;
        }
        #reset-btn:hover {
            background-color: #e68900;
        }
    </style>
</head>
<body>

    <h1>Tap the Ethiopian 1 Birr Coin</h1>
    <div id="game-area" onclick="tap()">
        <img id="coin" src="ei_1738424160057-removebg-preview (1).png/640px-1_Birr_Reverse.png" alt="1 Birr Coin">
    </div>
    <h2 id="score">Taps: 0</h2>
    <button id="reset-btn" onclick="resetGame()">Reset</button>

    <script>
        let score = 0;

        function tap() {
            score++;
            document.getElementById("score").innerText = "Taps: " + score;
        }

        function resetGame() {
            score = 0;
            document.getElementById("score").innerText = "Taps: " + score;
        }
    </script>

</body>
</html>
