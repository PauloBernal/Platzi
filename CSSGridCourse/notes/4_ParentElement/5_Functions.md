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

## Valores `auto-fit` y `auto-fill`

Ambos valores son importantes para implementar responsive design. En el caso de `auto-fit`, hace que las columnas o filas ocupen todo el espacio disponible en función de los elementos, mientras que en el caso de `auto-fill` supone que se trata sólo de una fracción del total, por lo que en vez de ocupar mayor espacio disminuye el tamaño de los elementos a su mínimo para permitir que más elementos entren en ese espacio.

~~~css
.container1 {
  grid-template: repeat(auto-fit, *size*) / repeat(auto-fit, *size*);
}

.container2 {
  grid-template: repeat(auto-fill, *size*) / repeat(auto-fill, *size*);
}
~~~

## Función `fit-content()`

Esta función permite organizar un contenido con un tamaño en específico. La sintaxis es bastante simple, solamente se coloca la función `fit-content()` con el tamaño del contenido como parámetro:

~~~css
.container {
  display: grid;
  grid-template: ... fit-content(*size*) ... / ... fit-content(*size*) ...; 
}
~~~
