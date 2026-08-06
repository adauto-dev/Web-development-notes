# Formulários HTML

## O que são Formulários?

Formulários são usados para receber informações dos usuários.

Exemplos:

- Cadastro de usuário.
- Login.
- Pesquisa.
- Contato.
- Agendamento de serviços.

Em um sistema real, como uma plataforma de barbearia, o cliente poderia usar um formulário para informar:

- Nome.
- Email.
- Telefone.
- Serviço desejado.
- Horário.

---

# Tag form

A tag principal de um formulário é:

```html
<form>
</form>
```

Ela indica ao navegador que dentro dela existem campos para o usuário preencher.

---

# Campo de texto

Usamos a tag:

```html
<input>
```

com o atributo:

```html
type="text"
```

Exemplo:

```html
<input type="text">
```

Cria um campo para escrever textos.

---

# Label

A tag:

```html
<label>
```

cria uma descrição para o campo.

Exemplo:

```html
<label>
Nome:
</label>

<input type="text">
```

Resultado:

Nome:
[ campo de texto ]

---

# Atributo placeholder

Mostra uma dica dentro do campo.

Exemplo:

```html
<input 
type="text"
placeholder="Digite seu nome">
```

Enquanto o usuário não escreve nada, aparece:

"Digite seu nome"

---

# Campo de email

Usamos:

```html
type="email"
```

Exemplo:

```html
<input 
type="email"
placeholder="Digite seu email">
```

O navegador entende que deve receber um email.

---

# Campo de senha

Usamos:

```html
type="password"
```

Exemplo:

```html
<input 
type="password">
```

O texto digitado fica escondido.

Exemplo:

```
********
```

---

# Botão de envio

Usamos:

```html
<button>
```

Exemplo:

```html
<button>
Enviar
</button>
```

Cria um botão.

---

# Exemplo completo

```html
<!DOCTYPE html>

<html>

<body>

<h1>
Cadastro
</h1>


<form>


<label>
Nome:
</label>

<input 
type="text"
placeholder="Seu nome">


<br>


<label>
Email:
</label>

<input 
type="email"
placeholder="Seu email">


<br>


<label>
Senha:
</label>

<input 
type="password">


<br>


<button>
Cadastrar
</button>


</form>


</body>

</html>
```

---

# Outros tipos de input

HTML possui vários tipos:

## Número

```html
<input type="number">
```

Usado para números.

Exemplo:

- idade;
- quantidade.

---

## Data

```html
<input type="date">
```

Usado para escolher datas.

---

## Checkbox

```html
<input type="checkbox">
```

Permite selecionar opções.

Exemplo:

```html
<input type="checkbox">

Aceito os termos
```

---

## Radio

```html
<input type="radio">
```

Permite escolher uma opção.

Exemplo:

```html
<input type="radio">

Mensal

<input type="radio">

Anual
```

---

# Como lembrar

Um formulário funciona assim:

```
<form>
   ↓
<input>
   ↓
Usuário coloca informação
   ↓
<button>
   ↓
Enviar
```

---

# Erros comuns

❌ Esquecer de colocar o formulário dentro de `<form>`.

❌ Usar `type="text"` para todos os campos.

Exemplo:

Email deve usar:

```html
type="email"
```

Senha deve usar:

```html
type="password"
```

---

# Resumo rápido

Formulários recebem informações do usuário.

Principais tags:

- `<form>` → cria o formulário.
- `<input>` → cria campos.
- `<label>` → descreve campos.
- `<button>` → cria botão.

Principais tipos:

- `text` → texto.
- `email` → email.
- `password` → senha.
- `number` → números.
- `date` → datas.

---

## Próximo assunto

09 - Tabelas HTML
