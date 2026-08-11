# 📦 CSS — Box Model

> **Módulo:** CSS Basic
> **Objetivo:** entender como o navegador calcula o tamanho, o espaço e os limites dos elementos.

---

# 📚 Cronograma do módulo

Estudaremos nesta ordem:

1. Content
2. `width`
3. `height`
4. Padding
5. Border
6. Margin
7. Margin com 1, 2 e 4 valores
8. `margin: auto`
9. Margin Collapse
10. `gap`
11. `gap` × `margin`
12. `box-sizing`
13. `content-box`
14. `border-box`
15. `min-width` / `max-width`
16. `min-height` / `max-height`
17. `overflow`
18. `overflow-x` / `overflow-y`
19. `box-shadow`
20. `inset`
21. `outline`
22. Revisão
23. Exercícios práticos
24. Desafio

---

# 1. O que é o Box Model?

Todo elemento HTML é tratado pelo navegador como uma **caixa**.

O Box Model possui quatro partes:

```text
┌───────────────────────────────┐
│            MARGIN             │
│  ┌─────────────────────────┐  │
│  │         BORDER          │  │
│  │  ┌───────────────────┐  │  │
│  │  │      PADDING      │  │  │
│  │  │  ┌─────────────┐  │  │  │
│  │  │  │   CONTENT   │  │  │  │
│  │  │  └─────────────┘  │  │  │
│  │  └───────────────────┘  │  │
│  └─────────────────────────┘  │
└───────────────────────────────┘
```

A ordem é:

```text
Content
↓
Padding
↓
Border
↓
Margin
```

### Regra mental

* **Content** = conteúdo
* **Padding** = espaço dentro
* **Border** = borda
* **Margin** = espaço fora

---

# 2. Content

É o conteúdo real do elemento.

Pode ser:

* texto
* imagem
* botão
* outro elemento HTML

Exemplo:

```css
.card {
  width: 300px;
  height: 200px;
}
```

Com `content-box`, `width` e `height` representam inicialmente a área do conteúdo.

### Quando usar?

O `content` existe naturalmente em qualquer elemento. O importante é entender que ele é a área onde o conteúdo fica.

### Erro comum

Pensar que `width: 300px` sempre significa que a caixa inteira terá 300px.

Isso depende do `box-sizing`.

---

# 3. `width`

Define a largura de um elemento.

```css
.card {
  width: 300px;
}
```

### Quando usar?

Quando precisamos controlar ou limitar a largura de um elemento.

### Quando evitar?

Em layouts responsivos, não devemos colocar larguras fixas indiscriminadamente.

Por exemplo:

```css
.card {
  width: 1200px;
}
```

pode causar problemas em uma tela pequena.

Frequentemente usamos combinações como:

```css
width: 100%;
max-width: 500px;
```

### ⚠️ Importante

Sempre considere o `box-sizing`.

---

# 4. `height`

Define a altura de um elemento.

```css
.card {
  height: 200px;
}
```

### Quando usar?

Quando realmente precisamos de uma altura definida.

### Quando evitar?

Evite definir alturas fixas sem necessidade quando o conteúdo pode crescer.

Exemplo potencialmente problemático:

```css
.card {
  height: 100px;
}
```

Se o conteúdo ocupar mais de 100px, poderá ocorrer overflow.

Muitas vezes é melhor deixar a altura ser determinada pelo conteúdo ou usar `min-height`.

---

# 5. Padding

`padding` cria espaço **dentro da caixa**, entre o conteúdo e a border.

```css
.card {
  padding: 20px;
}
```

Visualmente:

```text
┌─────────────────────┐
│      PADDING        │
│   ┌─────────────┐   │
│   │   CONTENT   │   │
│   └─────────────┘   │
└─────────────────────┘
```

### Quando usar?

Use `padding` para:

* dar espaço interno a cards;
* afastar texto da borda;
* criar espaço interno em botões;
* melhorar legibilidade;
* dar "respiro" ao conteúdo.

### Quando não usar?

Não use `padding` simplesmente para separar dois elementos independentes.

Exemplo:

```text
[Card]    [Card]
```

Para controlar a distância entre os cards, normalmente usamos `gap` em Flex/Grid.

### Regra mental

```text
padding = espaço interno
```

---

# 6. Padding com 1 valor

```css
padding: 20px;
```

Aplica:

```text
top    = 20px
right  = 20px
bottom = 20px
left   = 20px
```

---

# 7. Padding com 2 valores

```css
padding: 10px 20px;
```

Regra:

```text
10px → cima + baixo
20px → esquerda + direita
```

