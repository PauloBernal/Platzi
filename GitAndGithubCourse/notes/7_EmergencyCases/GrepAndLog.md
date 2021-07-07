# Buscar en archivos y commits de Git con Grep y Log

## Buscando en archivos

Cuando se quiere buscar por palabra las repeticiones en archivos que esta tiene existe un commando llamado `grep`:
~~~
$ git grep "word"
~~~
Para saber las líneas en las que esta aparece se utiliza el parámetro `-n`:
~~~
$ git grep -n "word"
~~~
Para contar la cantidad de veces que una palabra aparece se usa el parámetro `-c`:
~~~
$ git grep -c "word"
~~~


## Buscando en commits

Para buscar en que commits aparece cierta palabra se puede utilizar el comando `log` con el parámetro `-S` (Search):
~~~
$ git log -S "word
~~~
