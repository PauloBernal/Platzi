# BEM

## ¿Qué es BEM?

BEM significa 'Blocks, Elements and Modifiers' (bloques, elementos y modificadores). Es una metodología de estructuración de código y la más utilizada actualmente. Fue creada por Yandex para proyectos web grandes y pequeños y se basa en dividir lógicamente las piezas de las que se compone una web.

## Bloques, elementos y modificadores

- Bloques.- Son módulos individuales e independientes en la página (no dependen de otros bloques).
- Elementos.- Son componentes dependientes de un bloque (los elementos conforman un bloque).
- Modificador.- Son elementos que dependen del bloque a los cuales se les hace una modificación

## Sintaxis

Los bloques se definen simplemente como clases en CSS:

~~~css
.block {
    ...
}
~~~

Los elementos que están dentro de un bloque se definen con el nombre de la clase del bloque seguido de dos guiones bajos y posteriormente viene el nombre del elemento:

~~~css
.block__element {
    ...
}
~~~

Los modificadores se definen parecido a los elementos con la diferencia de que en vez de dos guiones bajos se utiliza dos guiones normales y después el nombre del modificador:

~~~css
.block--modifier {
    ...
}
~~~

## Ventajas

- Menos repeticiones
- Independencia absoluta
- Mejoría en la herencia múltiple
