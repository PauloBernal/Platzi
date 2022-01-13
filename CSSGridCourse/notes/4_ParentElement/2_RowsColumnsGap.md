# Filas columnas y espaciado

## Files y Columnas

Para crear columnas usando grid se usa la propiedad `grid-template-columns`, mientras que se usa una propiedad similar para crear filas `grid-template-rows`. Después de estas se coloca el tamaño de cada fila o columna de la siguiente forma:

~~~css
.parent {
  display: grid;
  grid-template-columns: *size1* *size2* ... *sizeN*;
  grid-template-rows: *size1* *size2* ... *sizeN*;
}
~~~

Si se quiere utilizar múltiples filas o columnas del mismo tamaño sin necesidad de escribir lo mismo varias veces se puede utilizar la función `repeat()`:

~~~css
.parent {
  display: grid;
  grid-template-columns: repeat(*N° columns*, *size*);
  grid-template-rows: repeat(*N° rows*, *size*);
}
~~~

En caso de querer escribir una sola propiedad para definir filas y columnas se puede utilizar `grid-template`, en la que primero se definen las filas y separado por un '`/`' (slash) se definen las columnas. en este caso también se puede hacer uso de la función `repeat()`:

~~~css
.parent {
  display: grid;
  grid-template: *row1* *row2* ... *rowN* / *col1* *col2* ... *colN*;
}
~~~

## Espaciado

Para definir el espaciado se utilizan distintas propiedades. En el caso de separar columnas se utiliza la propiedad `column-gap` (antiguamente `grid-column-gap`). Similarmente para el caso de filas, usando `row-gap` (antiguamente `grid-row-gap`). Es recomendable utilizar los estándares actuales en vez de los antiguos:

~~~css
.parent {
  display: grid;
  grid-template: ... /...;
  column-gap: *gap-size*;
  row-gap: *gap-size*;
}
~~~

Si se quiere utilizar una sola propiedad para definir el espaciado de filas y columnas existe `gap` (antiguamente `grid-gap`) que permite definir primero el espaciado de las filas y después de las columnas:

~~~css
.parent {
  display: grid;
  grid-template: ... /...;
  gap: *row-gap* *column-gap*;
}
~~~

## Areas

Las áreas como se dijo anteriormente, son un conjunto de celdas, las cuales también se pueden disponer con propiedades de grid. Para definir elementos en áreas específicas se utiliza la propiedad `grid-template-areas`, los valores son cadenas de texto entre comilllas que tienen los nombres de los elementos dentro separados por espacios. si no se quiere colocar ningún elemento en una celda simplemente se colca un punto (`.`) para indicar que es una celda vacía. Dentro de las cadenas de texto se colocan los nombres por columnas y cada cadena de texto es una fila:

~~~css 
.parent {
  display: grid;
  grid-template: ... /...;
  grid-template-areas:
    "el-name11 elname12 ... elname1N"
    "el-name21 elname22 ... elname2N"
    ...
    "el-nameM1 elnameM2 ... elnameMN";
}
~~~
