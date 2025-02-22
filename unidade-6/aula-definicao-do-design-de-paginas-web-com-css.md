# Aula - Definição do Design de Páginas Web com CSS

## Sem Flexbox

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;
}
```

## Com FlexBox

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;
}
```

## `flex-direction` - padrão

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
  flex-direction: row;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;
}
```

## `flex-direction: column`

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
  flex-direction: column;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;
}
```

## `row-reverse`

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
  flex-direction: row-reverse;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;
}
```

## `column-reverse`

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
  flex-direction: column-reverse;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;
}
```

## `flex: 1`

- O flex 1 fará com que os dois elementos se dividam na tela de forma igual

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;

  flex: 1;
}
```

## `flex: 2`

- A terceira div terá o dobro de tamanho das outras divs

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div id="terceira">Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;

  flex: 1;
}

#container div#terceira {
  flex: 2;
}
```

## Width - barra de rolagem

- Perceba que como a largura das divs é grande, vai gerar uma barra de rolagem e não vai quebrar em duas linhas

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;

  width: 1280px;
}
```

## `flex-wrap`

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
  flex-wrap: wrap;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;

  width: 1280px;
}
```

## `flex-flow: row wrap` / `column wrap`

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
  flex-wrap: row wrap;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;

  width: 1280px;
}
```

## Alinhamento

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;

  /* Alinha na horizontal */
  justify-content: center;

  /*Alinha na vertical */
  align-items: center;

  height: 768px;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;

  width: 200px;
  height: 200px;
}
```

## Alinhamento - Column

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
  flex-column: column;

  /* Alinha na horizontal */
  justify-content: center;

  /*Alinha na vertical */
  align-items: center;

  height: 768px;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;

  width: 200px;
  height: 200px;
}
```

## `justify-content: flex-start`

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
  flex-column: row;

  /* Alinha na horizontal */
  justify-content: flex-start;

  /*Alinha na vertical */
  align-items: center;

  height: 768px;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;

  width: 200px;
  height: 200px;
}
```

## `space-around`

- O espaçamento ao redor deles fica o mesmo

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
  flex-column: row;

  /* Alinha na horizontal */
  justify-content: space-around;

  /*Alinha na vertical */
  align-items: center;

  height: 768px;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;

  width: 200px;
  height: 200px;
}
```

## `space-between`

- O espaçamento entre eles fica o mesmo

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
  background: #ccc;

  display: flex;
  flex-column: row;

  /* Alinha na horizontal */
  justify-content: space-between;

  /*Alinha na vertical */
  align-items: center;

  height: 768px;
}

#container div {
  background: blueviolet;
  padding: 10px;
  margin: 10px;
  font-size: 20px;

  width: 200px;
  height: 200px;
}
```

## `align-self: flex-start` / `flex-end` / `center`

- Um alinhamento específico para uma div

```html
<div id="container">
  <div>Primeira</div>
  <div id="segunda">Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
 background: #ccc;

 display: flex;
 flex-column: row;

 /* Alinha na horizontal */
 justify-content: center

 /*Alinha na vertical */
 align-items: center;

 height: 768px;
}

#container div {
 background: blueviolet;
 padding: 10px;
 margin: 10px;
 font-size: 20px;

 width: 200px;
 height: 200px;
}

#container div#segunda {
 align-self: flex-start;
}
```

## `order`

- As que não foram especificadas são order 0, por isso a div 3 aparece primeiro

```html
<div id="container">
  <div id="primeira">Primeira</div>
  <div id="segunda">Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
 background: #ccc;

 display: flex;
 flex-column: row;

 /* Alinha na horizontal */
 justify-content: center

 /*Alinha na vertical */
 align-items: center;

 height: 768px;
}

#container div {
 background: blueviolet;
 padding: 10px;
 margin: 10px;
 font-size: 20px;

 width: 200px;
 height: 200px;
}

#container div#primeira {
 order: 1;
}

#container div#segunda {
 order: 2
}
```

- Caso queira forçar a posição antes da 0

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div id="terceira">Terceira</div>
</div>
```

```css
#container {
 background: #ccc;

 display: flex;
 flex-column: row;

 /* Alinha na horizontal */
 justify-content: center

 /*Alinha na vertical */
 align-items: center;

 height: 768px;
}

#container div {
 background: blueviolet;
 padding: 10px;
 margin: 10px;
 font-size: 20px;

 width: 200px;
 height: 200px;
}

#container div#terceira {
 order: -1;
}
```

## `align-content: flex-start` / `flex-end` / `space around` / `space-between`

- Funciona quando tem um wrap

```html
<div id="container">
  <div>Primeira</div>
  <div>Segunda</div>
  <div>Terceira</div>
</div>
```

```css
#container {
 background: #ccc;

 display: flex;
 flex-column: row;

 /* Alinha na horizontal */
 justify-content: center

 /*Alinha na vertical */
 align-items: center;

 height: 768px;

 flex-wrap: wrap;
 align-content: flex-start;
}

