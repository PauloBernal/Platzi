# Anidamientos e imports

## Imports

En Less es posible modularizar los estilos en distintos archivos de extensión `*.less`. Para llamar a estos componentes se utiliza la funcionalidad `@import` seguida de la ruta del archivo entre comillas y un punto y coma para especificar el salto de línea. Esto ayuda al momento de separar los estilos en múltiples archivos en función de los componentes creados en el archivo `.html`.

~~~less
@import "/route/";
~~~

## Anidación de elementos

La anidación en Less es distinta a la de CSS. En CSS para indicar elementos anidados se coloca el nombre del elemento padre y después el nombre del elemento hijo, en Less se coloca el elemento hijo dentro de las llaves del elemento padre:

***Less***

~~~less
parent {
    *parent styles*
    child {
        *child styles*
    }
}
~~~

***CSS***

~~~css
parent {
    *parent styles*
}

parent child {
    *child styles*
}
~~~

## BEM

En Less se puede utilizar la notación de clases en tema de bloques, elementos y modificadores de BEM, simplemente se debe colocar un ampersand (`&`) que hace alusión al elemento padre y el nombre del elemento o modificador con la respectiva notación de BEM:

***Less***

~~~less
.block {
    *parent styles*
    &__element {
        *child styles*
    }
}
~~~

***CSS***

~~~css
.block {
    *parent styles*
}

.block__element {
    *child styles*
}
~~~
