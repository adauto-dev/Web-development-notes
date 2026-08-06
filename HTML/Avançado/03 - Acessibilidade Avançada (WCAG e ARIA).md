# Acessibilidade Avançada (WCAG e ARIA)

## O que é WCAG?

WCAG significa:

**Web Content Accessibility Guidelines**

( Diretrizes de Acessibilidade para Conteúdo Web )

São recomendações internacionais para criar sites acessíveis.

O objetivo é garantir que pessoas com diferentes necessidades consigam usar a web.

---

# Os 4 princípios da WCAG

A acessibilidade é baseada em 4 princípios:

## 1. Perceptível

O usuário precisa conseguir perceber o conteúdo.

Exemplos:

- Imagens com descrição.
- Textos legíveis.
- Legendas em vídeos.

---

## 2. Operável

O usuário precisa conseguir controlar o site.

Exemplos:

- Navegação pelo teclado.
- Botões funcionando.
- Menus acessíveis.

---

## 3. Compreensível

O conteúdo deve ser fácil de entender.

Exemplos:

- Textos claros.
- Formulários organizados.
- Mensagens de erro explicativas.

---

## 4. Robusto

O site deve funcionar com diferentes tecnologias.

Exemplos:

- Navegadores diferentes.
- Leitores de tela.
- Dispositivos diferentes.

---

# O que é ARIA?

ARIA significa:

**Accessible Rich Internet Applications**

São atributos HTML que adicionam informações para tecnologias assistivas.

Usamos principalmente quando o HTML normal não é suficiente.

---

# Regra principal do ARIA

Primeiro use HTML semântico.

Exemplo:

Melhor:

```html
<button>
Enviar
</button>
```

Do que:

```html
<div role="button">
Enviar
</div>
```

O elemento `button` já possui acessibilidade.

---

# Principais atributos ARIA

## aria-label

Cria uma descrição para elementos.

Exemplo:

```html
<button aria-label="Fechar menu">

X

</button>
```

O leitor de tela entende:

"Fechar menu"

---

# aria-labelledby

Liga um elemento a outro texto.

Exemplo:

```html
<h2 id="titulo">
Contato
</h2>


<section aria-labelledby="titulo">

</section>
```

A seção recebe o nome do título.

---

# aria-describedby

Adiciona uma explicação extra.

Exemplo:

```html
<input
aria-describedby="ajuda">


<p id="ajuda">

Digite um email válido.

</p>
```

---

# aria-hidden

Esconde elementos de leitores de tela.

Exemplo:

```html
<span aria-hidden="true">

⭐

</span>
```

Usado para elementos apenas visuais.

---

# aria-expanded

Mostra se algo está aberto ou fechado.

Exemplo:

```html
<button aria-expanded="false">

Menu

</button>
```

Muito usado em menus.

---

# Navegação pelo teclado

Um site profissional deve funcionar usando:

- Tab.
- Enter.
- Espaço.
- Setas.

Exemplo:

```html
<button>
Enviar
</button>
```

Botões HTML já possuem suporte.

---

# Foco (Focus)

Quando navegamos pelo teclado, o usuário precisa saber onde está.

Exemplo:

```css
button:focus {

outline: 2px solid;

}
```

O CSS controla a aparência do foco.

---

# Formulários acessíveis

Exemplo:

```html
<label for="nome">

Nome

</label>


<input
id="nome"
type="text">
```

O campo possui identificação clara.

---

# Mensagens de erro

Ruim:

```
Erro!
```

Melhor:

```
O email informado não possui formato válido.
```

O usuário entende o problema.

---

# Imagens decorativas

Nem toda imagem precisa ser descrita.

Imagem importante:

```html
<img
src="produto.jpg"
alt="Tênis esportivo preto">
```

Imagem apenas decorativa:

```html
<img
src="linha.png"
alt="">
```

---

# Exemplo de menu acessível

```html
<nav aria-label="Menu principal">


<a href="/">
Home
</a>


<a href="/servicos">
Serviços
</a>


<a href="/contato">
Contato
</a>


</nav>
```

---

# Boas práticas profissionais

✅ Use HTML semântico primeiro.

✅ Use ARIA quando necessário.

✅ Teste navegação pelo teclado.

✅ Use textos claros.

✅ Descreva imagens importantes.

---

# Ferramentas para testar acessibilidade

Exemplos:

- Lighthouse (Chrome DevTools).
- WAVE.
- Leitores de tela.

---

# Resumo rápido

WCAG define princípios de acessibilidade:

- Perceptível.
- Operável.
- Compreensível.
- Robusto.

ARIA adiciona informações extras:

- `aria-label`
- `aria-labelledby`
- `aria-describedby`
- `aria-hidden`
- `aria-expanded`

---

# Importância profissional

Acessibilidade é importante em:

- Sites de empresas.
- Sistemas governamentais.
- Aplicações SaaS.
- Grandes produtos digitais.

Um bom desenvolvedor cria sistemas que todos conseguem usar.

---

## Próximo assunto

04 - Performance HTML
