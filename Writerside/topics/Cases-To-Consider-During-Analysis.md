# Cases To Consider During Analysis

Escolher uma entrada para considerar quando analisarmos um algoritimo pode ter um impacto significativo em omo um algoritmo vai performar 

Por exemplo: se a lista de entrada já está ordenada algum algoritmo de ordenação vai performar muito bem, mas outro algoritmo pode performar porcamente. O oposto aconteceria também

## (A) Best Case Input

Isso representa o conjunto de entrada que permite um algoritmo performar mais rapidamente. Com essa entrada o algoritmo tomaria um tempo de execução mais curto assim fazem os algoritmos terem uma carga de trabalho menor

- Por exemplo: em um algoritmo de busca, dado um valor $x$ que estamos a procura, o melhor caso seria encontrarmos na primeira posição que o algoritmo de pesquisa vai checar; assim o algoritmo precisaria unicamente de uma comparação

Não importa o qual grande é a entrada, a pesquisa no melhor caso vai ficar como um tempo constante de 1. Desde que o melhor caso para um algoritmo deve ser usualmente pequeno e frequentemente um valor constante, a análise do melhor muitas vezes não é feita

## (B) Worst Case Input

Essa entrada representa um conjunto que permite um algoritmo performar mais devagar. O pior caso é uma importante analise porque nós da uma ideia a quantidade de tempo que um algoritmo vai tomar. Worst case analyse requer que nós identifiquemos a entrada de valores que causa uma carga grande de trabalho para o algoritmo

- Por exemplo: o worst case, para um algoritmo de pesquisa seria o valor de $x$ não estar na lista ou ele está na última posição checada, já que isso indica que havera $n$ comparações dentro 

## (C) Average Case Input

Essa entrada representa o conjunto que permite o algoritmo entregar uma performance na média. Nessa analise é um processo de 4 passos:

1. Determinar o número de diferentes grupos no conjunto de todas as possibilidades podem ser dividas
2. Determinar a probabilidade que a entrada vai vir de cada um desses grupos:

**Lista de estruturas de dados:**

- Linear Data Structures: os elementos que formam uma sequencia
  - Arrays
  - Linked Lists
  - Stacks
  - Queues
  - Hash Table
- Non-Linear Data Structures: os elementos não formam uma sequência
  - Trees
  - Graphs

**Operações na Data Structures:**

1. Transversing (percurso):
   - Acessar cada um dos elementos em uma estrutura de dados é chamdo de _transversal of DS_ (transpor uma estrutura de dados)
2. Insertion: 
   - Adicionar um ou mais um dado na estrutura de dado nume posição particular é chamada de _insertion operations_
3. Deletion