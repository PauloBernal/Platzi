# Comprimiendo archivos

## TAR
Este es un formato de compresión generalmente utilizado en repositorios. Para comprimir en formato 'tar' se usa el comando:
~~~
$ tar -flags Compressed_name.tar dirname
~~~

### Parámetros
- `c` (compress).- Este parámetro se usa para comprimir un elemento.
- `v` (verbose).- Da información detallada en terminal acerca del estado de compresión.
- `f` (file).- Indica que el elemento a ser compreso es un archivo
- `z` (zip).- Comprime el archivo a un formato `.gzip`
- `x` (extract).- Descomprime el archivo o directorio seleccionado

Es importante tomar en cuenta el orden de los parámetros ya que `c` o `x` deben estar al inicio, debe seguir `v`, opcionalmente `z` después y finalmente `f`.


## ZIP
Es un formato de compresión que hace uso de un algoritmo de árboles binarios. Para usarlo se requiere la siguiente sintaxis:
~~~
$ zip -flags Zip_name.zip file_or_dir_name
~~~
Para descomprimir un archivo en formato `.zip` se hace uso del comando `unzip` con la siguiente sintaxis:
~~~
$ unzip Zip_name.zip
~~~

### Parámetros
- `r` (recursive).- Permite comprimir de forma recursiva un directorio


## RAR
La sintaxis para compresión en rar es practicamente la misma que en zip, solamente cambian los nombres de los comandos.
Para comprimir en rar:
~~~
$ rar -flags Rar_name.rar file_or_dir_name
~~~
Para descomprimir en rar:
~~~
$ unrar -flags Rar_name.rar
~~~

### Parámetros
- `r` (recursive).- Permite comprimir de forma recursiva un directorio
