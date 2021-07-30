# Posicionamiento

El posicionamiento es una de las cosas más importantes en CSS debido a que establece como estarán ubicados los elementos en pantalla. El posicionamiento de un elemento en CSS se modifica con la propiedad `position` y uno de los posibles valores:

~~~css
element {
  position: *value*;
}
~~~

## Posibles valores

| Valor | Descripción |
| ----- | ----------- |
| `static` | Los elementos son estáticos por defecto. siguen el flujo normal e la página y no se ven afectados por las propiedades `top`, `bottom`, `left` y `right` |
| `initial` | Ubica el elemento en su posición predeterminada |
| `inherital` | El elemento hereda el valor de la posición de su elemento padre |
| `relative` | Con esta posición el elemento se coloca en relación a su posición inicial |
| `absolute` | Con esta posición el elemento se coloca en relación al elemento relativo más cercano (por defecto al body) |
| `fixed` | El elemento se ubica en relación a la ventana del navegador y se mantiene fijo al hacer scroll |
| `sticky` | El elemento se posiciona en función del deslazamiento del usuario para después mantenerse fijo en una posición específica.
