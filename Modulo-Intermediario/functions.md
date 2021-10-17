# Funções CSS

Usar funções no CSS nos possibilita trabalhar com algumas variáveis e operações lógicas que podem
facilitar a maneira que construímos nossos estilos.

## attr()

A função attr() é capaz de capturar algum atributo/parâmetro do elemento ao qual ela está sendo utilizada.

Vamos capturar o href do elemento `a` a seguir:

`<a href="https://heartdevs.com/">He4rt<a/>`

No nosso CSS, iremos colocar o link entre colchetes ( [] ) no nosso pseudo-elemento `::after`.

```
a {
    color: violet;
}
a:after {
    content: " [" attr(href) "]";
}
```

Nosso retorno no HTML, é parecido com isto:

```
He4rt [https://heartdevs.com/]
```

## calc()

A função calc() é capaz de fazer cálculos sobre os valores e medidas no CSS.

Digamos que queremos que o container ocupe 100% da tela menos 20px. Podemos usar o calc() para isso desta maneira:

```
.container {
    width: calc(100% - 20px);
}
```

Os operadores que podemos usar nele são: adição, subtração, divisão e multiplicação.

## hsl()

A função hsl() define uma cor utilizando o sistema HSL. ela recebe 3 variáveis: o espectro, a saturação e a iluminação.

| Variável   | Valor                                            |
| ---------- | ------------------------------------------------ |
| espectro   | 0 a 360, sendo 0 vermelho, 120 verde, e 240 azul |
| saturação  | 0% a 100%, sendo 0% esmaecido e 100% intenso     |
| iluminação | 0% a 100%, sendo 0% preto e 100% branco          |

Sabendo os parâmetros que precisamos usar, para aplicar o o hsl() siga o exemplo abaixo:

```
div {
    background-color: hsl(120, 60%, 70%);
}
```

## hsla()

A função hsla() define uma cor utilizando o sistema HSL e Alfa. ela recebe 4 variáveis: o espectro, a saturação, a iluminação e o alfa.

| Variável   | Valor                                                     |
| ---------- | --------------------------------------------------------- |
| espectro   | 0 a 360, sendo 0 vermelho, 120 verde, e 240 azul          |
| saturação  | 0% a 100%, sendo 0% esmaecido e 100% intenso              |
| iluminação | 0% a 100%, sendo 0% preto e 100% branco                   |
| alfa       | 0 a 1, sendo 0 transparente e 1 opaco (sem transparência) |

Sabendo os parâmetros que precisamos usar, para aplicar o o hsla() siga o exemplo abaixo:

```
div {
    background-color: hsl(120, 60%, 70%, 0.5);
}
```

## linear-gradient()

A função linear-gradient() define gradiente de cor em uma direção para ser usado como background.

A função recebe um parâmetro como direção/ângulo, e pelo menos 2 parâmetros de cor.

| Direção         | Descrição                      |
| --------------- | ------------------------------ |
| 180deg          | 180 graus                      |
| to right        | para direita                   |
| to bottom right | diagonal: para baixo e direita |
| to top          | para cima                      |

Para aplicar o linear-gradient(), siga o exemplo abaixo:

```
div {
    background-image: linear-gradient(to top right, white, black);
}
```

## rgb()

A função rgb() define uma cor utilizando o sistema RGB com valores de 0 à 255 ou de 0% a 100% para cada canal. ela recebe 3 variáveis: red, green e blue.

Para aplicar a função rgb(), siga o exemplo abaixo:

```
div {
    background-color: rgb(128,128,128);
}
```

## rgba()

A função rgba() define uma cor utilizando alfa e o sistema RGB com valores de 0 à 255 ou de 0% a 100% para cada canal. ela recebe 4 variáveis: red, green, blue e o alfa.

Para aplicar a função rgba(), siga o exemplo abaixo:

```
div {
    background-color: rgb(128,128,128, 0.5);
}
```

## url()

A função url() define um link para um arquivo externo no CSS.

Por exemplo, para buscar uma imagem:

```
div {
    background-image: url("https://heartdevs.com/dist/images/logo-he4rt2.png");
}
```
