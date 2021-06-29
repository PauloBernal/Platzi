# **Introducción a la línea de comandos (bash)**

## **Comandos Útiles**

### Información Directorios
- `pwd`.- (print working directory).- Permite ver el directorio actual
~~~
$ pwd
~~~
- `ls`.- (list).- Lista los elementos dentro de un directorio
~~~
$ ls
~~~
- `cd`.- (change directory).- Permite cambiar de un directorio a otro, ya sea por rutas absolutas o relativas
~~~
$ cd route/
~~~
- `file`.- Describe información acerca de un archivo (extensión, contenido, etc)
~~~
$ file filename.ext
~~~
- `tree`.- Permite visualizar todos los directorios y archivos como un árbol de nodos
~~~
$ tree dirname/
~~~

### Manipulación de archivos y directorios
- `mkdir` (make directory).- Crea un directorio con el nombre o la ruta especificada
~~~
$ mkdir dirname/
~~~
- `touch`.- Crea un archivo con el nombre y extensión especificados
~~~
$ touch filename.ext
~~~
- `cp` (copy).- Copia el contenido del archivo de origen al archivo de destino
~~~
$ cp originfile.ext destinationfie.ext
~~~
- `mv` (move).- Permite cambiar la ubicación del archivo a la rute especificada. También sirve para renombrar archivos si se mueve un archivo al mismo directorio
~~~
$ mv filename.ext /destinationroute/
~~~
- `rm \[filename]` (remove).- Hay que tener cuidado con este comando ya que borra el archivo especificado sin confirmación previa
~~~
$ rm filename.ext
~~~

### Viendo el contenido de archivos

- `head`.- Muestra las primeras 10 líneas de un archivo de texto
~~~
$ head filename.ext
~~~
- `tail`.- Muestra las últimas 10 líneas de un archivo de texto
~~~
$ tail filename.ext
~~~
- `less`.- Muestra todo el archivo de texto de forma interactiva. Con '\/' se puede realizar una búsqueda dentro del archivo y con 'q' se sale de la vista interactiva
~~~
$ less filename.ext
~~~
- `xdg-open`.- Abre el archivo en el programa predeterminado por el usuario. En caso de url lo abre en el navegador y en caso de archivo en el editor de texto (Linux)
~~~
$ xdg-open filename.ext
~~~
- `nautilus`.- Accede al explorador de archivos en el directorio indicado (solamente en Ubuntu)
~~~
$ nautilus dirname/
~~~
- `code`.- Abre Visual Studio Code en la ruta especificada
~~~
$ code /route/
~~~

### Trabajando con comandos

- `man`.- Muestra un manual del comando especificado
~~~
$ man command
~~~
- `help`.- Muestra la funcionalidad y opciones de un comando especificado
~~~
$ help command
~~~
- `type`.- Muestra en la terminal el tipo del comando que se especifica
~~~
$ type command
~~~
- `alias`.- Permite crear comandos a partir de comandos ya establecidos de forma TEMPORAL
~~~
$ alias new_command="shell_command"
~~~
- `info`.- Da información acerca del comando especificado
~~~
$ info command
~~~
- `whatis`.- Brinda una breve descripción del comando especificado
~~~
$ whatis command
~~~


### Comandos extra

- `clear`.- Limpia los comandos previamente escritos en la terminal
~~~
$ clear
~~~

---

## **Opciones y parámetros**

### Comando 'ls'
- `-l` (long).- Lista información acerca de los archivos (peso, tipo, fecha de modificación, etc)
- `-a` (all).- Lista todas las carpetas y archivos (incluyendo los ocultos)
- `-h` (human).- Permite lectura humana de la información
- `-S` (size).- Ordena los directorios y archivos por 
- `-d` (directory).- Lista solamente los directorios y archivos en primer nivel
- `-r` (reverse).- Lista los elementos al revés (de la **Z** a la **A**)
~~~
$ ls -lahSdr
~~~

### Comando 'tree'
- `-L` \[num] (levels).- El árbol solamente muestra el número de niveles especificado 
~~~
$ tree -L n
~~~

### Comando 'rm'
- `-i` (interactive).- Tiene una entrada de confirmación antes de borrar un archivo
- `-r` (recursive).- Sirve para borrar directorios con archivos sin contenido
- `-f` (force).- Hay que tener cuidado con esta opción debido a que elimina directorios enteros junto con los archivos que hay dentro de ellos
~~~
$ rm -irf elementName
~~~

### Comandos 'head' y 'tail
- `-n` \[num] .- Modifica el número de líneas que se muestran por defecto
~~~
$ head filename.ext -n n 
~~~
~~~
$ tail filename.ext -n n 
~~~

---

## **Información extra**

### Rutas relativas

- **.** (punto) .- El punto hace referencia al directorio actual en el que se está trabajando
~~~
$ cd ./
~~~
- **. .** (dos puntos) .- Los dos puntos hacen referencia al directorio padre del directorio actual
~~~
$ cd ../
~~~
- **\-** (guión) .- El guión hace referencia al último directorio visitado
~~~
$ cd -
~~~
- **~** (virguilla) .- La virguilla hace referencia al directorio del usuario en /home
~~~
$ cd ~/
~~~

### Crear múltiples archivos y directorios

- Para crear múltiples directorios en un solo comando:
~~~
mkdir [dir 1] [dir 2] ... [dir n]
~~~
- Para crear múltiples archivos en un solo comando
~~~
touch [file 1] [file 2] ... [file n]
~~~

## **Combinaciones de teclas útiles en la terminal**
- `Ctrl + L` .- Limpia la terminal al igual que el comando 'clear'
- `Ctrl + C` .- Cancela cualquier proceso que esté ejecutando la terminal


---

[Anterior](./Concepts.md)

[Siguiente](./Wildcards.md)

[Índice del curso](../Index.md)
