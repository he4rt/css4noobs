# Background

A propriedade background serve para definirmos efeitos de fundo nos nossos elementos, podendo ser eles de cor (`background-color`) ou imagem (`background-image`).

Nesse documento, iremos aprender sobre essas duas propriedades e também as propriedades `background-repeat`, `background-attachment` e `background-position`.

## Background Color (background-color)

_Sintaxe_

```css
elemento {
  background-color: valor;
}
```

Onde:

- elemento: Qual elemento terá o seu fundo modificado, como por exemplo uma div.
- valor: Qual cor será definida nesse fundo.

Os valores podem ter quatro padrões

- Padrão nominal: Você pode definir o fundo usando um nome de cor. Ex: `background-color: red` para a cor vermelha.

- Padrão Hexadecimal: Você pode definir o fundo usando o hexadecimal de uma cor. Ex: `background-color: #ff0015` para a cor vermelha.

- Padrão RGB: Você pode definir o fundo usando o RGB de uma cor. Ex: `background-color: rgb(255, 0, 0)` para a para a cor vermelha.

- Padrão RGBA: Você pode definir o fundo usando o RGBA de uma cor. Ex: `background-color: rgba(255, 0, 0, 0.5)` para a cor vermelha. O parâmetro A, ou alfa, possibilita definir a opacidade de uma cor.

## Background Image (background-image)

_Sintaxe_

```css
elemento {
  background-image: url('');
}
```

Onde:

- elemento: Qual elemento terá o seu fundo modificado, como por exemplo uma div.
- url: Diretório onde está localizada a imagem ou endereço web da imagem.

## Background Repeat (background-repeat)

Caso a imagem não tenha tamanho suficiente para preencher toda área necessária, ela irá repetir na horizontal e na vertical até que toda área seja preenchida. Para controlarmos essa repetição usamos a propriedade `background-repeat`.

_Sintaxe_

```css
elemento {
  background-image: url('imagem/img1.png');
  background-repeat: valor;
}
```

Onde:

- elemento: Qual elemento terá o seu fundo modificado, como por exemplo uma div.
- valor: Qual padrão de repetição será utilizado.

Os valores podem ter quatro padrões

- no-repeat: Você pode definir que a imagem não se repita. Ex: `background-repeat: no-repeat`
- repeat: Você pode definir que a imagem se repita tanto na horizontal como na vertical. Ex: `background-repeat: repeat`
- repeat-x: Você pode definir que a imagem se repita apenas na horizontal. Ex: `background-repeat: repeat-x`
- repeat-y: Você pode definir que a imagem se repita apenas na vertical. Ex: `background-repeat: repeat-y`

## Background Attachment (background-attachment)

Com o `background-attachment` você pode definir se a imagem ficará fixada ou se ela irá se mover de acordo com o scrool.

_Sintaxe_

```css
elemento {
  background-image: url('imagem/img1.png');
  background-attachment: valor;
}
```

Onde:

- elemento: Qual elemento terá o seu fundo modificado, como por exemplo uma div.
- valor: Padrão que diz se a imagem ficará fixada ou se ela irá se mover.

Os valores podem ter dois padrões

- fixed: Você pode definir que a imagem fique fixada. Ex: `background-attachment: fixed`
- scrool: Você pode definir que a imagem se mova com o scrool. Ex: `background-attachment: scroll;`

## background Position (background-position)

Com o `background-position` você pode definir o a posição inicial em que a imagem irá se posicionar.

_Sintaxe_

```css
elemento {
  background-image: url('imagem/img1.png');
  background-position: valor;
}
```

Onde:

- elemento: Qual elemento terá o seu fundo modificado, como por exemplo uma div.
- valor: Qual padrão de posição será utilizado.

Os valores da propriedade de posição de background, podem ser feitas de várias formas, como mostrado na tabela abaixo.

| Valor         | Descrição                                                                                                                                      |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| left top      | O background se iniciará na esquerda no eixo horizontal e no topo no eixo vertical.                                                            |
| left center   | O background se iniciará na esquerda no eixo horizontal e no centro no eixo vertical.                                                          |
| left bottom   | O background se iniciará na esquerda no eixo horizontal e no ponto inferior no eixo vertical.                                                  |
| right top     | O background se iniciará na direita no eixo horizontal e no topo no eixo vertical.                                                             |
| right center  | O background se iniciará na direita no eixo horizontal e no centro no eixo vertical.                                                           |
| right bottom  | O background se iniciará na direita no eixo horizontal e no ponto inferior no eixo vertical.                                                   |
| center top    | O background se iniciará no centro no eixo horizontal e no topo no eixo vertical.                                                              |
| center center | O background se iniciará no centro no eixo horizontal e no centro no eixo vertical.                                                            |
| center bottom | O background se iniciará no centro no eixo horizontal e no ponto inferior no eixo vertical.                                                    |
| %             | Você também pode passar a porcentagem do eixo horizontal e eixo vertical utilizando o sinal de porcentagem. Ex: `background-position: 50% 50%` |
| rem, px, em   | Você também pode utilizar as medidas de CSS, como px, rem e em.                                                                                |
| initial       | Define o padrão default como valor.                                                                                                            |
| inherity      | Herda os valores do elemento pai.                                                                                                              |

**Obs: Em qualquer um dos casos, se você definir apenas o primeiro valor, ele define o segundo automaticamente**
