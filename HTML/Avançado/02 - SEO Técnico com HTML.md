# SEO Técnico com HTML

## O que é SEO Técnico?

SEO Técnico é a parte do SEO que trabalha a estrutura do site para facilitar que:

- Buscadores entendam a página.
- Usuários encontrem o conteúdo.
- Redes sociais mostrem informações corretas.

O HTML tem um papel importante nessa comunicação.

---

# 1. Title otimizado

O elemento:

```html
<title>
</title>
```

é uma das informações mais importantes da página.

Exemplo:

```html
<title>
Barbearia Premium | Corte e Barba em Antwerpen
</title>
```

Um bom título deve ser:

✅ Claro.

✅ Relacionado ao conteúdo.

✅ Ter palavras importantes.

---

# 2. Meta Description

A descrição aparece frequentemente nos resultados de busca.

Exemplo:

```html
<meta
name="description"
content="Barbearia profissional com cortes modernos, barba e agendamento online.">
```

Uma boa descrição:

- Explica o conteúdo.
- Incentiva o clique.
- Não deve ser enganosa.

---

# 3. Meta Robots

Controla como buscadores podem acessar uma página.

Exemplo:

```html
<meta
name="robots"
content="index, follow">
```

Significado:

```
index
→ permite aparecer nos resultados.

follow
→ permite seguir os links da página.
```

---

# 4. Canonical URL

Usado para informar qual é a versão principal de uma página.

Exemplo:

```html
<link
rel="canonical"
href="https://meusite.com/servicos">
```

Ajuda a evitar problemas de páginas duplicadas.

---

# 5. Open Graph

Open Graph controla como a página aparece quando compartilhada em redes sociais.

Exemplo:

```html
<meta
property="og:title"
content="Barbearia Premium">
```

---

Imagem compartilhada:

```html
<meta
property="og:image"
content="imagem.jpg">
```

---

Descrição:

```html
<meta
property="og:description"
content="Agende seu corte online.">
```

Quando alguém compartilha o link, essas informações podem aparecer.

---

# 6. Dados estruturados (Structured Data)

São informações extras para buscadores.

Usamos normalmente:

JSON-LD

Exemplo:

```html
<script type="application/ld+json">

{
 "@context": "https://schema.org",
 "@type": "LocalBusiness",
 "name": "Barbearia Premium"
}

</script>
```

Ajuda buscadores a entender:

- Empresa.
- Local.
- Serviços.
- Produtos.

---

# 7. Hierarquia correta de conteúdo

Buscadores analisam a organização.

Exemplo:

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

Não use títulos apenas pelo tamanho.

Use pelo significado.

---

# 8. URLs amigáveis

Uma URL boa:

```
site.com/agendamento
```

Uma URL ruim:

```
site.com/page?id=542
```

URLs claras ajudam usuários e buscadores.

---

# 9. Sitemap

O sitemap informa ao buscador quais páginas existem.

Exemplo:

```
sitemap.xml
```

Pode conter:

```
/
 /servicos
 /contato
 /sobre
```

Muito usado em sites maiores.

---

# 10. Favicon

É o pequeno ícone da página no navegador.

Exemplo:

```html
<link
rel="icon"
href="favicon.ico">
```

Melhora a identidade do site.

---

# Exemplo de Head otimizado

```html
<head>


<title>
ServiceFlow - Agendamento Online
</title>


<meta
charset="UTF-8">


<meta
name="viewport"
content="width=device-width, initial-scale=1.0">


<meta
name="description"
content="Sistema de agendamento online para empresas.">


<meta
name="robots"
content="index, follow">


<link
rel="icon"
href="favicon.ico">


</head>
```

---

# Erros comuns

❌ Repetir vários títulos iguais.

❌ Usar descrição que não tem relação com a página.

❌ Ignorar compartilhamento em redes sociais.

❌ Criar páginas duplicadas sem controle.

---

# Resumo rápido

SEO Técnico no HTML envolve:

- `<title>` → título da página.
- `description` → resumo.
- `robots` → controle de indexação.
- `canonical` → página principal.
- Open Graph → redes sociais.
- Schema → informações para buscadores.
- Sitemap → organização das páginas.

---

# Importância profissional

SEO Técnico é importante para:

- Sites de empresas.
- Lojas online.
- Blogs.
- Landing pages.
- SaaS.

---

## Próximo assunto

03 - Acessibilidade Avançada (WCAG e ARIA)
