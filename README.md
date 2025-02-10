<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Nicol ❤️</title>
    <style>
        body {
            text-align: center;
            font-family: 'Arial', sans-serif;
            background-color: #ffebef;
            color: #d63384;
            padding: 20px;
            overflow: hidden;
        }
        .card {
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            display: inline-block;
            margin-top: 50px;
            animation: fadeIn 2s ease-in-out;
        }
        h1 {
            font-size: 24px;
        }
        p {
            font-size: 18px;
            color: #333;
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            background-color: #d63384;
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 10px;
            margin: 10px;
            transition: 0.3s ease-in-out;
        }
        button:hover {
            background-color: #b52e6e;
            transform: scale(1.1);
        }
        .no-btn {
            position: absolute;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }
    </style>
</head>
<body>

    <div class="card">
        <h1>¿Quieres ser mi San Valentín? 💖</h1>
        <p>Nicol Campo, desde que llegaste a mi vida, cada día es más especial. No solo quiero que seas mi San Valentín, sino mi compañera de aventuras para siempre. 💕</p>
        <div class="buttons">
            <button onclick="respuesta()">¡Sí, quiero! 💘</button>
            <button class="no-btn" onmouseover="moverBoton()">No 😢</button>
        </div>
    </div>

    <script>
        function respuesta() {
            lanzarConfeti();
            alert("¡Sabía que dirías que sí! 💖 Te amo con todo mi corazón ❤️");
        }

        function moverBoton() {
            let boton = document.querySelector(".no-btn");
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            boton.style.position = "absolute";
            boton.style.left = x + "px";
            boton.style.top = y + "px";
        }

        function lanzarConfeti() {
            const confettiContainer = document.createElement("div");
            confettiContainer.style.position = "fixed";
            confettiContainer.style.top = "0";
            confettiContainer.style.left = "0";
            confettiContainer.style.width = "100vw";
            confettiContainer.style.height = "100vh";
            confettiContainer.style.pointerEvents = "none";
            document.body.appendChild(confettiContainer);

            for (let i = 0; i < 50; i++) {
                let confetti = document.createElement("div");
                confetti.style.position = "absolute";
                confetti.style.width = "10px";
                confetti.style.height = "10px";
                confetti.style.backgroundColor = ["#ff4081", "#ffd700", "#33ccff", "#ff66b2"][Math.floor(Math.random() * 4)];
                confetti.style.left = Math.random() * window.innerWidth + "px";
                confetti.style.top = "-10px";
                confetti.style.opacity = Math.random();
                confetti.style.transform = `rotate(${Math.random() * 360}deg)`;
                confetti.style.animation = "fall 2s linear infinite";
                confettiContainer.appendChild(confetti);
            }

            setTimeout(() => document.body.removeChild(confettiContainer), 3000);
        }
    </script>

</body>
</html>
