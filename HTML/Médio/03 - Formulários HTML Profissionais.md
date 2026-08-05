# Formulários HTML Profissionais

## O que são formulários profissionais?

Formulários são usados para coletar informações dos usuários.

Em sites reais eles aparecem em:

- Cadastro de clientes.
- Login.
- Agendamento.
- Compras.
- Contato.
- Pesquisas.

Exemplo:

Uma barbearia pode ter um formulário:

- Nome do cliente.
- Email.
- Telefone.
- Serviço escolhido.
- Data.
- Horário.

---

# Estrutura de um formulário

A tag principal continua sendo:

```html
<form>
</form>
```

Dentro dela colocamos:

- Labels.
- Inputs.
- Select.
- Textarea.
- Buttons.

---

# Atributo action

O atributo:

```html
action
```

define para onde os dados serão enviados.

Exemplo:

```html
<form action="/cadastro">
```

Quando o usuário envia, os dados vão para:

```
/cadastro
```

No HTML puro normalmente não usamos ainda, porque o envio será tratado com:

- JavaScript.
- Backend.
- APIs.

---

# Atributo method

Define como os dados serão enviados.

Existem dois principais:

## GET

Envia dados pela URL.

Exemplo:

```
site.com/busca?nome=Joao
```

Usado para:

- Pesquisas.
- Filtros.

---

## POST

Envia dados escondidos no corpo da requisição.

Usado para:

- Cadastro.
- Login.
- Informações privadas.

Exemplo:

```html
<form method="post">
```

---

# Input types profissionais

HTML possui vários tipos de campos.

---

# Email

```html
<input type="email">
```

Aceita emails.

Exemplo:

```
cliente@email.com
```

---

# Telefone

```html
<input type="tel">
```

Usado para números de telefone.

---

# Data

```html
<input type="date">
```

Cria um seletor de data.

Exemplo:

```
05/08/2026
```

---

# Hora

```html
<input type="time">
```

Seleciona horários.

Exemplo:

```
14:30
```

Muito usado em sistemas de agendamento.

---

# Número

```html
<input type="number">
```

Aceita números.

Exemplo:

- Quantidade.
- Idade.
- Preço.

---

# Campo obrigatório

Usamos:

```html
required
```

Exemplo:

```html
<input 
type="email"
required>
```

O usuário precisa preencher.

---

# Placeholder

Mostra uma dica.

Exemplo:

```html
<input
placeholder="Digite seu nome">
```

---

# Min e Max

Limitam valores.

Exemplo:

```html
<input
type="number"
min="1"
max="10">
```

Aceita apenas números entre 1 e 10.

---

# Select

Cria uma lista de opções.

Exemplo:

```html
<label>
Escolha o serviço:
</label>


<select>


<option>
Corte
</option>


<option>
Barba
</option>


<option>
Corte + Barba
</option>


</select>
```

Resultado:

```
Corte
Barba
Corte + Barba
```

---

# Textarea

Usado para textos maiores.

Exemplo:

```html
<textarea>

</textarea>
```

Usado para:

- Mensagens.
- Observações.
- Comentários.

---

# Radio Button

Permite escolher apenas uma opção.

Exemplo:

```html
<input 
type="radio"
name="plano">

Mensal


<input
type="radio"
name="plano">

Anual
```

O atributo `name` agrupa as opções.

---

# Checkbox

Permite escolher várias opções.

Exemplo:

```html
<input type="checkbox">

Aceito os termos
```

---

# Fieldset e Legend

Organizam grupos de campos.

Exemplo:

```html
<fieldset>


<legend>
Dados pessoais
</legend>


<label>
Nome:
</label>


<input type="text">


</fieldset>
```

Resultado:

Uma caixa agrupando informações.

---

# Exemplo profissional: Agendamento

```html
<form>


<label for="nome">
Nome:
</label>

<input
id="nome"
type="text"
required>


<label for="servico">
Serviço:
</label>


<select id="servico">

<option>
Corte
</option>

<option>
Barba
</option>

<option>
Corte e Barba
</option>

</select>


<label for="data">
Data:
</label>


<input
id="data"
type="date"
required>


<label for="hora">
Horário:
</label>


<input
id="hora"
type="time"
required>


<button>
Agendar
</button>


</form>
```

---

# Validação básica HTML

O navegador já consegue validar alguns campos.

Exemplo:

```html
<input 
type="email"
required>
```

Se o usuário colocar:

```
abc
```

O navegador avisa que o email não é válido.

---

# Erros comuns

❌ Usar input errado.

Exemplo:

Telefone:

Errado:

```html
<input type="text">
```

Melhor:

```html
<input type="tel">
```

---

❌ Esquecer o label.

Melhor:

```html
<label>
Nome
</label>

<input>
```

---

# Resumo rápido

Formulários profissionais usam:

- `<form>` → formulário.
- `<input>` → campos.
- `<select>` → opções.
- `<textarea>` → textos longos.
- `<button>` → enviar.
- `required` → obrigatório.
- `method` → forma de envio.

---

# Aplicação real

Esses conceitos são a base de:

- Sistemas de reservas.
- Lojas online.
- Plataformas SaaS.
- Cadastros de usuários.

---

## Próximo assunto

04 - Estrutura de Sites Reais
