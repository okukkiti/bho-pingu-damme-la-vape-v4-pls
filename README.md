<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>bho cazzo ne so</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100vh;
            background-color: black;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: Arial, sans-serif;
            overflow: hidden;
        }

        .container {
            display: flex;
            align-items: center;
            text-align: center;
        }

        .image-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-right: 20px;
        }

        .image-container img {
            max-width: 150px;
            border-radius: 10px;
        }

        .text-above-image {
            margin-bottom: 10px;
            font-size: 18px;
        }

        .text-button-container {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .text-above-button {
            margin-bottom: 20px;
            font-size: 24px;
        }

        .button {
            padding: 15px 30px;
            font-size: 18px;
            background-color: white;
            color: black;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .button:hover {
            background-color: grey;
        }

        .bottom-right-text {
            position: absolute;
            bottom: 10px;
            right: 10px;
            font-size: 14px;
        }

        #game-container {
            display: none;
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
            left: 0;
            background-color: black;
        }

        #player {
            width: 50px;
            height: 50px;
            background-color: red;
            position: absolute;
            bottom: 20px;
            left: calc(50% - 25px);
        }

        .obstacle {
            width: 50px;
            height: 50px;
            background-color: white;
            position: absolute;
            top: calc(50% - 25px);
            right: 0;
            animation: moveObstacle 3s linear infinite;
        }

        @keyframes moveObstacle {
            from { right: 0; }
            to { right: 100%; }
        }
    </style>
</head>
<body>
    <div id="main-content" class="container">
        <div class="image-container">
            <div class="text-above-image">la veippp v4 che acer che sono</div>
            <img src="C:\Users\cihom\Downloads\cazzo di pingu.jpg" alt="Immagine">
        </div>
        <div class="text-button-container">
            <div class="text-above-button">panino del macodnald con la mia gang ci beviamo una cocacola dentro al prive fuck ur opinion non mi interessi anche se sei piu basso di lionel messi</div>
            <button class="button" onclick="startGame()">Clicca qui</button>
        </div>
    </div>
    <div class="bottom-right-text">pingu dammi la vape per forza</div>

    <div id="game-container">
        <div id="player"></div>
        <div class="obstacle"></div>
    </div>

    <script>
        function startGame() {
           
            document.getElementById('main-content').style.display = 'none';
            document.getElementById('game-container').style.display = 'block';

            document.addEventListener('keydown', function(event) {
                var player = document.getElementById('player');
                var left = parseInt(window.getComputedStyle(player).getPropertyValue('left'));
                
                if (event.key === 'ArrowLeft' && left > 0) {
                    player.style.left = left - 10 + 'px';
                }
                if (event.key === 'ArrowRight' && left < window.innerWidth - 50) {
                    player.style.left = left + 10 + 'px';
                }
            });
        }
    </script>
</body>
</html>
