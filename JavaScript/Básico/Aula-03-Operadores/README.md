# JavaScript — Aula 03: Operadores

## 🎯 Objetivo da aula

Nesta aula aprendemos os principais operadores do JavaScript e começamos a combinar diferentes conceitos para criar pequenas lógicas de programação.

Ao final da aula, devemos conseguir:

* Fazer cálculos matemáticos.
* Alterar valores de variáveis.
* Incrementar e diminuir valores.
* Comparar valores.
* Trabalhar com `true` e `false`.
* Criar condições usando `&&`, `||` e `!`.
* Combinar comparações e operadores lógicos.
* Entender a ordem das operações.
* Saber quando guardar um resultado em uma variável.
* Saber quando usar `const` ou `let`.
* Entender que uma variável não é recalculada automaticamente quando outra variável muda.
* Criar pequenos programas combinando vários conceitos.

---

# 1. Operadores matemáticos

Os operadores matemáticos são utilizados para realizar cálculos.

| Operador | Significado      | Exemplo  |
| -------- | ---------------- | -------- |
| `+`      | Soma             | `10 + 5` |
| `-`      | Subtração        | `10 - 5` |
| `*`      | Multiplicação    | `10 * 5` |
| `/`      | Divisão          | `10 / 5` |
| `%`      | Resto da divisão | `10 % 3` |
| `**`     | Potência         | `2 ** 3` |

### Exemplos

```javascript
console.log(10 + 5);  // 15
console.log(10 - 5);  // 5
console.log(10 * 5);  // 50
console.log(10 / 5);  // 2
console.log(10 % 3);  // 1
console.log(2 ** 3);  // 8
```

---

# 2. O operador `%` — resto da divisão

O `%` não significa porcentagem.

Ele retorna o **resto de uma divisão**.

Exemplo:

```javascript
console.log(10 % 3);
```

Temos:

```text
10 ÷ 3 = 3
3 × 3 = 9
10 - 9 = 1
```

Portanto:

```text
10 % 3 = 1
```

Outro exemplo:

```javascript
console.log(10 % 2);
```

Resultado:

```text
0
```

Isso acontece porque 10 é divisível por 2 sem deixar resto.

O `%` será muito importante mais tarde, principalmente quando estudarmos condições e loops.

---

# 3. Ordem das operações

Quando temos várias operações na mesma expressão, JavaScript segue uma ordem de prioridade.

A ordem principal é:

1. `()`
2. `**`
3. `*`, `/`, `%`
4. `+`, `-`

### Exemplo

```javascript
console.log(10 + 5 * 2);
```

Primeiro:

```text
5 * 2 = 10
```

Depois:

```text
10 + 10 = 20
```

Resultado:

```text
20
```

### Usando parênteses

```javascript
console.log((10 + 5) * 2);
```

Primeiro:

```text
10 + 5 = 15
```

Depois:

```text
15 * 2 = 30
```

Resultado:

```text
30
```

Os parênteses podem mudar completamente o resultado.

---

# 4. Operadores de atribuição

São usados para atribuir ou alterar valores de variáveis.

## `=`

Atribui um valor:

```javascript
let price = 100;
```

---

## `+=`

Adiciona um valor à variável:

```javascript
let price = 100;

price += 20;

console.log(price);
```

Resultado:

```text
120
```

É equivalente a:

```javascript
price = price + 20;
```

---

## `-=`

Subtrai um valor:

```javascript
let price = 100;

price -= 20;

console.log(price);
```

Resultado:

```text
80
```

É equivalente a:

```javascript
price = price - 20;
```

---

## `*=`

Multiplica:

```javascript
let price = 100;

price *= 2;

console.log(price);
```

Resultado:

```text
200
```

É equivalente a:

```javascript
price = price * 2;
```

---

## `/=`

Divide:

```javascript
let price = 100;

price /= 2;

console.log(price);
```

Resultado:

```text
50
```

É equivalente a:

```javascript
price = price / 2;
```

---

# 5. Incremento `++`

O operador `++` aumenta uma variável em 1.

```javascript
let quantity = 3;

quantity++;

console.log(quantity);
```

Resultado:

```text
4
```

É equivalente a:

```javascript
quantity += 1;
```

---

# 6. Decremento `--`

