<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Decodificador de Texto</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Decodificador de Texto</h1>
        <div class="input-group">
            <textarea id="input-text" placeholder="Digite o texto aqui"></textarea>
            <button onclick="encodeText()">Criptografar</button>
            <button onclick="decodeText()">Descriptografar</button>
        </div>
        <div class="output-group">
            <textarea id="output-text" placeholder="Resultado" readonly></textarea>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f4f4f4;
    margin: 0;
}

.container {
    width: 90%;
    max-width: 600px;
    background: #fff;
    padding: 20px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
}

h1 {
    text-align: center;
}

.input-group, .output-group {
    margin: 20px 0;
}

textarea {
    width: 100%;
    height: 100px;
    padding: 10px;
    margin-bottom: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
    box-sizing: border-box;
}

button {
    width: 48%;
    padding: 10px;
    margin: 0 1%;
    border: none;
    border-radius: 4px;
    background-color: #007bff;
    color: #fff;
    font-size: 16px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}
function encodeText() {
    const text = document.getElementById('input-text').value;
    try {
        const encodedText = btoa(text); // Codifica o texto para base64
        document.getElementById('output-text').value = encodedText;
    } catch (e) {
        document.getElementById('output-text').value = 'Erro ao codificar o texto.';
    }
}

function decodeText() {
    const text = document.getElementById('input-text').value;
    try {
        const decodedText = atob(text); // Decodifica o texto de base64
        document.getElementById('output-text').value = decodedText;
    } catch (e) {
        document.getElementById('output-text').value = 'Texto inválido para decodificação.';
    }
}
cd decodificador-de-texto
git init
git add .
git commit -m "Initial commit with project files"
git remote add origin https://github.com/seu-usuario/decodificador-de-texto.git
git branch -M main
git push -u origin main
