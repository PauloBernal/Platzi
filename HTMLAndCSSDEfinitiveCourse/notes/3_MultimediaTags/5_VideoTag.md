# Etiqueta video

Al igual que imágenes, existe la posibilidad de insertar video en HTML. Esto se hace con la etiqueta de HTML 5 `<video>`. Esta etiqueta utiliza diversos atributos para mostrar el contenido:
- `src`.- Al igual que con imágenes, este atributo debe especificar la ruta del video.
- `controls`.- Este atributo no necesita de un valor. Lo que hace es mostrar controles de reproducción para que el usuario pueda manipular el video. 
- `preload`.- Ayuda a que el video empiece a renderizarse desde que la página se carga si se utiliza el valor `auto`.

~~~
<video src="/route/" controls preload="auto" ></video>
~~~

Si se quiere determinar un rango en el tiempo del video (un estado inicial y uno final) se puede modificar el valor de `src`. Para esto se coloca un hash '#' después de la ruta, una 't' que indica que se trata de tiempo y a la que se le asigna un segundo en el que iniciará el video y uno en el que terminará.

***Ejemplo***
~~~
<video src="/route/#t=3,5" controls preload="auto" ></video>
~~~
Este video empieza en el segundo 3 y acaba en el segundo 5 (solo la primera vez que este se reproduce)

## Etiqueta `<source>`

Esta etiqueta sirve para especificar distintas fuentes del video en caso de que el navegador no soporte ciertos formatos. Se puede colocar cuantas fuentes de video se quiera dependiendo de la variedad de formatos.
~~~
<video controls preload="auto">
    <source src="/route1/" />
    <source src="/route2/" />
    ...
    <source src="/routeN/" />
</video>
~~~
