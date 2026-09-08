

# JavaScript — Básico

## 🎯 Objetivo

Construir uma base sólida de JavaScript (**JavaScript fundamentals**) para que o aluno consiga:

* entender código JavaScript;
* escrever código do zero;
* compreender a sintaxe;
* entender o propósito de cada estrutura;
* saber quando usar cada recurso;
* resolver problemas de programação;
* identificar e corrigir erros;
* utilizar ferramentas de debugging;
* trabalhar com dados;
* criar funções reutilizáveis;
* trabalhar com arrays e objetos;
* compreender escopo;
* compreender conceitos fundamentais do JavaScript moderno;
* desenvolver vocabulário técnico em inglês;
* preparar-se para DOM, APIs, React, TypeScript, Next.js e Full Stack.

O objetivo não é decorar código.

> **Entender → pensar → escrever → testar → encontrar problemas → corrigir → melhorar.**

---

# 🧭 CRONOGRAMA GERAL

| Nº | Etapa                 | Inglês                 | Status      |
| -- | --------------------- | ---------------------- | ----------- |
| 01 | Fundamentos           | Fundamentals           | ✅ Concluída |
| 02 | Strings               | Strings                | ✅ Concluída |
| 03 | Operadores            | Operators              | ✅ Concluída |
| 04 | Condicionais          | Conditionals           | ✅ Concluída |
| 05 | Loops                 | Loops                  | ✅ Concluída |
| 06 | Funções               | Functions              | ⏳ Pendente  |
| 07 | Arrays                | Arrays                 | ⏳ Pendente  |
| 08 | Métodos de Arrays     | Array Methods          | ⏳ Pendente  |
| 09 | Objetos               | Objects                | ⏳ Pendente  |
| 10 | Escopo                | Scope                  | ⏳ Pendente  |
| 11 | Destructuring         | Destructuring          | ⏳ Pendente  |
| 12 | Spread e Rest         | Spread & Rest          | ⏳ Pendente  |
| 13 | Funções de Alta Ordem | Higher-Order Functions | ⏳ Pendente  |
| 14 | Callbacks             | Callbacks              | ⏳ Pendente  |
| 15 | Tratamento de Erros   | Error Handling         | ⏳ Pendente  |
| 16 | Debugging aprofundado | Advanced Debugging     | ⏳ Pendente  |
| 17 | Integração            | Integration            | ⏳ Pendente  |
| 18 | Projeto               | Project                | ⏳ Pendente  |
| 19 | Revisão Final         | Final Review           | ⏳ Pendente  |

---

# 📚 MÉTODO OFICIAL DAS AULAS

Cada conteúdo novo será trabalhado progressivamente:

### 1. O que é?

Definição do conceito.

### 2. Para que serve?

Qual problema ele resolve.

### 3. Sintaxe

Como escrever.

### 4. Como ler

Como interpretar o código.

### 5. Como funciona

O que acontece quando o código é executado.

### 6. Quando usar

Situações práticas.

### 7. Quando não usar

Erros de escolha ou utilização.

### 8. Exemplos

Exemplos simples antes dos mais complexos.

### 9. Exercícios

Aplicação orientada.

### 10. Prática

Problemas para resolver.

### 11. Desafio

Problema sem solução pronta.

### 12. Debugging

Investigar erros.

### 13. Revisão

Verificar se o conceito realmente foi compreendido.

### 14. README

Documentar o conhecimento.

---

# 🟢 AULA 01 — FUNDAMENTOS

## Fundamentals

📁 `Aula-01-Fundamentos`

### Conteúdo

* JavaScript;
* JavaScript runtime;
* Browser;
* Console;
* `console.log()`;
* comentários;
* statements;
* syntax;
* values;
* variables;
* `let`;
* `const`;
* declaration;
* assignment;
* nomes de variáveis;
* regras básicas de nomenclatura;
* lógica inicial.

### Termos importantes

| Português  | Inglês      |
| ---------- | ----------- |
| linguagem  | language    |
| código     | code        |
| sintaxe    | syntax      |
| valor      | value       |
| variável   | variable    |
| declaração | declaration |
| atribuição | assignment  |
| instrução  | statement   |
| expressão  | expression  |
| comentário | comment     |

### Objetivo

Entender a estrutura básica de um programa JavaScript e começar a escrever código.

