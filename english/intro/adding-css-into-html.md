# Adding css into HTML

We can add CSS into our HTML pages by three ways, using the style tag, using the attribute style or using the link tag, the last one is more recommended nowadays.

## Tag `<style>`

We can use the tag `<style>` to style our HTML pages.

To use it, you just have to add the tag inside the tag `<head>` into your HTML document.

```html
<html>
  <head>
  <!-- Adicionamos a tag style aqui para podermos estilizar nossa página -->
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
     <p> Box </p>
    </div>
  </body>
</html>
```

## Attribute style - Style Inline

Tte Attribute _style_, also known as inline style, is an attribute that we use into our tags to style them.

To use it, you just have to add the style attribute inside the tag into our HTML document.


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

## External style - Link

This last one, and more recommended way to use css, consist in use the tag `<link>` to make a connection with our HTML and CSS.

Imagine that our folder structure is as follows:

![](../../img/Introducao/projeto-1.png)

It's quite usual create a folder where we create our files.css and inside it, create the files itself, letting the folder structure as follows: 

![](../../img/Introducao/projeto-2.png)

After that, we write our CSS rules inside the file `main.css`.

How the HTML catch this info? with the tag `<link>`.

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


- __rel__ = The relationship that this link has with our file (in this case is a stylesheet).
- __href__ = The reference of where this file is located (in our case, inside the folder _css_ with the name _main.css_)
