
# CSS Flexbox — Intermediário

> Etapa concluída com teoria, exercícios, prática, desafios, DevTools, debugging, consolidação e avaliação.

---

# 📅 Cronograma da etapa

A etapa foi desenvolvida progressivamente, aumentando a dificuldade conforme os conceitos foram sendo combinados.

| Etapa | Conteúdo                                               | Status |
| ----- | ------------------------------------------------------ | ------ |
| 01    | `flex-grow`, `flex-shrink`, `flex-basis`               | 🟢     |
| 02    | Shorthand `flex`                                       | 🟢     |
| 03    | `min-width` e `max-width`                              | 🟢     |
| 04    | Distribuição de espaço + `gap`                         | 🟢     |
| 05    | Cálculos de crescimento e redução                      | 🟢     |
| 06    | Combinação de `basis`, `grow`, `shrink`, `min` e `max` | 🟢     |
| 07    | `box-sizing`, `content-box` e `border-box`             | 🟢     |
| 08    | Padding, border e tamanho real do elemento             | 🟢     |
| 09    | Overflow e identificação de causas                     | 🟢     |
| 10    | DevTools e Box Model                                   | 🟢     |
| 11    | Debugging de Flexbox                                   | 🟢     |
| 12    | Exercícios de consolidação                             | 🟢     |
| 13    | Desafios sem solução pronta                            | 🟢     |
| 14    | Avaliação e fechamento                                 | 🟢     |

### Método utilizado

```text
Teoria
↓
Visualização / previsão
↓
Exercício
↓
Correção
↓
Prática
↓
Desafio
↓
DevTools
↓
Debugging
↓
Consolidação
↓
Avaliação
```

O objetivo não foi apenas conhecer as propriedades, mas conseguir **prever o comportamento do layout, testar no navegador e explicar o resultado**.

---

# 📚 Conteúdo estudado

Nesta etapa foram aprofundados:

* `flex-basis`
* `flex-grow`
* `flex-shrink`
* shorthand `flex`
* `min-width`
* `max-width`
* `gap`
* distribuição de espaço
* crescimento e redução dos Flex Items
* limites mínimos e máximos
* `box-sizing`
* `content-box`
* `border-box`
* `padding`
* `border`
* `overflow`
* cálculos de espaço
* comportamento real dos elementos no DevTools
* debugging de Flexbox

---

# 1. Flex Item

Um elemento filho direto de um container com:

```css
.container {
    display: flex;
}
```

torna-se um **Flex Item**.

Exemplo:

```html
<div class="container">
    <div class="item">A</div>
    <div class="item">B</div>
    <div class="item">C</div>
</div>
```

```css
.container {
    display: flex;
}
```

Os elementos `.item` passam a participar do algoritmo de distribuição de espaço do Flexbox.

O tamanho final de um Flex Item não depende apenas de `width`.

Ele pode ser influenciado por:

* `flex-basis`
* `flex-grow`
* `flex-shrink`
* `min-width`
* `max-width`
* `gap`
* `padding`
* `border`
* `box-sizing`

---

# 2. `flex-basis`

`flex-basis` define o **tamanho inicial de referência** utilizado pelo Flexbox antes da distribuição do espaço.

```css
.item {
    flex-basis: 200px;
}
```

Isso **não significa necessariamente que o item terminará com 200px**.

O tamanho final pode mudar depois da aplicação de:

* `flex-grow`
* `flex-shrink`
* `min-width`
* `max-width`

### Exemplo

```css
.container {
    display: flex;
    width: 700px;
    gap: 20px;
}

.item {
    flex: 1 1 200px;
}
```

Existem:

* 3 itens;
* 2 gaps de 20px.

Gaps:

```text
20 + 20 = 40px
```

Espaço disponível para os itens:

```text
700 - 40 = 660px
```

Bases:

```text
200 + 200 + 200 = 600px
```

Espaço sobrando:

```text
660 - 600 = 60px
```

Com `flex-grow: 1`:

```text
60 ÷ 3 = 20px
```

Resultado:

```text
200 + 20 = 220px
```

Portanto:

```text
flex-basis = 200px
tamanho final = 220px
```

### Regra importante

```text
flex-basis
≠
tamanho final
```

`flex-basis` é a base inicial usada pelo algoritmo.

---

# 3. `flex-grow`

Controla como os Flex Items podem **crescer quando existe espaço sobrando**.

