# Seletores

## História

Até a versão 4.1 do HTML a forma mais comum de se estilizar conteúdo era usando atributos de estilo. Você provavelmente deve ter pensado em `style`, mas podíamos alterar o `background` de uma tabela usando o atributo `bgcolor`, ou a cor da fonte de uma tag `<font>` usando o atributo `color`. Abaixo, um código com sintaxe de HTML 4.1 de um card com uma imagem e um parágrafo:

```html
<div align="center">
  <img src="photo.jpeg" vspace="12px" alt="" />
  <p align="center">
    <font size="7" color="#F4F11A" face="Arial,sans-serif">Boas vindas</font>
  </p>
</div>

```
&nbsp;

Algumas propriedades acima foram depreciadas na transição do HTML 4.1 pra versão 5. Apesar da versão 4.1 já dar suporte pra tag _inline_ de estilos e a importação via `<link>`, a adoção dop CSS utilizado dessa maneira levou algum tempo, mas foi acelerada pela depreciação de estilos nativos. Abaixo, a referência dos estilos depreciados se quiser conhecer!

- `align` - Cada grudpo de elementos tinha sua definição de `align`. Na `<div>` por exemplo, os valores de `align` eram `left | center | right | justify`, pra imagens os valores eram `bottom | middle | top | right | left`. [Documentação oficial, em inglês](https://www.w3.org/TR/html401/struct/objects.html#adef-vspace) 
- `vspace` - Define o espaço a ser inserido acima ou abaixo dos elementos `<img>`, `<applet>` ou `<object>`, o valor é definido em `px`. [Documentação oficial do align pra `<img>`, em inglês](https://www.w3.org/TR/html401/struct/objects.html#adef-align-IMG), [Documentação oficial do align pra `<div>`, em inglês](https://www.w3.org/TR/html401/present/graphics.html#adef-align)
- `face` - Na tag `<font>`, define a familia da fonte a ser utilizada, substituido por `font-family` no CSS. [Documentação oficial, em inglês](https://www.w3.org/TR/html401/present/graphics.html#adef-face-FONT)

&nbsp;

> 💡 Você ainda pode usar a propriedade `align` pra elementos como `<div>` e `<table>`, em arquivos Markdown (.md) ela é perfeita pra centralizar conteúdo na ausência de CSS.

&nbsp;

Além da sintaxe limitada, o código era bem difícil de reutilizar, obrigando a pessoa desenvolvedora a copiar e colar grandes trechos de código. Na proposta de criar uma folha de estilos, era necessária uma forma de selecionar elementos do HTML através das suas características, pra que fosse possível selecionar um só, um grupo específico ou criar estilos padrões pra certos elementos.


<br />

---

<br />

## Seletores

&nbsp;

### ◽️ **Seletor universal**

O seletor universal `*` se refere à todos elementos que vão dentro do `<body>` e o elemento `<html>`. Usamos esse seletor quando queremos aplicar mudanças que influenciem todos elementos do HTML que são <a href="#tangivel">tangíveis<sup>1</sup></a>, ou seja, que renderizam na tela.

O uso mais comum dele é pra zerar as `margins` e `padding` quem vem por padrão na maioria dos elementos HTML, <a href="#agent">definido pelo _user-agent_ <sup>2</sup></a>.

```css
* {
  margin: 0px;
  padding: 0px;
}
```

&nbsp;

### ◽️ **Seletor de tipo**

O seletor de tipo seleciona um elemento de HTML diretamente. Usado dessa forma, ele aplica borda à todos elementos `<h1>` no documento.

Um uso comum de seletor de tipo é formatar os estilos base dos elementos HTML. Um exemplo disso são [resets de CSS](https://www.alura.com.br/artigos/o-que-e-reset-css), que removem estilos padrões definidos pelos navegadores, fazendo com que você não precise sobrescrevê-los.

```css
h1 {
  font-size: 2.5rem;
}
```

&nbsp;

### ◽️ **Seletor do tipo classe**

Esse seletor se refere ao atributo `class` de um elemento HTML. Cada elemento pode ter um ou mais classes e as classes podem ser reutilizadas entre elementos. As classes podem ter qualquer nome, com a restrição de não poderem começar com números e [caracteres não suportados](https://www.w3.org/TR/CSS21/syndata.html#characters). No HTML podemos definir a classe `class="btn"`, e pra acessá-la, basta usar o mesmo nome precedido de um ponto `.btn {}`.

Usando o exemplo acima, uma classe `.btn` que pode ser aplicada em todos os botões de uma mesma página:

No HTML

```html
<button class="btn">Click</button>
```

No CSS

```css
.btn {
  background: tomato;
  border: none;
  padding: 0.5em 0.75em;
}
```

&nbsp;

Podemos inclusive usar mais de uma classe em um elemento:

No HTML

```html
<button class="btn btn-outline">Click</button>
```

No CSS

```css
.btn-outline {
  background: transparent;
  border: tomato;
}
```

Como o `.btn-outline` também declara as propriedades `background` e `border` e vem depois da classe `.btn`, ela vai sobrescrever essas propriedades, mantendo o `padding` da classe original.


&nbsp;
### ◽️ **Seletor de Id**

O seletor de `id` segue as mesmas regras de nomenclatura que o de classe, porém no CSS ele é representado pela junção da hashtag `#` e o nome do id, ex: `#first-section`. Os ids foram pensados como identificadores únicos de um elemento e não podem ser reutilizados. Ao aplicar uma classe em um elemento, você:

- Cria um identificador único desse elemento
- Cria uma âncora que pode ser referenciada através de um link. [Artigo sobre links e âncoras com id](https://www.alura.com.br/artigos/ancorando-elementos-com-html5)
- Cria uma variável global contendo o elemento

Ou seja, usar `id` apenas pra estilizar elementos CSS pode fazer com que suas capacidades sejam mal aproveitadas. No geral, arquiteturas CSS costumam dar preferência às classes, pelo fato de seletores `id` serem mais específicos e não poderem ser reutilizados. Abaixo, um exemplo de `id`:

No HTML

```html
<section id="blog"></section>
```

No CSS

```css
#blog {
  display: grid;
  gap: 2ch;
}
```

&nbsp;
### ◽️ **Seletor com atributo**

Todos elementos HTML possuem atributos, e esses podem ser utilizados pra atribuir CSS. Elementos como `<input>` são diferenciados apenas pelo seu atributo type, o seletor de atributo possibilita estilizar, entre outras coisas, diferentes tipos de input individualmente:

No HTML

```html
<input type="text" />
<input type="submit" />
```

No CSS

```css

[type='text'] {
  width: 100px;
  height: 100px;
  background-color: red;
}

[type='submit'] {
  width: 100px;
  height: 100px;
  background-color: blue;
}
```

&nbsp;

O seletor de atributos dá suporte ao uso de caracteres coringa que possibilitam você a referenciar diferentes valores de atributos. No exemplo abaixo, podemos selecionar links de acordo com seu tipo de arquivo e colocar uma imagem referente a esse tipo nele usando CSS:

No HTML

```html
<ul>
  <li>
    <a href="my-image.jpg">Exemplo de imagem</a>
  </li>
  <li>
    <a href="my-document.pdf">Exemplo de documento PDF</a>
  </li>
  <li>
    <a href="my-document.pdf">Outro exemplo de documento PDF</a>
  </li>
</ul>
```

No CSS

```css

/* O caractere coringa $ significa "termina com". A linha abaixo adiciona um ícone à todo link que possui o final .pdf */
a[href$=".pdf"]::before {
  background-image: url(https://web-dev.imgix.net/image/VbAJIREinuYvovrBzzvEyZOpw5w1/fc7bLiJYf5US6QxTOKsF.png);
}

a[href$=".jpg"]::before,
a[href$=".png"]::before {
  background-image: url(https://web-dev.imgix.net/image/VbAJIREinuYvovrBzzvEyZOpw5w1/N79qCc0c06217YT4ofYM.png);
}

```

[Nesse link do Codepen](https://codepen.io/web-dot-dev/pen/BapBbOy) você consegue inspecionar o código desse exemplo. O exemplo foi criado pela galera do google no curso de CSS básico deles, o [web.dev](https://web.dev/learn/css).

&nbsp;

Os caracteres coringa do seletor de atributos são:

```css
/* Um href que contém o link "example.com" */
[href*='example.com'] {
  color: red;
}

/* Um href que começa com https */
[href^='https'] {
  color: green;
}

/* Um href que termina com .com */
[href$='.com'] {
  color: blue;
}
```
<small>Exemplo retirado [do curso web.dev nesse link.](https://web.dev/learn/css/selectors/#seletor-de-atributo)</small>

&nbsp;

### ◽️ **Agrupando seletores**

É possível estilizar vários seletores ao mesmo tempo separando-os por vírgula:

No CSS

```css
header,
footer,
section,
[data-body="section"],
.section {
  display: flex;
}

```

&nbsp;

Também podemos selecionar seletores que estão dentro de outros usando espaço em branco:

```css

/* Estiliza todo .input-text dentro de um <form> */
form .input-text {
  
  }

/* Estiliza todo #submit que estiver dentro de um <li> que estiver dentro de um <ul> */
ul li #submit {

}

```

&nbsp;

E selecionar elementos que precisam obrigatóriamente possuir mais de uma característica, como um elemento que precisa ter uma classe específica:

```css
/* Todo elemento do tipo form que também tem a classe .special-form */
form.special-form {
  
  }

/* Todo elemento do tipo input que também tem o atributo type=color */
input[type="color"] {

}
```

<br />

---

<br />

## Notas de rodapé

1. <a name="tangivel"></a>  **Tangível** é uma categoria de conteúdo do HTML. A categoria de **tangível** ou _palpable content_ é a de elementos que **não são vazios, nem ocultos (hidden), e que seu conteúdo é renderizado e substancial**. Elementos como `<head>` ou `<meta>`, por exemplo, não fazem parte dessa categoria. [Documentação oficial, em inglês](https://developer.mozilla.org/en-US/docs/Web/HTML/Content_categories#palpable_content).

2. <a name="agent"></a>  **<i>User-agent stylesheet</i>** se refere à folha de estilo do navegador. Cada navegador aplica uma folha de estilo padrão dando uma aparência base nos elementos HTML. O `<button>`, por exemplo, vem com uma borda preta e uma cor de fundo cinza mesmo se você não definir nenhum CSS pra ele. Os resets de CSS servem pra remover esses estilos. Recomendo a leitura [desse artigo do Ricardo Gouveia no Medium pra entender mais sobre](https://medium.com/trainingcenter/user-agent-style-sheet-o-porqu%C3%AA-de-um-css-que-s%C3%B3-serve-para-ser-sobrescrito-f1ef84c9ebf7). Caso queira ver o CSS das folhas de estilo dos navegadores, [esse artigo do Jens Oliver Meiert (em inglês)](https://meiert.com/en/blog/user-agent-style-sheets/) tem links pra algumas delas.