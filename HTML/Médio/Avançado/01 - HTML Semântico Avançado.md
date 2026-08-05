# HTML Semântico Avançado

## O que é HTML Semântico?

HTML semântico significa usar tags que possuem significado.

O objetivo é que o navegador, buscadores e tecnologias assistivas entendam melhor a estrutura da página.

Exemplo:

```html
<div>
Meu conteúdo
</div>
```

O elemento funciona, mas não informa o significado.

Melhor:

```html
<section>
Meu conteúdo
</section>
```

Agora existe um significado.

---

# Por que HTML semântico é importante?

Um HTML bem estruturado ajuda:

- SEO.
- Acessibilidade.
- Organização do código.
- Manutenção do projeto.

Mesmo usando React ou outros frameworks, o conceito continua sendo importante.

---

# Principais elementos semânticos

## header

Representa o cabeçalho de uma página ou seção.

Exemplo:

```html
<header>

<h1>
Minha Empresa
</h1>

</header>
```

Pode conter:

- Logo.
- Título.
- Menu.

---

## nav

Representa uma área de navegação.

Exemplo:

```html
<nav>

<a href="/">
Home
</a>

<a href="/servicos">
Serviços
</a>

</nav>
```

Usado para menus principais.

---

## main

Representa o conteúdo principal da página.

Exemplo:

```html
<main>

<h1>
Serviços
</h1>

</main>
```

Uma página normalmente possui apenas um elemento `main`.

---

## section

Representa uma seção de conteúdo.

Exemplo:

```html
<section>

<h2>
Nossos serviços
</h2>

<p>
Descrição dos serviços.
</p>

</section>
```

Cada seção deve ter um objetivo.

---

## article

Representa um conteúdo independente.

Exemplos:

- Notícias.
- Posts.
- Produtos.
- Avaliações.

Exemplo:

```html
<article>

<h2>
Título do artigo
</h2>

<p>
Texto do artigo.
</p>

</article>
```

---

## aside

Representa conteúdo relacionado, mas não principal.

Exemplo:

```html
<aside>

<h3>
Promoção
</h3>

<p>
20% de desconto.
</p>

</aside>
```

Pode ser usado para:

- Barras laterais.
- Informações extras.

---

## footer

Representa o rodapé.

Exemplo:

```html
<footer>

<p>
© 2026 Empresa
</p>

</footer>
```

Pode conter:

- Direitos autorais.
- Links.
- Contatos.

---

# Diferença entre section e article

## Section

Grupo de conteúdo relacionado.

Exemplo:

```html
<section>

<h2>
Serviços
</h2>

</section>
```

---

## Article

Conteúdo que poderia existir sozinho.

Exemplo:

```html
<article>

<h2>
Avaliação de cliente
</h2>

</article>
```

---

# Exemplo de estrutura profissional

```html
<body>


<header>

Logo

</header>


<nav>

Menu

</nav>


<main>


<section>

<h2>
Serviços
</h2>


<article>

<h3>
Corte masculino
</h3>

<p>
Descrição.
</p>

</article>


</section>


</main>


<aside>

Promoção

</aside>


<footer>

Contato

</footer>


</body>
```

---

# Div ainda existe?

Sim.

A tag:

```html
<div>
```

continua sendo usada.

Ela é um elemento genérico.

Usamos quando não existe uma tag semântica adequada.

Exemplo:

```html
<div class="card">

Conteúdo visual

</div>
```

---

# Erros comuns

❌ Usar div para tudo.

Exemplo:

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

Melhor:

```html
<header>

</header>


<nav>

</nav>


<main>

</main>
```

---

# Resumo rápido

HTML semântico usa tags com significado.

Principais:

- `header` → cabeçalho.
- `nav` → navegação.
- `main` → conteúdo principal.
- `section` → seção.
- `article` → conteúdo independente.
- `aside` → conteúdo complementar.
- `footer` → rodapé.

---

# Importância profissional

Um bom HTML é a base para:

- Sites profissionais.
- SEO.
- Acessibilidade.
- React.
- Next.js.
- Aplicações SaaS.

---

## Próximo assunto

02 - SEO Técnico com HTML
