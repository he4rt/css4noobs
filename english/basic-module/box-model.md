# Box Model - O que diabos é isso?

Um box model de CSS é basicamente uma caixa, um box, que está envolta de cada elemento HTML. Ela é composta por margem, bordas, padding e o conteúdo.

Ela funciona como camadas, a camada mais externa é a margem, e a mais interna é o conteúdo.

Sua organização, usando um exemplo de tag HTML é:

```html
  <Margin>
    <Border>
      <Padding>
        <Content>
      </Padding>
    </Border>
  </Margin>
```

Outro modo de você observar como funciona o box model é usar o inspecionar elementos do seu navegador. Na área de **Layout** você poderá ver o Box Model do elemento selecionado, como na imagem abaixo.

<p align="center">
  <img src="../img/box-model-intro.png">
</p>

## O que são essas camadas do Box Model?

Como dito acima, o box model é composto por margem, padding, borda e conteúdo.

**Conteúdo** - Como o nome diz, é o conteúdo desse box. Pode ser texto, imagem, link. É onde o seu conteúdo final irá aparecer.

Por exemplo:

```html
<div>
  Exemplo de conteúdo
</div>
```

**Padding** - É uma área transparente que fica além do seu conteúdo. Na imagem acima, ela é representada pela cor roxa.

**Borda (Border)** - Como o nome diz, é uma borda que fica ao redor do seu padding. Diferente do padding, ela pode possuir cor e forma.

**Margem (Margin)** - É a camada mais externa do box model. Ela irá determinar as distâncias para os outros elementos e assim como padding, ela é transparente.

## Atenção ao tamanho final do seu elemento

É importe lembrar que o tamanho final do seu elemento, será uma somatória de todas as medidas que você definiu para essas propriedades.

Se temos:

```css
div {
  width: 320px;
  padding: 10px;
  border: 5px solid #000;
  margin: 0;
}
```

O tamanho total do seu elemento é calculado como uma equação, onde temos:

Largura total = width + padding a esquerda + padding a direita + borda a esquerda + borda a direita + margem a esquerda + margem a direita

Se substituirmos os nomes pelos valores definidos no exemplo assim, fica:

Largura total = 320px + 10px + 10px + 5px + 5px + 0

Sendo um total de 350px.