Ou:

```text
padding: vertical horizontal;
```

---

# 8. Padding com 4 valores

```css
padding: 10px 20px 30px 40px;
```

Ordem:

```text
Top
Right
Bottom
Left
```

Memorização:

```text
TRBL
```

Resultado:

```text
top    = 10px
right  = 20px
bottom = 30px
left   = 40px
```

---

# 9. Border

`border` é a borda da caixa.

```css
.card {
  border: 2px solid black;
}
```

Uma border possui:

```text
espessura
estilo
cor
```

Exemplo:

```css
border: 5px solid black;
```

### Quando usar?

Use border quando queremos:

* delimitar visualmente um componente;
* criar bordas em cards;
* criar divisores;
* destacar campos;
* criar estilos visuais.

### Quando não usar?

Não use border apenas para criar espaço.

Para espaço interno:

```text
padding
```

Para espaço externo:

```text
margin
```

---

# 10. Margin

`margin` cria espaço **fora da caixa**.

```css
.card {
  margin: 20px;
}
```

### Quando usar?

Use margin para:

* separar elementos;
* criar espaço externo;
* controlar a posição de um elemento em relação aos elementos ao redor.

### Quando não usar?

Quando estiver usando Flexbox ou Grid e quiser simplesmente controlar o espaço **entre os itens**, normalmente `gap` é mais apropriado.

### Regra mental

```text
margin = espaço externo
```

---

# 11. Margin com 1 valor

```css
margin: 20px;
```

Todos os lados:

```text
top    = 20px
right  = 20px
bottom = 20px
left   = 20px
```

---

# 12. Margin com 2 valores

```css
margin: 10px 20px;
```

```text
10px → cima + baixo
20px → esquerda + direita
```

---

# 13. Margin com 4 valores

```css
margin: 10px 20px 30px 40px;
```

Ordem:

```text
Top
Right
Bottom
Left
```

---

# 14. `margin: 0 auto`

Uma forma muito comum de centralizar horizontalmente um elemento que possui largura limitada:

```css
.container {
  width: 300px;
  margin: 0 auto;
}
```

Significa:

```text
0    → cima + baixo
auto → esquerda + direita
```

O navegador distribui o espaço horizontal restante igualmente.

### Quando usar?

Quando queremos centralizar horizontalmente um bloco com largura definida ou limitada.

### Quando não usar?

Não é uma solução universal para centralizar qualquer coisa.

Em Flexbox e Grid existem técnicas próprias de alinhamento.

---

# 15. Margin Collapse

Margens verticais de elementos em fluxo normal podem **colapsar**.

Exemplo:

```css
.a {
  margin-bottom: 30px;
}

.b {
  margin-top: 20px;
}
```

Não devemos automaticamente pensar:

```text
30 + 20 = 50px
```

Em uma situação de margin collapse, a separação pode ser:

```text
30px
```

Ou seja, a maior margem.

### Quando isso acontece?

Principalmente com margens verticais em elementos no fluxo normal.

### Erro comum

Esperar que duas margens verticais sempre sejam somadas.

---

# 16. `gap`

`gap` cria espaço entre itens de layouts como:

```css
display: flex;
```

ou:

```css
display: grid;
```

Exemplo:

```css
.cards {
  display: flex;
  gap: 20px;
}
```

Resultado:

```text
[ CARD ] ← 20px → [ CARD ]
```

### Quando usar?

Use `gap` quando queremos controlar o espaço entre itens de Flexbox ou Grid.

### Quando não usar?

Não é a ferramenta para criar espaço interno dentro de um elemento.

Para isso usamos `padding`.

### Regra mental

```text
gap = espaço entre itens
```

---

# 17. `gap` × `margin`

### `gap`

```text
espaço entre itens de Flex/Grid
```

### `margin`

```text
espaço externo do elemento
```

Exemplo:

```css
.container {
  display: flex;
  gap: 20px;
}
```

é normalmente mais simples e previsível para separar os cards.

### Erro comum

Usar margin em todos os filhos quando um simples `gap` resolveria o problema.

---

# 18. `box-sizing`

`box-sizing` determina como o navegador calcula `width` e `height`.

Os valores mais importantes:

```css
box-sizing: content-box;
```

e:

```css
box-sizing: border-box;
```

---

# 19. `content-box`

É o comportamento padrão.

```css
box-sizing: content-box;
```

Exemplo:

```css
.card {
  width: 300px;
  padding: 20px;
  border: 5px solid black;
}
```

Cálculo:

```text
300px content
+ 20px padding-left
+ 20px padding-right
+ 5px border-left
+ 5px border-right
= 350px
```

