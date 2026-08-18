# JavaScript — Aula 02: Strings

## 🎯 Objetivo

Aprender a trabalhar com Strings em JavaScript, desde a criação de textos até métodos utilizados para manipular, pesquisar e transformar Strings.

---

## 1. O que é uma String?

String é um tipo de dado usado para representar texto.

Exemplo:

    const name = 'Adauto';
    const city = "Antwerp";

Também podemos ter números dentro de uma String:

    const phone = '123456789';

Nesse caso, '123456789' é String e não Number.

---

## 2. Aspas simples e duplas

Podemos criar Strings usando aspas simples:

    const name = 'Adauto';

Ou aspas duplas:

    const name = "Adauto";

As duas formas criam uma String.

Para Strings simples, podemos usar qualquer uma das duas. O mais importante é manter consistência no código.

---

## 3. Backticks e Template Literals

Também podemos criar Strings usando backticks:

    const name = `Adauto`;

Os backticks são especialmente importantes porque permitem usar Template Literals.

---

## 4. Template Literals e ${}

Template Literals permitem inserir variáveis dentro de um texto.

    const name = "Adauto";
    const age = 39;

    console.log(`Meu nome é ${name} e tenho ${age} anos.`);

Resultado:

    Meu nome é Adauto e tenho 39 anos.

Estrutura:

    `texto ${variavel} texto`

---

## 5. Expressões dentro de ${}

Também podemos colocar expressões dentro de ${}.

    const price = 50;
    const quantity = 3;

    console.log(`Total: ${price * quantity}`);

Resultado:

    Total: 150

---

## 6. Concatenação

Concatenação significa juntar Strings.

Podemos usar o operador +:

    const firstName = 'Adauto';
    const lastName = 'Gringo';

    const fullName = firstName + ' ' + lastName;

    console.log(fullName);

Resultado:

    Adauto Gringo

Também podemos usar +=:

    let message = 'Olá';

    message += ', ' + name;

Isso equivale a:

    message = message + ', ' + name;

---

## 7. Concatenação vs Template Literal

Podemos escrever:

    console.log('Olá, ' + name);

Ou:

    console.log(`Olá, ${name}`);

Os dois funcionam.

Template Literals normalmente são mais fáceis de ler quando temos várias variáveis dentro de uma frase.

---

## 8. .length

A propriedade .length informa quantos caracteres existem em uma String.

    const word = 'JavaScript';

    console.log(word.length);

Resultado:

    10

Espaços também são considerados caracteres.

---

## 9. Índices

Podemos acessar caracteres usando [ ].

    const word = 'JavaScript';

    console.log(word[0]);

Resultado:

    J

JavaScript começa os índices em 0.

    J a v a S c r i p t
    0 1 2 3 4 5 6 7 8 9

Importante:

    word.length

indica a quantidade de caracteres.

Enquanto:

    word[0]

acessa o caractere na posição 0.

---

## 10. .toUpperCase()

Converte uma String para letras maiúsculas.

    const name = 'adauto';

    console.log(name.toUpperCase());

Resultado:

    ADAUTO

---

## 11. .toLowerCase()

Converte uma String para letras minúsculas.

    const name = 'ADAUTO';

    console.log(name.toLowerCase());

Resultado:

    adauto

---

## 12. .includes()

Verifica se uma String contém determinado texto.

    const message = 'I am learning JavaScript';

    console.log(message.includes('JavaScript'));

Resultado:

    true

Se não encontrar:

    console.log(message.includes('Python'));

Resultado:

    false

### ⚠️ Case-sensitive

.includes() diferencia letras maiúsculas e minúsculas.

    'JavaScript'.includes('javascript');

Resultado:

    false

---

## 13. .trim()

Remove espaços do começo e do final da String.

    const name = '   Adauto   ';

    console.log(name.trim());

Resultado:

    Adauto

Importante:

.trim() não altera automaticamente a String original.

Podemos guardar o resultado:

    const text = '   JavaScript is amazing   ';

    const cleanText = text.trim();

Agora temos:

    text
    "   JavaScript is amazing   "

E:

    cleanText
    "JavaScript is amazing"

Se quisermos trabalhar com o texto limpo, usamos cleanText:

    console.log(cleanText);

---

## 14. .replace()

Substitui uma parte de uma String.

    const message = 'I like CSS';

    console.log(message.replace('CSS', 'JavaScript'));

Resultado:

    I like JavaScript

---

