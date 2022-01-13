# Posicionamiento de los elementos hijo

En el caso de los elementos hijo se puede posicionar los mismos utilizando propiedades específicas. Estas propiedades se pueden dividir en tres grupos:

- Start
- End
- Both

Estas propiedades ayudan a posicionar los elementos de acuerdo a las líneas de la grilla. Se dividen en propiedades para filas y para columnas:

## Propiedades para columnas

En el caso de las columnas que abarca un elemento hay 3 propiedades:

- `grid-column-start`.- Indica el número de línea (columna) en el que inicia el elemento.
- `grid-column-end`.- Indica el número de línea (columna) en el que termina el elemento.
- `grid-column`.- Indica los número de inicio y final de las líneas (columna) que abarca un elemento.

### **Opción 1**

~~~css
.parent {
  display: grid;
  ...
}

.child {
  grid-column-start: *N°line*;
  grid-column-end: *N°line*;
}
~~~

### **Opción 2**

~~~css
.parent {
  display: grid;
  ...
}

.child {
  grid-column: *N°line start* / *N°line end*;
}
~~~

## Propiedades para filas

En el caso de las filas que abarca un elemento hay 3 propiedades:

- `grid-row-start`.- Indica el número de línea (fila) en el que inicia el elemento.
- `grid-row-end`.- Indica el número de línea (fila) en el que termina el elemento.
- `grid-row`.- Indica los número de inicio y final de las líneas (fila) que abarca un elemento.

### **Opción 1**

~~~css
.parent {
  display: grid;
  ...
}

.child {
  grid-row-start: *N°line*;
  grid-row-end: *N°line*;
}
~~~

### **Opción 2**

~~~css
.parent {
  display: grid;
  ...
}

.child {
  grid-row: *N°line start* / *N°line end*;
}
~~~

## Posicionamiento con áreas

En el caso de posicionamiento con áreas se maneja de forma distinta. Previamente en el contenedor se deben nombrar las celdas (como se explicó en la lección [Filas, columnas y áreas](../4_ParentElement/2_RowsColumnsGap.md)). Posteriormente al elemento que se quiere posicionar se le coloca el nombre de las celdas que ocupará con la propiedad `grid-area`:

~~~css
.parent {
  display: grid;
  grid-template: ... /...;
  grid-template-areas:
    "el-name11 elname12 ... elname1N"
    "el-name21 elname22 ... elname2N"
    ...
    "el-nameM1 elnameM2 ... elnameMN";
}

.child {
  grid-area: *el-nameIJ*;
}
~~~
