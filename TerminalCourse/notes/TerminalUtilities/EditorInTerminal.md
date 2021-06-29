# Editores de texto en la terminal

Hay distintos editores de texto dentro de la terminal, en este caso se utilizará el editor "Vim" aunque existen otras alternativas como "Nano" o "Emax". Existen dos versiones de Vim, una es "Vi" (la versión antigua) y otra es "Vim" (Vi modern).

## Abrir en terminal

Para abrir el editor de texto Vim en terminal se hace uso del comando `vim`
~~~
$ vim filename.ext
~~~
Si se quiere crear un archivo de texto en Vim simplemente se ejecuta el comando `vim` con el nombre del nuevo archivo. Para salir de Vim simplemente se debe escribir `:q` y se volverá a terminal.


## Editando archivos

### Cambiando de modo

Vim tiene dos modos por defecto, el modo normal o de lectura y el modo insertar o de edición. Para cambiar del modo normal al modo de edición se hace uso de la tecla `i`. Cuando se está escribiendo Vim tiene un resaltado de sintaxis dependiendo del lenguaje o extensión que se esté usando. Para cambiar al modo normal simplemente se presiona la tecla `Esc`.  

### Teclas o combinaciones útiles
- `/`.- Permite buscar texto dentro del archivo en el modo normal
- `dd`.- Permite borrar una línea completa en el modo normal
- `i`.- Permite cambiar al modo de inserción
- `:w`.- Guarda los cambios realizados en el archivo
- `:q`.- Sale de Vim
- `:wq`.- Sale de Vim habiendo guardado los cambios previamente
- `:q!`.- Sale de forma agresiva (directamente o sin guardar cambios)