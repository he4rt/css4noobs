# Variáveis do CSS

Variáveis CSS são entidades definidas por nós desenvolvedores, contendo valores que irão ser utilizados em todo o nosso projeto. Utilizamos o `var(<variavel>)` para indicar que estamos chamando uma variável do CSS.

A utilização mais comum é setar as variáveis em um arquivo base de CSS, utilizando o `:root`:

```css
:root {
  --text-primary: red;
}
```

Utilizando a variável:

```css
section {
  background-color: var(--text-primary);
}
```

Nas variáveis de CSS, podemos setar qualquer tipo de atributo, como tamanhos:

```css
:root {
  --padding-1: 8px;
}
```

```css
article {
  padding: var(--padding-1);
}
```

Assim conseguimos controlar e definir tamanhos/cores com clareza e facilidade!
