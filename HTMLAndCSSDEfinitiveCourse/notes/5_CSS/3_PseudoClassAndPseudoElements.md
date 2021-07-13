# Pseudo clases y pseudo elementos

Existen diversas metodologías para colocar clases a los elementos HTML. Una de estas es BEM (Block Element Modifier), la cúal ayuda al momento de elegir el nombre correcto para la clase de un conjunto de elementos. Para ver más acerca de BEM se puede ingresar al siguiente [enlace](https://en.bem.info/methodology/faq/#why-bem).

El navegador añade a algunos elementos como listas o botones estilos por defecto. Esto puede variar dependiendo del navegador, sin embargo las diferencias no suelen ser demasiadas.

## Anidando elementos

Para especificar un elemento que se encuentra dentro de otro en CSS primero se especifica el elemento padre y después el elemento hijo. Se puede especificar múltiples elementos anidados.

### HTML

~~~html
<tag1>
    <tag2>
        ...
            <tagN></tagN>
        ...
    <tag2>
</tag1>
~~~

### CSS

~~~css
tag1 tag2 ... tagN {
    property1: value1;
    property2: value2;
    ...
    propertyN: valueN;
}
~~~

## Pseudoclases

Las pseudo clases son estados que tienen los elementos. Se puede aplicar distintos estilos a los elementos dependiendo del estado en el que se encuentren. Para especificar una pseudoclase en CSS se utilizan dos puntos (`:`)

~~~css
element:pseudoclass {
    ...
}
~~~

Entre las pseudoclases se encuentran:

- `hover`.- Se refiere a cuando el mouse está sobre el elemento

~~~css
element:hover {
    ...
}
~~~

- `active`.- Se refiere a cuando el elemento está activo (se hace click sobre él)

~~~css
element:active {
    ...
}
~~~

- `focus`.- Se refiere a cuando un elemento tiene el foco (fue seleccionado)

~~~css
element:focus {
    ...
}
~~~

Para ver una lista completa de pseudoclases se puede acceder al siguiente [enlace](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes)

## Pseudo elementos

Los pseudo elementos hacen referencia a partes de un elemento. Por ejemplo el pseudo elemento `after` hace referencia a la parte después del comtenido de un elemento, el pseudo elemento `before` hace referencia a la parte antes del contenido. Para añadir estilos a un pseudo elemento se utiliza dos veces el símbolo de dos puntos (`::`)

~~~css
element::pseudoelement {
    ...
}
~~~

Para ver una lista de pseudo elementos se puede ir al siguiente [enlace](https://developer.mozilla.org/es/docs/Web/CSS/::selection)

Se puede cambiar el contenido de un pseudoelemento haciendo uso del atributo `content`

~~~css
element::pseudoelement {
    content: "new content";
}
~~~

## Estilos útiles

- `background-color`.- Permite cambiar el color de fondo del elemento al que se hace referencia. En CSS los colores se pueden poner en formato escrito (red, blue, yellow, etc), formato rgb (rgb(v1, v2, v3)) o formato hexadecimal (#NNNNNN).

~~~css
element {
    background-color: *color*;
}
~~~

- `color`.- Permite cambiar el color de letras e íconos. Los formatos son los mismos que para `background-color`

~~~css
element {
    color: *color*;
}
~~~

- `font-size`.- Permite modificar el tamaño de la fuente. Hay distintas unidades como ser pixeles (px), unidades reltivas (em, rem), centímetros (cm), etc.

~~~css
element {
    font-size: *size*;
}
~~~

- `margin`.- Permite modificar la distancia y posición del elemento respecto a otros elementos externos. Igualmente se usan las medidas de tamaño o distancia

~~~css
element {
    margin: *len*;
}
~~~

- `list-style`.- Permite modificar los estilos por defecto de una lista

~~~css
element{
    list-style: *style*;
}
~~~

- `padding`.- Permite modificar las medidas internas del elemento (desde los bordes hacia en contenido u otros elementos dentro del elemento padre)

~~~css
element {
    padding: *len*;
}
~~~

- `display`.- Permite modificar la estructura de renderizado de los elementos (en línea, en bloque, etc)

~~~css
element {
    display: *value*;
}
~~~

- `border`.- Permite añadir un borde al elemento. Por lo general se especifica el tamaño del borde, después el tipo de borde y finalmente el color del mismo.

~~~css
element {
    border: *size* *type* *color*;
}
~~~

- `border-radius`.- Redondea las esquinas del elemento con un radio especificado. El radio se especifica en las mismas unidades que el tamaño o la distancia.

~~~css
element {
    border-radius: *radius*;
}
~~~
