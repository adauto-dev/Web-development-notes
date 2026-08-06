# Atributos HTML

## O que são Atributos?

Atributos são informações extras adicionadas dentro das tags HTML.

Eles servem para modificar ou dar mais informações sobre um elemento.

Os atributos aparecem dentro da tag de abertura.

---

## Estrutura de um Atributo

Exemplo:

```html
<tag atributo="valor">
```

Explicação:

```html
atributo
```

É a informação extra que queremos adicionar.

```html
valor
```

É o valor dessa informação.

---

# Exemplos de Atributos

## Atributo href

Usado principalmente na tag de link `<a>`.

Ele informa o endereço para onde o link deve levar.

Exemplo:

```html
<a href="https://www.google.com">
Abrir Google
</a>
```

Explicação:

```html
href
```

Significa **Hypertext Reference**.

Ele guarda o endereço do link.

---

## Atributo src

Usado na tag de imagem `<img>`.

Ele informa o local da imagem.

Exemplo:

```html
<img src="imagem.jpg">
```

Explicação:

```html
src
```

Significa **source** (origem).

Ele indica de onde o navegador deve buscar a imagem.

---

## Atributo alt

Também usado em imagens.

Ele descreve a imagem.

Exemplo:

```html
<img src="barbearia.jpg" alt="Interior de uma barbearia">
```

Por que usar?

- Ajuda pessoas que usam leitores de tela.
- Aparece se a imagem não carregar.
- Melhora a acessibilidade.

---

## Atributo class

Usado principalmente com CSS e JavaScript.

Ele permite identificar elementos.

Exemplo:

```html
<button class="botao-agendar">
Agendar
</button>
```

Depois podemos usar essa classe no CSS:

```css
.botao-agendar {
  background: black;
}
```

---

## Atributo id

Identifica um elemento único.

Exemplo:

```html
<h1 id="titulo">
Minha página
</h1>
```

Um `id` normalmente deve ser usado apenas uma vez na página.

---

# Exemplo completo

```html
<!DOCTYPE html>

<html>

<body>

<h1 id="titulo">
Minha Barbearia
</h1>

<p class="descricao">
Agende seu horário online.
</p>

<a href="https://google.com">
Localização
</a>

<img 
src="barbearia.jpg" 
alt="Foto da barbearia">

<button class="botao">
Agendar
</button>

</body>

</html>
```

---

# Diferença entre Tag e Atributo

Tag:

Define o elemento.

Exemplo:

```html
<img>
```

Significa:

"Existe uma imagem."

---

Atributo:

Adiciona uma informação.

Exemplo:

```html
<img src="foto.jpg">
```

Significa:

"A imagem está neste local."

---

# Erros comuns

❌ Colocar atributo fora da tag.

Errado:

```html
<img> src="foto.jpg"
```

Correto:

```html
<img src="foto.jpg">
```

---

❌ Esquecer as aspas.

Errado:

```html
<a href=https://google.com>
```

Correto:

```html
<a href="https://google.com">
```

---

# Resumo rápido

Atributos adicionam informações extras às tags.

Principais atributos:

- `href` → endereço de links.
- `src` → origem de imagens.
- `alt` → descrição de imagens.
- `class` → identifica grupos de elementos.
- `id` → identifica um elemento único.

---

## Próximo assunto

05 - Links e Navegação HTML
