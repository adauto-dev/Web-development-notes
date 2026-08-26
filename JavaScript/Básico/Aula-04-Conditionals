# JavaScript — Aula 04: Conditionals

## 📚 Roadmap — JavaScript Básico

| Aula        | Conteúdo                           | Status          |
| ----------- | ---------------------------------- | --------------- |
| Aula 01     | Fundamentos                        | ✅ Concluída     |
| Aula 02     | Strings                            | ✅ Concluída     |
| Aula 03     | Variables, Operators e Expressions | ✅ Concluída     |
| **Aula 04** | **Conditionals**                   | **✅ Concluída** |
| Aula 05     | Loops                              | ⏳ Próxima       |

---

# 🎯 Objetivo da Aula

Aprender como o JavaScript **toma decisões** usando condições.

Ao final desta aula, devemos conseguir:

* verificar condições;
* trabalhar com `true` e `false`;
* comparar valores;
* combinar várias condições;
* usar `if`, `else if` e `else`;
* entender `&&`, `||` e `!`;
* criar condições dentro de outras condições;
* entender a diferença entre `if` independente e uma cadeia `if / else if / else`;
* entender a ordem em que o JavaScript verifica as condições;
* entender por que algumas condições **nem chegam a ser avaliadas**;
* ler e explicar código condicional;
* utilizar a terminologia técnica em inglês.

---

# 1. O que são Conditionals?

**Conditionals** são estruturas usadas para fazer o programa tomar decisões.

A ideia básica é:

```text
SE uma condição for verdadeira
→ execute determinado código.

CASO CONTRÁRIO
→ execute outro código.
```

Exemplo:

```javascript
const age = 20;

if (age >= 18) {
    console.log("Adult");
}
```

O JavaScript verifica:

```text
20 >= 18
→ true
```

Como a condição é `true`, o código dentro do `if` é executado.

---

# 2. Boolean

As condições trabalham principalmente com valores Boolean.

Um Boolean possui apenas dois valores:

```javascript
true
false
```

### Vocabulário

**Boolean** → Booleano / valor lógico

**true** → verdadeiro

**false** → falso

Exemplo:

```javascript
const isLoggedIn = true;
const isBlocked = false;
```

---

# 3. `if` — If Statement

### Nome em inglês

**If Statement**

### Português

Instrução condicional `if`

Sintaxe:

```javascript
if (condition) {
    // código executado se a condição for true
}
```

Exemplo:

```javascript
const age = 20;

if (age >= 18) {
    console.log("Adult");
}
```

A condição:

```javascript
age >= 18
```

resulta em:

```text
true
```

Portanto:

```text
Adult
```

é exibido.

---

# 4. `else` — Else Statement

O `else` é executado quando a condição do `if` é `false`.

Exemplo:

```javascript
const age = 15;

if (age >= 18) {
    console.log("Adult");
} else {
    console.log("Child");
}
```

Avaliação:

```text
15 >= 18
→ false
```

Então:

```text
Child
```

é exibido.

### Vocabulário

**else** → caso contrário

---

# 5. `else if` — Else-If Statement

Usamos `else if` quando precisamos verificar outra condição.

```javascript
const age = 20;

if (age >= 18) {
    console.log("Adult");
} else if (age >= 13) {
    console.log("Teenager");
} else {
    console.log("Child");
}
```

O JavaScript verifica de cima para baixo.

Primeiro:

```text
20 >= 18
→ true
```

Então executa:

```text
Adult
```

E não continua verificando os próximos `else if`.

---

# 6. Regra fundamental de `if / else if / else`

Em uma cadeia:

```javascript
if (conditionA) {

} else if (conditionB) {

} else if (conditionC) {

} else {

}
```

O JavaScript:

1. verifica a primeira condição;
2. se for `true`, executa esse bloco;
3. depois encerra essa cadeia;
4. se for `false`, passa para o próximo `else if`;
5. continua até encontrar uma condição verdadeira;
6. se nenhuma for verdadeira, executa o `else`.

### Regra

