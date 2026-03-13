# Calculate Time and Space Complexity

## 1. Big O notation

Descreve o limite de crescimento
- É como dizer: "esse algoritmo nunca vai ser pior do que isso"

Exemplo: $3n + 2 = O(n)$. Mesmo que tenha o +2, o crescimento principal é linear ($n$)

<note>

Então, por exemplo, se temos um algoritmo com $O(n^2)$ sugere que o tempo de execução aumenta exponencialmente quando $n$ aumenta

</note>


## 2. Ômega Ω

Descreve o limite inferior do crescimento
- É como dizer: "esse algoritmo sempre vai gastar pelo menos isso"

Exemple: $3n + 2 = Ω(n)$. Ele nunca vai ser menor que algo proporcional a $n$


## 3. Teta Θ

Combina os dois, é o crescimento exato (quando superior e inferior coincidem)

> O ponto central dessas notações é o crescimento. Na análise assintótica, ignoramos constantes (como o "+2" do seu exemplo) e termos de menor ordem, porque conforme $n$ se torna muito grande, o termo de maior ondem (como o $n$ ou $n^2$) domina completamente o custo total

