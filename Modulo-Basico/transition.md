# Transições com CSS

Transições no CSS é relativamente fácil, usamos `transition: <elemento> <tempo> <tipo-de-transição>` para indicar como a transição será feita.

Um exemplo:

```css
div {
  background: blue;
  height: 100vh;
  width: 50vw;
  transition: width 1s ease;
}
```

```css
div:hover {
  width: 100vw;
}
```

* Podemos utilizar o `all` como `<elemento>` para afetar todos os elementos que estão no seletor, mas fazendo isso a transição irá ser acionada também quando a tela da aplicação for redimensionada.