O operador `--` diminui uma variável em 1.

```javascript
let quantity = 3;

quantity--;

console.log(quantity);
```

Resultado:

```text
2
```

É equivalente a:

```javascript
quantity -= 1;
```

---

# 7. `++` e `+= 1`

Esses dois códigos produzem a mesma alteração quando usados sozinhos:

```javascript
quantity++;
```

e:

```javascript
quantity += 1;
```

Ambos aumentam `quantity` em 1.

A diferença importante aparece quando `++` está dentro de uma expressão.

---

# 8. Pós-incremento

```javascript
let number = 5;

console.log(number++);
console.log(number);
```

Resultado:

```text
5
6
```

O valor antigo é utilizado primeiro.

Depois o número é aumentado.

---

# 9. Pré-incremento

```javascript
let number = 5;

console.log(++number);
console.log(number);
```

Resultado:

```text
6
6
```

O valor é aumentado primeiro e depois utilizado.

A mesma ideia existe para `--`.

---

# 10. Operadores de comparação

Os operadores de comparação verificam uma condição.

O resultado será sempre:

```text
true
```

ou:

```text
false
```

| Operador | Significado                | Exemplo     |
| -------- | -------------------------- | ----------- |
| `>`      | Maior que                  | `10 > 5`    |
| `<`      | Menor que                  | `5 < 10`    |
| `>=`     | Maior ou igual             | `10 >= 10`  |
| `<=`     | Menor ou igual             | `5 <= 10`   |
| `===`    | Igual em valor e tipo      | `10 === 10` |
| `!==`    | Diferente em valor ou tipo | `10 !== 20` |

---

# 11. `>` — maior que

```javascript
console.log(10 > 5);
```

Resultado:

```text
true
```

---

# 12. `<` — menor que

```javascript
console.log(5 < 10);
```

Resultado:

```text
true
```

---

# 13. `>=` — maior ou igual

```javascript
console.log(10 >= 10);
```

Resultado:

```text
true
```

10 é igual a 10, então a condição é verdadeira.

---

# 14. `<=` — menor ou igual

```javascript
console.log(5 <= 10);
```

Resultado:

```text
true
```

---

# 15. `===` — igualdade estrita

O `===` verifica:

1. O valor.
2. O tipo de dado.

Exemplo:

```javascript
console.log(10 === 10);
```

Resultado:

```text
true
```

Mas:

```javascript
console.log(10 === "10");
```

Resultado:

```text
false
```

Porque:

```text
10    → Number
"10"  → String
```

Os valores parecem iguais, mas os tipos são diferentes.

---

# 16. `!==` — diferente estrito

Verifica se o valor ou o tipo são diferentes.

```javascript
console.log(10 !== 20);
```

Resultado:

```text
true
```

Também:

```javascript
console.log(10 !== "10");
```

Resultado:

```text
true
```

porque `10` é Number e `"10"` é String.

---

# 17. `==` versus `===`

O `==` também compara valores, mas pode realizar conversão de tipos.

```javascript
console.log(10 == "10");
```

Resultado:

```text
true
```

Já:

```javascript
console.log(10 === "10");
```

Resultado:

```text
false
```

Na prática moderna, normalmente preferimos:

```javascript
===
```

e:

```javascript
!==
```

porque são comparações estritas e mais previsíveis.

---

# 18. Operador lógico `&&`

`&&` significa **E**.

Todas as condições precisam ser verdadeiras.

```javascript
console.log(true && true);
```

Resultado:

```text
true
```

Mas:

```javascript
console.log(true && false);
```

Resultado:

```text
false
```

### Exemplo

```javascript
const age = 25;

console.log(age >= 18 && age <= 60);
```

Temos:

```text
25 >= 18 → true
25 <= 60 → true
```

Então:

```text
true && true → true
```

---

# 19. Operador lógico `||`

`||` significa **OU**.

Pelo menos uma condição precisa ser verdadeira.

```javascript
console.log(true || false);
```

Resultado:

```text
true
```

Quando as duas são falsas:

```javascript
console.log(false || false);
```

Resultado:

```text
false
```

### Exemplo

```javascript
const age = 70;

console.log(age < 12 || age > 65);
```

Temos:

```text
70 < 12 → false
70 > 65 → true
```

