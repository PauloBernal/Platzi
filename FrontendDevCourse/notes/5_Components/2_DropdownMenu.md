# Desarrollo de componentes

## Menú desplegable

Un menú desplegable es un menú que permanece oculto hasta que ocurre algpun evento que lo lleva a mostrarse. Usualmente este tipo de menus poseen por defecto un `display: none` y con una pseudo-clase como `hover` o `active` se cambia a `display: block`:

~~~css
child {
  display: none
}

parent:event child, child {
  display: block
}
~~~

## Carousel

Para quitar el wrap de los elementos por defecto se coloca en su contenedor padre la propiedad `white-space: nowrap`, es decir, todos seguirán el flujo en fila sin posicionarse uno al lado del otro. También para esto los elementos hijo deben tener `display: inline-block` y el contenedor debe tener un `overflow-x: scroll`:

~~~css
parent {
  white-space: nowrap;
  overflow-x: scroll;
}

child {
  display: inline-block;
}
~~~

## Elementos del carousel

Para los elementos del caroussel se utiliza un efecto de hover, en el que el elemento crece y los otros se desplazan disminuyendo su opacidad. En esta caso se utilizará un ejemplo con medidas preestablecidas. Las propiedades a usarse para crear este efecto son:

- `transform`.- Permite modificar características en tema de escala, posición, inclinación, etc. de un elemento al ocurrir un evento.
- `transition`.- Permite crear transformaciones fluidas en una duración de tiempo establecida.
- `opacity`.- Altera la opacidad del elemento en una escala del 0 al 1.

En el ejemplo el evento para aplicar las transformaciones será `hover`:

***HTML***

~~~html
  <div class="container">
    <div class="item"></div>
    <div class="item"></div>
    ...
    <div class="item"></div>
  </div>
~~~

***CSS***

~~~css
.container {
  white-space: nowrap;
  overflow-x: scroll;
}

.item {
  display: inline-block;
  width: 200px;
  height: 250px;
  overflow: hidden;
  transition: 450ms;
  transform-origin: center left;
}

.item:hover ~ .item
  transform: translate3d(100px, 0, 0);

.container:hover .item
  opacity: 0.3

.container:hover .item:hover
  transform: scale(1.5);
  opacity: 1;
~~~

## Degradado linear

Para generar un efecto de gradiente se utiliza la función `linear-gradient`, la cuál requiere de algunos parámetros en específico:

- Dirección.- Se debe especificar de dónde a dónde va el degradado con la palabra `to` y la dirección hacia la que va el degradado.
- Inclinación.- Para indicar una inclinación en el gradiente se utiliza el ángulo en el sistema sexagesimal seguido de la unidad `deg`
- Color-porcentaje.- Esto indica desde que parte hasta que parte habrá un color. Primero se coloca el color y después seguido de un espacio el porcentaje del gradiente que ocupa ese color (desde donde inicia el color)

***Ejemplo*** Un degradado que vaya de abajo hacia arriba iniciando en negro y terminando en blanco

~~~css
element {
  background: linear-gradient(to top, #000000 0%, #FFFFFF 100%);
}
~~~
