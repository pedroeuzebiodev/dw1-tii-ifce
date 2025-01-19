# Aula - Formulários e Tabelas

## Formulários

- Um formulário HTML é usado para coletar a entrada do usuário
- A entrada do usuário é na maioria das vezes enviado para um servidor para processamento

```html
<form>
  <fieldset>
    <legend>Formulário</legend>

    <label for="email">E-mail</label>
    <input type="email" name="email" id="email" />

    <label for="senha">Senha</label>
    <input type="password" name="senha" id="senha" />

    <button>Enviar</button>
  </fieldset>
</form>
```

## GET x Post

- **Notas sobre o GET:**
  - Acrescenta os dados do formulário à URL, em pares nome/valor
  - NUNCA use GET para enviar dados confidenciais! (os dados do formulário enviado são visíveis no URL!)
  - O comprimento de um URL é limitado (2048 caracteres)
  - O GET é bom para dados não seguros, como cadeias de caracteres de consulta no Google
- **Notas no POST:**
  - Acrescenta os dados do formulário dentro do corpo da solicitação HTTP (o enviado os dados do formulário não são mostrados no URL)
  - O POST não tem limitações de tamanho e pode ser usado para enviar grandes quantidades de dados

## Inputs

- Diferentes tipos
  - Texto, número, data etc
- Devem ter um nome
- Devem ter um rótulo (_label_)

```html
<input type="text" name="texto" />
<input type="number" name="numero" />
<input type="date" name="data" />
```

## Rótulos (_labels_)

- O atributo da tag deve ser igual ao atributo do elemento para uni-los

```html
<label for="email">E-mail</label> <br />
<input type="email" name="email" id="email" />
```

ou

```html
<label>
  <span>E-mail</span>
  <input type="email" name="email" />
</label>
```

## **Radio Buttons**

```html
<input type="radio" name="tech" id="html" /> <label for="html">HTML</label>
<input type="radio" name="tech" id="css" /> <label for="css">CSS</label>
<input type="radio" name="tech" id="js" /> <label for="js">JS</label>
```

## **Caixas de seleção**

- O `input type="checkbox"` define uma caixa de seleção

```html
<input type="checkbox" name="techs" id="html" value="HTML" />
<label for="html">HTML</label>
<input type="checkbox" name="techs" id="css" value="CSS" />
<label for="css">CSS</label>
<input type="checkbox" name="techs" id="js" value="JS" />
<label for="js">JS</label>
```

## **Botões**

```html
<input type="submit" value="Enviar" />
```

ou

```html
<button type="submit">Enviar</button>
```

## `<button>`

```html
<button type="submit">Enviar</button>
```

## Atributo Name do Input

- Se você clicar no botão “Enviar”, os dados do formulário serão enviados para uma página
- Observe que o valor do campo “Nome” não será enviado, porque o elemento de entrada não tem atributo `name`

```html
<form>
  <label for="nome">Nome</label> <br />
  <input type="nome" name="nome" id="nome" />
  <button type="submit">Enviar</button>
</form>
```

## `<select>`

- O elemento define uma lista suspensa

```html
<label for="area">Selecione sua área de atuação: </label>
<select id="area" name="area">
  <option value="front-end">Front-end</option>
  <option value="back-end">Back-end</option>
  <option value="full-stack">Full Stack</option>
</select>
```

- O atributo size vai mostrar a quantidade de valores visíveis

```html
<label for="area">Selecione sua área de atuação: </label>
<select id="area" name="area" size="2">
  <option value="front-end">Front-end</option>
  <option value="back-end">Back-end</option>
  <option value="full-stack">Full Stack</option>
</select>
```

- O atributo multiple permite selecionar vários elementos

```html
<label for="area">Selecione sua área de atuação: </label>
<select id="area" name="area" size="2" multiple>
  <option value="front-end">Front-end</option>
  <option value="back-end">Back-end</option>
  <option value="full-stack">Full Stack</option>
</select>
```

## **`<textarea>`**

- O elemento `<textarea>` define um campo de entrada de várias linhas

```html
<label for="sobre">Fale um pouco sobre você: </label>
<textarea name="sobre" id="sobre" cols="30" rows="10"></textarea>
```

## `<fieldset>` e `<legend>`

- O elemento `fieldset` é usado para agrupar dados relacionados em um formulário, e o `legend` define uma legenda para o elemento `fieldset`

```html
<form>
  <fieldset>
    <legend>Formulário</legend>
  </fieldset>
</form>
```

## `<password>`

