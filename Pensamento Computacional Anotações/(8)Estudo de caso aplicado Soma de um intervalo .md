# Estudo de caso aplicado: Soma de um intervalo

Vamos supor que temos que somar os números no intervalo de 1 e 200.

Primeiro decompomos o problema, podemos somar o menor com o maior numero, e nas somas seguintes decrementar o maior número em 1 e incrementar o menor número em um.

200 + 1

199 + 2

198 + 3

197 + 4…

Com isso obtemos um padrão

200 + 1 = 201

199 + 2 = 201

198 + 3 = 201

197 + 4 = 201…

Agora podemos utilizar a abstração.

Verificamos quantas vezes esse padrão ira se repetir ao longo do intervalo, como são 200 números e ambos os lados da soma se aproximam de si de forma igual, teremos que o valor de repetição = 200/2

Ou seja 100.

Com essa informação podemos multiplicar o numero de repetições pelo valor da soma repetido:

201 * 100 = 20.100 (Resultado da soma dos números no intervalo 1 a 200)

### Como transformar em algo mais generalista?

Temos uma soma entre os numeros x e y

[x,y] → intervalo 1 e 200

x + y = resultado parcial

(x+1) + (y-1) = resultado parcial

Total * resultado parcial = resultado

y/2 = total

200/2 = 100

100 * 201 = 20.100

### Agora coloca-se isso em um algoritmo

- Passo 1 - Recebe os valores (x e y)
- Passo 2 - Resolva: y / 2 = Total
- Passo 3 - Resolva: y+x = resultado_parcial
- Passo 4 - Ache o Resultado final: total * resultado_parcial = final
- Passo 5 - Imprima o final na tela