# Ciclo básico de trabajo en Git

## Directorios y zonas

### Directorio del Proyecto

El directorio del proyecto es aquel en el que se almacenan los archivos del mismo. A este van los cambios que se realizan directamente con un editor de código y se guardan en los archivos (sin utilizar comandos de Git).

### Staging

Staging es una zona en memoria RAM donde se almacenan los cambios realizados de forma temporal antes de ser enviados al repositorio. Los cambios que se realizaron en el directorio del proyecto se agregan a staging con el comando `add` de git y se remueven de este con `rm` en caso de querer cambiar algo antes de ser enviado al repositorio.

## Repositorio

El repositorio es el directorio que almacena el historial de cambios del proyecto. Este se crea al utilizar el comando `init` de Git, y al cuál van los cambios almacenados en staging. Estos cambios van al repositorio con un mensaje por medio de un comando llamado `commit`.