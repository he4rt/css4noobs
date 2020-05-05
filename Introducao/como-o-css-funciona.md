# Como o CSS funciona

O CSS funciona através de uma estrutura de simples de seletor, propriedade e valor.

Então todos os nossos blocos de código que estilizarão algo, são feitos da seguinte forma.

```css

seletor {
  propriedade: valor;
  propriedade: valor;
  ...
}
```

onde:
- __seletor__: elemento do HTML que será estilizado (por exemplo, uma div, um parágrafo, uma section). Você pode entender um pouco melhor sobre os seletores acessando a página de [seletores](../Modulo-Basico/seletores.md).

- __propriedade__: o que será mudado no nosso seletor (por exemplo, a cor do texto, a cor de fundo do elemento, o tamanho dele).

- __valor__: como a propriedade será aplicada. (por exemplo, definirmos uma cor `red` para a nossa propriedade `color`).