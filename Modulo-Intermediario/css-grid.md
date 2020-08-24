# CSS Grid - display: grid

Da mesma forma que o flex, o grid também é baseado no conceito de linhas e colunas:

```css
grid-column-start: <number> | <name> | span <number> | span <name> | auto;
grid-column-end: <number> | <name> | span <number> | span <name> | auto;
grid-row-start: <number> | <name> | span <number> | span <name> | auto;
grid-row-end: <number> | <name> | span <number> | span <name> | auto;
```

Podemos resumir com:

```css
grid-column: <start-line> / <end-line>;
grid-row: <start-line> / <end-line>;
```

Podemos utilizar a unidade `fr` permite que você defina o tamanho de uma trilha como uma fração do espaço livre do contêiner da grade. Por exemplo, isso definirá cada item com um terço da largura do recipiente da grade:

```css
grid-template-columns: 1fr 1fr 1fr;
```
 
No grid, podemos utilizar o `justify-self` e o `align-selft` para posicionar nossos items:

```css
justify-self: start | end | center | stretch;
```

Um truque é utilizar o `repeat` para ter itens com o tamanho exato que precisamos:

```css

/* Vamos criar nosso grid com 12 linhas e 12 colunas */

main {
  display: grid;
  grid-template-rows: repeat(12, 1fr);
  grid-template-columns: repeat(12 ,1fr);
  width: 100%;
  height: 100vh;
}

/* Podemos utilizar o grid-area para posicionar exatamente onde queremos os nossos items */

/* grid-area: <linha-inicio> / <coluna-inicio> / <linha-fim> / <coluna-fim> */

section {
  grid-area: 2 / 2 / 10 / 12;
}
```

Para colocar um espaço entre os itens, podemos utilizar o `gap`

```css
main {
  gap: 10px;
}
```
