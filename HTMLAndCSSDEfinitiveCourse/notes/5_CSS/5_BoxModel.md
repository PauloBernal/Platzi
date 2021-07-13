# Modelo de caja

Todos los elementos HTML son cuadrados (aunque visualmente parezcan circulares). Estos se componen de 4 partes principales:

- Contenido
- Padding
- Border
- Margin

Se llama modelo de caja a los estilos que se aplican a los elementos renderizados como cajas. Todos estos a excepción del contenido se pueden modificar en 4 aspectos:

- Top.- Parte superior
- Bottom.- Parte inferior
- Right.- Parte derecha
- Left.- Parte izquierda

## Margin

Se denomina `margin` al espacio o distancia que tiene este un elemento hacia el exterior.

## Border

Se denomina `border` al borde del elemento. Este por defecto es invisible aunque se puede determinar un colo y un ancho utilizanco CSS

## Padding

Se denomina `padding` a un espacio interno que va del borde del elemento hacia el contenido del mismo.

## Contenido

El contenido puedeser texto, imágenes, etc. Todo lo que va dentro del elemento se denomina contenido. Las dimensiones de este se dividen en alto (`height`) y ancho (`width`).

## Propiedades laterales

Como ya se explicó, se puede modificar en cuatro aspectos las propiedades del modelo de caja (arriba, abajo, izquierda derecha).

### Modificando todos

Para modificar todos se coloca solamente el nombre de la propiedad seguido de un valor:

~~~css
element {
    property: *v*;
}
~~~

### Modificando por disposición (vertical u horizontal)

Para modificar la parte superior e inferior con un solo valor y la parte derrecha e izquierda con otro valor se colorca el nombre de la propiedad seguido de dos valores, el primero hace referencia a las posiciones verticales y el segundo a las horizontales:

~~~css
element {
    property: *v1_vertical* *v2_horizontal*
}
~~~

También se puede hacer con 3 posiciones (arriba, horizontal, abajo). Esto haciendo uso de 3 valores en el que el primero se refiere a la parte superior, el segundo a los laterales horizontales y el tercero a la parte inferior:

~~~css
element {
    property: *v1_top* *v2_horizontal* *v3_bottom*
}
~~~

### Modificando individualmente

Por último hay dos formas de modificar individualmente las distancioas y/o tamaños. El primero es colocar el nombre de la propiedad seguido del nombre de la dimensión a modificar separada por un guión.

~~~css
element {
    property-dim: *v*;
}
~~~

La segunda es colocar el nombre de la propiedad seguida de cuatro valores, el primero va a la parte superior, el segundo a la derecha, el tercero a la parte inferior y el último a la izquierda:

~~~css
element{
    property: *v1_top* *v2_right* *v3_bottom* *v4_left*;
}
~~~

## Reseteando estilos por defecto

Como el navegador aplica estilos por defecto existe algo llamado selector universal, que permite modificar los estilos por defecto (*):

~~~css
* {
    property1: value1;
    ...
}
~~~

Para evitar que al añadir un padding o un borde se salga el contenido del marco existe una propiedad llamada `box-sizing`. Esta permite alterar el modelo de caja para tener un tamaño o proporción constantes. Esto sirve sobretodo con el valor `border-box` ddebido a que considera desde el contenido hasta el borde del elemento el `width`, haciendo cálculos para que el elemento no exceda el ancho establecido:

~~~css
element {
    box-sizing: border-box;
}
~~~

Como una buena práctica el selector universal se puede colocar de la siguiente forma:

~~~css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
~~~
