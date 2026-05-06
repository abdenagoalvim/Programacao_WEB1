# HTML - Imagens

Imagens são recursos essenciais na web moderna, pois tornam o conteúdo mais atrativo, facilitam a compreensão das informações e melhoram a experiência do usuário. Em HTML, a inserção de imagens é feita principalmente por meio da tag `<img>`.

A tag `<img>` é uma tag vazia, ou seja, não possui tag de fechamento.

## Estrutura básica da tag `<img>`

```html
<img src="caminho/para/a/imagem.jpg" alt="Descrição da imagem">
```

**Onde:**

- `src` - caminho da imagem.
- `alt` - descrição alternativa da imagem.

**Exemplo:**

```html
<img src="imagens/foto.png" alt="Foto da turma em dia ensolarado.">
```

## Principais atributos da tag `<img>`

### `src` (source)

Define o caminho da imagem que será exibida. Pode ser:

- **Relativo:** quando a imagem está na mesma pasta ou em subpastas do projeto.
- **Absoluto:** quando a imagem está hospedada na internet (URL completa).

```html
<img src="imagem.jpg" alt="Exemplo">
<img src="https://site.com/imagem.jpg" alt="Imagem online">
```

### `alt` (texto alternativo)

Fornece uma descrição da imagem. Esse atributo é essencial para acessibilidade (leitores de tela) e exibição de uma descrição da imagem caso ela não carregue.

### `width` e `height`

Definem a largura e altura da imagem (em pixels ou porcentagem).

```html
<img src="foto.jpg" alt="Foto" width="300" height="200">
```

### `title`

Exibe um texto ao passar o mouse sobre a imagem.

```html
<img src="imagem.jpg" alt="Imagem" title="Descrição adicional">
```

## Boas práticas no uso de imagens

- Sempre utilizar o atributo `alt`
- Otimizar o tamanho da imagem (para melhorar o carregamento da página)
- Utilizar formatos adequados:
    - **JPEG/JPG:** fotos.
    - **PNG:** imagens com transparência.
    - **GIF:** imagens com animações.
    - **SVG:** gráficos vetoriais.
- Usar CSS para estilização.
- Organizar imagens em pastas (ex: /img ou /images).

## Imagens como links

Uma imagem pode funcionar como um link:

```html
<a href="pagina.html">
    <img src="botao.jpg" alt="Ir para página">
</a>
```
