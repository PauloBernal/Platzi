# Permisos

## Tipos de archivos
Al momento de listar los archivos se puede apreciar unos cuantos caracteres que hacen referencia al tipo de archivo que se está tratando.
- Guión (-).- Este hace referencia a un archivo normal
- d .- Este indicador hace referencia a que se trata de un directorio.
- l .- Este indicador hace referencia a que el archivo se trata de un link simbólico
- b .- Este indicador hace referencia a un archivo de bloque especial (generalmente guarda información acerca de una memoria USB o un disco duro externo)

## Tipos de modo

### Usuarios
Hay tres tipos de usuarios al momento de tratar los permisos de un archivo:
- Dueño.- Es el usuario creador del archivo 
- Grupo.- Son otros usuarios a los cuales puede que el dueño haya compartido el archivo
- World.- Son el resto de usuarios que no entran en la categoría de dueño ni de grupo

### Permisos
Existen tres tipos de permisos que se representan con distintas letras:
- Read (r).- Significa que el usuario tiene permiso para ver el contenido del archivo
- Write (w).- El usuario tiene permiso de cambiar y sobreescribir el contenido del archivo
- Execute (x).- El usuario puede ejecutar y hacer uso del archivo

### Representación
Los permisos activos para cada tipo de usuario se representan con un 1 si es que están activos y con un 0 si es que no lo están.

| Owner | Group | World |
| -- | -- | -- |
| r w x | r - x | r - x |
| 1  1  1 | 1  0  1 | 1  0  1 |

Donde se ve un guión son los permisos que no están activos. Como para cada usuario hay un conjunto de unos y ceros de a tres, se hace un sistema de tres bits también conocido como sistema octal.
Siendo así los permisos para cada usuario pueden representarse con números del 0 al 7. En el ejemplo anterior esto quedaría:
| Owner | Group | World |
| -- | -- | -- |
| r w x | r - x | r - x |
| 7 | 5 | 5 |

### Modo simbólico

En este caso se pueden asignar permisos utilizando directamente un comando y un flag del comando. De acuerdo a los símbolos estos se pueden representar:
- u.- Solo para el usuario
- g.- Solo para el grupo
- o.- Solo para otros (world)
- a.- Aplica para todos


## Modificando permisos
Se conoce como root al usuario que tiene acceso a absolutamente todo en el equipo y puede cambiar los permisos de cualquier archivo. Para poder acceder temporalmente a permisos de superusuario se utiliza `sudo` antes de un comando.
~~~
$ sudo cmd
~~~

Para modificar permisos existen distintos comandos que se detallan a continuación.

### Change mode (chmod)
Al usar este comando se cambia los permisos de un archivo para que otros usuarios puedan hacer uso de él. Se necesita especificar los permisos en formato octal y el archivo al cual se le modificará los permisos.
~~~
$ chmod num filename.ext
~~~

***Ejemplo***  *Modificar permisos de solo lectura a grupo y otros de un archivo llamado 'notes.md' a permisos de lectura y escritura*
~~~
$ chmod 766 notes.md
~~~

#### **Modo simbólico con chmod**
Se puede hacer uso del modo simbólico con este comando para añadir o quitar permisos. En caso de querer añadir permisos se puede usar:
~~~
$ chmod sim_mod+permits filename.ext
~~~
usando el '\+' para indicar que se están añadiendo permisos. En el caso de querer quitar permisos se hace uso de la sintaxis:
~~~
$ chmod sim_mod-permits filename.ext
~~~
usando el '\-' para indicar que se están quitando permisos. Por último hay un tercer operador que sirve para sobreescribir permisos el cuál es '\=':
~~~
$ chmod sim_mod=permits filename.ext
~~~
Para escribir múltiples permisos en una sola línea de comando se puede utilizar comas para separar los parámetros como se verá en el siguiente ejemplo.


***Ejemplo*** *Se quiere modificar los permisos de un archivo 'login.txt' para añadir al dueño permisos de escritura y quitar a grupo permisos de ejecución. Como paso final se reescriben los permisos de otros para que solamente tengan permisos de lectura*
~~~
$ chmod u+w,g-x,o=r login.txt
~~~



## Comandos útiles
- `whoami`.- Este comando es útil para saber el usuario actual
~~~
$ whoami
~~~
- `chmod` (change mode).- Este comando permite modificar los permisos y tiene dos sintaxis distintas. En la primera se hace uso de la notación octal de permisos y en la segunda se hace uso del modo simbólico y sus operadores.
~~~
$ chmod num filename.ext
~~~
~~~
$ chmod sim_mod[op]permits filename.ext  
~~~
- `su` (switch user).- Este comando permite alternar entre usuarios (cambiar de usuario)
~~~
$ su username
~~~
- `passwd` (password).- Este comando sirve para cambiar la contraseña del usuario actual
~~~
$ passwd
~~~


---

[Anterior](./EnvironmentVariables.md)

[Siguiente](./Redirections.md)

[Índice del curso](../Index.md)
