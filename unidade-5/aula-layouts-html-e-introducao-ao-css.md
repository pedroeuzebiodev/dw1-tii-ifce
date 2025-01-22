# Aula - Layouts HTML e Introdução ao CSS

## CSS - Cascading Style Sheets

- Separar visual da estrutura e conteúdo

## CSS - Cascata

- O inline prevalece entre as outras opções de CSS

```html
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>

    <style>
      /*CSS Incorporado*/
      h1 {
        color: red;
      }
    </style>
  </head>
  <body>
    <!-- CSS Inline -->
    <h1 style="color: blue;">Hello World</h1>
  </body>
</html>
```

```css
/* CSS Externo */
h1 {
  color: yellow;
}
```

## CSS - Especificidade

```html
<p class="blue">Esse é um texto</p>
<p>Esse é outro texto</p>
```

```css
p {
  color: red;
}

.blue {
  color: yellow;
}
```

## CSS - Herança

```html
<h1>Título</h1>
```

```css
:root {
  font-size: 62.5%; /* 10px */
}

/* Todos os elementos de texto dentro da tag <body> será 16px */
body * {
  font-size: 1.6rem;
}
```

## Bordas

```html
<div class="box"></div>
```

```css
.box {
  width: 200px;
  height: 200px;

  background: blue;

  border-radius: 8px;
}
```

## Degradê

```html
<div class="box"></div>
```

```css
.box {
  width: 200px;
  height: 200px;

  background: linear-gradient(white, blue);

  border-radius: 8px;
}
```

## Animação

```html
<div class="box"></div>
```

```css
.box {
  width: 200px;
  height: 200px;

  background: blue;

  border-radius: 8px;

  position: absolute;

  animation-name: move;
  animation-delay: 2s;
  animation-duration: 10s;
  animation-iteration-count: infinite;
}

@keyframes move {
  0% {
    left: 0;
    top: 0;
  }

  25% {
    left: 500px;
    top: 0;
  }

  50% {
    top: 500px;
    left: 500px;
  }

  75% {
    top: 500px;
    left: 0;
  }

  100% {
    left: 0;
    top: 0;
  }
}
```

## Sombras

- O primeiro valor é a distância da sombra horizontal, o segundo a distância vertical, o terceiro é o esfumaçamento da sombra e o quarto é a cor da sombra

```html
<div class="box"></div>

<p>Tem com sombra</p>
```

```css
.box {
  width: 200px;
  height: 200px;

  background: blue;

  border-radius: 8px;

  box-shadow: 4px 4px 4px black;
}

p {
  color: green;

  text-shadow: 4px 4px 4px black;
}
```

## Transição

- No transition o primeiro item diz que as propriedades serão aplicadas em
  todas as transições, depois é o tempo e depois que esse tempo será linear(constante)

```html
<div class="box"></div>
```

```css
.box {
  width: 200px;
  height: 200px;

  background: blue;

  border-radius: 8px;

  transition: all 0.3s;
}

.box:hover {
  background: red;
}
```

## Margin e Padding

- Padding é o espaço entre o conteúdo e a borda
- Margin é o espaço fora da borda
