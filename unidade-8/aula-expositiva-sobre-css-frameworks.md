# Aula expositiva sobre CSS - Frameworks

## Bootstrap

- Framework Front-end
- Responsivo, para projetos web e mobile
- Conjunto de Elementos HTML, CSS e JS
- Criado por um funcionário do Twitter

### Vantagens

- Reuso: velocidade de desenvolvimento
- Compatibilidade entre navegadores
- Comunidade grande e ativa

### Desvantagens

- Precisa alterar o HTML para aplicar as classes
- Carrega muito código que não será utilizado
- Designs parecidos: perda de identidade

## `container`

```html
<div class="container">
  <h1>Título do site</h1>
</div>
```

```css
.container {
  background: blue;
}
```

## `container-fluid`

```html
<div class="container-fluid">
  <h1>Título do site</h1>
</div>
```

```css
.container-fluid {
  background: blue;
}
```

## Grid - Bootstrap

**O sistema de grade Bootstrap 4 tem cinco classes:**

- `.col- (dispositivos extra pequenos - largura da tela inferior a 576px)`
- `.col-sm- (dispositivos pequenos - largura da tela igual ou superior a 576px)`
- `.col-md- (dispositivos médios - largura da tela igual ou superior a 768px)`
- `.col-lg- (dispositivos grandes - largura da tela igual ou superior a 992px)`
- `.col-xl- (dispositivos xlarge - largura da tela igual ou superior a 1200px)`

```html
<div class="container">
  <div class="row">
    <div class="col">Texto 1</div>
    <div class="col" style="background: red;">Texto 2</div>
    <div class="col">Texto 3</div>
  </div>
</div>
```

```css
.container {
  background: blue;
}
```

- Qualquer dispositivo menor que a configuração definida ele já irá alterar o layout do conteúdo

```html
<div class="container">
  <div class="row">
    <div class="col-sm">Texto 1</div>
    <div class="col-sm" style="background: red;">Texto 2</div>
    <div class="col-sm">Texto 3</div>
  </div>
</div>
```

```css
.container {
  background: blue;
}
```

## Colunas com largura fixa

```html
<div class="container">
  <div class="row">
    <div class="col-sm-2">Texto 1</div>
    <div class="col-sm" style="background: red;">Texto 2</div>
    <div class="col-sm">Texto 3</div>
  </div>
</div>
```

```css
.container {
  background: blue;
}
```

## Duas linhas no Bootstrap

```html
<div class="container">
  <div class="row">
    <div class="col-sm-2">Texto 1</div>
    <div class="col-sm" style="background: red;">Texto 2</div>
    <div class="col-sm">Texto 3</div>
  </div>
  <div class="row">
    <div class="col-sm-2">Texto 1</div>
    <div class="col-sm" style="background: yellow;">Texto 2</div>
    <div class="col-sm">Texto 3</div>
  </div>
</div>
```

```css
.container {
  background: blue;
}
```

## Ordenando colunas

