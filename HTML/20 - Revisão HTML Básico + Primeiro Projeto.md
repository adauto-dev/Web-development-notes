# Revisão HTML Básico + Primeiro Projeto

## O que aprendemos em HTML?

HTML significa:

**HyperText Markup Language**

É a linguagem usada para criar a estrutura de uma página web.

HTML não é responsável pelo design.

Ele cria a estrutura.

Exemplo:

```text
HTML → Estrutura
CSS → Aparência
JavaScript → Interação
```

---

# Estrutura básica de uma página

Todo documento HTML começa com:

```html
<!DOCTYPE html>
```

Depois:

```html
<html>

<head>

</head>


<body>

</body>

</html>
```

---

# Head

O `<head>` guarda informações da página.

Exemplos:

```html
<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>
Meu Site
</title>
```

---

# Body

O `<body>` contém tudo que aparece para o usuário.

Exemplo:

```html
<h1>
Título
</h1>

<p>
Texto
</p>
```

---

# Principais tags aprendidas

## Títulos

```html
<h1>
<h2>
<h3>
```

Usados para organizar títulos.

---

## Texto

```html
<p>
```

Cria parágrafos.

---

## Links

```html
<a href="pagina.html">
Clique aqui
</a>
```

Cria navegação entre páginas.

---

## Imagens

```html
<img 
src="imagem.jpg"
alt="Descrição">
```

Mostra imagens.

---

## Listas

Lista sem ordem:

```html
<ul>

<li>
Item
</li>

</ul>
```

Lista ordenada:

```html
<ol>

<li>
Primeiro
</li>

</ol>
```

---

## Formulários

Recebem informações:

```html
<form>

<input>

<button>

</form>
```

Usados para:

- Login.
- Cadastro.
- Agendamento.

---

## Tabelas

Organizam dados:

```html
<table>

<tr>

<td>
Dados
</td>

</tr>

</table>
```

---

## Estrutura semântica

HTML5 usa:

```html
<header>

<nav>

<main>

<section>

<footer>
```

Para organizar melhor a página.

---

# Div e Span

## Div

Agrupa blocos:

```html
<div>

Conteúdo

</div>
```

---

## Span

Modifica pequenas partes do texto:

```html
<span>
Texto
</span>
```

---

# Caminhos de arquivos

Mesma pasta:

```html
<img src="foto.jpg">
```

Dentro de pasta:

```html
<img src="images/foto.jpg">
```

Voltar pasta:

```html
../
```

---

# Acessibilidade

Criar sites para todos.

Exemplo:

```html
<img 
src="logo.png"
alt="Logo da empresa">
```

---

# Organização profissional

Estrutura:

```
meu-site/

index.html

css/

style.css

js/

script.js

images/

```

---

# Primeiro Projeto HTML

## Projeto:

# Site de uma Barbearia

Objetivo:

Criar uma página usando somente HTML.

---

## Estrutura:

O site terá:

```
Header

Menu

Apresentação

Serviços

Galeria

Contato

Footer
```

---

## Código inicial:

```html
<!DOCTYPE html>

<html lang="pt-BR">


<head>

<meta charset="UTF-8">

<meta name="viewport" 
content="width=device-width, initial-scale=1.0">


<title>
Barbearia Premium
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
Sobre nós
</h2>

<p>
Cortes modernos e atendimento profissional.
</p>

</section>


<section>

<h2>
Serviços
</h2>


<ul>

<li>
Corte masculino
</li>

<li>
Barba
</li>

<li>
Tratamento capilar
</li>

</ul>


</section>


<section>

<h2>
Contato
</h2>


<form>

<label>
Nome:
</label>

<input type="text">


<label>
Email:
</label>

<input type="email">


<button>
Enviar
</button>


</form>


</section>


</main>


<footer>

<p>
© 2026 Barbearia Premium
</p>

</footer>


</body>

</html>
```

---

# O que esse projeto usa?

✅ Estrutura HTML5

✅ Títulos

✅ Parágrafos

✅ Links

✅ Listas

✅ Formulário

✅ Tags semânticas

✅ Organização profissional

---

# Próximos passos

Depois desse projeto:

1. Criar uma versão com CSS.
2. Adicionar imagens.
3. Melhorar o design.
4. Adicionar JavaScript.
5. Transformar em um projeto real.

---

# Fim do HTML Básico

Agora você já entende a estrutura de uma página web.

Próxima etapa:

HTML Médio

Conteúdos:

- SEO.
- Acessibilidade avançada.
- Formulários profissionais.
- Boas práticas avançadas.
- Preparação para projetos reais.
