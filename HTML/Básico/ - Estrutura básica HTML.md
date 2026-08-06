

# Estrutura básica HTML

## O que é?

Todo documento HTML possui uma estrutura padrão.

Essa estrutura ajuda o navegador a entender como a página deve ser interpretada.

Todo site começa com essa base.

---

## Estrutura básica

```html
<!DOCTYPE html>

<html>

<head>

</head>

<body>

</body>

</html>
```

---

## Explicação da estrutura

### `<!DOCTYPE html>`

Informa ao navegador que estamos usando **HTML5**.

Deve sempre ser a primeira linha do documento.

Exemplo:

```html
<!DOCTYPE html>
```

---

### `<html>`

É o elemento principal da página.

Todo o código HTML fica dentro dele.

Exemplo:

```html
<html>

  Todo o conteúdo da página fica aqui.

</html>
```

---

### `<head>`

Guarda informações sobre a página.

Essas informações normalmente não aparecem para o usuário.

Pode conter:

- título da página;
- configurações;
- arquivos CSS.

Exemplo:

```html
<head>

<title>Meu site</title>

</head>
```

O texto "Meu site" aparece na aba do navegador.

---

### `<body>`

É onde fica tudo que o usuário vê na tela.

Exemplos:

- textos;
- imagens;
- botões;
- links.

Exemplo:

```html
<body>

<h1>Minha página</h1>

<p>Aprendendo HTML.</p>

</body>
```

Resultado:

A página mostra:

# Minha página

Aprendendo HTML.

---

# Exemplo completo

```html
<!DOCTYPE html>

<html>

<head>

<title>Meu primeiro site</title>

</head>

<body>

<h1>Olá mundo</h1>

<p>Estou aprendendo HTML.</p>

</body>

</html>
```

---

## Como o navegador interpreta

O navegador lê nessa ordem:

1. Encontra o documento HTML.

2. Lê a estrutura principal.

3. Encontra o `head` com informações da página.

4. Encontra o `body` com o conteúdo visível.

5. Mostra a página para o usuário.

---

## Erros comuns

❌ Esquecer o `<!DOCTYPE html>`

❌ Colocar conteúdo fora do `<html>`

❌ Colocar textos dentro do `head` achando que vão aparecer na página.

❌ Esquecer de fechar uma tag.

Errado:

```html
<p>Olá mundo
```

Correto:

```html
<p>Olá mundo</p>
```

---

## Resumo rápido

HTML possui uma estrutura padrão:

```
DOCTYPE
   ↓
HTML
   ↓
HEAD
   ↓
BODY
```

`head` = informações da página.

`body` = conteúdo que aparece para o usuário.

---

