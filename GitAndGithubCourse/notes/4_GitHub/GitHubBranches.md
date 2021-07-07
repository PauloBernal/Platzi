# Manejo de ramas en GitHub

## Visualizando ramas

Para visualizar las ramas y los cambios realizados en estas existe un comando llamado `show-branch`
~~~
$ git show-branch
~~~
Para ver más cosas acerca de las ramas se puede utilizar el parámetro `--all`
~~~
$ git show-branch --all
~~~
También git tiene una interfaz visual que se puede abrir con  el comando:
~~~
$ gitk
~~~

## Enviando ramas

Para continuar el flujo de trabajo es probable que se quiera enviar una rama de desarrollo a GitHub. Es por esto que crearon una alternativa que permite enviar ramas enteras a GitHub, con todos los cambios que estas contienen. Para enviar distintas ramas a GitHub se puede hacer uso del comando:
~~~
$ git push remote_repo_name branch_name
~~~
Sin olvidarse de primero traer todos los cambios al repositorio local.

## Configurar múltiples colaboradores en un repositorio

Lo primero es que la persona que está colaborando en el proyecto clone el repositorio remoto en su equipo local. Para esto se crea un directorio y directamente se clona (sin iniciar el repositorio):
~~~
$ git clone <url>
~~~
Al ser un repositorio público al momento de clonarlo no pide usuario y contraseña, lo que sí ocurre en repositorios privados. Los colaboradores pueden cambiar los archivos de forma normal al igual que el flujo de trabajo local funciona de forma normal. Al clonar el repositorio se copia todo el historial de cambios previos. Como una buena práctica después de clonar puede verificar con `pull` que no hayan más cambios, y posteriormente puede enviar los suyos al repositorio con `push`. Para que alguien pueda hacer `push` lo primero es que sea añadido al repositorio por la persona que maneja el proyecto. Hay dos maneras de hacer esto: por correo electrónico o por nombre de usuario. Para añadir colaboradores se debe acceder a los ajustes del repositorio en la sección de 'Collaborators' o 'Manage access', ahí hay un cuadro de texto donde se debe añadir el nombre de usuario o el correo electrónico del colaborador. El paso final para añadir un colaborador es enviar un correo o un link al usuario para que acepte colaborar en el proyecto.
