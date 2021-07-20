# Notas de la sección de 'header'

## Maquetación del Header

Por buenas prácticas todo sitio web debe tener únicamente un encabezado `<h1>`. Usualmente el `<header>` se compone de un título, una descripción, un logotipo o imagotipo y una  barra de navegación (esta también puede ir en la sección principal o en el footer)

## Implementando BEM

Es una metodología que ayuda a nombrar clases en HTML para manejar los estilos de mejor forma. Con BEM se nombran clases de forma escriptiva lo que ayuda a entender a qué elemento se refieren las clases para cualquier persona.

## Uso de linear-gradient

Como lo dice su nombre, `linear-gradient` es una función de css que permite crear degradados de forma lineal. Para esto se debe especificar la propiedad seguida de la función que toma como parámetros la inclinación en grados sexagesimales, el color inicial con porcentaje que ocupa y color final con porcentaje que ocupa:

~~~css
element {
    property: linear-gradient(*angle*deg, *color1* *percent1*%, *color2* *percent2*%);
}
~~~

Usualmente se utiliza para crear fondos degradados en contenedores. Para cambiar el tamaño del salto de línea en CSS se utiliza la propiedad `line-height`:

~~~css
element {
    line-height: *size*;
}
~~~

## Botón flotante

Para realizar un botón flotante usualmente se utiliza posición `absolute`, esto debido a que permite posicionar el botón en cualquier lugar de la ventana.

### Función `calc()`

Una función muy útil de CSS es `calc()`, la cuál permite operar entre medidas absolutas y relativas:

~~~css
element {
    property: calc(*v1* *operation* *v2*)
}
~~~

Por ejemplo esto permite centrar elementos con una posición absoluta conociendo el centro de estos (la mitad de su ancho):

~~~css
element {
    position: absolute;
    width: 300px;
    left: calc(50% - 150px);
}
~~~

### Añadiendo íconos de fondo

Para añadir un ícono o una imagen de fondo se puede utilizar la propiedad `background-image` y como valor la ruta de la imagen entre comillas simples y dentro de la función `url()`:

~~~css
element {
    background-image: url('/route/')
}
~~~
