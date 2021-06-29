# Variables de entorno

Las variables de entorno son configuraciones en el sistema que se pueden almacenar y modificar.

## Link simbólicos
Los link simbólicos son una especie de acceso directo en terminal que permite acceder a una ruta especificada sin necesidad de introducir todo el path cada que se quiera acceder a ella. Para crear un link simbólico se usa la sintaxis:
~~~
$ ln -s /route/ link_name
~~~


## Accediendo a variables de entorno

### Visualizando
Para visualizar las variables de entorno se puede hacer uso del comando `printenv`, el cuál muestra todas las variables de entorno configuradas:
~~~
$ printenv
~~~
Conociendo el nombre de una variable de entorno se puede imprimir el valor de dicha variable en pantalla con el comando `echo`:
~~~
$ echo $VAR_NAME
~~~

### Variables importantes
- `$HOME`.- Esta variable hace referencia al directorio `/home/username` y es una alternativa a '`~`' cuando se quiere acceder al directorio del usuario.
- `$PATH`.- Esta es una variable sumamente importante ya que al momento de usar un ejecutable binario el sistema busca las rutas en esta variable (ya sea NodeJS, Pearl, Python u otros)

### Modificando variables
En Linux existe un archivo en el que se encuentran las configuraciones de bash, el cuál se llama `.bashrc` y se encuentra en el directorio `/home`. En el caso de usar una Mas, este archivo recibe el nombre de `.zshrc`. Dicho archivo se puede abrir en un editor de texto y modificarlo. Se pueden realizar dos tipos de operaciones: modificar o crear 'alias' y variables de entorno. 

#### Alias
Para crear un alias de comando al final del archivo se puede colocar una línea de texto con la siguiente sintaxis:
~~~
alias cmd_name="cmd"
~~~

#### Variables de entorno
Para crear una variable de entorno al final del archivo se puede colocar una línea de texto con la siguiente sintaxis:
~~~
VAR_NAME=var_value 
~~~
En caso de querer concatenar algo a una variable se puede usar los dos puntos y comillas simples:
~~~
VAR_NAME=$VAR_NAME:'add_value'
~~~


## Comandos Útiles
- `printenv` (print environment).- Permite ver todas las variables de entorno configuradas
~~~
$ printenv
~~~
- `ln` (link).- Permite crear links simbólicos u otro tipo de link en terminal
~~~
$ ln -flag /route/ link_name
~~~
- `bash`.- En caso de estar dentro de la terminal de bash actualiza los cambios. Si se está trabajando en otra terminal que no use bash este comando abre una terminal de bash.
~~~
$ bash
~~~

---

[Anterior](./ControlOperators.md)

[Siguiente](./Permits.md)

[Índice del curso](../Index.md)
