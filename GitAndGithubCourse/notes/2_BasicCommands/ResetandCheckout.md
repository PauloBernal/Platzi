# Volver en el tiempo con Reset y Checkout

## Resetear

Esta función se utiliza para regresar a una versión anterior (revirtiendo los cambios) en el tiempo. Esto puede deberse a un error en la versión actual que no había en una versión previa, por lo que a veces se busca preservar algunos cambios de la versión actual. Para hacer esto se utiliza el comando `reset` con dos parámetros `--soft` y `--hard` junto al ID del commit al que se quiere regresar.
~~~
$ git reset --flag ID_ver
~~~

### Reseteo suave

El reseteo suave es aquel en el que se regresa a una versión anterior en todos los archivos del directorio mateniendo todos los cambios en staging de la versión actual. Esto sirve cuando se realizaron avances en el proyecto los cuales no se quieren perder.
~~~
$ git reset --soft ID_ver
~~~

### Reseteo forzado

El reseteo forzado es aquel en el que se regresa a una versión anterior borrando todos los avances en staging y todos los cambios previos (no se puede volver a versiones anteriores a la que se está regresando, por esto hay que tener bastante cuidado al realizar el reseteo forzado).
~~~
$ git reset --hard
~~~


## Viajando entre commits

Para ver una versión anterior de un archivo en específico (sin necesidad de resetear) existe un comando llamado `checkout`. Este permite cambiar el contenido de un archivo actual a como era antes, lo que facilita el flujo al momento de solucionar un problema que surgió en un punto específico del proyecto.
~~~
$ git checkout ID_ver filename.ext
~~~
Sin embargo, es posible volver al estado actual de dicho archivo si se hizo un uso correcto de las ramas y versiones, esto utilizando `checkout master`:
~~~
$ git checkout master filename.ext
~~~
Para cambiar el archivo definitivamente se utiliza el commit normal.
