# Excepciones

Muchas veces al programar existen errores que no se pueden evitar, simplemente ocurren como parte de la ejecución. Cuando se quiere manejar estos errores para que no rompan el flujo del programa y por el contrario son parte del mismo se utilizan las excepciones las cuales son formas de ejecutar cierto código cuando ocurre un error.

## Manejando excepciones con `try`, `catch` y `finally`

Para controlar el flujo del programa con las excepciones se utiliza la palabra reservada `try` seguida de la instrucción que contiene o puede contener el error entre llaves. Luego de esto viene la palabra reservada `catch`, con el nombre de la excepción seguido de dos puntos, el tipo de error a evitar y las instrucciones en caso de que el error ocurra entre llaves:

~~~kotlin
try {
  ...
}
catch (exception_var: TypeOfError) {
  ...
}
~~~

Si se quiere ejecutar un bloque de código en caso de que ocurra o no ocurra un error (siempre se ejecuta), se utiliza `finally`. Para esto se escribe la palabra reservada `finally` seguida de las instrucciones entre llaves:

~~~kotlin
try {
  ...
}
catch (exception_var: TypeOfError) {
  ...
}
finally {
  ...
}
~~~

si se quiere capturar cualquier tipo de error, como tipo de error se coloca el tipo general `Exception`:

~~~kotlin
try {
  ...
}
catch (exception_var: Exception) {
  ...
}
finally {
  ...
}
~~~

## Lanzando excepciones

Nosotros como programadores también podemos lanzar excepciones en caso de que ocurra un error. Esto es potencialmente útil al momento de crear librerías para otros programadores ya que nos permite lanzar las excepciones en caso de un error. Para lanzar una excepción se utiliza la palabra reservada `throw` seguida del tipo de error a lanzar y entre paréntesis un mensaje que acompañe a la excepción:

~~~kotlin
throw TypeOfError("message")
~~~