- O `input type="password"` define um campo de senha
- Os caracteres em um campo de senha são mascarados (mostrados como asteriscos ou círculos)

```html
<label for="senha">Digite sua senha: </label>
<input type="password" name="senha" id="senha" />
```

## Campo Data

- O `input type="date"` é usado para campos de entrada que devem conter uma data

```html
<label for="senha">Digite sua data de aniversário: </label>
<input type="date" name="data-de-aniversario" id="data-de-aniversario" />
```

## **Campo de Data e Hora**

```html
<label for="senha">Digite o horário de hoje: </label>
<input type="datetime-local" name="horario-de-hoje" id="horario-de-hoje" />
```

## **Campo de E-mail**

- O `input type="email"` é usado para campos de entrada que devem conter um endereço de email

```html
<label for="email">Digite seu e-mail: </label>
<input type="email" name="email" id="email" />
```

## Botão Submit com Imagem

```html
<input
  type="image"
  src="imagem-submit"
  alt="Submit Button"
  width="32px"
  height="32px"
/>
```

## Upload de Arquivos

- Mostra um campo de seleção de arquivo que permite que um arquivo seja escolhido para upload

```html
<label for="file">Selecione um arquivo: </label>
<input type="file" id="file" name="file" />
```

## Restrições de Datas

```html
<label for="senha">Digite sua data de aniversário: </label>
<input
  type="date"
  name="data-de-aniversario"
  id="data-de-aniversario"
  min="2000-01-02"
/>
```

```html
<label for="senha">Digite sua data de aniversário: </label>
<input
  type="date"
  name="data-de-aniversario"
  id="data-de-aniversario"
  max="1980-01-01"
/>
```

```html
<label for="senha">Digite sua data de aniversário: </label>
<input type="month" name="data-de-aniversario" id="data-de-aniversario" />
```

## Restrição de números

```html
<label for="number">Selecione um número: </label>
<input type="number" id="number" name="number" min="1" max="20" />
```

## Input de Telefone

```html
<label for="tel">Digite o seu número de telefone: </label>
<input
  type="tel"
  id="tel"
  name="tel"
  placeholder="123-45-678"
  pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}"
/>
```

## Input de Tempo

```html
<label for="tempo">Selecione um horário: </label>
<input type="time" id="tempo" name="tempo" />
```

## Campo do tipo URL

```html
<label for="url">Digite a URL de um site: </label>
<input type="url" id="url" name="url" />
```

## Campo de semana

```html
<label for="semana">Selecione uma semana: </label>
<input type="week" id="semana" name="semana" />
```

## Campo somente leitura

```html
<label for="nome">Nome: </label>
<input type="text" id="nome" name="nome" value="Pedro" readonly />
```

## Tamanho

```html
<input type="text" id="text" name="text" size="50" />
```

## Tamanho Máximo

```html
<input type="text" id="text" name="text" size="50" maxlength="30" />
```

## Campo desabilitado

```html
<label for="sobrenome">Sobrenome: </label>
<input type="text" id="sobrenome" name="sobrenome" value="Euzebii" disabled />
```

## Campo que aceita múltiplos arquivos

```html
<label for="file">Selecione um ou vários arquivos: </label>
<input type="file" id="file" name="file" multiple />
```

## Tornar campo obrigatório

```html
<label for="email">Digite seu e-mail: </label>
<input type="email" id="email" name="email" required />
```

## Manter o foco em um input

```html
<label for="email">Digite seu e-mail: </label>
<input type="email" id="email" name="email" autofocus />
```

## Definir o autocomplete

```html
<label for="email">Digite seu e-mail: </label>
<input type="email" id="email" name="email" autocomplete />
```

## Não validar um campo

```html
<label for="email">Digite seu e-mail: </label>
<input type="email" id="email" name="email" formnovalidate="formnovalidate" />
```

## Não validar os dados de formulário

```html
<form novalidate>
  <label for="email">Digite seu e-mail: </label>
  <input type="email" id="email" name="email" formnovalidate="formnovalidate" />
  <button type="submit">Enviar</button>
</form>
```

## Tabelas

- Apresentar dados tabulares
- Não deve ser usada para layout

```html
<table>
  <thead>
    <tr>
      <th>ID</th>
      <th>E-mail</th>
      <th>Senha</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <th>1</th>
      <th>pedroeuzebio@gmail.com</th>
      <th>12345678</th>
    </tr>
    <tr>
      <th>2</th>
      <th>ataslanmonteiro@gmail.com</th>
      <th>87654321</th>
    </tr>
  </tbody>
</table>
```