Então:

```text
false || true → true
```

---

# 20. Operador lógico `!`

`!` significa **NÃO**.

Ele inverte um valor booleano.

```javascript
console.log(!true);
```

Resultado:

```text
false
```

E:

```javascript
console.log(!false);
```

Resultado:

```text
true
```

---

# 21. Combinando comparação e lógica

Podemos combinar os operadores.

```javascript
const price = 1200;
const quantity = 2;

console.log(price >= 1000 && quantity >= 2);
```

Primeiro:

```text
1200 >= 1000 → true
2 >= 2 → true
```

Depois:

```text
true && true → true
```

Resultado:

```text
true
```

---

# 22. Parênteses em condições

Podemos utilizar parênteses para determinar qual parte será avaliada primeiro.

```javascript
age >= 18 && (hasPermission || isVIP)
```

Primeiro:

```javascript
hasPermission || isVIP
```

Depois o resultado é combinado com:

```javascript
age >= 18
```

Os parênteses também tornam a lógica mais fácil de ler.

---

# 23. Quando guardar um resultado?

Nem todo resultado precisa ser guardado.

Se queremos apenas mostrar o resultado uma vez:

```javascript
console.log(price >= 50 && quantity >= 2);
```

Não precisamos criar uma variável.

Mas se vamos usar o resultado novamente, podemos guardá-lo:

```javascript
const meetsCriteria = price >= 50 && quantity >= 2;
```

Depois podemos utilizar:

```javascript
console.log(meetsCriteria);
```

E posteriormente:

```javascript
if (meetsCriteria) {
    console.log("Produto aprovado");
}
```

### Regra importante

Guardar um resultado **não significa usar sempre `const`**.

A escolha entre `const` e `let` depende de o valor precisar ser reatribuído.

---

# 24. Quando usar `const`?

Usamos `const` quando a variável **não será reatribuída**.

Exemplo:

```javascript
const meetsCriteria = price >= 50 && quantity >= 2;
```

Se não vamos atribuir outro valor a `meetsCriteria`, `const` é apropriado.

Outro exemplo:

```javascript
const age = 39;
```

---

# 25. Quando usar `let`?

Usamos `let` quando o valor poderá ser alterado.

Exemplo:

```javascript
let quantity = 3;

quantity++;
```

Outro exemplo:

```javascript
let total = price * quantity;

total -= discount;
```

Aqui `total` precisa ser `let` porque estamos alterando seu valor.

Não podemos fazer:

```javascript
const total = price * quantity;

total -= discount;
```

Isso gera erro porque estamos tentando reatribuir uma variável declarada com `const`.

---

# 26. Regra prática para `const` e `let`

Pense assim:

```text
O valor vai mudar?
       ↓
      SIM → let
       ↓
      NÃO → const
```

Na prática moderna do JavaScript, uma boa regra é:

> **Use `const` por padrão e `let` quando realmente precisar alterar o valor.**

---

# 27. Variáveis não se atualizam automaticamente

Este foi um conceito importante da prática.

```javascript
let price = 80;
let quantity = 3;

let total = price * quantity;
```

Nesse momento:

```text
80 × 3 = 240
```

Então:

```text
total = 240
```

Depois:

```javascript
quantity++;
```

Agora:

```text
quantity = 4
```

Mas `total` continua:

```text
240
```

JavaScript não recalcula automaticamente `total`.

Para recalcular:

```javascript
total = price * quantity;
```

Agora:

```text
80 × 4 = 320
```

---

# 28. Declaração duplicada de variáveis

Durante a prática encontramos este erro:

```text
Identifier 'price' has already been declared
```

Isso acontece quando tentamos declarar novamente uma variável no mesmo escopo.

Errado:

```javascript
let price = 800;
let price = 1200;
```

Se queremos mudar o valor:

```javascript
let price = 800;

price = 1200;
```

Não usamos `let` novamente.

### Atenção ao CodePen

Durante os exercícios, quando reutilizamos nomes como:

```javascript
let price
let quantity
let total
```

podemos encontrar esse erro se o código anterior continuar sendo executado no mesmo contexto.

Nesse caso, podemos limpar/substituir o código anterior ou utilizar um novo bloco de código organizado.

O importante é entender a diferença entre:

