# Metodologías CSS

## OOCSS (Object Oriented CSS)

Esta metodología consiste en CSS orientado a objetos, es decir, se separa el diseño del contenido. En este caso se colocan clases a los elementos dependiendo si algunos estilos se repiten:

**Ejemplo** Se quiere que el footer y el header de la página tengan las mismas dimensiones, pero el header debe ser de color azul y el footer de color verde:

***HTML***

~~~html
<header class="header dimension"></header>
<footer class="footer dimension"></footer>
~~~

***CSS***

~~~css
.dimension {
  width: 100%;
  height: 80px;
}

.header {
  background-color: blue;
}

.footer {
  background-color: green;
}
~~~

## BEM (Blocks Elements Modifiers)

Es una metodología de clases basadas en bloques, elementos y modificadores. El bloque es un contenedor o un componente en sí, el cuál se representa solo con el nombre del mismo. El elemento es un subcomponente del bloque y se representa con el nombre del bloque, dos guiones bajos y el nombre del elemento. Por último los modificadores son variantes de un bloque o un elemento y se representan con el nombre del bloque o elemento seguido de dos guiones y el nombre del modificador:

### Bloque

***HTML***

~~~html
<tag class="block"></tag>
~~~

***CSS***

~~~css
.block {
  ...
}
~~~

### Elemento

***HTML***

~~~html
<parent class="block">
  <child class="block__element"></child>
</parent>
~~~

***CSS***

~~~css
.block {
  ...
}

.block__element {
  ...
}
~~~

### Modificador

***HTML***

~~~html
<parent class="block">
  <child class="block__element"></child>
  <child class="block__element--modifier"></child>
</parent>
<parent class="block--modifier">
  <child class="block--modifier__element"></child>
</parent>
~~~

***CSS***

~~~css
.block {
  ...
}

.block--modifier {
  ...
}

.block__element {
  ...
}

.block__element--modifier {
  ...
}
~~~

## SMACSS (Scalable and Modular Architecture for CSS)

Esta metodología se basa en 5 pasos:

1. Dividir el CSS en componentes base
2. Estructurar el Layout
3. Identificar los módulos (componentes reutilizables)
4. Definir los estados de los elementos
5. Estructurar los diversos temas como Dark Theme (Opcional)

## ITCSS (Inverted Triangle CSS)

Esta metodología se basa en dividir los archivos de CSS en distintas partes para que no se combinen entre sí. La división se daría por:

- Ajustes
- Herramientas
- Genérico
- Elementos
- Objetos
- Componentes
- Utilidades

Así se evita bastante el tema de la especificidad.

## Atomic Design

Este sistema de modularización está basado en estructura química básica teniendo la división de elementos en:

- Átomos.- Los elementos más pequeños y escenciales de la página
- Moléculas.- Un conjunto de átomos
- Organismos.- Conjunto de moléculas
- Templates.- Conjuntos de organismos
- Páginas.- Conjuntos de templates
