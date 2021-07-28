# Anatomía de un documento HTML

## Inicial

Para que el navegador sepa que se está trabajando con HTML 5 se utiliza al inicio del documento:

~~~html
<!DOCTYPE html>
~~~

Después viene la etiqueta principal o root element (elemento raíz) la cuál es `<html>` que engloba el `<head>` y el `<body>`.

~~~html
<html>
  <head></head>
  <body></body>
</html>
~~~

Generalmente para representar anidamiento se utiliza identación en los elementos hijo.

## Head

El head es la etiqueta que engloba información que no se renderiza como parte de la estructura (estilos, scripts, metadatos, etc). Algo básico en esta etiqueta es la codificación (generalmente UTF-8) y el título de la página:

~~~html
<head>
  <meta charset="UTF-8">
  <title> Title </title>
</head>
~~~

## Body

El body es la etiqueta que engloba los elementos a renderizarse como parte de la estructura de la página (div, párrafos, imágenes, etc). Un `<div>` es un contenedor comodín, es decir, no forma parte de la semántica de HTML pero se us como un contenedor genérico.

## Estructura básica

La estructura básica de un documento HTML se ve más o menos así:

~~~html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title> Title </title>
  </head>
  <body>
  </body>
</html>
~~~
