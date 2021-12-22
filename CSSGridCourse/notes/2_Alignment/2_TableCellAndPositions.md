# Table-cell y positions

## Técnica table-cell

Con esta técnica se hace uso de tres propiedades para alinear elementos:

- display: table-cell
- text-align
- vertical-align

La primera de estas convierte cualquier elemento de html en una tabla con la cuál se puede trabajar (sin necesidad de ser un elemento tabla).

## Técnica position

Con esta técnica se utiliza la propiedad `position` para alinear los elementos por medio de posiciones. Para esto se puede colocar una posición `relative` en los contenedores y una posición `absolute` en los elementos. Con las propiedades:

- top
- bottom
- right
- left

Se puede posicionar los elementos, con distancias respecto al borde de sus contenedores. Otra forma de mover los elementos de su posición inicial es haciendo uso de la propiedad `transform` y la función `translate()` con parámetros `x` e `y` que hacen referencia al desplazamiento del mismo desde el centro del elemento
