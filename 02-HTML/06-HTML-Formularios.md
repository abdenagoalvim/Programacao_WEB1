# HTML - Formulários

Os formulários são um dos principais recursos do HTML para permitir a interação entre usuários e páginas web. Por meio deles, é possível coletar informações como:

- Nome;
- E-mail;
- Senha;
- Data de nascimento;
- Endereço;
- Opções de escolha;
- Comentários;
- Arquivos;
- E muito mais.

Os controles de entrada, que também são chamados de campos ou elementos de formulário, são preenchidos pelo usuário. Depois os dados desses campos são enviados para um servidor para serem processados.

**Exemplo simples de formulário:**

```html
<form>
    <label>Nome:</label>
    <input type="text">

    <button>Enviar</button>
</form>
```

**Resultado:**

![formulário simples com caixa de texto e botão](imagens/form-simples.jpeg)

## O elemento `<form>`

O elemento `<form>` é utilizado para definir o início e o fim de um formulário HTML. O elemento `<form>` funciona como um container para os campos que pertencem ao mesmo formulário.

**Estrutura básica do formulário**

```html
<form>
    <!-- Campos do formulário -->
</form>
```

Um formulário pode conter diferentes tipos de elementos (campos), como:

- label
- input (text, password, email, number, date, checkbox, radio, file)
- select
- textarea
- button

### Atributo `action`

O atributo **`action`** indica para onde os dados do formulário serão enviados para serem processados.

```html
<form action="cadastrar.php">
```

Nesse caso, quando o formulário for enviado, os dados serão encaminhados para o arquivo: "**cadastro.php**"

**Exemplo:**

```html
<form action="cadastro.php">
    <label>Nome:</label>
    <input type="text" name="nome">

    <button type="submit">Cadastrar</button>
</form>
```

**Resultado:**

![formulário com action="cadastro.php"](imagens/form-action-cadastrar.jpeg)

Quando o usuário enviar o formulário, o servidor poderá processar os dados utilizando o arquivo "**cadastro.php**" indicado no atributo **`action`**.

### Atributo `method`

O atributo **`method`** define como os dados serão enviados. Os dois valores mais utilizados são: **`get`** e **`post`**.

#### Método `GET`

O método **`GET`** envia os dados por meio da URL.

**Exemplo:**

```html
<form action="pesquisar.php" method="get">
    <input type="text" name="pesquisa">

    <button type="submit">Pesquisar</button>
</form>
```

**Resultado:**

![formulário com método get](imagens/form-method-get.jpeg)

Se o usuário pesquisar por JavaScript, a URL será semelhante a:

```html
pesquisar.php?pesquisa=JavaScript
```

O método **`GET`** costuma ser utilizado em:

- Pesquisas;
- Filtros;
- Consultas;
- Formulários em que os dados não são sigilosos.

#### Método `POST`

O método **`POST`** envia os dados no corpo da requisição HTTP.

**Exemplo:**

```html
<form action="cadastro.php" method="post">
    <p><label>Nome:</label>
    <input type="text" name="nome"></p>
    
    <p><label>E-mail:</label>
    <input type="email" name="email"></p>
    
    <button type="submit">Cadastrar</button>
</form>
```

**Resultado:**

![formulário com método post](imagens/form-method-post.jpeg)

O método **`POST`** normalmente é utilizado em:

- Cadstro;
- Login;
- Envio de informações;
- Alteração de dados;
- Upload de arquivos.

**Atenção:** utilizar **`POST`** não significa, por si só, que os dados estão protegidos. Para proteger informações, especialmente senhas, também é necessário utilizar mecanismos como HTTPS e boas práticas de segurança.