```css
.item {
    flex-grow: 1;
}
```

Quando existe espaço livre, os itens que podem crescer recebem uma parte desse espaço.

### Exemplo

```css
.container {
    display: flex;
    width: 700px;
    gap: 20px;
}

.item {
    flex: 1 1 200px;
}
```

Como visto anteriormente:

```text
Container = 700px
Gaps = 40px
Espaço dos itens = 660px

Bases = 600px

Espaço sobrando = 60px
```

Com `flex-grow: 1`:

```text
60 ÷ 3 = 20px
```

Resultado:

```text
220px por item
```

---

# 4. `flex-shrink`

Controla como os Flex Items podem **diminuir quando não existe espaço suficiente**.

```css
.item {
    flex-shrink: 1;
}
```

Exemplo:

```css
.container {
    display: flex;
    width: 700px;
    gap: 20px;
}

.item {
    flex: 1 1 300px;
}
```

Gaps:

```text
20 + 20 = 40px
```

Espaço dos itens:

```text
700 - 40 = 660px
```

Bases:

```text
300 + 300 + 300 = 900px
```

Falta:

```text
900 - 660 = 240px
```

Os itens precisam diminuir.

Com `flex-shrink: 1`, o Flexbox pode reduzir os itens.

Resultado:

```text
220px por item
```

Total:

```text
220 + 220 + 220 = 660px
```

Mais os gaps:

```text
660 + 40 = 700px
```

O layout fecha exatamente.

---

# 5. Primeiro decidir: Grow ou Shrink?

Essa foi uma das principais regras utilizadas nos exercícios.

### Se existe espaço sobrando:

```text
espaço disponível > bases
```

→ analisar `flex-grow`.

### Se existe falta de espaço:

```text
bases > espaço disponível
```

→ analisar `flex-shrink`.

Somente depois devemos verificar como:

* `min-width`
* `max-width`

interferem no resultado.

---

# 6. Shorthand `flex`

A propriedade:

```css
flex
```

representa:

```text
flex-grow
flex-shrink
flex-basis
```

Exemplo:

```css
.item {
    flex: 1 1 200px;
}
```

Equivale a:

```css
.item {
    flex-grow: 1;
    flex-shrink: 1;
    flex-basis: 200px;
}
```

Também praticamos:

```css
flex: 1;
flex: 2;
flex: auto;
flex: none;
```

O ponto principal é compreender o comportamento do item, e não apenas decorar o shorthand.

---

# 7. `min-width`

Define o **menor tamanho permitido** para o item.

```css
.item {
    min-width: 200px;
}
```

O item não pode ser reduzido abaixo desse limite.

### Exemplo

```css
.container {
    display: flex;
    width: 600px;
    gap: 20px;
}

.item {
    flex: 1;
    min-width: 250px;
}
```

Espaço dos itens:

```text
600 - 40 = 560px
```

Sem o limite:

```text
560 ÷ 3 ≈ 186,67px
```

Mas:

```text
min-width = 250px
```

Então:

```text
250 × 3 = 750px
```

Mais os gaps:

```text
750 + 40 = 790px
```

Como o container tem 600px:

```text
790 > 600
```

Resultado:

```text
overflow
```

### Regra

`min-width` é um **limite mínimo**.

---

# 8. `min-width: 0`

Durante o debugging, descobrimos que:

```css
min-width: 220px;
```

pode impedir que um item encolha o suficiente.

Ao utilizar:

```css
min-width: 0;
```

permitimos que o Flex Item possa diminuir abaixo daquele limite.

### Importante

`min-width: 0` não:

* adiciona espaço;
* remove espaço automaticamente;
* define o tamanho final;
* força o item a ter 0px.

Ele apenas permite que o item seja reduzido abaixo do limite mínimo.

---

# 9. `max-width`

Define o **maior tamanho permitido**.

```css
.item {
    max-width: 250px;
}
```

Se o cálculo tentar deixar o item maior que esse valor, o limite pode impedir o crescimento.

Exemplo:

```css
.container {
    display: flex;
    width: 900px;
    gap: 20px;
}

.item {
    flex: 1 1 150px;
    min-width: 100px;
    max-width: 200px;
}
```

O espaço disponível é grande e os itens podem crescer.

Porém:

```text
max-width = 200px
```

limita o crescimento.

Resultado:

```text
200px por item
```

Mesmo existindo espaço sobrando no container.

---

