# Imagens HTML

## O que são Imagens em HTML?

Imagens são elementos usados para adicionar conteúdo visual em uma página web.

A tag usada para adicionar imagens é:

```html
<img>
```

Diferente de outras tags, a tag `img` não precisa de fechamento.

Exemplo:

```html
<img src="foto.jpg">
```

---

# Estrutura da tag de imagem

Exemplo:

```html
<img src="imagem.jpg" alt="Descrição da imagem">
```

A tag possui principalmente dois atributos:

---

## Atributo src

`src` significa **source** (origem).

Ele informa ao navegador onde está localizada a imagem.

Exemplo:

```html
<img src="barbearia.jpg">
```

O navegador procura o arquivo:

```
barbearia.jpg
```

para mostrar na página.

---

## Atributo alt

`alt` significa **alternative text** (texto alternativo).

Ele descreve a imagem.

Exemplo:

```html
<img 
src="barbearia.jpg" 
alt="Interior de uma barbearia moderna">
```

Por que usar `alt`?

- Ajuda pessoas que usam leitores de tela.
- Aparece caso a imagem não carregue.
- Melhora a acessibilidade.

---

# Caminho das imagens

O caminho informa onde o arquivo está.

## Imagem na mesma pasta

Estrutura:

```
site/

index.html

foto.jpg
```

Código:

```html
<img src="foto.jpg">
```

---

## Imagem dentro de uma pasta

Estrutura:

```
site/

index.html

imagens/

foto.jpg
```

Código:

```html
<img src="imagens/foto.jpg">
```

---

# Tamanho da imagem

Podemos alterar o tamanho usando atributos:

```html
<img 
src="foto.jpg"
width="300"
height="200">
```

`width` = largura

`height` = altura

---

# Imagem como link

Podemos colocar uma imagem dentro de um link.

Exemplo:

```html
<a href="https://google.com">

<img src="google.png">

</a>
```

Agora a imagem pode ser clicada.

---

# Exemplo completo

```html
<!DOCTYPE html>

<html>

<head>

<title>Minha página</title>

</head>

<body>

<h1>
Minha Barbearia
</h1>

<img 
src="barbearia.jpg"
alt="Interior da barbearia">

<p>
Um ambiente moderno para seu corte.
</p>

</body>

</html>
```

---

# Como lembrar

Pense assim:

```text
<img>
   |
   |
src = onde está a imagem

alt = o que é a imagem
```

---

# Erros comuns

❌ Esquecer o `src`.

Errado:

```html
<img>
```

Correto:

```html
<img src="foto.jpg">
```

---

❌ Nome do arquivo diferente.

Arquivo:

```
Foto.jpg
```

Código:

```html
<img src="foto.jpg">
```

Pode não funcionar porque:

```
Foto.jpg ≠ foto.jpg
```

---

❌ Usar imagens muito pesadas.

Imagens grandes podem deixar o site lento.

---

# Resumo rápido

A tag de imagem é:

```html
<img>
```

Principais atributos:

- `src` → localização da imagem.
- `alt` → descrição da imagem.
- `width` → largura.
- `height` → altura.

---

## Próximo assunto

07 - Listas HTML
