# Introducción a Git

## ¿Qué son Git y GitHub?

Git es un sistema de control de versiones, lo cual permite que en un proyecto grande si en algún momento ocurre un error se pueda volver al momento en el que el proyecto era funcional sin perder los cambios y configuraciones realizadas posteriormente. En la máquina local se maneja Git, que permite trbajar a un individuo que forma parte de un equipo de trabajo de forma independiente para luego juntar los cambios. Para trabajar en equipo, llevar registro de las actualizaciones y contribuciones del equipo se utiliza una plataforma como GitHub (también llamada la red social del código).

### Pasos para manejar un directorio en Git

- Crear un directorio
- Volverlo un repositorio de Git
- Añadir los archivos
- Confirmar los cambios en el repositorio

### Sistemas de control de versiones

Son sistemas que permiten llevar un registro de un proyecto grande a lo largo del tiempo. Estos sistemas registran los cambios y sus datos como fecha en la que se realizó, quién realizó el cambio, etc. y permite volver a un momento en específico del proyecto. El sistema de control de versiones más popular es Git, el cuál fue creado por Linus Torvalds (creador de Linux). Git solamente registra los cambios para no estar registrando todo el archivo cada que se actualiza o se borra algo en él.


## Empezando en Git

### Iniciar un repositorio

El primer paso para usar git en un directorio es iniciar un repositorio dentro de este. Antes de cualquier comando se debe especificar que se trata de una funcionalidad de Git con la palabra `git` al inicio. Para iniciar un repositorio se requiere hacer uso del comando `init` dentro del directorio en el que se manejará Git.

### Añadir cambios

Una vez que se crea o se modifica un archivo dentro del directorio es necesario añadir los cambios. Para añadir cambios se utiliza el comando `add` seguido del nombre del archivo o directorio que se quiere añadir.

### Confirmar cambios

Para confirmar los cambios realizados en el repositorio se hace uso del comando `commit`. Antes de confirmar es necesario escribir un mensaje de confirmación que será útil para reconocer que cambios se están haciendo.


---

[Siguiente](./InstallingGit_GitBash.md)

[Índice del curso](../Index.md)

