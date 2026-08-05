# Estrutura de um Projeto HTML Profissional

## O que é uma estrutura de projeto?

Uma estrutura de projeto é a forma como organizamos os arquivos de um site.

Um projeto bem organizado facilita:

- Encontrar arquivos.
- Trabalhar em equipe.
- Fazer alterações.
- Crescer o projeto no futuro.

---

# Estrutura simples de um site

Exemplo:

```
meu-site/

│
├── index.html
│
├── pages/
│   ├── sobre.html
│   └── contato.html
│
├── images/
│   ├── logo.png
│   └── foto.jpg
│
├── css/
│   └── style.css
│
└── js/
    └── script.js
```

---

# Arquivo index.html

O arquivo:

```html
index.html
```

normalmente é a página inicial do site.

Quando alguém entra no site:

```
www.meusite.com
```

o navegador procura:

```
index.html
```

---

# Pasta pages

Usada para guardar outras páginas.

Exemplo:

```
pages/

sobre.html

contato.html
```

Código para acessar:

```html
<a href="pages/sobre.html">
Sobre nós
</a>
```

---

# Pasta images

Guarda imagens do projeto.

Exemplo:

```
images/

logo.png

produto.jpg
```

Usamos:

```html
<img src="images/logo.png">
```

---

# Pasta css

Guarda os arquivos de estilo.

Exemplo:

```
css/

style.css
```

O HTML conecta com CSS usando:

```html
<link rel="stylesheet" href="css/style.css">
```

---

# Pasta js

Guarda arquivos JavaScript.

Exemplo:

```
js/

script.js
```

O HTML conecta usando:

```html
<script src="js/script.js"></script>
```

---

# Exemplo de index.html organizado

```html
<!DOCTYPE html>

<html lang="pt-BR">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">


<title>
Meu Site
</title>


<link rel="stylesheet" href="css/style.css">


</head>


<body>


<header>

<h1>
Meu Site
</h1>

</header>


<main>

<p>
Bem-vindo ao meu site.
</p>

</main>


<script src="js/script.js"></script>


</body>

</html>
```

---

# Caminho dos arquivos

Imagine o projeto como uma casa:

```
meu-site
    |
    ├── index.html
    |
    ├── css
    |     |
    |     └── style.css
    |
    └── images
          |
          └── logo.png
```

Cada pasta tem sua função.

---

# Por que não colocar tudo junto?

Exemplo ruim:

```
meu-site/

index.html

style.css

script.js

foto1.jpg

foto2.jpg

foto3.jpg
```

Com poucos arquivos funciona.

Mas em projetos grandes fica difícil encontrar tudo.

---

# Estrutura usada por profissionais

Em projetos reais podemos ter:

```
src/

components/

assets/

styles/

utils/

```

Isso aparece muito em:

- React.
- Next.js.
- Aplicações grandes.

---

# Como lembrar

Organização básica:

```
HTML
→ estrutura

CSS
→ aparência

JavaScript
→ comportamento
```

---

# Erros comuns

❌ Misturar imagens, CSS e JavaScript na mesma pasta.

❌ Criar nomes confusos.

Exemplo:

```
novo.html
teste2.html
final.html
```

Melhor:

```
contato.html
servicos.html
sobre.html
```

---

# Resumo rápido

Um projeto HTML organizado possui:

- `index.html` → página inicial.
- `pages/` → outras páginas.
- `images/` → imagens.
- `css/` → estilos.
- `js/` → scripts.

Organização é uma habilidade importante de todo desenvolvedor.

---

## Próximo assunto

19 - Boas práticas HTML
