# Manejo de Procesos
Son formas de tener control sobre los procesos en primer y segundo plano, ya sea visualizandolos, matándolos, parándolos, etc.

## Procesos
Existen dos tipos de procesos, aquellos que se ejecutan en primer plano (foreground) y aquellos que se ejecutan en segundo plano (background). Los procesos en Linux tienen una característica llamada PID (Process ID) el cuál es un número asignado al proceso durante su ejecución y nos permite trabajar con el proceso. Para saber el PID simplemente basta con escribir el comando `ps` en terminal.

### Matando procesos
Para matar un proceso es necesario saber previamente su PID (como se explicó anteriormente) y se hace uso del comando `kill` con la siguiente sintaxis:
~~~
$ kill PID
~~~
También si se quiere matar un proceso que se está ejecutando en primer plano simplemente se puede utilizar la combinación de teclas `Ctrl + C`, si se quiere pausar el proceso se puede hacer con la combinación de teclas `Ctrl + Z`.

### Foreground y Background
Para visualizar los procesos que están detenidos o ejecutándose en segundo plano se puede hacer uso del comando `jobs`
~~~
$ jobs
~~~
En este caso se indica un número de proceso, con dicho número de puede trabajar para enviar los procesos a foreground o background. Para enviar los procesos a foreground se hace uso del comando `fg`
~~~
$ fg num
~~~
De forma similar se trabaja con el comando `bg` para enviar los procesos a background
~~~
$ bg num
~~~
Si se quiere ejecutar un comando directamente en background se puede colocar la final de la línea del comando un '\&' (ampersand) 
~~~
$ cmd &
~~~


## Comandos útiles
- `ps`.- Este comando muestra los procesos que se están ejecutando actualmente
~~~
$ ps
~~~
- `kill`.- Conociendo el ID de un proceso permite terminarlo instantáneamente (si está en foreground)
~~~
$ kill PID
~~~
- `top`.- Permite ver en orden descendente cuales son los procesos que consumen mayor cantidad de recursos. Estos se pueden filtrar con distintas flags (`u` para usuarios, etc)
~~~
$ top
~~~
- `htop`.- Es una versión más evolucionada de top
~~~
$ htop
~~~
- `jobs`.- Muestra los procesos pausados o en segundo plano
~~~
$ jobs
~~~
- `fg`.- Permite enviar los procesos en `jobs` a foreground con el número de proceso
~~~
$ fg num 
~~~
- `bg`.- Permite enviar los procesos en `jobs` a background con el número de proceso
~~~
$ bg num 
~~~