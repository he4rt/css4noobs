# Position - relative, absolute, fixed, sticky, static

Vamos desvendar e aprender todas as propriedades do position que é muito importante para o posicionamento dos elementos.

## Position static

Dificilmente ou nunca você vera alguém utilizando o `position: static` pois ele é o valor default de todos os nossos elementos.

É bom conhecer `static` pois agora você sabe que qualquer elemento tem como padrão `position: static`.

## Position absolute

Quando usamos essa propriedade em nosso documento, retiramos o nosso elemento do fluxo normal de nosso documento, nenhum espaço é criado no layout da pagina e o mesmo é posicionado relativo ao seu elemento pai posicionado mais próximo, se houver. Caso contrário, será relativo ao bloco inicial.

No HTML:

```html
<div class="normal"></div>
<div class="absolute"></div>
<div class="normal"></div>
```

No CSS:

```css
.normal {
  width: 100px;
  height: 100px;
  background: green;
}

.absolute {
  width: 100px;
  height: 100px;
  background: red;
}
```

Sem setar a propriedade position, temos esse resultado na nossa tela:

<p align="center">
  <img src="../img/modulo-position-absolute-1.png">
</p>

Agora iremos setar a propriedade position para absolute:

No CSS:

```css
.normal {
  width: 100px;
  height: 100px;
  background: green;
}

.absolute {
  /* estamos pegando a div com classe absolute */
  position: absolute;
  width: 100px;
  height: 100px;
  background: red;
}
```

O resultado que temos é:

<p align="center">
  <img src="../img/modulo-position-absolute-1-2.gif">
</p>

O que ocorreu foi que devido o position absolute não criar espaço somente ocupar o conteúdo que o elemento tem, a nossa terceira div foi para cima já que não encontrou nenhum espaço e por conta disso ficou abaixo da nossa div com a position absolute, mas conforme você consegue ver no GIF acima a nossa terceira div esta lá.

Outro comportamento que o position absolute possui é que se você manipular o elemento com `top`,`left`, `right`, `bottom` ele sempre vai estar naquela posição por que não acompanha o fluxo do nosso documento, vamos ver com um exemplo:

No CSS:

```css
.normal {
  width: 100px;
  height: 100px;
  background: green;
}

.absolute {
  position: absolute;
  left: 30px;
  width: 100px;
  height: 100px;
  background: red;
}
```

Temos o resultado:

<p align="center">
  <img src="../img/modulo-position-absolute-1-3.png">
</p>

## Position relative

Quando usamos `position relative` ele vai deslocar o nosso elemento usando como base o posicionamento que ele tem no fluxo normal do nosso documento, segue um exemplo:

No CSS:

```css
.normal {
  width: 100px;
  height: 100px;
  background: green;
}

.absolute {
  position: relative;
  left: 15px;
  width: 100px;
  height: 100px;
  background: red;
}
```

No HTML:

```html
<div class="normal"></div>
<div class="absolute"></div>
<div class="normal"></div>
```

Esse é o fluxo normal que iria acontecer caso a gente faça as três divs acima:

<p align="center">
  <img src="../img/modulo-position-absolute-1.png">
</p>

Quando usamos a propriedade `position relative` e manipulamos o `top`,`left`, `right`, `bottom` iremos usar como base a posição que ele tem no fluxo do nosso documento, segue o exemplo:

<p align="center">
  <img src="../img/modulo-position-absolute-1.png">
  <img src="../img/modulo-1-position-relative-1.png">
</p>
<p align="center">
    A imagem da direita demonstra a posição que ira utilizar como base.
</p>

Agora vamos manipular a posição do elemento

Adicione ao seu CSS:

```css
.absolute {
  position: relative;
  left: 50px;
  width: 100px;
  height: 100px;
  background: red;
}
```

Temos o resultado:

<p align="center">
  <img src="../img/modulo-1-position-relative-1-2.png">
</p>

## Position fixed

Utilizamos ele para deixar o elemento fixo no nosso documento ou seja independente do que aconteça nunca vai mudar de posição, vamos demonstrar com um exemplo:

No HTML:

```html
<h1>Está fixado</h1>
<div></div>
<div></div>
<div></div>
<div></div>
<div></div>
<div></div>
```

No CSS:

```css
div {
  width: 300px;
  margin: 35px;
  height: 100px;
  background: blue;
}

h1 {
  position: fixed;
  top: 0;
  width: 500px;
  margin: 0 auto;
  background: white;
  padding: 10px;
}
```

Resultado:

<p align="center">
  <img src="../img/modulo-1-position-fixed-1.gif">
</p>

## Position sticky

É uma mistura entre `position relative` e `position fixed`, o elemento que possui a propriedade `position sticky` é tratado como relativo até alcançar um limite especificado definido pelo `top`,`left`, `right`, `bottom`, a partir do momento que alcança esse ponto ele passa a ser fixo. E se chegar a sua posição original volta a ser tratado como `relative`.

Vamos ver um exemplo pratico:

No HTML:

```html
<h1>Posicionamento sticky</h1>
<dl>
  <dt>A</dt>
  <dd>Apple</dd>
  <dd>Ant</dd>
  <dd>Altimeter</dd>
  <dd>Airplane</dd>

  <dt>B</dt>
  <dd>Bird</dd>
  <dd>Buzzard</dd>
  <dd>Bee</dd>
  <dd>Banana</dd>
  <dd>Beanstalk</dd>

  <dt>C</dt>
  <dd>Calculator</dd>
  <dd>Cane</dd>
  <dd>Camera</dd>
  <dd>Camel</dd>

  <dt>D</dt>
  <dd>Duck</dd>
  <dd>Dime</dd>
  <dd>Dipstick</dd>
  <dd>Drone</dd>

  <dt>E</dt>
  <dd>Egg</dd>
  <dd>Elephant</dd>
  <dd>Egret</dd>
</dl>
```

No CSS:

```css
dl {
  height: 200px; /* definimos uma altura para mostrar o scroll */
  overflow: auto; /* colocamos o overflow para mostrar o scroll */
}

dt {
  background-color: black;
  color: white;
  padding: 10px;
  position: sticky;
  top: 0; /* Quando o elemento chega na posição top 0 em relação ao elemento pai passa a ser fixo */
  margin: 1em 0;
}
```

Resultado:

<p align="center">
  <img src="../img/modulo-1-position-sticky-1.gif">
</p>

## Concluindo

Conhecer bem essa propriedade é essencial para definir o posicionamento de ícones, botões, imagens, etc..., espero que pratiquem bastante! pois, muito do que vimos aqui é só uma pontinha do que podemos fazer com elas.
