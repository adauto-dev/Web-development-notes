# Acessibilidade HTML Avançada

## O que é Acessibilidade?

Acessibilidade significa criar sites que podem ser usados pelo maior número de pessoas possível.

Um site acessível considera usuários que podem ter:

- Dificuldade de visão.
- Dificuldade de audição.
- Dificuldade de movimentação.
- Uso de leitores de tela.

Um bom desenvolvedor cria experiências para todos.

---

# Por que acessibilidade é importante?

Um site acessível:

- Melhora a experiência do usuário.
- Ajuda pessoas com necessidades diferentes.
- Pode melhorar o SEO.
- Mostra profissionalismo.

---

# 1. HTML Semântico

A primeira regra de acessibilidade é usar HTML com significado.

Exemplo ruim:

```html
<div>
Menu
</div>

<div>
Conteúdo
</div>
```

O navegador não sabe o significado.

---

Melhor:

```html
<nav>
Menu
</nav>


<main>
Conteúdo
</main>
```

Agora o navegador entende a função de cada parte.

---

# 2. Texto alternativo em imagens

Sempre use:

```html
alt
```

Exemplo:

```html
<img 
src="barbeiro.jpg"
alt="Barbeiro cortando cabelo de um cliente">
```

O leitor de tela pode descrever a imagem.

---

# 3. Formulários acessíveis

Um formulário deve explicar cada campo.

Errado:

```html
<input type="text">
```

O usuário não sabe o que escrever.

---

Correto:

```html
<label for="nome">
Nome:
</label>


<input 
id="nome"
type="text">
```

O `label` explica o campo.

---

# Atributo for e id

Eles conectam o texto ao campo.

Exemplo:

```html
<label for="email">
Email
</label>


<input 
id="email"
type="email">
```

Quando o usuário clica em "Email", o campo é selecionado.

---

# 4. Navegação pelo teclado

Algumas pessoas usam apenas o teclado.

O site deve permitir:

- Tab para navegar.
- Enter para selecionar.

Exemplo:

Links e botões HTML já possuem suporte:

```html
<a href="servicos.html">
Serviços
</a>


<button>
Enviar
</button>
```

---

# 5. Atributo ARIA

ARIA significa:

**Accessible Rich Internet Applications**

São atributos que dão informações extras para tecnologias assistivas.

Exemplo:

```html
<button aria-label="Fechar menu">

X

</button>
```

O leitor de tela entende:

"Fechar menu"

---

# 6. Roles

Role informa o papel de um elemento.

Exemplo:

```html
<div role="navigation">

Menu

</div>
```

Mas normalmente devemos preferir HTML semântico:

Melhor:

```html
<nav>

Menu

</nav>
```

---

# 7. Estados com ARIA

Exemplo de menu aberto ou fechado:

```html
<button aria-expanded="false">

Menu

</button>
```

O navegador entende o estado do botão.

---

# 8. Contraste de cores

O texto precisa ser fácil de ler.

Ruim:

```
Texto cinza claro
em fundo branco
```

Melhor:

```
Texto escuro
em fundo claro
```

Isso será mais trabalhado no CSS.

---

# 9. Vídeos acessíveis

Vídeos podem precisar de legendas.

Exemplo:

```html
<video controls>

<track 
src="legenda.vtt"
kind="subtitles">

</video>
```

Ajuda usuários com dificuldade de audição.

---

# Exemplo completo acessível

```html
<!DOCTYPE html>

<html lang="pt-BR">


<head>

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

<a href="servicos.html">
Serviços
</a>

</nav>


<main>


<section>

<h2>
Agendamento
</h2>


<form>


<label for="nome">
Nome:
</label>


<input 
id="nome"
type="text">


<label for="email">
Email:
</label>


<input
id="email"
type="email">


<button>
Enviar
</button>


</form>


</section>


</main>


</body>

</html>
```

---

# Erros comuns

❌ Usar imagens sem `alt`.

❌ Criar botões usando apenas div.

Errado:

```html
<div>
Enviar
</div>
```

Melhor:

```html
<button>
Enviar
</button>
```

---

❌ Usar ARIA quando HTML semântico já resolve.

Exemplo:

Não precisa:

```html
<div role="button">
```

Use:

```html
<button>
```

---

# Resumo rápido

Acessibilidade melhora o uso do site para todos.

Principais práticas:

✅ HTML semântico.

✅ Imagens com `alt`.

✅ Formulários com `label`.

✅ Navegação por teclado.

✅ Usar ARIA quando necessário.

✅ Criar textos claros.

---

## Próximo assunto

03 - Formulários HTML Profissionais
