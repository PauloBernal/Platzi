# Display Flex

Este display ayuda bastante a posicionar de mejor forma los elementos en la ventana. Soluciona problemas más complejos de resolver con los `display` y `position` anteriores. Flex permite hacer un layout de forma responsive debido a que como su nobre lo indica, es flexible. Al colcar `flex` en un contenedor padre automáticamente todos los elementos dentro se comportan como si fueran elementos de bloque en línea (`inline-block`).

~~~html
<parent>
  <child1></child1>
  <child2></child2>
  ...
  <childN></child3>
</parent>
~~~

~~~css
parent {
  display: flex;
}
~~~

Al hacer esto, todos los contenedores dentro del contenedor padre son mucho más fáciles de posicionar dentro de este.

## Disposición

Con flex es mucho más fácil cambiar la disposición de los elementos ya que existen valores preestablecidos para ello. La propiedad utilizada para cambiar la disposición de los elementos se llama `flex-direction` y sus posibles valores son:

- `row`.- Por defecto los elementos vienen colocados en fila uno al lado del otro:

~~~css
element {
  flex-direction: row;
}
~~~

- `column`.- Posiciona los elementos en una columna uno sobre el otro:

~~~css
element {
  flex-direction: column;
}
~~~

- `row-reverse`.- Posiciona los elementos en fila invirtiendo el orden de estos:

~~~css
element {
  flex-direction: row-reverse;
}
~~~

- `column-reverse`.- Posiciona los elementos en columna invirtiendo su orden:

~~~css
element {
  flex-direction: column-reverse;
}
~~~

## Reacomodando elementos

Cuando los elementos sobrepasan el ancho del elemento padre existe una propiedad llamada `flex-wrap` que permite controlar como se posicionan los elementos al exceder el límite establecido por el elemento padre. Como posibles valores para esta propiedad están:

- `wrap`.- Al exceder el ancho del elemento padre el siguiente elemento se posiciona abajo del primer elemento de la fila continuando con el flujo en una nueva fila (o columna dependiendo de la disposición):

~~~css
element {
  flex-wrap: wrap;
}
~~~

- `nowrap`.- Los elementos se siguen colocando uno al lado del otro generando un scroll que se puede controlar con `overflow`:

~~~css
element {
  flex-wrap: nowrap;
}
~~~

- `wrap-reverse`.- Es similar a `wrap` con la diferencia de que los elementos se posicionan a la inversa, es decir, si la disposición es filas en vez de colocarse abajo en un a nueva fila se colocan en la parte de arriba. En caso de columnas en vez de colocarse a la derecha la nueva columna se posiciona a la izquierda:

~~~css
element {
  flex-wrap: wrap-reverse;
}
~~~

## Alineando contenido

Para alinear contenido de forma horizontal existe una propiedad llamada `justify-content` que permite posicionar los elementos dentro del contenedor padre. Los posibles valores para esta propiedad son:

- `flex-start`.- Es el estilo por defecto y alinea los elementos al principio de la fila o columna:

~~~css
element {
  justify-content: flex-start;
}
~~~

- `center`.- Centra los elementos de forma que todos estén en la parte de en medio del contenedor padre:

~~~css
element {
  justify-content: center;
}
~~~

- `flex-end`.- Coloca los elementos posicionados al final de la fila o columna:

~~~css
element {
  justify-content: flex-end;
}
~~~

- `space-between`.- Distribuye el ancho entre todos los elementos colocando un espacio entre ellos. El primer y último elemento se posicionan en los extremos del ancho del elemento padre:

~~~css
element {
  justify-content: space-between;
}
~~~

- `space-around`.- Distribuye el ancho entre todos los elementos colocando un espacio entre ellos y entre los bordes laterales del elemento padre. Los espacios entre elementos son mayores a los espacios con los bordes:

~~~css
element {
  justify-content: space-around;
}
~~~

- `space-evenly`.- Distribuye el ancho entre todos los elementos colocando un espacio igual entre ellos y los bordes laterales del elemento padre:

~~~css
element {
  justify-content: space-evenly;
}
~~~