**Status: ✅ Concluída**

---

# 🟢 AULA 02 — STRINGS

## Strings

📁 `Aula-02-Strings`

### Conteúdo

* strings;
* texto;
* single quotes;
* double quotes;
* backticks;
* template literals;
* concatenação;
* interpolação;
* comprimento;
* caracteres;
* métodos básicos de strings.

### Aspas

#### Aspas simples — Single quotes

```javascript
let nome = 'Adauto';
```

#### Aspas duplas — Double quotes

```javascript
let nome = "Adauto";
```

#### Backticks

Também chamados de:

**Backticks / Template literals**

```javascript
let mensagem = `Olá, ${nome}`;
```

### Termos importantes

| Português      | Inglês        |
| -------------- | ------------- |
| texto          | text          |
| string         | string        |
| aspas simples  | single quotes |
| aspas duplas   | double quotes |
| crase/backtick | backtick      |
| concatenação   | concatenation |
| interpolação   | interpolation |
| caractere      | character     |
| comprimento    | length        |

### Objetivo

Aprender a trabalhar corretamente com informações textuais.

**Status: ✅ Concluída**

---

# 🟢 AULA 03 — OPERADORES

## Operators

📁 `Aula-03-Operadores`

Os operadores (**operators**) permitem realizar cálculos, comparações, atribuições e operações lógicas.

---

## 3.1 Operadores Aritméticos

### Arithmetic Operators

| Operador | Português        | Inglês             |
| -------- | ---------------- | ------------------ |
| `+`      | Adição           | Addition           |
| `-`      | Subtração        | Subtraction        |
| `*`      | Multiplicação    | Multiplication     |
| `/`      | Divisão          | Division           |
| `%`      | Resto da divisão | Remainder / Modulo |
| `**`     | Exponenciação    | Exponentiation     |

### Exemplo

```javascript
10 + 5
10 - 5
10 * 5
10 / 5
10 % 3
2 ** 3
```

---

## 3.2 Operadores de Comparação

### Comparison Operators

| Operador | Português            | Inglês                   | Função                  |
| -------- | -------------------- | ------------------------ | ----------------------- |
| `===`    | Igualdade estrita    | Strict equality          | compara valor e tipo    |
| `!==`    | Desigualdade estrita | Strict inequality        | verifica diferença      |
| `>`      | Maior que            | Greater than             | verifica se é maior     |
| `<`      | Menor que            | Less than                | verifica se é menor     |
| `>=`     | Maior ou igual       | Greater than or equal to | verifica maior ou igual |
| `<=`     | Menor ou igual       | Less than or equal to    | verifica menor ou igual |

### Exemplo

```javascript
idade >= 18
```

Leitura:

> idade é maior ou igual a 18?

---

## 3.3 Operadores Lógicos

### Logical Operators

| Operador | Português     | Inglês |    |    |
| -------- | ------------- | ------ | -- | -- |
| `&&`     | E             | AND    |    |    |
| `        |               | `      | OU | OR |
| `!`      | NÃO / negação | NOT    |    |    |

### Exemplo

```javascript
idade >= 18 && temDocumento
```

Significa:

> idade é maior ou igual a 18 **E** tem documento?

---

## 3.4 Operadores de Atribuição

### Assignment Operators

| Operador | Nome em inglês            |
| -------- | ------------------------- |
| `=`      | Assignment                |
| `+=`     | Addition assignment       |
| `-=`     | Subtraction assignment    |
| `*=`     | Multiplication assignment |
| `/=`     | Division assignment       |

### Exemplo

```javascript
let total = 10;

total += 5;
```

Equivale a:

```javascript
total = total + 5;
```

---

## 3.5 Incremento e Decremento

| Operador | Significado | Inglês    |
| -------- | ----------- | --------- |
| `++`     | aumenta 1   | Increment |
| `--`     | diminui 1   | Decrement |

Exemplo:

```javascript
i++;
```

Equivale a:

```javascript
i = i + 1;
```

### Objetivo

Aprender a realizar operações matemáticas, comparações e operações lógicas.

**Status: ✅ Concluída**

---

# 🟢 AULA 04 — CONDICIONAIS

## Conditionals

📁 `Aula-04-Conditionals`

Condicionais permitem que o programa tome decisões.

---

## `if`

**if statement**

```javascript
if (condition) {
    // código
}
```

