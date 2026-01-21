# Insertion Sort

No [Domus](WhatsALgorithms.md#agora-caminhamos-a-defini-o) passado, o algoritmo que usamos para solucionar o problema de ordenação:

| **Input:**  | A sequência de $n$ números $\langle a_{1}, a_{2}, \dots, a_{n}$                                                                                          |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Output:** | A permutação (reordenação) $\langle a'_{1}, a'_{2}, \dots, a'_{n}\rangle$ da sequência de entrada resulta em $a'_{1} \leq a'_{2} \leq \dots \leq a'_{n}$ |

Os números para serem ordenados são também conhecidos como as chaves. Claro que como o problema é de ordenação a entrada vem como array com $n$ elementos, quando estamos ordenando valores numericos costuma que usamos um dado associado as chaves (**keys**) que são chamadas de **satellite data** (dados guia). Juntos a key e o satellite data de um registro.

Por exemplo, considere uma spreadsheet contendo registro de estudantes com muitos pedaços de dados associados como: idade, pontuação média, número de cursos, etc. Qualquer uma dessas quantidades podem ser uma key, mas quando 
 a spreadsheet ordenada, os registros associados (o satellite data) com a key . Quando descrevemos um algoritmo de ordenamento, nós focamos nas keys, mas é importante para lembrar que eles usualmente estão associadados ao satellite data

> O Insertion é bom para um conjunto de valores pequenos 

## Pseudocode

```
for i = 2 to n
    key = A[i]
    
    j = i - 1
    while j > 0 and A[j] > key
        A[j + 1] = A[j]
        j = j - 1
    A[j + 1] = key
```

## Invariantes de Loop

A figura abaixo mostra como o algoritmo funciona para um array A, que inicia com a sequência: $\langle 5, 2, 4, 6, 1, 3 \rangle$. O indice $i$ indica a carta atual sendo iserida na mão. No começo de cada iteração do loop **for**, que é indexado pelo $i$, o subarray (uma porção contigua do array) consiste de elementos $A[1:i-1]$ que é $A[1]$ a $A[i-1]$ constiutue os atuais elementos ordenados na mão e o restande subarray $A[i+1: n]$ elementos $A[i + 1]$ a $A[n]$ correspondendo a pilha de cardas que estão na messa. De fato, elementos $A[1: i-1]$ são os elementos originalmente em posições 1 a i - 1, mas agora na ordem dos ordenados. Nós chamamos essas proprioedades de $A[1:i - 1]$ formalmente como **_loop invariant (invariantes de loop)_**

_Figura representativa do algoritmo de insertion sort:_

![Figura a cerca do Insertion Sort](image.png)



Loop invariants nos ajuda a entender porque um algoritmo é correto. Quando você usa um loop invariant, você precisa mostrar 3 coisas:

**Initialization:** É a primeira iteração do loop







