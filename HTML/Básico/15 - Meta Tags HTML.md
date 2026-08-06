# Meta Tags HTML

## O que são Meta Tags?

Meta Tags são informações sobre a página que ficam dentro da tag:

```html
<head>
</head>
```

Elas não aparecem diretamente para o usuário na página.

Elas ajudam:

- O navegador a entender o documento.
- Os buscadores (SEO).
- A página funcionar corretamente em diferentes dispositivos.

---

# Estrutura básica

As meta tags ficam dentro do:

```html
<head>

</head>
```

Exemplo:

```html
<head>

<meta charset="UTF-8">

</head>
```

---

# Meta charset

Define a codificação dos caracteres da página.

A mais usada atualmente é:

```html
<meta charset="UTF-8">
```

Ela permite mostrar corretamente:

- Acentos.
- Símbolos.
- Diferentes idiomas.

Exemplo:

Sem UTF-8:

```
Olá
```

Pode aparecer errado:

```
OlÃ¡
```

---

# Meta viewport

Muito importante para celulares.

Código:

```html
<meta 
name="viewport" 
content="width=device-width, initial-scale=1.0">
```

Explicação:

## width=device-width

Faz a página usar a largura do dispositivo.

Exemplo:

- Computador.
- Tablet.
- Celular.

---

## initial-scale=1.0

Define o zoom inicial da página.

---

# Por que viewport é importante?

Sem essa meta tag, um site pode ficar errado no celular.

Exemplo:

Computador:

```
-------------------
|                 |
|      Site       |
|                 |
-------------------
```

Celular sem viewport:

```
-------------------
| Site pequeno    |
-------------------
```

Com viewport:

```
---------
| Site |
---------
```

A página se adapta.

---

# Meta description

Usada para descrever a página nos buscadores.

Exemplo:

```html
<meta 
name="description"
content="Barbearia moderna com cortes e serviços profissionais">
```

Ajuda no SEO.

---

# Meta keywords

Antigamente era usada para palavras-chave.

Exemplo:

```html
<meta 
name="keywords"
content="barbearia, corte, barba">
```

Hoje os buscadores modernos não dão muita importância para ela.

---

# Título da página

Não é uma meta tag, mas fica dentro do `<head>`.

Usamos:

```html
<title>
</title>
```

Exemplo:

```html
<title>
Minha Barbearia
</title>
```

Aparece na aba do navegador.

---

# Exemplo completo do Head

```html
<head>

<meta charset="UTF-8">


<meta 
name="viewport" 
content="width=device-width, initial-scale=1.0">


<meta 
name="description"
content="Serviços de barbearia profissional">


<title>
Barbearia Premium
</title>


</head>
```

---

# Como lembrar

O:

```html
<head>
```

é como o cérebro da página.

Ele guarda informações que ajudam o navegador.

O:

```html
<body>
```

é o corpo.

Ele mostra o conteúdo para o usuário.

---

# Erros comuns

❌ Esquecer o viewport.

Principalmente em sites para celular.

---

❌ Colocar meta tags dentro do body.

Errado:

```html
<body>

<meta charset="UTF-8">

</body>
```

Correto:

```html
<head>

<meta charset="UTF-8">

</head>
```

---

# Resumo rápido

Meta Tags ficam no:

```html
<head>
```

Principais:

- `charset="UTF-8"` → caracteres.
- `viewport` → adaptação para celulares.
- `description` → descrição para buscadores.
- `<title>` → título da página.

---

## Próximo assunto

16 - Caminhos de Arquivos HTML (Paths)
