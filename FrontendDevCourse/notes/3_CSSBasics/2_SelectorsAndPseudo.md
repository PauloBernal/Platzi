# Tipos de selectores, pseudo clases y pseudo elementos

## Tipos de selectores

- Universal (`*`).- El selector universal es aquel que hace referencia a toos los elementos. Generalmente se utiliza para resetear estilos que vienen por defecto en el navegador:

~~~css
* {
  property: value;
  ...
}
~~~

- Tipo o etiqueta.- Es un selector que hace referencia a todas las etiquetas con ese nombre y se representan simplemente colocando el nombre de la etiqueta. No son recomendables al tratarse de proyectos grandes a menos que se trate con etiquetas únicas como `<html>` o `<body>`:

***HTML***

~~~html
<tag></tag>
~~~

***CSS***

~~~css
tag {
  property: value;
}
~~~

- Clase.- El selector de clase es aquel que hace referencia a un grupo de elementos que llevan el mismo nombre de clase (se define en atributos). Se representa con un punto al inicio del nombre de clase y el selector más utilizado debido a su versatilidad.

***HTML***

~~~html
<tag class="classname"></tag>
~~~

***CSS***

~~~css
.classname {
  property: value;
}
~~~

- ID.- El selector de ID hace referencia a un solo elemento con el mismo id que al igual que las clases se define en atributos. Para utilizar este selector se coloca un hash (`#`) por delante del ID. Tampoco es recomendable trabajar con ID por temas de especificidad:

***HTML***

~~~html
<tag id="element_id"></tag>
~~~

***CSS***

~~~css
#element_id {
  property: value;
}
~~~

## Pseudo clases

Las pseudo clases son como estados o partes en específico de un elemento (como el primer hijo, el último hijo, etc) que se utilizan como selectores representados con dos puntos (`:`):

~~~css
element:pseudo-class {
  property: value;
}
~~~

Algunas de las pseudo-clases más comunes son:

- `first-child`.- Aplica los estilos al primer hijo del elemento
- `last-child`.- Aplica los estilos al último hijo del elemento
- `nth-child(n+a)`.- Aplica los estilos por intervalos a los hijos del elemento (por medio de una ecuación del n-ésimo elemento) haciendo alusión a los números ordinales.
- `hover`.- Aplica los estilos al elemento cuando el mouse está encima de él
- `active`.- Aplica los estilos al elemento cuando se hace click sobre él
- `focus`.- Aplica los estilos al elemento cuando este tiene el foco

Para ver documentación completa acerca de las pseudo-clases se puede acceder al siguiente [enlace](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes).

## Pseudo elementos

Los pseudo elementos hacen alusión a una parte específica de un elemento. Estos se representan con un par de dos puntos (`::`) y el nombre del pseudo-elemento:

~~~css
element::pseudo-element {
  property: value;
}
~~~

Algunos de los pseudo-elementos más usados son:

- `before`.- Hace referencia a la parte anterior del elemento
- `after`.- Hace referencia a la parte posterios del elemento
- `first-letter`.- Hace referencia a la primera letra del elemento
- `selection`.- Hace referencia a la selección de texto

Para ver documentación completa acerca de los pseudo-elementos se puede acceder al siguiente [enlace](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements).