# 10. `gap`

`gap` cria espaço entre os Flex Items.

```css
.container {
    display: flex;
    gap: 20px;
}
```

Com três itens:

```text
Item | 20px | Item | 20px | Item
```

Existem dois gaps:

```text
20 + 20 = 40px
```

Em um container de 600px:

```text
600 - 40 = 560px
```

ficam disponíveis para os itens.

### Regra

Nos cálculos realizados:

```text
espaço dos itens
=
largura do container
-
espaço ocupado pelos gaps
```

---

# 11. Combinação de propriedades

Exemplo:

```css
.item {
    flex: 1 1 300px;
    min-width: 180px;
    max-width: 260px;
}
```

Temos:

```text
grow = 1
shrink = 1
basis = 300px
min = 180px
max = 260px
```

Processo:

```text
1. Verificar o container
2. Descontar os gaps
3. Somar as bases
4. Comparar bases × espaço disponível
5. Decidir grow ou shrink
6. Verificar min/max
7. Conferir o tamanho final
8. Somar itens + gaps
9. Verificar overflow
```

---

# 12. Bases diferentes

Também praticamos situações em que cada item possui uma base diferente.

Exemplo:

```text
Item A = 300px
Item B = 200px
Item C = 100px
```

Container:

```text
700px
```

Gaps:

```text
40px
```

Espaço dos itens:

```text
700 - 40 = 660px
```

Bases:

```text
300 + 200 + 100 = 600px
```

Sobram:

```text
60px
```

Com crescimento equivalente:

```text
60 ÷ 3 = 20px
```

Resultado:

```text
A = 320px
B = 220px
C = 120px
```

O Flexbox parte das bases individuais de cada item.

---

# 13. `box-sizing`

Estudamos dois comportamentos principais:

```css
box-sizing: content-box;
```

e:

```css
box-sizing: border-box;
```

---

# 14. `content-box`

É o comportamento padrão.

```css
.item {
    width: 200px;
    padding: 20px;
    border: 5px solid black;
}
```

Com `content-box`:

```text
content = 200px
padding = 40px
border = 10px
```

Total físico:

```text
200 + 40 + 10 = 250px
```

Portanto:

```text
width: 200px
```

não significa que o elemento físico terá 200px.

---

# 15. `border-box`

Com:

```css
box-sizing: border-box;
```

a largura total inclui:

* conteúdo;
* padding;
* border.

Exemplo:

```css
.item {
    width: 220px;
    padding: 20px;
    border: 5px solid black;
    box-sizing: border-box;
}
```

Total:

```text
220px
```

Padding:

```text
40px
```

Border:

```text
10px
```

Conteúdo:

```text
220 - 40 - 10 = 170px
```

Portanto:

```text
total = 220px
content = 170px
```

---

# 16. `flex-basis` × tamanho final × conteúdo

Essa diferença foi especialmente importante durante o debugging.

Considere:

```css
.item {
    flex: 1 1 200px;
    padding: 20px;
    border: 5px solid black;
    box-sizing: border-box;
}
```

Existem três conceitos diferentes:

### `flex-basis`

```text
200px
```

É a base inicial usada pelo Flexbox.

### Tamanho final

Pode ser, por exemplo:

```text
220px
```

depois do crescimento.

### Conteúdo

Com:

```text
padding = 40px
border = 10px
```

o conteúdo será:

```text
220 - 40 - 10 = 170px
```

Portanto:

```text
flex-basis = 200px
tamanho final = 220px
content = 170px
```

São três coisas diferentes.

---

# 17. Border do container × border do item

Este foi um dos pontos importantes aprendidos no DevTools.

Exemplo:

```css
.container {
    width: 600px;
    border: 2px solid red;
}
```

Com:

```css
box-sizing: content-box;
```

os `600px` representam o **content box**.

A borda fica fora:

```text
600px de conteúdo
+
2px de border
+
2px de border
=
604px físicos
```

O Flexbox utiliza os:

```text
600px
```

da área de conteúdo como referência para a distribuição interna.

Por isso, a borda do container não reduz os 600px de espaço interno.

Já nos Flex Items, `padding` e `border` fazem parte do Box Model do próprio item.

Com `content-box`, podem aumentar o tamanho físico.

Com `border-box`, ficam incluídos no tamanho total.

---

# 18. Overflow

Overflow ocorre quando os elementos precisam de mais espaço do que o disponível.

