# Introduction of Array

Um array é uma lista finita de elementos de mesmo tipo

Os arrays podem ser classificados como:

- uni-direcional ou linear que requer somente um indice para acessar um elemento individual de um array
- Bidirecional são arrays que requer dois indices para acessar um elemento individual e isto é chamado de _matrix_
- Multi-dimensional são arrays que precisamos de mais de dois indices para acessar um elemento

## Linear

- Os elementos de uma array são referenciados por um conjunto de indices consistente de $n$ consecutivos números inteiros

- Os elementos de um array são armazenados respectivamente em localizações na memoria

- O número $n$ de elementos é chamado de _size_ (tamanho do array). Se não explicitarmos vai ser assumido que o valor é um inteiro $1,2, \dots, n$

No geral o tamanho ou o número dos elementos de um array pode ser obtido do indice por essa fórmula:

$$
N = UB - LB + 1
$$

Temos $A$ é o endereço base (nome do array)

$$LB \text{é o Lower Bound (limite inferior)}$$

$$UB \text{é o Upper Bound (limite superior)}$$

- Por exemplo:

$LB$ é o limite inferior ex: 1

$$\text{Base address} = 200$$

Encontrar o endereço do 3° elemento $Loc(A[K])$

$W = \text{numero de celulas de memória para um unico} elemento$

$Loc(A[K]) = base(A) + W \times (K - LB) = 200 + 2 \times (3 - 1) = 204$

### ADT Array

Um array é uma coleção de elementos homogeneos:

- Nós podemos acessar cada elemento por um indece númerico
- Cada elemento é referenciado com um index e se normalmente se inicia com o valor 0 no indice 
- Array é armazenado na memoria em locais conjuntos

### Operations on Linear Array:

- Transversing
- Searching
- Insertion
- Deletion
- Merging
- Sorting

#### 1. Transversing

Transversing é o processo de visitar cada elemento de um array exatamente uma vez. Os elementos só podem ser acessados diretamente se nós varrermos do indice do limite inferior até o limite superior em passos de um a um para acessar individualmente os elementos em ordem

Para um array de size $n$, o loop é executado $n$ vezes para que a operação de transversing seja executada com exit em linear arrays a operação é O(n)

$$TRANSVERSE(ARR, LB, UB)$$

Temos que $ARR$ é um linear array com lower bound (LB) e upper bound (UB). Esse algoritmo transverse ARR aplica uma operação PROCESS para cada elemento de LA:

```
Passo 1.    Set K := LB [initialize counter]
Passo 2.    Repeat steps 3 and 4 while K <= UB
Passo 3.    Apply PROCESS to A[K] [visit element]
Passo 4.    Set K := K + 1 [increase counter] [fim do passo 2]
Passo 5.    Exit
```