Portanto:

```text
content = 300px
caixa total = 350px
```

### Quando usar?

Pode ser útil quando queremos que `width` represente especificamente a área do conteúdo.

### Quando evitar?

Para layouts gerais, `border-box` costuma ser mais previsível e conveniente.

### Regra mental

```text
content-box
→ width/height = content
→ padding + border aumentam a caixa
```

---

# 20. `border-box`

```css
box-sizing: border-box;
```

Aqui:

```text
width/height = caixa inteira
```

Exemplo:

```css
.card {
  width: 300px;
  padding: 20px;
  border: 5px solid black;
  box-sizing: border-box;
}
```

A caixa inteira continua:

```text
300px
```

O conteúdo disponível:

```text
300
- 20 padding-left
- 20 padding-right
- 5 border-left
- 5 border-right
= 250px
```

### Quando usar?

É extremamente útil para layouts previsíveis, especialmente quando usamos:

* `width: 100%`;
* padding;
* border;
* componentes responsivos;
* formulários;
* cards.

### Regra mental

```text
border-box
→ width/height = caixa total
→ padding + border ficam dentro
```

---

# 21. `box-sizing` global

Uma prática muito comum:

```css
* {
  box-sizing: border-box;
}
```

O `*` seleciona todos os elementos.

Também podemos usar:

```css
*,
*::before,
*::after {
  box-sizing: border-box;
}
```

### Por que usar?

Deixa o cálculo dos tamanhos mais previsível.

---

# 22. Exemplo importante: `width: 100%`

Temos:

```css
.container {
  width: 400px;
}

input {
  width: 100%;
  padding: 20px;
  border: 5px solid black;
}
```

Sem `border-box`:

```text
400 content
+ 40 padding
+ 10 border
= 450px
```

O input pode ultrapassar o container.

Com:

```css
* {
  box-sizing: border-box;
}
```

o input total será:

```text
400px
```

O padding e a border ficam dentro dos 400px.

### Erro comum

Pensar:

```text
width: 100%
```

sempre significa:

> "a caixa inteira terá 100%".

Com `content-box`, não necessariamente.

---

# 23. `min-width`

Define a largura mínima.

```css
.card {
  min-width: 300px;
}
```

### Quando usar?

Quando um elemento não deve ficar abaixo de determinado tamanho.

### Quando não usar?

Não coloque mínimos arbitrariamente em elementos que precisam se adaptar a telas muito pequenas.

### Regra mental

```text
min = chão
```

---

# 24. `max-width`

Define a largura máxima.

```css
.card {
  max-width: 600px;
}
```

### Quando usar?

Muito útil para:

* limitar cards;
* limitar textos;
* impedir que conteúdos fiquem largos demais;
* criar layouts mais confortáveis.

### Regra mental

```text
max = teto
```

---

# 25. `min-width` + `max-width`

Exemplo:

```css
.card {
  width: 100%;
  min-width: 300px;
  max-width: 600px;
}
```

A intenção é manter o elemento dentro de uma faixa:

```text
300px ≤ largura ≤ 600px
```

> Em layouts realmente responsivos, precisamos considerar também o espaço disponível e as técnicas que estudaremos nos módulos seguintes.

---

# 26. `min-height`

Define a altura mínima.

```css
.card {
  min-height: 200px;
}
```

### Quando usar?

Quando queremos garantir que um componente tenha uma altura mínima, mas ainda possa crescer com o conteúdo.

---

# 27. `max-height`

Define a altura máxima.

```css
.card {
  max-height: 500px;
}
```

### Quando usar?

Quando precisamos limitar a altura de um elemento.

### Cuidado

Se o conteúdo continuar crescendo depois do limite, precisamos decidir o que fazer com o conteúdo usando `overflow`.

---

# 28. `overflow`

Controla o que acontece quando o conteúdo ultrapassa os limites da caixa.

## `visible`

```css
overflow: visible;
```

O conteúdo pode aparecer para fora.

## `hidden`

```css
overflow: hidden;
```

A parte que ultrapassa é escondida.

## `scroll`

```css
overflow: scroll;
```

Cria uma área de rolagem.

## `auto`

```css
overflow: auto;
```

Permite rolagem quando necessária.

### Quando usar?

Quando o conteúdo pode ultrapassar os limites e precisamos definir um comportamento.

### Quando não usar?

Não use `hidden` automaticamente para "consertar" qualquer problema de layout.

Você pode simplesmente estar escondendo conteúdo que deveria estar visível.

---