- Você pode usar order-last
- Pode usar: order-1 (Nesse caso, as que não tem ordem aparecem primeiro, são order 0

```html
<div class="container">
  <div class="row">
    <div class="col-sm-2">Texto 1</div>
    <div class="col-sm" style="background: red;">Texto 2</div>
    <div class="col-sm order-last">Texto 3</div>
  </div>
</div>
```

```css
.container {
  background: blue;
}
```

## Alinhamento

**Pode usar:**

- `align-items-start`
- `align-items-center`
- `align-items-end`

**Pode usar:**

- `justify-content-start`
- `justify-content-end`
- `justify-content-around`
- `justify-content-between`

```html
<div class="container">
  <div class="row justify-content-center">
    <div class="col-sm-2" style="background: red;">Texto 1</div>
    <div class="col-sm-2" style="background: red;">Texto 2</div>
    <div class="col-sm-2" style="background: red;">Texto 3</div>
  </div>
</div>
```

```css
.container {
  background: blue;
}
```

## Estilos de Respostas

```html
<p class="text-danger">Esse texto representa perigo</p>
```

```html
<p class="bg-danger">Esse fundo representa perigo</p>
```

```html
<p class="bg-sucess">Esse fundo representa sucesso</p>
```

```html
<p class="bg-info">Esse fundo representa informação</p>
```

```html
<p class="bg-warning">Esse fundo representa alerta</p>
```

```html
<p class="bg-primary">Esse fundo representa primário</p>
```

## Alinhamento dos Textos

```html
<p class="text-center">Texto centralizado</p>
```

```html
<p class="text-uppercase">Texto maiúsculo</p>
```

```html
<p class="text-lowercase">Texto minúsculo</p>
```

## Botões

```html
<button type="button" class="btn">Básico</button>
<button type="button" class="btn btn-default">Padrão</button>
<button type="button" class="btn btn-primary">Primária</button>
<button type="button" class="btn btn-sucess">Sucesso</button>
<button type="button" class="btn btn-info">Informação</button>
<button type="button" class="btn btn-warning">Aviso</button>
<button type="button" class="btn btn-danger">Erro</button>
<button type="button" class="btn btn-link">Link</button>
```

## Grupo de Botões

```html
<div class="btn-group">
  <button type="button" class="btn btn-primary">Home</button>
  <button type="button" class="btn btn-primary">Quem somos</button>
  <button type="button" class="btn btn-primary">Contato</button>
</div>
```

```html
<div class="container">
  <div class="btn-group">
    <button type="button" class="btn btn-primary">Home</button>
    <button type="button" class="btn btn-primary">Quem somos</button>
    <button type="button" class="btn btn-primary">Contato</button>
  </div>

  <div class="btn-group btn-group-lg">
    <button type="button" class="btn btn-primary">Home</button>
    <button type="button" class="btn btn-primary">Quem somos</button>
    <button type="button" class="btn btn-primary">Contato</button>
  </div>

  <div class="btn-group btn-group-sm">
    <button type="button" class="btn btn-primary">Home</button>
    <button type="button" class="btn btn-primary">Quem somos</button>
    <button type="button" class="btn btn-primary">Contato</button>
  </div>

  <div class="btn-group btn-group-xs">
    <button type="button" class="btn btn-primary">Home</button>
    <button type="button" class="btn btn-primary">Quem somos</button>
    <button type="button" class="btn btn-primary">Contato</button>
  </div>
</div>
```

## Botões – Vertical e Justificado

```html
<div class="container">
  <div class="btn-group btn-group-justifed">
    <button type="button" class="btn btn-primary">Apple</button>
    <button type="button" class="btn btn-primary">Samsung</button>
    <button type="button" class="btn btn-primary">Sony</button>
  </div>
</div>
```

## Botão Dropdown

```html
<div class="btn-group">
  <button type="button" class="btn btn-primary">Sony</button>
  <button
    type="button"
    class="btn btn-primary dropdown-toggle dropdown-toggle-split"
    data-toggle="dropdown"
  >
    <span class="caret"></span>
  </button>

  <div class="dropdown-menu">
    <a href="#" class="dropdown-item">Tablet</a>
    <a href="#" class="dropdown-item">Smartphone</a>
  </div>
</div>
```

## Icones - `glyphicon`

```html
<p>
  Icone de envelope:
  <span class="glyphicon glyphicon-envelope"></span>
</p>

<p>
  Link com icone de envelope:
  <a href="#">
    <span class="glyphicon glyphicon-envelope"></span>
  </a>
</p>

<p>
  Icone de busca:
  <span class="glyphicon glyphicon-search"></span>
</p>

<p>
  Botão com icone de busca:
  <button type="button" class="btn btn-default">
    <span class="glyphicon glyphicon-search"></span>
  </button>
</p>

<p>
  Botão de busca com estilo:
  <button type="button" class="btn btn-info">
    <span class="glyphicon glyphicon-search"></span>
  </button>
</p>

<p>
  Icone de impressora:
  <span class="glyphicon glyphicon-print"></span>
</p>
```

## Alertas

```html
<div class="alert alert-sucess">
  <strong>Sucesso!</strong> Esse alerta indica sucesso.
</div>

<div class="alert alert-info">
  <strong>Informação!</strong> Esse alerta indica informação.
</div>

<div class="alert alert-warning">
  <strong>Aviso</strong> Esse alerta indica aviso.
</div>

<div class="alert alert-danger">
  <strong>Erro!</strong> Esse alerta indica erro.
</div>
```

## Imagens

```html
<img src="./assets/images/image.png" alt="image" class="rounded" />

<img src="./assets/images/image.png" alt="image" class="img-thumbnail" />

<img src="./assets/images/image.png" alt="image" class="rounded-circle" />
```

## Imagem Responsiva

```html
<img src="./assets/images/image.png" alt="image" class="img-fluid" />
```

## Tabela

```html
<table class="table">
  <thead>
    <tr>
      <th>Primeiro nome</th>
      <th>Último nome</th>
      <th>E-mail</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <th>Pedro</th>
      <th>Euzebio</th>
      <th>pedroeuzebio@gmail.com</th>
    </tr>
  </tbody>
</table>
```

```html
<table class=".table-striped">
  <thead>
    <tr>
      <th>Primeiro nome</th>
      <th>Último nome</th>
      <th>E-mail</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <th>Pedro</th>
      <th>Euzebio</th>
      <th>pedroeuzebio@gmail.com</th>
    </tr>
  </tbody>
</table>
```