```javascript
let price = 800;
```

e:

```javascript
price = 1200;
```

O primeiro declara a variável.

O segundo apenas altera seu valor.

---

# 29. Exemplo completo — Sistema de loja

Durante a prática criamos um pequeno sistema de loja.

```javascript
let product = "Headphones";
let price = 80;
let quantity = 3;

let total = price * quantity;

let discount = 20;

total -= discount;

const meetsCriteria = price >= 50 && quantity >= 2;

quantity++;

console.log(
  `Produto: ${product}\n` +
  `Preço: ${price}\n` +
  `Quantidade: ${quantity}\n` +
  `Total: ${total}\n` +
  `Produto atende aos critérios: ${meetsCriteria}`
);
```

Resultado:

```text
Produto: Headphones
Preço: 80
Quantidade: 4
Total: 220
Produto atende aos critérios: true
```

Neste exercício combinamos:

* `let`
* `const`
* Strings
* Numbers
* multiplicação
* `-=`
* `>=`
* `&&`
* Boolean
* `++`
* template literals
* `\n`
* variáveis
* cálculos
* comparação
* armazenamento de resultado

---

# 30. Erros que encontramos na prática

## Erro 1 — declarar a mesma variável novamente

Errado:

```javascript
let price = 800;
let price = 1200;
```

Correção:

```javascript
let price = 800;

price = 1200;
```

---

## Erro 2 — aplicar o desconto na variável errada

Errado:

```javascript
discount -= total;
```

Se:

```text
discount = 20
total = 240
```

teríamos:

```text
20 - 240 = -220
```

O correto é:

```javascript
total -= discount;
```

Resultado:

```text
240 - 20 = 220
```

---

## Erro 3 — usar `||` quando precisamos de `&&`

Se queremos:

> preço maior ou igual a 50 **E** quantidade maior ou igual a 2

usamos:

```javascript
price >= 50 && quantity >= 2
```

Não:

```javascript
price >= 50 || quantity >= 2
```

---

## Erro 4 — excesso de `+` no incremento

Errado:

```javascript
quantity+++
```

Correto:

```javascript
quantity++;
```

---

# 31. Exercícios realizados

Durante a aula foram realizados exercícios progressivos envolvendo:

### Matemática

* Soma.
* Subtração.
* Multiplicação.
* Divisão.
* Resto.
* Potência.
* Ordem das operações.

### Atribuição

* `=`
* `+=`
* `-=`
* `*=`
* `/=`

### Incremento

* `++`
* `--`
* pré-incremento.
* pós-incremento.

### Comparação

* `>`
* `<`
* `>=`
* `<=`
* `===`
* `!==`

### Lógica

* `&&`
* `||`
* `!`
* combinação de condições.
* parênteses.

### Variáveis

* declaração com `let`.
* declaração com `const`.
* alteração de valores.
* armazenamento de resultados.
* diferença entre declaração e reatribuição.

### Prática

* CodePen.
* sistema simples de loja.
* cálculo de total.
* desconto.
* quantidade.
* verificação de critérios.
* saída organizada no console.

---

# 32. Desafio final

O desafio final consistiu em criar um pequeno sistema de loja.

O programa deveria:

1. Criar um produto.
2. Definir o preço.
3. Definir a quantidade.
4. Calcular o total.
5. Aplicar um desconto.
6. Verificar se o produto atende a determinados critérios.
7. Aumentar a quantidade.
8. Mostrar as informações no console.
9. Utilizar template literals.
10. Utilizar `\n`.
11. Utilizar operadores matemáticos.
12. Utilizar operadores de atribuição.
13. Utilizar operadores de comparação.
14. Utilizar operadores lógicos.

O desafio foi concluído corretamente após as correções.

---

# 33. Checklist da Aula 03

Antes de considerar a aula dominada, devo conseguir explicar:

