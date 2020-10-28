# Z-Index

A propriedade **z-index** funciona como camadas no CSS, por **padrão**, todos os elementos estão com essa propriedade no 0, quer dizer que todos os elementos estão na camada 0 ou **initial**.

# Exemplo

Aqui temos duas divs:

<p>
  <img src="../img/Modulo-Basico/z-index/padrao-divs.png" />
</p>

HTML:
```html
<div class="um"></div>
<div class="dois"></div>
```

CSS:
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
    <img src="../img/Modulo-Basico/z-index/position-divs.png" />
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
    <img src="../img/Modulo-Basico/z-index/z-index-divs.png" />
</p>

# Observações

- A propriedade z-index aceita somente valores numéricos, incluindo valores negativos.
- Só é possível aplicar o z-index caso o elemento tenha uma **position** setada (relative, absolute, fixed ou sticky).<br>
  Por esse motivo aplicamos o z-index na div 1.
