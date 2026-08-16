
# 📱 Responsive Design — Básico

## 🎯 Objetivo

Aprender os fundamentos necessários para criar layouts que se adaptem ao espaço disponível.

Nesta etapa estudamos principalmente:

* unidades CSS;
* dimensões;
* limites de tamanho;
* overflow;
* box-sizing;
* Grid responsivo;
* imagens responsivas;
* diferenças entre técnicas;
* diagnóstico de problemas em layouts.

---

# 🗺️ Cronograma

```text
RESPONSIVE DESIGN
│
├── 🟢 BÁSICO
│   │
│   ├── Fundamentos
│   │   ├── Responsive Design
│   │   └── Viewport
│   │
│   ├── Unidades
│   │   ├── px
│   │   ├── %
│   │   ├── rem
│   │   ├── em
│   │   ├── vw
│   │   ├── vh
│   │   └── clamp()
│   │
│   ├── Dimensões
│   │   ├── width
│   │   ├── height
│   │   ├── min-width
│   │   ├── max-width
│   │   ├── min-height
│   │   └── max-height
│   │
│   ├── Controle
│   │   ├── box-sizing
│   │   └── overflow
│   │
│   ├── Grid
│   │   ├── display: grid
│   │   ├── grid-template-columns
│   │   ├── fr
│   │   ├── gap
│   │   ├── repeat()
│   │   ├── minmax()
│   │   ├── auto-fit
│   │   └── auto-fill
│   │
│   ├── Imagens
│   │   ├── width: 100%
│   │   ├── max-width: 100%
│   │   ├── height: auto
│   │   ├── object-fit
│   │   ├── cover
│   │   ├── contain
│   │   └── object-position
│   │
│   ├── Flexbox × Grid
│   │
│   └── Prática
│       ├── Exercícios
│       ├── CodePen
│       └── Desafio
│
├── 🟡 INTERMEDIÁRIO
│   ├── Media Queries
│   ├── Breakpoints
│   ├── Mobile First
│   ├── Mobile / Tablet / Desktop
│   └── Orientação
│
└── 🔴 AVANÇADO
    └── Layouts e técnicas avançadas
```

---

# 📚 Legenda

* ✅ Estudado e praticado
* 🔄 Estudado / conceito inicial
* ⬜ Ainda não estudado

---

# 1. Responsive Design

Responsive Design significa criar uma interface capaz de se adaptar a diferentes espaços disponíveis.

O layout pode ser visualizado em:

* celular;
* tablet;
* notebook;
* desktop.

A ideia não é simplesmente diminuir tudo.

O layout pode:

* reduzir o número de colunas;
* reorganizar elementos;
* alterar tamanhos;
* adaptar imagens;
* mudar espaçamentos.

---

# 2. Viewport

Viewport é a área disponível para visualização da página no navegador.

A largura e a altura do viewport podem mudar.

Isso é importante para entender:

* `%`;
* `vw`;
* `vh`;
* Grid responsivo;
* layouts fluidos.

🔄 Conceito estudado.

O aprofundamento de viewport × dispositivos ficará para o Responsive Intermediário.

---

# 3. `px`

`px` representa pixels CSS.

Exemplo:

```css
.card {
  width: 300px;
}
```

### Quando usar

Útil quando precisamos de um valor específico e previsível.

Exemplos:

* pequenas bordas;
* detalhes;
* dimensões específicas;
* alguns limites mínimos.

### Quando não usar

Não devemos construir todo o layout responsivo apenas com larguras fixas em `px`.

---

# 4. `%`

Percentual é relativo ao espaço de referência.

Exemplo:

```css
.container {
  width: 90%;
}
```

Se o espaço de referência for `1000px`:

```text
1000 × 90%
= 900px
```

## Quando usar

Bom para:

* containers;
* larguras fluidas;
* elementos que devem acompanhar o espaço disponível.

## Quando não usar

Não significa que todos os elementos precisam ter:

```css
width: 100%;
```

Devemos deixar o Grid/Flexbox controlar o espaço quando apropriado.

---

# 5. `rem`

`rem` é relativo ao tamanho da fonte do elemento raiz (`html`).

Normalmente:

```text
1rem = 16px
```

Exemplo:

```css
html {
  font-size: 16px;
}

.title {
  font-size: 2rem;
}
```