> **O primeiro caminho verdadeiro da cadeia é executado.**

---

# 7. Exemplo importante sobre a ordem

```javascript
const score = 90;

if (score >= 50) {
    console.log("Passed");
} else if (score >= 70) {
    console.log("Good");
} else if (score >= 90) {
    console.log("Excellent");
}
```

O resultado será:

```text
Passed
```

Por quê?

Porque:

```text
90 >= 50
→ true
```

O JavaScript encontrou `true` primeiro.

Ele não continua para:

```text
90 >= 70
```

nem:

```text
90 >= 90
```

### Melhor organização

Quando as condições representam faixas, normalmente devemos colocá-las em uma ordem lógica:

```javascript
const score = 90;

if (score >= 90) {
    console.log("Excellent");
} else if (score >= 70) {
    console.log("Good");
} else if (score >= 50) {
    console.log("Passed");
} else {
    console.log("Failed");
}
```

Agora o resultado é:

```text
Excellent
```

---

# 8. `if` independente

Dois `if` separados são independentes.

Exemplo:

```javascript
const age = 20;

if (age >= 18) {
    console.log("Adult");
}

if (age >= 13) {
    console.log("Teenager");
}
```

Os dois serão executados:

```text
Adult
Teenager
```

Porque são duas verificações independentes.

---

# 9. `if` independente x `else if`

### Independentes

```javascript
if (conditionA) {
    // ...
}

if (conditionB) {
    // ...
}
```

As duas condições podem ser `true`.

Os dois blocos podem executar.

### Em cadeia

```javascript
if (conditionA) {
    // ...
} else if (conditionB) {
    // ...
}
```

Se `conditionA` for `true`, o `else if` não será avaliado.

---

# 10. Comparison Operators

Os **Comparison Operators** são usados para comparar valores.

## Tabela completa

| Símbolo | Nome em inglês                        | Português            | Exemplo    |
| ------- | ------------------------------------- | -------------------- | ---------- |
| `===`   | **Strict Equality Operator**          | Igualdade estrita    | `5 === 5`  |
| `!==`   | **Strict Inequality Operator**        | Desigualdade estrita | `5 !== 10` |
| `>`     | **Greater Than Operator**             | Maior que            | `10 > 5`   |
| `<`     | **Less Than Operator**                | Menor que            | `5 < 10`   |
| `>=`    | **Greater Than or Equal To Operator** | Maior ou igual a     | `10 >= 10` |
| `<=`    | **Less Than or Equal To Operator**    | Menor ou igual a     | `5 <= 10`  |

Esses operadores normalmente produzem:

```text
true
```

ou:

```text
false
```

---

# 11. `===` — Strict Equality Operator

### Inglês

**Strict Equality Operator**

### Português

Operador de igualdade estrita

Verifica se:

1. o valor é igual;
2. o tipo também é igual.

Exemplo:

```javascript
5 === 5
```

Resultado:

```text
true
```

Mas:

```javascript
5 === "5"
```

Resultado:

```text
false
```

Porque:

```text
5   → Number
"5" → String
```

Mesmo que visualmente pareçam iguais, os tipos são diferentes.

### Regra

```text
=== → mesmo valor + mesmo tipo
```

---

# 12. `!==` — Strict Inequality Operator

### Inglês

**Strict Inequality Operator**

### Português

Operador de desigualdade estrita

Exemplo:

```javascript
5 !== 10
```

Resultado:

```text
true
```

Porque os valores são diferentes.

Outro exemplo:

```javascript
5 !== 5
```

Resultado:

```text
false
```

E:

```javascript
5 !== "5"
```

Resultado:

```text
true
```

Porque os tipos são diferentes.

### Regra

```text
!== → diferente em valor ou tipo
```

---

# 13. `>` — Greater Than Operator

### Inglês

**Greater Than Operator**

### Português

Maior que

```javascript
10 > 5
```

Resultado:

```text
true
```

---

# 14. `<` — Less Than Operator

### Inglês

**Less Than Operator**

### Português

Menor que

```javascript
5 < 10
```

Resultado:

