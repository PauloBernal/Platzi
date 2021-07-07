# Introducción a las ramas de Git

## ¿Qué son y como funcionan las ramas?

Las ramas son una forma de realizar cambios sin afectar el eje del proyecto. Esto es importante debido a que cuando se quiere corregir un problema casi siempre se debe hacer aparte, por si se llega a romper algo en el proceso. La rama principal se llama `master` por defecto, y en esta está el historial de commits realizados hasta el momento. Al último commit se lo denomina cabecera del proyecto o `HEAD`. al crear una rama lo que ocurre es que se crea una copia del último commit, mientras en esta rama se trabaje de forma independiente no afectará a la rama `master`. Una vez se tienen listos los cambios se puede fusionar ambas ramas para obtener una nueva completa.

## Trabajando con ramas

### Creando ramas

Para crear una rama en Git se utiliza el comando `branch` seguido del nombre de la rama a crear
~~~
$ git branch branch_name
~~~

### Viajando entre ramas

Para cambiar de una rama a otra se utiliza el comando `checkout` seguido del nombre de la rama a la cual se quiere cambiar
~~~
$ git checkout branch_name
~~~


## Comandos útiles

- `branch`.- Permite visualizar las ramas disponibles si no se coloca ningún parámetro y crear una nueva rama si se coloca un nombre después del comando
~~~
$ git branch
~~~
~~~
$ git branch branch_name
~~~
- `checkout`.- Este comando permite cambiar de una rama de trabajo a otra
~~~
$ git checkout branch_name
~~~
