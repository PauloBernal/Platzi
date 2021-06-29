# Comandos de búsqueda
Estos comandos ayudan a buscar y filtrar archivos y directorios por su extensión, nombre, ubicación, etc. Esto es útil sobretodo al momento de tratar archivos `.log`

## Comando `find`
Este comando sirve para relizar búsquedas, ya sea para encontrar un archivo o un directorio

### Partes del comando
- Ruta.- La ruta especifica el directorio desde el que se empezará a buscar hasta todos los subdirectorios contenidos en este
- Parámetro.- especifica el tipo de búsqueda que se llevará a cabo
- Patrón.- El patrón es la coincidencia que se buscará en los distintos directorios y que cuando se halle se imprimirá en pantalla todos los archivos que coincidan

### Parámetros de find
- name.- Utilizando este parámetro devuelve todas las coincidencias con el nombre especificado como patrón. Con find también se pueden usar Wildcards para una búsqueda más amplia.
- type.- Este parámetro se utiliza para buscar por tipo de elemento. Este recibe dos patrones: `f` (file) para archivos y `d` (directory) para directorios.
- size.- Permite buscar archivos o directorios por tamaño en bytes. Para buscar por Megabytes se puede usar el prefijo **M**.


## Comando `grep`
Este comando sirve para buscar coincidencias dentro de un archivo de texto plano. Se puede buscar por medio de palabras o también se puede hacer uso de expresiones regulares. La sintaxis viene de la forma:
~~~
$ grep "pattern" filename.ext
~~~

### Parámetros
- `i`.- Esto permite buscar un texto sin importar si se trata de mayúsculas o minúsculas
- `c`.- Cuenta la cantidad de coincidencias que hay en el archivo especificado
- `v`.- Devuelve todas las palabras que NO coinciden con el patrón buscado


## Comandos útiles
- `which`.- Este comando busca en todas las rutas del path para encontrar un ejecutable binario
~~~
$ which cmd
~~~
- `find`.- Este comando permite buscar archivos y directorios dependiendo de distintos parámetros
~~~
$ find /route/ -parameter pattern
~~~
- `grep`.- Permite buscar palabras o patrones en archivos de texto
~~~
$ grep "word_or_pattern" filename.ext
~~~
- `wc` (word counter).- Permite contar la cantidad de palabras o caracteres dentro de un archivo de texto
~~~
$ wc filename.ext
~~~


---

[Anterior](./Redirections.md)

[Siguiente](../TerminalUtilities/CompressFiles.md)

[Índice del curso](../Index.md)