Resultado:

```text
2 × 16px = 32px
```

## Quando usar

Muito útil para:

* fontes;
* espaçamentos;
* padding;
* margin;
* escala geral da interface.

## Regra mental

```text
rem
↓
html
↓
raiz
```

---

# 6. `em`

`em` é uma unidade relativa ao contexto do tamanho da fonte.

Exemplo:

```css
.box {
  font-size: 20px;
}

.box h2 {
  font-size: 2em;
}
```

Resultado:

```text
2 × 20px
= 40px
```

## `em` × `rem`

```text
rem
→ referência no html

em
→ referência no contexto
```

Exemplo:

```css
html {
  font-size: 16px;
}

.box {
  font-size: 20px;
}

.box h2 {
  font-size: 2em;
}

.box p {
  font-size: 2rem;
}
```

Resultado:

```text
h2 = 40px
p  = 32px
```

## Quando usar `em`

É útil quando queremos que partes de um componente acompanhem sua própria escala tipográfica.

Exemplo:

```css
.button {
  font-size: 1rem;
  padding: 0.5em 1em;
}
```

Se a fonte do botão aumentar, o padding em `em` também acompanha.

## Quando não usar

Não é necessário transformar todos os tamanhos em `em`.

Se queremos uma escala global previsível, `rem` pode ser mais simples.

🔄 Conceito estudado / prática inicial.

---

# 7. `vw`

`vw` significa:

> viewport width

```text
1vw = 1% da largura do viewport
```

Se o viewport tiver `800px`:

```text
1vw  = 8px
10vw = 80px
25vw = 200px
50vw = 400px
```

Exemplo:

```css
.box {
  width: 50vw;
}
```

Se a largura do viewport for `800px`:

```text
50vw = 400px
```

## Quando usar

Pode ser útil quando queremos que algo acompanhe diretamente a largura do viewport.

## Quando não usar

Não devemos usar `vw` automaticamente em todos os elementos.

Muitas vezes `%`, `max-width`, `rem` ou Grid são mais apropriados.

🔄 Conceito estudado / prática inicial.

---

# 8. `vh`

`vh` significa:

> viewport height

```text
1vh = 1% da altura do viewport
```

Exemplo:

```css
.hero {
  min-height: 100vh;
}
```

Isso pode fazer uma seção ocupar pelo menos a altura do viewport.

## Quando usar

Útil para:

* seções;
* áreas que precisam acompanhar a altura disponível;
* layouts de tela inteira.

## Quando não usar

Não devemos colocar `height: 100vh` em tudo.

Conteúdo pode precisar de mais espaço e causar problemas.

🔄 Conceito estudado / prática inicial.

---

# 9. `clamp()`

`clamp()` permite definir:

```text
mínimo
+
valor preferido
+
máximo
```

Estrutura:

```css
font-size: clamp(MIN, IDEAL, MAX);
```

Exemplo:

```css
font-size: clamp(1rem, 2vw, 2rem);
```

Significa aproximadamente:

```text
não menor que 1rem
↓
tenta acompanhar 2vw
↓
não maior que 2rem
```

## Quando usar

É muito útil para valores que devem crescer de maneira fluida, mas precisam de limites.

## Quando não usar

Não devemos usar `clamp()` só para deixar o CSS "mais avançado".

Se um valor simples resolve o problema, use uma solução simples.

🔄 Conceito estudado / inicial.

---

# 10. `width`

Controla a largura.

```css
.card {
  width: 300px;
}
```

Pode usar:

```css
width: 300px;
width: 90%;
width: 50vw;
width: 20rem;
```

A unidade depende do objetivo.

---

# 11. `height`

Controla a altura.

```css
.card {
  height: 200px;
}
```

## ⚠️ Cuidado

Alturas fixas podem causar problemas quando o conteúdo precisa de mais espaço.

Quando não precisamos de uma altura específica, deixar o conteúdo determinar a altura pode ser melhor.

---

# 12. `min-width`

Define o menor tamanho permitido.

```css
.card {
  min-width: 180px;
}
```

Muito importante para Grid responsivo.

---

# 13. `max-width`

Define o limite máximo.

Exemplo:

```css
.container {
  width: 90%;
  max-width: 1200px;
}
```

Mesmo que a tela seja enorme, o container não passa de `1200px`.

