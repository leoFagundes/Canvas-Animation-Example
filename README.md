# Jogo da Cobrinha - Usando a Tag `<canvas>`

Este é um exemplo simples de um jogo da cobrinha criado com a tag `<canvas>` do HTML5. O jogo é desenvolvido inteiramente com JavaScript, utilizando o contexto 2D da tag `<canvas>` para desenhar a cobrinha e os alimentos. A mecânica básica envolve movimentar a cobrinha, coletar alimentos e evitar colisões com as paredes ou consigo mesma.

## Tecnologias Usadas

- **HTML5**: Para estruturar a página e a tag `<canvas>`.
- **CSS**: Para estilizar o jogo, a tela e os botões.
- **JavaScript**: Para controlar a lógica do jogo, movimentação da cobrinha, detecção de colisões e pontuação.

## Como Funciona?

### 1. **A Tag `<canvas>`**

A tag `<canvas>` é um elemento HTML utilizado para desenhar gráficos, animações e até mesmo criar jogos diretamente no navegador. Através da API de contexto 2D (acessada via `getContext("2d")`), podemos desenhar objetos como retângulos, linhas e formas no elemento.

### 2. **Estrutura do Código**

- **HTML**: A página contém um elemento `<canvas>` com id `gameCanvas`, que serve de área de jogo, além de um botão para iniciar o jogo.
- **CSS**: O estilo é aplicado para centralizar a tela, definir o fundo do jogo, a aparência dos botões e a borda da tela de jogo.
- **JavaScript**: A lógica do jogo é controlada via JavaScript, incluindo a movimentação da cobrinha, o aparecimento de alimentos e a verificação de colisões.

### 3. **Como Jogar**

- Ao clicar no botão "Iniciar Jogo", a partida começa.
- Use as teclas de seta do teclado para mover a cobrinha:
  - **Seta para cima**: Move a cobrinha para cima.
  - **Seta para baixo**: Move a cobrinha para baixo.
  - **Seta para esquerda**: Move a cobrinha para a esquerda.
  - **Seta para direita**: Move a cobrinha para a direita.
- A cobrinha cresce cada vez que come um alimento, e o objetivo é alcançar a maior pontuação possível sem colidir com as paredes ou com o próprio corpo da cobrinha.
- O jogo salva o recorde da pontuação, que é mantido no `localStorage`.

### 4. **Como o Jogo Funciona**

- **Início do Jogo**: Ao clicar no botão, a função `startGame()` é chamada, iniciando a partida e resetando as variáveis necessárias.
- **Movimentação da Cobrinha**: A posição da cobrinha é controlada por um vetor de segmentos, com a posição da cabeça sendo atualizada com base na direção atual.
- **Alimentos**: O alimento aparece aleatoriamente dentro da área de jogo, e cada vez que a cobrinha o consome, sua pontuação aumenta e um novo alimento é gerado.
- **Colisões**: O jogo verifica se a cobrinha colidiu com as paredes ou com seu próprio corpo. Se uma colisão ocorrer, o jogo é encerrado e o recorde é atualizado, se necessário.
