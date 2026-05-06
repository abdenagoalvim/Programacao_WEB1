# HTML - Links (hiperlinks/âncoras)

Os **links** em HTML, também chamados de **hiperlinks**, são elementos fundamentais da web. Eles permitem conectar uma página a outra, criar navegação entre conteúdos e direcionar o usuário para diferentes recursos, como páginas, arquivos, e-mails ou até partes específicas de um mesmo documento.

Um **link** é um elemento clicável que leva o usuário de um ponto a outro. É graças aos **links** que a web funciona como uma **“teia”** de informações interligadas.

No HTML, os **links** são criados com a tag `<a>`, que vem da palavra anchor (âncora).

## Estrutura básica de um link

```html
<a href="URL">Texto ou imagem</a>
```

**Onde:**

- `<a>`: define o link.
- `href`: atributo que define o destino do link.
- `URL`: endereço único de um recurso na WEB para onde o link aponta.
- `Texto ou imagem`: conteúdo visível e clicável.

**Exemplo:**

```html
<a href="https://www.google.com">Ir para o Google</a>
```

## Tipos de links

### Link externo

Aponta para um site fora do seu projeto (site).

**Exemplo:**

```html
<a href="https://www.youtube.com">YouTube</a>
```

### Link interno

Aponta para outra página do mesmo site.

**Exemplo:**

```html
<a href="pagina2.html">Ir para Página 2</a>
```

### Link para e-mail

Aponta para um e-mail específico, abrindo a aplicação de e-mail padrão da máquina do usuário.

**Exemplo:**

```html
<a href="mailto:exemplo@mail.com">Enviar e-mail</a>
```

### Link para telefone

Aponta para um número de telefone.

```html
<a href="tel:+5531999999999">Ligar agora</a>
```

### Link para download de arquivos

Aponta para um arquivo a ser baixado.

```html
<a href="arquivo.pdf" download>Baixar arquivo</a>
```

### Âncoras (links dentro da mesma página)

Permitem navegar entre seções da mesma página.

```html
<a href="#secao1">Seção 1</a>
...
<h2 id="secao1">Seção 1</h2>
```

## Atributos da tag `<a>`

### `target`

Define onde o link será aberto.

Valores comuns:

- `_self` - mesma aba (padrão).
- `_blank` - nova aba.

**Exemplo:**
```html
<a href="https://www.google.com" target="_blank">Ir para o Google</a>
```

### `title`

Define um título para o link. Exibe uma dica ao passar o mouse sobre o link.

**Exemplo:**
```html
<a href="https://www.google.com" title="Ir para o Google">Google</a>
```
