# HTML - Tabelas

Neste tópico você aprenderá como organizar e apresentar dados de forma clara, estruturada e visualmente agradável, no formato tabular (linhas e colunas), em páginas web. Serão abordados os principais elementos de tabelas em **HTML**, como `<table>`, `<tr>`, `<th>` e `<td>`, além dos elementos semânticos: `<caption>`, `<thead>`, `<tbody>` e `<tfoot>`, que contribuem para a acessibilidade e melhor interpretação pelos motores de busca e leitores de tela.

Ao final, você será capaz de criar tabelas completas e bem estruturadas e compreender quando utilizar tabelas de forma adequada — especialmente para exibição de dados tabulares, evitando seu uso indevido para layout de páginas.

As tabelas são elementos fundamentais no desenvolvimento web quando precisamos organizar e apresentar dados de forma estruturada. Informações como notas de alunos, listas de produtos, horários ou relatórios são exemplos clássicos de uso de tabelas. 

## Estrutura básica de uma tabela em HTML

Uma tabela em HTML é definida pela tag `<table>`. Dentro dela, utilizamos outras tags para organizar linhas e colunas:

- **`<tr>` (table row):** define uma linha da tabela
- **`<th>` (table header):** define uma célula de cabeçalho
- **`<td>` (table data):** define uma célula de dados

**Exemplo:**

```html
<table border="1">
  <tr>
    <th>Nome</th>
    <th>Idade</th>
    <th>Curso</th>
  </tr>
  <tr>
    <td>Marcolino</td>
    <td>21</td>
    <td>Informática</td>
  </tr>
  <tr>
    <td>Felisberto</td>
    <td>25</td>
    <td>Design Gráfico</td>
  </tr>
</table>
```

Esse código gera uma tabela com três colunas (três células em cada linha), uma linha de títulos das colunas e duas linhas de dados.

Esse exemplo está usando o atributo `border`, com o valor 1, na abertura da tag `table`, definindo uma borda de 1px para a tabela, para que você consiga ver melhor a tabela. Mas, o ideal é definir a borda através do CSS, como será estudado posteriormente.

## Melhorando a semântica da tabela

No HTML5, é recomendado usar elementos que tornam a tabela mais organizada.

- **`<caption>`:** título da tabela
- **`<thead>`:** cabeçalho da tabela
- **`<tbody>`:** corpo da tabela
- **`<tfoot>`:** rodapé da tabela

Essa abordagem não só torna a tabela mais organizada, como também facilita a sua estilização. Também torna a tabela mais compreensível, tanto para os mecanismos de busca (SEO) como para os leitores de tela, melhorando a acessibilidade.

**Exemplo:**

```html
<table border="1">
  <caption>Lista de Alunos</caption>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Curso</th>
      <th>Nota</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Felisberto</td>
      <td>Informática</td>
      <td>9</td>
    </tr>
    <tr>
      <td>Marcolino</td>
      <td>Eletrônica</td>
      <td>7</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th colspan="2">Média</th>
      <td>8</td>
    </tr>
  </tfoot>
</table>
```

O atributo `colspan` em `<th colspan="2">Média</th>` define que a primeira célula da linha do rodapé deverá ocupar duas colunas.

Você também pode usar o atributo `rowspan` para definir que uma determinada célula ocupe mais de uma linha.

Repare também que, nesse exemplo, a tag `th` está sendo usada como título de colunas (**Nome**, **Curso** e **Nota**), mas também como título de linha (**Média**). Para melhorar a semântica e a acessibilidade isso deverá ser informado, explicitamente, através do atributo `scope`:

- `scope="col"`: Define que o th é o cabeçalho de uma coluna (aplica-se a todas as células abaixo dele).
- `scope="row"`: Define que o th é o cabeçalho de uma linha (aplica-se a todas as células à sua direita).

**Exemplo:**

```html
<table border="1">
  <tr>
    <th></th> <!-- Célula vazia no canto superior -->
    <th scope="col">Jan</th>
    <th scope="col">Fev</th>
    <th scope="col">Mar</th>
  </tr>
  <tr>
    <th scope="row">Receita</th> <!-- Cabeçalho de linha -->
    <td>R$ 1500</td>
    <td>R$ 2000</td>
    <td>R$ 2500</td>
  </tr>
  <tr>
    <th scope="row">Despesa</th> <!-- Cabeçalho de linha -->
    <td>R$ 1000</td>
    <td>R$ 1300</td>
    <td>R$ 1600</td>
  </tr>
  <tr>
    <th scope="row">Lucro</th> <!-- Cabeçalho de linha -->
    <td>R$ 500</td>
    <td>R$ 700</td>
    <td>R$ 900</td>
  </tr>
</table>
```

## Boas práticas no uso de tabelas
- Utilize tabelas apenas para dados tabulares (não para layout de páginas)
- Sempre use <th> para cabeçalhos
- Inclua <caption> para descrever a tabela
- Prefira CSS para estilização
- Mantenha o código organizado e indentado