## 15. .slice()

Extrai uma parte da String.

    const word = 'JavaScript';

    console.log(word.slice(0, 4));

Resultado:

    Java

Regra importante:

    slice(início, fim)

O índice final não é incluído.

    J a v a S c r i p t
    0 1 2 3 4 5 6 7 8 9

    word.slice(0, 4);

Pega:

    J a v a

---

## 16. .charAt()

Também podemos acessar um caractere usando .charAt().

    const word = 'JavaScript';

    console.log(word.charAt(0));

Resultado:

    J

Também podemos usar:

    word[0];

---

## 17. Métodos precisam de ()

Métodos como:

    toUpperCase()
    toLowerCase()
    includes()
    trim()
    replace()
    slice()
    charAt()

são chamados usando parênteses.

Correto:

    name.toUpperCase();

Errado:

    name.toUpperCase;

---

## 18. Erros importantes encontrados durante a aula

### Esquecer de fechar o Template Literal

Errado:

    console.log(`Olá, ${name});

Correto:

    console.log(`Olá, ${name}`);

---

### Usar ${} com aspas normais

Errado:

    console.log('Olá, ${name}');

Correto:

    console.log(`Olá, ${name}`);

---

### Confundir console.log() com atribuição

Errado:

    console.log = 'Olá';

Correto:

    console.log('Olá');

---

### Usar uma variável que não existe

Errado:

    console.log(word.charAt(0));

quando word não foi criada.

Se temos:

    const text = 'JavaScript';

devemos usar:

    console.log(text.charAt(0));

---

### Criar uma String limpa e continuar usando a original

    const text = '   JavaScript   ';

    const cleanText = text.trim();

text continua com os espaços.

Para usar o texto limpo:

    console.log(cleanText);

---

# 🧪 Prática no CodePen

Durante a aula foram praticados:

- Strings
- Aspas simples
- Aspas duplas
- Backticks
- Template Literals
- ${}
- Concatenação
- +=
- .length
- Índices
- .toUpperCase()
- .toLowerCase()
- .includes()
- .trim()
- .replace()
- .slice()
- .charAt()

---

# 🏆 Desafio Final

Foi criado no CodePen um programa utilizando:

- trim()
- toUpperCase()
- toLowerCase()
- includes()
- length
- Template Literals
- ${}

O desafio foi realizado no CodePen e funcionou corretamente.

---

# 📌 Resumo dos principais recursos

| Recurso | Função |
|---|---|
| 'texto' | Criar String |
| "texto" | Criar String |
| `texto` | Template Literal |
| ${} | Inserir variável ou expressão |
| + | Concatenar |
| += | Adicionar ou juntar valor |
| .length | Quantidade de caracteres |
| [0] | Acessar caractere |
| .toUpperCase() | Converter para maiúsculas |
| .toLowerCase() | Converter para minúsculas |
| .includes() | Verificar se contém texto |
| .trim() | Remover espaços das extremidades |
| .replace() | Substituir texto |
| .slice() | Extrair parte da String |
| .charAt() | Acessar caractere |

---

# 🎯 O que aprendi nesta aula

- Strings representam textos.
- Strings podem usar aspas simples, aspas duplas ou backticks.
- Template Literals permitem inserir variáveis usando ${}.
- O operador + pode concatenar Strings.
- += pode adicionar texto ao valor existente.
- .length informa a quantidade de caracteres.
- Os índices começam em 0.
- .toUpperCase() transforma texto em maiúsculas.
- .toLowerCase() transforma texto em minúsculas.
- .includes() verifica se determinado texto existe.
- .trim() remove espaços das extremidades.
- .replace() substitui texto.
- .slice() extrai uma parte da String.
- .charAt() acessa um caractere.
- Métodos precisam ser chamados com ().
- O resultado de métodos como trim() pode ser guardado em uma nova variável.

---

# ✅ Status da Aula

Aula 02 — Strings: CONCLUÍDA

- Teoria: ✅
- Exercícios: ✅
- Prática: ✅
- CodePen: ✅
- Desafio: ✅
- Revisão: ✅
- README: ✅

---

# 📚 Próxima aula

## Aula 03 — Operadores

Conteúdos previstos:

- Operadores aritméticos
- +
- -
- *
- /
- %
- **
- Ordem das operações
- Operadores de atribuição
- +=
- -=
- *=
- /=
- Incremento e decremento
- Exercícios
- CodePen
- Desafio
- Revisão
