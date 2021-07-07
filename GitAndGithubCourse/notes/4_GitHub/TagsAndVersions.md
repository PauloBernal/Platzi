# Tags y versiones en Git y GitHub

## Creando Tags

Los tags son etiquietas que especifican cambios o versiones hechos en un proecto. Estos son útiles más que todo en GitHub ya que la interfaz permite ver de mejor manera las etiquetas que se colocan en el historial de cambios.

### Viendo el historial del repositorio

Para ver la historia de un repositorio de forma resumida y mostrar las ramas de donde proceden los commits se puede utilizar el comando:
~~~
$ git log --all --graph -- decorate --oneline
~~~
Como es un comando largo es recomendable utilizar alias de Linux para hacer referencia a él.

### Colocando Tags

Una vez que se tiene el historial resumido del repositorio es posible copiar el hash del commit al cuál se quiere agregar la etiqueta y colocar el comando:
~~~
$ git tag -a tag_name -m "message" commit_hash
~~~
Los parámetros representan:

- `-a`.- Se está añadiendo una etiquieta
- `-m`.- Mensaje que acompaña a la etiqueta

Por lo que una vez hecho esto ya se tiene añadida una etiqueta de Git en el commit especificado con el hash.

### Visualizando tags

Para ver una lista de tags se puede hacer uso del comando:
~~~
$ git tag
~~~
Para ver los tags junto a los hash de los commit a los que pertenecen se puede utilizar otro comando:
~~~
$ git show-ref --tags
~~~
Para visualizar tags en GitHub hay que enviarlas primero con el comando:
~~~
$ git push remote_repo_name --tags
~~~
Una vez se enviaron en la interfaz de GitHub se puede ver una sección que dice 'Release' en la cuál está 'Tags' (etiquetas).

### Borrando tags

Para remover un tag que fue añadido por error o que simplemente ya no se quiere se hace uso del comando:
~~~
$ git tag -d tag_name
~~~
Como es una forma de manipular versiones al hacer push no se borran directamente en GitHub. Para realizar esto se utiliza el comando:
~~~
$ git push remote_repo_name :refs/tags/tag_name
~~~
