# Funciones

Las funciones en Less funcionan de forma distinta debido a que en vez de nosotros almacenar código Less nos brinda código ya preestablecido que permite ahorrar tiempo al momento de cambiar los estilos.

## Funciones útiles de Less

### Fade

Esta función permite agregar transparencia a cualquier color que se elija. Para utilizar la función se debe especificar como argumentos el color y la opacidad en porcentaje:

~~~less
fade(*color*, *percent*)
~~~

**Ejemplo** Se quiere agregar opacidad del 60% a un texto cualquiera (en un párrafo genérico) de color `#333333`:

~~~less
p {
  color: fade(#333333, 60%);
}
~~~

## Operaciones

En Less se puede realizar operaciones entre medidas absolutas y relativas con símbolos matemáticos. Por ejemplo operar pixeles con porcentajes o `rem` con porcentajes es posible en Less de forma nativa. Lo que se debe hace es colorcar la primera medida, después la operación (suma, resta, multiplicación o división) y después la segunda medida. En caso de tratarse de multiplicación o división la operación es con una constante:

~~~less
element {
  property: *measure1* operation *measure2*;
}
~~~

Para ver más funciones se puede revisar la documentación de Less en el siguiente [enlace](https://lesscss.org/functions/)
