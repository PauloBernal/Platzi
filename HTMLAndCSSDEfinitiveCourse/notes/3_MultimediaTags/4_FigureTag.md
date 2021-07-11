## Etiqueta figure

`<figure>` es una etiqueta contenedora de imágenes. Esto se utiliza mayormente por cuestión de buenas prácticas y un uso correcto de la semántica de HTML debido a que de antemano el navegador sabe que debe desplegar una imagen.
~~~
<figure>
    <img src="/route/" alt="alternative_text" />
</figure>
~~~

## Descripción de imágenes

Se añadió una nueva etiqueta llamada `<figcaption>`, la cuál va dentro de `<figure>` y permite agregar una breve descripción de la imagen en cuestión

~~~
<figure>
    <img src="/route/" alt="alternative_text" />
    <figcaption>IMG_description</figcaption>
</figure>
~~~