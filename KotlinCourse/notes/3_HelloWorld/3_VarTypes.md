# Tipos de variables

En Kotlin existen múltiples tipos de variables, los cuáles se detallarán a continuación. Es importante recalcar que al asignar un valor a una variable, se pueden acceder a múltiples propiedades y funcionalidades a las que no se puede acceder con un valor ordinario. Esto es debido a que todo en Kotlin es un objeto (más adelante se explicará a detalle el tema de objetos).

## Booleano

El tipo booleano hace relación a los valores binarios `true` o `false`. Para declarar una variable de tipo booleano se utiliza la palabra `Boolean`:

~~~kotlin
var var_name: Boolean = value
~~~

## Números enteros

El tipo de número entero, como su nombre lo indica, es el tipo de valor que permite asignar a la variable números pertenecientes al conjunto de los números enteros. Para declarar una variable entera se hace uso de la palabra `Int`:

~~~kotlin
var var_name: Int = value
~~~

## Números largos

El tipo número largo permite realizar operaciones con números mucho más grandes de forma más optimizada que el tipo de valor entero. Para declarar una variable de este tipo se utiliza la palabra `Long`:

~~~kotlin
var var_name: Long = value
~~~

La segunda forma es colocar una 'L' al final del valor para que el programa sepa que se trata de un long:

~~~kotlin
var var_name = *value*L
~~~

## Números dobles

El tipo de número doble hace referencia a números decimales (como $\pi$ o $e$) o fracciones. Para declarar una variable de tipo doble se utiliza la palabra reservada `Double`:

~~~kotlin
var var_name: Double = value
~~~

## Números flotantes

El tipo de número flotante generalmente se usa para determinar porcentajes. Para declarar una variable de este tipo se utiliza la palabra `Float`:

~~~kotlin
var var_name: Float = value
~~~

La segunda forma es colocar una 'f' al final del valor para que el programa sepa que se trata de un float:

~~~kotlin
var var_name = *value*f
~~~

## Cadena de texto

El tipo cadena de texto es uno de los tipos de valores más usados en múltiples programas y aplicaciones, esto debido a que la interacción y comunicación con el usuario depende mayormente de las palabras. Para declarar una variable de tipo cadena de texto se utiliza la palabra `String` y se escribe el valor de la variable entre comillas:

~~~kotlin
var var_name: String = "value"
~~~

Es posible concatenar cadenas de texto utilizando el símbolo de suma (`+`) o la forma más recomendable es utilizando las referencias a variables en cadenas de texto o las "templates", las cuáles se realizan colocando un símbolo de dólar (`$`) seguido del nombre de la variable:

~~~kotlin
"$var_name1 ...some text... $varname_2"
~~~
