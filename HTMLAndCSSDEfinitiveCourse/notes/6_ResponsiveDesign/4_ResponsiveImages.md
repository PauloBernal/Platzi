# Imágenes responsive

Anteriormente se utilizaban `<div>` con una sola imagen al momento de desarrollar, lo cuál se considera una mala práctica. Esto debido a que en dispositivos pequeños se descargaban imágenes grandes y se ampliaban los tiempos de carga de forma innecesaria. Para solucionar esto existe una nueva etiqueta llamada `<picture>`. Al igual que con `<video>`, `<picture>` permite añadir distintas rutas con `<source>`, en este caso dependiendo del tamaño de la pantalla.

~~~html
<picture>
    <source media="*size*" srcset="/route1/">
    <source media="*size*" srcset="/route2/">
    ...
    <source media="*size*" srcset="/routeN/">
    <img src="/route/" alt="text" />
</picture>
~~~

En 'size' va el tamaño mínimo o máximo del dispositivo por ejemplo `(min-width: 600px)`. Es importante la etiqueta `<img/>` debido a que esta renderiza la imagen y `<source>` lo que hace es pasarle una nueva ruta de imagen. Se debe 
colocar las rutas en orden descendente (de la que es para el dispositivo más grande hasta la que es para el dispositivo más pequeño con `<img/>`)