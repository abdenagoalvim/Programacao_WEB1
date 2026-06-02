# CSS - Posicionando Elementos

A propriedade `position` no CSS define como um elemento é posicionado dentro da página. Ela permite criar desde pequenos ajustes visuais até menus fixos ou detalhes flutuantes. Para definir a distância exata, ela é combinada com as propriedades `top`, `right`, `bottom` e `left`.

**Os principais valores da propriedade `position` são:**

- `static` **(Padrão)**: É o comportamento natural de qualquer elemento no HTML. Ele segue o fluxo normal da página e ignora as propriedades `top`, `right`, `bottom` e `left`.
- `relative`: Move o elemento em relação à sua posição original na página. O espaço original que ele ocupava continua reservado no layout.
- `absolute`: Remove o elemento do fluxo normal e o posiciona em relação ao seu elemento pai mais próximo (que possua qualquer valor de `position` diferente de `static`).
- `fixed`: Fixa o elemento em um local exato da tela. Ele não se move ao rolar a barra de rolagem (ex: botões **"Voltar"**).
- `sticky`: Funciona como um elemento **"relativo"** até atingir um ponto específico da tela. Ao rolar, ele **"gruda"** e se comporta como **"fixo"**.

**Exemplo:**

**CSS**
```css
.cartao {
    position: relative;
    width: 400px;
    height: 400px;
    background-color: #e7e7e7;
}

.desconto {
    position: absolute;
    top: 25px; 
    right: 25px; 
    background-color: #d70000;
    color: #fff;
    padding: 7px 13px;
}
```