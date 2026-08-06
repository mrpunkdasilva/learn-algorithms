# 1. SELECTION SORTING

o selection sort inicia de um primeiro elemento e pesquisa lista inteira até que encontre o valor mínimo. A ordenação coloca o valor mínimo em primeiro lugar, seleciona o segundo elemento e busca o segundo menor elemento 

O processo continua até que a lista esteja completamente ordenada. O selection sort é um dos que sucessivamente os elementos são selecionados na ordem e lugar dentro da suas proprias posições ordenadas

O processo de seleção precisa ser feito apenas de 1 a n-1, em vez de até n. A análise do tipo de seleção é simples. A primeira passagem faz n - 1 comparações, a segunda faz n – 2 e assim por diante. Portanto, as comparações totais são (N - 1)+ (N - 2) + (N - 3) + ... + 2 + 1 = N (N-1)/2 = O (N2). Há pouco armazenamento adicional necessário (exceto para guardar algumas variáveis temporárias)

Portanto, a ordenação pode ser categorizada como O(N2), embora seja mais rápida que a ordenação por bolhas, mas não há melhora se o arquivo de entrada estiver completamente ordenado ou não ordenado. Apesar de ser simples de programar, é improvável que a ordenação por seleção direta seja usada em arquivos que não sejam aqueles para os quais n é pequeno.

O algoritmo de ordenação por seleção para ordenação funciona da seguinte forma. Primeiro, encontre o menor elemento da lista e coloque-o na primeira posição. Depois, encontre o segundo elemento menor da lista e coloque-o na segunda posição.

> Vale notar que o número de comparações no algoritmo de seleção é independente do tipo original dos elementos. O método de seleção de ordenação requer (n – 1) passagens para ordenar um array.


| **Melhor Caso** | **Caso Médio** | **Pior Caso** |
|-----------------|----------------|---------------|
| $$O(N^2)$$      | $$O(N^2)$$     | $$O(N^2)$$    |


### SELECTION_SORT(A, N)

Aqui A é um array com N elementos. Esse algoritmo ordena o array A com N elememntos em ordem ascendente:

```
Repeat steps 2 to 5 for I = 1 to N - 1:
    Set MIN := A[I] 
    Set POS := I
    
    Repeat steps for J = I + 1 to N:
        if A[J] < MIN, then:
           (a) Set MIN := A[J]
           (b) Set POST := J
        [End of strucuture]
    [End of Step 4 loop]
    if I > POS, then: 
        (a) Set TEMP := A[I]
        (b) Set A[I] := A[POS]
        (c) Set A[POST] := TEMP
    [End of if structure]
[End of step 1 loop]
```
