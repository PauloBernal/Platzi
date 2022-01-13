# Elvis Operator

Este operador nos permite asignar valores a variables que provienen de otras de tipo nullable pero no deberían devolver `null`. Por ejemplo cuando se quiere obtener la longitud de una cadena de caracteres pero en vez de un string la variable tiene como valor `null`. Para esto se utiliza una safe call, seguido del método o propiedad de la variable, seguido del Elvis operator (llamado así por la semejanza con el artista norteamericano) el cuál está compuesto de un signo de interrogación y dos puntos (`?:`). Luego de esto se coloca el valor a asignar en caso de que el valor por defecto sea `null`:

~~~kotlin
var_name?.property ?: *value* 
~~~
