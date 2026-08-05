# Entidades HTML

## O que são Entidades HTML?

Entidades HTML são códigos especiais usados para mostrar caracteres que possuem um significado reservado no HTML ou símbolos que não são fáceis de digitar.

Elas começam com:

```html
&
```

e terminam com:

```html
;
```

---

# Por que usar entidades?

Alguns símbolos possuem funções dentro do HTML.

Por exemplo:

O símbolo:

```html
<
```

é usado para criar tags:

```html
<p>
```

Então, se quisermos mostrar o símbolo `<` como texto na página, precisamos usar uma entidade.

---

# Entidades mais usadas

## Menor que `<`

Código:

```html
&lt;
```

Resultado:

```
<
```

Exemplo:

```html
<p>

5 &lt; 10

</p>
```

Mostra:

```
5 < 10
```

---

## Maior que `>`

Código:

```html
&gt;
```

Resultado:

```
>
```

Exemplo:

```html
<p>

10 &gt; 5

</p>
```

Mostra:

```
10 > 5
```

---

## E comercial `&`

Código:

```html
&amp;
```

Resultado:

```
&
```

Exemplo:

```html
<p>

HTML &amp; CSS

</p>
```

Mostra:

```
HTML & CSS
```

---

## Espaço especial

Código:

```html
&nbsp;
```

Significa:

**Non-breaking space**

(espaço que não quebra)

Exemplo:

```html
<p>

Meu&nbsp;Site

</p>
```

---

## Símbolo de copyright

Código:

```html
&copy;
```

Resultado:

```
©
```

Exemplo:

```html
<p>

&copy; 2026 Minha Empresa

</p>
```

Mostra:

```
© 2026 Minha Empresa
```

---

## Euro €

Código:

```html
&euro;
```

Resultado:

```
€
```

Exemplo:

```html
<p>

Preço: 20&euro;

</p>
```

Mostra:

```
Preço: 20€
```

---

# Exemplo completo

```html
<!DOCTYPE html>

<html>

<body>


<h1>
Minha Loja
</h1>


<p>
Preço: 20&euro;
</p>


<p>
Direitos reservados &copy; 2026
</p>


<p>
5 &lt; 10
</p>


</body>

</html>
```

---

# Como lembrar

Entidades seguem o formato:

```
& nome ;
```

Exemplo:

```
&copy;
```

Começa com:

```
&
```

Termina com:

```
;
```

---

# Erros comuns

❌ Escrever símbolos especiais diretamente quando podem causar conflito.

Exemplo:

```html
5 < 10
```

Melhor:

```html
5 &lt; 10
```

---

❌ Esquecer o ponto e vírgula.

Errado:

```html
&copy
```

Correto:

```html
&copy;
```

---

# Resumo rápido

Entidades HTML mostram símbolos especiais.

Principais:

| Símbolo | Código |
|---|---|
| < | `&lt;` |
| > | `&gt;` |
| & | `&amp;` |
| © | `&copy;` |
| € | `&euro;` |
| espaço | `&nbsp;` |

---

## Próximo assunto

14 - Áudio e Vídeo HTML
