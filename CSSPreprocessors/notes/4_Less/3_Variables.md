# Variables

Las variables son otra parte importante de Less y que permiten almacenar paletas, fuentes, tamaños, etc. predeterminados para los estilos.

## Declaración

Las variables en Less se declaran con un símbolo de arroba por delante (`@`) y después el nombre de la variable. Con dos puntos se especifica el valor de la variable y se cierra con punto y coma:

~~~less
@var_name: *value*;
~~~

## Llamada

Llamar una variable en Less es sumamente sencillo debido a que solamente se debe especificar el nombre de la variable con un arroba por delante (`@`):

~~~less
element {
  property: @var_name;
}
~~~
