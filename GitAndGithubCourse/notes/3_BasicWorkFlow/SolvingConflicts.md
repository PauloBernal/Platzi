# Resolución de conflictos al hacer un merge

## Conflictos

Los conflictos en merge generalmente ocurren debido a una línea de texto modificada en el mismo archivo. Al momento de hacer merge ocurre que git indica los archivos queentraron en conflicto. Si se está haciendo uso de VS Code, este resalta las líneas en conflicto y en ambos casos se indica que se debe resolver el conflicto antes de hacer merge.


## Resolviendo conflictos

Para resolver un conflicto durante un merge se puede conservar uno de los cambios solamente, esto modificando el archivo en una de las ramas antes de realizar el merge nuevamente. También se puede utilizar `reset` para volver a una versión anterior en una de las ramas antes de que surja el conflicto. Finalmente se debe confirmar el merge con un commit, para lo cual se puede utilizar el comando
~~~
git merge --continue
~~~
o directamente con el comando
~~~
$ git commit -am "message"
~~~
También es posible que simplemente se quiera cancelar o abortar el merge en proceso. Para esto es posible utilizar el comando:
~~~
$ git merge --abort
~~~


## Comandos útiles

- `merge --continue`.- Este comando se utiliza cuando se quiere reanudar el proceso de merge después de haber resuelto conflictos
~~~
$ git merge --continue
~~~
- `merge --abort`.- Este comando se utiliza cuando se quiere abortar el proceso de merge en vez de solucionar el conflicto para reanudar
~~~
$ git merge --abort
~~~
