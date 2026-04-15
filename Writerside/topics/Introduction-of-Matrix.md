# Introduction of Matrix

Um array bidirecional é uma lista de números finitos de dados homogeneo, como também:
- Os elementos do array são referenciados por dois conjuntos consistindo de m e n consecutivamente números inteiros
- Os elementos do array são armazenados em localizações consecutivas na memoria
- O tamanho do array bidimensional é denodado por $m \times n$


## Representação de um array bidimensional na memoria:

Sendo A um uma metrix bidimensional de tamanho $m \times n$. Podemos representar A como um retangulo padrão com m linhas e n colunas 


O array será representado na memoria por um bloco de $m \times n$ localização sequencial de memoria. Entretanto o leemnto pode ser armazenado em duas formas diferentes:

1. **COLUMN MAJOR ORDER:**

Os elementos são armazenados colunas por coluna: os m elementos da primeira coluna são armazenados na primeira m localização, elementos da segunda coluna são armazenados na próxima na coluna na localização m e assim por diante

2. **ROW MAJOR ORDER:**

Os elementos armazenados linha por linha: os n lementos da primeira linha são armazenados na primeira n localização, elementos da segunda linha são armazenados na próxima n localização e assim por diante


**_Imagem repreesntando essas duas formas de armazenamento:_**

![Column Major e Row Major Order](Column Major e Row Major Order)


## O endereço LOC(A[J,K]) de um array pode ser obtido pela formula:


### Row-Major Order:

$$
LOC(A[J,K]) = BASE(A) + W * [N * (J - LB) + (K - LB)]
$$


### Column-Major Order:

$$
LOC(A[J, K]) = BASE(A) + W * [N * (J - LB) + (K - LB)]
$$


Onde W = número de celulas da memoria para um unico elemento

Uma matrix $m \times n$ é uma bidimensional. Cujo m,n elementos são arranjados em m linhas e n colunas

Uma matrix é denotada pela letra maiuscula como A, B, C... e os elementos são correspondentemente letras minusculas sufixadas com indices de linha e colunas como: A(j,k), B(j,k)...


## Tipos de matrix

| **Tipo de Matriz** | **Definição** | **Exemplo Simplificado** | **Observações** |
|---------------------|---------------|---------------------------|-----------------|
| Matriz Diagonal | Apenas os elementos da diagonal principal são diferentes de zero. | $$\begin{bmatrix}1 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 3\end{bmatrix}$$ | É sempre uma matriz quadrada. |
| Matriz Tridiagonal | Elementos não nulos apenas na diagonal principal e nas diagonais imediatamente acima e abaixo. | $$\begin{bmatrix}1 & 2 & 0 \\ 3 & 4 & 5 \\ 0 & 6 & 7\end{bmatrix}$$ | Usada em sistemas lineares e métodos numéricos. |
| Matriz Triangular Inferior | Todos os elementos acima da diagonal principal são zero. | $$\begin{bmatrix}1 & 0 & 0 \\ 2 & 3 & 0 \\ 4 & 5 & 6\end{bmatrix}$$ | Importante em decomposições LU. |
| Matriz Triangular Superior | Todos os elementos abaixo da diagonal principal são zero. | $$\begin{bmatrix}1 & 2 & 3 \\ 0 & 4 & 5 \\ 0 & 0 & 6\end{bmatrix}$$ | Também usada em decomposições LU. |
| Matriz Esparsa | A maioria dos elementos é zero. | $$\begin{bmatrix}1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 2 & 0\end{bmatrix}$$ | Economiza memória e processamento. |
| Matriz Densa | Poucos ou nenhum elemento são zero. | $$\begin{bmatrix}1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9\end{bmatrix}$$ | O oposto da matriz esparsa. |
| Matriz Identidade | Diagonal principal composta apenas por 1, e o restante por 0. | $$\begin{bmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{bmatrix}$$ | É o “neutro” da multiplicação de matrizes. |
| Matriz Simétrica | É igual à sua transposta (\(A = A^T\)). | $$\begin{bmatrix}1 & 2 & 3 \\ 2 & 4 & 5 \\ 3 & 5 & 6\end{bmatrix}$$ | Muito usada em álgebra linear e estatística. |


## Matrix operation

1. Soma
2. Multiplicação
3. Transposição
4. Ordenação


## TRANSPOSE (SM1, SM2)

Aqui SM1 e SM2  são duas matrizes esparsas. Esse algoritmo computa a transposições de SM1 para SM2. N é o número de elementos não zeros. A linha do cabeçalho é 0


```
1.  Set MAXROW := SM1[0, 2], MAXCOL := SM1[0, 3], N := SM1[0,1]
2.  Set SM2[0 ,1] := N, SM2[0, 2] := MAXCOL, SM2[0 ,3] := MAXROW
3.  If N > 0, then: [if number of non zero elements are more than 0]
4.      Set I := 1[I is a counter for SM2]
5.  Repeat step 6 for COL := 1 to MAXCOL [counter for counting columns]
6.      Repeat step (a) for P := 1 tp N [Counter to SM1]
            (a) If SM1[P, 3] := COL, then:
                (i)   SM2[I, 1] := SM1[P, 1]
                (ii)  SM2[I, 2] := SM1[P, 2]
                (iii) SM2[I, 3] := SM1[P, 3]
                (iv) Set I := I + 1 [End of if structure] [End of step 6 loop] [end of step 5] 
7. Exit
```

