# Bucles: `while` y `do while`

Un bucle es una iteración de un bloque de código que se repite hasta que cierta condición se cumpla o deje de cumplirse.

## Bucle `while`

El bucle `while` es un bucle que ejecuta un bloque de código mientras se cumpla una condición, cuando esta condición ya no se cumple el bucle se rompe. Para crear un bucle `while` en Kotlin, se utiliza la palabra reservada `while`, seguida de la condición de ejecución entre paréntesis y el bloque de código entre llaves:

~~~kotlin
while (*condition*) {
  ...
}
~~~

## Bucle `do while`

La diferencia de este con el bucle `while`, es que antes de verificar la condición del bucle ejecuta la instrucción una primera vez. Esto puede ser útil sobretodo si en el mismo bucle se inicializa alguna variable utilizada en la condición. Para generar este bucle se utiliza la palabra reservada `do`, seguida de las instrucciones a ejecutar entre llaves y después de eso la palabra reservada `while` seguida de la condición del bucle entre paréntesis:

~~~kotlin
do {
  ...
} while (*condition*)
~~~
