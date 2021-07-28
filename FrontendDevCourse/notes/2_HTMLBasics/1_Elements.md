# Anatomía de un elemento HTML

## Anatomía

Un elemento HTML se conforma por:

- Etiqueta de apertura
- Contenido
- Etiqueta de cierre

~~~html
<tag> Content </tag>
~~~

***Ejemplo 1*** Anatomía de la etiqueta h1

~~~html
<h1> Title </h1>
~~~

- Etiqueta de apertura: `<h1>`
- Contenido: `Title`
- Etiqueta de cierre: `</h1>`

Hay elementos especiales que solamente poseen etiqueta de apertura, no de cierre.

## Atributos

Los atributos son propiedades del elemento que van en la etiqueta de apertura y que se conforman por un nombre de atributo y un valor (en algunos casos no hay valor). La forma de representar un atributo es colocar el nombre del atributo, después un signo de igualdad y el valor entre comillas.

~~~html
<tag property_name="property_value"> Content </tag>
~~~

***Ejemplo 2*** Como atributos la clase `title` y el id `first` en la etiqueta del ejemplo 1:

~~~html
<h1 class="title" id="first"> Title </h1>
~~~

## Anidamiento

El anidamiento se refiere a elementos que van dentro de otros elementos. En HTML el anidamiento es muy común con elementos contenedores o elementos padre y elementos de contenido o elementos hijo. Los elementos hijo van dentro de los elementos padre como si fueran parte de su contenido:

~~~html
<parent>
  <child></child>
</parent>
~~~

***Ejemplo 3*** Utilizando anidamiento crear una lista desordenada de HTML con 3 elementos:

~~~html
<ul>
  <li> Element 1</li>
  <li> Element 2</li>
  <li> Element 3</li>
</ul>
~~~

## Elementos vacíos

Los elementos vacíos o autoconclusivos son aquellos que no poseen ni contenido ni etiqueta de cierre, solamente una etiqueta de apertura con atributos que definen el elemento (por ejemplo las imágenes o inputs):

~~~html
<tag property_name="property_value" ... />
~~~

***Ejemplo 4*** Utilizar una imagen que está en la ruta `'./img/img.png'` con un texto alternativo 'image'

~~~html
<img src="./img/img.png" alt="image" />
~~~
