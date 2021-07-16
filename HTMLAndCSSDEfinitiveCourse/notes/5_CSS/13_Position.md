# Position

Es la forma en la que se puede posicionar un elemento en el DOM haciendo uso de CSS. Los tipos de `position` que se usan son:

- static
- absolute
- relative
- fixed
- sticky

## Static

Es el estilo por defecto en CSS que tienen todos los elementos. Su posición es estática, es decir, no varía al hacer scroll.

~~~css
element {
  position: static;
}
~~~

## Absolute

En esta posición el elemento permanece en su posición original pero los demás elementos recorren. Se puede modificar su posición absoluta respecto a la ventana con `top`, `bottom`, `right` y `left`.

~~~css
element {
  position: absolute
}
~~~

## Relative

En esta posición se puede modificar la posición del elemento respecto a su posición original (o al elemento padre) con `top`, `bottom`, `right` y `left`.

~~~css
element {
  position: relative
}
~~~

## Fixed

En esta posición se toma una posición absoluta respecto a la ventana que no varía con el scroll, es decir, el elemento siempre estará en el mismo lugar.

~~~css
element {
  position: fixed;
}
~~~

## Sticky

Es una combinación entre `absolute` y `fixed` ya que a cierta distancia establecida en `top` se queda fijo el elemento.

~~~css
element {
  position: sticky;
  top: *distance*;
}
~~~