Português:

> se a condição for verdadeira, execute.

---

## `else`

**else statement**

```javascript
if (condition) {
    // código
} else {
    // código
}
```

---

## `else if`

Permite testar outra condição.

```javascript
if (condition1) {

} else if (condition2) {

} else {

}
```

---

## Independent if

Condições independentes:

```javascript
if (condition1) {

}

if (condition2) {

}
```

As duas podem ser executadas.

---

## Conditional chain

Em uma cadeia:

```javascript
if (...) {

} else if (...) {

} else {

}
```

Depois que uma condição verdadeira é encontrada, o restante da cadeia é ignorado.

---

## Nested if

**Nested if = if aninhado**

Um `if` dentro de outro.

---

## Operadores usados

* `===` — Strict equality
* `!==` — Strict inequality
* `>`
* `<`
* `>=`
* `<=`
* `&&` — AND
* `||` — OR
* `!` — NOT

---

## Termos importantes

| Português      | Inglês     |
| -------------- | ---------- |
| condição       | condition  |
| verdadeiro     | true       |
| falso          | false      |
| decisão        | decision   |
| comparação     | comparison |
| se             | if         |
| senão          | else       |
| caso contrário | otherwise  |
| aninhado       | nested     |

### Objetivo

Ensinar o programa a tomar decisões.

**Status: ✅ Concluída**

---

# 🟢 AULA 05 — LOOPS

## Loops

📁 `Aula-05-Loops`

Loops são estruturas de repetição (**iteration / repetition structures**).

---

# `for loop`

Usado principalmente quando a estrutura da repetição é conhecida ou bem definida.

### Sintaxe

```javascript
for (initialization; condition; update) {
    // código
}
```

### Exemplo

```javascript
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```

### Partes

| Parte       | Inglês         | Função   |
| ----------- | -------------- | -------- |
| `let i = 1` | initialization | inicia   |
| `i <= 5`    | condition      | controla |
| `i++`       | update         | atualiza |

---

# `while loop`

Executa enquanto uma condição for verdadeira.

### Sintaxe

```javascript
while (condition) {
    // código
}
```

Exemplo:

```javascript
let i = 1;

while (i <= 5) {
    console.log(i);
    i++;
}
```

---

# `for` × `while`

| `for loop`                  | `while loop`                      |
| --------------------------- | --------------------------------- |
| repetição estruturada       | repetição controlada por condição |
| initialization no cabeçalho | normalmente separado              |
| update no cabeçalho         | normalmente dentro do bloco       |
| ótimo para contadores       | útil quando a condição é o foco   |

---

# `break`

### Break statement

Interrompe completamente o loop.

```javascript
break;
```

---

# `continue`

### Continue statement

Pula a iteração atual e continua o loop.

```javascript
continue;
```

---

# Nested loops

**Nested loop = loop aninhado**

Loop dentro de outro loop.

```javascript
for (let linha = 1; linha <= 3; linha++) {
    for (let coluna = 1; coluna <= 4; coluna++) {
        console.log(linha, coluna);
    }
}
```

---

# Accumulator

### Accumulator = acumulador

Usado para acumular valores.

```javascript
let total = 0;

total += valor;
```

---

# Remainder / Modulo

O operador `%` retorna o resto da divisão.

Exemplo:

```javascript
10 % 2
```

Resultado:

```text
0
```

Pode ser usado para verificar números pares:

```javascript
numero % 2 === 0
```

E ímpares:

```javascript
numero % 2 !== 0
```

---

# Debugging aprendido

Foram trabalhados problemas como:

* loop infinito;
* esquecer a atualização;
* `continue` pulando a atualização;
* posição incorreta de `console.log()`;
* diferença entre resultado intermediário e resultado final;
* lógica incorreta;
* diferença entre Browser e Node.js.

### Termos importantes

| Português     | Inglês        |
| ------------- | ------------- |
| repetição     | repetition    |
| iteração      | iteration     |
| contador      | counter       |
| condição      | condition     |
| atualização   | update        |
| acumulador    | accumulator   |
| interromper   | break         |
| continuar     | continue      |
| loop aninhado | nested loop   |
| loop infinito | infinite loop |
| depuração     | debugging     |

### Objetivo

Aprender a repetir operações e resolver problemas utilizando lógica.

**Status: ✅ Concluída**

