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

Similarmente, quando nós falamos sobre grafos, nós usualmente mensuramos o tamanho de uma instância pelo número de nós e arestas (ou ambos) envolvidos
