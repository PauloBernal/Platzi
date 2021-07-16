# Flexbox layouts

## Alineando verticalmente

Una de las propiedades más útiles para lograr esto es `align-items`, una propiedad que alinea de forma vertical los elementos dentro del elemento padre. Algunos valores para esta propiedad son:

- `flex-start`.- Es el estilo pñor defecto y posiciona todos los elementos en la parte superior del elemento padre:

~~~css
element {
  align-items: flex-start;
}
~~~

- `center`.- Centra de forma vertical los elementos respecto a la altura del elemento padre:

~~~css
element {
  align-items: center;
}
~~~

- `flex-end`.- Coloca todos los elementos posicionados en la parte inferior del elemento padre.

~~~css
element {
  align-items: flex-end;
}
~~~

- `stretch`.- Estira la altura de los elementos para ocupar el 100% de la altura del contenedor padre:

~~~css
element {
  align-items: stretch;
}
~~~

- `baseline`.- Cambia la altura de los elementos para que sean del tamaño de su contenido:

~~~css
element {
  align-items: baseline;
}
~~~

## Ordenando

Se puede alterar el orden de elementos dentro de un flex. Es importante tomar en cuenta que los elementos con un orden establecido se colocan a la derecha y los elementos sin orden establecido se colocan a la izquierda. Para cambiar el orden se utiliza la propiedad `order`, la cual va dentro de los elementos hijo, no del elemento padre como todas las anteriores propiedades de flex.

~~~css
element {
  order: *N*;
}
~~~

## Estirando elementos

Para layouts responsive muchas veces se quiere que los elementos dentro de el elemento padre crezcan en proporción al crecimiento de la ventana. Para esto existe una propiedad llamada `flex-grow`, la cuál hace crecer a los elementos hijo para ocupar el 100% del espacio horizontal con el resto de elementos. Dicha propiedad forma parte de los elementos hijo:

~~~css
element {
  flex-grow: *N*;
} 
~~~

Donde 'N' va el número de posiciones extra que ocupará el elemento (en función del espacio sobrante). Si más de un elemento tiene esta propiedad el espacio resultante se divide en forma fraccionaria dependiendo del valor de 'N' en cada elemento.

Para determinar el tamaño por defecto de un elemento dentro de un elemento padre con display flex existe una propiedad llamada `flex-basis`. En esta se coloca similar al width un tamaño, sin embargo en este caso crecerá o se reacomodará con wrap conforme se cambie el tamaño del contenedor padre:

~~~css
element {
  flex-basis: *size*;
}
~~~
