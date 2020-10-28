# PostCSS

[PostCSS](https://postcss.org/) é uma ferramenta para transformar estilos com plug-ins JS. Esses plug-ins podem melhor sua experiência geral com CSS com muitas features diferentes.

## Instalação

A utilização depende da forma que seu projeto está estruturado, recomendamos [ler a documentação](https://github.com/postcss/postcss#usage)

## Plugins

Iremos mostrar os principais plugins do PostCSS:

### Autoprefixier

O [autoprefixier](https://github.com/postcss/autoprefixer) adiciona as tag's necessárias para obter compatibilidade com os browsers. Exemplo:

O plugin transforma:

```css
.example {
  display: grid;
  background: linear-gradient(to bottom, white, black);
}
```

Nisso:

```css
.classe {
  display: -ms-grid;
  display: grid;
  background: -webkit-gradient(linear, left top, left bottom, from(white), to(black));
  background: -o-linear-gradient(top, white, black);
  background: linear-gradient(to bottom, white, black);
}
```

Dessa forma, não precisamos nos preocupar(pelo menos de forma geral) com a compatibilidade de nosso CSS.

### PostCSS-Utilities

O [postcss-utilities](https://github.com/ismamz/postcss-utilities) adiciona o `@util`, que tráz simplificação de código CSS, facilitando a sua utilização.

Exemplo:

```css
.borda-topo {
  @util border-top-radius(4px);
}
```

É transformado em:

```css
.borda-topo {
  border-top-left-radius: 4px;
  border-top-right-radius: 4px;
}
```

A lista completa do que temos disponível:

```text
aspect-ratio
border-color
border-radius
border-style
border-width
center
center-block
circle
clear-fix
hd breakpoint
hide-visually
hr
margin
no-hover
no-js
padding
position
reset-list
reset-text
size
min-size
max-size
sticky-footer
text-hide
text-stroke
triangle
truncate
word-wrap
```

### PurgeCSS

O [PurgeCSS](https://www.npmjs.com/package/@fullhuman/postcss-purgecss) pode ser utilizado com PostCSS, seu objetivo é diminuir o tamanho do bundle final de nosso CSS.
