# Áudio e Vídeo HTML

## O que são elementos de mídia?

Elementos de mídia permitem adicionar conteúdos como:

- Áudio.
- Vídeo.
- Sons.
- Apresentações.

O HTML5 trouxe suporte próprio para mídia, sem precisar de plugins externos.

---

# Áudio HTML

A tag usada para adicionar áudio é:

```html
<audio>
</audio>
```

Ela permite colocar arquivos de som na página.

Exemplos:

- Música.
- Podcast.
- Sons de aplicativos.

---

## Estrutura básica de áudio

```html
<audio controls>

<source src="musica.mp3" type="audio/mpeg">

</audio>
```

---

## Explicação

### `<audio>`

Cria o elemento de áudio.

---

### `controls`

Mostra os controles para o usuário.

Exemplo:

- Play.
- Pause.
- Volume.

Sem `controls`, o usuário não consegue controlar o áudio.

---

### `<source>`

Define o arquivo que será reproduzido.

Exemplo:

```html
<source src="musica.mp3">
```

---

# Exemplo completo de áudio

```html
<!DOCTYPE html>

<html>

<body>


<h1>
Meu Podcast
</h1>


<audio controls>

<source src="podcast.mp3" type="audio/mpeg">

</audio>


</body>

</html>
```

---

# Vídeo HTML

A tag usada para vídeos é:

```html
<video>
</video>
```

Ela permite colocar vídeos diretamente na página.

Exemplos:

- Vídeos de apresentação.
- Cursos.
- Demonstrações de produtos.

---

## Estrutura básica de vídeo

```html
<video controls>

<source src="video.mp4" type="video/mp4">

</video>
```

---

## Atributos importantes do vídeo

### controls

Mostra os controles.

```html
<video controls>
```

---

### width

Define a largura.

Exemplo:

```html
<video width="500">
```

---

### autoplay

Inicia automaticamente.

Exemplo:

```html
<video autoplay>
```

Obs:

Muitos navegadores bloqueiam autoplay com som.

---

### loop

Repete o vídeo.

Exemplo:

```html
<video loop>
```

---

### muted

Inicia sem som.

Exemplo:

```html
<video muted>
```

---

# Exemplo completo de vídeo

```html
<!DOCTYPE html>

<html>

<body>


<h1>
Apresentação da empresa
</h1>


<video 
controls
width="500">


<source 
src="apresentacao.mp4"
type="video/mp4">


</video>


</body>

</html>
```

---

# Formatos comuns

## Áudio

```
.mp3
.wav
.ogg
```

---

## Vídeo

```
.mp4
.webm
.ogg
```

O formato mais usado atualmente:

```
.mp4
```

---

# Exemplo em um site real

Imagine uma barbearia:

```html
<section>

<h2>
Conheça nosso espaço
</h2>


<video controls>

<source src="barbearia.mp4">

</video>


</section>
```

O cliente pode ver o ambiente antes de agendar.

---

# Erros comuns

❌ Esquecer o atributo `controls`.

Sem ele:

```html
<audio>
```

O usuário não verá os controles.

---

❌ Usar arquivos muito pesados.

Vídeos grandes deixam a página lenta.

---

❌ Esquecer o formato correto.

Exemplo:

Arquivo:

```
video.mp4
```

Código:

```html
<source src="video.mp4">
```

O nome precisa ser igual.

---

# Resumo rápido

HTML permite adicionar mídia usando:

Áudio:

```html
<audio>
```

Vídeo:

```html
<video>
```

Principais atributos:

- `controls` → mostra controles.
- `src` → localização do arquivo.
- `width` → largura.
- `autoplay` → inicia automaticamente.
- `loop` → repete.
- `muted` → sem som.

---

## Próximo assunto

15 - Meta Tags HTML
