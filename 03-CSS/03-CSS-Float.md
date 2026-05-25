# CSS - Propriedade Float

A propriedade `float` no CSS serve para flutuar elementos (como imagens, blocos...) "empurrando-os" para a esquerda ou para a direita, permitindo que outros elementos o contornem (fluam ao seu redor). Em outras palavras, a propriedade `float` retira um elemento do seu fluxo normal colocando-o ao longo do lado esquerdo ou direito do seu container.

## Valore possíveis para a propriedade `float`

- `left`: flutuar para a esquerda.
- `right`: flutuar para a direita.
- `none`: não flutuar.

**Exemplo:**

**HTML**
```html
<div>
    <img src="imagem.jpg" alt="Exemplo de imagem">
    <p>
        lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
        Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
        Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
    </p>
</div>
```

**CSS**
```css
img {
    float: left;
    margin-right: 10px;
    width: 50%;
}

p {
    float: none;

}
```
**ATENÇÃO:** Você teve ter uma imagem chamada `imagem.jpg` na mesma pasta do arquivo `.html`.

## Como "limpar" o Float (`clear`)

Quando um elemento usa a propriedade `float`, ele se *"desprende"* do fluxo natural da página. Isso faz com que os elementos seguintes fiquem desalinhados ou invadam o espaço do elemento flutuante.

Para impedir que elementos fiquem ao lado de um `float`, usamos a propriedade `clear`.

- `clear: left;`  - Nenhum elemento flutuante à esquerda.
- `clear: right;` - Nenhum elemento flutuante à direita.
- `clear: both;`  - Limpa flutuações de ambos os lados (o mais recomendado).

**Exemplo:**

**HTML**
```html
<div class="caixa-1">Caixa 1 (Esquerda)</div>
<div class="caixa-2">Caixa 2 (Direita)</div>
<p class="texto-inferior">Este texto deve ficar ABAIXO das duas caixas.</p>
```

**CSS**
```css
.caixa-1 {
    float: left;
    width: 200px;
}

.caixa-2 {
    float: right;
    width: 200px;
}

.texto-inferior {
    clear: both;
}
```
