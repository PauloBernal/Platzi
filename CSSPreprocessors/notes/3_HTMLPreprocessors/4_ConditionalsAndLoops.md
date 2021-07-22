# Condicionales y ciclos

## Ciclos

Un ciclo es una porción de código que se ejecuta un cierto número de veces hasta que se cumpla una condición. Esto en HTML ayuda cuando se tiene múltiples elementos que se repiten en tema de estructura o contenido. Para crear un ciclo en Pug se utiliza la palabra clave `each` seguida del nombre de una variable temporal, después la palabra `in` y finalmente el nombre de un arreglo creado anteriormente. En la parte de abajo con identación se coloca el nombre de la etiqueta que será contenedor del nuevo elemento y el contenido con la variable que se reservó anteriormente:

~~~pug
-var array = ["value1", "value2", ... , "valueN"]

each value in array
    tag #{value}
~~~

***HTML***

~~~html
<tag>value1</tag>
<tag>value2</tag>
...
<tag>valueN</tag>
~~~

## Condicionales

Los condicionales son formas de ejecutar cierto código dependiendo de si se cumple o no una condición en específico. Esto es útil al momento de definir si se quiere colocar un elemento HTML o no, dependiendo de alguna condición. Para realizar condicionales en Pug se utiliza la palabra reservada `if` seguida de la condición a validar, por ejemplo la existencia de una variable. Despúes de eso en la parte de abajo con identación se coloca la instrucción a cumplir en caso de que la condición sea verdadera. Si se quiere que en caso contrario se ejecute otro blque de código se coloca la palabra reservada `else` con identación a la misma altura que el `if` y en la parte de abajo con identación se coloca el bloque a ejecutarse si no se cumple la condición:

***Pug***

~~~pug
if *condition*
    *instructions*

//- optional

else
    *instructions*
~~~

**Ejemplo** Se quiere verificar si un usuario está autenticado o no con una variable llamada `user`, si no hay un usuario registrado se quiere mostrar un botón de registro y si el usuario está registrado se quiere mostrar un texto que diga *"Hola `nombre`"*. En este caso el usuario está registrado y su nombre es *Mateo*.

***Pug***

~~~pug
-var user = "Mateo"

if user
    p Hola #{user}
else
    a(href="#") Registrarse
~~~

***HTML***

~~~html
<p>
    Hola Mateo
</p>
~~~
