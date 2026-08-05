# HTML Preparação para CSS

## Por que preparar o HTML para CSS?

HTML cria a estrutura da página.

CSS cria o visual:

- Cores.
- Espaçamentos.
- Tamanhos.
- Layout.
- Animações.

Para o CSS funcionar bem, o HTML precisa estar organizado.

---

# HTML e CSS trabalham juntos

Exemplo:

HTML:

```html
<h1>
Barbearia Premium
</h1>
```

CSS:

```css
h1 {

color: black;

}
```

O HTML cria o elemento.

O CSS modifica a aparência.

---

# Classes (class)

A classe é uma forma de identificar elementos.

Exemplo:

```html
<h1 class="titulo">

Barbearia Premium

</h1>
```

No CSS:

```css
.titulo {

font-size: 40px;

}
```

---

# Quando usar class?

Usamos `class` quando vários elementos podem ter o mesmo estilo.

Exemplo:

```html
<button class="botao">

Agendar

</button>


<button class="botao">

Comprar

</button>
```

CSS:

```css
.botao {

background: black;

}
```

Os dois botões recebem o mesmo estilo.

---

# IDs (id)

O ID identifica um elemento único.

Exemplo:

```html
<section id="contato">

Contato

</section>
```

CSS:

```css
#contato {

padding: 20px;

}
```

---

# Class x ID

## Class

Pode repetir:

```html
<div class="card">

</div>


<div class="card">

</div>
```

Usado para estilos gerais.

---

## ID

Deve ser único:

```html
<div id="menu">

</div>
```

Usado para elementos específicos.

---

# Nomes de classes profissionais

Evite:

```html
<div class="caixa1">
```

ou:

```html
<div class="azul">
```

Porque o nome fala da aparência.

---

Melhor:

```html
<div class="card-servico">
```

ou:

```html
<div class="lista-produtos">
```

O nome deve explicar a função.

---

# Estrutura preparada para CSS

Exemplo:

```html
<header class="header">

<h1 class="logo">

Minha Empresa

</h1>


<nav class="menu">

<a href="#">
Home
</a>

</nav>


</header>
```

Agora o CSS consegue controlar cada parte.

---

# Organização com containers

Usamos containers para organizar conteúdo.

Exemplo:

```html
<section class="servicos">


<div class="container">


<h2>
Serviços
</h2>


<p>
Nossos serviços profissionais.
</p>


</div>


</section>
```

---

# HTML semântico + classes

Exemplo profissional:

```html
<header class="header">


<nav class="navbar">

<a class="logo">
Logo
</a>


</nav>


</header>
```

Misturamos:

HTML semântico:

```
header
nav
section
footer
```

com:

Classes:

```
header
navbar
logo
```

---

# Preparando imagens

Imagem:

```html
<img 
class="imagem-produto"
src="produto.jpg"
alt="Produto">
```

CSS poderá controlar:

- Tamanho.
- Bordas.
- Posicionamento.

---

# Preparando botões

HTML:

```html
<button class="btn-primary">

Agendar agora

</button>
```

CSS:

```css
.btn-primary {

padding: 10px;

}
```

---

# Estrutura profissional de uma página

```html
<body>


<header class="header">

</header>


<main>


<section class="hero">

</section>


<section class="services">

</section>


<section class="contact">

</section>


</main>


<footer class="footer">

</footer>


</body>
```

---

# Boas práticas

✅ Use classes com nomes claros.

✅ Use HTML semântico.

✅ Pense na organização antes do CSS.

✅ Evite estilos direto no HTML.

---

# Evitar CSS dentro do HTML

Evite:

```html
<h1 style="color:red">

Título

</h1>
```

Melhor:

HTML:

```html
<h1 class="titulo">

Título

</h1>
```

CSS:

```css
.titulo {

color:red;

}
```

---

# Resumo rápido

Para preparar HTML para CSS:

- Use `class`.
- Use `id` quando necessário.
- Use nomes claros.
- Organize seções.
- Separe HTML e CSS.

---

# Próxima etapa

Agora o HTML está preparado para receber design.

Próximo passo:

## CSS - Fundamentos
