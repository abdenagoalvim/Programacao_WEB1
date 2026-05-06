# CSS (Cascading Style Sheets)

As CSS (Folhas de Estilo em Cascata) é uma linguagem de estilos usada para definir o layout e a aparéncia visual (cores, fontes, espaçamento, animações, responsividade...) de páginas WEB estruturadas com HTML. 
Ou seja, o HTML estrutura o conteúdo e o CSS cuida da estética.

Principais responsabilidades das CSS:

- **Estilização Visual:** Definir cores, tipos de fonte, tamanhos de texto, bordas...
- **Layout e posicionamento:** Organizar elementos na página.
- **Responsividade:** Adaptar a página WEB para diferentes tamanhos de tela (desktop, celular, tablet...).
- **Separação de Conteúdo e Design:** Manter o HTML limpo a partir do gerenciamento de estilos em um arquivo (`.css`) separado, facilitando a manutenção.

## Estrutura Básica CSS

Uma regra CSS é composta por:

- **Seletor:** indica qual elemento será estilizado.
- **Propriedade:** determina o aspecto que será alterado.
- **Valor:** a definição da propriedade.

**Sintaxe:**

```css
seletor {
  propriedade: valor;
}
```

**Exemplo:**

```css
p {
  color: blue;
  font-size: 16px;
}
```

Nesse exemplo, todos os parágrafos (`<p>`) terão texto azul e tamanho 16px.

## Formas de aplicar CSS

Existem três formas principais: inline, interno e externo.

### CSS Inline

O CSS é aplicado diretamente dentro da tag HTML, utilizando o atributo `style`.

**Características:**

- Aplica estilo apenas a um elemento específico.
- Tem alta prioridade (sobrescreve outros estilos).
- Não é reutilizável.

**Vantagens:**

- Simples e rápido para testes.
- Útil para ajustes pontuais.

**Desvantagens:**

- Dificulta a manutenção.
- Polui o código HTML.
- Não é reutilizável.
- Não segue boas práticas de organização.

**Exemplo:**

```css
<p style="color: blue; font-size: 18px;">
  Este é um parágrafo com estilo inline.
</p>
```

### CSS Interno (ou incorporado)

Os estilos são definidos dentro da própria página HTML, na seção `<head>`, utilizando a tag `<style>`.

**Características:**

- Aplica estilos a vários elementos da página.
- Válido apenas para uma única página.

**Vantagens:**

- Organização melhor que o inline.
- Não precisa de arquivo externo.

**Desvantagens:**

- Não permite reutilização em outras páginas.
- Pode deixar o HTML mais carregado.

**Exemplo:**
```html
<!DOCTYPE html>
<html>
<head>
  <style>
    p {
      color: green;
      font-size: 16px;
    }
  </style>
</head>
<body>
  <p>Este é um parágrafo com CSS interno.</p>
</body>
</html>
```

### 3. CSS Externo (arquivo separado)

Os estilos são definidos em um arquivo `.css` separado e vinculados ao HTML com a tag `<link>`.

**Características:**

- Estilos ficam em um arquivo separado.
- Pode ser reutilizado em várias páginas.

**Vantagens:**

- Melhor organização e manutenção.
- Reutilização de código.
- Segue boas práticas de desenvolvimento.

**Desvantagens:**

- Requer um arquivo adicional.
- Depende do carregamento externo.

**Exemplo:**<br>
**Arquivo HTML:**
```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="estilos.css">
</head>
<body>
  <p>Este é um parágrafo com CSS externo.</p>
</body>
</html>
```

**Arquivo CSS:**
```css
p {
  color: red;
  font-size: 20px;
}
```

### Boas Práticas

- Evite **CSS Inline**. Use apenas em casos muito específicos.
- Use **CSS Interno** para páginas simples.
- Prefira sempre o **CSS Externo**, pois é a forma mais profissional e escalável.

