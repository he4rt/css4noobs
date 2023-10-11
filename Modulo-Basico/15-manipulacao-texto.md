# Manipulação de Texto

Neste módulo iremos ensinar os conceitos básicos de como manipular textos com CSS!

## Cores

Podemos manipular a cor dos textos usando `color: <cor-aqui>` de várias formas diferentes:

HEX: `color: #AAAAAA`

HSV: `color: hsl(0, 100%, 50%)`

RGB `color: rgb(255, 0, 0)`

RGBA `color: rgba(255, 0, 0, 0.5)`

Aplicando em um Seletor:

```css
p {
  color: #aaaaaa;
}
```

## Fonte

Para trocar a fonte padrão, usamos `font-family: 'nome-da-fonte', 'outra-fonte', ...`, por exemplo:

O CSS irá dar prioridade sempre para a primeira fonte a esquerda, em caso de não encontrado, irá carregar a próxima e assim por diante:

```css
p {
  font-family: "Poppins", "Raleway", "Muli";
}
```

Ou seja, se a fonte Poppins não for encontrada, irá chamar a Raleway, se não achar a Raleway, irá chamar a Muli, e se não achar a Muli, irá carregar uma fonte padrão do navegador.

## Estilos

Para aplicar um estilo a uma fonte, usamos `font-style: 'nome do estilo'`, por exemplo

```css
p {
  font-style: italic;
}
```

Ou seja todas as tags `<p>` da página vão está com o estilo da fonte em itálico.

## Peso

Para aplicar um peso a uma fonte, usamos `font-weight: 'nome do peso da fonte'`, por exemplo.

```css
h1 {
  font-weight: bold;
}
```

Ou seja todas as tags `<h1>` da página vão está com o peso da fonte `bold`.

## Importar Fontes

Por requisição usando o Google Fonts, podemos usar o `@import` no nosso arquivo CSS e utilizar a fonte:

```css
@import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");

p {
  font-family: "Poppins", "sans-serif";
}
```

Procure fontes de seu interesse [aqui](https://fonts.google.com/)

Podemos registrar fontes localmente, usando o `@font-face`:

`main.css`

```css
@font-face {
  font-family: "Poppins Normal";
  src: url("./to/path/fonts/Poppins-Medium.otf") format("opentype");
}
```

`outro_arquivo.css`

```css
p {
  font-family: "Poppins Normal", "sans-serif";
}
```

# Links

Para conseguirmos navegar por link's, podemos usar a tag `<a>` usando `href`:

`<a href="https://github.com/mathh95/css4noobs">Ir para o CSS4Noobs</a>`

Dessa forma, assim que clicarmos em `Ir para o CSS4Noobs`, iremos para o repositório

Para formatar essa tag, usamos:

```css
a {
  text-decoration: none;
  color: black;
}
```

- Usando o `text-decoration: none;` tiramos a linha inferior que vem por padrão.
