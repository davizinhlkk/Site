<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Brincadeira com Ramon</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffffff;
            color: #000000;
            margin: 0;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }
        h1 {
            font-size: 2rem;
            margin-bottom: 20px;
        }
        .btn {
            padding: 10px 20px;
            margin: 10px;
            font-size: 1.2rem;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        .yes {
            background-color: #4caf50;
            color: white;
        }
        .no {
            background-color: #f44336;
            color: white;
            position: absolute;
        }
        .result {
            font-size: 2rem;
            color: #000000;
            display: none;
        }
    </style>
</head>
<body>
    <div id="content">
        <h1>Ramon, vocÃª gosta da Jamily?</h1>
        <button class="btn yes" onclick="showResult()">Sim</button>
        <button class="btn no" onmouseover="moveButton()">NÃ£o</button>
    </div>
    <div class="result" id="result">ðŸ˜‚ Eu sabia! ðŸ˜‚</div>
    
    <script>
        function moveButton() {
            const noButton = document.querySelector('.no');
            const randomX = Math.random() * (window.innerWidth - noButton.offsetWidth);
            const randomY = Math.random() * (window.innerHeight - noButton.offsetHeight);
            noButton.style.left = `${randomX}px`;
            noButton.style.top = `${randomY}px`;
        }

        function showResult() {
            // Esconde a pergunta e os botÃµes
            document.getElementById('content').style.display = 'none';
            // Mostra o resultado
            document.getElementById('result').style.display = 'block';
        }
    </script>
</body>
</html>
