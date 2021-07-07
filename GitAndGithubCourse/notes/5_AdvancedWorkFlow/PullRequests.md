# Utilizando Pull Requests en GitHub

## Como colaborador

Cuando se está trabajando en un proyecto por lo general lo que se hace es trabajar en ramas de desarrolllo distintas a master. Cuando se quiere integrar los cambios al proyecto lo recomendable es enviar primero esas ramas de desarrollo en vez de realizar directamente el merge a master y posteriormente realizar un pull request. Hay una sección para realizar el pull request de forma manual, de todas formas al realizar un cambio en una rama GitHub automáticamente sugiere realizar un pull request con 'Compare and pull request'. Ahí GitHub indica si es posible realizar el merge a master. El nombre del Pull request toma el nombre del último commit de la rama a fusionar, se puede agregar una descripción y personas que revisen los cambios antes de integrarlos a master.  

### Revisando Pull Requests

una vez que se asigna un grupo de personas para revisar los cambios y aprobar o rechazar el merge, a estas les llegará una notificaión indicando que revisen dichos cambios. De estos depende aprobar o no el merge, realizar sugerencias o dejando un comentario. Dependiendo de esto le llegará a la persona que realizó el pull request una notificación para realizar cambios en caso de que el pull request haya sido rechazado. Estos cambios se registran en el mismo pull request que se mantiene hasta que dichos cambios sean aceptados o bien se cancelen. A este proceso se denomina 'Code Review' y son una buena práctica para llevar registro de que todos los cambios realizados no afecten de forma negativa el proyecto. Una vez aceptado un pull request es posible desde la interfaz de GitHub borrar la rama en la que se realizaron los cambios.


## Como contribuidor independiente

Una persona que no forma parte del proyecto como colaborador puede hacer cambios a este por medio de pull requests, sin embargo no puede crear tags, hacer merge, hacer push ni opciones a las que solamente pueden acceder colaboradores del proyecto. 

### Forks

Un fork es una forma de clonar un proyecto en su estado actual y llevar el desarrollo del mismo de forma independiente. Esta es una característica específica de Github, no de Git. Para hacer fork en la pestaña del repositorio existe una opción llamada 'Fork'. Es importante tener en cuenta que solamente se puede hacer fork sin ser colaborador a un proyecto si este es público, en caso contrario pedirá usuario y contraseña para acceder al contenido del mismo. Para obtener el repositorio en el equipo local se realiza el proceso de clonar un repositorio:
~~~
$ git clone url
~~~
Es posible comparar los cambios que se tiene en el repositorio original y en el fork después de haber realizado cambios con el flujo estándar. Si se quiere contribuir con el proyecto se puede realizar un pull request o un draft pull request que es una forma de esperar antes de enviar el pull request.

### Manejando Pull Requests en local

Para manejar y probar cambios realizados con pull requests es recomendable crear otra fuente para traer los cambios del repositorio original. Para esto se añade un nuevo repositorio remoto que generalmente recibe el nombre de `upstream`:
~~~
$ git remote add upstream url
~~~
Lo cual se puede comprobar por medio del comando
~~~
$ git remote -v
~~~
Una vez se tiene el segundo repositorio remoto se puede realizar el pull al repositorio remoto para obtener cambios y finalmente :
~~~
$ git pull upstream master
~~~
Para enviar cambios al repositorio simplemente se hace push al repositorio remoto:
~~~
$ git push origin master
~~~
Así se tiene dos versiones completamente actualizadas
