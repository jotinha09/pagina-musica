<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Conversor de Moeda</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0px 4px 8px rgba(0,0,0,0.2);
            text-align: center;
        }
        input {
            padding: 10px;
            width: 200px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            padding: 10px 20px;
            background-color: #0077cc;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #005fa3;
        }
        .resultado {
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
            color: #333;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Conversor de Reais para Dólares</h2>
        <input type="number" id="valorReais" placeholder="Digite o valor em R$">
        <br>
        <button onclick="converter()">Converter</button>
        <div class="resultado" id="resultado"></div>
    </div>

    <script>
        function converter() {
            const taxa = 5.30; // 1 dólar = R$ 5,30
            let reais = document.getElementById("valorReais").value;
            let dolares = reais / taxa;
            document.getElementById("resultado").innerText = 
                `Valor em dólares: U$ ${dolares.toFixed(2)}`;
        }
    </script>
</body>
</html>
