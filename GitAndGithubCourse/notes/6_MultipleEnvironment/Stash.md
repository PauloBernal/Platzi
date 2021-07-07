# Git Stash: Guardar cambios en memoria y recuperarlos después

Cuando se quiere almacenar modificaciones de forma temporal sin realizar commit directamente se realiza un `stash`, que es guardar cambios en un espacio de la memoria sin añadirlos al track. Esto es útil al momento de experimentar. Al realizar pequeños cambios con stash no es necesario realizar commits ni crear nuevas ramas para almacenar los cambios.

## Guardando cambios con stash

Para guardar cambios en memoria sin añadirlos a staging se puede usar el comando:
~~~
$ git stash
~~~
Si se quiere listar dichos cambios se puede usar el comando:
~~~
$ git stash list
~~~
Donde hay una salida similar a este ejemplo:
~~~
stash@{0}: WIP on master: 62d3c2e Last Commit
~~~
Si después de realizar más modificaciones se quiere añadir los cambios de stash al directorio de nuevo se puede hacer uso del comando:
~~~
$ git stash pop
~~~


## Guardando cambios en una rama con stash

Para crear una rama y almacenar cambios en ella con stash se puede hacer uso del comando:
~~~
$ git stash branch branch_name
~~~

## Vaciando stash

Para borrar cambios de stash basta con ejecutar el comando:
~~~
$ git stash drop
~~~
