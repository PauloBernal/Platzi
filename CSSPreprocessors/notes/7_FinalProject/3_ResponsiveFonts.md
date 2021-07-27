# Manejo de fuentes responsivas con mixins

Lo mejor al momento de crear un sitio web es trabajar con REM debido a que permite reescalar las fuentes en caso de que el usuario tnega un problema de vista. Para esto se pueden crear funciones y mixins en SASS que ayuden a calcular pixeles y convertirlos en REM. La primera función denominada `calculateRem()` debe tener como parámetro el tamaño del elemento en pixeles y debe calcular a cuantos REM equivale la fuente dividiendo entre el tamaño de fuente del elemento raíz (html):

~~~sass
@function calculateRem($size)
  $remSize: $size / 16px
  @return $remSize * 1rem
~~~

Seguidamente se debe crear un mixin en el que vaya incluída dicha función y el `line-height` por defecto:

~~~sass
@mixin font-size($size)
  font-size: $size
  font-size: calculateRem($size)
  line-height: calculateRem($size)*1.5
~~~
