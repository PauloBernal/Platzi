# Ciclos

## Ciclo `for`

Este ciclo permite ejecutar un código para cada elemento de una lista (estructura de datos que se verá más adelante). Como se itera entre los elementos hay una variable temporal que se inicializa en el mismo ciclo. Para crear un ciclo de este tipo se hace uso de la palabra reservada `for`, seguida de la variable de iteración, la palabra reservada `in` y el nombre de la lista entre paréntesis. Por último las instrucciones a realizar por cada iteración entre llaves:

~~~kotlin
for (it_var in list_name) {
  ...
}
~~~

## `for` simplificado

Al igual que con el condicional `if`, el ciclo for permite escribir el código en una sola línea si se tiene una sola instrucción. Esto se hace utilizando la misma estructura que antes con la diferencia de que en este caso no se encierra la instrucción entre llaves:

~~~kotlin
for (it_var in list_name) *instruction*
~~~

## Ciclo `forEach`

El `forEach` es una función de extensión o método de una lista que se utiliza de igual forma para iterar los elementos de la misma. Para utilizar el ciclo `forEach` se coloca el nombre de la lista seguido del método `forEach`, seguida de unas llaves en las que se declara la variable de iteración y con una flecha se asigna una instrucción para cada iteración:

~~~kotlin
list_name.forEach {it_var -> *instructions*}
~~~

La función declarada entre llaves se denomina función anónima y se explicará más sobre esta a lo largo del curso.

## Iteración con `map`

El método o función de extensión `map` permite iterar entre los elementos de una lista devolviendo otra lista con el resultado de cada iteración. esto es útil si se quiere iterar entre todos los elementos de la lista una operación en específico y obtener una lista con los resultados. para utilizar la función map se declara una nueva variable con su respectivo nombre, y luego del operador de asignación se coloca el nombre de la lista a operar con el método `map` y entre llaves la variable de la iteración seguida de una flecha que indica las instrucciones:

~~~kotlin
var mapped_list = list_name.map {it_var -> *instructions*}
~~~

## Iteración con `filter`

Esta función permite crear una nueva lista a partir de un filtro condicional en una lista previa. En otras palabras, permite crear una nueva lista filtrando datos de otra lista. Para filtrar datos con el método `filter` se realiza de forma similar a `map`, con la diferencia de que en vez del método `map` se usa el método `filter` y no son instrucciones que se colocan en la función anónima, sino condiciones:

~~~kotlin
var filtered_list = list_name.filter {it_var -> *filter condition*}
~~~
