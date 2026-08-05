# SEO HTML

## O que é SEO?

SEO significa:

**Search Engine Optimization**

(otimização para motores de busca)

É o conjunto de técnicas para ajudar uma página a ser encontrada pelos buscadores.

Exemplo:

Quando alguém pesquisa:

```
barbearia perto de mim
```

O Google analisa várias informações para decidir quais páginas mostrar.

---

# Por que HTML é importante para SEO?

O HTML ajuda os buscadores a entender:

- Sobre o que é a página.
- Qual é o conteúdo principal.
- Quais informações são importantes.

Um HTML bem organizado melhora a comunicação com os buscadores.

---

# 1. Usar títulos corretamente

O título principal deve usar:

```html
<h1>
```

Exemplo:

```html
<h1>
Barbearia Premium em Antwerpen
</h1>
```

O `<h1>` deve representar o assunto principal da página.

Normalmente usamos apenas um `<h1>` por página.

---

# Hierarquia de títulos

Depois usamos:

```html
<h2>
<h3>
<h4>
```

Exemplo:

```html
<h1>
Serviços de Barbearia
</h1>


<h2>
Cortes
</h2>


<h3>
Corte masculino
</h3>
```

Isso cria uma organização para usuários e buscadores.

---

# 2. Title da página

O elemento:

```html
<title>
</title>
```

aparece na aba do navegador e ajuda no SEO.

Exemplo:

```html
<title>
Barbearia Premium | Cortes e Barba
</title>
```

Um bom título deve ser:

- Claro.
- Específico.
- Relacionado ao conteúdo.

---

# 3. Meta Description

A meta description é uma pequena descrição da página.

Exemplo:

```html
<meta 
name="description"
content="Barbearia profissional com cortes modernos, barba e agendamento online.">
```

Ela pode aparecer nos resultados de busca.

---

# 4. URLs amigáveis

Um endereço claro ajuda usuários e buscadores.

Ruim:

```
site.com/page?id=123
```

Melhor:

```
site.com/servicos-barbearia
```

---

# 5. Imagens com alt

Sempre descreva imagens.

Ruim:

```html
<img src="foto.jpg">
```

Melhor:

```html
<img 
src="foto.jpg"
alt="Barbeiro realizando corte masculino">
```

O buscador entende o conteúdo da imagem.

---

# 6. Links internos

Links entre páginas ajudam a navegação.

Exemplo:

```html
<a href="servicos.html">
Conheça nossos serviços
</a>
```

Isso ajuda:

- Usuários.
- Organização do site.
- SEO.

---

# 7. HTML Semântico e SEO

Usar:

```html
<header>

<nav>

<main>

<section>

<footer>
```

ajuda os buscadores a entenderem a estrutura.

Exemplo:

```html
<main>

<section>

<h2>
Nossos serviços
</h2>

<p>
Corte e barba profissional.
</p>

</section>

</main>
```

---

# 8. Mobile SEO

Sites precisam funcionar bem no celular.

Por isso usamos:

```html
<meta 
name="viewport"
content="width=device-width, initial-scale=1.0">
```

Um site que funciona bem no celular tem melhor experiência.

---

# Exemplo de página otimizada

```html
<!DOCTYPE html>

<html lang="pt-BR">


<head>


<meta charset="UTF-8">


<meta 
name="viewport"
content="width=device-width, initial-scale=1.0">


<title>
Barbearia Premium | Corte e Barba
</title>


<meta 
name="description"
content="Agende seu corte e barba em uma barbearia profissional.">


</head>


<body>


<header>

<h1>
Barbearia Premium
</h1>

</header>


<main>

<section>

<h2>
Serviços
</h2>

<p>
Cortes modernos e atendimento profissional.
</p>

</section>

</main>


</body>

</html>
```

---

# Erros comuns de SEO

❌ Usar vários `<h1>` sem necessidade.

❌ Colocar títulos que não têm relação com o conteúdo.

❌ Não usar `alt` nas imagens.

❌ Ignorar usuários de celular.

❌ Criar páginas sem estrutura.

---

# Resumo rápido

SEO ajuda uma página a ser encontrada.

Principais cuidados:

✅ Usar títulos corretamente.

✅ Criar bons `<title>`.

✅ Usar meta description.

✅ Usar imagens com `alt`.

✅ Criar URLs claras.

✅ Usar HTML semântico.

---

## Próximo assunto

02 - Acessibilidade HTML Avançada
