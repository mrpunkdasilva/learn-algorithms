# The efficiency of algorithms

Quando nós temos um problema para resolver, existem diversas opções de algoritmos para resolver. Isso levanta questão de como decidir qual algoritmo deve ser preferido

<warning>
Se tivermos somente uma ou duas pequenas instâncias de um problema simples, não precisamos nos preocupar muito sobre qual algoritmo escolher: assim nossa escolha se resume simplesmente no mais fácil para programar ou o qual já existe programado, sem ficar se martirizando a cerca de questões teóricas
</warning>


- A abordagem _**empirical**_ (ou _a posteriori_) para escolher um algoritmo consistem de programar as técnicas concorrentes e tentar nas diferentes instâncias com ajuda do computador

- A abordagem **_theoretical_** (ou a _a priori_) consiste de determinar matematicamente a quantidade de recursos necessarios para cada algoritmo como **uma função do tamanho de uma instância considerada**

Os recursos de mais interesse são tempo de computação e espaço de armazenamento

Ao longo dos _Domus_ vamos comparar os algoritmos com base em sua _eficiencia_ que é o quão rapido ele executa. Somente em alguns casos que vamos nos preocupar com requerimentos de armazenamento. ou pensar em outros recursos

<note>
Um desses exemplos de outro requerimento são número de processadore, pensariamos nisso se estivessemos precisando de algoritmo paralelos e também artificial ou uma combinação
</note> 

O tamanho de uma **instância corresponde formalmente ao número de bits necessarios para representar a instância no computador**, usando algum modelo de código definido precisamente e compacto. Entretando para fazer nosa analise clara, usualmente somos menos formal, então usamos a palavra "size" para significar algum intereiro que de alguma forma mensuramos o número de compponentes numa instância. Por exemplo, quando nós falamos sobre ordenação, usualmente nós medimos o tamanho de uma instância pelo número de itens para ser ordenado, ignorando o fato que cada um desses itens deveria tomar mais que um bit para representação no computador. 

Similarmente, quando nós falamos sobre grafos, nós usualmente mensuramos o tamanho de uma instância pelo número de nós e arestas (ou ambos) envolvidos. 

No entanto quando nos afastamos dessa regra geral, quando falamos de problemas envolvendo inteiros, nós devemos algumas vezes temos que lidar com a eficiencia de nossos algoritmos em termos de valor da instância a ser considerada, tratando então o tamanho (que deve ser o número de bits necessarios para representar esse valor em binario)

**A vantagem da abordagem teorica é que isso não depende do computador sendo usado, da linguagem de programação, alguma skill de programação**. Salva ambos o tempo que poderia ter sido gasto desnecessariamente um algoritimo ineficiente e o tempo da máquina que poderia ser gasto testando. Mais significante, isso nos permite estudar a eficiencia dde um algoritmo quando usado numa instância de qualquer tamanho

Isso não é frequentemente o caso com o **empirical approach, onde considerações praticas deve forçar a gente a testar nosso algoritmo somente com um pequeno numero de instâncias arbitrarias escolhidas de tamanho moderado**. A partir disso frequentemente tem novas descoberdas de algoritmos novos para performar melhor que o predecessor somente quando ambos usam grandes instâncias, esse último ponto é particularmente importante

Também podemos analisar algoritmos usando o **_hybrid approach_**, que consistem na forma da função de descrever a eficiencia do algoritmo é determinada de modo teorico

Usando essa abordagem podemos predizer o tempo que uma implementação real vai levar para resolver uma instância muito larga que será usada nos testes. Entretanto claro que não podemos extrapolar quebrano as considerações teoricas; predições feitas sem o suporte da base teorica serão imprecisas, se não erradas. 

| **Abordagem**        | **Características**                                                                 | **Vantagens**                                                                                           | **Limitações**                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **Teórica**           | Baseada em análise matemática e independente de computador, linguagem ou skill.     | Não depende da máquina ou linguagem.<br>Economiza tempo evitando algoritmos ineficientes.<br>Permite estudar eficiência em qualquer tamanho de instância. | Pode ser abstrata demais.<br>Nem sempre reflete o desempenho real em implementações práticas. |
| **Empírica**          | Testa algoritmos em instâncias escolhidas e observa desempenho real.                | Dá resultados práticos e observáveis.<br>Pode revelar diferenças de desempenho em instâncias grandes. | Normalmente limitado a instâncias pequenas/moderadas.<br>Pode não capturar comportamento em larga escala. |
| **Híbrida**           | Combina análise teórica com testes práticos; usa funções teóricas para prever tempo. | Permite prever desempenho em instâncias muito grandes.<br>Une rigor teórico com validação prática.    | Extrapolações sem base teórica podem ser imprecisas.<br>Requer equilíbrio entre teoria e prática. |

Se quisermos mensurar o quanto de armazenamento um algoritmo usa como uma função do tamanho de instâncias, existe uma unidade natural para nós, nomeada de _bit_.

Independente da máquina sendo usada, a noção de bit do armazenamento é bem definido. Se na outra mão , como é mais frequente o caso, **nós queremos mensurar a eficiencia de um algoritmo pelo tempo que demora para chegarmos a uma resposta**, não existe uma escolha obvia

Uma resposta para esse problema é dado pelo _principio da invariância_, possuindo dois estados diferentes do mesmo algoritmo não vai diferir na eficiencia para mais que alguma contante multiplicativa,

Por exemplo, se essa constante for de 5, então nós sabemos que se a primeira implementação leva 1 segundo para solucionar instâncias de tamanho particular então a segunda implmentação não vai levar mais que 5 segundos para solucionar as mesmas instâncias

> Mesmo que talvez esteja sendo usado uma maquina diferente, ou escrito em uma linguagem de programação diferente

Sendo mais preciso e formal, se duas implementações do mesmo algoritmo tomam $t_{1}(n)$ e $t_{2}(n)$ segundos, respoectivamente para solucionar uma instância de tamanho $n$ então existem sempre uma constante positiva $c$ e $d$ também temos $t_{1}(n) \leq ct_{2}(n)$  e $t_{2}(n) \leq dt_{1}(n)$ qualquer $n$ é suficientemente largo 

Em outras palavras, o tempo de execução da implementação é limitado pela por uma constante multiplicativa de tempo de execuçãodo outra, a escolha de qual implementação vai primeiro ou segundo é irrelevante

A condição que $n$ seja suficiente larga não é realmente necessaria:  