```text
true
```

---

# 15. `>=` — Greater Than or Equal To Operator

### Inglês

**Greater Than or Equal To Operator**

### Português

Maior ou igual a

```javascript
18 >= 18
```

Resultado:

```text
true
```

Também:

```javascript
20 >= 18
```

Resultado:

```text
true
```

Mas:

```javascript
17 >= 18
```

Resultado:

```text
false
```

### Atenção

Quando temos:

```javascript
age >= 18
```

isso significa:

```text
18, 19, 20, 21, 22...
```

Ou seja:

> 18 também está incluído.

---

# 16. `<=` — Less Than or Equal To Operator

### Inglês

**Less Than or Equal To Operator**

### Português

Menor ou igual a

```javascript
18 <= 18
```

Resultado:

```text
true
```

Também:

```javascript
15 <= 18
```

Resultado:

```text
true
```

---

# 17. Logical Operators

Logical Operators permitem combinar ou inverter condições.

| Símbolo | Nome em inglês           | Português      |                         |           |
| ------- | ------------------------ | -------------- | ----------------------- | --------- |
| `&&`    | **Logical AND Operator** | E lógico       |                         |           |
| `       |                          | `              | **Logical OR Operator** | OU lógico |
| `!`     | **Logical NOT Operator** | Negação lógica |                         |           |

---

# 18. `&&` — Logical AND Operator

### Inglês

**Logical AND Operator**

### Português

Operador lógico E

Todas as condições precisam ser `true`.

```javascript
true && true
```

Resultado:

```text
true
```

Mas:

```javascript
true && false
```

Resultado:

```text
false
```

Também:

```javascript
false && true
```

Resultado:

```text
false
```

E:

```javascript
false && false
```

Resultado:

```text
false
```

### Regra

> Com `&&`, todas as condições precisam ser verdadeiras.

Exemplo:

```javascript
const age = 20;
const hasTicket = true;

if (age >= 18 && hasTicket) {
    console.log("Entry allowed");
}
```

Temos:

```text
age >= 18 → true
hasTicket → true

true && true
→ true
```

---

# 19. `||` — Logical OR Operator

### Inglês

**Logical OR Operator**

### Português

Operador lógico OU

Pelo menos uma condição precisa ser `true`.

```javascript
true || false
```

Resultado:

```text
true
```

```javascript
false || true
```

Resultado:

```text
true
```

Somente:

```javascript
false || false
```

produz:

```text
false
```

### Regra

> Com `||`, basta uma condição ser verdadeira.

Exemplo:

```javascript
const hasTicket = false;
const isVip = true;

if (hasTicket || isVip) {
    console.log("Entry allowed");
}
```

Temos:

```text
false || true
→ true
```

---

# 20. `!` — Logical NOT Operator

### Inglês

**Logical NOT Operator**

### Português

Operador lógico de negação

Ele inverte o Boolean.

```javascript
!true
```

Resultado:

```text
false
```

E:

```javascript
!false
```

Resultado:

```text
true
```

Exemplo:

```javascript
const isBlocked = false;

if (!isBlocked) {
    console.log("Access allowed");
}
```

Temos:

```text
isBlocked → false
!false → true
```

Então o bloco executa.

---

# 21. Tabela rápida dos Logical Operators

| A | B | `A && B` | `A || B` |
|---|---|---|---|
| true | true | true | true |
| true | false | false | true |
| false | true | false | true |
| false | false | false | false |

Para `!`:

| Valor    | Resultado |
| -------- | --------- |
| `!true`  | `false`   |
| `!false` | `true`    |

---

# 22. `=` não é `===`

Essa diferença é fundamental.

### `=`

**Assignment Operator**

Operador de atribuição.

```javascript
let age = 20;
```

Significa:

> Armazene `20` em `age`.

### `===`

**Strict Equality Operator**

Operador de igualdade estrita.

```javascript
age === 20
```

Significa:

> `age` é estritamente igual a `20`?

Portanto:

```text
=   → atribuição
=== → comparação
```

---

# 23. Nested If

