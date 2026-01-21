# Mathematical Notation

## Propositional calculus

Existem dois valores, "TRUE" ou "FALSO". Uma variavel **[booleana](https://google.com   )** (ou propositional) deve tomar somente um desses dois valores

Se $p$ é uma variavel _boolean_, nós escrevemos: "$p$ é $true$", ou simplesmente "$p$" para significar "$p = true$". Isso generaliza as expressões com valores $true$

| Conceito                        | Símbolo / Notação       | Descrição                                                                  |
|---------------------------------|-------------------------|----------------------------------------------------------------------------|
| **Valores de verdade**          | `true`, `false`         | Existem apenas dois valores possíveis: verdadeiro e falso.                 |
| **Variável booleana**           | $p, q$                  | Pode assumir apenas os valores `true` ou `false`.                          |
| **Afirmação “p é verdadeiro”**  | $p$                     | Significa que $p = true$.                                                  |
| **Conjunção (E lógico)**        | $p \land q$             | É verdadeiro somente se $p$ e $q$ forem ambos verdadeiros.                 |
| **Disjunção (OU lógico)**       | $p \lor q$              | É verdadeiro se pelo menos um entre $p$ ou $q$ for verdadeiro.           |
| **Negação (NÃO lógico)**        | $\lnot p$ ou $-p$       | É verdadeiro somente se $p$ for falso.                                     |
| **Implicação (SE...ENTÃO)**     | $p \Rightarrow q$      | É verdadeiro se, sempre que $p$ for verdadeiro, $q$ também for verdadeiro. |
| **Equivalência (SE E SOMENTE SE)** | $p \Leftrightarrow q$ | É verdadeiro se $p$ e $q$ forem ambos verdadeiros ou ambos falsos.         |


> See more: [Propositional](https://google.com)


## Set Theory

- Um **conjunto** é uma coleção não ordenada de elementos distintos.  
- Um conjunto é **finito** se contém um número finito de elementos; caso contrário, é **infinito**.  
- Se $X$ é finito, sua **cardinalidade** é denotada por:  
  $$
  |X|
  $$
- Se $X$ é infinito, podemos escrever:  
  $$
  |X| = \infty
  $$
- O **conjunto vazio**, denotado por:  
  $$
  \varnothing
  $$
  é o único conjunto cuja cardinalidade é 0.

---

### Exemplos de notação

- O conjunto dos primos de um dígito:  
  $$
  {2, 3, 5, 7}
  $$

- O conjunto dos números naturais:  
  $$
  \mathbb{N} = {0, 1, 2, 3, \dots}
  $$

- Se $X$ é um conjunto e $x \in X$, significa que $x$ pertence a $X$.  
- Se $x \notin X$, significa que $x$ **não** pertence a $X$.

---

### Definição por propriedade

- Usando a barra vertical “tal que”:  
  $$
  {n \in \mathbb{N} \mid n \text{ é ímpar}}
  $$

- Outra forma equivalente:  
  $$
  {2n+1 \mid n \in \mathbb{N}}
  $$

---

### Relações entre conjuntos

- **Subconjunto**:  
  $$
  X \subseteq Y \quad \text{se todo elemento de } X \text{ pertence a } Y
  $$

- **Subconjunto próprio**:  
  $$
  X \subset Y \quad \text{se } X \subseteq Y \text{ e } X \neq Y
  $$

- **Igualdade de conjuntos**:  
  $$
  X = Y \quad \Leftrightarrow \quad X \subseteq Y \text{ e } Y \subseteq X
  $$

---

### Operações entre conjuntos

- **União**:  
  $$
  X \cup Y = {z \mid z \in X \text{ ou } z \in Y}
  $$

- **Interseção**:  
  $$
  X \cap Y = {z \mid z \in X \text{ e } z \in Y}
  $$

- **Diferença**:  
  $$
  X \setminus Y = {z \mid z \in X \text{ e } z \notin Y}
  $$

---

### Produto cartesiano

- **Par ordenado**:  
  $$
  (x, y)
  $$

- **Produto cartesiano**:  
  $$
  X \times Y = {(x, y) \mid x \in X, y \in Y}
  $$

- Para potências de conjuntos:  
  $$
  X^2 = X \times X, \quad X^i \text{ para } i > 3
  $$


> See more: [Set Theory](https://google.com)

## Integers, reals and intervals

- O conjunto dos **inteiros** é denotado por:  
  $$
  \mathbb{Z} = \{..., -2, -1, 0, 1, 2, ...\}
  $$

- O conjunto dos **números naturais**:  
  $$
  \mathbb{N} = \{0, 1, 2, ...\}
  $$

- O conjunto dos **inteiros positivos**:  
  $$
  \mathbb{N}^+ = \{1, 2, 3, ...\}
  $$

- O conjunto dos **números reais**:  
  $$
  \mathbb{R}
  $$

- O conjunto dos **reais positivos**:  
  $$
  \mathbb{R}^+ = \{x \in \mathbb{R} \mid x > 0\}
  $$

- O conjunto dos **reais não negativos**:  
  $$
  \mathbb{R}_{\geq 0} = \{x \in \mathbb{R} \mid x \geq 0\}
  $$

---

### Intervalos reais

Se $a, b \in \mathbb{R}$ e $a < b$:

- **Intervalo aberto**:  
  $$
  (a, b) = \{x \in \mathbb{R} \mid a < x < b\}
  $$

- **Intervalo fechado**:  
  $$
  [a, b] = \{x \in \mathbb{R} \mid a \leq x \leq b\}
  $$

- **Intervalo semiaberto à direita**:  
  $$
  (a, b] = \{x \in \mathbb{R} \mid a < x \leq b\}
  $$

- **Intervalo semiaberto à esquerda**:  
  $$
  [a, b) = \{x \in \mathbb{R} \mid a \leq x < b\}
  $$

<note>

Observação: valores $a = -\infty$ ou $b = +\infty$ são permitidos, desde que fiquem no lado aberto do intervalo.

</note>


---

### Intervalos inteiros

Se $i, j \in \mathbb{Z}$ e $i \leq j$:

- **Intervalo inteiro**:  
  $$
  [i..j] = \{n \in \mathbb{Z} \mid i \leq n \leq j\}
  $$

- **Cardinalidade do intervalo inteiro**:  
  $$
  |[i..j]| = j - i + 1
  $$


> See more: [Integers, reals and intervals](https://google.com)


## Functions and relations

Sejam $X$ e $Y$ dois conjuntos. Qualquer subconjunto $p$ do produto cartesiano  
$$
X \times Y
$$  
é chamado de **relação**.  

Quando $x \in X$ e $y \in Y$, dizemos que $x$ está em relação com $y$ segundo $p$, denotado:  
$$
x \; p \; y \quad \Leftrightarrow \quad (x, y) \in p
$$  

Exemplo: a relação “$<$” sobre os inteiros pode ser vista como o conjunto de pares $(a, b)$ tal que $a < b$.

---

### Funções

Uma relação $f$ entre $X$ e $Y$ é chamada de **função** se, para cada $x \in X$, existe **um único** $y \in Y$ tal que $(x, y) \in f$.  

Denotamos:  
$$
f: X \to Y
$$  
e escrevemos $f(x)$ para o único $y$ associado a $x$.  

- O conjunto $X$ é o **domínio** da função.  
- O conjunto $Y$ é o **contradomínio** (imagem).  
- O conjunto  
  $$
  f[X] = \{f(x) \mid x \in X\}
  $$  
  é o **conjunto imagem** ou **alcance** da função.  

Mais geralmente, para $Z \subseteq X$:  
$$
f[Z] = \{f(x) \mid x \in Z\}
$$

---

### Tipos de funções

- **Injetiva (um-para-um)**:  
  $$
  f(x_1) = f(x_2) \;\Rightarrow\; x_1 = x_2
  $$  
  Não existem dois elementos distintos de $X$ com a mesma imagem.

- **Sobrejetiva (sobre)**:  
  Para cada $y \in Y$, existe ao menos um $x \in X$ tal que $f(x) = y$.  
  Equivalentemente:  
  $$
  f[X] = Y
  $$

- **Bijetiva**:  
  $f$ é **injetiva e sobrejetiva** ao mesmo tempo.  
  Nesse caso, existe a **função inversa**:  
  $$
  f^{-1}: Y \to X, \quad f(f^{-1}(y)) = y \quad \forall y \in Y
  $$

---

### Predicados

Dado um conjunto $X$, uma função  
$$
P: X \to \{true, false\}
$$  
é chamada de **predicado sobre $X$**.  

Há uma equivalência natural entre predicados e subconjuntos de $X$:  
$$
\{x \in X \mid P(x)\}
$$  

Exemplo: a propriedade “ser ímpar” é um predicado sobre os inteiros.  
- $P(n) = true$ se $n$ é ímpar.  
- $P(n) = false$ se $n$ é par.  

---

### Fórmulas Booleanas como Predicados

Podemos interpretar fórmulas booleanas como predicados.  

Exemplo:  
$$
P(p, q, r) = (p \land q) \lor (\lnot q \land r)
$$  

Neste caso:  
$$
P(true, false, true) = true
$$

> See more: [Functions and relations](https://google.com)


## Quantifiers

Os quantificadores são símbolos usados para expressar propriedades sobre elementos de conjuntos.

### Principais quantificadores

| Quantificador         | Símbolo             | Leitura                        | Significado                                                                 |
|-----------------------|---------------------|--------------------------------|------------------------------------------------------------------------------|
| Universal             | $$\forall$$         | "para todo"                    | A propriedade vale para todos os elementos do conjunto                      |
| Existencial           | $$\exists$$         | "existe"                       | Existe ao menos um elemento que satisfaz a propriedade                      |
| Existência única      | $$\exists!$$        | "existe exatamente um"         | Há um único elemento que satisfaz a propriedade                             |
| Existência infinita   | $$\exists^\infty$$  | "existem infinitos"            | Há infinitos elementos que satisfazem a propriedade                         |
| Universal infinito    | $$\forall^\infty$$  | "para quase todos"             | A propriedade vale para todos exceto um número finito de exceções           |

---

### Exemplos

- Soma dos primeiros $$n$$ naturais:
  $$
  \forall n \in \mathbb{N}, \quad \sum_{i=1}^{n} i = \frac{n(n+1)}{2}
  $$

- Soma igual a quadrado:
  $$
  \exists! n \in \mathbb{N}^+, \quad \sum_{i=1}^{n} i = n^2
  $$

- Número composto:
  $$
  \exists m, n \in \mathbb{N}, \quad m > 1 \land n > 1 \land mn = 12573
  $$

- Alternância de quantificadores:
  $$
  \forall n \in \mathbb{N}, \quad \exists m \in \mathbb{N}, \quad m > n
  $$

  Mas:
  $$
  \exists m \in \mathbb{N}, \quad \forall n \in \mathbb{N}, \quad m > n
  $$
  é falso, pois não existe um número maior que todos os naturais.

---

### Princípio da Dualidade

- Negação do universal:
  $$
  \neg(\forall x \in X)\, P(x) \quad \Leftrightarrow \quad \exists x \in X\, \neg P(x)
  $$

- Negação do existencial:
  $$
  \neg(\exists x \in X)\, P(x) \quad \Leftrightarrow \quad \forall x \in X\, \neg P(x)
  $$

---

### Predicados {id="predicados_1"}

Um predicado é uma função:
$$
P: X \to \{true, false\}
$$

Exemplo:
$$
P(p, q, r) = (p \land q) \lor (\lnot q \land r)
$$

Então:
$$
P(true, false, true) = true
$$



> See more: [Quantifiers](https://google.com)



## Sums and products

Considere uma função:
$$
f : \mathbb{N} \to \mathbb{R}
$$
e um inteiro $n \geq 0$. (Isso inclui funções do tipo $f : \mathbb{N} \to \mathbb{N}$ como caso especial.)

A soma dos valores assumidos por $f$ nos primeiros $n$ inteiros positivos é denotada por:
$$
\sum_{i=1}^{n} f(i) = f(1) + f(2) + \cdots + f(n)
$$
Essa notação é lida como “a soma de $f(i)$ conforme $i$ vai de 1 até $n$”.

No caso $n = 0$, a soma é definida como 0.

---

### Soma condicional

Se $P$ é uma propriedade dos inteiros, podemos definir:
$$
\sum_{P(i)} f(i)
$$
como a soma dos valores de $f(i)$ para os inteiros $i$ que satisfazem a propriedade $P$.

Exemplo com notação mista:
$$
\sum_{\substack{i=1 \\ i \text{ ímpar}}}^{10} i = 1 + 3 + 5 + 7 + 9 = 25
$$

---

### Produto

O produto dos valores assumidos por $f$ nos primeiros $n$ inteiros positivos é denotado por:
$$
\prod_{i=1}^{n} f(i) = f(1) \times f(2) \times \cdots \times f(n)
$$
Lido como “o produto de $f(i)$ conforme $i$ vai de 1 até $n$”.

No caso $n = 0$, o produto é definido como 1.

---

### Notações adicionais

- $$\log \log n$$ representa o logaritmo do logaritmo de $n$.
- $$\log^2 n$$ representa o quadrado do logaritmo de $n$.

---

### Identidades logarítmicas

- $$\log_a(xy) = \log_a x + \log_a y$$  
- $$\log_a x^y = y \log_a x$$  
- $$\log_a x = \frac{\log_b x}{\log_b a}$$  
- $$x^{\log_b y} = y^{\log_b x}$$

---

### Função piso (floor)

A função piso é denotada por:
$$
\lfloor x \rfloor
$$
e representa o maior inteiro menor ou igual a $x$.

Exemplo:
$$
\left\lfloor \frac{13}{2} \right\rfloor = 6
$$

> See more: [Sums and Products](https://google.com)


## Miscellaneous

### Função piso (floor) {id="fun-o-piso-floor_1"}

A função piso de um número real $x$ é:
$$
\lfloor x \rfloor
$$
Ela representa o maior inteiro menor ou igual a $x$.

Exemplo:
$$
\lfloor -3.5 \rfloor = -4
$$

---

### Função teto (ceiling)

A função teto de um número real $x$ é:
$$
\lceil x \rceil
$$
Ela representa o menor inteiro maior ou igual a $x$.

Propriedade:
$$
x - 1 < \lfloor x \rfloor \leq x \leq \lceil x \rceil < x + 1
$$
para todo $x \in \mathbb{R}$.

---

### Divisão

Se $m \geq 0$ e $n > 0$ são inteiros, então:
$$
\frac{m}{n}
$$
representa a divisão de $m$ por $n$.

Exemplo:
$$
7 \div 2 = \lfloor \frac{7}{2} \rfloor = 3
$$

---

### Operador módulo

O operador módulo é definido por:
$$
m \mod n = m - n \cdot \left\lfloor \frac{m}{n} \right\rfloor
$$

Interpretação: $m \mod n$ é o **resto** da divisão de $m$ por $n$.

---

### Fatorial

Se $m$ é um inteiro positivo:
$$
m! = m \cdot (m - 1)!
$$

Definição especial:
$$
0! = 1
$$

---

### Fórmula de Stirling

Aproximação para o fatorial de $n$:
$$
n! \approx \sqrt{2\pi n} \left( \frac{n}{e} \right)^n
$$

---

### Coeficiente binomial

Para inteiros $n$ e $r$ com $0 \leq r \leq n$:
$$
\binom{n}{r}
$$

Representa o número de maneiras de escolher $r$ elementos de um conjunto com $n$ elementos, **sem considerar a ordem**.


> See more: [Miscellaneous](https://google.com)


## Tabela de Operadores e Funções Matemáticas

| Conceito              | Notação                     | Definição Formal                                                                 | Exemplo                                      |
|-----------------------|-----------------------------|----------------------------------------------------------------------------------|----------------------------------------------|
| Piso (floor)          | $$\lfloor x \rfloor$$       | Maior inteiro menor ou igual a $$x$$                                            | $$\lfloor -3.5 \rfloor = -4$$                |
| Teto (ceiling)        | $$\lceil x \rceil$$         | Menor inteiro maior ou igual a $$x$$                                            | $$\lceil 2.3 \rceil = 3$$                    |
| Divisão inteira       | $$m \div n$$                | $$\lfloor \frac{m}{n} \rfloor$$                                                 | $$7 \div 2 = 3$$                             |
| Módulo                | $$m \mod n$$                | $$m - n \cdot \lfloor \frac{m}{n} \rfloor$$                                     | $$7 \mod 2 = 1$$                             |
| Fatorial              | $$n!$$                      | $$n! = n \cdot (n - 1)!$$ com $$0! = 1$$                                         | $$5! = 120$$                                 |
| Stirling (aprox.)     | $$n! \approx \sqrt{2\pi n} \left( \frac{n}{e} \right)^n$$ | Aproximação para grandes $$n$$                                 | $$10! \approx \sqrt{20\pi} \left( \frac{10}{e} \right)^{10}$$ |
| Coef. binomial        | $$\binom{n}{r}$$            | Número de combinações de $$r$$ elementos entre $$n$$                            | $$\binom{5}{2} = 10$$                        |
| Soma                  | $$\sum_{i=1}^{n} f(i)$$     | Soma dos valores de $$f(i)$$ de $$i = 1$$ até $$n$$                             | $$\sum_{i=1}^{3} i = 1 + 2 + 3 = 6$$         |
| Soma condicional      | $$\sum_{P(i)} f(i)$$        | Soma dos $$f(i)$$ para os $$i$$ que satisfazem a propriedade $$P$$              | $$\sum_{\substack{i=1 \\ i \text{ ímpar}}}^{10} i = 25$$ |
| Produto               | $$\prod_{i=1}^{n} f(i)$$     | Produto dos valores de $$f(i)$$ de $$i = 1$$ até $$n$$                          | $$\prod_{i=1}^{3} i = 1 \cdot 2 \cdot 3 = 6$$ |
| Logaritmo             | $$\log_b x$$                | Único $$y$$ tal que $$b^y = x$$                                                 | $$\log_{10} 1000 = 3$$                       |
| Mudança de base       | $$\log_a x = \frac{\log_b x}{\log_b a}$$ | Conversão entre bases de logaritmo                          | $$\log_2 8 = \frac{\log_{10} 8}{\log_{10} 2}$$ |
| Logaritmo duplo       | $$\log \log n$$             | Logaritmo do logaritmo de $$n$$                                                 | $$\log \log 1000$$                           |
| Logaritmo ao quadrado | $$\log^2 n$$                | Quadrado do logaritmo de $$n$$                                                  | $$\log^2 10 = (\log 10)^2 = 1^2 = 1$$        |