---

# ⏳ AULA 06 — FUNÇÕES

## Functions

📁 `Aula-06-Functions`

### Conteúdo planejado

* function;
* function declaration;
* function call;
* parameters;
* arguments;
* return;
* return value;
* múltiplos parâmetros;
* valores padrão;
* reutilização;
* organização do código;
* escopo básico;
* erros comuns;
* debugging.

### Sintaxe

```javascript
function functionName(parameter) {
    // código
}
```

### Chamada

```javascript
functionName(argument);
```

### Retorno

```javascript
return value;
```

### Termos

| Português       | Inglês        |
| --------------- | ------------- |
| função          | function      |
| parâmetro       | parameter     |
| argumento       | argument      |
| chamada         | function call |
| retorno         | return        |
| valor retornado | return value  |
| reutilizável    | reusable      |

**Status: ⏳ Pendente**

---

# ⏳ AULA 07 — ARRAYS

## Arrays

📁 `Aula-07-Arrays`

### Conteúdo planejado

* criação;
* elementos;
* índices;
* index;
* índice `0`;
* acesso;
* alteração;
* `length`;
* percorrer arrays;
* arrays de strings;
* arrays de números;
* arrays de objetos;
* arrays + loops;
* erros comuns.

### Sintaxe

```javascript
const fruits = ["apple", "banana", "orange"];
```

### Acesso

```javascript
fruits[0]
```

### Termos

| Português   | Inglês     |
| ----------- | ---------- |
| array       | array      |
| elemento    | element    |
| índice      | index      |
| posição     | position   |
| comprimento | length     |
| coleção     | collection |

**Status: ⏳ Pendente**

---

# ⏳ AULA 08 — MÉTODOS DE ARRAYS

## Array Methods

📁 `Aula-08-Array-Methods`

### Conteúdo planejado

Métodos fundamentais:

* `push()`;
* `pop()`;
* `shift()`;
* `unshift()`;
* `slice()`;
* `splice()`;
* `includes()`;
* `indexOf()`;
* `join()`.

Posteriormente serão introduzidos métodos de iteração e transformação quando a base estiver preparada.

### Também será estudado

* o que cada método faz;
* sintaxe;
* valor retornado;
* se modifica o array original;
* quando usar;
* erros comuns.

**Status: ⏳ Pendente**

---

# ⏳ AULA 09 — OBJETOS

## Objects

📁 `Aula-09-Objects`

### Conteúdo planejado

* objects;
* properties;
* values;
* keys;
* criação;
* acesso por ponto;
* bracket notation;
* alteração;
* adição;
* remoção;
* nested objects;
* arrays of objects;
* methods;
* objetos em aplicações reais.

### Exemplo que será estudado

```javascript
const user = {
    name: "Adauto",
    age: 39
};
```

### Termos

| Português       | Inglês        |
| --------------- | ------------- |
| objeto          | object        |
| propriedade     | property      |
| chave           | key           |
| valor           | value         |
| método          | method        |
| objeto aninhado | nested object |

**Status: ⏳ Pendente**

---

# ⏳ AULA 10 — ESCOPO

## Scope

📁 `Aula-10-Scope`

### Conteúdo

* global scope;
* function scope;
* block scope;
* escopo de `let`;
* escopo de `const`;
* escopo em `if`;
* escopo em loops;
* escopo de funções;
* erros de acesso;
* boas práticas.

### Objetivo

Entender onde uma variável pode ser utilizada.

**Status: ⏳ Pendente**

---

# ⏳ AULA 11 — DESTRUCTURING

## Destructuring

📁 `Aula-11-Destructuring`

### Conteúdo

* array destructuring;
* object destructuring;
* múltiplas variáveis;
* default values;
* renaming;
* destructuring em funções;
* aplicações práticas.

### Objetivo

Extrair valores de arrays e propriedades de objetos de forma organizada.

**Status: ⏳ Pendente**

---

# ⏳ AULA 12 — SPREAD E REST

## Spread & Rest

📁 `Aula-12-Spread-Rest`

### Conteúdo

* spread operator;
* rest parameter;
* `...`;
* diferença entre spread e rest;
* cópia de arrays;
* combinação de arrays;
* cópia de objetos;
* combinação de objetos;
* múltiplos argumentos;
* aplicações práticas.

### Objetivo

