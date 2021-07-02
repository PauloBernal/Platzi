# Instalando Git

##  En Windows

Se puede descargar Git del sitio web oficial, mientras la instalación es la que viene en Windows por defecto. Es importante verificar que al momento de instalar Git también se instale GitBash. También se debe seleccionar la opción de instalar la librería OpenSSL para tener conexiones seguras. Al terminar de instalar se abre una terminal que usa bash, por lo tanto los comandos son prácticamente los mismos que en Linux


## En MacOS

La instalación es casi la misma que en Windows, descargando el archivo del sitio web oficial de Git. No es necesario instalar Git Bash ni OpenSSL debido a que ya viene por defecto en Mac. Se instala con  un aventana de instalación simplemente configurando las opciones por defecto y se accede desde la terminal de Mac.

## En Linux

En Linux existe lo que se llama un administrador de paquetes, que es la forma de instalar programas y funcionalidades. Para instalar un paquete se usa el comando `apt-get install`, generalmente en modo superusuario con `sudo`. Para instalar Git se ejecuta el comando:
~~~
$ sudo apt-get install git
~~~
Para conocer más acerca de los comandos Linux se puede acceder a los apuntes del [Curso de Introducción a la Terminal](../../../TerminalCourse/notes/FirstSteps/Concepts.md)


---

[Anterior](./IntroToGit.md)

[Siguiente](./CodeEditors.md)

[Índice del curso](../Index.md)
