# Grid y las relaciones padres a hijos inmediatos

Grid permite crear una grilla para disponer los elementos en filas y columnas. En esta las propiedades se dividen en 2: las propiedades para los elementos padres y las propiedades para los elementos hijos.

## Tipos de elementos

Los elementos contenedores se denominan **padres**, mientras que los que se ubican dentro de estos se denominan **hijos**. Los elementos se pueden anidar sin limitación, es decir, los elementos padres pueden ser a su vez elementos hijos. En el caso de grid todos los elementos padre deben tener la propiedad:

~~~css
.parent {
  display: grid;
}
~~~
