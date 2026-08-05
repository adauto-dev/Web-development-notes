# Estrutura Semântica HTML

## O que é HTML Semântico?

HTML semântico significa usar tags que possuem um significado claro sobre o conteúdo da página.

Em vez de usar apenas `<div>` para tudo, usamos elementos que explicam a função de cada parte.

Isso ajuda:

- O navegador a entender melhor a página.
- Motores de busca (SEO).
- Acessibilidade.
- Organização do código.

---

# Estrutura de uma página moderna

Uma página normalmente possui:

```html
<header>
<nav>
<main>
<section>
<footer>
```

---

# Tag `<header>`

Representa o cabeçalho da página.

Normalmente contém:

- Logo.
- Nome do site.
- Introdução.
- Menu.

Exemplo:

```html
<header>

<h1>
Minha Barbearia
</h1>

</header>
```

---

# Tag `<nav>`

Representa uma área de navegação.

Normalmente contém links do menu.

Exemplo:

```html
<nav>

<a href="index.html">
Home
</a>

<a href="servicos.html">
Serviços
</a>

<a href="contato.html">
Contato
</a>

</nav>
```

---

# Tag `<main>`

Representa o conteúdo principal da página.

Deve conter a parte mais importante do site.

Exemplo:

```html
<main>

<h1>
Serviços
</h1>

<p>
Conheça nossos serviços.
</p>

</main>
```

---

# Tag `<section>`

Cria uma seção dentro da página.

Usamos para separar conteúdos relacionados.

Exemplo:

```html
<section>

<h2>
Nossos serviços
</h2>

<p>
Corte e barba.
</p>

</section>
```

Uma página pode ter várias sections.

---

# Tag `<article>`

Representa um conteúdo independente.

Exemplos:

- Artigo de blog.
- Notícia.
- Avaliação de cliente.

Exemplo:

```html
<article>

<h2>
Avaliação do cliente
</h2>

<p>
Excelente atendimento.
</p>

</article>
```

---

# Tag `<footer>`

Representa o rodapé da página.

Normalmente contém:

- Direitos autorais.
- Contatos.
- Links importantes.

Exemplo:

```html
<footer>

<p>
© 2026 Minha Barbearia
</p>

</footer>
```

---

# Exemplo completo de uma página

```html
<!DOCTYPE html>

<html>

<head>

<title>
Barbearia
</title>

</head>


<body>


<header>

<h1>
Barbearia Premium
</h1>

</header>


<nav>

<a href="#">
Home
</a>

<a href="#">
Serviços
</a>

<a href="#">
Contato
</a>

</nav>


<main>


<section>

<h2>
Serviços
</h2>

<p>
Corte, barba e tratamento.
</p>

</section>


<section>

<h2>
Sobre nós
</h2>

<p>
Experiência e qualidade.
</p>

</section>


</main>


<footer>

<p>
© 2026 Barbearia
</p>

</footer>


</body>

</html>
```

---

# HTML semântico x div

## Div

```html
<div>
Conteúdo
</div>
```

É uma caixa genérica.

Não informa o significado do conteúdo.

---

## Semântico

```html
<section>
Serviços
</section>
```

Mostra que aquele conteúdo é uma seção.

---

# Como lembrar

Pense em uma página como um jornal:

```
<header
Título do jornal

<nav
Menu

<main
Notícia principal

<section
Categorias

<footer
Informações finais
```

---

# Erros comuns

❌ Usar somente `<div>` para tudo.

❌ Colocar vários `<main>` na mesma página.

Normalmente uma página possui apenas um:

```html
<main>
```

---

# Resumo rápido

HTML semântico organiza a página usando tags com significado.

Principais tags:

- `<header>` → cabeçalho.
- `<nav>` → menu.
- `<main>` → conteúdo principal.
- `<section>` → seção.
- `<article>` → conteúdo independente.
- `<footer>` → rodapé.

---

## Próximo assunto

11 - Div e Span HTML
