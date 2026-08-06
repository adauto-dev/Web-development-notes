# Caminhos de Arquivos HTML (Paths)

## O que são Paths?

Paths são os caminhos usados pelo HTML para encontrar arquivos.

Um site possui vários arquivos:

- Páginas HTML.
- Imagens.
- Arquivos CSS.
- Arquivos JavaScript.

O caminho informa ao navegador onde encontrar esses arquivos.

---

# Caminho relativo (Relative Path)

É o caminho mais usado em projetos.

Ele mostra a localização do arquivo em relação ao arquivo atual.

Exemplo:

Estrutura:

```
site/

index.html

imagem.jpg
```

Código:

```html
<img src="imagem.jpg">
```

O HTML procura a imagem na mesma pasta.

---

# Arquivo dentro de uma pasta

Exemplo:

Estrutura:

```
site/

index.html

imagens/

   foto.jpg
```

Código:

```html
<img src="imagens/foto.jpg">
```

O navegador entra na pasta:

```
imagens
```

e procura:

```
foto.jpg
```

---

# Voltar uma pasta

Usamos:

```
../
```

Significa:

"voltar para a pasta anterior".

Exemplo:

Estrutura:

```
site/

index.html

pages/

   contato.html

imagens/

   logo.png
```

Dentro de:

```
contato.html
```

Para acessar:

```
logo.png
```

usamos:

```html
<img src="../imagens/logo.png">
```

Explicação:

```
../
```

volta uma pasta.

Depois:

```
imagens/logo.png
```

entra na pasta da imagem.

---

# Caminho absoluto (Absolute Path)

É o endereço completo de um arquivo na internet.

Exemplo:

```html
<img src="https://site.com/imagem.jpg">
```

Usado principalmente para arquivos externos.

---

# Links entre páginas

Exemplo de estrutura:

```
site/

index.html

pages/

sobre.html
```

Dentro do:

```
index.html
```

Link:

```html
<a href="pages/sobre.html">
Sobre
</a>
```

---

# Organização profissional de projeto

Um site normalmente fica assim:

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
│   └── logo.png
│
├── css/
│   └── style.css
│
└── js/
    └── script.js
```

---

# Exemplo completo

Estrutura:

```
barbearia/

index.html

images/

  logo.png

pages/

  contato.html
```

No index:

```html
<img src="images/logo.png">


<a href="pages/contato.html">
Contato
</a>
```

---

# Erros comuns

❌ Errar o nome do arquivo.

Arquivo:

```
Logo.png
```

Código:

```html
<img src="logo.png">
```

Pode não funcionar.

Maiúsculas e minúsculas podem fazer diferença.

---

❌ Esquecer a pasta.

Errado:

```html
<img src="foto.jpg">
```

Quando a imagem está em:

```
images/foto.jpg
```

Correto:

```html
<img src="images/foto.jpg">
```

---

# Como lembrar

Pense como um endereço:

```
Casa → Rua → Número
```

No computador:

```
Projeto → Pasta → Arquivo
```

Exemplo:

```
site/images/logo.png
```

---

# Resumo rápido

Paths mostram onde estão os arquivos.

Principais:

- `arquivo.jpg` → mesma pasta.
- `pasta/arquivo.jpg` → entrar em uma pasta.
- `../` → voltar uma pasta.
- `https://` → caminho externo.

---

## Próximo assunto

17 - HTML5 e Acessibilidade
