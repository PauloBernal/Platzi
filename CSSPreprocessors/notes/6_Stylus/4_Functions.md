# Funciones

Las funciones son características de los preprocesadores parecidas a los mixins. La diferencia entre funciones y mixins de Stylus es que a la función se le pueden pasar parámetros, al mixin no.

## Definiendo funciones

Para definir una función se coloca primero el nombre de la función seguido de paréntesis en los que van los parámetros de la función. Abajo con identación va el código de la función:

~~~stylus
function_name(par1, par2, ... , parN)
  *code*
~~~

## Llamando funciones

Al llamar una función de Stylus se utiliza el nombre de la función seguido de paréntesis en los cuales van los b¿valores de los parámetros de la función:

~~~stylus
element
  property: function_name(value1, value2, ... , valueN)
  ...
~~~

## Funciones de Stylus

Stylus tiene algunas funciones que vienen incluidas con el preprocesador, entre estas se encuentra `alpha()` que permite agregar opacidad a los colores con el color y el porcentaje como parámetros.
