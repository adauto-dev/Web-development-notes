# JavaScript — Aula 01: Fundamentos

## 🎯 Objetivo

Aprender os fundamentos iniciais de JavaScript:

* `console.log()`
* String
* Number
* Boolean
* Variáveis
* `let`
* `const`
* Atribuição
* Reatribuição
* Operações matemáticas
* Operadores de atribuição
* Case-sensitive

---

# 1. O que é JavaScript?

JavaScript é uma linguagem de programação usada para adicionar lógica e comportamento às páginas e aplicações web.

### HTML, CSS e JavaScript

* **HTML** → estrutura
* **CSS** → aparência
* **JavaScript** → comportamento e lógica

---

# 2. `console.log()`

`console.log()` mostra informações no Console do navegador.

```javascript
console.log('Hello World!');
console.log(100);
console.log(true);
```

### Quando usar

É útil para:

* testar valores;
* verificar se o código está funcionando;
* acompanhar valores durante o desenvolvimento;
* ajudar a encontrar erros.

### Exemplo

```javascript
const name = 'Adauto';

console.log(name);
```

Resultado:

```text
Adauto
```

---

# 3. Tipos básicos

## String

Representa texto.

```javascript
'Hello'
"Hello"
```

## Number

Representa números.

```javascript
100
3.14
```

## Boolean

Representa verdadeiro ou falso.

```javascript
true
false
```

### Atenção

```javascript
100
```

é Number.

Enquanto:

```javascript
'100'
```

é String.

As aspas fazem diferença.

---

# 4. Variáveis

Uma variável armazena um valor para ser utilizado posteriormente.

```javascript
let name = 'Adauto';

console.log(name);
```

---

# 5. `let`

Usamos `let` quando precisamos poder reatribuir outro valor.

```javascript
let score = 0;

score = 100;

console.log(score);
```

Resultado:

```text
100
```

### Regra

Use `let` quando a variável precisar receber outro valor depois.

---

# 6. `const`

Usamos `const` quando não vamos reatribuir outro valor à variável.

```javascript
const name = 'Adauto';
const country = 'Brazil';
```

Não podemos fazer:

```javascript
const name = 'Adauto';

name = 'João';
```

Isso gera erro porque estamos tentando reatribuir uma variável criada com `const`.

### Regra prática

> Prefira `const`. Use `let` quando precisar reatribuir.

---

# 7. `let` vs `const`

| Situação                   | Usar    |
| -------------------------- | ------- |
| Valor não será reatribuído | `const` |
| Valor será reatribuído     | `let`   |

### Exemplo

```javascript
const product = 'T-shirt';

let score = 0;
score = 100;
```

---

# 8. Operador `=`

O operador `=` faz atribuição.

```javascript
let age = 39;
```

Significa que a variável `age` recebe o valor `39`.

Não devemos confundir `=` com comparação. Comparações serão estudadas posteriormente.

---

# 9. Reatribuição

Podemos alterar o valor de uma variável criada com `let`.

```javascript
let price = 50;

price = 60;

console.log(price);
```

Resultado:

```text
60
```

Não precisamos escrever `let` novamente.

---

# 10. Operações matemáticas

JavaScript permite realizar operações matemáticas.

```javascript
10 + 5
10 - 5
10 * 5
10 / 5
```

### Exemplo

```javascript
let score = 10;

score = score + 5;
```

Agora `score` vale `15`.

Podemos continuar:

```javascript
score = score * 2;
```

Agora `score` vale `30`.

---

# 11. Operadores de atribuição

Podemos usar formas abreviadas.

```javascript
score += 5;
```

equivale a:

```javascript
score = score + 5;
```

---

```javascript
score -= 5;
```

equivale a:

```javascript
score = score - 5;
```

---

```javascript
score *= 2;
```

equivale a:

```javascript
score = score * 2;
```

---

```javascript
score /= 2;
```

equivale a:

```javascript
score = score / 2;
```

---

# 12. Ordem das operações

Quando várias operações estão na mesma expressão, seguimos a ordem matemática.

Exemplo:

```javascript
10 + 5 * 2
```

Primeiro:

```text
5 × 2 = 10
```

Depois:

```text
10 + 10 = 20
```

Resultado:

```text
20
```

### Atenção

Instruções em linhas diferentes são executadas de cima para baixo.

```javascript
let score = 10;

score = score + 5;
score = score * 2;
```

Primeiro:

```text
10 + 5 = 15
```

Depois:

```text
15 × 2 = 30
```

Resultado:

```text
30
```

---

# 13. Case-sensitive

JavaScript diferencia letras maiúsculas e minúsculas.

```javascript
name
Name
NAME
```

São nomes diferentes.

Exemplo:

```javascript
const isLearning = true;

console.log(islearning);
```

Está errado porque:

```text
isLearning
```

é diferente de:

```text
islearning
```

---

# 14. Erros comuns

## `console.long()` ❌

Errado:

```javascript
console.long('Hello');
```

Correto:

```javascript
console.log('Hello');
```

---

## Reatribuir `const` ❌

Errado:

```javascript
const price = 50;

price = 60;
```

Se precisamos reatribuir:

```javascript
let price = 50;

price = 60;
```

---

## Declarar a mesma variável novamente ❌

Evite:

```javascript
let score = 10;
let score = 20;
```

Correto:

```javascript
let score = 10;
score = 20;
```

---

## Confundir String com Number ❌

```javascript
100
```

é Number.

```javascript
'100'
```

é String.

---

# 15. `console.log()` não precisa ficar abaixo de cada variável

Isto é correto:

```javascript
const productName = 'T-shirt';
const price = 50;
const quantity = 3;

const total = price * quantity;

console.log(productName);
console.log(price);
console.log(quantity);
console.log(total);
```

O JavaScript executa o código de cima para baixo.

`console.log()` apenas mostra o valor no Console.

---

# 16. Exemplo final da aula

```javascript
const productName = 'T-shirt';
const price = 50;
const quantity = 3;

const total = price * quantity;

console.log(productName);
console.log(price);
console.log(quantity);
console.log(total);
```

Resultado:

```text
T-shirt
50
3
150
```

---

# 🧠 Regras principais

* `console.log()` → mostra valores no Console.
* String → texto.
* Number → número.
* Boolean → `true` ou `false`.
* `let` → pode ser reatribuído.
* `const` → não pode ser reatribuído.
* `=` → atribuição.
* JavaScript é case-sensitive.
* O código é executado de cima para baixo.
* Prefira `const` quando não precisar reatribuir.
* Use `let` quando precisar reatribuir.

---

# ⚠️ O que ainda não estudamos

Não tente decorar estes assuntos ainda:

* Template literals
* Backticks
* `${}`
* Comparações
* Operadores lógicos
* Condicionais
* Functions
* Arrays
* Objects
* DOM
* Events
* APIs
* Async JavaScript

Eles serão estudados nas próximas aulas.

---

# 🏆 Resultado

**Aula 01 — Fundamentos: CONCLUÍDA ✅**

Foi praticado:

* Teoria
* Exercícios
* Prática
* Desafio
* Revisão
* Teste final

**Próxima aula: Aula 02 — Strings**
