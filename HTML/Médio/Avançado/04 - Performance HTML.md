# Performance HTML

## O que é Performance?

Performance significa a velocidade e eficiência de um site.

Um site com boa performance:

- Carrega mais rápido.
- Oferece melhor experiência.
- Consome menos recursos.
- Pode melhorar o SEO.

---

# Por que performance é importante?

Usuários esperam páginas rápidas.

Um site lento pode causar:

- Usuário sair da página.
- Menos conversões.
- Pior experiência.

Exemplo:

Uma loja online lenta pode perder clientes.

---

# 1. Otimização de imagens

Imagens geralmente são os arquivos mais pesados de um site.

Antes:

```
foto.jpg
5 MB
```

Depois:

```
foto.webp
200 KB
```

A página carrega mais rápido.

---

# Formatos modernos de imagem

## JPEG

Usado para:

- Fotos.
- Imagens com muitas cores.

---

## PNG

Usado para:

- Transparência.
- Logos.

---

## WebP

Formato moderno:

- Arquivos menores.
- Boa qualidade.

---

# Exemplo:

```html
<img
src="imagem.webp"
alt="Descrição da imagem">
```

---

# 2. Usar atributo loading

O atributo:

```html
loading="lazy"
```

faz imagens carregarem somente quando necessário.

Exemplo:

```html
<img
src="foto.jpg"
alt="Foto"
loading="lazy">
```

Útil para páginas grandes.

---

# 3. Definir tamanho das imagens

Informe largura e altura.

Exemplo:

```html
<img
src="logo.png"
width="200"
height="100"
alt="Logo">
```

Ajuda o navegador a organizar o espaço antes da imagem carregar.

---

# 4. Evitar código desnecessário

Um HTML limpo ajuda:

Ruim:

```html
<div>

<div>

<div>

Texto

</div>

</div>

</div>
```

Melhor:

```html
<section>

Texto

</section>
```

---

# 5. Carregamento de JavaScript

JavaScript pode bloquear o carregamento da página.

Exemplo:

```html
<script src="script.js"></script>
```

Pode atrasar a página.

---

Usamos:

```html
<script
src="script.js"
defer>
</script>
```

O navegador continua carregando o HTML.

---

# 6. CSS e arquivos externos

Evite colocar muito CSS dentro do HTML.

Ruim:

```html
<style>

Muito código CSS

</style>
```

Melhor:

```html
<link
rel="stylesheet"
href="style.css">
```

---

# 7. Meta viewport

Essencial para celulares.

```html
<meta
name="viewport"
content="width=device-width, initial-scale=1.0">
```

Ajuda na experiência mobile.

---

# 8. Lazy Loading

Além de imagens, pode ser usado em conteúdos pesados.

Exemplo:

```html
<iframe
loading="lazy">
</iframe>
```

---

# 9. Reduzir requisições

Cada arquivo externo precisa ser carregado.

Exemplo:

Muitos arquivos:

```
style1.css

style2.css

style3.css
```

Podem ser organizados.

---

# 10. HTML bem estruturado

Um HTML organizado ajuda:

- Navegadores.
- Ferramentas de análise.
- Manutenção.

---

# Exemplo de HTML otimizado

```html
<!DOCTYPE html>

<html lang="pt-BR">


<head>


<meta charset="UTF-8">


<meta
name="viewport"
content="width=device-width, initial-scale=1.0">


<link
rel="stylesheet"
href="style.css">


<title>
Site rápido
</title>


</head>


<body>


<img
src="logo.webp"
alt="Logo da empresa">


<script
src="script.js"
defer>
</script>


</body>


</html>
```

---

# Ferramentas para medir performance

Exemplos:

- Lighthouse.
- PageSpeed Insights.
- Chrome DevTools.

---

# Erros comuns

❌ Imagens enormes.

❌ Muitos scripts bloqueando a página.

❌ Código desorganizado.

❌ Não pensar em celular.

---

# Resumo rápido

Performance HTML envolve:

✅ Otimizar imagens.

✅ Usar formatos modernos.

✅ Usar lazy loading.

✅ Organizar código.

✅ Carregar scripts corretamente.

✅ Pensar em mobile.

---

# Importância profissional

Performance é importante para:

- Sites profissionais.
- E-commerce.
- Aplicações SaaS.
- Landing pages.

Um site rápido melhora a experiência do usuário.

---

## Próximo assunto

05 - HTML para Aplicações Web
