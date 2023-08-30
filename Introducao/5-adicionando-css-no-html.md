# Adicionando CSS nas páginas HTML

Há 3 formas comuns de se adicionar estilos à um documento HTML. Usando a tag `<style>`, o atributo `style` ou a tag `<link>`.

<br/>

---

<br/>

## Tag `<style>`

Podemos usar a tag `<style>` para estilizar nossas páginas HTML. Ela fica dentro do elemento `<head>`, pois ela deve ser interpretada pelo navegador de forma prioritária, junto com o HTML. A tag `<style>` não precisa receber nenhum atributo e como os estilos vão dentro dela, ela precisa de uma tag de abertura e uma de fechamento.

A tag `style` é recomendada em projetos maiores que contém CSS prioritário que precisa ser processado de forma imediata.


```html
<html>
  <head>
  <!-- Adicionamos aqui a tag style e os estilos dentro dela -->
    <style>
      .box-red {
        background-color: red;
        width: 100px;
        height: 100px;
      }
    </style>
  </head>
  <body>
    <div class="box-red">
     <p>Box</p>
    </div>
  </body>
</html>
```

<br/>

---

<br/>

## Style externo - Link

O estilo externo é a forma mais comum de se trabalhar com CSS. Ele consiste no uso de uma tag `<link>` contendo uma URL apontando para o arquivo CSS. Dessa forma, ao identificar a tag o navegador irá baixar a folha de estilos e associar ao documento de HTML que a contém.

Um HTML pode conter múltiplas folhas de estilo, sendo a ordem de prioridade entre elas da última para primeira.

Suponhamos que nossa estrutura de pastas está da seguinte forma:

![No VSCode, pasta chamada "projeto" contendo um arquivo index.html](../img/Introducao/projeto-1.png)

<br/>

Quando trabalhamos com múltiplos arquivos `.css`, é comum agrupá-los dentro de uma mesma pasta:

![o VSCode, pasta chamada "projeto" contendo um arquivo index.html e uma pasta com o nome de css contendo o arquivo main.css](../img/Introducao/projeto-2.png)

<br/>

Pensando no exemplo acima, o carregamento do arquivo CSS `main.css` usando a tag `<link>` ficaria da seguinte maneira:

```html
<html>
  <head>
   <!-- Aqui adicionamos a tag link, com referência para nosso arquivo CSS -->
   <link rel="stylesheet" href="css/main.css">
  </head>
  <body>
    <div class="box-red">
     <p style="color:red;"> Box </p>
    </div>
  </body>
</html>
```
<br />

Em que:
- __rel__ - Esse atributo sinaliza ao navegador que o recurso a ser baixado é uma folha de estilo. Isso faz com que ele seja identificado com o tipo `text/css` e seja baixado com alta prioridade.
- __href__ - Um atributo de <span lang="en-US">__hyperlink reference__</span>. Ele recebe o link para a folha de estilo, podendo esse se referir à um arquivo local (ex: `./style.css`) ou um arquivo remoto.

<br/>

---

<br/>

## Atributo style - Style Inline

O atributo _style_, também conhecido como style inline é usado diretamente em qualquer elemento HTML, definindo propriedades CSS pra apenas pro elemento que a possuí. Cada elemento pode possuir apenas um atributo `style` e ele pode receber um ou mais estilos CSS, na mesma sintaxe `propriedade: valor;`.

```html
<html>
  <head>
    <title> CSS Inline </title>
  </head>
  <body>
    <div class="box-red">
    <!-- Adicionamos o atributo style aqui para podermos estilizar nossa tag -->
     <p style="color:red;"> Box </p>
    </div>
  </body>
</html>
```

O estilo inline não é muito recomendado por ter uma especificidade muito alta e difícil replicabilidade - você precisa escrever diretamente em todas as tags que vai estilizar, tornando-o difícil de manter.

Um jeito seguro de usar estilos inline é passando [variáveis CSS](../Modulo-Intermediario/variables.md).


