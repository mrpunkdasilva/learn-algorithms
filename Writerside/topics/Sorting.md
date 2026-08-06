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









## 3. INSERTION SORTING

A ordenação por inserção é ordenar um conjundo de registros num arquivo já ordenado. Se o arquivo inicial for odernado, apenas uma comparação é feita em cada passagem. Então essa ordenação tem complexidade $O(N)$. Se o arquivo é inicialmente ordenado na ordem reversa, a ordenação é de $O(N^2)$

Quanto mais próximo o arquivo tiver ordenado, mais eficiente se torna a ordenação simples por insertion

A média do número das comparações numa simples insertion sort (por considerar todas as possibilidades de permutação de um input de array) é também $O(N^2)$

O espaço requerido para essa ordenação consiste de somente uma variavel temporaria. **Ambos selection sort e simple insertion sort são mais eficientes que o bubble sort**. Selection sort requer mais atribuições que insertion sort, mas mais comparações

> o algoritmo de insertion sort é um algoritmo devagar se $n$ for muito grande. Insertion sort é normalmente usado quando $n$ é menor. Esse algoritmo é muito popular como uma ponte entre os jogadores quando eles fazem a primeira ordenação das cartas. Nesse procedimento, nós escolhemos um valor particular e então inserir ele no lugar apropriado na sub lista ordenada


A performance do pior caso ocorre quando os elementos do input array são em ordem descendente. A primeira passagem faz 1 comparação, a segunda passagem faz 2 e a terceira faz $N - 1$ comparações: 

$$
1 + 2 + \dots + (N - 2) + (N - 1) = \frac{N(N - 1)}{2} = O(N^2) 
$$


| Best case | Average  | Worst Case |
|-----------|----------|------------|
| $O(N)$    | $O(N^2)$ | $O(N^2)$   |


$$
INSERTION_SORT(A, N)
$$

Aqui A é um array com N elementos. Esse algoritmo ordena o array A com N elementos em ordem ascendente

```
repeat steps 2 to 5 for i = to n:
    set item := a[1]
    set j := i - 1
    repeat steps while j >= 1 and a[j] > item:
        (a) set a[j+1] := a[j] [moves element forward]
        (b) set j := j - 1 
    [end of step 4 loop]
    set a[j + 1] := item [inserts element in proper place]
[end of step 1 loop]
return
```



## 4. SHELL SORTING

É também chamado de **diminishing increment sort**, nomeado depois e descoberto shell sort algorithm prove mais significante melhorias do que o simple insertion sort 

Esse metodo separa ordenadamente sub arquivos do arquivo original. Esses sub arquivos contem cada k elemento do arquivo original. O valor de k é chamado de incremento ou um gap 

A ideia por trás do shel sort é uma só e simples. Nós já temos noteado que o simples insertion sort é altamente eficiente no arquivo que está quase todo ordenado. É também importante para realizar que quando o tamanho do arquivo n é pequeno um ordenamento $O(N^2)$ é mais frequentemente eficiente que um ordenamento $O(N log N)$ 

A razão para isso é que ordenamentos $O(N^2)$ são geralmente bem simples de programar e envolve muitas poucas ações que outras comparações e trocas em cada passagem 

Um ordenamento $O(N log N)$ é geralmente mais complexo e emprega um grande número de operações extras em cada passagem na ordem para reduzir o trabalho de passagem subsequentes

Quando n é grande $(N log N)$ é melhor que ($N^2$). Entretanto quando n é pequeno (N^2) e não muito grande que ($N log N$), então uma grande diferença nessas constantes frequentes causam um ordenamento $O(N^2)$ para ser mais rápido

Desde o primeiro incremento usado pelo shell sort é grande, os sub arquivos individuais são menores que um simples insertion ordena nesses sub arquivos são relativamente rápidos. Cada ordenação de um sub arquivo fique mais próximo de estar mais ordenado

Isso, sucessivamente passa do shell sort usa pequenos incrementos e por tanto lidar com grandes sub arquivos esses sub arquivos são quase ordenados até para a ação de passagens anteriores. Assim o insertion sort nesses sub arquivos são muito eficientes 

Nessas conexões é significante notar que se o arquivo é parcialmente ordenado usando um incremento k e é subsequente parcialmente ordenado usando um incremento j, o arquivo continua parcialmente ordenado no incremento k. Que é subsequente parcial ordenado para não distorcer os anteriores

O atual tempo requerido para um ordenamento especifico depende do número de elementos no array incrementados e nos seus valores atuais. Quando o intervalo é igual a 1, o array é também sorteado. Isso tem sido mostrado que a ordenação de shell sort pode ser aproximada por $O(n (log n)^2)$ se uma sequencia apropriada de incrementos é usada. Em geral o shell sort é recomendado para arquivos que tem inumeros elementos


| Best case        | Average         | Worst Case      |
|------------------|-----------------|-----------------|
| $O(N (log N^2))$ | $O(N(log N)^2)$ | $O(N(log n)^2)$ |


$$
SHELL_SORT(A, N)
$$


```
set span = n/2 [initialize]
repeat steps from 3 to 5 while span >= 1:
    set i := span + 1
    repeat steps while i <= n:
        (a) set item := a[i]
        (b) set j := i - span
        (c) repeat steps while j >= 1 and a[j] > item:
            set a[j + span] := a[j] [shifting]
            set j := j - span
        [end of step (c) loop]
        (d) set a[j + span] := item[insert] 
        (e) set i := i + 1 [end of step 4 loop]
    set span := span / 2
[end of step 2 loop]
return
```


## 5. MERGE SORTING




