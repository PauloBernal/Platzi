# Alineamiento de elementos en el contenedor

Al alinear en el contenedor automáticamente todos los elementos se alinean de la misma forma, por lo que más adelante se verá como personalizar la alineación  a partir de propiedades de los elementos hijo. Las propiedades de alineamiento en el contenedor se dividen en 2:

- Elementos: `justify-items`, `align-items`, `place-items`
- Contenido: `justify-content`, `align-content`, `place-content`

## Propiedades

### Diferencias entre `items` y `content`

Es importante reconocer las diferencias entre estos debido a que funcionan de distinta forma, siendo las propiedades con `items` referentes a la alineación de los elementos dentro de las celdas y las propiedades con `content` referentes al posicionamiento de las celdas respecto a la grilla o el elemento contenedor. Es importante tomar en cuenta que no se manejan alineaciones horizontales ni verticales, sino alineaciones `inline` y `block` dado que el sentido horizontal o vertical se puede modificar con propiedades como `transform`.

### Propiedades `justify`

Estas propiedades permiten modificar la alineación inline de los elementos, es decir, cómo se disponen los elementos posicionados uno al lado del otro. Ambas propiedades, `justify-items` y `justify-content`, poseen los siguientes valores:

- `start`.- Posiciona los elementos o celdas pegados al inicio de la fila.
- `center`.- Centra los elementos o celdas.
- `end`.- Posiciona los elementos o celdas pegados al final de la fila.
- `stretch`.- Permite que los elementos o celdas abarquen la totalidad del espacio en fila.
- `space-between` (sólo para content).- Posiciona las celdas de tal forma que hay un espacio de igual tamaño entre ellos, pero no hay ningún espacio respecto al borde.
- `space-evenly` (sólo para content).- Posiciona las celdas de tal forma que hay un espacio de igual tamaño entre ellos, incluyendo en este caso también un espacio de igual tamaño respecto al borde.
- `space-around` (sólo para content).- Posiciona las celdas de tal forma que hay un espacio de igual tamaño entre ellos pero un espacio mejor proporcionado respecto al borde.

~~~css
.container {
  justify-items: *value*;
  justify-content: *value*;
}
~~~

### Propiedades `align`

Estas propiedades son similares a `justify`, con la diferencia de que permiten modificar la alineación block de los elementos, es decir, cómo se comportan los elementos en bloque respecto a una alineación "vertical". Ambas propiedades, `align-items` y `align-content`, poseen los siguientes valores:

- `start`.- Posiciona los elementos pegados al inicio de la columna.
- `center`.- Centra los elementos.
- `end`.- Posiciona los elementos pegados al final de la columna.
- `stretch`.- Permite que los elementos o celdas abarquen la totalidad del espacio en columna.
- `space-between` (sólo para content).- Posiciona las celdas de tal forma que hay un espacio de igual tamaño entre ellos, pero no hay ningún espacio respecto al borde.
- `space-evenly` (sólo para content).- Posiciona las celdas de tal forma que hay un espacio de igual tamaño entre ellos, incluyendo en este caso también un espacio de igual tamaño respecto al borde.
- `space-around` (sólo para content).- Posiciona las celdas de tal forma que hay un espacio de igual tamaño entre ellos pero un espacio mejor proporcionado respecto al borde.

~~~css
.container {
  align-items: *value*;
  align-content: *value*;
}
~~~

### Propiedades `place`

En caso de no querer escribir por separado las propiedades y querer utilizar una sola, se puede utilizar las propiedades `place`, las cuales son respectivamente `place-items` y `place-content`. Realizan lo mismo que `align` y `justify` pero en una sola, y ambos valores deben separarse por un '`'/`' (slash):

~~~css
.container {
  place-items: <align-items> / <justify-items>;
}
~~~
