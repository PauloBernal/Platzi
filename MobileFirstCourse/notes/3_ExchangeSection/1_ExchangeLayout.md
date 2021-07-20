# Notas de la sección de intercambio

## Background image

Cuando se tiene una imagen de fondo en caso de que el contenedor sea más grande que esta empezará a repetirse, se posiciona a la izquierda, etc. Estos aspectos se pueden modificar con distintos atributos de CSS como ser:

- `background-repeat`.- Especifica si se repetirá la imagen de fondo a lo largo del contenedor. Para evitar que se repita se coloca el valor `no-repeat`.

~~~css
element {
    background-repeat: *value*;
}
~~~

- `background-size`.- En caso de que la imagen no sea del tamaño del contenedor es posible modificar su tamaño para que cubra todo (`cover`), que sea de su tamaño original (`auto`), que se adapte a la altura del contenedor (`contain`), etc.

~~~css
element {
    background-size: *value*;
}
~~~

- `background-position`.- Puede que se busque posicionar la imagen de fondo de forma distinta, ya sea a la izquierda, centro, derecha, etc. Para ello existe este parámetro.

~~~css
element {
    background-position: *value*;
}
~~~

## Tablas HTML

Las tablas son una forma de organizar contenido en filas y columnas. HTML tiene sus propias etiquetas para definir tablas, filas y columnas. La base para crear una tabla es la etiqueta `<table>`. Dentro de la tabla se colocan las filas con la etiqueta `<tr>` y dentro de las filas se colocan las columnas con la etiqueta `<td>`.

~~~html
<table>
    <tr>
        <td></td>
        <td></td>
        ...
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        ...
        <td></td>
    </tr>
    ...
    <tr>
        <td></td>
        <td></td>
        ...
        <td></td>
    </tr>
</table>
~~~

## Problemas de herencia

Al utilizar especificidad puede haber ciertos problemas con el tema de estilos heredados. Para poder corregir ese problema se puede utilizar estilos con ID o clases para cambiar o resetear dichos estilos.