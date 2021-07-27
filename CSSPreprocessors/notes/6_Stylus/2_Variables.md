# Variables

Las variables son una de las características más utilizadas de Stylus debido a que permiten almacenar valores de colores, fuentes, tamaños, etc.

## Definiendo variables

Para definir variables en Stylus simplemente se coloca el nombre de la variable seguido de un símbolo de igual y el valor de la variable. Por buenas prácticas las variables deben declararse o importarse antes de los estilos:

~~~stylus
var_name = value
~~~

## Llamando variables

Para llamar variables en Stylus simplemente se debe colocar como valor el nombre de la variable (debido a esto no se debe colocar palabras reservadas en CSS como nombres de variables tales como `sans-serif`, `none`, `solid`, etc):

~~~stylus
element
  property: var_name
  ...
~~~
