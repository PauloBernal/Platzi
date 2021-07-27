# Imports y Extends

Al momento de estructurar el código la modularización es un aspecto clave. En SASS hay dos formas de incluir archivos externos o estilos de otra parte del código en SCSS y SASS, los `import` y los `extend`.

## Extend

Los extend son formas de copiar los estilos completos de un elemento para usarlos en otro elemento. Esto se hace colocando un arroba y seguido la palabra `extend` con el selector del elemento del cuál se copiarán los estilos:

***SCSS***

~~~scss
element1 {
  *element1 styles*
}

element2 {
  @extend element1;
}
~~~

***SASS***

~~~sass
element1
  *element1 styles*

element2
  @extend element1;
~~~

***CSS***

~~~css
element1 {
  *element1 styles
}

element2 {
  *element1 styles*
}
~~~

## Imports

Como se dijo anteriormente una de las mejores características de SASS es la modularización que permite tener en diversos archivos los estilos de distintos componentes e incluso las variables. Para los nombres de archivos de los componentes se coloca un guión bajo por delante para indicar que no se debe compilar al tratarse de un componente. Para importar archivos en SCSS y SASS se utiliza la palabra `import` con un arroba (`@`) por delante y después con separación de un espacio se coloca la ruta del componente entre comillas. En SCSS es importante utilizar el punto y coma al final de la línea:

***SCSS***

~~~scss
@import "/route/_component";
~~~

***SASS***

~~~sass
@import "/route/_component"
~~~

Si se tiene un  archivo en el que se almacenen variables siempre debe ir este primero debido a que si otro archivo requiere una variable y no está definida antes saltará un error al momento de compilar.
