# Anatomía de una etiqueta de HTML

## Etiquetas cerradas

Una etiqueta cerrada posee distintas secciones:

- Etiqueta de apertura.- Es la parte desde la que se abre el elemento
- Etiqueta de cierre.- Es la parte que indica un cierre del elemento
- Contenido.- Es lo que va entre la etiqueta de apertura y la etiqueta de cierre
- Atributo.- Son distintas propiedades o características de la etiqueta
    - Nombre del atributo.- Es el nombre que recibe la propiedad
    - Valor del atributo.- Es el valor que modifica la propiedad o el comportamiento de la etiqueta

***Plantilla***

~~~html
<tag name="value" >Content</tag>
~~~

***Ejemplo*** Identificar las partes de una etiqueta de ancla `<a>`:

~~~html
<a href="mywebsite.com" > link </a>
~~~

- `<a>`: Etiqueta de apertura
- `</a>`: Etiqueta de cierre
- `link`: Contenido
- `href`: Nombre del atributo
- `mywebsite.com`: Valor del atributo

## Etiquetas abiertas

Las etiquetas abiertas poseen partes similares a las etiquetas cerradas:

- Etiqueta.- El elemento se abre y se cierra con una sola etiqueta
- Atributo.- Son distintas propiedades o características de la etiqueta
    - Nombre del atributo.- Es el nombre que recibe la propiedad
    - Valor del atributo.- Es el valor que modifica la propiedad o el comportamiento de la etiqueta

***Plantilla***

~~~html
<tag name="value" />
~~~

***Ejemplo*** Identificar las partes de una etiqueta de imagen `<img>`:

~~~html
<img src="./img.png" />
~~~

- `<img />`: Etiqueta
- `src`: Nombre del atributo
- `./img.png`: Valor del atributo
