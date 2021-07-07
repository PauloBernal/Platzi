# Git Rebase: Reorganizando el trabajo realizado

Cuando se quiere integrar cambios a una rama sin dejar rastro de la existencia de otra rama en vez de un merge se realiza un `rebase`. Un rebase añade todos los cambios realizados desde otra rama como si fueran parte de la rama a la que se están añadiendo. Este comando es solo para repositorios locales porque reescribe la historia del repositorio.

## Haciendo rebase

Vale recalcar que hacer rebase en vez de merge es una mala práctica debido a que se estpa cambiando la historia del proyecto (dos ramas tienen exactamente los mismos cambios realizados) y se cambia el registro de cambios. Sin embargo es útil cuando se crea una rama temporal para reparar pequeños errores en el código. Es importante seguir este orden al momento de hacer rebase:
- Hacer rebase desde la rama que se quiere borrar hacia master
- Hacer rebase desde master hacia la rama que se quiere borrar
Caso contrario se entra en un conflicto que solamente se puede solucionar con `reset`. Para hacer rebase de una rama a otra es parecido a como se realiza con merge:
~~~
$ git rebase branch_name
~~~
Con lo cual se añaden los cambios de la rama y se sobreescribe la historia para que no haya una aparente ramificación. Hecho esto al momento de borrar la rama parece que la rama de arreglo de errores nunca existió.
