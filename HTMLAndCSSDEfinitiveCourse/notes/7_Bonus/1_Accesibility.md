# Accesibilidad

## Semántica

El tema de accesibilidad es bastante amplio ya que se debe cubrir diversos tipos de discapacidades que puede llegar a tener una persona. Entre los temas de accesibilidad se encuentra semántica, que se refiere a hacer un uso correcto de las etiquetas que provee HTML 5 para estructurar el proyecto (header, main, footer, etc) evitando usar `<div>` como contenedor en todo. Esto es importante debido a que si un sitio tiene buena semántica este puede ayudar a una persona con discapacidad visual a navegar con ayuda de un programa que identifique estas partes específicas en el documento.

## Textos

Esto muy aparte del tema de legibilidad en las fuentes hace referencia al uso de medidas relativas (como `rem`) al desarrollar el sitio. Si alguien tiene problemas en la vista y quiere ampliar el texto el utilizar medidas relativas en el texto lo hace posible, algo que no se puede con medidas absolutas como pixeles.

## Labels, alt y title

En accesibilidad, a pesar de que muchos desarrolladores no suelen utilizarlas, las etiquetas `<label>` son importantes debido a que ayudan al usuario a posicionarse en el input de una forma más rápida.

El atributo `alt` se utiliza con cierto software diseñado para personas con discapacidad visual debido a que al llegar a una imagen este puede leer la descripción de la misma especificada en `alt`.

Por último, el atributo `title` permite agregar a algunos elementos como imágenes una breve descripción cuando el mouse se posiciona sobre el elemento. También funciona en hipervínculos.
