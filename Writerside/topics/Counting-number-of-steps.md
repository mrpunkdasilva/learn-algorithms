# Counting number of steps

* **Método de Contagem**: Introduz-se uma variável global `count` (inicialmente 0) que é incrementada a cada instrução
  executada para medir o custo computacional.
*
* **Análise do Código**:
    1. **Inicialização**: A instrução `s := 0` conta como **1 passo**.
    2. **Loop `for`**: Para uma entrada de tamanho $n$, o corpo do loop é executado $n$ vezes. Dentro dele, há dois
       incrementos (um para a lógica do loop e outro para a soma `s := s + a[I]`), totalizando **$2n$ passos**.
    3. **Finalização**: Ocorre mais **1 passo** para a última verificação da condição do loop (quando ela se torna
       falsa) e **1 passo** para a instrução de retorno `return s`.
* **Resultado**: O total de passos é **$2n + 3$**, o que caracteriza uma **taxa de crescimento linear**, classificada
  assintoticamente como **$O(n)$**.

```c
Algorithm Sum(a, n)
{
     s:= 0
     count := count + 1 [count is global it is initially zero.]

     for I: = 1 to n do
     {
         count := count + 1  [ for FOR loop ]
         s := s + a[I]
         count := count + 1  [ for s ]
     }
     
     count := count + 1[for last time of for]
     count := count + 1[for the return]
     
     return s
}
```

<note> 

Vamos buscar entender o porque do $2n + 3$, ese valor surge da contagem de cada operação (ou "passo") que o computador
realiza ao executar o algoritmo que temos

**1. O "+ 1" inicial (Inicialização):**

Antes de entrar no loop, o algoritmo executa a instrução `s := 0`. Logo abaixo dela, existem um comando explicito para
incrementar o contador: `count := count + 1`. Isso representa **1 passo**

**2. O "$2n$" (o corpo do loop)**

O loop `for` é configurado para rodar de 1 até $n$. Iso significa que o que estiver dentro dele será repetido $n$ vezes.
Dentro de cada uma dessas repetições, o código faz o seguinte:

- Incrementa `count` uma vez para a mecânica do próprio loop `for`
- Realiza a soma `s := s + a[i]`
- Incrementa `count` uma segunda vez após a soma. Como são dois incrementos realizados em cada uma das $n$ voltas,
  temos $2n$, resultado em $2n$ passos

**3. O "+1" da saída do loop**

Em loops `for` ou `while`, a condição de teste é executada **uma vez a mais** do que o corpo do loop que é o momento em que o programa percebe que a condição é falsa e deve sair

No código acima, isso está marcado explicitamente pela linha do `count := count + 1[for last time of for]`, adicionando mais 1 passo

**4. O "+1" final (retorno)**
A última instrução do algoritmo é o `return s`. O código inclui um incremento final logo antes dessa linha:
`count := count + 1[for the return]`

**Assim, temos:**

- $1$ (inicialização)
- $+ 2n$ (repetição do loop)
- $+1$ (verificação final para sair do loop)
- $+1$ (operação de retorno)

$$Total = 2n + 3$$


</note>