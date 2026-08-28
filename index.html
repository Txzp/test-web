<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bingo de Mamá</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            user-select: none;
        }

        body {
            background-color: #ffffff;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            overflow: hidden;
            position: relative;
            color: #333;
        }

        .main-content {
            z-index: 10;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            flex-grow: 1;
            gap: 20px;
        }

        h1 {
            font-size: clamp(2rem, 5vw, 3rem);
            color: #ff477e;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-weight: 800;
            text-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }

        .number-box {
            width: 220px;
            height: 220px;
            background: linear-gradient(135deg, #ff758c 0%, #ff7eb3 100%);
            border-radius: 35px;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 15px 35px rgba(255, 117, 140, 0.3);
            position: relative;
            overflow: hidden;
        }

        #current-number {
            font-size: clamp(5rem, 12vw, 7rem);
            font-weight: bold;
            color: #ffffff;
        }

        /* Animación de revelación de 2.5 segundos */
        .reveal-anim {
            animation: revealEffect 2.5s cubic-bezier(0.1, 0.8, 0.3, 1) forwards;
        }

        @keyframes revealEffect {
            0% {
                transform: scale(0.3) rotate(-15deg);
                opacity: 0.2;
                filter: blur(4px);
            }
            50% {
                transform: scale(1.15) rotate(5deg);
                opacity: 0.8;
                filter: blur(1px);
            }
            100% {
                transform: scale(1) rotate(0deg);
                opacity: 1;
                filter: blur(0);
            }
        }

        #btn-next {
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
            border: none;
            padding: 18px 45px;
            font-size: 1.4rem;
            font-weight: bold;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 10px 25px rgba(37, 117, 252, 0.3);
            transition: transform 0.2s, box-shadow 0.2s;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        #btn-next:hover {
            transform: scale(1.05);
            box-shadow: 0 15px 30px rgba(37, 117, 252, 0.4);
        }

        #btn-next:active {
            transform: scale(0.95);
        }

        #btn-next:disabled {
            background: #cccccc;
            cursor: not-allowed;
            box-shadow: none;
            transform: none;
        }

        .history-container {
            width: 90%;
            max-width: 600px;
            background: #f8f9fa;
            border-radius: 15px;
            padding: 10px 15px;
            margin-bottom: 20px;
            box-shadow: inset 0 2px 5px rgba(0,0,0,0.03);
            text-align: center;
            z-index: 10;
        }

        .history-title {
            font-size: 0.9rem;
            color: #6c757d;
            margin-bottom: 5px;
            font-weight: 600;
        }

        #history-list {
            display: flex;
            gap: 8px;
            overflow-x: auto;
            padding-bottom: 5px;
            justify-content: center;
            flex-wrap: wrap;
            max-height: 70px;
        }

        .history-badge {
            background: #ffffff;
            border: 2px solid #ff7eb3;
            color: #ff477e;
            font-weight: bold;
            width: 35px;
            height: 35px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 0.9rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }

        .wave-container {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 150px;
            overflow: hidden;
            z-index: 1;
            pointer-events: none;
        }

        .wave {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 200%;
            height: 100%;
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 800 88.7'%3E%3Cpath d='M800 56.9c-155.5 0-204.9-50-405.5-50-200.8 0-250 50-394.5 50v31.8h800v-31.8z' fill='%23f1f3f5'/%3E%3C/svg%3E");
            background-size: 50% 100%;
        }

        .wave1 {
            animation: waveMove 12s linear infinite;
            opacity: 0.7;
            bottom: 0px;
        }

        .wave2 {
            animation: waveMove 8s linear infinite reverse;
            opacity: 0.4;
            bottom: 10px;
        }

        @keyframes waveMove {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }
    </style>
</head>
<body>

    <div class="main-content">
        <h1>Bingo 🎯</h1>
        
        <div class="number-box">
            <span id="current-number">--</span>
        </div>

        <button id="btn-next">¡Sacar Número!</button>
    </div>

    <div class="history-container">
        <div class="history-title">Últimos números cantados:</div>
        <div id="history-list"></div>
    </div>

    <div class="wave-container">
        <div class="wave wave1"></div>
        <div class="wave wave2"></div>
    </div>

    <script>
        // Secuencia exacta solicitada por tu mamá
        const bingoSequence = [18, 14, 10, 8, 11, 16, 13];
        let currentIndex = 0;
        let calledNumbers = [];

        const btnNext = document.getElementById('btn-next');
        const numberDisplay = document.getElementById('current-number');
        const historyList = document.getElementById('history-list');

        // Función para reproducir sonido de revelación integrado (Web Audio API)
        function playRevealSound() {
            try {
                const audioCtx = new (window.AudioContext || window.webkitAudioContext)();
                const osc = audioCtx.createOscillator();
                const gain = audioCtx.createGain();
                
                osc.type = 'sine';
                // Tono de suspenso que sube durante los 2.5 segundos
                osc.frequency.setValueAtTime(300, audioCtx.currentTime);
                osc.frequency.exponentialRampToValueAtTime(750, audioCtx.currentTime + 2.5);
                
                gain.gain.setValueAtTime(0.2, audioCtx.currentTime);
                gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + 2.5);
                
                osc.connect(gain);
                gain.connect(audioCtx.destination);
                
                osc.start();
                osc.stop(audioCtx.currentTime + 2.5);
            } catch (e) {
                console.log("Audio no soportado o bloqueado por el navegador");
            }
        }

        btnNext.addEventListener('click', () => {
            if (currentIndex >= bingoSequence.length) {
                alert('¡Se acabaron todos los números de la secuencia!');
                btnNext.disabled = true;
                return;
            }

            btnNext.disabled = true;
            playRevealSound();

            const targetNumber = bingoSequence[currentIndex];
            currentIndex++;

            // Efecto visual de números aleatorios cambiando rápidamente durante los primeros 2 segundos
            let shuffleTimer = setInterval(() => {
                const randomTemp = Math.floor(Math.random() * 90) + 1;
                numberDisplay.innerText = randomTemp;
            }, 80);

            // Reiniciar y aplicar la animación lenta de 2.5 segundos
            numberDisplay.classList.remove('reveal-anim');
            void numberDisplay.offsetWidth; 
            numberDisplay.classList.add('reveal-anim');

            // A los 2.5 segundos se detiene el cambio rápido y se muestra el número correcto
            setTimeout(() => {
                clearInterval(shuffleTimer);
                numberDisplay.innerText = targetNumber;
                calledNumbers.unshift(targetNumber);
                updateHistory();
                
                if (currentIndex < bingoSequence.length) {
                    btnNext.disabled = false;
                }
            }, 2500);
        });

        function updateHistory() {
            historyList.innerHTML = '';
            calledNumbers.forEach(num => {
                const badge = document.createElement('div');
                badge.className = 'history-badge';
                badge.innerText = num;
                historyList.appendChild(badge);
            });
        }
    </script>
</body>
</html>
