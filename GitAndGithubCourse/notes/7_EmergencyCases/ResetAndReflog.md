# Git Reset y Reflog

A veces se puede borrar una rama o un archivo por accidente y se rompe todo el proyecto. Cuando esto ocurre al ejecutar `git log` no se puede ver los commits en los que estaba la rama o es como si nunca hubiera existido. Para enmendar problemas de este estilo existe un comando llamado `reflog` que permite ver todo el historial de commits y cambios (incluso los realizados en git como un merge o borrar una rama):
~~~
$ git reflog
~~~

Con git reset se puede volver a cuando estaba bien el proyecto como ya se explicó en la parte de `reset`:
~~~
$ git reset --hard hash
~~~