Aprender uma das ferramentas importantes do JavaScript moderno.

**Status: ⏳ Pendente**

---

# ⏳ AULA 13 — HIGHER-ORDER FUNCTIONS

📁 `Aula-13-Higher-Order-Functions`

### Conteúdo

* funções como valores;
* passar funções como argumentos;
* retornar funções;
* funções que trabalham com outras funções;
* relação com arrays;
* preparação para métodos como `map`, `filter` e `reduce`.

### Termos

| Português             | Inglês                  |
| --------------------- | ----------------------- |
| função de alta ordem  | higher-order function   |
| função como argumento | function as an argument |
| retornar uma função   | return a function       |

**Status: ⏳ Pendente**

---

# ⏳ AULA 14 — CALLBACKS

## Callbacks

📁 `Aula-14-Callbacks`

### Conteúdo

* callback;
* passar função como argumento;
* execução de callback;
* callbacks síncronos;
* callbacks em métodos de arrays;
* relação com programação assíncrona;
* preparação para `Promise` e `async/await`, que serão estudados posteriormente.

### Objetivo

Compreender um conceito fundamental do JavaScript moderno.

**Status: ⏳ Pendente**

---

# ⏳ AULA 15 — TRATAMENTO DE ERROS

## Error Handling

📁 `Aula-15-Error-Handling`

### Conteúdo

* syntax errors;
* runtime errors;
* logical errors;
* error messages;
* `try`;
* `catch`;
* `finally`;
* `throw`;
* tratamento de erros;
* debugging.

### Tipos de erro

| Português           | Inglês         |
| ------------------- | -------------- |
| erro de sintaxe     | syntax error   |
| erro de execução    | runtime error  |
| erro lógico         | logical error  |
| mensagem de erro    | error message  |
| tratamento de erros | error handling |

**Status: ⏳ Pendente**

---

# ⏳ AULA 16 — DEBUGGING APROFUNDADO

## Advanced Debugging

📁 `Aula-16-Debugging`

### Conteúdo

* DevTools;
* Console;
* breakpoints;
* debugger;
* inspeção de variáveis;
* Call Stack;
* execução passo a passo;
* leitura de erros;
* localização da origem do problema;
* isolamento do problema;
* criação de hipóteses;
* testes;
* correção;
* prevenção.

### Método

```text
Problem
   ↓
Reproduce
   ↓
Observe
   ↓
Hypothesis
   ↓
Test
   ↓
Fix
   ↓
Verify
```

### Objetivo

Desenvolver autonomia para encontrar e corrigir bugs.

**Status: ⏳ Pendente**

---

# ⏳ AULA 17 — INTEGRAÇÃO

## Integration

📁 `Aula-17-Integracao`

Será necessário combinar os conhecimentos:

* variables;
* strings;
* operators;
* conditionals;
* loops;
* functions;
* arrays;
* array methods;
* objects;
* scope;
* destructuring;
* spread/rest;
* callbacks;
* error handling;
* debugging.

### Objetivo

Resolver problemas que exigem vários conceitos simultaneamente.

**Status: ⏳ Pendente**

---

# ⏳ AULA 18 — PROJETO

## Project

📁 `Aula-18-Projeto`

Será desenvolvido um projeto de JavaScript Básico.

O projeto deverá utilizar conhecimentos reais da etapa, incluindo:

* lógica;
* condições;
* loops;
* funções;
* arrays;
* objetos;
* métodos;
* manipulação de dados;
* debugging;
* organização de código.

O projeto será definido quando chegarmos a essa etapa, de acordo com o conhecimento realmente adquirido.

**Status: ⏳ Pendente**

---

# ⏳ AULA 19 — REVISÃO FINAL

## Final Review

📁 `Aula-19-Revisao-Final`

Antes de sair do JavaScript Básico, será realizada uma avaliação.

## Checklist

### Fundamentals

* [ ] variáveis;
* [ ] `let`;
* [ ] `const`;
* [ ] valores;
* [ ] syntax;
* [ ] statements;
* [ ] expressions.

### Strings

* [ ] strings;
* [ ] single quotes;
* [ ] double quotes;
* [ ] backticks;
* [ ] template literals;
* [ ] operações básicas.

### Operators

* [ ] arithmetic operators;
* [ ] comparison operators;
* [ ] logical operators;
* [ ] assignment operators;
* [ ] increment/decrement;
* [ ] `%`.

