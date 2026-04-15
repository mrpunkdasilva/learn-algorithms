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



