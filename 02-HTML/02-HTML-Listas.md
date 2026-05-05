# HTML - Listas

As listas são usadas para organizar informações em forma de itens, deixando o conteúdo mais claro e legível em uma página WEB.

Existem três tipos de listas em HTML: lista não ordenada, lista ordenada e lista de definição.

## Lista Não Ordenada (`<ul>`)

Usada quando a ordem dos itens **não** importa. Nessa lista os itens aparecem com marcadores (normalmente bolinhas)

Os itens da lista, definidos pela tag `<li>`, são organizados em um contêiner definido pela tag `<ul>`.

**Exemplo:**

```html
<ul>
  <li>Primeiro item</li>
  <li>Segundo item</li>
  <li>Terceiro item</li>
</ul>
```

## Lista Ordenada (`<ol>`)

Usa quando a ordem dos itens é importante. Normalmente os itens aparecem numerados. 

Os itens da lista, definidos pela tag `<li>`, são organizados em um contêiner definido pela tag `<ol>`.

**Exemplo:**

```html
<ol>
  <li>Acordar</li>
  <li>Trocar de roupa</li>
  <li>Tomar café</li>
  <li>Ir para a escola</li>
</ol>
```

O tipo de numeração pode ser alterado usando o atributo `type` com um dos seguintes valores: 
- `'1'` - números (padrão).
- `'A'` - letras maiúsculas.
- `'a'` - letras minúsculas.
- `'I'` - algarismos romanos maiúsculos.
- `'i'` - algarismos romanos minúsculos.

**Exemplo:**

```html
<ol type='A'>
  <li>Tópico a</li>
  <li>Tópico b</li>
</ol>
```
