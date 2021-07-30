# Displays

El display es la forma en que se muestra un elemento en pantalla y las más comunes son:

- `block`
- `inline`
- `inline-block`
- `flex`
- `table`
- `grid`
- `none`

## Block

Este display permite modificar todo el modelo de caja de un elemento y por defecto los elementos con este display se acomodan uno debajo del otro:

~~~css
element {
  display: block;
}
~~~

## Inline

Este display solamente permite afectar los laterales horizontales de un elemento en el modelo de caja y al haber más de un elemento estos se colocan uno al lado del otro:

~~~css
element {
  display: inline;
}
~~~

## Inline-block

Este display permite modificar todo el modelo de caja de un elemento al igual que con display block y que los elementos se coloquen uno al lado del otro como en display inline:

~~~css
element {
  display: inline-block;
}
~~~

## None

Este display se utiliza para eliminar elementos de la vista del usuario sin que desaparezcan completamente del DOM:

~~~css
element {
  display: none;
}
~~~

## Table

Los elementos de este displayb tienen el mismo comportamiento que el elemento `<table></table>`

~~~css
element {
  display: table;
}
~~~

## Flex

Este display hace que los elementos hijo del mismo se puedan modificar desde el elemento padre (en tema de posición y disposición). Cosas como alinear elementos, centrarlos vertical y horizaontalmente entre otras cosas se pueden hacer con flex. Para ver más acerca de este display se puede acceder al siguiente [enlace](https://css-tricks.com/snippets/css/a-guide-to-flexbox)

~~~css
parent-element {
  display: flex;
}
~~~

## Grid

Flex permite alinear elementos en una dimensión mientras que grid maneja un sistema de filas y columnas que permiten posicionar elementos en dos dimensiones. Para ver más acerca de este display se puede acceder al siguiente [enlace](https://css-tricks.com/snippets/css/complete-guide-grid).

~~~css
parent-element {
  display: grid;
}
~~~