Exemplo:

```css
.container {
    display: flex;
    width: 600px;
    gap: 20px;
}

.item {
    flex: 1;
    min-width: 250px;
}
```

Espaço dos itens:

```text
600 - 40 = 560px
```

Mínimo exigido:

```text
250 × 3 = 750px
```

Mais gaps:

```text
750 + 40 = 790px
```

Container:

```text
600px
```

Excesso:

```text
790 - 600 = 190px
```

Resultado:

```text
overflow
```

---

# 19. DevTools

O DevTools foi utilizado como ferramenta de **investigação e debugging**.

Praticamos:

* Elements;
* Styles;
* Computed;
* Box Model;
* inspeção das dimensões;
* alteração de CSS em tempo real;
* observação do Flexbox;
* análise de `padding`;
* análise de `border`;
* comparação entre content e tamanho total;
* identificação de overflow.

---

# 20. Debugging

O método utilizado foi:

```text
Problema
↓
Hipótese
↓
Alteração no DevTools
↓
Observação
↓
Confirmar ou refutar
↓
Correção
```

O objetivo não era simplesmente mudar propriedades até funcionar.

Era descobrir **qual propriedade estava causando o comportamento**.

---

# 21. Exemplo de debugging com `min-width`

```css
.container {
    display: flex;
    width: 600px;
    gap: 20px;
}

.item {
    flex: 1;
    min-width: 250px;
}
```

Cálculo:

```text
600 - 40 = 560px
```

Ideal:

```text
560 ÷ 3 ≈ 186,67px
```

Mas:

```text
min-width = 250px
```

Resultado mínimo:

```text
250 × 3 = 750px
```

Mais gaps:

```text
790px
```

Como:

```text
790 > 600
```

temos overflow.

O problema está no limite mínimo impedir o encolhimento necessário.

---

# 22. Debugging com `box-sizing`

Exemplo:

```css
.item {
    flex: 1 1 250px;
    min-width: 220px;
    padding: 20px;
    border: 5px solid black;
}
```

Adicionamos:

```css
box-sizing: border-box;
```

Isso faz com que padding e border façam parte do tamanho total.

Porém:

> `border-box` sozinho não corrige um problema causado por `min-width`.

Se:

```text
min-width = 220px
```

continua impedindo o shrink, o overflow pode continuar.

Precisamos analisar as duas coisas separadamente.

---

# 23. Debugging com `min-width: 0`

Em um dos exercícios:

```css
.item {
    flex: 1 1 300px;
    min-width: 220px;
    max-width: 260px;
    padding: 30px;
    border: 5px solid black;
    box-sizing: border-box;
}
```

O cálculo exigia que os itens chegassem aproximadamente a:

```text
213,33px
```

Mas:

```text
min-width = 220px
```

impedia essa redução.

O resultado ficava em:

```text
220px
```

por item.

Depois:

```css
min-width: 0;
```

permitiu que o Flexbox reduzisse os itens conforme necessário.

---

# 24. Debugging: quando não existe erro

Também praticamos situações em que o código estava correto.

Verificamos:

* container;
* gaps;
* bases;
* grow/shrink;
* min/max;
* padding;
* border;
* box-sizing;
* tamanho final;
* overflow.

Quando tudo estava correto, a conclusão era:

```text
Não existe bug.
```

Isso também é debugging.

O objetivo é confirmar uma hipótese com evidências, e não obrigatoriamente encontrar um erro.

---

# 25. Exemplo completo de cálculo

```css
.container {
    display: flex;
    width: 750px;
    gap: 25px;
}

.item {
    flex: 1 1 300px;
    min-width: 180px;
    max-width: 260px;
}
```

### Gaps

```text
25 × 2 = 50px
```

### Espaço dos itens

```text
750 - 50 = 700px
```

### Bases

```text
300 × 3 = 900px
```

Existe falta de:

```text
900 - 700 = 200px
```

Então precisamos de `flex-shrink`.

Redução:

```text
200 ÷ 3 ≈ 66,67px
```

Cada item:

```text
300 - 66,67 ≈ 233,33px
```

Limites:

```text
min-width = 180px
max-width = 260px
```

O resultado:

```text
233,33px
```

está dentro dos limites.

Resultado:

```text
Item A ≈ 233,33px
Item B ≈ 233,33px
Item C ≈ 233,33px
```

Total dos itens:

```text
233,33 × 3 ≈ 700px
```

