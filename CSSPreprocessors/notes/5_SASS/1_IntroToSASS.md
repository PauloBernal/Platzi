# Introducción a SASS

SASS (Syntactally Awesome StyleSheets) es una extensión de CSS que añade características potentes y elegantes. Como preprocesador admite el uso de variables, mixins, modularización, etc. En los últimos años se convirtió en el preprocesador de CSS con mayor grado de satisfacción entre los usuarios.

## SASS vs SCSS

Tanto SASS como SCSS tienen las mismas funcionalidades, sin embargo lo que más cambia es la sintaxis en ambas. En el caso de SCSS la sintaxis es casi idéntica a CSS, con algunas diferencias en temas de anidación y variables. En SASS la sintaxis elimina completamente las llaves para basarse en un sistema de identación similar a Pug. En SASS también se elimina el punto y coma de la sintaxis y se debe dejar un espacio después de los dos puntos en los estilos:

***SCSS***

~~~scss
element {
  property: value;
}
~~~

***SASS***

~~~sass
element
  property: value
~~~

## Anidación

La anidación tanto en SCSS como en SASS se da colocando los estilos de un elemento dentro de otro.

***SCSS***

~~~scss
parent {
  *parent styles*

  child {
    *child styles*
  }
}
~~~

***SASS***

~~~sass
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

## BEM y referencias al elemento

Para referenciar al elemento dentro de los estilos se utiliza un ampersand (`&`). Esto es útil al utilizar la metodología de estructuración BEM porque las clases de los elementos y modificadores incluyen el nombre de la clase de su bloque:

***SCSS***

~~~scss
block {
  *block styles*

  &__element {
    *element styles*
  }
}
~~~

***SASS***

~~~sass
block
  *block styles*

  &__element
    *element styles*
~~~

***CSS***

~~~css
block {
  *block styles*
}

block__element {
  *element styles*
}
~~~
