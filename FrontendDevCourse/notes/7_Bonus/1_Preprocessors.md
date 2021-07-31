# Preprocesadores

Uno de los problemas más grandes en CSS es que casi siempre las hojas de estilo llegan a ser muy extensas debido a la cantidad de elementos que hay en una página. Esto debido a que al querer modificar algo puede ser mucho más complicado encontrar el elemento en específico. Como una colución a esto nacieron los preprocesadores, herramientas que permien modularizar el código y hacer uso de otras funcionalidades como variables, funciones, mixins, etc.

## Funcionamiento

Cada preprocesador tiene una sintaxis distinta pero el funcionamiento por detrás es el mismo, convierte los archivos modularizados en una sola hoja de estilos compilando el resultado en un solo archivo CSS. Los preprocesadores más conocidos son SASS, Stylus y Less; y entre todos estos el más utilizado es SASS (más que todo por su sistema de modularización). Con los siguientes enlaces se puede acceder a la documentación de los preprocesadores antes mencionados:

- [SASS 1](https://sass-lang.com/guide)
- [SASS 2](https://github.com/teffcode/sass-workshop)
- [Less](https://lesscss.org/)
- [Stylus](https://stylus-lang.com/)

## Instalación de SASS

Hay tres alternativas para insatalar SASS, una con `npm`, otra con Chocolatey Package Manager y otra para MAC:

***npm***

~~~shell
$ npm install -g sass
~~~

***Chocolatey Package Manager***

~~~shell
$ choco install sass
~~~

***MAC OSX***

~~~shell
$ brew install sass/sass/sass
~~~

## Compilación con SASS

Para compilar un archivo en SASS y que se compile a CSS con cada cambio realizado se hace uso del comando:

~~~bash
$ sass --watch /sass-route/ /css-route/
~~~

Donde `/sass-route/` es la ruta del archivo SASS a compilar y `/css-route/` es la ruta de destino del archivo compilado.

## Características de SASS

### Variables

Las variables son lugares en memoria en los cuales se almacena un valor. Para definir una variable en SASS se hace uso del símbolo de dólar (`$`), al igual que para llamarla:

~~~sass
// Def var

$var_name: value


// Call var

element
  property: $var_name
~~~

### Anidamiento

El anidamiento es la forma en que se relacionan contenedores con elementos dentro de estos (también se usa para especificidad). Para anidar elementos en SASS simplemente se debe colocar el selector del elemento descendiente identado respecto al selector del contenedor:

~~~sass
parent
  *parent styles*

  child
    *child styles*
~~~

### Herencia

Cuando se repiten muchos estilos puede reultar conveniente heredar los mismos de una clase. Para esto se utiliza la palabra reservada `@extend` con el arroba por delante seguido del nombre de la clase:

~~~sass
.class_name
  *styles*

element 
  @extend .generic-class
  ...
~~~

### Mixins

Los mixins son una forma de reutilizar un pedazo de código de forma específica. Para crear un mixin se utiliza la palabra reservada `@mixin` con el arroba por delante seguido del nombre del mixin; en este caso los estilos se colocan en la parte de abajo con identación. Para llamar al mixin se utiliza la palabra reservada `@include` con el arroba por delante seguida del nommbre del mixin:

~~~sass
@mixin mixin_name
  *mixin styles*

element
  @include mixin_name
  ...
~~~
