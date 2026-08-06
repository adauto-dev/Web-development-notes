# Tags HTML

## O que são Tags?

Tags são elementos usados pelo HTML para criar e organizar o conteúdo de uma página.

Elas informam ao navegador o que cada parte da página representa.

Exemplos:

- título;
- parágrafo;
- imagem;
- link;
- botão.

---

## Estrutura de uma Tag

A maioria das tags possui:

- Tag de abertura.
- Conteúdo.
- Tag de fechamento.

Exemplo:

```html
<p>Meu primeiro texto</p>
```

Explicação:

```html
<p>
```

Tag de abertura.

```html
Meu primeiro texto
```

Conteúdo.

```html
</p>
```

Tag de fechamento.

---

# Tags mais usadas

## Títulos

HTML possui títulos de diferentes tamanhos.

Do maior para o menor:

```html
<h1>Título principal</h1>

<h2>Subtítulo</h2>

<h3>Título menor</h3>
```

Exemplo:

```html
<h1>Minha Barbearia</h1>

<h2>Serviços</h2>
```

Resultado:

Um título principal e um subtítulo aparecem na página.

---

## Parágrafo

A tag `<p>` cria textos em parágrafos.

Exemplo:

```html
<p>
Bem-vindo ao meu site.
</p>
```

Usamos para textos comuns.

---

## Link

A tag `<a>` cria links.

Exemplo:

```html
<a href="https://www.google.com">
Abrir Google
</a>
```

Explicação:

`a` significa **anchor** (âncora).

`href` informa o endereço para onde o link vai.

---

## Imagem

A tag `<img>` mostra imagens.

Exemplo:

```html
<img src="foto.jpg">
```

Explicação:

`src` significa source (origem).

Ele indica o caminho da imagem.

---

## Botão

A tag `<button>` cria botões.

Exemplo:

```html
<button>
Agendar horário
</button>
```

Sozinho o botão não faz nada.

O JavaScript será usado depois para criar ações.

---

# Exemplo de uma página simples

```html
<!DOCTYPE html>

<html>

<head>

<title>Barbearia</title>

</head>

<body>

<h1>Barbearia Premium</h1>

<p>Agende seu horário online.</p>

<img src="barbearia.jpg">

<button>Agendar</button>

</body>

</html>
```

---

# Como lembrar

HTML é como uma caixa de ferramentas.

Cada tag tem uma função:

```
<h1>
Título

<p>
Texto

<a>
Link

<img>
Imagem

<button>
Botão
```

---

# Erros comuns

❌ Usar várias vezes o `<h1>` sem necessidade.

O ideal:

```html
<h1>
Título principal
</h1>
```

Depois:

```html
<h2>
Subtítulos
</h2>
```

---

❌ Esquecer de fechar tags.

Errado:

```html
<p>Texto
```

Correto:

```html
<p>Texto</p>
```

---

# Resumo rápido

Tags são elementos que informam ao navegador o que cada conteúdo representa.

As principais tags:

- `<h1>` → título
- `<p>` → parágrafo
- `<a>` → link
- `<img>` → imagem
- `<button>` → botão

---

## Próximo assunto

04 - Atributos HTML
