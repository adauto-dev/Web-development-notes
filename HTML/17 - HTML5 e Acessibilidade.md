# HTML5 e Acessibilidade

## O que é HTML5?

HTML5 é a versão moderna do HTML.

Ele trouxe novas funcionalidades e elementos para criar páginas mais organizadas, rápidas e acessíveis.

Com HTML5 podemos criar:

- Estruturas semânticas.
- Áudio e vídeo.
- Formulários melhores.
- Aplicações web modernas.

---

# Diferença entre HTML antigo e HTML5

Antes:

```html
<div>
Cabeçalho
</div>

<div>
Menu
</div>

<div>
Conteúdo
</div>
```

O navegador via apenas caixas.

---

HTML5:

```html
<header>
Cabeçalho
</header>

<nav>
Menu
</nav>

<main>
Conteúdo
</main>
```

Agora cada parte possui um significado.

---

# O que é Acessibilidade?

Acessibilidade significa criar sites que possam ser usados por todas as pessoas.

Incluindo pessoas com:

- Dificuldade de visão.
- Dificuldade de audição.
- Dificuldade de movimentação.
- Uso de leitores de tela.

Um bom site deve ser fácil de usar para todos.

---

# Importância do atributo alt

Em imagens usamos:

```html
<img src="foto.jpg" alt="Descrição da imagem">
```

O atributo `alt` ajuda pessoas que usam leitores de tela.

Exemplo:

```html
<img 
src="barbearia.jpg"
alt="Interior moderno de uma barbearia">
```

O leitor de tela pode informar:

"Interior moderno de uma barbearia"

---

# Usar títulos corretamente

Os títulos devem seguir uma ordem.

Correto:

```html
<h1>
Barbearia Premium
</h1>

<h2>
Serviços
</h2>

<h3>
Corte masculino
</h3>
```

O `h1` representa o título principal.

Depois usamos:

```
h2
h3
h4
```

para organizar o conteúdo.

---

# Usar labels em formulários

Errado:

```html
<input type="email">
```

O usuário pode não saber o que colocar.

Melhor:

```html
<label>
Email:
</label>

<input type="email">
```

O label ajuda usuários e leitores de tela.

---

# Botões e links claros

Evite:

```html
<a href="#">
Clique aqui
</a>
```

Melhor:

```html
<a href="servicos.html">
Ver nossos serviços
</a>
```

O usuário entende para onde vai.

---

# Idioma da página

Devemos informar o idioma do site.

Exemplo:

Português:

```html
<html lang="pt-BR">
```

Inglês:

```html
<html lang="en">
```

Isso ajuda navegadores e leitores de tela.

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
Nossos serviços
</h2>


<img
src="corte.jpg"
alt="Cliente fazendo corte de cabelo">


<p>
Cortes profissionais.
</p>


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

# Boas práticas

Sempre:

✅ Usar HTML semântico.

✅ Colocar `alt` nas imagens.

✅ Usar títulos na ordem correta.

✅ Usar labels nos formulários.

✅ Informar o idioma da página.

---

# Erros comuns

❌ Usar imagens sem descrição:

```html
<img src="foto.jpg">
```

Melhor:

```html
<img src="foto.jpg" alt="Descrição">
```

---

❌ Pular níveis de títulos.

Evite:

```html
<h1>
Título
</h1>

<h4>
Subtítulo
</h4>
```

Use a sequência correta.

---

# Resumo rápido

HTML5 trouxe uma estrutura mais moderna.

Acessibilidade significa criar sites que todos conseguem usar.

Principais cuidados:

- `alt` nas imagens.
- `label` nos formulários.
- Títulos organizados.
- HTML semântico.
- Idioma correto.

---

## Próximo assunto

18 - Estrutura de um Projeto HTML Profissional
