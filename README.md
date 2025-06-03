
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Meu amor 🙃💙</title>
    <style>
        body {
            background: linear-gradient(to right, #cce7ff, #ffe6f0);
            color: #003366;
            text-align: center;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            overflow: hidden;
            margin: 0;
        }
        h1 {
            font-size: 3em;
            margin-top: 60px;
        }
        p {
            font-size: 1.8em;
            color: #99004d;
        }
        .heart {
            position: fixed;
            top: -50px;
            color: red;
            animation: fall linear infinite;
        }
        @keyframes fall {
            0% {transform: translateY(-50px);}
            100% {transform: translateY(100vh);}
        }
        #playButton {
            margin-top: 40px;
            padding: 15px 30px;
            font-size: 1.2em;
            background-color: #ff99cc;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: background-color 0.3s ease;
        }
        #playButton:hover {
            background-color: #ff66aa;
        }
        #playerContainer {
            display: none;
        }
    </style>
</head>
<body>
    <h1>Meu amor 🙃💙</h1>
    <p>Eu te amo 🙃💙</p>

    <button id="playButton">Clique para ouvir nossa música 🎵</button>

    <div id="playerContainer">
        <iframe 
            width="0" height="0" 
            src="https://www.youtube.com/embed/qvBf6WBatk0?autoplay=1&loop=1&playlist=qvBf6WBatk0" 
            frameborder="0" allow="autoplay" allowfullscreen>
        </iframe>
    </div>

    <script>
        const hearts = "❤️💕💖💘💗".split("");
        for (let i = 0; i < 30; i++) {
            const heart = document.createElement("div");
            heart.className = "heart";
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.fontSize = (Math.random() * 20 + 20) + "px";
            heart.style.animationDuration = (Math.random() * 3 + 2) + "s";
            heart.innerText = hearts[Math.floor(Math.random() * hearts.length)];
            document.body.appendChild(heart);
        }

        document.getElementById("playButton").addEventListener("click", function () {
            document.getElementById("playerContainer").style.display = "block";
            this.style.display = "none";
        });
    </script>
</body>
</html>
