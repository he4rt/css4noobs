# Display - desmistificando block, inline e inline-block

Nesse modulo iremos aprender umas das propriedades mais importantes do css, o famigerado **Display** que influencia na forma como os elementos são dispostos na tela. Por **padrão** o display do elemento pode vir setado de duas formas diferentes: Block e Inline.

## Tudo são Boxes

Antes de partimos, você precisa ter outra visão sobre os elementos HTML. Toda vez que colocar um elemento qualquer em sua página (seja ele um titulo, um parágrafo, ou qualquer outro) tenha em mente que está colocando uma "caixa", mesmo que não veja a delimitação dessa caixa, o seu elemento se comportará como uma, se precisar de alguma forma visualizar essa delimitação, faça uso de bordas ou backgrounds para entender melhor. Guarde isso, pois precisará para entender os principais tipos de posicionamento especialmente o que vamos aprender agora.

## Display Block

Começando pelo mais simples, o display block possui duas características básicas: ele sempre ocupa todo espaço disponível na horizontal e sempre começará a partir de uma **nova** linha.

### Vamos para o exemplo, irei criar dois elementos button.

HTML

```html
<button class="btn">Block</button>
<button class="">Block</button>
```

### Resultado

![Btn](../img/block-buttons.gif)

### Agora vamos aplicar o display block no primeiro button e você verá a mágica acontecendo.

CSS

```css
.btn {
  display: block;
}
```

### Resultado

![Btn](../img/block-buttons2.gif)

Note o efeito resultante, o simples fato do primeiro button ter o display block joga o elemento concorrente para a linha seguinte.

### Algumas considerações

Mesmo que elementos block ocupem todo o espaço horizontalmente, você pode setar o tamanho desejado, ao contrário de outros elementos que veremos nesse mesmo módulo.

É importante você ter em mente quais elementos possuem display block por padrão, portanto listarei alguns abaixo:

- div
- Todos elementos de título (h1 ao h6)
- p
- form
- header
- footer
- section

## Display Inline

O display inline também possui um funcionamento bastante simples, podemos dizer que se o display block ocupa todo espaço disponível, o display inline é totalmente o contrário, ocupando somente o tamanho correspondente ao seu conteúdo. Vamos aos exemplos.

Html

```html
<h1 class="inline">Titulo maior 1</h1>
<h1 class="inline">Titulo 2</h1>
```

Novamente criei dois elementos. Nesse caso terei que aplicar a propriedade em ambos, uma vez que são elementos block, então sempre partem da próxima linha.

<em>(Irei colocar um background para melhor visualização dos efeitos do inline, mas você pode ignora-lo por enquanto)</em>

```css
.inline {
  background: gray;
}
```

### Resultado

![Btn](../img/inline1.png)

### Aplicando o Inline

```css
.inline {
  display: inline;
  background: gray;
}
```

### Resultado

![Btn](../img/inline2.png)

Note que o tamanho do elemento é determinado **apenas** pelo seu conteúdo.

### Observações

Algo muito importante sobre o display inline é que ele não obedece nenhum tipo de definição de largura ou altura, sendo assim, seu tamanho é definido somente pelo seu conteúdo interno.

## Display Inline-Block

Como o nome já sugere, o inline-block é uma "junção" dos dois anteriores, com algumas particularidades. À primeira vista pode parecer um pouco complexo, mas é exatamente o que o nome sugere. Com Inline-block você tem um comportamento inline, ou seja, por padrão o elemento irá ocupar o espaço demandado pelo seu conteúdo, mas com uma característica herdada do display block, você pode setar o tamanho (largura e altura) que desejar sem restrições.

Irei usar a mesma estrutura do anterior

HTML

```html
<h1 class="inline-block">Titulo maior 1</h1>
<h1 class="inline-block">Titulo 2</h1>
```

Aqui estou setando a largura (width) de 250 pixels, a altura (height) de 50 pixels, o display e um background cinza.

```css
.inline-block {
  display: inline-block;
  background: gray;
  width: 250px;
  height: 50px;
}
```

### Resultado

![Btn](../img/inline-block1.png)

Observe que mesmo o segundo elemento possuindo um conteúdo menor que o primeiro, os dois possuem mesma largura e altura, pois setamos isso anteriormente. Mas se não tivessemos setado, ambos teriam seus tamanhos próprios.

## Concluindo

Saber bem todas essas propriedades é requisito quase obrigatório se você quiser controlar bem seus Layouts e são pré-requisitos para aprender algumas outras propriedades mais avançadas, por isso pratique todos e tenha-os em mente. Obrigado por ler até aqui e até a próxima :zap:
