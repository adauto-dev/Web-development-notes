# JavaScript — Aula 05: Loops

## 📚 Aula 05 — Loops

**Nível:** JavaScript Básico
**Status:** ✅ Concluída
**Roadmap:** Full Stack 2.4
**Método:** Teoria → Exercícios → Prática → Desafio → Debugging → Revisão

---

# 🎯 Objetivos da Aula

Ao final desta aula, o objetivo é compreender e utilizar:

* Loops
* `for`
* `while`
* Contadores
* Inicialização
* Condição
* Atualização
* Incremento e decremento
* `break`
* `continue`
* Nested loops
* Acumuladores
* Operador `%`
* Loops combinados com `if`
* Infinite loops
* Debugging de loops
* Diferença entre `for` e `while`
* Problemas práticos usando múltiplos conceitos

---

# 🗓️ Cronograma da Aula 05

## 🔵 Segunda — Fundamentos de Loops

### Conteúdo

* O que é um loop
* Repetição de código
* `for`
* Inicialização
* Condição
* Atualização
* Counter
* Increment
* Decrement

### Estrutura principal

```javascript
for (inicialização; condição; atualização) {
    // código repetido
}
```

### Exemplo

```javascript
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```

---

## 🔵 Terça — Loops na Prática

### Conteúdo

* `for` com diferentes condições
* `while`
* Nested loops
* Contadores
* Acumuladores
* `break`
* `continue`
* Infinite loops
* Debugging
* Problemas práticos
* Desafios

---

# 🔁 O que é um Loop?

Um **loop** é uma estrutura de programação usada para executar um bloco de código repetidamente enquanto uma determinada regra ou condição permitir.

Em inglês:

**loop = repetição / laço**

Cada execução do bloco é chamada de:

**iteration = iteração**

Exemplo:

```javascript
for (let i = 1; i <= 3; i++) {
    console.log(i);
}
```

Resultado:

```text
1
2
3
```

---

# 🔷 FOR LOOP

## Fórmula / Sintaxe

```javascript
for (inicialização; condição; atualização) {
    // código que será repetido
}
```

### Exemplo

```javascript
for (let i = 1; i <= 10; i++) {
    console.log(i);
}
```

---

## Como ler um `for`

```javascript
for (let i = 1; i <= 10; i++) {
```

### 1. Inicialização

```javascript
let i = 1
```

Cria a variável e define seu valor inicial.

**initialization = inicialização**

---

### 2. Condição

```javascript
i <= 10
```

Enquanto essa condição for verdadeira, o loop continua.

**condition = condição**

`<=` significa:

**less than or equal to = menor ou igual a**

---

### 3. Atualização

```javascript
i++
```

Aumenta `i` em 1.

**update = atualização**

**increment = incremento**

```javascript
i++
```

é equivalente a:

```javascript
i = i + 1;
```

ou:

```javascript
i += 1;
```

---

# ➕ Incremento

```javascript
i++;
```

Aumenta 1.

```javascript
i += 2;
```

Aumenta 2.

```javascript
i += 3;
```

Aumenta 3.

Exemplo:

```javascript
for (let i = 2; i <= 10; i += 2) {
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
```

---

# ➖ Decremento

```javascript
i--;
```

Diminui 1.

**decrement = decremento**

Exemplo:

```javascript
for (let i = 5; i >= 1; i--) {
    console.log(i);
}
```

Resultado:

```text
5
4
3
2
1
```

---

# 🔷 WHILE LOOP

## Fórmula / Sintaxe

```javascript
inicialização;

while (condição) {
    // código repetido

    atualização;
}
```

### Exemplo

```javascript
let i = 1;

while (i <= 5) {
    console.log(i);
    i++;
}
```

---

# Como funciona o `while`

A execução acontece assim:

```text
1. Inicializa
2. Verifica a condição
3. Executa o código
4. Atualiza a variável
5. Volta para a condição
6. Repete enquanto for verdadeira
```

Exemplo:

```javascript
let i = 1;

while (i <= 3) {
    console.log(i);
    i++;
}
```

Resultado:

```text
1
2
3
```

Quando termina:

```text
i = 4
```

Como:

```text
4 <= 3
```

é falso, o loop termina.

---

# 🆚 FOR vs WHILE

## `for`

```javascript
for (inicialização; condição; atualização) {
    // código
}
```

A inicialização, condição e atualização ficam organizadas no cabeçalho.

É muito útil quando temos uma estrutura de contagem ou repetição bem definida.

Exemplo:

```javascript
for (let i = 1; i <= 10; i++) {
    console.log(i);
}
```

---

## `while`

```javascript
inicialização;

while (condição) {
    // código

    atualização;
}
```

A condição fica no centro da estrutura e a atualização normalmente fica dentro do bloco.

É especialmente útil quando a condição é o principal fator que controla a repetição.

---

## Regra prática

```text
FOR
→ repetição com estrutura de contagem bem definida

WHILE
→ repetição controlada por uma condição
```

Essa é uma regra prática, não uma proibição. Os dois podem resolver muitos dos mesmos problemas.

---

# 🔢 COUNTER — Contador

**counter = contador**

É uma variável utilizada para acompanhar a progressão das repetições.

Exemplo:

```javascript
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```

Aqui:

```text
i = counter
```

O contador começa em 1 e aumenta até a condição deixar de ser verdadeira.

---

# 🧮 ACCUMULATOR — Acumulador

**accumulator = acumulador**

Um acumulador guarda e atualiza progressivamente um resultado.

## Fórmula

```javascript
let total = 0;

total += valor;
```

Exemplo:

```javascript
let total = 0;

total += 10;
total += 5;
total += 20;

console.log(total);
```

Resultado:

```text
35
```

---

## Acumulador dentro de um loop