# 29. `overflow-x` e `overflow-y`

Podemos controlar cada direção:

```css
.box {
  overflow-x: hidden;
  overflow-y: auto;
}
```

Neste exemplo:

```text
horizontal → hidden
vertical   → auto
```

### Quando usar?

Quando o comportamento horizontal e vertical precisa ser diferente.

---

# 30. `overflow` × `flex-wrap`

Não confundir:

```css
flex-wrap: wrap;
```

com:

```css
overflow: hidden;
```

### `flex-wrap`

Organiza os itens do Flexbox:

```text
[card] [card] [card]
[card] [card]
```

### `overflow`

Controla conteúdo que ultrapassa os limites da caixa.

```text
flex-wrap → organiza itens
overflow  → controla conteúdo que ultrapassa
```

`flex-wrap` será estudado profundamente no módulo de Flexbox.

---

# 31. `box-shadow`

Cria uma sombra visual.

```css
.card {
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
}
```

Estrutura básica:

```text
box-shadow: X Y BLUR COLOR;
```

Exemplo:

```css
box-shadow: 0 10px 20px gray;
```

```text
0     → deslocamento horizontal
10px  → deslocamento vertical
20px  → blur
gray  → cor
```

### Quando usar?

Use para:

* destacar cards;
* criar profundidade;
* criar componentes visualmente elevados;
* dar acabamento visual.

### Quando não usar?

Não use sombras excessivas em todos os elementos.

Muita sombra pode deixar a interface pesada.

---

# 32. Blur

O `blur` controla o quanto a sombra se espalha.

```text
blur pequeno
→ sombra mais concentrada

blur grande
→ sombra mais espalhada e suave
```

Exemplo:

```css
box-shadow: 0 4px 2px gray;
```

é mais concentrada que:

```css
box-shadow: 0 4px 20px gray;
```

---

# 33. `box-shadow` não altera o layout

Exemplo:

```css
.card {
  width: 300px;
  box-shadow: 0 10px 30px gray;
}
```

A largura usada pelo layout continua:

```text
300px
```

A sombra é visual.

---

# 34. `inset`

`inset` coloca a sombra para dentro.

Sombra externa:

```css
box-shadow: 0 5px 15px gray;
```

Sombra interna:

```css
box-shadow: inset 0 0 15px gray;
```

### Regra mental

```text
normal → sombra externa
inset  → sombra interna
```

---

# 35. `outline`

`outline` cria um contorno visual.

```css
.card {
  outline: 2px solid red;
}
```

Ele parece com `border`, mas não funciona da mesma forma.

---

# 36. `border` × `outline`

### Border

```css
border: 5px solid black;
```

A border:

* faz parte da caixa;
* participa do Box Model;
* pode afetar o tamanho dependendo do `box-sizing`.

### Outline

```css
outline: 5px solid red;
```

O outline:

* é visual;
* não ocupa espaço no layout;
* não aumenta a largura/altura calculada.

### Regra mental

```text
border  → participa da caixa
outline → não ocupa espaço
```

---

# 37. Quando usar `outline`

É muito usado para indicar foco:

```css
input:focus {
  outline: 2px solid blue;
}
```

Isso é importante para acessibilidade e navegação pelo teclado.

### Quando não usar?

Não devemos simplesmente remover o `outline` de foco sem fornecer outra indicação visual equivalente.

---

# 38. Box Model — exemplo completo

```css
.card {
  width: 100%;
  max-width: 500px;
  min-width: 300px;

  padding: 20px;

  border: 4px solid black;

  margin: 20px auto;

  box-sizing: border-box;

  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.15);
}
```

O que cada propriedade faz:

```text
width
→ ocupa até 100% do espaço disponível

max-width
→ limita a largura máxima

min-width
→ define uma largura mínima

padding
→ cria espaço interno

border
→ cria a borda

margin
→ cria espaço externo

auto
→ distribui o espaço lateral restante

box-sizing
→ inclui padding + border no tamanho

box-shadow
→ adiciona sombra visual
```

---

# 🧠 Tabela de decisão

| Quero fazer...                       | Normalmente uso...       |
| ------------------------------------ | ------------------------ |
| Espaço dentro do elemento            | `padding`                |
| Espaço fora do elemento              | `margin`                 |
| Espaço entre itens Flex/Grid         | `gap`                    |
| Borda                                | `border`                 |
| Contorno sem ocupar espaço           | `outline`                |
| Limitar largura mínima               | `min-width`              |
| Limitar largura máxima               | `max-width`              |
| Limitar altura mínima                | `min-height`             |
| Limitar altura máxima                | `max-height`             |
| Controlar conteúdo que ultrapassa    | `overflow`               |
| Criar sombra                         | `box-shadow`             |
| Criar sombra interna                 | `box-shadow: inset ...`  |
| Tornar width/height mais previsíveis | `box-sizing: border-box` |

