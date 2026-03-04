# Analysing Algorithms


Analisar um algoritmo tem como objetivo principal **predizer os recursos que o algoritmo requer**

> Devemos considerar os recursos como **memoria**, **conexão com a internet**, ou **consumo de energia** 

Frequentemente, você vai querer mensurar por **tempo computacional** (_computational time_). Se você analisar varios algoritmos candidatos para um problema você pode identificar o mais eficiente.

Antes vocẽ pode analisar um algoritmo, você precisa de um modelo de tecnologia que é rodado, incluindo o recurso dessa tecnologia e o jeito para expressar esse custo; vamos assumir no caso algo generico


## Analysis of insertion sort

Quanto tempo leva i INSERTION SORT? Um jeito de responder isso é rodando no seu computador e notar o tempo que levou para rodar. Claro que você tem que implementar isso em alguma linguagem de programaçã, você não poderia (dependendo) rodar diretamente por um pseudocode (poderia sim, em linguagens como égua)

O que esse tempo de teste diria a você? Simplesmente diria quanto tempo levou para rodar no seu computador, somente teriamos empiricamente o tempo que levou no seu computador, na lib especifica que tu usou na linguagem, os processos que estavam em segundo plano no computador, ou seja, tem muitas particularidades que me impedem de colocar na ponta da caneta e dizer qual é o tempo desse algoritmo desta forma

Assim precusamos de uum jeito para predizer, dada ua nova entrada, quanto tempo insertion sort vai levar

Ao invez de rodar 