Mais os gaps:

```text
700 + 50 = 750px
```

Layout correto.

---

# 26. Principais problemas que aprendemos a identificar

Durante a etapa identificamos e analisamos problemas como:

### Item não encolhe

Possível causa:

```text
min-width
```

---

### Existe overflow

Investigar:

```text
gap
flex-basis
flex-shrink
min-width
padding
border
box-sizing
```

---

### O tamanho observado é diferente do esperado

Investigar:

```text
flex-basis
tamanho final
padding
border
box-sizing
```

---

### O conteúdo parece menor que o tamanho do item

Verificar:

```text
padding
border
box-sizing
```

---

### `border-box` não resolveu o overflow

Verificar:

```text
min-width
```

porque `border-box` e `min-width` resolvem problemas diferentes.

---

### O item não cresce como esperado

Verificar:

```text
max-width
```

---

### O cálculo parece correto, mas o navegador mostra outro tamanho

Usar:

```text
DevTools
→ Elements
→ Styles
→ Computed
→ Box Model
```

e comparar o resultado real com a previsão.

---

# 27. O que foi aprendido

Ao finalizar esta etapa, fomos capazes de:

* entender o comportamento dos Flex Items;
* trabalhar com `flex-basis`;
* trabalhar com `flex-grow`;
* trabalhar com `flex-shrink`;
* utilizar o shorthand `flex`;
* entender `min-width`;
* entender `max-width`;
* utilizar `gap`;
* calcular espaço disponível;
* calcular crescimento;
* calcular redução;
* trabalhar com bases diferentes;
* identificar overflow;
* entender o Box Model;
* diferenciar `content-box` e `border-box`;
* entender padding e border;
* diferenciar `flex-basis`, tamanho final e content;
* entender `min-width: 0`;
* usar DevTools para investigar;
* testar alterações em tempo real;
* formular hipóteses;
* confirmar ou refutar hipóteses;
* identificar a causa de problemas;
* corrigir problemas de Flexbox;
* reconhecer quando não existe um erro.

---

# 28. Checklist de debugging

## Container

* [ ] `display: flex` está correto?
* [ ] Qual é a largura?
* [ ] Qual é o `gap`?
* [ ] Existe `border`?
* [ ] Qual é o `box-sizing`?

## Flex Items

* [ ] Qual é o `flex-basis`?
* [ ] Qual é o `flex-grow`?
* [ ] Qual é o `flex-shrink`?
* [ ] Existe `min-width`?
* [ ] Existe `max-width`?
* [ ] Existe `padding`?
* [ ] Existe `border`?
* [ ] Qual é o `box-sizing`?

## Cálculo

* [ ] Quanto os gaps ocupam?
* [ ] Quanto sobra para os itens?
* [ ] A soma das bases é maior ou menor?
* [ ] É necessário grow ou shrink?
* [ ] `min-width` está impedindo o shrink?
* [ ] `max-width` está impedindo o grow?
* [ ] Padding e border estão sendo considerados?
* [ ] Existe overflow?

---

# 29. Método aprendido

A habilidade principal desenvolvida nesta etapa foi aprender a:

> **Prever → Testar → Inspecionar → Explicar → Corrigir**

Processo:

```text
1. Ler o CSS
2. Identificar o container
3. Identificar os Flex Items
4. Calcular os gaps
5. Identificar os flex-basis
6. Comparar bases × espaço disponível
7. Determinar grow ou shrink
8. Verificar min/max
9. Considerar padding, border e box-sizing
10. Prever o resultado
11. Testar no DevTools
12. Comparar com a previsão
13. Encontrar a causa
14. Corrigir
15. Confirmar o resultado
```

---

# 30. Conclusão

O **CSS Flexbox Intermediário** foi concluído após passar por:

```text
Teoria
↓
Exercícios
↓
Prática
↓
Desafios
↓
Consolidação
↓
DevTools
↓
Debugging
↓
Avaliação
```

A etapa não foi considerada concluída apenas por conhecer as propriedades.

Foi necessário demonstrar compreensão do comportamento dos itens, realizar cálculos, analisar problemas, utilizar o DevTools e explicar as causas encontradas.

### Status final

```text
CSS — Flexbox Intermediário
🟢 CONCLUÍDO
```

**Próxima etapa:** seguir o Roadmap Full Stack 2.4 sem repetir o conteúdo já dominado nesta etapa.
