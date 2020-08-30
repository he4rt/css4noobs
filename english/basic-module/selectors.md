# Seletores - O que diabos é isso?

Seletor simplesmente é você informar quais elementos se aplicam a uma regra (estilo) definida por você, **devemos ficar atento pois o seletor pega todos os elementos que ele encontra.**

## Seletor com elemento

Para selecionar qualquer elemento pela tag dele, simplesmente coloque tag, exemplo:

No HTML

```html
<div id="exemplo"></div>
```

No CSS

```css
div {
  width: 100px;
  height: 100px;
  background-color: red;
}
```

## Seletor com ID

Para selecionar qualquer elemento pelo o id dele, devemos colocar uma cerquilha `#` antes de colocar qual o id do elemento, segue exemplo abaixo:

No HTML

```html
<div id="exemplo"></div>
```

No CSS

```css
#exemplo {
  width: 100px;
  height: 100px;
  background-color: red;
}
```

## Seletor com Classe

Para selecionar qualquer elemento pela classe, devemos colocar um ponto final `.` antes de referenciar pela classe, segue exemplo:

No HTML

```html
<div class="exemplo"></div>
```

No CSS

```css
.exemplo {
  width: 100px;
  height: 100px;
  background-color: red;
}
```

<p align="center">
  Importante dizer que ira pegar todos os elementos com a classe referenciada.
</p>

## Seletor com atributo

Não estamos presos a somente selecionar pela classe ou id do elemento, podemos tambem selecionar pelo atributo usando colchetes `[ ]` colocando o nome do atributo e opcionalmente um operador seguido pelo valor dele.

No HTML

```html
<div class="exemplo">
  <button type="button"></button>
</div>
```

No CSS

```css
/* Estamos pegando todos os elementos que tem o atributo type com valor "button" */
[type='button'] {
  width: 100px;
  height: 100px;
  background-color: red;
}
```

## Seletor com pseudo-classes

Uma pseudo-classe basicamente é uma classe que automaticamente o navegador adiciona em certas ocasiões, por exemplo quando você clica em botão, passa por cima de elemento, visita algum link.

Para usarmos pseudo-classe vamos adicionar na frente do seletor dois pontos `:` e a pseudo-classe, exemplo:

No HTML

```html
<div class="exemplo"></div>
```

No CSS

```css
/* Hover é a pseudo classe para quando a mouse passa sobre o elemento */
.exemplo:hover {
  background-color: blue;
}
```

A lista de pseudo-classes são as abaixo:

- :link
- :visited
- :active
- :hover
- :focus
- :first-child
- :last-child
- :nth-child
- :nth-last-child
- :nth-of-type
- :first-of-type
- :last-of-type
- :empty
- :target
- :checked
- :enabled
- :disabled

## Para finalizar

Podemos combinar todos esses seletores, por exemplo podemos pegar todos elementos div com a class vermelho:

No HTML

```html
<div class="vermelho"></div>
<div class="vermelho"></div>
<div class="vermelho"></div>
<button class="vermelho">
  Opa isso aqui não vai <span id="font_red">pegar</span>.
</button>
```

No CSS

```css
/* O nosso elemento button não vai entrar no estilo abaixo, pois ele não é uma div */

div.vermelho {
  background-color: red;
}

/* Estamos pegando todos os elementos com tag span que tenha a ID font_red */

span#font_red {
  color: red;
}

/* Vamos pegar agora todos os button dentro da div */

div button {
  background-color: blue;
}
```
