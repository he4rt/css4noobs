# Specificity - Especificidade

## Conceito
A especificação é a maneira de como os navegadores definem quais valores de propriedades são os mais relevantes para o elemento a ser utilizado.

## Prioridades

Ordem crescente de especificação

- Seletores Universais (`*`)
- Tags (`h1`)
- Classes seletoras (`.class`)
- Atributos Seletores (`a[href="https://example.org"]`)
- Pseudo-classes (`:first-child`)
- Seletores ID (`#id`)
- Estilo Inline (`<h1 style="color: pink;">`)

## A exceção !important

Quando a regra !important é utilizada na declaração do estilo substitui qualquer outra declaração feita no CSS, onde quer que esteja na lista de declaração. Contudo, !important não tem nada a ver com especificação.

## Exemplo:

```html
<div>
  <p id="cor">Qual é minha cor?</p>
</div>
```

```css
p {
  background-color: red;
}

#cor {
  background-color: green;
}
```

> "Qual vai ser a cor do elemento p?"

De acordo com a **especificidade** vamos ter a prioridade para a seletor do ID, logo nossa cor vai ser **Verde**.
