# Valores nulos, double bang y soluciones

Los null no son de por sí malos para un programa, como toda herramienta pueden ser bien o mal utilizados, dependiendo del programador. Kotlin incluye los tipos de dato nullables, que son aquellos tipos de dato que pueden tener como valor un `null`.

## Declarando variables nullables

Para declarar un tipo de dato nullable se realiza la declaración de la variable de forma usual con la diferencia de que al final del tipo de dato que se especifica se añade un signo de interrogación:

~~~kotlin
var var_name: Type? = *value*
~~~

## Tips

- Es importante saber reconocer las advertencias del compilador ya que nos permite interpretar estos tipos y nos advierte de las fallas que pueden haber al momento de ejecutar el programa. Por lo tanto, no siempre lo mejor es utilizar una solución rápida a uno de estos errores, sino saber utilizar las herramientas del lenguaje para sacar provecho a los recursos del mismo.
- Se debe crear código pensando en personas, no en máquinas. Esto quiere decir que el código debe ser legible, y así lo dejemos durante un periodo largo podríamos retomar el desarrollo sin problemas, comprendiendo todo.
- Dejar el código mejor que como uno lo encontró

## Safe calls y double bang

Las safe calls son una herramienta del lenguaje que ayudan a ejecutar código cuando una variable del tipo nullable no es nula. para utilizar un safe-call se coloca un signo de interrogación después del nombre de la variable al momento de llamarla:

~~~kotlin
var_name?
~~~

Por otro lado el double bang es un operador que le dice al compilador que en ese punto la variable no puede ser nula. Para utilizar un double bang s coloca dos signos de exclamación después del nombre de la variable al momento de llamarla:

~~~kotlin
var_name!!
~~~

Esto no es recomendable debido a que es considerado una mala práctica. No está bien usarlo siempre para que el código compile.

## Null y la inteoperabilidad con Java

Debido a que en Java no existe el tipo nullable, Kotlin no puede determinar con certeza al momento de usar una variable creada en java si esta es nullable o no nullable, por lo que el tipo de la variable aparece con un signo de exclamación al final: `var_name!`. Por recomendación se debe tratar estas variables como nullables.
