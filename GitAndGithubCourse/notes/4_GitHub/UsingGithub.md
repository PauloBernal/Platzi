# Uso de GitHub

## ¿Qué es GitHub?

GitHub es un sitio web que funciona como un superservidor de Git en el cuál los usuarios pueden crear un repositorio remoto y compartirlo con otros usuarios. También tiene una interfaz visual que permite visualizar los cambios y colaboraciones en el repositorio del proyecto. Debido a la gran popularidad de la plataforma muchos la llaman la red social de los programadores.

## Iniciando en GitHub

Primero se debe crear una cuenta en la plataforma como se hace en cualquier otra. Existen diversas opciones entre las que están importar un repositorio (puede ser de otro sistema de control de versiones) o crear uno nuevo. Al momento de crear un repositorio este nos pide un título para el repositorio y una descripción. También se puede escoger si es público o privado, si se inicia con un `README.md`, el cuál es un archivo que describe el proyecto y es útil para personas que colaboran o acceden de este, un gitignore y una licencia.

### Reconociendo la interfaz (archivos)

Sobre el los archivos que se abren en la plataforma hay algunas opciones:

- Raw.- Permite visualizar el texto plano del archivo
- Blame.- Permite ver el historial de commits junto a los usuarios que los realizaron
- History (obsoleto).- Permitía ver el historial de commits
- Computadora (ícono).- Permite abrir el archivo en GitHub Desktop si es que se tiene el programa
- Lápiz (ícono).- Permite editar el archivo en el mismo repositorio remoto
- Basurero (ícono).- Permite borrar el archivo del repositorio remoto

### Editando archivos

Al editar los archivos de texto plano en GitHub se puede realizar un commit en la misma plataforma. Esto en una interfaz con un cuadro de texto. En GitHub también se puede visualizar todo el historial de commits de el archivo editado, de igual forma ocurre al llevarlo al repositorio local.


## Trabajando con Github

### Trayendo un repositorio remoto de GitHub

Para trabajar con u repositorio en GitHub es necesario primero clonar dicho repositorio. Para eso en la página de nuestro repositorio se encuentra una opción llamada 'Clone or download'. Haciendo click en esta permite desplegar una lista de formas de clonar el repositorio, en este caso se hará el uso de la url. En el repositorio local se crea un origen remoto de los archivos para trabajar con el repositorio remoto. Esto se hace por medio del comando:
~~~
$ git remote add remote_repo_name url
~~~
En el cual se debe especificar el nombre del repositorio remoto y la url del repositorio remoto. Por conveniencia este nombre suele ser `origin`, por lo que el comando sería:
~~~
$ git remote add origin url
~~~

### Visualizando repositorios remotos

Hacer esto es bastante simple por medio del comando `remote` y sus parámetros.

- Para solamente visualizar los nombres de los repositorios remotos
~~~
$ git remote
~~~
- Para visualizar de una forma detallada los repositorios remotos
~~~
$ git remote -v
~~~

### Trayendo cambios

Existen dos formas de hacer esto. La primera es por medio del comando fetch que trae los cambios pero no los integra al directorio. La segunda y la que se verá a continuación es `pull`. Este comando permite traer los cambios del repositorio remoto al repositorio local e integrar dichos cambios en el directrio de trabajo.
~~~
$ git pull remote_repo name remote_repo_branch
~~~
Generalmente dichos nombres suelen ser:
~~~
$ git pull origin master
~~~

#### Historiales no relacionados

A veces cuando el repositorio remoto contiene archivos distintos a los del repositorio local o los commits de ambos no están relacionados ocurre un error denominado 'unrelated histories'. Esto es bastante simple de solucionar utilizando el parámetro `--allow-unrelated-histories` para indicar que los dos repositorios no están relacionados previamente. 
~~~
$ git pull --allow-unrelated-histories remote_repo_name remote_repo_branch
~~~
~~~
$ git pull --allow-unrelated-histories origin master
~~~

### Llevando cambios

Para llevar archivos y cambios de un repositorio local a un repositorio remoto es necesario primero realizar un `pull` (traer los archivos del repositorio remoto) y posteriormente para llevar todos los cambios en los archivos se usa el comando `push` de forma similar a `pull`:
~~~
$ git push remote_repo_name remote_repo_branch
~~~
~~~
$ git push origin master
~~~
