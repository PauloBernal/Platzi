# Mixins

Los mixins son uno de los aspectos más útiles en preprocesadores debido a que son porciones de código que se pueden reutilizar en cualquier parte del proyecto. Antes de crear mixins se debe definir los estilos similares para no tener demasiados.

## Creando mixins

Para crear un mixin se debe utilizar la palabar reservada `mixin` con un arroba por delante y después el nombre del mixin. En SCSS se encierra los estilos entre llaves mientras que en SASS no:

***SCSS***

~~~scss
@mixin mixin_name {
  *styles*
}
~~~

***SASS***

~~~sass
@mixin mixin_name
  *styles*
~~~

## Inluyendo mixins

Para incluir un mixin en cualquier parte del código se utiliza la palabra reservada `include` con un arroba (`@`) por delante seguida del nombre del mixin. En SCSS debe finalizar con un punto y coma:

***SCSS***

~~~scss
@include mixin_name;
~~~

***SASS***

~~~sass
@include mixin_name
~~~
