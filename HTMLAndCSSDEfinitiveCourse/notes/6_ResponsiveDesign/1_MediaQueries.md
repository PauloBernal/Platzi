# Responsive Design: media queries

Responsive design se basa en diseño multiplataforma para distintos dispositivos.

## Breakpoints

Los breakpoints (puntos de quiebre) son tamaños específicos en los que se genera un cambio al momento de diseñar un sitio web (un estilo para cada breakpoint). Al reescalar una ventana y llegar a un breakpoint cambia la disposición o tamaño de algunos elementos para que el sitio se vea mejor.

## Media queries

Los media queries son estilos que cambian al momento de llegar a un breakpoint. Existen distintas formas de realizar un sitio web y entre las más populares hoy en día están 'Mobile First' (primero dispositivos móviles) y 'Mobile Only' (solamente dispositivos móviles). La forma de realizar un media query es con la siguiente sintaxis:

~~~css
@media (*breakpoint*) {
    ...
}
~~~

Donde \*breakpoint\* va una o más de las siguientes condiciones:

- `min-width`
- `max-width`

haciendo alusión al tamaño de la pantalla del dispositivo o la ventana (en medidas absolutas como pixeles). En 'Mobile First' se empieza por los tamaños más pequeños hacia los tamaños más grandes.

## Media Queries en HTML

Usualmente se tiene más de una hoja de estilos dependiendo de la cantidad de dispositivos para los cuales se tenga soporte. Aparte de importar estos estilos con una etiqueta `<link>` como se hace usualmente, esta debe tener el atributo `media` y como valor la condición del media querie (tamaño de pantalla del dispositivo o ventana). Estas hojas de estilo se deben importar desde el más pequeño hasta el más grande.