---

# ⚠️ Erros comuns

## ❌ Confundir padding e margin

```text
padding → dentro
margin  → fora
```

## ❌ Confundir gap e margin

```text
gap    → entre itens
margin → espaço externo
```

## ❌ Esquecer `box-sizing`

Antes de calcular a largura real, pergunte:

> Qual é o `box-sizing`?

## ❌ Somar padding e border quando existe `border-box`

Com:

```css
box-sizing: border-box;
width: 300px;
```

os 300px já representam a caixa inteira.

## ❌ Pensar que `outline` aumenta a caixa

Não aumenta.

## ❌ Usar `overflow: hidden` para esconder problemas

Pode esconder conteúdo importante.

## ❌ Colocar `height` fixa em conteúdo que pode crescer

Pode causar overflow.

## ❌ Usar `margin` para tudo

Em Flexbox/Grid, `gap` frequentemente é mais apropriado para separar itens.

## ❌ Usar largura fixa sem pensar na tela

```css
width: 1200px;
```

pode causar problemas em telas menores.

---

# 🧠 Como resolver qualquer questão de Box Model

Antes de calcular, siga esta ordem:

### 1. Qual é o `box-sizing`?

```text
content-box?
border-box?
```

### 2. Qual tamanho estamos procurando?

```text
content?
border box?
caixa total?
```

### 3. Existe padding?

Verifique esquerda/direita e cima/baixo.

### 4. Existe border?

Verifique esquerda/direita e cima/baixo.

### 5. Existe `min` ou `max`?

Esses valores podem limitar o tamanho.

### 6. Existe overflow?

O conteúdo pode ultrapassar?

### 7. É `gap` ou `margin`?

Pergunte:

> Estou criando espaço entre itens ou espaço externo?

---

# 🎯 Checklist de domínio

Antes de passar para o próximo módulo, devo conseguir explicar:

* [ ] O que é o Box Model
* [ ] Content
* [ ] Padding
* [ ] Border
* [ ] Margin
* [ ] `margin: auto`
* [ ] Margin Collapse
* [ ] `gap`
* [ ] `gap` × `margin`
* [ ] `width`
* [ ] `height`
* [ ] `box-sizing`
* [ ] `content-box`
* [ ] `border-box`
* [ ] `min-width`
* [ ] `max-width`
* [ ] `min-height`
* [ ] `max-height`
* [ ] `overflow`
* [ ] `overflow-x`
* [ ] `overflow-y`
* [ ] `box-shadow`
* [ ] `blur`
* [ ] `inset`
* [ ] `outline`
* [ ] `border` × `outline`

---

# 🧪 Prática

Depois da teoria:

### Exercício 1 — cálculo

Resolver situações de:

* `content-box`;
* `border-box`;
* padding;
* border;
* width;
* min/max.

### Exercício 2 — CodePen

Construir pequenos componentes usando:

* width;
* padding;
* border;
* margin;
* gap;
* box-sizing.

### Exercício 3 — layout

Criar cards e controlar:

* tamanho;
* espaço interno;
* espaço externo;
* espaço entre cards;
* limites de largura.

### Exercício 4 — overflow

Criar uma caixa com conteúdo maior que seu espaço e testar:

* `visible`;
* `hidden`;
* `scroll`;
* `auto`.

### Exercício 5 — desafio

Construir uma pequena seção de página sem receber o código pronto.

Você deverá decidir sozinho:

* quando usar `padding`;
* quando usar `margin`;
* quando usar `gap`;
* quando usar `width`;
* quando usar `min/max`;
* quando usar `overflow`;
* quando usar `box-sizing`.

---

# 🚀 Próximo módulo

Depois de terminar os exercícios do Box Model, passaremos para o próximo assunto.

**Não misturar neste README:**

```text
fr
rem
em
%
vw
vh
calc()
clamp()
minmax()
auto-fit
auto-fill
```

Esses conceitos terão seus próprios módulos porque fazem parte de **CSS Units, Sizing, Layout e Responsive Design**.

### Ordem geral

```text
BOX MODEL
    ↓
CSS UNITS & SIZING
    ↓
FLEXBOX
    ↓
GRID
    ↓
RESPONSIVE DESIGN
```

O objetivo é aprender cada parte separadamente e depois juntar tudo para construir páginas reais.
