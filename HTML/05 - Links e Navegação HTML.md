# Links e Navegação HTML

## O que são Links?

Links são elementos que permitem navegar de uma página para outra ou acessar outros lugares.

Na internet, os links são responsáveis pela conexão entre páginas.

A tag usada para criar links é:

```html
<a>
```

---

# Tag de Link

A estrutura básica:

```html
<a href="endereco">
Texto do link
</a>
```

Explicação:

```html
<a>
```

É a tag de link.

```html
href
```

É o atributo que informa o destino do link.

```html
Texto do link
```

É o que o usuário vê e pode clicar.

---

# Exemplo

```html
<a href="https://www.google.com">
Pesquisar no Google
</a>
```

Resultado:

O usuário verá:

Pesquisar no Google

Ao clicar, será levado para o Google.

---

# Links para páginas do próprio site

Um site normalmente possui várias páginas.

Exemplo:

```text
site/

index.html

sobre.html

contato.html
```

Para conectar essas páginas:

```html
<a href="sobre.html">
Sobre nós
</a>
```

Ao clicar, abre a página:

```
sobre.html
```

---

# Link abrindo em nova aba

Usamos o atributo:

```html
target
```

Exemplo:

```html
<a 
href="https://www.google.com"
target="_blank">

Google

</a>
```

Explicação:

```html
target="_blank"
```

Faz o link abrir uma nova aba do navegador.

---

# Link de Email

Podemos criar um link para enviar email.

Exemplo:

```html
<a href="mailto:exemplo@email.com">
Enviar email
</a>
```

Ao clicar, abre o programa de email.

---

# Link dentro de uma imagem

Também podemos transformar uma imagem em link.

Exemplo:

```html
<a href="https://google.com">

<img src="google.png">

</a>
```

Agora ao clicar na imagem, o usuário será direcionado.

---

# Exemplo de Menu de Navegação

Um site normalmente possui um menu.

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

Resultado:

```
Home | Serviços | Contato
```

---

# Como lembrar

A tag:

```html
<a>
```

vem de:

**Anchor**

Significa âncora.

Ela cria uma ligação entre lugares.

---

# Erros comuns

❌ Esquecer o atributo `href`.

Errado:

```html
<a>
Google
</a>
```

Correto:

```html
<a href="https://google.com">
Google
</a>
```

---

❌ Colocar o endereço errado.

Exemplo:

```html
<a href="google">
```

O navegador não sabe para onde ir.

---

# Resumo rápido

Links conectam páginas e conteúdos.

A tag principal é:

```html
<a>
```

Principais atributos:

- `href` → destino do link.
- `target="_blank"` → abre nova aba.
- `mailto:` → abre email.

---

## Próximo assunto

06 - Imagens HTML
