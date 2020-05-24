# Z-Index

A propriedade **z-index** funciona como camadas do no CSS, por **padrão**, todos os elementos estão com essa propriedade no 0, quer dizer que todos os elementos estão na camada 0 ou **initial**.

# Exemplo
Aqui temos duas divs.

<p>
    <img src="../img/Modulo-Basico/z-index/divs-padrao.png" />
</p>

```css
  .um {
    width: 100px;
    height: 100px;
    background-color: brown;
 }

 .dois {
    width: 200px;
    height: 200px;
    background-color: chocolate;
 }
```

Caso eu aplique um **position: relative; top: 40px;** na **Div 1**:
```css
  .um {
    width: 100px;
    height: 100px;
    background-color: brown;
    position: relative;
    top: 40px;
 }
```

<p>
    <img src="../img/Modulo-Basico/z-index/divs-position.png" />
</p>

Mas eu quero que a **Div 2** fique por cima, então eu aplico a propriedade **z-index: -1** na **Div 1**.
```css
  .um {
    width: 100px;
    height: 100px;
    background-color: brown;
    position: relative;
    top: 40px;
    z-index: -1;
 ```
<p>
    <img src="../img/Modulo-Basico/z-index/divs-z-index.png" />
</p>

# Observações

 - A propriedade z-index aceita somente valores numéricos, incluindo valores negativos.
 - Só é possivel aplicar o z-index caso o elemento tenha uma **position** setada (relative, absolute, fixed, sticky).
    Por esse motivo aplicamos o z-index na div 1.
    