# Estrutura de Sites Reais

## O que é uma estrutura de site real?

Uma estrutura de site real é a forma como empresas e desenvolvedores organizam páginas, componentes e arquivos para criar projetos maiores.

Um site profissional normalmente não é apenas:

```
index.html
style.css
script.js
```

Ele possui uma organização pensada para crescer.

---

# Exemplo de um site simples

Estrutura:

```
meu-site/

│
├── index.html
│
├── sobre.html
│
├── contato.html
│
├── images/
│
├── css/
│
└── js/
```

Funciona bem para sites pequenos.

---

# Estrutura de um projeto maior

Projetos profissionais podem ser organizados assim:

```
meu-projeto/

│
├── public/
│   ├── images/
│   └── favicon.ico
│
├── src/
│   ├── pages/
│   ├── components/
│   ├── styles/
│   └── scripts/
│
├── README.md
│
└── package.json
```

---

# Pasta public

Guarda arquivos públicos.

Exemplos:

- Imagens.
- Ícones.
- Arquivos que o navegador acessa diretamente.

Exemplo:

```
public/

logo.png

favicon.ico
```

---

# Pasta src

Significa:

**Source**

(Fonte do projeto)

É onde fica o código principal.

Exemplo:

```
src/

components/

pages/

styles/
```

---

# Pasta pages

Guarda páginas do site.

Exemplo:

```
pages/

home.html

servicos.html

contato.html
```

Em frameworks como React e Next.js, essa ideia é muito usada.

---

# Pasta components

Componentes são partes reutilizáveis.

Exemplo:

Um menu aparece em todas as páginas:

```
Navbar
```

Em vez de criar várias vezes, criamos um componente.

Exemplo:

```
components/

Navbar

Footer

Button
```

---

# O conceito de reutilização

Imagine um site com:

10 páginas.

Todas possuem:

- Menu.
- Rodapé.

Sem componentes:

```
Copiar e colar 10 vezes.
```

Problema:

Se mudar o menu, precisa alterar 10 arquivos.

---

Com componentes:

```
Navbar único
```

Mudou uma vez, muda em todo lugar.

---

# Layout de uma página profissional

Uma página geralmente segue:

```
Header

Navigation

Hero Section

Content Sections

Footer
```

---

# Hero Section

É a primeira parte que o usuário vê.

Normalmente possui:

- Título principal.
- Descrição.
- Botão de ação.

Exemplo:

```html
<section>

<h1>
Agende seu horário online
</h1>


<p>
Sistema simples para sua empresa.
</p>


<button>
Começar agora
</button>


</section>
```

---

# Call To Action (CTA)

CTA significa:

**Call To Action**

(Chamada para ação)

Exemplos:

- Agendar agora.
- Comprar.
- Criar conta.
- Saiba mais.

---

# Estrutura pensando em usuário

Um site profissional deve responder:

## Quem somos?

Página:

```
Sobre
```

---

## O que oferecemos?

Página:

```
Serviços
```

---

## Como entrar em contato?

Página:

```
Contato
```

---

# Exemplo: Site de Barbearia

Estrutura:

```
Barbearia/

index.html

pages/

sobre.html

servicos.html

agendamento.html


images/

logo.png


css/

style.css


js/

script.js
```

---

# Exemplo: SaaS de agendamento

Pensando no seu futuro projeto:

```
ServiceFlow/

pages/

landing-page

login

dashboard

agendamento


components/

Navbar

Calendar

BookingForm


styles/

global.css
```

---

# Importância da organização

Um projeto organizado:

✅ Cresce mais fácil.

✅ Facilita manutenção.

✅ Ajuda equipes.

✅ Evita erros.

---

# Erros comuns

❌ Colocar todos os arquivos juntos.

❌ Criar nomes confusos.

Exemplo:

```
teste-final2.html
novo-certo.html
```

Melhor:

```
agendamento.html
servicos.html
```

---

# Resumo rápido

Sites profissionais possuem:

- Estrutura organizada.
- Pastas separadas.
- Componentes reutilizáveis.
- Páginas bem definidas.

Conceitos importantes:

- `pages` → páginas.
- `components` → partes reutilizáveis.
- `public` → arquivos públicos.
- `src` → código principal.

---

# Relação com o futuro

Esses conceitos aparecem em:

- React.
- Next.js.
- Aplicações SaaS.
- Sistemas profissionais.

---

## Próximo assunto

05 - HTML Preparação para CSS
