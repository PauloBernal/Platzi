# Sección de planes

## Line height

Una de las propiedades que ayuda a corregir interlineados y alturas de bloques de texto es `line-height`. Con este propiedad se especifica la altura de línea que permite controlar las características antes mencionadas.

~~~css
element {
    line-height: *size*;
}
~~~

## Overflow

A veces el contenido puede superar el tamaño del elemento padre o incluso el tamaño de la ventana. Esto puede ser perjuicioso debido a que el overflow se da en toda la ventana y se rompe todo el diseño. Como una solución existen tres propiedades, `overflow-x` que permite controlar cuando el contenido sobrepasa al contenedor de forma horizontal, `overflow-y` que permite controlar cuando el contenido sobrepasa al contenedor de forma vertical y `overflow` que permite controlar el flujo tanto horizontal como vetical. Algunos valores para estas propiedades son:

- `hidden`.- Oculta todo el contenido que sobrepasa al contenedor.

~~~css
element {
    overflow: hidden;
}
~~~

- `scroll`.- Genera un scroll para visualizar el contenido dentro del contenedor.

~~~css
element {
    overflow: scroll;
}
~~~

- `visible`.- Se muestra el contenido que sobrepasa al contenedor

~~~css
element {
    overflow: visible;
}
~~~

## Sección de terjetas con scroll

En algunas páginas de productos se puede observar los estilos en tarjetas dentro de un contenedor, las cuales se recorre con un scroll o botones. Son estilos espcíficos con propiedades de CSS que en muchos casos permiten realizar dichos efectos. Primero el contenedor padre debe tener `overflow-x: scroll` para utilizar un scroll que permita visualizar todos los elementos dentro de él de forma horizontal:

~~~html
<parent>
    <child></child>
    <child></child>
    ...
    <child></child>
</parent>
~~~

~~~css
parent {
    overflow: scroll;
}
~~~

Posteriormente se utiliza la propiedad `overflow-behavior` en el elemento padre para controlar el comportamiento del scroll. Para lograr el efecto deseado se utiliza el valor `contain`:

~~~css
parent {
    overflow-behavior: contain;
}
~~~

Después se ajusta el desplazamiento con la propiedad `scroll-snap-type` al elemento más cercano de forma horizontal con `x proximity`.

~~~css
parent {
    scroll-snap-type: x proximity;
}
~~~

En los elementos hijo se especifica la alineación de la propiedad anteriormente mencionada con `scroll-snap-align` y como se quiere centrar se utiliza el valor `center`.

~~~css
child {
    scroll-snap-align: center;
}
~~~

Los estilos completos serían:

~~~css
parent {
    display: flex;
    overflow: scroll;
    overflow-behavior: contain;
    scroll-snap-type: x proximity;
}

child {
    scroll-snap-align: center;
}
~~~

## Gap

Para crear un espaciado entre elementos dentro de un flex o un grid existe una propiedad que se coloca en el elemento padre la cuál se llama `gap`:

~~~css
parent {
    display: flex;
    gap: *length*;
}
~~~

Esta es una propiedad experimental por lo que en algunos navegadores todavía no está incluida. Para ver que navegadores tienen disponibles ciertas propiedades se puede ir al sitio web en el siguiente [enlace](https://caniuse.com/)
