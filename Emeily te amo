<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Emeily ❤️</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #ffe6e6;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
            text-align: center;
            transition: background-color 1s ease;
        }
        .container {
            background-color: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            z-index: 10;
            max-width: 400px;
            width: 90%;
        }
        h1 {
            color: #ff4d4d;
            margin-bottom: 30px;
            font-size: 28px;
            transition: all 0.5s ease;
        }
        .buttons {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
            height: 60px;
        }
        button {
            padding: 12px 30px;
            font-size: 18px;
            font-weight: bold;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.2s ease;
        }
        #btn-si {
            background-color: #4caf50;
            color: white;
        }
        #btn-si:hover {
            transform: scale(1.1);
        }
        #btn-no {
            background-color: #f44336;
            color: white;
        }
        /* Estilos para los corazones flotantes */
        .corazon {
            position: absolute;
            color: #ff4d4d;
            font-size: 24px;
            position: fixed;
            bottom: -10px;
            animation: flotar 3s linear infinite;
            z-index: 1;
            user-select: none;
        }
        @keyframes flotar {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-105vh) rotate(360deg);
                opacity: 0;
            }
        }
    </style>
</head>
<body>

    <div class="container">
        <h1 id="question">Emeily, ¿quieres ser mi novia? ❤️</h1>
        <div class="buttons" id="contenedor-botones">
            <button id="btn-si" onclick="aceptar()">¡SÍ!</button>
            <button id="btn-no" onclick="achicarBoton()">NO</button>
        </div>
    </div>

    <script>
        let clicksEnNo = 0;
        let tamañoBtnSi = 18;

        function achicarBoton() {
            clicksEnNo++;
            const btnNo = document.getElementById('btn-no');
            const btnSi = document.getElementById('btn-si');
            
            if (clicksEnNo === 1) {
                btnNo.innerText = "¿Segura? 🥺";
                btnNo.style.transform = "scale(0.8)";
                tamañoBtnSi += 5;
                btnSi.style.fontSize = tamañoBtnSi + "px";
            } else if (clicksEnNo === 2) {
                btnNo.innerText = "Piénsalo bien... 💔";
                btnNo.style.transform = "scale(0.5)";
                tamañoBtnSi += 8;
                btnSi.style.fontSize = tamañoBtnSi + "px";
            } else {
                // Al tercer intento el botón NO desaparece por completo
                btnNo.style.display = "none";
                btnSi.style.transform = "scale(1.3)";
                btnSi.style.width = "100%";
            }
        }

        function aceptar() {
            // Cambia el contenido visual por algo hermoso
            document.getElementById('question').innerHTML = '¡Me haces la persona más feliz del mundo! 😍<br><br>✨ Te amo Emeily ✨';
            document.getElementById('contenedor-botones').style.display = 'none';
            document.body.style.backgroundColor = '#ffb3b3';
            
            // Activa la lluvia de corazones continuos
            setInterval(crearCorazon, 150);
        }

        function crearCorazon() {
            const corazon = document.createElement('div');
            corazon.classList.add('corazon');
            corazon.innerHTML = '❤️';
            
            // Posición horizontal aleatoria
            corazon.style.left = Math.random() * 100 + 'vw';
            // Tamaño aleatorio del corazón
            corazon.style.fontSize = Math.random() * 20 + 15 + 'px';
            // Velocidad de subida aleatoria
            corazon.style.animationDuration = Math.random() * 2 + 2s;
            
            document.body.appendChild(corazon);
            
            // Elimina el corazón después de que termina la animación
            setTimeout(() => {
                corazon.remove();
            }, 4000);
        }
    </script>

</body>
</html>
