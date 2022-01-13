# Estruturas de control: `if`

Las estructuras de control son herramientas que nos permiten determinar el flujo del código, usualmente por medio de condiciones. La estructura de control `if`, permite determinar si un determinado bloque de código se ejecuta a partir de una condición.

## `if`, `else` y `else if` en Kotlin

Para crear una estructura condicional `if` en Kotlin se coloca la palabra reservada `if`, seguida de la condición entre paréntesis y el código a ejecutarse entre llaves:

~~~kotlin
if (*condition*) {
  ...
}
~~~

Si se quiere añadir condiciones aparte se puede utilizar la palabra reservada `else if`, seguida de la nueva condición entre paréntesis y las instrucciones entre llaves:

~~~kotlin
if (*condition1*) {
  ...
}
else if(*condition2*) {
  ...
}
else if(*condition3*) {
  ...
}
...
~~~

En el caso de que no se cumpla ninguna condición y se quiere ejecutar otro bloque de código se utiliza la palabra `else` después de lo anterior, seguida de las instrucciones entre llaves:

~~~kotlin
if (*condition1*) {
  ...
}
else if(*condition2*) {
  ...
}
...
else {
  ...
}
~~~

## `if` simplificado

Kotlin permite escribir el condicional `if` sin necesidad de utilizar las llaves y en una sola línea (si es que solamente hay una instrucción). Para esto se escribe la palabra `if` seguida de la condición entre paréntesis seguida de un espacio y el código a ejecutar si la condición es verdadera. Si se quiere añadir una instrucción en caso de que la condición no se cumpla se coloca un espacio seguido de la palabra `else` seguida de la instrucción a ejecutar:

~~~kotlin
if (*condition*) *instruction1* else *instruction2*
~~~

## `if` como asignación de variable

Si se quiere asignar un valor a una variable dependiendo de una condición específica se puede utilizar el `if` en la asignación de la variable. Para esto se escribe el nombre de la variable seguido del operador de asignación, seguido de la estructura `if` con los valores a asignarse dependiendo de la condición:

~~~kotlin
var_name = if (*condition*) {
  *value1*
}
else {
  *value2*
}
~~~

Es posible realizar la asignación junto a la declaración.
