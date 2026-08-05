# Div e Span HTML

## O que são Div e Span?

`div` e `span` são elementos usados para agrupar partes do HTML.

Eles não possuem significado próprio como:

```html
<header>
<section>
<footer>
```

Eles são usados principalmente para organização e aplicação de CSS e JavaScript.

---

# Tag `<div>`

`div` significa **division** (divisão).

É um elemento de bloco usado para agrupar vários elementos.

Exemplo:

```html
<div>

<h2>
Serviços
</h2>

<p>
Corte e barba.
</p>

</div>
```

A `div` cria uma caixa que contém:

- título;
- texto;
- outros elementos.

---

# Como a div funciona

Imagine uma caixa.

Dentro dela podemos colocar várias coisas:

```
<div>

   título

   texto

   imagem

   botão

</div>
```

Ela ajuda a organizar o código.

---

# Exemplo com uma página

```html
<div>

<h1>
Barbearia Premium
</h1>

<p>
Agende seu horário.
</p>

<button>
Agendar
</button>

</div>
```

Tudo está agrupado dentro da mesma caixa.

---

# Tag `<span>`

`span` é usado para pequenas partes de texto.

Ele é um elemento de linha.

Normalmente usamos para modificar uma palavra ou parte de uma frase.

Exemplo:

```html
<p>

Meu corte custa 

<span>
20€
</span>

</p>
```

O `span` permite estilizar apenas o valor.

---

# Diferença entre div e span

## div

Usado para grandes blocos.

Exemplo:

```html
<div>

<section>
Serviços
</section>

</div>
```

Pode conter vários elementos.

---

## span

Usado para pequenas partes dentro de um texto.

Exemplo:

```html
<p>

Preço:

<span>
20€
</span>

</p>
```

---

# Div com classe

A maior utilização da `div` é junto com CSS.

Exemplo:

HTML:

```html
<div class="card">

<h2>
Corte
</h2>

<p>
30 minutos
</p>

</div>
```

CSS:

```css
.card {

border: 1px solid black;

}
```

Agora podemos modificar essa caixa.

---

# Span com classe

Exemplo:

HTML:

```html
<p>

Preço:

<span class="preco">
20€
</span>

</p>
```

CSS:

```css
.preco {

color: red;

}
```

Somente o preço será alterado.

---

# Quando usar?

## Use div quando:

- Precisa agrupar elementos.
- Criar caixas.
- Organizar layouts.

Exemplo:

```html
<div class="produto">

imagem

título

preço

botão

</div>
```

---

## Use span quando:

- Precisa mudar uma parte pequena do texto.

Exemplo:

```html
<p>
Oferta de <span>50%</span>
</p>
```

---

# Div x HTML Semântico

Antes:

```html
<div>
Cabeçalho
</div>

<div>
Menu
</div>

<div>
Conteúdo
</div>
```

Hoje preferimos:

```html
<header>
Cabeçalho
</header>

<nav>
Menu
</nav>

<main>
Conteúdo
</main>
```

Porque possuem significado.

---

# Erros comuns

❌ Usar div para tudo sem necessidade.

Se existe uma tag semântica adequada, prefira ela.

Exemplo:

Melhor:

```html
<header>
</header>
```

Do que:

```html
<div>
Cabeçalho
</div>
```

---

❌ Usar span para criar grandes estruturas.

Span é para pequenas partes de texto.

---

# Resumo rápido

`div`:

- Agrupa blocos.
- Cria caixas.
- Muito usado com CSS.

`span`:

- Agrupa pequenas partes de texto.
- Muito usado para estilos específicos.

---

## Próximo assunto

12 - Comentários HTML
