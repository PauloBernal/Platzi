# Reconstruir commits en Git con amend

A veces se cometen errores al momento de enviar un commit. Para enmendar esto existe un parámetro del comando commit llamado `--amend` (enmendar), que pega lo que se añade al commit anterior sin necesidad de crear uno nuevo. Para realizar esto, después de añadir los cambios que se nos olvidaron se utiliza el comando:
~~~
$ git add .
~~~
Para posteriormente realizar el commit con:
~~~
$ git commit --amend
~~~
Al realizar el commit es posible cambiar el mensaje del mismo si se desea.
