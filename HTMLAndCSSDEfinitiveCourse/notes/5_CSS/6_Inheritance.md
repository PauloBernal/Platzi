# Herencia

Es el código CSS que se pasa de un elemento padre a un elemento hijo. Esto quiere decir que los estilos que se le apliquen al elemento padre también se aplican al elemento hijo. Por defecto las etiquetas de texto heredan sus estilos de la etiqueta `<html>`. Los encabezados heredan el tipo de letra, sin embargo no el tamaño de la misma. Los estilos aplicados por defecto son `16px` en `font-size` y `'Times New Roman'` en `font-family`.

## Heredando estilos

Para que un elemento hijo herede un estilo del elemento padre más cercano se utiliza el valor `inherit` en la propiedad:

~~~css
element {
  property: inherit;
}
~~~

***Ejemplo*** Hacer que un `ul` dentro de un `nav` herede el margen y el padding del mismo

### HTML

~~~html
<nav>
  <ul></ul>
</nav>
~~~

### CSS

~~~css
nav {
  margin: 0;
  padding: 5%;
}

ul {
  margin: inherit;
  padding: inherit;
}
~~~
