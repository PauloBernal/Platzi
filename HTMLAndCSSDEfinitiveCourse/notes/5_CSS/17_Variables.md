# Variables

Las variables en CSS son una forma de almacenar valores y ahorrar código al momento de realizar los estilos. Por ejemplo para colores, tamaños, fuentes, etc. que se repiten en más de un elemento se puede colocar variables que facilitan el trabajo.

## Declarando variables

Lo correcto al momento de generar variables es declararlas en el elemento root:

~~~css
:root {
    ...
}
~~~

Para declarar una variable en CSS se coloca dos guiones antes del nombre de la variable y el valor se asigna con dos puntos y un punto y coma al final:

~~~css
:root {
    --var-name1: value1;
    --var-name2: value2;
    ...
    --var-nameN: valueN;
}
~~~

## Llamando variables

Para llamar una variable desde otro lugar del código se utiliza la función `var()` con el nombre de la variable dentro:

~~~css
element {
    property1: var(--var-name1);
    property2: var(--var-name2);
    ...
    propertyN: var(--var-nameN);
}
~~~
