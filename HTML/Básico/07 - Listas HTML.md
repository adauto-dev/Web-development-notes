# Listas HTML

## O que são Listas?

Listas são usadas para organizar informações em uma página.

Exemplos:

- Menu de um site.
- Lista de serviços.
- Passos de um processo.
- Produtos.

HTML possui dois tipos principais de listas:

1. Lista não ordenada.
2. Lista ordenada.

---

# Lista não ordenada

A lista não ordenada usa pontos (•).

A tag principal é:

```html
<ul>
```

Significa:

**Unordered List**

(Lista sem ordem)

Cada item da lista usa:

```html
<li>
```

Significa:

**List Item**

(Item da lista)

---

## Exemplo

```html
<ul>

<li>Corte masculino</li>

<li>Barba</li>

<li>Sobrancelha</li>

</ul>
```

Resultado:

- Corte masculino
- Barba
- Sobrancelha

---

# Lista ordenada

A lista ordenada usa números.

A tag principal é:

```html
<ol>
```

Significa:

**Ordered List**

(Lista com ordem)

Também usa:

```html
<li>
```

para cada item.

---

## Exemplo

```html
<ol>

<li>Escolher serviço</li>

<li>Escolher horário</li>

<li>Confirmar agendamento</li>

</ol>
```

Resultado:

1. Escolher serviço
2. Escolher horário
3. Confirmar agendamento

---

# Diferença entre ul e ol

## ul

Usado quando a ordem não importa.

Exemplo:

```html
<ul>

<li>Shampoo</li>

<li>Pomada</li>

<li>Perfume</li>

</ul>
```

A ordem dos produtos não faz diferença.

---

## ol

Usado quando existe uma sequência.

Exemplo:

```html
<ol>

<li>Fazer cadastro</li>

<li>Escolher plano</li>

<li>Pagar</li>

</ol>
```

A ordem é importante.

---

# Listas dentro de listas

Podemos criar listas dentro de outras listas.

Exemplo:

```html
<ul>

<li>
Cabelo

<ul>

<li>Corte</li>

<li>Pintura</li>

</ul>

</li>

<li>
Barba
</li>

</ul>
```

Resultado:

- Cabelo
  - Corte
  - Pintura
- Barba

---

# Exemplo completo

```html
<!DOCTYPE html>

<html>

<body>

<h1>
Serviços da Barbearia
</h1>


<ul>

<li>Corte</li>

<li>Barba</li>

<li>Tratamento capilar</li>

</ul>


<h2>
Como agendar
</h2>


<ol>

<li>Escolha o serviço</li>

<li>Escolha o horário</li>

<li>Confirme o agendamento</li>

</ol>


</body>

</html>
```

---

# Como lembrar

Pense:

```
<ul>
Lista sem ordem
(pontos)

<ol>
Lista com ordem
(números)

<li>
Cada item
```

---

# Erros comuns

❌ Colocar texto diretamente dentro do `<ul>`.

Errado:

```html
<ul>

Corte

Barba

</ul>
```

Correto:

```html
<ul>

<li>Corte</li>

<li>Barba</li>

</ul>
```

---

❌ Esquecer o fechamento das tags.

Correto:

```html
<li>Barba</li>
```

---

# Resumo rápido

Listas organizam informações.

Principais tags:

- `<ul>` → lista sem ordem.
- `<ol>` → lista ordenada.
- `<li>` → item da lista.

---

## Próximo assunto

08 - Formulários HTML