## Regra mental

```text
width
→ tamanho desejado

max-width
→ teto
```

---

# 14. `min-height`

Define uma altura mínima.

```css
.section {
  min-height: 300px;
}
```

O conteúdo ainda pode fazer o elemento crescer além disso.

---

# 15. `max-height`

Define uma altura máxima.

```css
.box {
  max-height: 500px;
}
```

⚠️ Se o conteúdo ultrapassar esse limite, pode ocorrer overflow.

---

# 16. `box-sizing`

Uma configuração muito útil:

```css
* {
  box-sizing: border-box;
}
```

Com `border-box`, a largura/altura declarada inclui:

```text
conteúdo
+
padding
+
border
```

Isso torna o controle de dimensões mais previsível.

---

# 17. `overflow`

Overflow acontece quando o conteúdo ultrapassa a área disponível.

Pode ocorrer por:

* largura fixa;
* altura fixa;
* imagem grande;
* texto;
* padding;
* elementos mal dimensionados.

Antes de usar:

```css
overflow: hidden;
```

devemos descobrir a causa.

### Regra

```text
problema de overflow
↓
descobrir a causa
↓
corrigir o layout
```

e não simplesmente esconder o problema.

🔄 Conceito estudado / inicial.

---

# 18. Grid

Inicialização:

```css
.grid {
  display: grid;
}
```

Grid trabalha muito bem com linhas e colunas.

---

# 19. `grid-template-columns`

Define as colunas.

```css
.grid {
  grid-template-columns: 1fr 1fr 1fr;
}
```

Ou:

```css
.grid {
  grid-template-columns: repeat(3, 1fr);
}
```

---

# 20. `fr`

`fr` representa uma fração do espaço disponível no Grid.

```css
grid-template-columns: 1fr 2fr;
```

Temos:

```text
1fr + 2fr
= 3 partes
```

Se houver `900px`:

```text
900 ÷ 3 = 300px

1fr = 300px
2fr = 600px
```

---

# 21. `gap`

Define o espaço entre os itens:

```css
.grid {
  gap: 15px;
}
```

É preferível a criar margens individuais apenas para separar os itens do Grid.

---

# 22. `repeat()`

Evita repetição:

```css
grid-template-columns:
  repeat(3, 1fr);
```

É equivalente a:

```css
grid-template-columns:
  1fr 1fr 1fr;
```

---

# 23. `minmax()`

Estrutura:

```css
minmax(MIN, MAX)
```

Exemplo:

```css
minmax(180px, 1fr)
```

Significa:

```text
mínimo = 180px
máximo = 1fr
```

A coluna não deve ficar menor que o mínimo e pode crescer conforme o espaço disponível.

---

# 24. `auto-fit`

Exemplo:

```css
.grid {
  display: grid;

  grid-template-columns:
    repeat(auto-fit, minmax(180px, 1fr));

  gap: 15px;
}
```

O Grid calcula quantas colunas conseguem caber.

Quando a largura diminui, os cards podem passar para novas linhas.

Isso permite criar um Grid responsivo sem precisar imediatamente de Media Queries.

---

# 25. `auto-fill`

Também pode ser usado:

```css
grid-template-columns:
  repeat(auto-fill, minmax(180px, 1fr));
```

A ideia é preencher a quantidade de colunas que cabe no espaço disponível, mesmo quando algumas posições calculadas podem permanecer vazias.

---

# 26. `auto-fit` × `auto-fill`

Regra mental inicial:

```text
auto-fit
→ ajusta as colunas existentes

auto-fill
→ mantém as colunas que cabem
```

A diferença fica mais perceptível quando existem poucos itens e sobra espaço.

🔄 `auto-fill` = conceito inicial.

Ainda precisamos praticar especificamente:

```text
auto-fit × auto-fill
```

antes de considerar esse assunto dominado.

---

# 27. Flexbox × Grid

### Flexbox

Normalmente trabalha melhor em uma dimensão:

```text
linha
OU
coluna
```

### Grid

Trabalha muito bem com:

```text
linhas
+
colunas
```

Regra mental:

```text
Flexbox
→ uma dimensão

Grid
→ duas dimensões
```

Isso é uma regra prática, não uma obrigação absoluta.

---

# 28. Imagens responsivas

