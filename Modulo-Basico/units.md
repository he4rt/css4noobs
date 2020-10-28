# Units - Unidades em CSS

Dentro do CSS, existem várias propriedades que aceitam unidades como valores, como por exemplos as propriedades `width` ou `height`.
Nessa seção, iremos abordar melhor quais as unidades existem e pra que cada uma serve.

Para começo de conversa, precisamos saber que existem dois tipos de unidades de tamanho, as unidades de tamanho **relativas** e unidades de tamanho **absolutas**.

## Unidades absolutas

Os tamanhos de unidade absolutas irão aparecer do tamanho exato que você definir na tela.
Por exemplo, se você definir que o o `width` de um elemento é _100px_, ele será _100px_ independente do tamanho da tela do dispositivo que você estiver usando.
Esses tamanhos de unidade não são muito recomendados para definir tamanhos em tela, devido a grande quantidade de telas que existem no mercado hoje em dia.
A unidade de medida mais utilizada entre as unidades absolutas, é o **px**, mesmo entrando cada vez mais em desuso, devido as unidades relativas.
Vale lembrar que a unidade **px** varia de acordo com o dispositivo. Para dispositivos com um baixo [dpi](https://www.significados.com.br/dpi/) o comportamento de 1px é igual a um pixel do dispositivo (um ponto), na tela.

> Caso queira olhar todas as unidades absolutas, você pode consultar o link de referência ao final da página.

## Unidades relativas

As unidades relativas de tamanho especificam o tamanho relativo em relação com outra propriedade de tamanho. Essas medidas escalam melhor na renderização de dispositivos de tamanhos diferentes, por isso são fortemente indicadas para usar quando se pensa em criar elementos com tamanho escalável e diferentes tipos de responsividade.

As principais unidades de medida relativas são a **em**, **rem**, **vw** e **vh**.

A unidade de medida **em** é relativa de acordo com o tamanho da `font-size` do elemento. Por exemplo, **2em** equivalem a 2 vezes o tamanho da fonte atual.

A unidade de medida **rem** é relativa ao tamanho da fonte do elemento root.

A unidade de medida **vw** equivale a 1% do `width` do viewport.

A unidade de medida **vh** equivale a 1% do `height` do viewport.

***viewport**: o tamanho da janela do browser. Por exemplo, se o viewport for 100cm, 1vw = 1cm

> Caso queira olhar todas as unidades relativas, você pode consultar o link de referência ao final da página.

## Qual unidade de medida usar

Caso você tenha dúvidas de qual unidade usar, recomendo seguir o que [este artigo](https://www.w3.org/Style/Examples/007/units.pt_BR.html) indica.

## Referências

[https://www.w3schools.com/cssref/css_units.asp](https://www.w3schools.com/cssref/css_units.asp)