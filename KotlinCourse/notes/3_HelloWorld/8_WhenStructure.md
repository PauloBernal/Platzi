# Estructuras de control: `when`

En el caso de que en una variable se quieran evaluar múltiples condiciones se puede utilizar la estructura de control `when`.

## Estructura `when` en Kotlin

Como se indicó antes, la estructura `when` permite evaluar múltiples condiciones a partir de una variable, tal y como lo hace la estructura `switch` en lenguajes como Javascript o C++. Para utilizar esta estructura se escribe la palabra reservada `switch`, seguida del nombre de la variable a evaluar entre paréntesis y entre llaves las condiciones con las instrucciones. es importante tomar en cuenta que la condición se relaciona con la instrucción por medio de flechas de la forma `->`. Las condiciones son el valor que tiene la variable:

~~~kotlin
when (var_name) {
  *value1* -> *instruction1*
  *value2* -> *instruction2*
  ...
  *valueN* -> *instructionN*
}
~~~

En la estructura `when` también existe el `else` en caso de que no se cumpla la igualdad con ninguno de los valores. Este se coloca al final con la palabra reservada `else` seguida de la flecha y la instrucción a ejecutar:

~~~kotlin
when (var_name) {
  *value1* -> *instruction1*
  *value2* -> *instruction2*
  ...
  *valueN* -> *instructionN*
  else -> *elseInstruction*
}
~~~

Si se quiere evaluar más de un valor, oero con una misma condición, se pueden utilizar comas para separar ambos valores:

~~~kotlin
when (var_name) {
  *value1*, *value2*, ..., *valueN* -> *instruction1*
}
~~~

## Rangos e `in` en Kotlin

En Kotlin es posible ver si un número está en un rango determinado. Para esto se utiliza la palabra reservada `in`, seguida del valor mínimo del rango, dos puntos consecutivos y el valor máximo del rango:

~~~kotlin
in *min*..*max*
~~~

La expresión `in` también se puede utilizar para verificar si una variable se encuentra en una lista o conjunto (más adelante se verá a fondo estos conceptos).

## `when` como asignación de variable

Al igual que con el `if`, la estructura `when` se puede utilizar para asignar valores a una variable. Para esto se escribe el nombre de la variable seguido del operador de asignación y la estructura `when`, que en lugar de instrucciones tiene los valores a asignar a la nueva variable:

~~~kotlin
var_name1 = when (var_name2) {
  *value1* -> *val1*
  *value2* -> *val2*
  ...
  *valueN* -> *valN*
  else -> *elseVal*
}
~~~

Es importante que si se está asignando un valor a una variable por medio de estructuras se cubran todas las posibilidades, en otras palabras, es recomendable que haya un `else` al momento de usar `if` o `when` para asignar valores a una variable.
