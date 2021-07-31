# Media Queries

Los media queries son formas de utilizar estilos distintos con distintos tamaños de pantalla. Para utilizar media queries en un archivo se coloca la palabra `@media` seguida de `only screen` generalmente y el tamaño mínimo o máximo de la pantalla a la cuál se le aplicará el media querie. Dentro de las llaves se colocan los estilos a aplicar en el media querie:

~~~css
@media only screen and (*size*) {
  ...
}
~~~

Lo recomendable al maquetar sitios responsive es utilizar la metodología Mobile First, empezando con el diseño para dispositivos móviles e ir adaptando a medida que crece la pantalla.
