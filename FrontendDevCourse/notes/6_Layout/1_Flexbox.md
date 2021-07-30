# Flexbox

Uno de los mayores problemas de CSS es alinear elementos. Para alinear un solo elemento se puede utilizar la posición `absolute` y colocar todos los valores en 0 con un margen automático, sin embargo la cosa se complica cuando se tiene más de un elemento. Como una solución a esto llega flexbox, el cual es un display para contenedores:

~~~css
.container {
  display: flex;
}
~~~

## Propiedades

Las propiedades de flexbox se dividen en 2:

- Propiedades del contenedor
- Propiedades de los items

### Propiedades del contenedor

Algunas de las propiedades más usadas con flex en el contenedor son:

- `flex-direction`.- Indica la forma en la que se oriemtan los elementos, pudiendo ser filas, columnas o de forma invertida en ambas. Por defecto la orientación es `row` (en fila)
- `flex-wrap`.- Este propiedad permite definir si los elementos se colocan uno debajo de otro al sobrepasar el ancho del contenedor. Por defecto el valor es `wrap`.
- `flex-flow`.- Es una forma abreviada de colocar la dirección y el wrap con una sola propiedad.
- `justify-content`.- Indica la forma de alinear los elementos horizontalmente.
- `align-items`.- Indica la forma de alinear los elementos verticalmente.

### Propiedades de los items

- `order`.- con esta propiedad se puede modificar el orden de los elementos.
- `flex-grow`.- Determina el crecimiento de un elemento en relación al contenedor.
- `flex-shrink`.- Esta propiedad define la reducción de tamaño de un objeto en relación al crecimiento del contenedor (lo opuesto a `flex-grow`).
- `flex-basis`.- Define un ancho base para que posteriormente se estire el elemento.
- `flex`.- Es una combinación de las propiedades `flex-grow`, `flex-shrink` y `flex-basis`.
- `align-self`.- Indica la alineación de forma vertical de un solo elemento.

Para ver más propiedades se puede acceder a la siguiente [documentación](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) o para practicar se puede acceder al siguiente [enlace](https://flexboxfroggy.com/#es).
