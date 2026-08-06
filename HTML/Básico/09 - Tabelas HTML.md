# Tabelas HTML

## O que são Tabelas?

Tabelas são usadas para organizar informações em linhas e colunas.

Exemplos:

- Lista de preços.
- Horários de atendimento.
- Comparação de planos.
- Dados de clientes.

Uma tabela é formada por:

- Linhas.
- Colunas.
- Células.

---

# Estrutura básica de uma tabela

A tag principal é:

```html
<table>
```

Dentro dela usamos:

```html
<tr>
```

para criar uma linha.

Significa:

**Table Row**

(Linha da tabela)

---

Para criar uma célula usamos:

```html
<td>
```

Significa:

**Table Data**

(Dado da tabela)

---

## Exemplo simples

```html
<table>

<tr>

<td>Nome</td>

<td>Idade</td>

</tr>


<tr>

<td>João</td>

<td>30</td>

</tr>

</table>
```

Resultado:

| Nome | Idade |
|---|---|
| João | 30 |

---

# Cabeçalho da tabela

Para criar títulos nas colunas usamos:

```html
<th>
```

Significa:

**Table Header**

(Cabeçalho da tabela)

Exemplo:

```html
<table>

<tr>

<th>Serviço</th>

<th>Preço</th>

</tr>


<tr>

<td>Corte</td>

<td>20€</td>

</tr>


</table>
```

Resultado:

| Serviço | Preço |
|---|---|
| Corte | 20€ |

---

# Estrutura completa de uma tabela

Uma tabela normalmente possui:

```html
<table>

<thead>

</thead>


<tbody>

</tbody>


</table>
```

---

## Thead

Representa o cabeçalho da tabela.

Exemplo:

```html
<thead>

<tr>

<th>Nome</th>

<th>Email</th>

</tr>

</thead>
```

---

## Tbody

Representa o conteúdo da tabela.

Exemplo:

```html
<tbody>

<tr>

<td>Maria</td>

<td>email@email.com</td>

</tr>

</tbody>
```

---

# Exemplo completo

```html
<!DOCTYPE html>

<html>

<body>


<h1>
Serviços
</h1>


<table>


<thead>

<tr>

<th>Serviço</th>

<th>Preço</th>

<th>Duração</th>

</tr>

</thead>


<tbody>


<tr>

<td>Corte</td>

<td>20€</td>

<td>30 min</td>

</tr>


<tr>

<td>Barba</td>

<td>15€</td>

<td>20 min</td>

</tr>


</tbody>


</table>


</body>

</html>
```

---

# Como lembrar

Pense em uma tabela:

```
<table>
Tabela inteira

<tr>
Linha

<th>
Título da coluna

<td>
Informação
```

---

# Erros comuns

❌ Usar tabela para criar o layout inteiro de um site.

Antigamente era usado, mas hoje usamos:

- CSS;
- Flexbox;
- Grid.

---

❌ Esquecer de colocar células dentro de uma linha.

Errado:

```html
<table>

<td>Texto</td>

</table>
```

Correto:

```html
<table>

<tr>

<td>Texto</td>

</tr>

</table>
```

---

# Resumo rápido

Tabelas organizam dados em linhas e colunas.

Principais tags:

- `<table>` → cria a tabela.
- `<tr>` → cria uma linha.
- `<th>` → cria um cabeçalho.
- `<td>` → cria uma célula.
- `<thead>` → cabeçalho.
- `<tbody>` → conteúdo.

---

## Próximo assunto

10 - Estrutura Semântica HTML
