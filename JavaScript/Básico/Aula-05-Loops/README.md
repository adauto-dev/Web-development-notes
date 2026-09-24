
# JavaScript — Aula 05: Loops

> **Nível:** Básico → Médio → Avançado
> **Status:** ✅ Concluída com domínio
> **Objetivo principal:** aprender a repetir ações, percorrer valores, controlar repetições, filtrar informações, contar, acumular valores, combinar condições, fazer debugging e transformar problemas descritos em linguagem humana em lógica JavaScript.

---

# 📚 Índice

1. [Objetivos da Aula](#1-objetivos-da-aula)
2. [O que são Loops](#2-o-que-são-loops)
3. [Por que usamos Loops](#3-por-que-usamos-loops)
4. [`for`](#4-for)
5. [Estrutura do `for`](#5-estrutura-do-for)
6. [Como o `for` funciona passo a passo](#6-como-o-for-funciona-passo-a-passo)
7. [`i++` e `i--`](#7-i-e-i-)
8. [`while`](#8-while)
9. [`for` vs `while`](#9-for-vs-while)
10. [Loop infinito](#10-loop-infinito)
11. [Contador](#11-contador)
12. [Acumulador](#12-acumulador)
13. [Contador vs Acumulador](#13-contador-vs-acumulador)
14. [`+=` e outros operadores de atribuição](#14--e-outros-operadores-de-atribuição)
15. [Operador `%` — remainder](#15-operador---remainder)
16. [Par e Ímpar](#16-par-e-ímpar)
17. [Múltiplos](#17-múltiplos)
18. [`===` e `!==`](#18--e-)
19. [`&&` — AND](#19---and)
20. [`||` — OR](#20---or)
21. [Parênteses e agrupamento lógico](#21-parênteses-e-agrupamento-lógico)
22. [`if` dentro de Loops](#22-if-dentro-de-loops)
23. [`break`](#23-break)
24. [`continue`](#24-continue)
25. [`break` vs `continue`](#25-break-vs-continue)
26. [Loops + Condições + Acumuladores](#26-loops--condições--acumuladores)
27. [Nested Loops](#27-nested-loops)
28. [Erros comuns de sintaxe](#28-erros-comuns-de-sintaxe)
29. [Erros comuns de lógica](#29-erros-comuns-de-lógica)
30. [Debugging](#30-debugging)
31. [Problem Solving: problema → lógica → código](#31-problem-solving-problema--lógica--código)
32. [Exemplos completos](#32-exemplos-completos)
33. [Exercícios e habilidades praticadas](#33-exercícios-e-habilidades-praticadas)
34. [Avaliação Final](#34-avaliação-final)
35. [Inglês Técnico](#35-inglês-técnico)
36. [Cronograma da Aula 05](#36-cronograma-da-aula-05)
37. [Checklist de Domínio](#37-checklist-de-domínio)
38. [Erros e pontos de atenção pessoais](#38-erros-e-pontos-de-atenção-pessoais)
39. [Próxima etapa](#39-próxima-etapa)
40. [Conclusão](#40-conclusão)

---

# 1. Objetivos da Aula

Ao terminar esta aula, o objetivo é conseguir:

* entender o que é um loop;
* usar `for`;
* usar `while`;
* controlar o início, condição e atualização de um loop;
* entender `i++` e `i--`;
* evitar loops infinitos;
* usar contadores;
* usar acumuladores;
* usar `+=`;
* entender `%`;
* identificar números pares e ímpares;
* identificar múltiplos;
* usar `===`;
* usar `!==`;
* usar `&&`;
* usar `||`;
* combinar várias condições;
* usar parênteses para agrupar lógica;
* usar `break`;
* usar `continue`;
* usar `if` dentro de loops;
* usar loops aninhados;
* combinar loops, condições e acumuladores;
* interpretar problemas;
* transformar requisitos em lógica;
* transformar lógica em JavaScript;
* encontrar erros de sintaxe;
* encontrar erros de lógica;
* fazer debugging;
* resolver problemas sem receber o código pronto.

---

# 2. O que são Loops

Um **loop** é uma estrutura que permite executar um bloco de código repetidamente.

Sem loop:

```js
console.log(1);
console.log(2);
console.log(3);
console.log(4);
console.log(5);
```

Com loop:

```js
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

Resultado:

```text
1
2
3
4
5
```

## Ideia principal

Um loop é útil quando precisamos dizer ao programa:

> "Repita esta ação enquanto determinada regra for verdadeira."

---

# 3. Por que usamos Loops

Loops aparecem constantemente na programação.

Podemos utilizá-los para:

* percorrer números;
* percorrer listas;
* procurar valores;
* verificar condições;
* contar elementos;
* somar valores;
* filtrar informações;
* repetir uma ação;
* processar vários dados;
* trabalhar com tabelas;
* trabalhar com estruturas de várias dimensões.

Um loop evita repetir manualmente o mesmo código várias vezes.

---

# 4. `for`

O `for` é uma das estruturas mais utilizadas para repetição.

Exemplo:

```js
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

Resultado:

```text
1
2
3
4
5
```

---

# 5. Estrutura do `for`

A estrutura básica é:

```js
for (inicialização; condição; atualização) {
  // código que será repetido
}
```

Exemplo:

```js
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

Existem três partes principais:

```text
let i = 1
↓
Inicialização

i <= 5
↓
Condição

i++
↓
Atualização
```

## 5.1 Inicialização

```js
let i = 1;
```

Define o valor inicial.

## 5.2 Condição

```js
i <= 5;
```

Enquanto a condição for `true`, o loop continua.

## 5.3 Atualização

```js
i++;
```

Modifica o valor de `i` depois de cada repetição.

---

# 6. Como o `for` funciona passo a passo

Código:

```js
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

O processo é:

```text
i = 1
↓
1 <= 5 → true
↓
console.log(1)
↓
i++

i = 2
↓
2 <= 5 → true
↓
console.log(2)
↓
i++

i = 3
↓
3 <= 5 → true
↓
console.log(3)
↓
i++

...
```

Quando chega:

```text
i = 6
```

temos:

```text
6 <= 5 → false
```

Então o loop termina.

## Modelo mental

```text
INICIALIZA
    ↓
VERIFICA
    ↓
EXECUTA
    ↓
ATUALIZA
    ↓
VERIFICA NOVAMENTE
    ↓
...
    ↓
FALSE → PARA
```

---

# 7. `i++` e `i--`

## `i++`

Significa aumentar `i` em 1.

```js
i++;
```

Equivale, para este contexto, a:

```js
i = i + 1;
```

Exemplo:

```js
let i = 1;

i++;
```

Agora:

```text
i = 2
```

---

## `i--`

Significa diminuir `i` em 1.

```js
i--;
```

Equivale a:

```js
i = i - 1;
```

Exemplo:

```js
let i = 5;

i--;
```

Agora:

```text
i = 4
```

---

## Importante

A atualização precisa fazer sentido em relação à condição.

Exemplo:

```js
let number = 1;

while (number <= 5) {
  console.log(number);
  number++;
}
```

Funciona porque `number` está caminhando em direção ao limite.

Mas:

```js
let number = 1;

while (number <= 5) {
  console.log(number);
  number--;
}
```

é um problema.

Os valores vão:

```text
1
0
-1
-2
-3
...
```

e nunca chegam a uma situação em que:

```text
number <= 5
```

seja `false`.

---

# 8. `while`

O `while` também executa código repetidamente.

Estrutura:

```js
while (condição) {
  // código
}
```

Exemplo:

```js
let number = 1;

while (number <= 5) {
  console.log(number);
  number++;
}
```

Resultado:

```text
1
2
3
4
5
```

O `while` continua enquanto sua condição for verdadeira.

---

# 9. `for` vs `while`

## `for`

Exemplo:

```js
for (let i = 1; i <= 10; i++) {
  console.log(i);
}
```

O início, condição e atualização ficam organizados na própria estrutura.

## `while`

Exemplo:

```js
let i = 1;

while (i <= 10) {
  console.log(i);
  i++;
}
```

A condição aparece no `while` e a atualização fica dentro do bloco.

### Regra prática

Não existe uma regra absoluta dizendo que determinado problema obrigatoriamente precisa de `for` ou `while`.

A escolha depende da estrutura do problema.

---

# 10. Loop infinito

Um **infinite loop** acontece quando a condição nunca se torna `false`.

Exemplo:

```js
let number = 1;

while (number <= 5) {
  console.log(number);
}
```

Problema:

```js
number
```

nunca é atualizado.

Então:

```text
1 <= 5 → true
1 <= 5 → true
1 <= 5 → true
...
```

Outro problema:

```js
let number = 1;

while (number <= 5) {
  console.log(number);
  number--;
}
```

Aqui o valor está indo na direção errada.

### Como evitar

Sempre pergunte:

> "Minha variável está caminhando para tornar a condição falsa?"

---

# 11. Contador

Um **counter** é uma variável usada para contar quantas vezes alguma coisa aconteceu.

Exemplo:

```js
let count = 0;

for (let i = 1; i <= 5; i++) {
  count++;
}

console.log(count);
```

Resultado:

```text
5
```

---

## Exemplo: contar números pares

```js
let count = 0;

for (let i = 1; i <= 20; i++) {
  if (i % 2 === 0) {
    count++;
  }
}

console.log(count);
```

Aqui estamos perguntando:

> "Quantos números pares existem entre 1 e 20?"

---

# 12. Acumulador

Um **accumulator** guarda e acumula valores.

Exemplo:

```js
let total = 0;

for (let i = 1; i <= 5; i++) {
  total += i;
}

console.log(total);
```

Resultado:

```text
15
```

Processo:

```text
total = 0

0 + 1 = 1
1 + 2 = 3
3 + 3 = 6
6 + 4 = 10
10 + 5 = 15
```

---

# 13. Contador vs Acumulador

É importante diferenciar.

## Counter

Conta **quantas vezes** algo acontece.

```js
let count = 0;

count++;
```

Exemplo:

> Quantos números pares existem?

---

## Accumulator

Acumula **valores**.

```js
let total = 0;

total += i;
```

Exemplo:

> Qual é a soma dos números pares?

### Resumo

```text
COUNTER
↓
quantidade

ACCUMULATOR
↓
valor acumulado
```

---

# 14. `+=` e outros operadores de atribuição

Esta expressão:

```js
total += i;
```

é uma forma abreviada de:

```js
total = total + i;
```

Exemplo:

```js
let total = 10;

total += 5;
```

Resultado:

```text
15
```

Outros operadores:

```js
total -= 2;
total *= 3;
total /= 2;
```

---

# 15. Operador `%` — Remainder

O operador `%` retorna o **resto da divisão**.

Em inglês:

> **remainder**

Exemplo:

```js
6 % 3
```

A divisão:

```text
6 ÷ 3 = 2
```

Resto:

```text
0
```

Portanto:

```js
6 % 3
```

resulta em:

```text
0
```

Outro exemplo:

```js
7 % 3
```

Temos:

```text
7 ÷ 3 = 2
resto = 1
```

Resultado:

```text
1
```

---

## O `%` não retorna o quociente

```js
6 / 3
```

retorna:

```text
2
```

Enquanto:

```js
6 % 3
```

retorna:

```text
0
```

Portanto:

```text
/ → divisão
% → resto
```

---

## Regra importante

O resto de uma divisão é sempre menor que o divisor.

Por exemplo:

```text
7 % 3 → 1
8 % 3 → 2
9 % 3 → 0
```

Não teremos:

```text
7 % 3 → 4
```

---

# 16. Par e Ímpar

## Número par

Um número é par quando o resto da divisão por 2 é zero.

```js
i % 2 === 0
```

Exemplo:

```js
for (let i = 1; i <= 10; i++) {
  if (i % 2 === 0) {
    console.log(i);
  }
}
```

Resultado:

```text
2
4
6
8
10
```

---

## Número ímpar

Um número é ímpar quando o resto da divisão por 2 é diferente de zero.

```js
i % 2 !== 0
```

Exemplo:

```js
for (let i = 1; i <= 10; i++) {
  if (i % 2 !== 0) {
    console.log(i);
  }
}
```

Resultado:

```text
1
3
5
7
9
```

### Regra para lembrar

```text
PAR
→ % 2 === 0

ÍMPAR
→ % 2 !== 0
```

---

# 17. Múltiplos

Para verificar se um número é múltiplo de outro, podemos usar `%`.

Múltiplo de 3:

```js
i % 3 === 0
```

Múltiplo de 4:

```js
i % 4 === 0
```

Múltiplo de 5:

```js
i % 5 === 0
```

Exemplo:

```js
for (let i = 1; i <= 20; i++) {
  if (i % 3 === 0) {
    console.log(i);
  }
}
```

Resultado:

```text
3
6
9
12
15
18
```

---

# 18. `===` e `!==`

## `===`

Significa **strict equality**.

Verifica se dois valores são exatamente iguais.

```js
5 === 5
```

Resultado:

```text
true
```

```js
5 === 6
```

Resultado:

```text
false
```

Exemplo:

```js
i % 2 === 0
```

Significa:

> O resto da divisão de `i` por 2 é exatamente 0?

---

## `!==`

Significa **strict inequality**.

Verifica se os valores são diferentes.

```js
5 !== 6
```

Resultado:

```text
true
```

```js
5 !== 5
```

Resultado:

```text
false
```

Exemplo:

```js
i % 2 !== 0
```

Significa:

> O resto da divisão de `i` por 2 é diferente de 0?

---

# 19. `&&` — AND

`&&` significa:

> **AND = E**

As duas condições precisam ser verdadeiras.

Exemplo:

```js
if (i % 2 === 0 && i % 3 === 0) {
  console.log(i);
}
```

O número precisa:

```text
ser par
E
ser múltiplo de 3
```

Exemplo com `6`:

```text
6 % 2 === 0 → true
6 % 3 === 0 → true

true && true → true
```

Portanto `6` passa.

Exemplo com `9`:

```text
9 % 2 === 0 → false
9 % 3 === 0 → true

false && true → false
```

`9` não passa.

---

# 20. `||` — OR

`||` significa:

> **OR = OU**

Pelo menos uma das condições precisa ser verdadeira.

Exemplo:

```js
if (i % 3 === 0 || i % 5 === 0) {
  console.log(i);
}
```

O número pode ser:

```text
múltiplo de 3
OU
múltiplo de 5
```

Se uma das condições for verdadeira, o resultado geral será verdadeiro.

---

# 21. Parênteses e agrupamento lógico

Parênteses ajudam a separar grupos de lógica.

Exemplo:

```js
if (
  (i % 2 === 0 && i % 3 === 0)
  ||
  (i % 2 !== 0 && i % 5 === 0)
) {
  console.log(i);
}
```

Podemos ler:

```text
(PAR E múltiplo de 3)
OU
(ÍMPAR E múltiplo de 5)
```

Os parênteses representam **logical groups**.

Eles não servem para organizar o `console.log()`.

Servem para deixar claro quais condições pertencem ao mesmo grupo.

---

# 22. `if` dentro de Loops

O loop percorre os valores.

O `if` decide quais valores interessam.

Exemplo:

```js
for (let i = 1; i <= 10; i++) {
  if (i % 2 === 0) {
    console.log(i);
  }
}
```

O `for` percorre:

```text
1
2
3
4
5
6
7
8
9
10
```

O `if` filtra:

```text
2
4
6
8
10
```

### Modelo mental

```text
for
↓
percorre

if
↓
pergunta

condition
↓
true ou false

console.log()
↓
mostra o resultado
```

---

# 23. `break`

`break` encerra o loop imediatamente.

Exemplo:

```js
for (let i = 1; i <= 10; i++) {
  if (i === 6) {
    break;
  }

  console.log(i);
}
```

Resultado:

```text
1
2
3
4
5
```

Quando `i` chega a `6`, o `break` encerra o loop.

O `6` não aparece porque o `console.log()` está depois do `break`.

---

# 24. `continue`

`continue` não encerra o loop.

Ele pula a **iteração atual** e passa para a próxima.

Exemplo:

```js
for (let i = 1; i <= 6; i++) {
  if (i === 3) {
    continue;
  }

  console.log(i);
}
```

Resultado:

```text
1
2
4
5
6
```

O `3` foi pulado.

---

# 25. `break` vs `continue`

## `break`

```text
ENCERRA O LOOP
```

## `continue`

```text
PULA A ITERAÇÃO ATUAL
E CONTINUA O LOOP
```

Exemplo:

```js
for (let i = 1; i <= 10; i++) {
  if (i === 3) {
    continue;
  }

  if (i === 7) {
    break;
  }

  console.log(i);
}
```

Resultado:

```text
1
2
4
5
6
```

---

# 26. Loops + Condições + Acumuladores

Podemos combinar várias ferramentas.

Exemplo:

> Somar todos os números pares de 1 até 20.

```js
let total = 0;

for (let i = 1; i <= 20; i++) {
  if (i % 2 === 0) {
    total += i;
  }
}

console.log(total);
```

Resultado:

```text
110
```

Fluxo:

```text
percorrer
↓
verificar
↓
é par?
↓
sim → adicionar ao total
↓
continuar
```

---

## Exemplo praticado na avaliação

> Somar os números que são pares e múltiplos de 3 entre 1 e 50.

```js
let total = 0;

for (let i = 1; i <= 50; i++) {
  if (i % 2 === 0 && i % 3 === 0) {
    total += i;
  }
}

console.log(total);
```

Valores encontrados:

```text
6
12
18
24
30
36
42
48
```

Total:

```text
216
```

---

# 27. Nested Loops

**Nested loop** significa um loop dentro de outro loop.

Exemplo:

```js
for (let i = 1; i <= 3; i++) {
  for (let j = 1; j <= 3; j++) {
    console.log(i, j);
  }
}
```

O loop externo controla `i`.

O loop interno controla `j`.

Fluxo:

```text
i = 1
  j = 1
  j = 2
  j = 3

i = 2
  j = 1
  j = 2
  j = 3

i = 3
  j = 1
  j = 2
  j = 3
```

Nested loops são úteis em situações como:

* tabelas;
* linhas e colunas;
* grades;
* matrizes;
* estruturas bidimensionais.

## Pontos de atenção

Durante a prática, erros comuns foram:

* esquecer `j` na condição;
* colocar `;` no lugar errado;
* colocar `console.log()` no lugar errado;
* pequenos erros de sintaxe.

A ideia dos nested loops foi compreendida, mas a escrita exige atenção.

---

# 28. Erros comuns de sintaxe

Erros de sintaxe impedem o código de ser interpretado corretamente.

Exemplos:

### Parêntese faltando

```js
if (i % 2 === 0 {
```

### Chave faltando

```js
if (i % 2 === 0) {
  console.log(i);
```

### Estrutura do `for` incorreta

```js
for (let i = 1 i <= 10; i++) {
```

### Condição de nested loop escrita incorretamente

Pequenos erros de escrita podem impedir o funcionamento do programa.

### Regra prática

Quando houver erro de sintaxe:

1. leia a linha indicada;
2. confira parênteses;
3. confira chaves;
4. confira `;`;
5. confira a estrutura da expressão;
6. leia algumas linhas antes e depois.

O erro nem sempre está exatamente na linha indicada.

---

# 29. Erros comuns de lógica

Um código pode funcionar tecnicamente e ainda estar errado.

Isso é um **logic error**.

Durante a Aula 05 foram praticados vários tipos.

## `<` vs `<=`

Objetivo:

> 1 até 60, incluindo 60.

Errado:

```js
i < 60
```

Correto:

```js
i <= 60
```

---

## `&&` vs `||`

Objetivo:

> par E múltiplo de 4

Errado:

```js
i % 2 === 0 || i % 4 === 0
```

Correto:

```js
i % 2 === 0 && i % 4 === 0
```

---

## Par vs ímpar

Objetivo:

> ímpar

Errado:

```js
i % 2 === 0
```

Correto:

```js
i % 2 !== 0
```

---

## Grupo lógico incorreto

Objetivo:

```text
(A E B) OU (C E D)
```

Não podemos transformar isso acidentalmente em:

```text
(A OU B) E (C OU D)
```

A estrutura lógica precisa ser preservada.

---

## Acumulador desnecessário

Se o objetivo é:

> mostrar os números

não precisamos de:

```js
let total = 0;
```

Nem:

```js
total += i;
```

Nesse caso:

```js
console.log(i);
```

é suficiente.

---

# 30. Debugging

**Debugging** é o processo de encontrar, entender e corrigir problemas no código.

Não significa apenas procurar erros de sintaxe.

Existem também erros de lógica.

---

## Processo de Debugging

```text
1. Ler o objetivo
        ↓
2. Entender o comportamento esperado
        ↓
3. Ler o código
        ↓
4. Comparar objetivo × código
        ↓
5. Encontrar diferenças
        ↓
6. Explicar por que estão erradas
        ↓
7. Corrigir
        ↓
8. Testar
        ↓
9. Comparar resultado esperado × resultado obtido
```

---

## Tipos de erro praticados

### Syntax Error

Erro de sintaxe.

Exemplo:

```js
if (i % 2 === 0 {
```

---

### Logic Error

O código executa, mas produz um resultado incorreto.

Exemplo:

```js
if (i % 2 === 0 || i % 3 === 0)
```

quando o problema pede:

```text
par E múltiplo de 3
```

---

### Infinite Loop

O loop nunca termina.

Exemplo:

```js
let number = 1;

while (number <= 5) {
  console.log(number);
}
```

---

# 31. Problem Solving: problema → lógica → código

Esta foi uma das habilidades mais importantes da avaliação.

Programação não começa necessariamente escrevendo código.

Muitas vezes recebemos um **problem statement** ou um **requirement**.

Exemplo:

> "Percorra de 1 até 60 e mostre os números que sejam pares e múltiplos de 4 ou ímpares e múltiplos de 5."

Primeiro entendemos o problema.

Depois transformamos em lógica:

```text
1 até 60

(PAR E múltiplo de 4)
OU
(ÍMPAR E múltiplo de 5)
```

Depois transformamos cada conceito:

```text
PAR
→ i % 2 === 0

ÍMPAR
→ i % 2 !== 0

MÚLTIPLO DE 4
→ i % 4 === 0

MÚLTIPLO DE 5
→ i % 5 === 0

E
→ &&

OU
→ ||
```

Depois escrevemos o código:

```js
for (let i = 1; i <= 60; i++) {
  if (
    (i % 2 === 0 && i % 4 === 0)
    ||
    (i % 2 !== 0 && i % 5 === 0)
  ) {
    console.log(i);
  }
}
```

---

## Fluxo de Problem Solving

```text
PROBLEMA
   ↓
ENTENDER O QUE FOI PEDIDO
   ↓
SEPARAR AS REGRAS
   ↓
IDENTIFICAR CONDIÇÕES
   ↓
IDENTIFICAR E / OU
   ↓
IDENTIFICAR LIMITES
   ↓
MONTAR A LÓGICA
   ↓
TRANSFORMAR EM JAVASCRIPT
   ↓
TESTAR
   ↓
DEBUGAR
```

Essa habilidade será utilizada em todas as próximas etapas de programação.

---

# 32. Exemplos completos

## 32.1 Números pares de 1 a 30

```js
for (let i = 1; i <= 30; i++) {
  if (i % 2 === 0) {
    console.log(i);
  }
}
```

---

## 32.2 Números ímpares de 1 a 30

```js
for (let i = 1; i <= 30; i++) {
  if (i % 2 !== 0) {
    console.log(i);
  }
}
```

---

## 32.3 Múltiplos de 3

```js
for (let i = 1; i <= 20; i++) {
  if (i % 3 === 0) {
    console.log(i);
  }
}
```

---

## 32.4 Soma dos números pares

```js
let total = 0;

for (let i = 1; i <= 20; i++) {
  if (i % 2 === 0) {
    total += i;
  }
}

console.log(total);
```

---

## 32.5 Múltiplos de 3 E pares

```js
for (let i = 1; i <= 30; i++) {
  if (i % 3 === 0 && i % 2 === 0) {
    console.log(i);
  }
}
```

Resultado:

```text
6
12
18
24
30
```

---

## 32.6 Múltiplos de 3 OU 5

```js
for (let i = 1; i <= 50; i++) {
  if (i % 3 === 0 || i % 5 === 0) {
    console.log(i);
  }
}
```

---

## 32.7 Ímpares E múltiplos de 5

```js
for (let i = 1; i <= 50; i++) {
  if (i % 2 !== 0 && i % 5 === 0) {
    console.log(i);
  }
}
```

Resultado:

```text
5
15
25
35
45
```

---

## 32.8 `continue` + `break`

Objetivo:

> Mostrar números pares de 1 até 30, mas parar antes do 20.

```js
for (let i = 1; i <= 30; i++) {
  if (i % 2 !== 0) {
    continue;
  }

  if (i === 20) {
    break;
  }

  console.log(i);
}
```

Resultado:

```text
2
4
6
8
10
12
14
16
18
```

---

## 32.9 Condição com grupos

Objetivo:

> Múltiplos de 3 e 4, ou múltiplos de 10.

```js
for (let i = 1; i <= 100; i++) {
  if (
    (i % 3 === 0 && i % 4 === 0)
    ||
    i % 10 === 0
  ) {
    console.log(i);
  }
}
```

---

## 32.10 Condição combinada mais complexa

Objetivo:

> Pares e múltiplos de 3, ou ímpares e múltiplos de 5.

```js
for (let i = 1; i <= 100; i++) {
  if (
    (i % 2 === 0 && i % 3 === 0)
    ||
    (i % 2 !== 0 && i % 5 === 0)
  ) {
    console.log(i);
  }
}
```

---

# 33. Exercícios e habilidades praticadas

Durante a consolidação da Aula 05 foram praticados:

## `for`

* estrutura;
* inicialização;
* condição;
* atualização;
* `i++`;
* limites;
* `<`;
* `<=`.

## `while`

* condição;
* atualização;
* `i++`;
* `i--`;
* prevenção de loops infinitos.

## Controles

* `break`;
* `continue`;
* combinação de `break` e `continue`.

## Matemática

* `%`;
* resto;
* par;
* ímpar;
* múltiplos;
* soma.

## Comparação

* `===`;
* `!==`.

## Lógica

* `&&`;
* `||`;
* parênteses;
* grupos de condições.

## Estruturas

* `if`;
* nested loops;
* loop + condição;
* loop + condição + acumulador.

## Problem Solving

* interpretar enunciados;
* identificar requisitos;
* separar condições;
* transformar palavras em operadores;
* montar lógica;
* escrever código.

## Debugging

* encontrar erros;
* explicar erros;
* corrigir erros;
* testar novamente;
* comparar resultado esperado e resultado obtido.

---

# 34. Avaliação Final

A avaliação final foi dividida em três partes.

---

## Parte 1 — Lógica combinada

Objetivo:

> Percorrer de 1 até 100 e mostrar números pares e múltiplos de 3, ou ímpares e múltiplos de 7.

Solução construída de forma independente:

```js
for (let i = 1; i <= 100; i++) {
  if (
    (i % 2 === 0 && i % 3 === 0)
    ||
    (i % 2 !== 0 && i % 7 === 0)
  ) {
    console.log(i);
  }
}
```

Resultado:

> ✅ Correto.

---

## Parte 2 — Acumulador + condição

Objetivo:

> Somar os números pares e múltiplos de 3 entre 1 e 50.

Solução:

```js
let total = 0;

for (let i = 1; i <= 50; i++) {
  if (i % 2 === 0 && i % 3 === 0) {
    total += i;
  }
}

console.log(total);
```

Resultado:

```text
216
```

> ✅ Correto.

---

## Parte 3 — Debugging independente

Objetivo:

> Mostrar de 1 até 80 os números que sejam pares e múltiplos de 4, ou ímpares e múltiplos de 5.

O código inicialmente possuía problemas em:

* limite do `for`;
* paridade;
* `&&` / `||`;
* agrupamento lógico;
* segundo grupo;
* uso desnecessário de acumulador;
* saída incorreta.

Os problemas foram identificados e explicados antes da correção.

Código final:

```js
for (let i = 1; i <= 80; i++) {
  if (
    (i % 2 === 0 && i % 4 === 0)
    ||
    (i % 2 !== 0 && i % 5 === 0)
  ) {
    console.log(i);
  }
}
```

> ✅ Correto.

---

# 35. Inglês Técnico

A programação utiliza muitos termos em inglês.

O objetivo não é decorar todas as palavras imediatamente, mas começar a reconhecê-las naturalmente.

---

## Loops

| English        | Português          |
| -------------- | ------------------ |
| Loop           | Laço / repetição   |
| Iteration      | Iteração           |
| Iterate        | Iterar / percorrer |
| Repeat         | Repetir            |
| Condition      | Condição           |
| Initialization | Inicialização      |
| Update         | Atualização        |
| Counter        | Contador           |
| Accumulator    | Acumulador         |
| Nested loop    | Loop aninhado      |
| Infinite loop  | Loop infinito      |

---

## Controle

| English  | Português           |
| -------- | ------------------- |
| Break    | Interromper / parar |
| Continue | Continuar           |
| Skip     | Pular               |
| Exit     | Sair / encerrar     |

---

## Lógica

| English            | Português        |
| ------------------ | ---------------- |
| Logic              | Lógica           |
| Logical expression | Expressão lógica |
| Condition          | Condição         |
| True               | Verdadeiro       |
| False              | Falso            |
| Equal              | Igual            |
| Not equal          | Diferente        |
| And                | E                |
| Or                 | Ou               |
| Comparison         | Comparação       |
| Operator           | Operador         |
| Logical operator   | Operador lógico  |
| Grouping           | Agrupamento      |

---

## Matemática

| English   | Português      |
| --------- | -------------- |
| Number    | Número         |
| Integer   | Número inteiro |
| Even      | Par            |
| Odd       | Ímpar          |
| Multiple  | Múltiplo       |
| Remainder | Resto          |
| Division  | Divisão        |
| Sum       | Soma           |
| Total     | Total          |
| Increment | Incrementar    |
| Decrement | Decrementar    |

---

## Problem Solving

| English              | Português              |
| -------------------- | ---------------------- |
| Problem              | Problema               |
| Problem statement    | Enunciado do problema  |
| Requirement          | Requisito              |
| Rule                 | Regra                  |
| Constraint           | Restrição              |
| Requirement analysis | Análise de requisitos  |
| Logic                | Lógica                 |
| Solution             | Solução                |
| Approach             | Abordagem              |
| Expected behavior    | Comportamento esperado |

---

## Debugging

| English       | Português                 |
| ------------- | ------------------------- |
| Bug           | Erro / problema           |
| Debug         | Depurar                   |
| Debugging     | Depuração                 |
| Error         | Erro                      |
| Syntax error  | Erro de sintaxe           |
| Logic error   | Erro de lógica            |
| Runtime error | Erro em tempo de execução |
| Infinite loop | Loop infinito             |
| Fix           | Corrigir                  |
| Test          | Testar                    |
| Expected      | Esperado                  |
| Actual        | Obtido / real             |
| Output        | Saída / resultado         |
| Input         | Entrada                   |

---

## Programação geral

| English    | Português |
| ---------- | --------- |
| Code       | Código    |
| Statement  | Instrução |
| Expression | Expressão |
| Variable   | Variável  |
| Value      | Valor     |
| Execute    | Executar  |
| Run        | Executar  |
| Call       | Chamar    |
| Scope      | Escopo    |
| Function   | Função    |
| Parameter  | Parâmetro |
| Argument   | Argumento |
| Return     | Retornar  |

---

## Frases técnicas

```text
The loop runs from 1 to 10.
→ O loop vai de 1 até 10.

The condition is true.
→ A condição é verdadeira.

The condition is false.
→ A condição é falsa.

The loop stops when the condition is false.
→ O loop para quando a condição é falsa.

Skip the current iteration.
→ Pule a iteração atual.

Break out of the loop.
→ Interrompa/saia do loop.

The variable stores the total.
→ A variável armazena o total.

This condition checks if the number is even.
→ Esta condição verifica se o número é par.

The code has a logic error.
→ O código tem um erro de lógica.

Let's debug the code.
→ Vamos depurar o código.

The expected output is...
→ A saída esperada é...

The actual output is...
→ A saída obtida é...

The loop runs indefinitely.
→ O loop executa indefinidamente.

This condition filters the values.
→ Esta condição filtra os valores.

The two conditions must be true.
→ As duas condições precisam ser verdadeiras.

At least one condition must be true.
→ Pelo menos uma condição precisa ser verdadeira.
```

---

# 36. Cronograma da Aula 05

A Aula 05 não foi considerada concluída apenas por ter terminado o conteúdo teórico.

O processo utilizado foi:

```text
ETAPA 1 — TEORIA
↓
O que são Loops
↓
for
↓
while
↓
contador
↓
acumulador
↓
%
↓
===
↓
!==
↓
&&
↓
||
↓
parênteses
↓
break
↓
continue
↓
nested loops


ETAPA 2 — EXERCÍCIOS
↓
for
↓
while
↓
pares
↓
ímpares
↓
múltiplos
↓
acumuladores
↓
condições


ETAPA 3 — COMBINAÇÕES
↓
loop + if
↓
loop + condição
↓
loop + condição + acumulador
↓
&&
↓
||
↓
parênteses
↓
condições complexas


ETAPA 4 — DEBUGGING
↓
encontrar erro
↓
explicar erro
↓
corrigir
↓
testar


ETAPA 5 — PROBLEM SOLVING
↓
ler o enunciado
↓
entender o requisito
↓
separar as regras
↓
montar a lógica
↓
escrever JavaScript


ETAPA 6 — AVALIAÇÃO
↓
lógica combinada
↓
acumulador + condição
↓
debugging sem pistas
↓
correção independente


RESULTADO
↓
AULA 05 CONCLUÍDA COM DOMÍNIO
```

---

# 37. Checklist de Domínio

## Básico

* [x] Entender o que é um loop
* [x] Entender `for`
* [x] Entender `while`
* [x] Entender inicialização
* [x] Entender condição
* [x] Entender atualização
* [x] Entender `i++`
* [x] Entender `i--`
* [x] Entender limites
* [x] Entender `<`
* [x] Entender `<=`

## Contagem e acumulação

* [x] Entender counter
* [x] Entender accumulator
* [x] Diferenciar counter de accumulator
* [x] Entender `+=`

## Matemática

* [x] Entender `/`
* [x] Entender `%`
* [x] Entender remainder
* [x] Identificar pares
* [x] Identificar ímpares
* [x] Identificar múltiplos
* [x] Calcular somas

## Comparação

* [x] Entender `===`
* [x] Entender `!==`

## Lógica

* [x] Entender `&&`
* [x] Entender `||`
* [x] Combinar `&&` e `||`
* [x] Usar parênteses
* [x] Entender agrupamento lógico
* [x] Traduzir "E" para `&&`
* [x] Traduzir "OU" para `||`

## Controle

* [x] Entender `break`
* [x] Entender `continue`
* [x] Diferenciar `break` de `continue`

## Estruturas

* [x] `if` dentro de loops
* [x] Nested loops
* [x] Loop + condição
* [x] Loop + condição + acumulador

## Debugging

* [x] Identificar erro de sintaxe
* [x] Identificar erro de lógica
* [x] Identificar loop infinito
* [x] Identificar `<` vs `<=`
* [x] Identificar `===` vs `!==`
* [x] Identificar `&&` vs `||`
* [x] Identificar condição invertida
* [x] Identificar grupo lógico incorreto
* [x] Identificar acumulador desnecessário
* [x] Corrigir `console.log()`
* [x] Testar código corrigido

## Problem Solving

* [x] Ler um enunciado
* [x] Identificar o objetivo
* [x] Identificar requisitos
* [x] Separar condições
* [x] Identificar limites
* [x] Transformar palavras em lógica
* [x] Transformar lógica em JavaScript
* [x] Resolver problemas sem código pronto

## Avaliação

* [x] Resolver lógica combinada sozinho
* [x] Resolver acumulador + condição sozinho
* [x] Fazer debugging sem receber a localização dos erros
* [x] Explicar por que cada erro estava errado
* [x] Corrigir o código sozinho
* [x] Testar o resultado

### Resultado final

> **✅ Aula 05 — Loops: CONCLUÍDA COM DOMÍNIO**

---

# 38. Erros e pontos de atenção pessoais

Durante a prática, alguns erros apareceram. Eles foram importantes porque ajudaram a consolidar o conhecimento.

## Sintaxe

Houve pequenos erros em:

* condições;
* `j` em nested loops;
* `;`;
* posição de `console.log()`;
* estrutura de loops.

Esses erros foram corrigidos durante a prática.

---

## Lógica

Também foram encontrados erros como:

* usar `<` quando precisava incluir o limite com `<=`;
* confundir `&&` com `||`;
* confundir par com ímpar;
* esquecer que `!==` pode ser usado para identificar ímpares;
* montar grupos lógicos incorretamente;
* usar acumulador quando o objetivo era apenas mostrar valores.

O ponto importante é que, nos exercícios finais, esses problemas foram **identificados e corrigidos de forma independente**.

---

# 39. Próxima etapa

A próxima aula da sequência é:

# Aula 06 — Functions

A transição será:

```text
Aula 05
Loops
↓
Aula 06
Functions
```

A próxima etapa não será apenas aprender a escrever:

```js
function something() {
}
```

Será necessário compreender:

* por que Functions existem;
* qual problema elas resolvem;
* quando usar;
* quando não usar;
* declaração de funções;
* chamada de funções;
* parâmetros;
* argumentos;
* `return`;
* diferença entre `console.log()` e `return`;
* escopo;
* reutilização de código;
* combinação entre Functions e estruturas já aprendidas.

O conhecimento de Loops continuará sendo utilizado dentro das próximas aulas.

---

# 40. Conclusão

A Aula 05 não foi apenas sobre aprender `for` e `while`.

O objetivo principal foi desenvolver a capacidade de:

```text
PERCORRER
↓
VERIFICAR
↓
FILTRAR
↓
CONTAR
↓
ACUMULAR
↓
CONTROLAR
↓
COMBINAR CONDIÇÕES
↓
DEBUGAR
↓
RESOLVER PROBLEMAS
```

A habilidade mais importante consolidada foi:

```text
PROBLEMA
↓
ENTENDER O REQUISITO
↓
MONTAR A LÓGICA
↓
ESCREVER O CÓDIGO
↓
TESTAR
↓
DEBUGAR
```

Essa forma de pensar será reutilizada durante todo o aprendizado de JavaScript e posteriormente em:

* DOM;
* eventos;
* APIs;
* arrays;
* objetos;
* funções;
* React;
* Node.js;
* bancos de dados;
* backend;
* testes;
* arquitetura;
* projetos reais.

## Status final

```text
JavaScript — Aula 05
        ↓
Loops
        ↓
✅ CONCLUÍDA COM DOMÍNIO
```

**README oficial da Aula 05 — versão final.**