### Conditionals

* [ ] `if`;
* [ ] `else`;
* [ ] `else if`;
* [ ] independent `if`;
* [ ] nested `if`;
* [ ] `true`;
* [ ] `false`;
* [ ] operadores lógicos.

### Loops

* [ ] `for`;
* [ ] `while`;
* [ ] `break`;
* [ ] `continue`;
* [ ] nested loops;
* [ ] accumulator;
* [ ] infinite loops.

### Functions

* [ ] declaration;
* [ ] call;
* [ ] parameters;
* [ ] arguments;
* [ ] return.

### Arrays

* [ ] criação;
* [ ] índice;
* [ ] elementos;
* [ ] `length`;
* [ ] percorrer;
* [ ] métodos.

### Objects

* [ ] criação;
* [ ] properties;
* [ ] values;
* [ ] keys;
* [ ] acesso;
* [ ] alteração;
* [ ] nested objects.

### Modern JavaScript

* [ ] scope;
* [ ] destructuring;
* [ ] spread;
* [ ] rest;
* [ ] higher-order functions;
* [ ] callbacks.

### Errors & Debugging

* [ ] entender mensagens de erro;
* [ ] diferenciar syntax/runtime/logical errors;
* [ ] usar `console.log`;
* [ ] utilizar DevTools;
* [ ] investigar bugs;
* [ ] testar hipóteses;
* [ ] corrigir problemas.

**Status: ⏳ Pendente**

---

# 🧠 CAMADA DE APRIMORAMENTO PROFISSIONAL

Esta camada acompanha o curso inteiro.

Ela **não adiciona horas extras** à rotina.

---

## 1. Problem Solving

### Resolução de problemas

Aprender a transformar:

```text
Problema
   ↓
Entender
   ↓
Dividir em partes
   ↓
Criar estratégia
   ↓
Escrever código
   ↓
Testar
   ↓
Encontrar problema
   ↓
Corrigir
   ↓
Verificar
```

---

# 2. Debugging

### Debugging = Depuração

Não significa simplesmente procurar um erro.

Significa investigar **por que** o programa não está funcionando como esperado.

Serão trabalhados progressivamente:

* Console;
* mensagens de erro;
* DevTools;
* breakpoints;
* inspeção de valores;
* Call Stack;
* Network quando necessário;
* reprodução do bug;
* isolamento;
* hipótese;
* teste;
* correção.

---

# 3. Technical English

O inglês técnico será aprendido junto com programação.

Exemplos:

| Português   | Inglês      |
| ----------- | ----------- |
| variável    | variable    |
| valor       | value       |
| tipo        | type        |
| string      | string      |
| número      | number      |
| condição    | condition   |
| expressão   | expression  |
| instrução   | statement   |
| operador    | operator    |
| comparação  | comparison  |
| função      | function    |
| parâmetro   | parameter   |
| argumento   | argument    |
| retorno     | return      |
| array       | array       |
| elemento    | element     |
| índice      | index       |
| objeto      | object      |
| propriedade | property    |
| método      | method      |
| escopo      | scope       |
| erro        | error       |
| depuração   | debugging   |
| repetição   | loop        |
| iteração    | iteration   |
| contador    | counter     |
| acumulador  | accumulator |
| evento      | event       |
| resposta    | response    |
| requisição  | request     |

---

# 4. Code Quality

### Qualidade de código

Progressivamente:

* nomes claros;
* código legível;
* organização;
* evitar repetição desnecessária;
* funções pequenas quando apropriado;
* responsabilidade clara;
* consistência;
* manutenção.

---

# 5. Acessibilidade

Acessibilidade será aplicada principalmente quando começarmos a trabalhar com HTML, interfaces e aplicações.

Exemplos futuros:

* HTML semântico;
* labels;
* teclado;
* contraste;
* textos alternativos;
* estrutura correta.

---

# 6. SEO

SEO será trabalhado principalmente na parte de desenvolvimento web.

Será integrado quando houver contexto real:

* HTML semântico;
* headings;
* metadata;
* estrutura;
* performance;
* acessibilidade.

---

# 7. Performance

Performance será introduzida progressivamente.

O objetivo não é otimizar código sem necessidade.

Primeiro:

> **código correto**

Depois:

> **código organizado**

Depois:

