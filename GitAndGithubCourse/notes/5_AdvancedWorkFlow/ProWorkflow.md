# Trabajando con flujos de trabajo profesionales

Por cuestión de buenas prácticas no se debe añadir imágenes ni otros archivos binarios a un repositorio. Esto debido a que no se puede mostrar las diferencias en un archivo binario, por lo que son archivos completamente distintos de los cuales debe tener registro el repositorio. También al trabajar con binarios GitHub crea un caché especial para manejarlos, es por esto que al momento de realizar cambios con binarios se retrasa el flujo de trabajo.

## Haciendo merge de ramas de desarrollo a master (para colaboradores)

Cuando se está colabroando en un proyecto en GitHub no se suele hacer los cambios directamente en la rama `master`, sino que se trae las ramas de desarrollo al proyecto para trabajar en ellas. Para realizar cambios en master simplemente se debe hacer merge entre las ramas de desarrollo y la rama `master` (quien generalmente se encarga de esto es el project manager o el CTO por cuestiones de seguridad y estabilidad en el proyecto). 


## Para no colaboradores

### Pull requests

#### Introducción

Por lo general se bloquea la posibilidad de hacer merge a la rama master a excepción del administrador del proyecto. La rama master susle formar parte de algo llamado servidor de producción donde se almacenan las versiones finales del desarrollo (después de que se implementan todos los cambios necesarios para incluir una nueva versión abierta para todos). También por lo general existe un entorno muy parecido al entorno de producción creado para poder realizar pruebas en él, dicho servidor se llama servidor de staging (no confundir con el área de staging de Git) o servidor de desarrollo. En este servidor hay ramas que se utilizan antes de enviar los cambios a master. Si se está trabajando en una característica de una versión probablemente se quiera hacer merge directamente en la rama de desarrollo (antes de master) pero la forma correcta de hacerlo en vez de utilizar merge es por medio de pull requests.

#### ¿Qué son pull requests?

Los pull requests son una característica de GitHub que funcionan como un estado intermedio previo a realizar el merge a la rama. Esto permite que otros miembros del equipo revisen los cambios y los aprueben antes de obtener una versión final. Esta característica en GitLab recibe el nombre de 'Merge request' y en Bitbucket como push request. Estos también son importantes porque permiten a no colaboradores apoyar con el desarrollo en un proyecto. Los pull requests generalmente son aprobados por el administrador del proyecto o con un DevOps.