#container div {
 background: blueviolet;
 padding: 10px;
 margin: 10px;
 font-size: 20px;

 width: 200px;
 height: 200px;
}
```

## Grid

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

## Formatação de todos os itens

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

## `grid-template-columns: auto`

- Distribui de forma igual todos os itens na linha

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: auto;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

## `grid-template-columns`

- Especifica tamanho para cada coluna

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: 200px 500px 100px;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

## `grid-gap`

- Espaçamento de linha e coluna entre as divs

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

- Primeiro ele define a coluna de 200px, depois separa o restante do espaço da linha entre três colunas

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, 1fr) 200px;
  grid-gap: 10px;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

## `grid-column-gap`

- Gap só das colunas

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, 1fr) 200px;
  grid-column-gap: 10px;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

## `grid-row-gap`

- Gap só das linhas

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, 1fr) 200px;
  grid-row-gap: 10px;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

## `grid-auto-rows`

- Altura das linhas

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: auto auto auto;
  grid-auto-rows: 100px;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

## `justify-content: center` / `start` / `end`

- Alinhamento horizontal dos itens do container

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, 1fr) 200px;
  grid-gap: 100px;
  justify-content: center;

  background: blue;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

## `justify-content: space-around`

- Alinhamento com o mesmo espaço entre e ao redor das colunas

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, 1fr) 200px;
  grid-gap: 100px;
  justify-content: space-around;

  background: blue;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

## `justify-content: space-between`

- Alinhamento com o mesmo espaço entre as colunas

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, 1fr) 200px;
  grid-gap: 100px;
  justify-content: space-between;

  background: blue;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

## `align-items: center` / `start` / `end`/ `space-between` / `space-around`

- Alinhamento vertical dos itens em cada linha do container

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, 1fr) 200px;
  grid-gap: 100px;
  align-items: center;

  background: blue;

  height: 768px;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

## `align-content: center` / `start` / `end`

- Alinhamento vertical de todos os itens do container

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, 1fr) 200px;
  grid-gap: 100px;
  align-content: center;

  background: blue;

  height: 768px;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

## `align-content` e `justify-content`

- Alinhamento horizontal e vertical de todos os itens

```html
<div id="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, 1fr) 200px;
  grid-gap: 100px;
  align-content: center;
  justify-content: center;

  background: blue;

  height: 768px;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}
```

## Mesclando colunas: `grid-column-start` / `end`

```html
<div id="container">
  <div class="item item1">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, auto);
  grid-gap: 10px;

  background: blue;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}

.item1 {
  grid-column-start: 1;
  grid-column-end: 3;
}
```

## Mesclando colunas: `grid-row-start` / `end`

```html
<div id="container">
  <div class="item item1">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, auto);
  grid-gap: 10px;

  background: blue;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}

.item1 {
  grid-row-start: 1;
  grid-row-end: 3;
}
```

## `grid-column` e `grid-row`

```html
<div id="container">
  <div class="item item1">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-columns: repeat(3, auto);
  grid-gap: 10px;

  background: blue;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}

.item1 {
  grid-row: 1/3;
  grid-column: 1/3;
}
```

## Template Area

```html
<div id="container">
  <div class="item item1">1</div>
  <div class="item item2">2</div>
  <div class="item item3">3</div>
  <div class="item item4">4</div>
</div>
```

```css
#container {
  display: grid;
  grid-template-area:
    "item1 item1"
    "item2 item3"
    "item4 item4";
  grid-gap: 10px;

  background: blue;
}

.item {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}

.item1 {
  grid-area: item1;
}

.item2 {
  grid-area: item2;
}

.item1 {
  grid-area: item2;
}

.item3 {
  grid-area: item4;
}
```

## Exemplo Layout

```html
<div id="container">
  <header>1</header>
  <main>2</main>
  <aside>3</aside>
  <footer>4</footer>
</div>
```

```css
#container {
  display: grid;
  grid-template-area:
    "header header"
    "main aside"
    "footer footer";
  grid-gap: 10px;

  background: blue;
}

header,
main,
aside,
footer {
  background: red;
  padding: 10px;
  border-radius: 8px;
  font-size: 20px;
  color: #fff;
}

header {
  grid-area: header;
}

main {
  grid-area: main;
}

aside {
  grid-area: aside;
}

footer {
  grid-area: footer;
}
```

## Grid dentro de Grid - Layout

```html
<div id="app">
  <header>
    Cabeçalho
    <nav>
      <img src="./assets/images/logo.png" alt="Logo" />

      <ul>
        <li>
          <a href="#">Item</a>
          <a href="#">Item</a>
          <a href="#">Item</a>
        </li>
      </ul>
    </nav>
  </header>

  <main>Conteúdo principal</main>

  <aside>Conteúdo lateral</aside>

  <footer>Rodapé</footer>
</div>
```

```css
#app {
  display: grid;
  gap: 20px;
  grid-template-area:
    "header header"
    "main aside"
    "footer footer";
}

header,
main,
aside,
footer {
  background: red;
  padding: 16px;
  border-radius: 8px;
  font-size: 18px;
  color: white;
}

header {
  display: grid;
  gap: 20px;
  grid-template-area: "logo menu";
  grid-area: header;
}

img,
ul {
  background: blue;
  padding: 16px;
  border-radius: 8px;
  font-size: 18px;
  color: white;
}

img {
  grid-area: logo;
}

ul {
  grid-area: menu;
}

main {
  grid-area: main;
}

aside {
  grid-area: aside;
}

footer {
  grid-area: footer;
}
```
