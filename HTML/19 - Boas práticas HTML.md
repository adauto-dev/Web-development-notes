# Boas práticas HTML

## O que são boas práticas?

Boas práticas são formas corretas de escrever código para deixar o projeto:

- Mais organizado.
- Mais fácil de entender.
- Mais fácil de modificar.
- Mais profissional.

Um bom programador não pensa apenas em fazer funcionar, mas também em criar um código limpo.

---

# 1. Usar HTML semântico

Prefira tags que possuem significado.

Melhor:

```html
<header>

Logo e menu

</header>
```

Do que:

```html
<div>

Logo e menu

</div>
```

O HTML semântico ajuda:

- SEO.
- Acessibilidade.
- Organização.

---

# 2. Organizar o código

Use espaços e identação.

Ruim:

```html
<body>
<h1>Site</h1>
<p>Texto</p>
</body>
```

Melhor:

```html
<body>

  <h1>
    Site
  </h1>

  <p>
    Texto
  </p>

</body>
```

Fica mais fácil de ler.

---

# 3. Usar nomes claros

Evite nomes confusos.

Ruim:

```html
<div class="box1">
</div>
```

Melhor:

```html
<div class="card-servico">
</div>
```

O nome deve explicar a função.

---

# 4. Fechar as tags corretamente

Sempre feche tags que precisam de fechamento.

Correto:

```html
<p>
Meu texto
</p>
```

Errado:

```html
<p>
Meu texto
```

---

# 5. Usar atributos importantes

Imagens:

```html
<img 
src="foto.jpg"
alt="Descrição da foto">
```

Formulários:

```html
<label>
Nome
</label>

<input type="text">
```

Esses detalhes melhoram a qualidade do site.

---

# 6. Não repetir código sem necessidade

Evite criar a mesma estrutura várias vezes.

Exemplo:

Ruim:

```html
<h2>
Serviço 1
</h2>

<h2>
Serviço 2
</h2>

<h2>
Serviço 3
</h2>
```

Em projetos maiores podemos usar:

- Componentes.
- JavaScript.
- Frameworks.

---

# 7. Separar HTML, CSS e JavaScript

Cada tecnologia tem uma função.

HTML:

```text
Estrutura
```

CSS:

```text
Design
```

JavaScript:

```text
Interação
```

Exemplo:

```
index.html

style.css

script.js
```

---

# 8. Usar nomes de arquivos organizados

Evite:

```
pagina1.html
teste.html
novo2.html
```

Use:

```
sobre.html
contato.html
servicos.html
```

---

# 9. Pensar em responsividade

Um site deve funcionar em:

- Computador.
- Tablet.
- Celular.

Por isso usamos:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

---

# 10. Validar o HTML

Podemos verificar se o código possui erros.

Ferramentas:

- W3C Validator.
- Ferramentas do navegador.

Isso ajuda a encontrar problemas.

---

# Exemplo de HTML organizado

```html
<!DOCTYPE html>

<html lang="pt-BR">


<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>
Minha Empresa
</title>

</head>


<body>


<header>

<h1>
Minha Empresa
</h1>

</header>


<main>


<section>

<h2>
Serviços
</h2>

<p>
Qualidade e profissionalismo.
</p>

</section>


</main>


<footer>

<p>
© 2026 Minha Empresa
</p>

</footer>


</body>


</html>
```

---

# Erros comuns de iniciantes

❌ Colocar tudo dentro de uma única div.

❌ Misturar CSS e JavaScript dentro do HTML sem necessidade.

❌ Não organizar pastas.

❌ Não usar nomes claros.

❌ Copiar código sem entender.

---

# Resumo rápido

Boas práticas deixam o código:

✅ Limpo.

✅ Organizado.

✅ Fácil de manter.

✅ Profissional.

Principais regras:

- Use HTML semântico.
- Organize arquivos.
- Escreva código legível.
- Use nomes claros.
- Pense no usuário.

---

## Próximo assunto

20 - Revisão HTML Básico + Primeiro Projeto
