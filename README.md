# Projeto-PWFE

Relatorio:

# Relatório sobre o Script JavaScript

## Introdução
O script JavaScript fornecido implementa a lógica do jogo da velha para a página web. Ele define os jogadores, controla a lógica do jogo e verifica se houve um vencedor ou se o jogo terminou em empate.

## Estrutura Geral

### Inicialização da Página
- `window.onload`: Esta função é executada quando a página é completamente carregada. Neste caso, ela esconde a div com o id `game`.

### Definição de Jogadores
- `Jogador(nome, forma)`: Esta função é um construtor para criar objetos de jogador. Cada jogador tem um nome (`nome`) e uma forma (`forma`) que será usada para marcar as células do tabuleiro (X ou O).

### Variáveis Globais
- `jogador1`, `jogador2`: Representam os jogadores.
- `jogadorAtual`: Indica qual jogador está atualmente em sua rodada.
- `formas`: Um array contendo as formas que os jogadores usam para marcar as células (X e O).
- `index`: Variável não utilizada no script, permanece como `null`.

### Tabuleiro
- `tabuleiro`: Um array de 9 elementos que representa o estado do tabuleiro. As posições preenchidas por X ou O são armazenadas aqui.

### Inicialização do Jogo
- `initGame()`: Esta função é chamada quando o botão "Iniciar" é clicado. Ela obtém os nomes dos jogadores do formulário, cria os objetos de jogador e inicia o jogo, tornando a div com o id `game` visível.

### Funções de Verificação
- `tabuleiroIsFilled()`: Verifica se todas as células do tabuleiro estão preenchidas. Retorna verdadeiro se o tabuleiro estiver completamente preenchido.
- `allElementsInSomeLine()`: Verifica se algum jogador ganhou em alguma linha horizontal.
- `allElementsInSomeColumn()`: Verifica se algum jogador ganhou em alguma coluna vertical.
- `allElementsInSomeDiagonal()`: Verifica se algum jogador ganhou em alguma diagonal.

### Atualização do Jogador Atual
- `setLabelJogadorAtual()`: Atualiza o texto que indica qual jogador está na rodada atual.

### Marcação de Células do Tabuleiro
- `setOnCeil(cel, pos)`: Esta função é chamada quando uma célula do tabuleiro é clicada. Ela verifica se a célula já está marcada, caso contrário, marca com a forma do jogador atual. Em seguida, atualiza o jogador da rodada e chama as funções de verificação de vencedores.

### Reiniciar o Jogo
- `reset()`: Esta função é chamada quando o jogo precisa ser reiniciado. Ela recarrega a página, reiniciando todo o estado do jogo.

## Conclusão
O script JavaScript fornece a lógica necessária para a implementação de um jogo da velha funcional. Ele controla a interação do usuário, verifica o estado do tabuleiro e determina se houve um vencedor ou se o jogo terminou em empate. Além disso, permite a reinicialização do jogo quando necessário. Recomenda-se testar o script em conjunto com a estrutura HTML fornecida para uma experiência completa do jogo.