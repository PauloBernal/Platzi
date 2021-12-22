# Generación automática de Tracks

Como se vio anteriormente un track es la unión de dos o más celdas consecutivas (ya sea hacia arriba o hacia abajo). En CSS es posible generar tracks de forma automática, es decir, sin necesidad de ir actualizando el contenedor manualmente.

A esta forma de que se creen columnas o filas a medida que se añade contenido se denomina "grid implícita", solamente es necesario establecer ciertos parámetros a partir de los cuales se generarán los tracks.

## Disposición de elementos

Para que un elemento ocupe cierta cantidad de celdas se especifica en el elemento hijo con las propiedades:

~~~css
.element {
  grid-column: *initial-column* / *final-column*;
  grid-row: *initial-row* / *final-row*;
}
~~~

Los números hacen referencia a las líneas de la grilla, no a las columnas o filas como tal.

## Generación automática

Para generar de forma automática se usan las propiedades `auto`. En el caso de columnas se utiliza `grid-auto-columns`, especificando como valor el tamaño de las columnas a generar. En el caso de filas se utiliza una propiedad similar llamada `grid-auto-rows`, especificando como valor el tamaño de las filas:

~~~css
.container {
  grid-auto-columns: *size*;
  grid-auto-rows: *size*;
}
~~~

Para definir el flujo de la grid de forma automática se utiliza la propiedad `grid-auto-flow`, con la cuálse establece si los elementos irán aumentando filas, columnas u otro:

~~~css
.container {
  grid-auto-flow: row | column | row dense | column dense;
}
~~~

Los valores significan:

- `row`.- Los elementos nuevos se apilan en las filas.
- `column`.- Los elementos nuevos se apilan en columnas.
- `row dense`.- Similar a `row` pero cambiando el orden visual de los elementos.
- `column dense`.- Similar a `column` pero cambiando el orden visual de sus elementos.
