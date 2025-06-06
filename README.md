<!DOCTYPE html>
<html>
<head>
    <title>Happy Birthday RAMUU! 🎉</title>
    <style>
        body {
            background: linear-gradient(45deg, #ff6b6b, #ffd93d);
            text-align: center;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
        }
        
        .container {
            margin-top: 100px;
            position: relative;
        }

        h1 {
            color: #ffffff;
            font-size: 3em;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            animation: bounce 2s infinite;
        }

        .message {
            background: white;
            padding: 20px;
            border-radius: 15px;
            margin: 30px auto;
            width: 70%;
            box-shadow: 0 0 20px rgba(0,0,0,0.2);
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .balloon {
            position: absolute;
            width: 60px;
            height: 80px;
            border-radius: 50%;
            animation: float 6s infinite;
        }

        @keyframes float {
            0% { transform: translateY(100vh); }
            100% { transform: translateY(-100vh); }
        }

        button {
            padding: 15px 30px;
            font-size: 1.2em;
            background: #4CAF50;
            color: white;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            transition: transform 0.3s;
        }

        button:hover {
            transform: scale(1.1);
            background: #45a049;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Balloons -->
        <div class="balloon" style="left: 10%; background: #ff0000;"></div>
        <div class="balloon" style="left: 30%; background: #00ff00;"></div>
        <div class="balloon" style="left: 50%; background: #0000ff;"></div>
        <div class="balloon" style="left: 70%; background: #ffff00;"></div>
        <div class="balloon" style="left: 90%; background: #ff00ff;"></div>

        <h1>🎂 Happy Birthday RAMUU! 🎉</h1>
        
        <div class="message">
            <p>Namma Preethiyaaa Raaamuuuu</p>
            <p>Wishing you an amazing birthday filled with joy, laughter, and wonderful memories! 🎈</p>
            <p>May all your dreams turn into reality and may success follow you wherever you go! 💫</p>
            <p>Enjoy your special day! 🥳 ROCK ON</p>
        </div>

        <button onclick="playMusic()">Click for Birthday Song! 🎵</button>
    </div>

    <script>
        function playMusic() {
            const audio = new Audio('https://www.dropbox.com/s/9ihdv8x4wxn4k0t/happy-birthday-song.mp3?raw=1');
            audio.play().catch(error => alert('Click the button again to play music!'));
        }

        // Create more balloons dynamically
        function createBalloons() {
            const container = document.querySelector('.container');
            for (let i = 0; i < 20; i++) {
                const balloon = document.createElement('div');
                balloon.className = 'balloon';
                balloon.style.left = Math.random() * 100 + '%';
                balloon.style.background = `hsl(${Math.random() * 360}, 100%, 50%)`;
                balloon.style.animationDelay = Math.random() * 6 + 's';
                container.appendChild(balloon);
            }
        }

        createBalloons();
    </script>
</body>
</html>
