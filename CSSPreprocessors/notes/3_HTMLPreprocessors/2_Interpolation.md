# Interpolación

## `<div>`

Al trabajar en Pug se puede generar un `div` con una clase sin necesidad de especificar que se trata de un `div`. Para esto solamente basta colocar el nombre de la clase con un punto por delante y por defecto Pug lo entenderá como un `div`:

***Pug***

~~~pug
.classname
~~~

***HTML***

~~~html
<div class="classname"></div>
~~~

## Hijo único

Cuando un elemento padre solamente tiene un elemento hijo se puede escribir de la siguiente forma:

***Pug***

~~~pug
parent: child
~~~

***HTML***

~~~html
<parent>
    <child></child>
</parent>
~~~

## Salto de líneas

Cuando el contenido de una etiqueta es muy amplio y se requiere de mayor espacio de visualización se puede colocar el nombre de la etiqueta seguida de un punto y un salto de línea, todo lo que siga Pug entenderá como parte del contenido de la etiqueta:

***Pug***

~~~pug
tag.
    Content
    Content
    ...
    Content
~~~

***HTML***

~~~html
<tag>
    Content
    Content
    ...
    Content
</tag>
~~~

Sin embargo esto no es bueno al momento de utilizar una etiqueta como contenedor debido a que confundirá el contenido con los elementos hijo. Par esto existe otra solución que consiste en utilizar una pleca (`|`) y un espacio antes del contenido:

***Pug***

~~~pug
parent
    | Content
    | Content
    child
    | Content
~~~

***HTML***

~~~html
<parent>
    Content
    Content
    <child></child>
    Content
</parent>
~~~
