# Funciones especiales en grid

Existen diversas funciones en CSS que permiten facilitar el trabajo en grid. Entre estas funciones están:

- `repeat()`
- `minmax()`
- `fit-content()`

## Función `repeat()`

Cuando se quiere generar un número determinado de filas o columnas con un mismo tamaño puede reultar tedioso escribir tantas veces el mismo valor. Para esto existe la función `repeat()`, la cuál permite generar *n* filas o columnas con un tamaño determinado. La función tiene el formato:

`repeat(*N° tracks*, *size*)`

~~~css
.container {
  grid-template: repeat(*N° rows*, *row size*) / repeat(*N° cols*, *col size*);
}
~~~

## Función `minmax()`

A veces al manejar medidas relativas puede resultar molesto el modificar el tamaño de la ventana debido a que algunos elementos pueden llegar a distorisionarse. Para definir tamaños mínimos o máximos en los elementos de la grilla se puede hacer uso de la función `minmax()` en la cual se establece un tamaño mínimo y un tamaño máximo para las filas o columnas. La función tiene el formato:

`minmax(*min size*, *max size*)`

~~~css
.container {
  grid-template: repeat(*N° rows*, minmax(*min size*, *max size*)) / repeat(*N° cols*, minmax(*min size*, *max size*));
}
~~~
