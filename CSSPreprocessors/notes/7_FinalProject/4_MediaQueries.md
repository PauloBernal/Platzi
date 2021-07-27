# Funciones y mixins para media queries

En el caso de media queries puede ayudar bastante el tener funciones y mixins con tamaños preestablecidos. Por ejemplo tener un `large`, `medium` y `small` como dispositivos conun tamaño de pantalla ya definido. Un ejemplo de esto sería el siguiente mixin:

~~~sass
@mixin media($size)
  @if $size == small
    @media screen and (min-width: 320px)
      @content
  @else if == medium
    @media screen and (min-width: 600px)
      @content
  @else if == large
    @media screen and (min-width: 800px)
      @content
~~~
