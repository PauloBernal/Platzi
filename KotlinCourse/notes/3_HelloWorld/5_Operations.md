# Operaciones entre datos

Es importante entender que en Kotlin las operaciones son traducidas a funciones internamente al ser compiladas. Esto debido a que los datos se tratan como objetos y las operaciones se pueden expresar en forma de funciones. A continuación se muestra una tabla con las equivalencias entre expresiones simbólicas, funciones y funciones de operadores:

| Expresión | Función | Operator fun |
|---|---|---|
|a + b|c = a + b|public operator fun plus(other: Int): Int|
|a - b|c = a - b|public operator fun minus(other: Int): Int|
|a * b|c = a * b|public operator fun times(other: Int): Int|
|a / b|c = a / b|public operator fun div(other: Int): Int|
|a % b|c = a % b|public operator fun rem(other: Int): Int|
|a++|c = a++|public operator fun inc(): Int|
|a-|c = a-|public operator fun dec(): Int|
|a > b|c = a > b|public override operator fun compareTo(other: Int): Int|
|a < b|c = a < b|public override operator fun compareTo(other: Int): Int|
|a >= b|c = a >= b|public override operator fun compareTo(other: Int): Int|
|a <= b|c = a <= b|public override operator fun compareTo(other: Int): Int|
|a != b|c = a != b|public open operator fun equals(other: Any?): Boolean|

Estas operaciones generalmente están restringidas a cierto tipo de datos, a menos que se creen funciones equivalentes para los demás tipos de datos.
