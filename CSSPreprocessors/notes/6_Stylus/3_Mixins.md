# Mixins

Como ya se explicó anteriormente, los mixins son pedazos de código que se pueden reutilizar en otras partes del documento. En Stylus también son una de las características más utilizadas debido a que permiten reducir y modificar de mejor forma el código.

## Creando un mixin

Para crear un mixin en Stylus se debe colocar el nombre del mixin seguido de paréntesis y abajo con identación los estilos que contiene el mixin:

~~~stylus
mixin_name()
  *styles*
  ...
~~~

## Llamando un mixin

Para llamar un mixin en Stylus simplemente en la parte de estilos de un elemento se coloca como un estilo más el nombre del mixin seguido de paréntesis:

~~~stylus
element
  mixin_name()
  *element styles*
  ...
~~~
