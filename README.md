# Criando-um-Jogo-do-Detona-Ralph-com-JavaScript
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jogo Detona Ralph</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <canvas id="gameCanvas" width="800" height="600"></canvas>
    <script src="script.js"></script>
</body>
</html>
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
    margin: 0;
}

canvas {
    border: 2px solid #000;
}
const canvas = document.getElementById('gameCanvas');
const ctx = canvas.getContext('2d');

let score = 0;
let gameOver = false;

// Função para desenhar o personagem
function drawCharacter(x, y) {
    ctx.fillStyle = 'blue'; // Cor do personagem
    ctx.fillRect(x, y, 50, 50); // Desenhe um quadrado como personagem
}

// Função principal do jogo
function gameLoop() {
    if (gameOver) return;

    ctx.clearRect(0, 0, canvas.width, canvas.height); // Limpa o canvas
    drawCharacter(100, 100); // Desenha o personagem em uma posição fixa

    // Atualize a lógica do jogo aqui (movimentos, colisões, etc.)
    
    requestAnimationFrame(gameLoop); // Chama novamente o loop do jogo
}

gameLoop(); // Inicia o loop do jogo
document.addEventListener('keydown', (event) => {
    if (event.key === 'ArrowRight') {
        // Mova o personagem para a direita
    }
    if (event.key === 'ArrowLeft') {
        // Mova o personagem para a esquerda
    }
    // Outras teclas e interações
});
