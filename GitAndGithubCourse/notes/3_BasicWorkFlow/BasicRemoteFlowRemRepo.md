# Flujo de trabajo básico con un repositorio remoto

## Flujo local

Como ya se explicó anteriormente hay tres áreas en el entorno local, el directorio de trabajo, el área de preparación o staging y el repositorio local donde se almacena el historial de versiones. Inicialmente los cambios están en el directorio de trabajo, para llevarlos a Staging se utiliza el comando `add`, con lo que Git empieza a llevar un registro de los cambios añadidos lo que se representa con dos estados 'tracked' (rastreado) o 'untracked' (no rastreado). Los cambios en staging como son almacenados en memoria RAM se pueden perder con el tiempo debido al Garbage Collector que es un sistema encargado de liberar para mantener en uso la memoria RAM durante el flujo de trabajo. Para enviar perder dichos cambios en Git es necesario confirmar los cambios y enviarlos al repositorio, para lo cual se usa el comando `commit`, con lo cual posteriormente se puede acceder a historial de versiones.


## Repositorio local y repositorio remoto

Un repositorio local es aquel que permite ver el historial de versiones en una máquina donde el flujo de trabajo sea de forma individual (entorno de desarrollo personal). El repositorio remoto es aquel que está en otra máquina y al cuál se puede acceder por medio de la red. Ejemplos de repositorios remotos pueden ser GitHub, GitLab o uno configurado de forma manual. Este tipo de repositorios son útiles al momento de trabajar con equipos de forma remota.


## Trabajando con repositorios remotos

### Clonar un repositorio remoto

Para traer datos de un repositorio remoto al repositorio local este se clona en la máquina en la que se quiere continuar con el desarrollo. Para esto existe el comando `clone`, que permite clonar los datos del repositorio remoto al repositorio local
~~~
$ git clone url
~~~
Hay que tener en cuenta que esto solo clona los archivos, no se puede acceder de esta forma al historial de cambios del repositorio remoto.

### Enviar cambios al repositorio remoto

Una vez que se trabajó en el repositorio clonado y ya se tienen listos los cambios para añadirlos la repositorio remoto se hace uso del comando `push` de Git.
~~~
$ git push
~~~

### Traer cambios del repositorio remoto

Cuando se desea traer los cambios que alguien más realizó (una vez que se tiene el repositorio clonado) se hace lo que se denomina un fetch (extraer) con el comando del mismo nombre.
~~~
$ git fetch
~~~
Esto trae los cambios al repositorio, no al directorio de trabajo. Para llevar los cambios al directorio de trabajo es necesario fusionar las ramas, lo que se denomina un merge
~~~
$ git merge 
~~~

Existe un comando que hace el trabajo de `fetch` y `merge` juntos, llamado `pull`, el cuál trae los cambios del repositorio remoto y los aplica al directorio de trabajo. 
~~~
$ git pull
~~~


## Comandos útiles

- `clone`.- Este comando sirve para clonar un repositorio remoto para trabajar como repositorio local
~~~
$ git clone url
~~~
