# Anatomía de una regla en CSS

Se llama 'regla' de CSS al conjunto del elemento y sus propiedades.
El selector es la parte que hace referencia al elemento de HTML, la declaración es el conjunto del nombre de la propiedad con su valor. Esto se representa de la siguiente forma:

~~~css
selector {
    property_name: property_value;
}
~~~

Es necesario cumplir con la sintaxis ya que si no se cumple una parte de eestalos estilos se puede llegar a romper.

## Ejemplos

Al modificar el color de fondo del `body`:

~~~css
body {
    background-color: #000022;
}
~~~

- Selector.- `body`
- Nombre de la propiedad: `background-color`
- Valor de la propiedad: `#000022`

Al quitar el subrayado a un enlace cuya clase es `link`:

~~~css
.link {
    text-decoration: none;
}
~~~

- Selector.- `.link`
- Nombre de la propiedad: `text-decoration`
- Valor de la propiedad: `none`

Al cambiar el color a un párrafo cuyo id es `par`:

~~~css
#par {
    color: #444456
}
~~~

- Selector.- `#par`
- Nombre de la propiedad: `color`
- Valor de la propiedad: `#444456`
