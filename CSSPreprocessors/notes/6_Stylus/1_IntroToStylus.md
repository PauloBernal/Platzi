# Introducción a Stylus

Al igual que Less y SASS, Stylus es un preprocesador de CSS. Este tiene ciertas características que lo diferencian de los otros:

- Es un preprocesador de hojas de estilos dinámico que se compila en CSS
- Está escrito e JADE y Javascript (Node.js)
- Fue creado por TJ Holowaychuk, ex-programador de Node.js

Para crear un archivo de Stylus se debe colocar la extensión `*.styl` después del nombre de archivo.

## Sintaxis

La sintaxis de Stylus es similar a la de SASS o Pug, sin corchetes ni punto y coma, solamente identación. En caso de colocar llaves o punto y coma no hay problema debido a que el compilador lo realiza de igual forma:

***Stylus***

~~~stylus
selector
  property: value
  ...
~~~

***CSS***

~~~css
selector {
  property: value;
}
~~~

## Anidación

La anidación en Stylus funciona igual que en SASS, colocando el elemento hijo dentro del elemento padre:

***Stylus***

~~~stylus
parent
  *parent styles*

  child 
    *child styles*
~~~

***CSS***

~~~css
parent {
  *parent styles*
}

parent child {
  *child styles*
}
~~~

## Referencia al elemento

Nuevamente se puede utilizar el ampersand (`&`) para hacer referencia al elemento del cuál se toman los estilos:

***Stylus***

~~~stylus
block
  *styles*
  &__element
    *element styles*
~~~

***CSS***

~~~css
block {
  *styles*
}

block__element {
  *element styles*
}
~~~

## Modularización

Para modularizar el código se puede crear un archivo para cada componente o bloque e importarlos en un archivo, el cuál se compila como los estilos. Para esto simplemente se utiliza la palabra reservada `import` con un arroba (`@`) por delante y seguida de la ruta del archivo entre comillas:

~~~stylus
@import "/route/"
~~~