```javascript
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

Evolução:

```text
i = 1 → total = 1
i = 2 → total = 3
i = 3 → total = 6
i = 4 → total = 10
i = 5 → total = 15
```

---

# ➕ `+=`

```javascript
total += i;
```

Significa:

```javascript
total = total + i;
```

O `+=` modifica o valor existente.

Não confundir com:

```javascript
console.log(total);
```

`+=` modifica.

`console.log()` mostra.

---

# 🛑 BREAK

**break = interromper / encerrar**

## Fórmula

```javascript
if (condição) {
    break;
}
```

O `break` encerra o loop completamente.

Exemplo:

```javascript
for (let i = 1; i <= 10; i++) {

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
3
4
5
6
```

Se quisermos imprimir o 7 antes de parar:

```javascript
for (let i = 1; i <= 10; i++) {

    console.log(i);

    if (i === 7) {
        break;
    }
}
```

Resultado:

```text
1
2
3
4
5
6
7
```

### Regra

**`break` → encerra o loop inteiro.**

---

# ⏭️ CONTINUE

**continue = continuar para a próxima iteração**

## Fórmula

```javascript
if (condição) {
    continue;
}
```

O `continue` não encerra o loop.

Ele pula a iteração atual e continua com a próxima.

Exemplo:

```javascript
for (let i = 1; i <= 10; i++) {

    if (i === 5) {
        continue;
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
6
7
8
9
10
```

### Regra

**`continue` → pula somente a iteração atual.**

---

# 🆚 BREAK vs CONTINUE

| Recurso    | O que faz                    |
| ---------- | ---------------------------- |
| `break`    | Encerra o loop completamente |
| `continue` | Pula a iteração atual        |
| `break`    | Não existem mais iterações   |
| `continue` | O loop continua              |

### Visualmente

```text
BREAK

1 → 2 → 3 → 4 → 5 → 🛑 FIM
```

```text
CONTINUE

1 → 2 → 3 → ⏭️ 5 → 6 → 7 → ...
```

---

# ⚠️ CONTINUE + WHILE

Existe uma diferença importante.

No `for`:

```javascript
for (let i = 1; i <= 5; i++) {

    if (i === 3) {
        continue;
    }

    console.log(i);
}
```

O `i++` está no cabeçalho do `for`, então a atualização continua acontecendo.

No `while`, precisamos ter cuidado:

```javascript
let i = 1;

while (i <= 5) {

    if (i === 3) {
        continue;
    }

    console.log(i);
    i++;
}
```

Esse código pode entrar em um **infinite loop**.

Quando `i` chega a 3:

```text
i = 3
↓
continue
↓
i++ não é executado
↓
i continua 3
↓
continue
↓
i continua 3
↓
∞
```

---

## Forma segura

```javascript
let i = 1;

while (i <= 5) {

    if (i === 3) {
        i++;
        continue;
    }

    console.log(i);
    i++;
}
```

Agora o `i` avança antes do `continue`.

---

# ♾️ INFINITE LOOP

**infinite loop = loop infinito**

É quando o loop nunca consegue chegar a uma condição falsa.

Exemplo:

```javascript
let i = 1;

while (i <= 5) {
    console.log(i);
}
```

O problema:

```text
i começa em 1
↓
i <= 5 → true
↓
executa
↓
i continua 1
↓
i <= 5 → true
↓
∞
```

O `i` nunca é atualizado.

### Regra de debugging

Quando encontrar um `while`, pergunte:

> **"O que faz a condição eventualmente se tornar falsa?"**

Em inglês:

**termination condition = condição de término**

---

# 🔷 NESTED LOOPS

**nested loop = loop aninhado**

É um loop dentro de outro loop.

## Fórmula

```javascript
for (...) {

    for (...) {

        // código

    }

}
```

Exemplo:

```javascript
for (let i = 1; i <= 3; i++) {

    for (let j = 1; j <= 2; j++) {

        console.log(i, j);

    }
}
```

Resultado:

```text
1 1
1 2
2 1
2 2
3 1
3 2
```

---

## `i` e `j`

`i` e `j` são apenas nomes de variáveis.

Eles poderiam ser:

```javascript
linha
coluna
```

Por exemplo:

```javascript
for (let linha = 1; linha <= 3; linha++) {

    for (let coluna = 1; coluna <= 4; coluna++) {

        console.log(linha, coluna);

    }
}
```

Resultado:

```text
1 1
1 2
1 3
1 4
2 1
2 2
2 3
2 4
3 1
3 2
3 3
3 4
```

Total:

```text
3 × 4 = 12 execuções
```

### Regra importante

O loop interno executa completamente para cada repetição do loop externo.

Quando `linha` muda:

```text
linha = 1 → coluna 1,2,3,4
linha = 2 → coluna 1,2,3,4
linha = 3 → coluna 1,2,3,4
```

A coluna reinicia em 1 a cada nova linha.

---

# 🔢 OPERADOR `%`

**remainder operator = operador de resto**

O `%` retorna o resto de uma divisão.

Exemplo:

```javascript
10 % 2
```

Resultado:

```text
0
```

---

## Números pares

Para verificar se um número é par:

```javascript
numero % 2 === 0
```

Por quê?

Porque números pares são divisíveis por 2 sem resto.

Exemplo:

```javascript
if (i % 2 === 0) {
    console.log(i);
}
```

---

## Números ímpares

Para verificar se um número é ímpar:

```javascript
numero % 2 !== 0
```

Exemplo:

```javascript
if (i % 2 !== 0) {
    console.log(i);
}
```

### Regra

Para verificar **paridade**:

```text
% 2 === 0 → par
% 2 !== 0 → ímpar
```

O número `2` é específico para verificar paridade porque a definição de par/ímpar depende da divisão por 2.

O `%`, porém, pode ser usado com outros divisores.

---

# 🔗 FOR + IF + CONTINUE

Exemplo:

```javascript
for (let i = 1; i <= 10; i++) {

    if (i === 5) {
        continue;
    }

    console.log(i);
}
```

Uso:

* percorrer valores
* identificar uma condição
* ignorar determinados valores
* continuar o processamento

---

# 🔗 FOR + IF + BREAK

Exemplo:

```javascript
for (let i = 1; i <= 10; i++) {

    if (i === 7) {
        break;
    }

    console.log(i);
}
```

Uso:

* parar quando encontramos o que procuramos
* interromper quando uma condição é atingida
* evitar processamento desnecessário

---

# 🧮 LOOP + ACCUMULATOR + CONDITION

Exemplo:

```javascript
let total = 0;

for (let i = 1; i <= 10; i++) {

    if (i % 2 === 0) {
        total += i;
    }
}

console.log(total);
```

Resultado:

```text
30
```

O programa:

```text
percorre 1–10
↓
verifica se é par
↓
se for par → adiciona ao total
↓
mostra o resultado
```

---

# 🧩 PROBLEMA PRÁTICO FINAL

Problema:

Percorrer os números de 1 até 20.

* Ignorar os números pares.
* Somar somente os ímpares.
* Quando chegar ao 15, parar.
* Mostrar o resultado final.

Solução:

```javascript
let total = 0;

for (let i = 1; i <= 20; i++) {

    if (i % 2 === 0) {
        continue;
    }

    if (i === 15) {
        break;
    }

    total += i;
}

console.log(total);
```

Resultado:

```text
49
```

O programa combina:

```text
for
+
if
+
%
+
continue
+
break
+
accumulator
```

---

# 🐛 DEBUGGING

**debugging = depuração**

Debugging é o processo de encontrar e corrigir problemas no código.

## Estratégia para loops

Quando um loop não funciona:

### 1. Verifique a inicialização

```javascript
let i = 1;
```

### 2. Verifique a condição

```javascript
i <= 10
```

### 3. Verifique a atualização

```javascript
i++;
```

### 4. Verifique `break`

Pergunte:

> O loop está sendo encerrado antes da hora?

### 5. Verifique `continue`

Pergunte:

> Estou pulando uma parte necessária da execução?

### 6. Verifique `while`

Pergunte:

> O que faz a condição eventualmente ficar falsa?

### 7. Use `console.log()` para observar valores

```javascript
console.log(i);
console.log(total);
```

Isso permite acompanhar o estado do programa.

---

# ⚠️ ERROS COMUNS

## Esquecer a atualização

```javascript
let i = 1;

while (i <= 10) {
    console.log(i);
}
```

Pode gerar um loop infinito.

---

## Colocar `continue` antes da atualização em um `while`

```javascript
while (i <= 10) {

    if (condição) {
        continue;
    }

    i++;
}
```

A atualização pode nunca acontecer.

---

## Confundir `break` com `continue`

```text
break → termina
continue → pula e continua
```

---

## Colocar `console.log()` no lugar de uma decisão

Errado:

```javascript
console.log(i === 5) {
```

Correto:

```javascript
if (i === 5) {
```

`console.log()` mostra informações.

`if` toma decisões.

---

## Colocar atualização duas vezes em um `for`

Evitar:

```javascript
for (let i = 1; i <= 10; i++) {

    console.log(i);

    i++;
}
```

O `for` já possui:

```javascript
i++
```

no cabeçalho.

Isso pode fazer o contador avançar duas vezes.

---

# 🧠 CONSOLE.LOG DENTRO VS FORA

Dentro:

```javascript
for (...) {
    total += i;
    console.log(total);
}
```

Mostra a evolução do acumulador.

Fora:

```javascript
for (...) {
    total += i;
}

console.log(total);
```

Mostra somente o resultado final.

---

# 📖 EXERCÍCIOS REALIZADOS

Durante a aula foram praticados:

* Contagem crescente
* Contagem decrescente
* Incrementos diferentes
* Decrementos
* `for`
* `while`
* `break`
* `continue`
* Infinite loop
* Debugging
* Nested loops
* Linhas e colunas
* Accumulator
* Soma de valores
* Soma de números pares
* Soma de números ímpares
* `%`
* `for + if`
* `for + if + continue`
* `for + if + break`
* `while + if + continue`
* Combinação de múltiplos conceitos

---

# 🇬🇧 TECHNICAL ENGLISH

| Inglês                | Português                         |
| --------------------- | --------------------------------- |
| loop                  | loop / repetição                  |
| iteration             | iteração                          |
| condition             | condição                          |
| counter               | contador                          |
| initialization        | inicialização                     |
| update                | atualização                       |
| increment             | incremento                        |
| decrement             | decremento                        |
| termination           | término                           |
| termination condition | condição de término               |
| infinite loop         | loop infinito                     |
| break                 | interromper / encerrar            |
| continue              | continuar para a próxima iteração |
| nested loop           | loop aninhado                     |
| accumulator           | acumulador                        |
| remainder             | resto                             |
| even number           | número par                        |
| odd number            | número ímpar                      |
| debugging             | depuração                         |

### Frases técnicas

**The loop runs five times.**
O loop executa cinco vezes.

**The counter increases by one.**
O contador aumenta em um.

**The condition is false.**
A condição é falsa.

**The loop terminates.**
O loop termina.

**This creates an infinite loop.**
Isso cria um loop infinito.

**The `break` statement exits the loop.**
O `break` encerra o loop.

**The `continue` statement skips the current iteration.**
O `continue` pula a iteração atual.

**The variable stores the accumulated value.**
A variável armazena o valor acumulado.

---

# 📋 REFERÊNCIA RÁPIDA

## FOR

```javascript
for (inicialização; condição; atualização) {
    // código
}
```

**Use:** repetição com estrutura de contagem bem definida.

---

## WHILE

```javascript
inicialização;

while (condição) {
    // código

    atualização;
}
```

**Use:** repetição controlada por uma condição.

---

## BREAK

```javascript
if (condição) {
    break;
}
```

**Use:** encerrar completamente o loop.

---

## CONTINUE

```javascript
if (condição) {
    continue;
}
```

**Use:** pular a iteração atual.

---

## NESTED LOOP

```javascript
for (...) {
    for (...) {
        // código
    }
}
```

**Use:** trabalhar com estruturas dentro de estruturas, como linhas e colunas.

---

## ACCUMULATOR

```javascript
let total = 0;

total += valor;
```

**Use:** acumular resultados.

---

## PAR

```javascript
numero % 2 === 0
```

---

## ÍMPAR

```javascript
numero % 2 !== 0
```

---

# ✅ CHECKLIST DE DOMÍNIO

* [x] Entendo o conceito de loop
* [x] Sei escrever um `for`
* [x] Sei explicar inicialização
* [x] Sei explicar condição
* [x] Sei explicar atualização
* [x] Sei usar `++`
* [x] Sei usar `--`
* [x] Sei usar `+=`
* [x] Sei usar `-=`
* [x] Sei escrever um `while`
* [x] Sei diferenciar `for` e `while`
* [x] Sei usar `break`
* [x] Sei usar `continue`
* [x] Entendo a diferença entre `break` e `continue`
* [x] Entendo nested loops
* [x] Entendo `i` e `j`
* [x] Entendo linhas e colunas
* [x] Sei usar acumuladores
* [x] Sei usar `%` para par/ímpar
* [x] Consigo combinar loops com `if`
* [x] Sei identificar um infinite loop
* [x] Sei fazer debugging básico de loops
* [x] Sei acompanhar valores usando `console.log`
* [x] Conheço o vocabulário técnico em inglês

---

# 🏁 STATUS

**Aula 05 — Loops: ✅ CONCLUÍDA**

### Competências adquiridas

O aluno consegue criar, ler, explicar, combinar e depurar loops básicos em JavaScript, utilizando `for`, `while`, `break`, `continue`, nested loops, counters, accumulators e condições.

**Próxima etapa:** seguir para a próxima aula prevista no cronograma oficial de JavaScript, sem pular conteúdo.
