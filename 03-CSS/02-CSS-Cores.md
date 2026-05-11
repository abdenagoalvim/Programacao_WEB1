# CSS - Trabalhando com cores

As cores são elementos fundamentais no desenvolvimento de páginas WEB. Elas ajudam a melhorar a aparência visual, organizar informações, destacar conteúdos importantes e tornar a navegação mais agradável para o usuário.

No desenvolvimento WEB, as cores são aplicadas principalmente utilizando CSS (Cascading Style Sheets). Com o CSS, é possível definir cores para: textos, fundos, bordas, links, botões, tabelas, etc.

Além da estética, o uso correto das cores também influencia a acessibilidade e a experiência do usuário.

## Como aplicar cores no CSS

As cores são definidas através de propriedades CSS, como:

```css
color
background-color
border-color
```

**Exemplo:**

```html
<body>

    <h1>Título Azul</h1>

    <p>Parágrafo com fundo cinza claro.</p>

</body>
```

```css
h1 {
    color: blue;
}
p {
    background-color: #e7e7e7;
}
```

## A propriedade `color`

A propriedade `color` é usada para definir a cor do texto.

**Exemplo:**

```css
p{
    color: blue;
}
```

**Resultado:**

o texto dos parágrafos serão exibidos em azul.

## A propriedade `background-color`

A propriedade `background-color` é usada para definir a cor de fundo de um elemento.

**Exmplo:**
```css
body{
    background-color: lightblue;
}
```

**Resultado:**

o fundo dá página será exibido em azul claro.

## Formas de representar cores no CSS

O CSS permite representar cores de diferentes maneiras.

### Nome da cor

É a forma mais simples. Veja na lista abaixo alguns nomes disponíveis:

- red
- blue
- green
- yellow
- black
- white
- gray
- orange
- purple

**Exemplo:**

```css
p{
    color: green;
}
```

### Cores Hexadecimais

As cores hexadecimais são muito utilizadas no desenvolvimento WEB.

A sintaxe utiliza o símbolo # seguido de 6 caracteres.

```css
#RRGGBB
```

Onde:

- RR → intensidade do vermelho
- GG → intensidade do verde
- BB → intensidade do azul

Os valores variam de `00` (nenhuma intensidade) a `FF` (intensidade total).

**Exemplos:**
```css
color: #FF0000 /* vermelho */
color: #00FF00 /* verde */
color: #0000FF /* azul */
color: #FFFF00 /* amarelo */
color: #000000 /* preto */
color: #FFFFFF /* branco */
```

### Sistema RGB

RGB significa:

- R → Red (vermelho)
- G → Green (verde)
- B → Blue (azul)

**Exemplos:**

```css
color: rgb(255, 0, 0); /* vermelho */
rgb(0, 255, 0)   /* verde */
rgb(0, 0, 255)   /* azul */
rgb(255, 255, 0) /* amarelo */
rgb(0, 0, 0)     /* preto */
rgb(255, 255, 255) /* branco */
```

### Sistema RGBA

O RGBA funciona como o RGB, porém adiciona transparência. A letra A significa Alpha.

O valor alpha varia de: `0` (totalmente transparente) até `1` (totalmente opaco).

**Exemplo:**

```css
background-color: rgba(255, 0, 0, 0.5);
/* fundo vermelho com 50% de transparência */
```

### Sistema HSL

HSL significa:

- H → Hue (matiz/tonalidade)
- S → Saturation (saturação)
- L → Lightness (luminosidade)

**Exemplo:**

```css
color: hsl(240, 100%, 50%);
/* azul */
```

### Sistema HSLA

O HSLA funciona como o HSL, porém adiciona transparência. A letra A significa Alpha.

O valor alpha varia de: `0` (totalmente transparente) até `1` (totalmente opaco).

**Exemplo:**

```css
background-color: hsla(240, 100%, 50%, 0.6);
/* fundo azul 60% opaco ou com 40% de transparência */
```

## Transparência e Opacidade

O CSS possui a propriedade `opacity` para definir a opacidade de um elemento. Ela controla o nível de transparência do elemento inteiro.

O valor possível para essa propriedade é de `0` (totalmente transparente) a `1` (totalmente opaco).

Aplicar essa propriedade em um elemento faz com que todos os elementos nele contidos herdem o valor aplicado a ele. Por exemplo, um texto de um parágrafo inserido em um elemento `div` herdará a opcidade definida para o elemento `div`.

**Exemplo:**

```html
<div>
    <p>Texto do primeiro parágrafo</p>
    <p class="destaque">Texto destacado</p>
</div>
```

```css
div {
    opacity: 0.5;
    color: blue;
}
p.destaque {
    opacity: 0.5;
}
```

Nesse exemplo, o `Texto do primeiro parágrafo` terá uma opacidade de 50% herdada do elemento `div` enquanto o texto `Texto destacado` terá uma opacidade de 25% (0.5 * 0.5 - 50% de 50%).

## Gradientes

Gradientes são transições suaves entre cores. É possível criar gradiente de cores para serem usados como imagem de fundo de elementos.

**Exemplo:**

```css
body {
    background-image: linear-gradient(to right, blue, purple);
}
```

**Resultado:**

- fundo da página com gradiente linear com transição do azul para o roxo da esquerda para a direita.

## Boas práticas no uso de cores

- **Utilize poucas cores** - Evite excesso de cores na página.
- **Mantenha padrão visual** - Utilize uma paleta de cores consistente.
- **Garanta contraste** - Textos devem ser fáceis de ler.
- **Pense na acessibilidade** - Usuários com deficiência visual precisam conseguir visualizar o conteúdo adequadamente.

**LEMBRE-SE:** O uso correto das cores melhora a aparência, a organização visual e a experiência do usuário em páginas WEB.
