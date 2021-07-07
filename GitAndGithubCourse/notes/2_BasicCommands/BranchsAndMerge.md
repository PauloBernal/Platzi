# Ramas (branch) y merge en Git

## Ramas

Se denomina rama a un flujo del proyecto el cuál tiene múltiples versiones. La rama por defecto en Git se llama `master` (maestra) y existen otros tipos de ramas también que suelen ser muy comunes:
- `master`.- Es la rama en la que están las versiones finales del proyecto
- `main`.- Es la rama principal del desarrollo del proyecto
- `development`.- Es la rama en la que se realizan cambios experimentales sobre el proyecto
- `hotpix`.- Es la rama en la que se realiza la corrección de un error en el proyecto para después unirlo rápidamente a la rama `master`

## Merge

Se denomina hacer 'merge' en Git a fusionar los cambios realizados en dos ramas para obtener una versión completa con todos los cambios. Esto es útil al momento de trabajar en proyectos grandes, debido a que se puede fusionar los cambios de múltiples desarrolladores en una sola versión definitiva. Cuando un merge de dos ramas ocasiona que el flujo de una de ellas se rompa esto se denomina un 'conflicto'.
