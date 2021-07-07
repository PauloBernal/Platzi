# Fusión de ramas con Git merge

## Como funciona la fusión entre ramas

Un error muy común al iniciar trabajando con ramas es creer que al fusionar dos ramas distintas se crea una tercera rama, lo cuál no es así. Lo que sucede al fusionar dos ramas es que los cambios realizados en una de ellas pasan a la otra mientras la cabecera cambia de posición y se centra en la rama final (resultado de traer los cambios de la otra rama). Al fusionar dos ramas hay dos posibles resultados, o la rama en la que se estaba trabajando desaparece o s eantiene para seguir trabajando de forma independiente en ella.


## Fusionando ramas

Al fusionar ramas se juntan los cambios del último commit de cada rama. Para fusionar ramas se utiliza el comando `merge` seguido del nombre de la rama de la cual se quiere traer los cambios. Es importante saber en que rama se está ya que de esto depende donde termine la fusión de ambas.
~~~
$ git merge branch_name
~~~
Un merge es un commit, por lo que al momento de hacer un merge lo más probable es que se abra un editor de texto como Vim y pida introducir un mensaje para realizar dicho commit.


## Entendiendo el log de un merge

Al fusionar ambas ramas se crea un commit que indica la unión de ols cambios. Al colocar el comando `log`:
~~~
$ git log
~~~
Se puede ver este commit indicando de dónde provienen los cambios en `Merge` con los primeros 7 caracteres de los últimos commit de cada rama de las cuáles se obtuvieron los cambios.

## Borrando ramas

Una vez fusionada una rama es probable que no se la vuelva a utilizar y se la quiera borrar. Para borrar una rama es tan simple como usar el comando `branch`  con el parámetro `-d` (delete). 
~~~
$ git branch -d branch_name
~~~

## Comandos útiles

-`merge`.- Este comando permite fusionar dos ramas combinando los últimos commits registrados. Para esto se debe estar posicionado en la rama en la que se quiere fusionar y colocar el nombre de la rama que se quiere fusionar
~~~
$ git merge branch_name
~~~
