# Diferencias entre `reset` y `rm`

Estos comandos se pueden utilizar de forma similar, sin embargo es importante no confundirlos.

## Remover (`rm`)

Este comando permite eliminar archivos del flujo de Git sin eliminar su historial de versiones en el repositorio. Esto es útil ya que si por accidente borramos un archivo del disco duro se puede hacer uso de `reset` o `checkout` para volver a como estaba antes. Hay dos formas de remover un archivo en Git:
- `--cached`.- Esto borra los archivos del area de staging (y por lo tanto del siguiente commit a realizar) pero mantiene estos en disco duro
- `--force`.- Este último borra los cambios en staging y los archivos del disco duro


## Resetear (`reset`)

Este comando permite volver a versiones pasadas sin opción a acceder a las versiones posteriores a esa (borra todo el historial de cambios después de la versión a la que se está regresando). Hay dos formas de realizar un `reset` en Git:
- `--soft`.- Esto borra todo el historial de versiones posteriores a la que se está cambiando pero mantiene todos los cambios en staging en caso de que se quiera volver al último estado de cambios
- `--hard`.- ESto borra todo el historial de versiones posteriores a la que se está regresando eliminando todos los cambios de staging también


## Utilizando `reset` para limpiar staging

El comando `reset` tiene un uso más ya que permite regresar los archivos de staging a unstaged, en el directorio. esto se hace utilizando:
~~~
$ git reset HEAD
~~~
Esto es útil ya que a diferencia de `rm` no borra el archivo de git, como se dijo anteriormente, solamente lo mueve de Staging a unstaged, con lo que después de realizar los cambios pertinentes se puede regresar dichos cambios a staging con `git add .`
