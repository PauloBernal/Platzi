# **Operadores de control**

## Concepto
Son simbolos reservados por la terminal que permiten ejecutar mas de un comando a la vez. Se pueden correr de forma síncrona, asíncrona o de forma condicional


## Ejecución síncrona 
La ejecución síncrona se refiere a eventos que ocurren uno detrás de otro (de forma sucesiva). Para ejecutar comandos de forma síncrona se usa el operador **'\;' (punto y coma)** entre los comandos a ejecutar. Se usa la siguiente sintaxis:
~~~
$ cmd1 ; cmd2 ; cmd3 ; ... ; cmdn
~~~
Se ejecuta primero el comando 1, después el comando 2 y así sucesivamente.


## Ejecución asíncrona
La ejecución asíncrona se refiere a eventos que no se dan de forma sucesiva. Estos se ejecutan a la par en segundo plano por lo que también se podría denominar una ejecución en paralelo. El stdout se muestra en pantalla conforme al tiempo de finalización de los procesos. Para ejecutar múltiples comandos asíncronamente se hace uso de la sintaxis:
~~~
$ cmd1 & cmd2 & cmd3 & ... & cmdn
~~~
Los comandos desde 1 hasta n se ejecutan en paralelo y llega una salida estándar al usuario conforme estos terminan.


## Ejecución condicional
La ejecución condicional se da con dos partes, un comando que hace de condición y un comando que se ejecuta si se cumple esa condición o no.
Para esto existen dos operadores:

### Operador **AND (&&)**
Los comandos se ejecutan de forma síncrona y un comando se ejecuta solamente si el anterior se ejecutó correctamente. La sintaxis es:
~~~
$ cmd_condition && cmd_answer
~~~
Caso contrario todo el proceso se rompe donde el comando dio error.

### Operador **OR (||)**
Los comandos se ejecutan de forma síncrona y un comando se ejecuta sin importar si el anterior se ejecutó correctamente o no. La sintaxis es:
~~~
$ cmd_condition && cmd_answer
~~~
Hay que tener cuidado con el operador "OR" ya que a veces ocurre que el proceso es interrumpido y no se ejecutan todos los comandos.


## Comandos útiles
- `cal` (calendar).- Este comando muestra en la terminal un calendario señalando la fecha actual.
~~~
$ cal
~~~
- `date` .- Este comando muestra información acerca del día y la hora actuales.
~~~
$ date
~~~


---

[Anterior](../FirstSteps/Wildcards.md)

[Siguiente](./EnvironmentVariables.md)

[Índice del curso](../Index.md)
