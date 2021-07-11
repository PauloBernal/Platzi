# Index y su estructura básica: body

## Body

### Tipos de etiquetas

En el body de un documento HTML existen dos tipos de etiquetas:
- Etiquetas contenedoras.- Son etiquetas dentro de la que se coloca más etiquetas (de ahí el término 'contenedoras')
- Etiquetas de contenido.- Son aquellas que llevan texto, imágenes, video, etc.

## Etiquetas contenedoras

### Principales

- `header`.- Dentro de esta etiqueta se ubica la cabecera de la página. Esta forma parte de la estructura básica de una página.
~~~
<header></header>
~~~

- `main`.- Es la etiqueta que contiene el contenido principal de la página. Esta también forma parte de la estructura básica de una página.
~~~
<main></main>
~~~

- `footer`.- Es la etiqueta en la que se coloca el contenido secundario. Generalmente va al pie de la página pero en sitios con scroll infinito como Facebook puede ir al costado de la misma. Esta igualmente forma parte de la estructura básica de una página.
~~~
<footer></footer>
~~~

La estructura del body quedaría de la siguiente forma:
~~~
<body>
    <header></header>
    <main></main>
    <footer></footer>
</body>
~~~

Se denomina 'semántica' de HTML al correcto uso de las etiquetas dependiendo del contenido (si se hará una cabecera se utilizará `<header>`, si se trata de contenido principal se utilizará `<main>`, etc)

### Secundarias

- `nav`.- Se usa como base para crear una barra de navegación. Por lo general va dentro del header.
~~~
<header>
    <nav></nav>
</header>
~~~

- `section`.- Son secciones que van dentro de `main` y que pueden usarse para tener de forma más ordenada la estrucura del contenido principal.
~~~
<main>
    <section></section>
</main>
~~~

- `article`.- DEntro de estas se puede colocar artículos, o sea contenido de texto, imágenes, etc. Generalmente van dentro de una sección.
~~~
<main>
    <section>
        <article></article>
    </section>
</main>
~~~

### Listas

En HTML existen dos tipos de listas: ordenadas y no ordenadas

#### Ordenadas

Las listas ordenadas son aquellas que tienen el contenido ennumerado, ya sea de forma ordinal con números o con incisos. Para crear listas ordenadas se utiliza la etiqueta `<ol>` (ordered list):
~~~
<ol></ol>
~~~
Para ennumerar los elementos que aparecen dentro de la lista se utiliza la etiqueta `<li>` (list item), la cuál indica que el contenido dentro de esta se trata de un elemento de la lista. Se puede colocar cuantos elementos se desee dentro de una lista:
~~~
<ol>
    <li></li>
    <li></li>
    <li></li>
    ...
    <li></li>
</ol>
~~~

#### No ordenadas

Las listas no ordenadas son aquellas que no poseen una numeración específica para los elementos dentro de ellas (se da de forma arbitraria). Para crear una lista no ordenada se utiliza la etiqueta `<ul>` (unordered list):
~~~
<ul></ul>
~~~
Para especificar los elementos que aparecen dentro de la lista se utiliza la etiqueta `<li>` (list item), al igual que con las listas ordenadas. Igualmente se puede colocar cuantos elementos se desee dentro de la lista:
~~~
<ul>
    <li></li>
    <li></li>
    <li></li>
    ...
    <li></li>
</ul>
~~~
Se denomina anidar listas a colocar una lista dentro de otra:
~~~
<ul>
    <li>
        <ol>
        </ol>
    </li>
<ul>
~~~


### Contenedores y comodines

- `div`.- Esta etiqueta se utiliza comúnmente como un comodín, es decir que sirve como un contenedor para cualquier otra etiqueta.
~~~
<div></div>
~~~
- `figure`.- Esta etiqueta sirve como un contenedor de multimedia (videos, imágenes, gifs). Antes de su aparición se utilizaban `<div>` para cumplir esta misma función.
~~~
<figure></figure>
~~~
- `span`.- Este es un contenedor genérico en línea y se utiliza mayormente para manejar texto en HTML.
~~~
<span></span>
~~~


## Etiquetas de contenido

### Etiquetas de texto

- `p` (paragraph).- Esta etiqueta es común para colocar texto genérico dentro de ella.
~~~
<p>Text</p>
~~~
- `hn`.- Estas etiquetas se utilizan para crear títulos o subtítulos de encabezado. El 'n' de la etiqueta va desde 1 hasta 6.
~~~
<h1>Title 1</h1>
<h2>Subtitle 2</h2>
<h3>Subtitle 3</h3>
<h4>Subtitle 4</h4>
<h5>Subtitle 5</h5>
<h6>Subtitle 6</h6>
~~~

- `li`.- Dentro de los elementos de las listas se puede colocar texto, ya sea una lista ordenada o no ordenada
~~~
<li>Text</li>
~~~

- `a` (anchor).- La etiqueta de ancla sirve para crear hipervínculos con el atributo `href` especificando la dirección a la que hace referencia el hipervínculo.
~~~
<a href="/route/" >Link text</a>
~~~
Para evitar que el hipervínculo actualice una página completa se puede utilizar el valor de '#' en `href`
~~~
<a href="#" >Link text</a>
~~~
