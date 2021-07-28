# Modelo de caja

Todos los elementos de caja poseen un modelo de caja. Este se compone de cuatro partes:

- `margin`.- Es el espacio externo desde el borde del elemento hacia otros elementos
- `border`.- Es el borde del elemento y puede ser visible o invisible
- `padding`.- Es el espacio interno desde el borde del elemento hasta el contenido
- Contenido.- Es aquello que va dentro del elemento

## Propiedades

Las principales propiedades para modificar el modelo de caja de un elemento son:

- `width`.- Permite ajustar el ancho del contenido de un elemento.
- `height`.- Permite ajustar la altura del contenido de un elemento.
- `padding`.- Permite aumentar o reducir el espacio interno de un elemento.
- `border`.- Permite modificar el borde de un elemento.
- `margin`.- Permite modificar y controlar el espacio externo desde el borde del elemento a otros elementos.

Todas estas propiedades tienen valores con unidades de medida de longitud (absolutas o relativas) y las tres últimas se pueden modificar de forma lateral, es decir, se puede modificar el lateral superior (`top`), inferior (`bottom`), de la izquierda (`left`) o derecha (`right`).

## Border

Esta propiedad se diferencia de las demás debido a que se necesita tres parámetros en vez de uno los cuales son el tamaño del borde, el tipo de borde y el color del borde:

~~~css
element {
  border: *size* *type* *color*;
}
~~~

***Ejemplo 1*** Añadir a todos los `<div>` un borde de 3 pixeles, sólido y de color rojo:

~~~css
div {
  border: 3px solid red;
}
~~~

## Box sizing

En muchos casos es molesto que al modificar una propiedad del modelo de caja se desconfigure todo. Para esto existe la propiedad `box-sizing` que recalcula el ancho y el alto de un elemento sin que se vea afectado por el relleno o el borde si se utiliza el valor `border-box`:

~~~css
element {
  box-sizing: border-box;
}
~~~

***Ejemplo 2*** Crear un header que abarque el 100% de ancho, con un relleno de 30px y un borde de 5px, sólido de color verde sin afectar el modelo de caja (ancho constante):

~~~css
header {
  box-sizing: border-box;
  width: 100%;
  padding: 30px;
  border: 5px solid green;
}
~~~

## Buenas prácticas

Por defecto el navegador coloca estilos a los elementos. Es una buea práctica resetear estos estilos haciendo uso del selector universal:

~~~css
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
~~~
