# Aula expositiva sobre CSS - Variáveis e Responsividade

## Variáveis CSS

- Facilita a leitura e edição do CSS
- Melhora o entendimento do código
- Diminui os erros

```css
:root {
  --cor-de-fundo: #d94218;
}

body {
  background: var(--cor-de-fundo);
}
```

## Responsividade

- O site vai detectar o tamanho da tela e vai se ajustar ao tamanho
- Você pode desenhar o site para o computador, mas já pensando em como ele vai funcionar no celular
- Conteúdo legível em qualquer tamanho de tela
- Evitar barras de rolagem na horizontal

## Responsividade - Layout adaptativo e Layout responsivo

- Em um layout adaptativo você cria versões diferentes de acordo com o dispositivo que ele está executando, para cada dispositivo ele vai se adaptando ao tamanho da tela, de acordo com as pre definições de tamanho que você criou
- Já em um site responsivo ele vai se ajustando à tela de acordo com o tamanho
- O ideal é que o site seja adaptativo e responsivo, ou seja, ele vai se adaptando ao tamanho da tela de acordo com os tamanhos que você definiu inicialmente, e entre cada um dos tamanho ele fica responsivo

```html
<meta name="viewport" content="width=device-width, initial-scale1.0" />
```

- Essa tag já vai fazer com que em dispositivos móveis o conteúdo seja rendererizado de acordo com o tamanho da tela, criando uma responsividade

## Propriedades de Imagem

```html
<img src="./assets/image.png" alt="image" />
```

```css
img {
  width: 500px;
  height: 500px;
}
```

- Imagem achatada

## `object-fit`

```html
<img src="./assets/image.png" alt="image" />
```

```css
img {
  width: 500px;
  height: 500px;
  object-fit: cover;
}
```

- Tenta ajustar a imagem para caber na div, mantendo as proporções
- Note que aconteceu um recorte da imagem

```css
img {
  width: 500px;
  height: 500px;
  object-fit: contain;
}
```

- Ajusta a imagem dentro da div, sem cortar e mantendo as proporções

```css
img {
  width: 500px;
  height: 500px;
  object-fit: none;
}
```

- Manteve o tamanho da imagem, fazendo um recorte na parte que é possível exibir

## `@media`

- Usando `Media` você consegue definir CSS alternativos de acordo com uma propriedade que você passou
- No exemplo: Até uma largura máxima de `600px` tenha a cor de fundo azul, depois disso é aplicado o padrão do `body`

```css
body {
  background: black;
}

@media (max-width: 600px) {
  body {
    background: blue;
  }
}
```

## `min` e `max`

- Se a largura da tela for maior que `800px`, a imagem vai ocupar `50%` da tela

```html
<img src="./assets/image.png" alt="image" />
```

```css
img {
  width: min(50%, 400px);
}
```

- Se a largura da tela for menor que `800px`, a imagem vai ter uma largura fixa de `400px`

```html
<img src="./assets/image.png" alt="image" />
```

```css
img {
  width: max(50%, 400px);
}
```

## Responsividade - CSS `calc`

- A propriedade `Calc` vai aplicar uma largura de pegando os `100%` da tela, sempre menos `20px`
- Isso vai garantir que esse espaçamento seja o mesmo em qualquer resolução

```html
<div id="app"></div>
```

```css
#app {
  width: calc(100% - 20px);
  height: 500px;
  background: blue;
}
```
