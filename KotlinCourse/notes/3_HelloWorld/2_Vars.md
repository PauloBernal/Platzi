# Variables

Las variables son un factor imprescindible al momento de desarrollar software, debido a que permiten almacenar información en memoria. Las variables son referencias en memoria que almacenan datos e información del programa para no tener que repetirlos constantemente.

## Creando variables en Kotlin

### Variables de lectura y escritura

Para declarar una variable de lectura y escritura en Kotlin se debe colocar la palabra reservada `var`, seguida del nombre de la variable, con dos puntos se indica el tipo de dato de la variable y para asignarle un valor se utiliza el símbolo de igualdad seguido del valor de la variable.

~~~kotlin
var var_name: type = value
~~~

si más adelante en el código se quiere cambiar el valor de la variable se utiliza el nombre de la variable seguido del operador de asignación (`=`), seguido del nuevo valor de la variable.

~~~kotlin
var_name = new_value
~~~

### Variables de solo lectura

Las variables de solo lectura, son valores almacenados en una variable los cuales una vez asignados ya no pueden ser modificados. Para crear una variable de este tipo se utiliza la palabra reservada `var`, seguida del operador de asignación y el valor.

~~~kotlin
val var_name = value
~~~

### Constantes

Son similares a las variables de solo lectura, con la diferencia de que estas se generan al momento de compilación (mientras se crea el programa) mientras que las anteriores variables se generan al momento de ejecución (mientras se ejecuta el programa). Para crear una constante se debe colocar antes de la función `main()` la palabra reservada `const`, seguida de la palabra reservada `val`, seguida del nombre de la variable, el operador de asignación y el valor de la constante.

~~~kotlin
const val var_name = value
fun main(args: Array<String>) {
  ...
}
~~~