## `width: 100%`

```css
img {
  width: 100%;
}
```

A imagem ocupa a largura disponível.

---

# 29. `max-width: 100%`

```css
img {
  max-width: 100%;
}
```

Impede que a imagem ultrapasse a largura disponível.

---

# 30. `height: auto`

```css
img {
  width: 100%;
  height: auto;
}
```

Mantém a proporção original.

Exemplo:

```text
800 × 400
↓
largura reduzida
↓
altura reduzida proporcionalmente
```

---

# 31. `object-fit`

Controla como uma imagem se encaixa dentro da caixa definida.

Principais valores estudados:

```text
cover
contain
```

---

# 32. `object-fit: cover`

```css
.card img {
  width: 100%;
  height: 180px;
  object-fit: cover;
}
```

A imagem:

* preenche a caixa;
* mantém a proporção;
* pode cortar partes da foto;
* não deve ficar deformada.

Ideal para:

* cards;
* thumbnails;
* galerias;
* imagens de produtos.

---

# 33. `object-fit: contain`

```css
.card img {
  width: 100%;
  height: 180px;
  object-fit: contain;
}
```

A imagem tenta aparecer inteira.

Pode sobrar espaço dentro da caixa.

### Regra mental

```text
cover
→ preencher
→ pode cortar

contain
→ mostrar inteira
→ pode sobrar espaço
```

---

# 34. `object-position`

Controla **qual parte da imagem fica visível** quando existe corte.

Exemplo:

```css
.card img {
  width: 100%;
  height: 180px;
  object-fit: cover;
  object-position: center;
}
```

Valores comuns:

```css
object-position: center;
object-position: top;
object-position: bottom;
object-position: left;
object-position: right;
```

Por exemplo:

```css
object-position: top;
```

prioriza a parte superior da imagem.

### `object-fit` × `object-position`

```text
object-fit
→ como a imagem preenche a caixa

object-position
→ qual parte da imagem fica posicionada/visível
```

🔄 Conceito estudado / prática inicial.

---

# 35. Exemplo completo

```css
* {
  box-sizing: border-box;
}

.container {
  width: 90%;
  max-width: 1200px;
  margin: 0 auto;
}

.grid {
  display: grid;

  grid-template-columns:
    repeat(auto-fit, minmax(180px, 1fr));

  gap: 15px;
}

.card {
  border: 2px solid red;
  border-radius: 5px;
  background: lightgrey;
}

.card img {
  width: 100%;
  height: 180px;
  object-fit: cover;
  object-position: center;
}

.card h2,
.card p {
  padding: 1px;
  margin: 10px;
}
```

---

# 36. 🧠 Como interpretar esse código

### Container

```css
width: 90%;
max-width: 1200px;
margin: 0 auto;
```

```text
90% do espaço
↓
máximo de 1200px
↓
centralizado
```

### Grid

```css
repeat(auto-fit, minmax(180px, 1fr))
```

```text
quantas colunas couberem
↓
mínimo de 180px
↓
podem crescer
↓
quando não couberem
↓
passam para outra linha
```

### Imagem

```css
width: 100%;
height: 180px;
object-fit: cover;
```

```text
largura do card
+
altura controlada
+
preenche a caixa
+
mantém proporção
+
pode cortar
```

---

# 37. ❌ Erros encontrados durante a prática

## `obeject-fit`

Errado:

```css
obeject-fit: cover;
```

Correto:

```css
object-fit: cover;
```

---

## `conver`

Errado:

```css
object-fit: conver;
```

Correto:

```css
object-fit: cover;
```

---

## `padding: 0 auto`

Errado:

```css
padding: 0 auto;
```

`auto` não funciona dessa forma para `padding`.

Para centralização horizontal:

```css
margin: 0 auto;
```

---

## `.card h2 p`

Isso significa:

```css
.card h2 p
```

um `p` dentro de um `h2`.

Se queremos selecionar ambos:

```css
.card h2,
.card p {
}
```

---

## Alturas diferentes nas imagens

Com:

```css
height: auto;
```

imagens com proporções diferentes podem apresentar alturas diferentes.

Para criar cards visualmente uniformes:

```css
width: 100%;
height: 180px;
object-fit: cover;
```

---

## Aumentar `minmax()` demais

Exemplo:

```css
minmax(300px, 1fr)
```

