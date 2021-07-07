# Git Clean: limpiar el proyecto de archivos no deseados

A veces hay archivos que se añaden de forma accidental y que no se registran en el repositorio. A estos archivos se los denomina archivos basura y se los puede listar con:
~~~
$ git clean --dry-run
~~~
Para remover los archivos que se listan se utiliza el comando:
~~~
$ git clean -f
~~~
Hay que tener en cuenta que por defecto no borra directorios ni archivos que están dentr de un `.gitignore`. Para borrar directorios con `clean` se debe usar el parámetro `-d`:
~~~
$ git clean -d
~~~
