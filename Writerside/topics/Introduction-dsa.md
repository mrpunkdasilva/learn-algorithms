# Introduction DSA

## Intro

Uma estrutura de dados é uma maneira estruturada de organizar e armazenar dados na memória do computador, assim essas estruturas possuem operações que são básicas entre elas e que são usadas para manipular esses dados 

Uma estrutura de dados signifca que existe uma relação entre os dados e está relação determina qual tipo de data structure está sendo usada


### Data

Um valor ou um conjunto de valores


### Data Item 

Um data item é uma única unidade de valores, por exemplo: o número de milfs no milfsgo, data de nascimento, cidade, zip, etc

- Grupo de itens: os data items podem ser divididos entre sub-itens que são chamados grupo de itens. Por exemplo: um endereço é um grupo de itens que podem ser divididos em sub itens, como: número da casa, rua, etc

- Itens elementares: data items que não podem ser divididos em sub itens são por exemplo: número da casa, cidade, etc

### Entity

Entidade (Entity) é algo que tem certos atributos ou propriedades, dos quais podem ser atribuidos valores. Por exemplo: cafetão é uma entidade que possui seus atributos/propriedades 

> Estas duas palavras _atributos_ e _propriedades_ tem o mesmo significado, elas são sinonimos 


### Field

Um field (campo) é um atributo/propriedade de uma **[Entidade](Introduction-dsa.md#entity)**, dentro do MilfsGO temos a entidade **MILF**, que por sua vez possui campos como: nome, idade, etc e estes data são atributos que é o mesmo que dizer que são fields 

### Key

A key é um data item num record (_registro_) que são valores únicos e podem ser usados para distinguir um record de outros records. No MilfsGO encontrariamos uma **key** como o ID de uma Milf
- Já que o valor do data item seria único e seria usado para distinguir uma Milf da outra

> Nós podemos usar somente um data item como chave, assim temos o **primary key**, mas dependendo do problema teremos outras chaves conhecidas com _alternative keys_

### Information 

A informação pode ser confundida com data, mas quando falamos de informação falamos de uma dado que possui significado, que não só possui um valor como: o nome da uma Milf é só um dado, mas quando atribuimos a ele relação com outros dados temos signifcado e assim temos uma informação

> Assim: a informação é o dado processado e o dado é apenas a coleção de valores (raw data) 

Os dados não são uteis para tomar decisões, mas quando processamos o dado geramos informação e logo isso se torna útil