Se não houver espaço suficiente para várias colunas, menos colunas vão caber.

Isso pode fazer cards descerem para novas linhas.

Não é necessariamente um erro.

---

# 38. Quando usar cada técnica

| Problema                             | Solução possível         |
| ------------------------------------ | ------------------------ |
| largura fluida                       | `%`                      |
| limitar largura                      | `max-width`              |
| tamanho mínimo                       | `min-width`              |
| altura mínima                        | `min-height`             |
| escala global                        | `rem`                    |
| escala relacionada à fonte           | `em`                     |
| largura do viewport                  | `vw`                     |
| altura do viewport                   | `vh`                     |
| tamanho fluido com limites           | `clamp()`                |
| distribuir espaço no Grid            | `fr`                     |
| espaço entre itens                   | `gap`                    |
| mínimo + crescimento                 | `minmax()`               |
| Grid adaptável                       | `auto-fit`               |
| manter possíveis colunas             | `auto-fill`              |
| imagem ocupar largura                | `width: 100%`            |
| impedir imagem maior que o container | `max-width: 100%`        |
| manter proporção                     | `height: auto`           |
| preencher caixa                      | `object-fit: cover`      |
| mostrar imagem inteira               | `object-fit: contain`    |
| escolher área visível                | `object-position`        |
| incluir padding/border no tamanho    | `box-sizing: border-box` |

---

# 39. Quando NÃO usar

## Não usar `vw` em tudo

Se o elemento deve acompanhar o container, `%` ou Grid pode ser mais apropriado.

## Não usar `vh` em tudo

Uma altura baseada no viewport pode não ser adequada para conteúdos de tamanho variável.

## Não usar `height` fixa sem necessidade

Pode causar overflow.

## Não usar `cover` em toda imagem

Pode cortar informações importantes.

## Não usar `contain` em toda imagem

Pode deixar espaços vazios.

## Não usar `overflow: hidden` apenas para esconder um erro

Primeiro descubra a causa.

## Não usar `100%` automaticamente

O Grid/Flexbox pode já controlar o tamanho.

## Não usar `em` para tudo

Use quando a relação com a tipografia/contexto for desejada.

---

# 40. 🧪 Exercícios

## Exercício 1 — Unidades

Testar:

```css
px
%
rem
em
vw
vh
```

Alterar o tamanho da janela e observar o comportamento.

---

## Exercício 2 — `em` × `rem`

Criar:

```css
html {
  font-size: 16px;
}

.box {
  font-size: 20px;
}

.box h2 {
  font-size: 2em;
}

.box p {
  font-size: 2rem;
}
```

Calcular antes de olhar o resultado.

Resultado:

```text
h2 = 40px
p  = 32px
```

---

## Exercício 3 — Grid

Criar seis cards usando:

```css
display: grid;
repeat();
minmax();
auto-fit;
1fr;
gap;
```

---

## Exercício 4 — Imagens

Testar:

```css
height: auto;
```

Depois:

```css
height: 180px;
object-fit: cover;
```

Depois:

```css
object-fit: contain;
```

Depois testar:

```css
object-position: top;
object-position: center;
object-position: bottom;
```

---

## Exercício 5 — `auto-fit` × `auto-fill`

Criar o mesmo Grid duas vezes:

```css
repeat(auto-fit, minmax(180px, 1fr));
```

e:

```css
repeat(auto-fill, minmax(180px, 1fr));
```

Usar poucos cards e aumentar bastante a largura do container.

Observar a diferença.

🔄 Ainda precisa ser praticado.

---

# 41. 💻 CodePen

Criar:

```text
Container
│
└── Grid
    │
    ├── Card 1
    ├── Card 2
    ├── Card 3
    ├── Card 4
    ├── Card 5
    └── Card 6
```

Cada card:

```text
imagem
h2
p
```

Praticar:

* `%`;
* `max-width`;
* `margin: 0 auto`;
* Grid;
* `fr`;
* `gap`;
* `minmax()`;
* `auto-fit`;
* imagens responsivas;
* `object-fit`;
* `cover`;
* `contain`;
* `object-position`;
* `box-sizing`.

---

# 42. 🏆 Desafio

Criar uma página com seis cards responsivos.

Requisitos:

```text
container
↓
90%
↓
max-width
↓
centralizado
```