**Nested if** significa um `if` dentro de outro `if`.

Exemplo:

```javascript
const age = 20;
const hasTicket = true;

if (age >= 18) {

    if (hasTicket) {
        console.log("Entry allowed");
    }

}
```

Primeiro o JavaScript verifica:

```text
age >= 18
```

Somente se essa condição for `true`, ele entra no bloco e chega ao segundo `if`.

---

# 24. Condição externa controlando condição interna

Este é um dos conceitos mais importantes desta aula.

```javascript
const age = 17;
const hasTicket = true;

if (age >= 18) {

    if (hasTicket) {
        console.log("Entry allowed");
    }

} else {
    console.log("Entry denied");
}
```

Primeiro:

```text
17 >= 18
→ false
```

Como o primeiro `if` é `false`, o JavaScript vai para:

```text
Entry denied
```

O segundo `if` **não é alcançado**.

Mesmo:

```text
hasTicket → true
```

não muda o resultado.

### Regra

> Uma condição pode ser verdadeira, mas o JavaScript pode nunca chegar a avaliá-la.

---

# 25. Condição que não é avaliada

Exemplo:

```javascript
const age = 17;
const hasTicket = true;

if (age >= 18) {
    if (hasTicket) {
        console.log("Entry allowed");
    }
}
```

O programa faz:

```text
age >= 18
↓
false
↓
não entra no bloco
↓
hasTicket não é avaliado nesse caminho
```

Não devemos dizer:

> "O segundo `if` foi `true`, mas não executou."

O mais correto é:

> **"O segundo `if` nem foi alcançado."**

Essa diferença é importante em programação.

---

# 26. Nested If + Else

Exemplo:

```javascript
const age = 21;
const isBlocked = false;
const hasTicket = false;
const isVip = true;

if (age >= 18 && !isBlocked) {

    if (hasTicket || isVip) {
        console.log("Access granted");
    } else {
        console.log("No ticket");
    }

} else {
    console.log("Access denied");
}
```

Primeira condição:

```text
age >= 18
→ true

!isBlocked
→ true

true && true
→ true
```

Entra no primeiro `if`.

Depois:

```text
hasTicket
→ false

isVip
→ true

false || true
→ true
```

Resultado:

```text
Access granted
```

---

# 27. Exemplo de loja

```javascript
const total = 250;
const isBlocked = false;
const hasCoupon = false;

if (!isBlocked) {

    if (total >= 500) {
        console.log("20% discount");

    } else if (total >= 100) {
        console.log("10% discount");

    } else if (hasCoupon) {
        console.log("Special coupon discount");

    } else {
        console.log("No discount");
    }

} else {
    console.log("Customer blocked");
}
```

Primeiro:

```text
!isBlocked
→ true
```

Entra no primeiro `if`.

Depois:

```text
250 >= 500
→ false
```

Passa para o próximo:

```text
250 >= 100
→ true
```

Executa:

```text
10% discount
```

E para a cadeia.

O:

```javascript
else if (hasCoupon)
```

**não é avaliado**.

Isso continua verdadeiro mesmo se:

```javascript
hasCoupon = true;
```

porque o programa já encontrou uma condição verdadeira antes.

---

# 28. Ordem geral de execução

O JavaScript normalmente executa o código de cima para baixo.

Exemplo:

```javascript
console.log("A");

if (true) {
    console.log("B");
}

console.log("C");
```

Resultado:

```text
A
B
C
```

Nos condicionais, o fluxo pode mudar dependendo do resultado das condições.

---

# 29. Condições com parênteses

Podemos usar parênteses para agrupar condições.

Exemplo:

```javascript
if ((age >= 18 && hasMoney) || hasCoupon) {
    console.log("Purchase allowed");
}
```

Primeiro avaliamos:

```text
age >= 18 && hasMoney
```

Depois o resultado é combinado com:

```text
|| hasCoupon
```

Os parênteses ajudam a deixar a lógica mais clara.

---

# 30. Exemplo completo de decisão

