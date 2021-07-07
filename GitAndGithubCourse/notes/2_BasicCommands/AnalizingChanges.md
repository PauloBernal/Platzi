# Analizando cambios en el proyecto de Git

## Visualizando cambios

Una forma de visualizar los cambios en un proyecto de git es haciendo uso del comando `show`, el cuál muestra los cambios que fueron realizados en un archivo.
~~~
$ git show filename.ext
~~~
Esto muestra un 'diff', lo cuál es una comparación del estado del archivo en el anterior commit con el estado del último commit. Lo que fue añadido se representa con un `+` (más) y lo que fue removido del archivo es representado con un `-` (menos).
~~~
-Esta es la representación de contenido removido
+Esta es la representación de contenido añadido
~~~


## Comparando versiones

Para visualizar y comparar las diferencias entre dos versiones de un mismo proyecto existe un comando llamado `diff`. Para esto se debe colocar los ID de los respectivos commit a comparar, los cuáles se pueden saber utilizando el comando `log` explicado en la anterior página.
~~~
$ git diff ID_ver1 ID_ver2
~~~
Si se coloca simplemente `diff` sin especificar versiones entonces Git compara los cambios del repositorio (último commit) con los cambios en staging
~~~
$ git diff
~~~

## Ver cambios rápidamente

Por último también se puede hacer uso del comando `log` para visualizar cambios si se hace uso del parámetro `--stat`:
~~~
$ git log --stat
~~~


## Comandos útiles
- `show`.- Muestra los cambios realizados en un archivo
~~~
$ git show filename.ext
~~~
- `diff`.- Este comando permite comparar los cambios en dos versiones distintas por medio de los ID de sus commits.
~~~
$ git diff ID_ver1 ID_ver2
~~~
También si no se especifica las versiones compara los cambios en el repositorio con los cambios en staging