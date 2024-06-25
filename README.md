# Simulacao-Agregacao-Difusao

**Aluno:** Norton Escopelli Soares  
**Disciplina:** Linguagem C para Engenharia  

## Descrição do Projeto

O presente trabalho tem por finalidade simular um ambiente de agregação em duas dimensões, representado por uma matriz. Nesse ambiente, um quadrado é representado por uma matriz quadrada `n x n`, de tamanho variável escolhido pelo usuário. 

## Funcionamento

1. Em uma posição aleatória é colocada uma partícula, que na matriz é representada pelo valor `1`.
2. Em seguida, é colocada mais uma partícula em local aleatório, e essa segunda partícula inicia um movimento também aleatório.
3. Quando a partícula em movimento tem posição adjacente à partícula parada, ela interrompe o movimento e uma nova partícula inicia o processo.
4. Isso simula o contato entre duas partículas, onde a partícula em movimento se junta ao agregado.
5. Se a partícula em movimento nunca estiver em posição adjacente a uma partícula em repouso e sair do espaço definido para o quadrado, uma nova partícula inicia o processo.
6. O processo é repetido até que um número de partículas igual ao tamanho do lado do quadrado forme o agregado.

## Estrutura do Programa

O programa foi estruturado com funções, tendo por objetivo deixá-lo mais modular. Ao executar o programa, é solicitado ao usuário que entre com as dimensões da matriz, sendo essa a única solicitação feita ao usuário.

Para delimitar a fronteira do espaço solicitado, foi utilizada uma matriz com dimensão `n+2`. Assim, a partícula nunca se posiciona em `i=0`, `i=(n-1)`, `j=0` e `j=(n-1)`.

### Exemplo de Matriz

0 0 0 0 0 0 0
0 0 0 0 0 0 0
0 0 1 0 0 0 0
0 0 0 0 0 0 0
0 0 0 0 0 0 0
0 0 0 0 0 0 0
0 0 0 0 0 0 0


Nesse exemplo, a matriz que o usuário solicitou é `5x5`, porém o programa utilizou uma matriz `7x7`.

## Informações Impressas

Durante a execução, são impressas na tela informações relevantes ao processo, como:
- A matriz “atual”
- Os índices `i` e `j`
- A direção do movimento atual `(x, y)`
- A iteração atual

O processo todo é gravado em arquivo e também impresso na tela. Uma variável `struct` guarda o tamanho da matriz, a matriz inicial e a matriz final. Esses três dados são apresentados na tela ao fim do processo.


