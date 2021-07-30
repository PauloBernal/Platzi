# Grid

Con CSS Grid se puede manipular todo el layout de la página. Algunos sitios para consultar documentación acerca de CSS Grid son:

- [CSS Tricks](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS/grid)
- [Jen Simmons](https://labs.jensimmons.com/)
- [Layout Land](https://www.youtube.com/channel/UC7TizprGknbDalbHplROtag)
- [Grid Garden](https://cssgridgarden.com/#es)

## Iniciando con Grid

Al igual que con flexbox, grid debe ser el display del contenedor (o inline-grid):

~~~css
.container {
  display: grid | inline-grid;
}
~~~

Una de las cosas más importantes al momento de trabajar con Grid es definir las columnas y las filas de la cuadrícula. Para esto existen las propiedades `grid-template-columns` y `grid-template-rows`, definiendo los tamaños de las columnas y filas respectivamente separadas por espacios:

~~~css
.container {
  display: grid;
  grid-template-columns: *size1* *size2* ... *sizeN*;
  grid-template-rows: *size1* *size2* ... *sizeN*;
}
~~~

## Elementos

Para definir en que fila o columna inicia y termina un elemento se utiliza las propiedades:

- `grid-column-start`.- Indica en que columna inicia el elemento.
- `grid-column-end`.- Indica en que columna termina el elemento.
- `grid-row-start`.- Indica en que fila inicia el elemento.
- `grid-row-end`.- Indica en que fila termina el elemento.

Estas propiedades se pueden abreviar en solamente dos:

- `grid-column`.- Indica las columnas en que inicia y termina el elemento.
- `grid-row`.- Indica las filas en que inicia y termina el elemento.

Los índices inicial y final se separan por un slash (`/`):

~~~css
.item {
  grid-column: *start* / *end*;
  grid-row: *start* / *end*;
}
~~~

### Span

Si se quiere especificar un número relativo de columnas o filas que abarca el elemento se puede utilizar la palabra `span` seguida del número de filas o columnas.
