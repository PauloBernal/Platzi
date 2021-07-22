# Selectores

Mucho de como salga un proyecto en tema de estilos depende de qué tan bien el desarrollador sepa utilizar los selectores de CSS. Como ya se mencionó anteriormente, un selector es aquello que hace referencia a un elemento HTML.

## Tipos de selectores

### Selector universal (`*`)

El selector universal sirve para hacer referencia a absolutamente todos los elementos del documento. Generalmente este selector se utiliza para resetear estilos y borrar los predeterminados en el navegador:

~~~css
* {
    ...
}
~~~

### Selector de etiqueta (`<...>`)

El selector de etiqueta o selector de elementos hace referencia a todas las etiquetas del documento con el mismo nombre del selector. Para hacer referencia a una etiqueta solamente es necesario escribir el nombre de la etiqueta como selector:

***HTML***

~~~html
<tagname></tagname>
~~~

***CSS***

~~~css
tagname {
    ...
}
~~~

### Selector de clase (`.*`)

Las clases son formas de agrupar múltiples elementos para aplicarles estilos. Para definir una clase en html se utiliza el atributo `class` con el nombre de la clase. Para hacer utilizar este selector en CSS se coloca un punto (`.`) por delante del nombre de la clase:

***HTML***

~~~html
<tag class="tag_class"></tag>
~~~

***CSS***

~~~css
.tag_class {
    ...
}
~~~

Este selector es el que más se utilza entre todos (aproximadamente un 90% de las veces)

### Selector de ID

El selector de ID hace referencia solamente a un elemento en específico. El ID del elemento se coloca en el documento HTML y se especifica en los estilos con un hash (`#`) por delante:

***HTML***

~~~html
<tag id="tag_id"></tag>
~~~

***CSS***

~~~css
#tag_id {
    ...
}
~~~

## Operadores y más selectores

### Múltiples selectores

Para múltiples selectores se separa de estos con comas (`,`):

~~~css
sel1, sel2, ..., selN {
    ...
}
~~~

### Selectores anidados

Los selectores anidados son aquellos que hacen referencia a elementos uno detro de otro. Para utilizar selectores anidados se coloca primero el selector del elemento padre y después separado con un espacio el selector del elemento hijo:

***HTML***

~~~html
<parent>
    <child>
        <child2></child2>
    </child>
</parent>
~~~

***CSS***

~~~css
parent child2 {
    ...
}
~~~

### Selector de hijos

A diferencia del selector anidado el selector de hijos hace referencia a los hijos en primer nivel, es decir, a sus hijos directos. Para utilizar este seletor se coloca un signo de mayor que (`>`) entre los selectores del elemento padre y el elemento hijo respectivamente:

~~~html
<parent>
    <child></child>
</parent>
~~~

~~~css
parent>child {
    ...
}
~~~

### Selector adyacente

El selector adyacente se refiere a un elemento que está al lado de otro, es decir son elementos hermanos y uno está después de otro en el documento. Para utilizar el selector adyacente primero se coloca el selector del elemento anterior al que se quiere colocar estilos, después un signo más (`+`) y finalmente el selector del elemento al cual se aplicarán los estilos:

~~~html
<parent>
    <child1></child1>
    <child2></child2>
</parent>
~~~

~~~css
child1+child2{ 
    ...
}
~~~

En este caso los estilos se aplican al elemento `child2`.

### Selector de atributos

Este selector se utiliza a menudo cuando se quiere especificar un elemento con un atributo en específico (como `for`, `value`, `placeholder`, etc). Para esto se utiliza primero el selector del elemento, después se colocan corchetes y dentro de los corchetes el nombre del atributo con su valor entre comillas simples después de un símbolo de igual.

~~~html
<element prop="value"></element>
~~~

~~~css
element[prop='value'] {
    ...
}
~~~

## Prioridad de selectores

El navegador prioriza los selectores dependiendo de su tipo. El orden de prioridad (de más importante a menos importante) es:

1. ID (100)
2. Clase (10)
3. Etiqueta (1)

Los números entre paréntesis son el valor de prioridad de cada selector. Si se utilizan múltiples selectores o selectores más específicos (el nombre y la clase), automáticamente el selector combinado gana mayor prioridad. No es una buena práctica utilizar ID para estilos debido a que rompe el esquema de prioridad (al ser extremadamente específico) y ser más difícil de arreglar.

## Important

Al utilizar `!important` en un estilo se rompe con el esquema de prioridades debido a que una propiedad con este flag sobreescribe todo lo anterior y no permite reescribir esa misma propiedad después (1000000). Al ser una mala práctica se debe tener mucho cuidado al utilizarlo debido a que puede terminar rompiendo todos los estilos. Para utilizar el flag `!important` se coloca este después del valor de la propiedad que se quiere definir como importante y antes del punto y coma:

~~~css
element {
    property: *value* !important;
}
~~~

Esto generalmente se usa cuando se trabaja con código ajeno como una solución rápida.
