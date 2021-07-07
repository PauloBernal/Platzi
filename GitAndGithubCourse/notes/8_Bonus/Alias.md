# Comandos y recursos colaborativos en Git y GitHub

También existen alias en Git y pueden ser útiles para manejar comandos largos con utilidad. aquí se listan unos cuantos:

## Stats

Este comando listará la cantidad commits (sin merge) que realizó cada colaborador del proyecto. Como base se usa el comando `git shortlog` que muestra un log por persona de los commits realizados. Los parámetros `-sn` para acortar y solamente mostrar el número de commits por persona, el parámetro `--all` para mostrar todos los commits y el parámetro `--no-merge` para ignorar los merges realizados. Para crear un alias de git con estas características se debe ejecutar:
~~~
$ git config --global alias.stats "shortlog -sn --all --no-merges"
~~~


## iblame

Este comando mostrará los cambios realizados por cada persona de una forma mejor identada que `blame`. Como base se utilizará el comando `git blame`, el cuál muestra que hizo cada persona en un archivo. Usando el parámetro `-c` se identa de mejor forma el output por lo que para crear el alias se debe ejecutar:
~~~
$ git config --global alias.iblame "blame -c"
~~~
Para especificar un rango de líneas se utiliza la sintaxis: `-LN1,N2`, donde N1 y N2 son la línea inicial y la línea final.


## Ramas remotas

Para listar las ramas que se tiene en el repositorio local y en el repositorio remoto se utiliza el comando `git branch` con el parámetro `-a`, para listar solamente las ramas remotas se utiliza el parámetro `-r`.


## Estadísticas en GitHub

Para ver la cantidad de pulls, cambios, commits, etc. existe una pestaña en GitHub llamada 'Insights', la cuál muestra estadísticas del repositorio y también para los contribuidores. Para ver contribuidores existe una sección llamada Contribuitors, para commits también existe una sección.