```javascript
const age = 21;
const money = 80;
const price = 100;
const isBlocked = false;
const hasCoupon = true;

if (age >= 18 && !isBlocked) {

    if (money >= price || hasCoupon) {
        console.log("Purchase allowed");
    } else {
        console.log("Not enough money");
    }

} else {
    console.log("Purchase denied");
}
```

Primeiro:

```text
age >= 18
→ true

!isBlocked
→ true

true && true
→ true
```

Entra no primeiro `if`.

Depois:

```text
money >= price
80 >= 100
→ false

hasCoupon
→ true

false || true
→ true
```

Resultado:

```text
Purchase allowed
```

---

# 31. Operators — Referência rápida

## Assignment

| Símbolo | Inglês                  | Português  |
| ------- | ----------------------- | ---------- |
| `=`     | **Assignment Operator** | Atribuição |

## Comparison

| Símbolo | Inglês                                | Português            |
| ------- | ------------------------------------- | -------------------- |
| `===`   | **Strict Equality Operator**          | Igualdade estrita    |
| `!==`   | **Strict Inequality Operator**        | Desigualdade estrita |
| `>`     | **Greater Than Operator**             | Maior que            |
| `<`     | **Less Than Operator**                | Menor que            |
| `>=`    | **Greater Than or Equal To Operator** | Maior ou igual       |
| `<=`    | **Less Than or Equal To Operator**    | Menor ou igual       |

## Logical

| Símbolo | Inglês                   | Português      |                         |           |
| ------- | ------------------------ | -------------- | ----------------------- | --------- |
| `&&`    | **Logical AND Operator** | E lógico       |                         |           |
| `       |                          | `              | **Logical OR Operator** | OU lógico |
| `!`     | **Logical NOT Operator** | Negação lógica |                         |           |

## Boolean

```text
true  → verdadeiro
false → falso
```

---

# 32. Vocabulário técnico

| Inglês           | Português             |
| ---------------- | --------------------- |
| Condition        | Condição              |
| Conditional      | Condicional           |
| Statement        | Instrução             |
| Expression       | Expressão             |
| Block            | Bloco                 |
| Evaluate         | Avaliar               |
| Execute          | Executar              |
| Comparison       | Comparação            |
| Equality         | Igualdade             |
| Inequality       | Desigualdade          |
| Strict Equality  | Igualdade estrita     |
| Logical Operator | Operador lógico       |
| Nested           | Aninhado              |
| Boolean          | Booleano              |
| True             | Verdadeiro            |
| False            | Falso                 |
| Branch           | Ramificação / caminho |
| Chain            | Cadeia                |
| Access granted   | Acesso permitido      |
| Access denied    | Acesso negado         |

---

# 33. Frases úteis em inglês para programação

### Condition

> The condition is true.

A condição é verdadeira.

### False

> The condition is false.

A condição é falsa.

### Evaluate

> JavaScript evaluates the condition.

O JavaScript avalia a condição.

### Execute

> The `if` block is executed.

O bloco `if` é executado.

### Else

> The `else` block is executed because the condition is false.

O bloco `else` é executado porque a condição é falsa.

### Logical AND

> Both conditions must be true.

As duas condições precisam ser verdadeiras.

### Logical OR

> At least one condition must be true.

Pelo menos uma condição precisa ser verdadeira.

### First true condition

> JavaScript executes the first true condition in the chain.

O JavaScript executa a primeira condição verdadeira da cadeia.

### Nested condition

> This condition is inside another `if` statement.

Essa condição está dentro de outro `if`.

### Not reached

> The second condition is never reached.

A segunda condição nunca é alcançada.

---

# 34. Erros e armadilhas importantes

## Armadilha 1 — Confundir `=` com `===`

Errado para comparação:

```javascript
if (age = 18) {
}
```

`=` é atribuição.

Para comparação estrita:

```javascript
if (age === 18) {
}
```

---

## Armadilha 2 — Achar que todo `true` será executado

```javascript
if (conditionA) {

} else if (conditionB) {

}
```

Se `conditionA` for `true`, `conditionB` não será avaliada.

