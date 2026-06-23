# Sorting

## Introduction

Ordenar significa arranjar um conjunto em determinada ordem que se espera. Existem diferentes e muitos metodos que podem ser usados para ordenar os dados de forma ascendente ou descendente 

Esses metodos podem ser dividios em duas categorias. E elas são:

1. **INTERNAL SORTING:**

Se todos os dados que forem para ordenar podem ser acomodado no tempo em memoria então memtodos intenros de ordenamento são usados

2. **EXTERNAL SORTING:**

Quando o dado para ser ordenado é muito grande que o dado está tanto presente na memoria e outra parte na memoria auxiliar (hard disk) então os metodos de external sorting são usados. Merge sorting pode ser usado em external sorting


| **Algoritmo de Ordenação Interna** | **Melhor Caso** | **Caso Médio** | **Pior Caso** |
|------------------------------------|-----------------|----------------|---------------|
| Selection Sort                     | $$O(N^2)$$      | $$O(N^2)$$     | $$O(N^2)$$    |
| Bubble Sort                        | $$O(N)$$        | $$O(N^2)$$     | $$O(N^2)$$    |
| Insertion Sort                     | $$O(N)$$        | $$O(N^2)$$     | $$O(N^2)$$    |
| Shell Sort (Diminishing Increment) | $$O(N(\log N)^2)$$ | $$O(N(\log N)^2)$$ | $$O(N(\log N)^2)$$ |
| Merge Sort                         | $$O(N \log N)$$ | $$O(N \log N)$$ | $$O(N \log N)$$ |
| Radix Sort (Bucket Sort)           | $$O(d \cdot N)$$ | $$O(d \cdot N)$$ | $$O(d \cdot N)$$ |
| Quick Sort                         | $$O(N \log N)$$ | $$O(N \log N)$$ | $$O(N^2)$$    |
| Heap Sort                          | $$O(N \log N)$$ | $$O(N \log N)$$ | $$O(N \log N)$$ |



## 1. SELECTION SORTING:

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


## 2. BUBBLE SORTING:
1. Verifica se nos dois primeiros valores, o menor valor está na primeira posição, se sim não troca senão troca
2. Pega o segundo valor e vai fazendo as comparações se ele é o maior que o antecessor, se ele for troca senão for não troca, isso eu vou fazendo até o final
3. Assim eu faço comparações e trocas para cada elemento um por vez

![image_2.png](image_2.png)



> Nesse tipo de algoritmo, o número de trocas não pode ser maior que o número de comparações

Uma das questões desse tipo de ordenação é que ele precisa de um espaço adicional, um armazenamento adicional para valores temporarios para as trocas e algumas variaveis inteiras simples, e isso é O(N) no caso em que o arquivo é completamente ordenado ou a maioria é ordenado

Isso segue de uma observação que somente uma passagem de (N-1) comparações (e não mudanças) é necessario para estabelecer que o arquivo ordenado está ordenado. Bubble sort tem uma propriedade muito importante: 

> A menos que não tenha uma troca de elementos em uma passagem particular, não hávera mais troca de elementos nas passagens seguintes

Essa propriedade pode ser explorada para reduzir as passagens redundantes

Para esse proposito podemos usar uma flag para determinar if alguma mudança tomou um lugar, se sim somente então procede com a próxima passagem; senão para. A primeira passagem faz $n - 1$ comparações, a segunda passagem faz $n - 2$ e assim por diante. Então o total de comparações são 

$$
(N - 1) + (N - 2) + (N - 3) + \dots + 2 + 1 = \frac{N (N - 1)}{2} = O(N^2)
$$

| Best case | Average  | Worst Case |
|-----------|----------|------------|
| $O(N)$    | $O(N^2)$ | $O(N^2)$   |

$$
BUBBLE_SORT(A, N)
$$

Aqui A é um array com N elementos. Esse algoritmo é com ordenação ascendente:

````
set swap := true
set i := 1
repeat steps 4 to 6 while i < n and swap = true:
    set swap := false
    repeat steps for j := 1 to n - i:
        if a[j] > a[j + 1], then:
            (a) set temp := a[j]
            (b) set a[j] := a[j + 1]
            (c) set a[j + 1] := temp
            (d) set swap := true
        [end of if]
    [end of step 5 loop]
    set i := i + 1
[end of step 3 loop]
return   
````




## 3. INSERTION SORTING