* [ ] O que fazem `+`, `-`, `*`, `/`, `%` e `**`.
* [ ] O que significa o operador `%`.
* [ ] A ordem básica das operações.
* [ ] O que fazem `+=`, `-=`, `*=`, `/=`.
* [ ] O que fazem `++` e `--`.
* [ ] A diferença entre pré e pós-incremento.
* [ ] O que significam `>`, `<`, `>=` e `<=`.
* [ ] A diferença entre `==` e `===`.
* [ ] O que significa `!==`.
* [ ] Como funciona `&&`.
* [ ] Como funciona `||`.
* [ ] Como funciona `!`.
* [ ] Como usar parênteses em condições.
* [ ] Quando guardar um resultado em uma variável.
* [ ] Quando usar `const`.
* [ ] Quando usar `let`.
* [ ] Por que uma variável não se atualiza automaticamente.
* [ ] A diferença entre declarar e reatribuir uma variável.
* [ ] Como evitar o erro `Identifier has already been declared`.

---

# 34. Resumo rápido para consulta

```text
MATEMÁTICA

+    soma
-    subtração
*    multiplicação
/    divisão
%    resto
**   potência


ATRIBUIÇÃO

=    atribui
+=   soma e atribui
-=   subtrai e atribui
*=   multiplica e atribui
/=   divide e atribui


INCREMENTO

++   aumenta 1
--   diminui 1


COMPARAÇÃO

>    maior
<    menor
>=   maior ou igual
<=   menor ou igual
===  igual em valor e tipo
!==  diferente em valor ou tipo


LÓGICA

&&   E
||   OU
!    NÃO


VARIÁVEIS

const → não será reatribuída
let   → poderá ser alterada
```

---

# 35. Método de estudo utilizado

O curso seguirá o mesmo método em todas as aulas:

```text
TEORIA
↓
EXPLICAÇÃO
↓
EXERCÍCIOS
↓
PRÁTICA
↓
CODEPEN
↓
DESAFIO
↓
CORREÇÃO
↓
REVISÃO
↓
README
```

O conteúdo só será considerado concluído depois dessa sequência.

---

# 📚 Cronograma JavaScript Básico

## ✅ Aula 01 — Fundamentos

* JavaScript.
* `console.log()`.
* Variáveis.
* `let`.
* `const`.
* Tipos básicos.
* String.
* Number.
* Boolean.

## ✅ Aula 02 — Strings

* Strings.
* Concatenação.
* Template literals.
* Interpolação.
* `.length`.
* `.charAt()`.
* `.slice()`.
* `.includes()`.
* `.trim()`.
* `.replace()`.
* `.toUpperCase()`.
* `.toLowerCase()`.
* `\n`.

## ✅ Aula 03 — Operadores

* Operadores matemáticos.
* Ordem das operações.
* Operadores de atribuição.
* Incremento.
* Decremento.
* Comparação.
* Booleanos.
* Operadores lógicos.
* `const` e `let` na prática.
* Armazenamento de resultados.
* Prática com CodePen.
* Desafio de loja.

## ⏭️ Aula 04 — Condicionais

Próxima etapa:

* `if`
* `else`
* `else if`
* blocos `{ }`
* condições simples.
* condições compostas.
* combinação com `&&`, `||` e `!`.
* exercícios.
* prática.
* desafio.
* revisão.
* README.

## 🔜 Próximas etapas

```text
Aula 04 → Condicionais
Aula 05 → Funções
Aula 06 → Arrays
Aula 07 → Objetos
Aula 08 → Loops
Aula 09 → DOM
Aula 10 → Eventos
Aula 11 → JSON
Aula 12 → Debug
Aulas seguintes → Projetos e JavaScript intermediário
```

---

# 📊 Status da Aula

**Aula:** 03
**Tema:** Operadores
**Nível:** JavaScript Básico
**Status:** ✅ Concluída

### Progresso

```text
Aula 01 — Fundamentos     ✅
Aula 02 — Strings         ✅
Aula 03 — Operadores      ✅
Aula 04 — Condicionais    ⏳
```

---

# 🎯 Próxima aula

**Aula 04 — Condicionais**

Na próxima aula vamos aprender a fazer o JavaScript **tomar decisões**.

Exemplo:

```javascript
if (age >= 18) {
    console.log("Pode entrar");
}
```

Depois vamos combinar isso com os operadores que aprendemos nesta aula:

```javascript
if (age >= 18 && hasTicket) {
    console.log("Entrada permitida");
}
```

Assim, os operadores aprendidos na Aula 03 passam a ser utilizados dentro da lógica real dos programas.

**Aula 03 concluída. ✅**
