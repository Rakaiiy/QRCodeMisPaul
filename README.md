# QRCodeMisPaul
QR CODE com um contador personalizado para dar de presente.
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nosso Tempo Juntos</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            font-family: 'Arial', sans-serif;
            color: #fff;
            text-align: center;
            padding: 20px;
        }
        h1 {
            font-size: 3em;
            margin-bottom: 20px;
        }
        p {
            font-size: 2em;
        }
    </style>
</head>
<body>
    <div>
        <h1>Estamos juntos há:</h1>
        <p id="contador">0 dias</p>
        <p>❤️ Te amo! ❤️</p>
    </div>

    <script>
        // Substitua por a data que vocês começaram a namorar (formato: 'YYYY-MM-DD')
        const dataInicio = new Date('2021-10-17');

        function atualizarContador() {
            const hoje = new Date();
            const diffTime = hoje - dataInicio;
            const diffDias = Math.floor(diffTime / (1000 * 60 * 60 * 24));
            document.getElementById('contador').textContent = `${diffDias} dias`;
        }

        atualizarContador();
        setInterval(atualizarContador, 60000); // Atualiza a cada minuto
    </script>
</body>
</html>
