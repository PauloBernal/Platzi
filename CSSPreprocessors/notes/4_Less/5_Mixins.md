# Mixins

Como ya se dijo anteriormente, los mixins son pedazos de código que se pueden reutilizar en otra parte del código.

## Declarando mixins

Para declarar mixins en Less se utiliza un punto por delante y después el nombre del mixin. Entre llaves se coloca el bloque de estilos que se reutilizará con el mixin:

~~~less
.mixin_name {
  *styles*
}
~~~

## Llamando mixins

Para utilizar los estilos dentro del bloque de un mixin enotra parte del código solamente se necesita colocar el nombre del mixin con el punto por delante:

~~~less
.mixin_name;
~~~

## Parámetros (mixins como funciones)

Un mixin también puede recibir un parámetro como una función. Para lograr esto se utiliza la misma sintaxis que se utiliza para un mixin con la diferencia de que al momento de declarar un mixin se especifica variables provisionales entre paréntesis y al momento de llamar al mixin se colocan como argumentos los valores de dichas variables:

***Declarando mixin***

~~~less
.mixin_name(@var1, @var2, ..., @varN) {
  *styles*
}
~~~

***Llamando mixin***

~~~less
.mixin_name(value1, value2, ... , valueN)
~~~
