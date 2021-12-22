# Creando el contenedor

Al momento de utilizar grid, es importante distinguir entre dos valores: `display: grid` y `display: inline-grid`. La propiedad `display` hace referencia a cómo se comporta el elemento dentro de la página (la visualización), es decir, como bloque, en línea, flexbox, grid, etc. Los valores de display se dividen en **inner** y **outer**.

## Inner y outer

- **Valores inner**.- Son aquellos que modifican los hijos directos del contenedor.
- **Valores outer**.- Modifican el display del mismo contenedor.

Los valores principales que se manejan en display y modifican la disposición de los elementos son:

- Inline.- Los elementos se colocan uno al lado de otro, en línea.
- Block.- Los elementos se colocan uno debajo del otro, en bloque.

En el caso de grid existen los dos valores mencionados anteriormente:

- `grid`.- El elemento se comporta como bloque de forma outer y como grid de forma inner (los elementos hijo se disponen en la grilla).
- `inline-grid`.- el elemento se comporta como inline de forma outer y como grid de forma inner.

~~~css
.parent1 {
  display: grid;
}

.parent2 {
  display: inline-grid;
}
~~~