Grid:

```text
auto-fit
+
minmax()
+
1fr
+
gap
```

Imagem:

```text
width: 100%
+
height definida
+
object-fit
+
object-position
```

O layout deve reorganizar os cards quando o espaço diminuir.

---

# 43. 🔎 Checklist para encontrar erros

Quando algo quebrar:

### O card está grande?

Verificar:

```text
width
max-width
padding
border
box-sizing
```

### O card está pequeno?

Verificar:

```text
min-width
minmax()
Grid
```

### O card caiu para outra linha?

Verificar:

```text
minmax()
auto-fit
auto-fill
gap
largura disponível
```

### A imagem está deformada?

Verificar:

```text
width
height
height: auto
object-fit
```

### A imagem está cortando a parte errada?

Verificar:

```text
object-position
```

### Conteúdo saiu da caixa?

Verificar:

```text
overflow
width
height
max-width
```

---

# 44. 📊 Estado atual

## Fundamentos

* [x] Responsive Design
* [x] Viewport — conceito
* [x] `px`
* [x] `%`
* [x] `rem`
* [x] `em` — conceito estudado
* [x] `vw` — conceito estudado
* [x] `vh` — conceito estudado
* [x] `clamp()` — conceito inicial

## Dimensões

* [x] `width`
* [x] `height`
* [x] `min-width`
* [x] `max-width`
* [x] `min-height`
* [x] `max-height`

## Controle

* [x] `box-sizing`
* [x] `overflow` — conceito inicial

## Grid

* [x] `display: grid`
* [x] `grid-template-columns`
* [x] `fr`
* [x] `gap`
* [x] `repeat()`
* [x] `minmax()`
* [x] `auto-fit`
* [x] `auto-fill` — conceito inicial

## Imagens

* [x] `width: 100%`
* [x] `max-width: 100%`
* [x] `height: auto`
* [x] `object-fit`
* [x] `cover`
* [x] `contain`
* [x] `object-position` — conceito inicial

## Layout

* [x] Flexbox × Grid — conceito inicial

---

# 45. 🔄 Conceitos que precisam de prática

```text
auto-fit × auto-fill
clamp()
vw
vh
em
object-position
overflow
Flexbox × Grid
```

Ter sido explicado **não significa domínio completo**.

---

# 46. ⬜ O que ainda NÃO pertence a esta etapa

Não colocar tudo no Básico.

Os seguintes assuntos serão estudados posteriormente:

```text
Media Queries
Breakpoints
Mobile First
Desktop First
Mobile / Tablet / Desktop
Orientação
estratégias avançadas de responsividade
```

Eles entram no **Responsive Intermediário**.

Também não misturar:

```text
position: relative
position: absolute
position: fixed
position: sticky
```

com imagens.

`position` será estudado na etapa própria de layout/posicionamento.

---

# 47. 🗓️ Método de estudo

Para cada etapa:

```text
TEORIA
   ↓
EXERCÍCIOS
   ↓
CODEPEN
   ↓
DESAFIO
   ↓
REVISÃO
   ↓
README
   ↓
FECHAR ETAPA
   ↓
NOVA CONVERSA
   ↓
PRÓXIMO ASSUNTO
```

Não tentar aprender HTML, CSS, JavaScript e Responsive Design profundamente no mesmo dia.

O objetivo é:

```text
entender
↓
praticar
↓
errar
↓
corrigir
↓
conseguir explicar
↓
avançar
```

---

# 48. 🏁 Status

```text
RESPONSIVE DESIGN — BÁSICO

Fundamentos       🔄
Unidades          🔄
Dimensões         🔄
Grid              🔄
Imagens           🔄
Exercícios        ⬜
CodePen           ⬜
Desafio           ⬜
README            🔄
```

O README só deve ser considerado **100% concluído** depois de:

```text
✅ teoria
✅ exercícios
✅ CodePen
✅ desafio
✅ revisão
✅ correção dos erros
```

---

# 49. ➡️ Próxima etapa

Depois de finalizar todos os exercícios desta etapa:

```text
RESPONSIVE DESIGN — INTERMEDIÁRIO
```

A próxima conversa deverá começar pelo primeiro assunto da etapa intermediária, seguindo o cronograma, sem misturar assuntos aleatoriamente.
