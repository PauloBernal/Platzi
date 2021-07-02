# Iniciando un repositorio de Git

## Configurando git

Antes de trabajar con repositorios es importante configurar git para que se sepa quién está realizando los cambios 8en caso de que se trabaje en un proyecto con un equipo). Para acceder a las opciones de configuración de git existe el comando `config`
~~~
$ git config --configuration
~~~
Con el parámetro `list` se puede ver la configuración por defecto de git
~~~
$ git config --list
~~~
Y si este se utiliza junto al parámetro `show-origin` se puede ver las configuraciones guardadas
~~~
$ git config --list --show-origin
~~~

### Nombre de usuario

Para configurar el nombre de usuario se utiliza el parámetro `global` del comando `config`, lo que nos permite modificar las variables globales. Para este caso se modifica la propiedad `user.name`.
~~~
$ git config --global user.name "Username"
~~~

### Correo electrónico
Al igual que al modificar el nombre de usuario se utiliza el comando `config` con el parámetro `global`, solo que esta vez modificando `user.email`
~~~
$ git config --global user.email "example@email.dom" 
~~~


## Creando un repositorio

Una vez que se está dentro del directorio en el que se trabajará, se utiliza comandos de Git para realizar el manejo de versiones. Previo a esto es importante iniciar el repositorio en el que se trabajará (repositorio es el directorio donde están los archivos del proyecto y en el cuál se almacenan los cambios realizados). Para iniciar un repositorio se utiliza el comando `init` de Git.
~~~
$ git init
~~~
Para confirmar que se inició un repositorio se puede listar los archivos ocultos con el comando
~~~
$ ls -la
~~~
Y ahí debe haber un directorio llamado `.git`, con el cual queda verificado que se inició de forma satisfactoria un repositorio. Para ver los archivos que se añadieron al repositorio (o los cambios) se puede hacer uso del comando `status` de git:
~~~
$ git status
~~~
el cuál indica el estado del repositorio. Los cambios resaltados con rojo son aquellos que no fueron añadidos al repositorio.


## Añadiendo y retirando elementos del repositorio

### Añadiendo cambios

Al momento de añadir cambios estos se almacenan en un espacio denominado 'staging' donde se almacenan temporalmente múltiples cambios para posteriormente ser confirmados. Para añadir cambios se utiliza el comando `add` de git, el cuál permite añadir un archivo o un directorio.
~~~
$ git add filename.ext
~~~
~~~
$ git add dirname/
~~~
Para añadir todos los cambios al repositorio se utiliza la ruta relativa `.` que hace referencia al directoro actual:
~~~
$ git add .
~~~

### Retirando cambios

Para retirar un cambio de staging se utiliza el comando `rm` que funciona de forma similar a `add`, sin embargo posee dos parámetros que indican la forma en la que se remueven los cambios.
~~~
$ git rm -flag filename.ext
~~~
Para remover directorios completos es necesario especificar que se realice de forma recursiva
~~~
$ git rm -r -flag dirname/
~~~
Existen dos opciones para remover cambios de staging:
- `-f`.- Remueve los cambios de staging y borra el archivo completamente
~~~
$ git rm -f filename.ext
~~~
- `--cached`.- Remueve los cambios de staging pero el archivo permanece intacto en el directorio
~~~
$ git rm --cached filename.ext
~~~
Estas opciones también se aplican a directorios con el flag `-r` (recursive).


### Confirmando cambios

Para enviar los cambios en staging al repositorio se utiliza el comando `commit`, el cuál requiere de un mensaje descriptivo de los cambios realizados como una buena práctica para reconocer la versión.
~~~
$ git commit -m "message"
~~~


## Comandos útiles

- `init`.- Sirve para iniciar un repositorio dentro de un directorio
~~~
$ git init
~~~
- `add`.- Se utiliza para añadir los cambios a staging
~~~
$ git add filename.ext
~~~
- `rm`.- Se utiliza para remover cambios de staging
~~~
$ git rm --cached filename
~~~
~~~
$ git rm --cached -r dirname/
~~~
- `commit`.- Se utiliza para confirmar cambios con un mensaje descriptivo
~~~
$ git commit -m "message"
~~~
- `status`.- Sirve para ver los cambios que fueron o no añadidos (antes de ser confirmados)
~~~
$ git status
~~~
- `show`.- Muestra todos los cambios hechos dentro del repositorio con fecha de modificación y usuario que realizó la modificación
~~~
$ git show
~~~
- `log`.- Muestra el historial de cambios realizados a un archivo en específico
~~~
$ git log filename.ext
~~~


---

[Anterior](../1_Introduction/IntroductionToTerminal.md)

[Siguiente](./Wildcards.md)

[Índice del curso](../Index.md)
