# Combinadores

Los combinadores son parámetros que permiten combinar múltiples selectores y crear una mayor especificidad. Entro estos combinadores están:

- Hermano cercano (adjacent sibling)
- Hermano general (general sibling)
- Hijo (child)
- Descendiente (descendant)

## Adjacent sibling

Un hermano cercano de un elemento es aquel que se ubica en el mismo nivel del elemento (tienen el mismo padre) y se encuentra al lado de este. Para especificar hermanos cercanos en CSS se utiliza el símbolo de suma (+).

***HTML***

~~~html
<parent>
  <sibling1></sibling1>
  <sibling2></sibling2>
  <tag1></tag1>
  <tag2></tag2>
  ...
  <sibling1></sibling1>
</parent>
~~~

***CSS***

~~~css
sibling1 + sibling2 {
  ...
}
~~~

Al hacer esto los estilos se aplican solamente al primer `<sibling1>` debido a que está al lado del elemento `<sibling2>`.

## General Sibling

Un hermano general de un elemento es aquel que solamente se ubica en el mismo nivel del elemento (tienen el mismo padre). Para especificar hermanos generales se utiliza el símbolo virguilla (\~).

***HTML***

~~~html
<parent>
  <sibling1></sibling1>
  <sibling2></sibling2>
  <tag1></tag1>
  <tag2></tag2>
  ...
  <sibling1></sibling1>
</parent>
~~~

***CSS***

~~~css
sibling1 ~ sibling2 {
  ...
}
~~~

Al hacer esto los estilos se aplican solamente a todos los `<sibling1>` debido a que están en el mismo nivel que el elemento `<sibling2>` (tienen el mismo padre).

## Child

Un elemento hijo es aquel que es descendiente directo de un elemento. Es decir, se encuentra un nivel por debajo de este. Para especificar un elemento hijo se utiliza el símbolo mayor que (>).

***HTML***

~~~html
<parent>
  <firstchild>
    <secondchild>
      <firstchild></firstchild>
    </secondchild>
  </firstchild>
  <secondchild></secondchild>
</parent>
~~~

***CSS***

~~~css
parent > firstchild {
  ...
}
~~~

Al hacer esto los estilos se aplican solamente al primer `<firstchild>` debido a que es el único `<firsthchild>` descendiente directo del elemento `<parent>`.

## Descendant

Un elemento descendiente es aquel que está dentro de un elemento mayor. Para definir un elemento descendiente simplemente se separa el elemento padre del elemento descendiente por medio de un espacio ' '.

***HTML***

~~~html
<parent>
  <firstchild>
    <secondchild></secondchild>
  </firstchild>
  <secondchild>
  <secondchild>
</parent>
~~~

***CSS***

~~~css
parent secondchild {
  ...
}
~~~

Al hacer esto los estilos se aplican a todos los `<secondchild>` debido a que se ubican dentro del elemento `<parent>`, es decir, son descendientes del mismo. En este caso se considera al padre mayor si hay más de un elemento que encierra al elemento hijo. Para practicar selectores y combinadores se puede acceder a un juego en el siguiente [enlace](https://flukeout.github.io/). Si se quiere ver más combinadores se puede acceder al siguiente [enlace](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Combinators).
