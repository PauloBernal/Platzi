# Git cherry-pick: traer commits viejos al HEAD de un branch

Cuando se necesita en master un avance que se realiza en una rama alterna se utiliza un comando llamado `cherry-pick`. Para esto es necesario conocer el hash de dicho commit:
~~~
$ git cherry-pick hash
~~~
Esto trae el commit a la rama master incluyendo el mensaje con el que se realizó dicho commit. Al ver el historial de commits sale el antiguo commit realizado como si fuera el HEAD de la rama master. Para fusionar definitivamente ambas ramas se utiliza un merge como de costumbre.

Esto es una mala práctica porque cambia la historia de los commits realizados.
