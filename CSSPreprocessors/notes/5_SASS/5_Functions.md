# Funciones

Las funciones son una de las características más utilizadas en los preprocesadores. Su principal utilidad es realizar cálculos u otras operaciones con medidas o variables.

## Definiendo funciones

Para definir una función se utiliza la palabra reservada `function` con un arroba (`@`) por delante. Después de eso se coloca el nombre de la función y paréntesis que indican que se trata de una función (en dichos paréntesis se pueden definir argumentos de la función con variables provisionales que llevan un símbolo de dolas por delante). En SCSS las instrucciones se colocan dentro de llaves mientras que en SASS simplemente se utiliza la identación. Para retornar un valor con la función se utiliza la palabra reservada `return` con un arroba (`@`) por delante:

***SCSS***

~~~scss
@function function_name($arg1, $arg2, ..., $argN) {
  *instructions*
  @return *value*
}
~~~

***SASS***

~~~sass
@function function_name($arg1, $arg2, ..., $argN)
  *instructions*
  @return *value*
~~~

## Llamando funciones

Para llamar una función se coloca el nombre de la función seguido de paréntesis en los cuales van los valores de los argumentos. La función va como valor de la propiedad de un elemento:

***SCSS***

~~~scss
element {
  property: function_name(value1, value2, ... , valueN );
}
~~~

***SASS***

~~~sass
element
  property: function_name(value1, value2, ... , valueN )
~~~