> **código eficiente**

---

# 🌐 AMBIENTES

JavaScript não está limitado ao CodePen.

### Browser

JavaScript pode executar no navegador.

### Node.js

Posteriormente será estudado para:

* backend;
* servidores;
* APIs;
* ferramentas;
* automação.

O ambiente de prática não define os limites da linguagem.

**CodePen é uma ferramenta de prática.**

**JavaScript é a linguagem.**

---

# 🗂️ ORGANIZAÇÃO DO GITHUB

Estrutura atual:

```text
JavaScript/
└── Básico/
    ├── Aula-01-Fundamentos/
    │   └── README.md
    │
    ├── Aula-02-Strings/
    │   └── README.md
    │
    ├── Aula-03-Operadores/
    │   └── README.md
    │
    ├── Aula-04-Conditionals/
    │   └── README.md
    │
    ├── Aula-05-Loops/
    │   └── README.md
    │
    └── README.md
```

As próximas pastas serão criadas somente quando cada etapa começar.

---

# 📈 PROGRESSÃO

Uma aula somente será marcada como concluída quando houver domínio suficiente.

### Processo:

```text
Teoria
   ↓
Sintaxe
   ↓
Compreensão
   ↓
Exercícios
   ↓
Prática
   ↓
Problemas
   ↓
Desafio
   ↓
Debugging
   ↓
Revisão
   ↓
README
   ↓
✅ Concluída
```

Não avançar simplesmente para terminar o cronograma.

---

# 🔗 CAMINHO DO JAVASCRIPT NO ROADMAP FULL STACK 2.4

```text
JavaScript — Básico
        ↓
JavaScript — Médio
        ↓
JavaScript — Avançado
        ↓
HTML + CSS + JavaScript
        ↓
DOM
        ↓
APIs + JSON + Fetch
        ↓
Git + GitHub
        ↓
Web Design + Figma
        ↓
Responsive Design
        ↓
Tailwind CSS
        ↓
React
        ↓
TypeScript
        ↓
Next.js
        ↓
Node.js
        ↓
REST APIs
        ↓
PostgreSQL
        ↓
Prisma
        ↓
Autenticação
        ↓
Testes
        ↓
Segurança
        ↓
Engenharia de Software
        ↓
Arquitetura
        ↓
Linux
        ↓
Docker
        ↓
Cloud + Deploy
        ↓
GraphQL
        ↓
Python
        ↓
IA
        ↓
RAG
        ↓
Tools / Function Calling
        ↓
Agents
        ↓
Multi-Agent
        ↓
Queues / Workers
        ↓
Background Jobs
        ↓
Automação
        ↓
Apps
        ↓
SaaS
        ↓
Freelance + Clientes + Renda Recorrente
```

---

# 📊 PROGRESSO ATUAL

## JavaScript Básico

**01 — Fundamentals** → ✅
**02 — Strings** → ✅
**03 — Operators** → ✅
**04 — Conditionals** → ✅
**05 — Loops** → ✅
**06 — Functions** → ⏳ Próxima etapa
**07 — Arrays** → ⏳
**08 — Array Methods** → ⏳
**09 — Objects** → ⏳
**10 — Scope** → ⏳
**11 — Destructuring** → ⏳
**12 — Spread & Rest** → ⏳
**13 — Higher-Order Functions** → ⏳
**14 — Callbacks** → ⏳
**15 — Error Handling** → ⏳
**16 — Advanced Debugging** → ⏳
**17 — Integration** → ⏳
**18 — Project** → ⏳
**19 — Final Review** → ⏳

---

# 🏁 META DA ETAPA

Ao terminar JavaScript Básico, o aluno deverá ser capaz de olhar para um problema e pensar:

> **"Qual estrutura JavaScript resolve este problema?"**

Em vez de:

> "Qual código devo copiar?"

A meta é construir uma base que permita avançar com segurança para as próximas etapas do Roadmap Full Stack 2.4.

---

# 📌 REGRA DO PROFESSOR

O cronograma mostra **o caminho completo**.

As aulas detalhadas serão ensinadas **uma por uma**.

Nenhuma etapa futura será considerada aprendida antes de ser estudada.

O progresso será atualizado somente quando o conteúdo tiver sido realmente praticado, revisado e validado.

**Próxima etapa oficial: Aula 06 — Functions.**
