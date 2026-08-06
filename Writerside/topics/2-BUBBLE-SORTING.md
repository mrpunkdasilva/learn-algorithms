# 2. BUBBLE SORTING:
1. Verifica se nos dois primeiros valores, o menor valor está na primeira posição, se sim não troca senão troca
2. Pega o segundo valor e vai fazendo as comparações se ele é o maior que o antecessor, se ele for troca senão for não troca, isso eu vou fazendo até o final
3. Assim eu faço comparações e trocas para cada elemento um por vez

![image_2.png](image_2.png)



> Nesse tipo de algoritmo, o número de trocas não pode ser maior que o número de comparações

Uma das questões desse tipo de ordenação é que ele precisa de um espaço adicional, um armazenamento adicional para valores temporarios para as trocas e algumas variaveis inteiras simples, e isso é O(N) no caso em que o arquivo é completamente ordenado ou a maioria é ordenado

Isso segue de uma observação que somente uma passagem de (N-1) comparações (e não mudanças) é necessario para estabelecer que o arquivo ordenado está ordenado. Bubble sort tem uma propriedade muito importante: 

- E é um algoritmo que não é bom para listas grandes já que é mais lento

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



