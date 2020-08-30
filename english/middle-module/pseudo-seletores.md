# Pseudo-Seletores

Já aprendemos os seletores básicos do CSS, mas que tal dar uma aprofundada?

## \*

Este seletor é usado para **resetar o css** que vem "por padrão", assim temos todo os elementos da página como alvo.

Exemplo de \* que é bastante utilizado:

```css
* {
  padding: 0;
  margin: 0;
  outline: 0;
  box-sizing: border-box;
}
```

## A > B

Irá selecionar os filhos B que são diretos de A.

No exemplo a seguir, todos os filhos de ul que são li serão afetados:

```css
ul > li {
  color: white;
}
```

## A + B

O seletor adjacente irá selecionar somente o elemento imediatamente(B) após o primeiro(A) elemento.

No exemplo a seguir, ele irá chamar o segundo span, e não o primeiro.

```css
span + span {
  color: white;
}
```

## A ~ B

O seletor é parecido com o A + B, com a diferença que irá selecionar todos os elementos imediatamente após B

```css
ul ~ section {
  background-color: red;
}
```

Existem outros seletores bastante específicos, mas nesta seção mostramos apenas os principais e que com certeza você irá utilizá-los!
