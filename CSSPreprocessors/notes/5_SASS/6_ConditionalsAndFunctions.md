# Condicionales y ciclos

Los condicionales y los ciclos son estructuras de programación que ejecutan cierto pedazo de código dependiendo de una condición.

## Ciclos

Los ciclos son estructuras que repiten un pedazo de código un cierto número de veces dependiendo de una cnodición o iteración. Para generar un bucle en SCSS y SASS se utiliza la palabra reservada `each` con un arroba (`@`) por delante. En este caso se llega a utilizar dos variables provisionales para iterar, una que hace referencia al elemento y otra que hace referencia al valor separadas por dos puntos y los pares de variables se separan con comas:

***SCSS***

~~~scss
@each $var_element, $var_value in (el1: val1, el2: val2, ... , elN: valN) {
  #{$var_element} {
    property: $var_value;
    ... 
  }
}
~~~

***SASS***

~~~sass
@each $var_element, $var_value in (el1: val1, el2: val2, ... , elN: valN)
  #{$var_element}
    property: $var_value
    ...
~~~

## Condicionales

Los condicionales son estructuras que al verificar si se cumple una condición ejecutan un pedazo de código. Los condicionales se generan con la palabra reservada `if` y un arroba (`@`) por delante. Después de esto se coloca la condición y abajo el código a ejecutarse. Si se quiere ejecutar una instrucción en el caso contrario se utiliza la palabra `else` igualmente con un arroba (`@`) por delante y abajo el bloque de código. En SCSS debe haber llaves y punto y coma.

***SCSS***

~~~scss
@if *condition* {
  *styles*
}
@else {
  *styles*
}
~~~

***SASS***

~~~sass
@if *condition*
  *styles*
@else
  *styles
~~~
