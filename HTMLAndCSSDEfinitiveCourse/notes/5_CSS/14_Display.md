# Display

El display se refiere a como se renderizan los elementos HTML por parte del navegador, es decir, como se muestran estos.

## Block

Este display utiliza el 100% del espacio de forma horizontal sin importar el tamaño del contenido. De esta forma permite cambiar su modelo de caja, padding, margin, width, height, etc.

~~~css
element {
  display: block;
}
~~~

## Inline

Como indica su nombre, los elementos con este display se muestran en línea, es decir, el ancho solamente abarca su contenido. En este caso no se puede modificar propiedades como el padding o el margin en los 4 laterales, solamente se puede a la izquierda o a la derecha. Tampoco se puede modificar as dimensiones del elemento con `width` o `height`. Si queda espacio más adelante y hay otra etiqueta en línea estos elementos se apilarán hasta donde alcance el espacio.

~~~css
element {
  display: inline;
}
~~~

## Inline-block

En este caso los elementos se apilan en línea con la diferencia de que se puede modificar completamente su modelo de caja (margin, padding, width, height, etc). Se puede definir como una fusión de los mejores aspectos de `inline` y `block` (solo abarca el espacio del contenido como `inline` y se puede manipular el modelo de caja como `block`).

~~~css
element {
  display: inline-block;
}
~~~
