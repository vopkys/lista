<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Planejamento de Eventos</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            text-align: center;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 20px;
        }
        .container {
            width: 80%;
            margin: 20px auto;
        }
        .lista {
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            margin: 20px;
            padding: 20px;
            display: inline-block;
            vertical-align: top;
            width: 28%;
            text-align: left;
        }
        .lista h2 {
            color: #333;
        }
        .lista ul {
            lista-style: none;
            padding: 0;
        }
        .lista ul li {
            padding: 10px;
            border-bottom: 1px solid #ddd;
        }
        .lista ul li:last-child {
            border-bottom: none;
        }
        .lista input, .lista button {
            width: 100%;
            padding: 10px;
            margin: 5px 0;
            box-sizing: border-box;
        }
    </style>
</head>
<body>
    <header>
        <h1>Gastos do Mês</h1>
    </header>
    <div class="container">
        <div class="lista">
            <h2>Carnês</h2>
            <ul id="Carnês-lista"> </ul>
            <input type="text" id="Carnês-input" placeholder="Adicionar item">
            <button onclick="addItem('Carnês')">Adicionar</button>
        </div>
        <div class="lista">
            <h2>Pendentes</h2>
            <ul id="pendentes-lista">

            </ul>
            <input type="text" id="pendentes-input" placeholder="Adicionar item">
            <button onclick="addItem('pendentes')">Adicionar</button>
        </div>
        <div class="lista">
            <h2>Boletos</h2>
            <ul id="boletos-lista">

            </ul>
            <input type="text" id="boletos-input" placeholder="Adicionar item">
            <button onclick="addItem('boletos')">Adicionar</button>
        </div>
    </div>
    <script>
        function addItem(listaType) {
            const input = document.getElementById(`${listaType}-input`);
            const lista = document.getElementById(`${listaType}-lista`);
            const itemText = input.value.trim();

            if (itemText !== '') {
                const listaItem = document.createElement('li');
                listaItem.textContent = itemText;
                lista.appendChild(listaItem);
                input.value = '';
            }
        }
    </script>
</body>
</html>
