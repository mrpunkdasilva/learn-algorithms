# What is Algorithm?
## Alguns passos antes de definirmos
A palavra "algoritmo" remonta eras da antiguidade até os dias atuais, sua origem se data por causa do matematico persa, Muhammad Al-Khwarizmi, que é conhecido como "pai da álgebra" e que a palavra "algoritimo" vem de seu nome latinizada

## Agora caminhamos a definição

De maneira direta e informal, um algorítimo é qualquer procedimento computacional bem definido que toma alguns valores ou um conjunto de valores, como **input** (entrada) e produz alguns valores ou um conjunto de valores como **output** (saída) em um tempo finito 

_Figura 1: Diagrama representativo do que seria um algoritimo_
![Figura 1: Diagrama representativo do que seria um algoritimo](algoritmos)

Temos também uma visão mais ferramental, de que um "algoritimo" é uma ferramenta para resolver problema computacionais especificos

A descrição do problema especifica em termos gerais a relção da entrada/saida para as instâncias do problema

O algoritimo descreve um procedimento computacional especifico  para atingir um relacionamento de entrada e saida para todas as instâncias do problema

Vamos a um exemplo, suponha que você precisa organizar uma sequência de números numa ordem crescente monotonica. Vamos fazer a formalização desse algoritimo de ordenação:

| **Input:**  | Uma sequência de $n$ números $\langle a_{1}, a_{2}, \dots, a_{n} \rangle$                                                                             
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Output:** | Uma permutação (reordenação) $\langle a_1', a_2', \dots, a_n' \rangle$ de uma sequência de entrada em que $a_{1}' \leq a_{2}' \leq \dots \leq a_{n}'$ |

Isso nos dá uma sequência de entrada $\langle 31,41,59,26,41,58 \rangle$, assim temos uma saída o conjunto desses valores ordenados corretamente $\langle 26, 31,41,41,58,59 \rangle$

<note>

Essa sequência de entrada é chamada de **instância** do problema de ordenação

Em geral, uma **instância de um problema** $^1$ consiste de uma entrada (satisfazendo todas as regras que a declaração daquele problema possui) precisa para computar uma solução para o problema



> $^1$ Por vezes, quando o problema é conhecido, instâncias de problemas são apenas chamados de problemas


</note>

Com os muitos programas que existem como um passo intermediario, ordenar é uma operação fundamental na **ciência da computação** 

Como resultado, temos um grande número de bons algoritimos de ordenação a disposição que foram e são usados e testados 

Lembrando que cada um desses algoritimos tem suas caractericas e elas apontam se o algoritimo é bom para ser usado em determinado problema, considerando alguns fatores, como:
- o número de itens para ser ordenado
- a extensão dos valores
- a arquitetura do computador
- procedure tipo de dispositivo de armazenamento para ser usado:
  - memoria principal
  - disco
  - dispositivos mais arcaicos 

Um algoritimo para um problema computacional é **correto** se, para cada instância do problema provida com entradas, paradas e finalização em tempo finito e a saída correta para a instância do problema. 

- Um algoritimo correto **soluciona** o problema computacional
- Um algoritimo incorreto para em algumas entradas de instâncias, ou ele deve parar com uma resposta incorreta

<note>

Indo na contra-mão do que se pensa, algoritimos incorretos podem ser uteis as vezes, se você pode controlar sua porcentagem de erro

</note>

Um algoritimo pode ser especificado em ptbr ou inglês, como um programa de computador, ou como um hardware design. O único requisito é que a especificação deve prover uma descrição precisa do procedimento computacional a ser seguido

Além do que podemos pensar existem algoritmos que não são **[algoritmos deterministico](#)**, que input tem um output previsto, já que algumas funções podem gerar saídas aleatórias assim temos os **[algoritmos probabilisticos](#)**

<note>
O ponto importante aqui é que "aleatório" não significa arbitrario, pelo contrario, nós usamos valores escolhidos de modo que a probabilidade dos valores escolhidos seja conhecida e controlada 
</note>

Uma instrução como "escolha um número entre 1 e 6" de modo que não tem detalhes dados, isso não é aceitavel num algoritmo. Portando, para ser aceitavel precisaria ter mais informações e ser dito deste modo: "escolha um número entre 1 e 6 de modo que cada valor possa ter a mesma probabilidade de ser escolhido"

Quando nós usamos um algoritmo para calcular a resposta para um problema particular, nós usualmente assumimos que as regras vão, se aplicadas corretamente vai gerar a resposta correta. Um conjunto ode regras que calcula que $23 \times 51 = 1170$ isso não é geralmnete util na pratica. Se queremos calcular a $\sqrt{2}$ para uma instância, não teremos algoritmos que podem nos ajudar com uma resposta exata na notação decimal

Nesse caso, nós devemos nos contentar if um algoritmo pode nos dar uma resposta que é precisa com a nossa escolha: 4 casas de precisão ou 10 casas, ou qualquer nos interesse

Existem problemas para os quais não se conhecem algoritmos práticos. Para esses problemas usamos um dos algoritmos disponiveis para encontrar a resposta exata o que na maioria dos casos toma muito tempo. Quando isso acontece nós somos obrigados, se for preciso a termos um tipo de solução para o problema, buscando um conjunto de regras que nos da uma boa aproximação a resposta correta e que nós podemos executar em um tempo razoavel. Se nós podemos provar isso a resposta computada pelo conjunto de regras não está muito errada, ou então muito melhor. Algumas vezes isso não é possivel e podemos contar com a boa sorte

Esse tipo de procedimento baseado no otimistmo e frequentemente com o suporte teorico minimo é chamado de "**[algoritmo heuristico](#)**", ou simplesmente, "**heuristica**"    

<note>
Assim heurística seria uma solução que se volta a prática, ou seja, é pragmatica utilizando conhecimentos do senso comum e "regras de bolso" para se ter a prática e velocidade em troca da perfeição
</note>







