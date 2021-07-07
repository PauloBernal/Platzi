# Ignorar archivos en el repositorio con .gitignore

Hay elementos que no se debe añadir al repositorio cuando se quiere compartir o por conveniencia en tema de espacio no se suele añadir. Para estos archivos existe un archivo especial llamado `.gitignore`, en el cual se añade los nombres de los archivos que serán ignorados en el repositorio, ya sea porque son archivos binarios, porque contienen información privada o porque son archivos de configuración del equipo. Añadir un gitignore es una buena práctica ya que permite tener un mejor registro de los cambios en el código. 

### Creando un .gitignore

Es una lista de los archivos que se desean ignorar. Se puede utilizar Wildacards para generalizar una extensión o un nombre de archivo como .log o .jpg,. Para crear un gitignore simplemente se crea un archivo con ese nombre:
~~~
$ touch .gitignore
~~~
O también se puede realizar desde un editor de código cualquiera. Este archivo debe ubicarse en el directorio principal del proyecto. un buen sitio para añadir imágenes u otros binarios es [imgur](https://www.imgur.com)