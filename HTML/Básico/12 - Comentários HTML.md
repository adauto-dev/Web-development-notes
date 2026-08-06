# Comentários HTML

## O que são Comentários?

Comentários são textos escritos dentro do código que não aparecem na página para o usuário.

Eles servem para:

- Explicar partes do código.
- Organizar arquivos grandes.
- Deixar lembretes para outros desenvolvedores.

O navegador ignora os comentários.

---

# Estrutura de um comentário HTML

Um comentário começa com:

```html
<!--
```

e termina com:

```html
-->
```

Exemplo:

```html
<!-- Este é um comentário -->
```

---

# Exemplo dentro de uma página

```html
<!DOCTYPE html>

<html>

<body>


<!-- Cabeçalho do site -->

<header>

<h1>
Minha Barbearia
</h1>

</header>


<!-- Lista de serviços -->

<section>

<h2>
Serviços
</h2>

<p>
Corte e barba.
</p>

</section>


</body>

</html>
```

Os comentários ajudam a identificar cada parte do código.

---

# Comentários em uma linha

Exemplo:

```html
<!-- Título principal -->

<h1>
Meu Site
</h1>
```

---

# Comentários em várias linhas

Também podemos escrever comentários maiores:

```html
<!--

Esta seção contém
os serviços da empresa.

-->

<section>

<h2>
Serviços
</h2>

</section>
```

---

# Quando usar comentários?

## Para organizar código grande

Exemplo:

```html
<!-- Menu de navegação -->

<nav>

</nav>


<!-- Conteúdo principal -->

<main>

</main>
```

---

## Para deixar explicações

Exemplo:

```html
<!--
Esta imagem representa
o logo da empresa
-->

<img src="logo.png">
```

---

# Quando NÃO usar?

Não coloque comentários explicando coisas óbvias.

Exemplo desnecessário:

```html
<!-- Criando um parágrafo -->

<p>
Olá
</p>
```

Qualquer programador já sabe que `<p>` cria um parágrafo.

---

# Comentários e segurança

Importante:

Comentários HTML ficam dentro do código da página.

Qualquer pessoa pode ver usando:

```
Botão direito → Ver código-fonte
```

Então nunca coloque:

❌ Senhas.

❌ Informações privadas.

❌ Chaves de API.

---

# Atalho no editor

No VS Code existe um atalho para comentar linhas:

Mac:

```
⌘ + /
```

Windows:

```
Ctrl + /
```

Ele adiciona ou remove comentários automaticamente.

---

# Exemplo profissional

```html
<!-- Header -->

<header>

<h1>
Empresa
</h1>

</header>


<!-- Main content -->

<main>

<section>

<h2>
Produtos
</h2>

</section>

</main>


<!-- Footer -->

<footer>

</footer>
```

---

# Resumo rápido

Comentários:

- Não aparecem na página.
- Ajudam a organizar o código.
- São usados como explicações e lembretes.

Sintaxe:

```html
<!-- comentário -->
```

Nunca coloque informações secretas dentro deles.

---

## Próximo assunto

13 - Entidades HTML
