# Alineamiento de los elementos hijo

Para alinear, centrar o posicionar un elemento dentro de las celdas se pueden utilizar tres propiedades de los elementos hijo. Estas propiedades son:

- `justify-self`
- `align-self`
- `place-self`

## Propiedad `justify-self`

Esta propiedad permite alinear el elemento de forma inline (por defecto horizontal). Los valores que acepta son:

- `start`.- Posiciona el elemento al inicio de la línea.
- `center`.- Centra el elemento.
- `end`.- Posiciona el elemento al final de la línea.
- `stretch`.- Alarga el elemento para ocupar todo el espacio disponible en línea.

~~~css
.parent {
  display: grid;
  ...
}

.child {
  justify-self: *value*;
}
~~~

## Propiedad `align-self`

Esta propiedad permite alinear el elemento de forma block (por defecto vertical). Los valores que acepta son:

- `start`.- Posiciona el elemento al inicio de la columna.
- `center`.- Centra el elemento.
- `end`.- Posiciona el elemento al final de la columna.
- `stretch`.- Alarga el elemento para ocupar todo el espacio disponible en bloque.

~~~css
.parent {
  display: grid;
  ...
}

.child {
  align-self: *value*;
}
~~~

## Propiedad `place-self`

Esta propiedad permite alinear el elemento de ambas formas, *justify* y *align*. Los valores que acepta son:

- `start`.- Posiciona el elemento al inicio de la línea (fila o columna).
- `center`.- Centra el elemento respecto a la fila o columna.
- `end`.- Posiciona el elemento al final de la línea (fila o columna)
- `stretch`.- Alarga el elemento para ocupar todo el espacio disponible en línea o bloque.

~~~css
.parent {
  display: grid;
  ...
}

.child {
  place-self: *align-value* / *justify-value*;
}
~~~
