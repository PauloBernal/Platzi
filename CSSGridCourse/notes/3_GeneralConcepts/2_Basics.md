# Conceptos fundamentales

Para trabajar con grid es importante tener en cuenta ciertos conceptos que vienen con esta característica de CSS, los cuáles son:

- Lines
- Tracks
- Cell
- Area
- Gutters
- Grid Axis
- Grid Row
- Grid Column

## Lines, tracks, cell, area

Cómo se vio anteriormente, las propiedades en grid se dividen en propiedades del padre y propiedades de los hijos. En este caso las propiedades del padre son: `lines`, `track`, `area` y del hijo: `cell`.

### Lines

Esto hace referencia a las líneas de la cuadrícula. Los límites que separan las celdas de la grilla son "lines".

### Track

Es un conjunto de celdas de la cuadrícula que van en un solo sentido. Las filas y columnas son ejemplos de "tracks".

### Area

Un "area" es un conjunto de celdas dentro de la cuadrícula. Es posible caracterizar áreas completas en CSS.

### Cell

Una "cell" es una celda en la cuadrícula. Cada una de las pequeñas divisiones de la grilla se denominan "cell".

## Gutters, grid axis, grid row, grid column

En este caso las propiedades del padre son: `gutters` y `grid-axis`, mientras que las del hijo son: `grid-row`, `grid-column`, `grid-axis`.

### Gutters

Los gutters son los espacios entre filas y columnas. En CSS se pueden personalizar dependiendo de la fila o columna.

### Grid axis

Esta propiedad hace referencia a la alineación, ya sea izquierda a derecha, derecha a izquierda, arriba a abajo o abajo a arriba. Grid axis significa "eje de la grilla".

### Grid Row

Hace referencia a las filas de la grilla. Es importante recalcar que debido a que se puede modificar el eje de la grilla no siempre una fila será horizontal.

### Grid Column

Es similar al Grid Row, pero haciendo referencia a las columnas.

## Usando grid

Es importante saber maquetar el sitio dentro de la grilla, posicionando las distintas secciones en un solo layout. Se puede realizar un boceto general para ubicarse cómo posicionar cada elemento. Lo que no es recomendable es utilizar una sola cuadrícula para posicionar todos los elementos de la página, es preferible utilizar sub-cuadrículas para posicionar elementos de secciones específicas. Igualmente es recomendable no utilizar un gran número de filas y columnas, debido a que esto puede ocasionar confusión y que el sitio quede desorganizado en vez de bien posicionado.