---

## Armadilha 3 — Confundir `if` independente com `else if`

```javascript
if (conditionA) {
}

if (conditionB) {
}
```

São independentes.

Já:

```javascript
if (conditionA) {
} else if (conditionB) {
}
```

é uma cadeia.

---

## Armadilha 4 — Esquecer o `!`

```javascript
const isBlocked = false;

if (!isBlocked) {
}
```

Temos:

```text
!false
→ true
```

O `!` inverte o Boolean.

---

## Armadilha 5 — Pensar que uma condição interna sempre será verificada

```javascript
if (conditionA) {
    if (conditionB) {
    }
}
```

Se `conditionA` for `false`, `conditionB` não será alcançada.

---

# 35. Checklist — Aula 04

* [x] Boolean
* [x] `true`
* [x] `false`
* [x] `if`
* [x] `else`
* [x] `else if`
* [x] If Statement
* [x] Else Statement
* [x] Else-If Statement
* [x] Comparison Operators
* [x] `===`
* [x] `!==`
* [x] `>`
* [x] `<`
* [x] `>=`
* [x] `<=`
* [x] Logical Operators
* [x] `&&`
* [x] `||`
* [x] `!`
* [x] `if` independente
* [x] `if / else if / else`
* [x] Nested If
* [x] Ordem de avaliação
* [x] Primeira condição verdadeira
* [x] Condições que não chegam a ser avaliadas
* [x] Condições compostas
* [x] Parênteses em condições
* [x] Vocabulário técnico em inglês
* [x] Frases técnicas em inglês
* [x] Exercícios práticos
* [x] Desafios de raciocínio

---

# 🧠 O que devo saber explicar antes de avançar?

Antes de começar a Aula 05, devo conseguir explicar com minhas próprias palavras:

### 1.

O que acontece quando um `if` recebe uma condição `true`?

### 2.

Qual é a diferença entre:

```javascript
if
```

e:

```javascript
else if
```

### 3.

Qual é a diferença entre:

```javascript
=
```

e:

```javascript
===
```

### 4.

O que significa:

```javascript
!isBlocked
```

quando:

```javascript
isBlocked = false
```

### 5.

Qual é a diferença entre:

```javascript
&&
```

e:

```javascript
||
```

### 6.

O que acontece em uma cadeia quando o primeiro `if` é `true`?

### 7.

Por que um `if` interno pode nunca ser alcançado?

### 8.

Qual é a diferença entre `if` independente e `if / else if / else`?

---

# 🎯 Resultado da Aula

Ao terminar esta aula, o objetivo é entender que um programa pode:

```text
receber informações
      ↓
comparar valores
      ↓
obter true ou false
      ↓
avaliar condições
      ↓
escolher um caminho
      ↓
executar determinado bloco
```

Esse conceito é fundamental para praticamente toda programação.

---

# 📌 Progresso no Roadmap

### JavaScript Básico

**Aula 01 — Fundamentos**
✅ Concluída

**Aula 02 — Strings**
✅ Concluída

**Aula 03 — Variables, Operators e Expressions**
✅ Concluída

**Aula 04 — Conditionals**
✅ Concluída

**Aula 05 — Loops**
⏳ Próxima aula

---

# 🚀 Próxima Aula — Loops

Na Aula 05 vamos aprender como repetir código automaticamente.

Conteúdos previstos:

* O que é um Loop
* Por que usamos Loops
* `for`
* inicialização
* condição
* incremento
* `i++`
* contagem crescente
* contagem regressiva
* como o JavaScript percorre um Loop
* risco de Infinite Loops
* prática
* exercícios
* desafio
* revisão
* vocabulário técnico em inglês

### Pergunta que vamos responder:

> "Se uma loja tiver 100 produtos, preciso escrever o mesmo código 100 vezes?"

**Não.**

É exatamente para resolver esse tipo de problema que vamos aprender **Loops**.

---

## Status

**Aula 04 — Conditionals: ✅ CONCLUÍDA**

**Próximo passo: Aula 05 — Loops**
