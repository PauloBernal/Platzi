# **Wildcards**

## Sintaxis
En este caso se hará uso del comando `ls` para demostrar la funcionalidad de las Wildcards. Para listar los elementos que coincidan con las Wildcards en un directorio se usa el comando:
~~~
$ ls *wildcard*
~~~
dentro del directorio a buscar. Para listar solamente elementos del directorio actual se usa la opción `-d`, la cuál se usará de ahora en adelante para explicar las Wildcards debido a que por defecto busca en 3 niveles:
~~~
$ ls -d *wildcard*
~~~

## Caracteres especiales

### **\* (asterisco)**
El asterisco se utiliza para representar un número indefinido de caracteres.

***Ejemplo*** *Cuando se quiere buscar solamente directorios se usa el comando:*
~~~
$ ls -d */
~~~ 

*Y cuando se quiere buscar solamente archivos (con una extensión) se usa el comando:*
 ~~~
 $ ls -d *.*
 ~~~

### **\? (interrogación)**
El signo de interrogación se usa al momento de hacer referencia a solamente un caracter.

***Ejemplo*** *Cuando se quiere buscar archivos enumerados como file1.txt, file2.txt, etc. se puede hacer uso del comando:*
~~~
$ ls -d file?.txt
~~~

## Tipo de letra

### **Mayúsculas**
Para esto se hace uso de una sintaxis en particular de la forma `[[:upper:]]` (upper hace referencia a la letra mayúscula que se busca)

***Ejemplo*** *Para listar directorios y archivos que comiencen con una letra mayúscula se puede hacer uso del comando:*
~~~
$ ls -d [[:upper:]]*
~~~

### **Minúsculas**
Para esto se hace uso de una sintaxis en particular de la forma `[[:lower:]]` (lower hace referencia a la letra minúscula que se busca)

***Ejemplo*** *Para listar directorios y archivos que empiecen y terminen con una letra minúscula se puede hacer uso del comando:*
~~~
$ ls -d [[:lower]]*[[:lower:]]
~~~


## Clases
Las clases hacen referencia a un conjunto de caracteres que pueden coincidir en algún punto.

***Ejemplo*** *Para listar los archivos cuyo nombre acabe en __z__ o __s__ (sin considerar extensión)*
~~~
$ ls -d *[szSZ].*
~~~
