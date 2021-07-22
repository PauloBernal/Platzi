# Variables

## Declarando variables

Como ya se explicó anteriormente las variables son espacios en memoria que almacenan valores los cuáles se pueden reutilizar posteriormente. Por buenas prácticas las variables y mixins seben ser declarados antes de cualquier otro tipo de código (al principio dle documento). Para declarar una variable en Pug se utiliza la palabra `-var` con un guión al inicio, seguido del nombre de la variable con un símbolo de igual y el valor de esta entre comillas:

~~~pug
-var var_name="value"
~~~

## Llamando variables

Para llamar una variable se coloca el símbolo de igual `=` después de la etiqueta o la clase del elemento. Se deja un espacio y a continuación se escribe el nombre de la variable. Utilizando la variable definida en el anterior subtítulo:

***Pug***

~~~pug
tag= var_name
~~~

***HTML***

~~~html
<tag>
    value
</tag>
~~~

Otra forma de llamar a la variable es con un hash (`#`), seguido de llaves entre  las que va el nombre de la variable a llamar. Esto es útil cuando el valor debe estar entre cierto contenido ya que en el caso anterior no se podía añadir contenido extra. Utilizando la variable definida anteriormente:

***Pug***

~~~pug
tag Content #{var_name} More Content
~~~

***HTML***

~~~html
<tag>
    Content value More Content
</tag>
~~~

## Arreglos

### Declaración

Los arreglos son formas de almacenar múltiples valores en una sola variable. Para declarar un arreglo en Pug se hace de la misma forma que una variable normal con la diferencia de que los múltiples valores van entre corchetes y separados por comas:

~~~pug
-var var_name = ["value1", "value2", ... , "valueN"]
~~~

### Llamada

Para llamar un valor de un arreglo se realiza de forma similar a como se llama el valor de una variable normal con la diferencia de que después del nombre de la variable se debe indicar la posición del elemento (el arreglo comienza desde la posición 0) entre corchetes.

***Pug***

~~~pug
tag #{var_name[N]}
~~~

***HTML***

~~~html
<tag>
    valueN
</tag>
~~~

### Doble posición

Si se indica una doble posición al llamar el elemento de un arreglo lo que sucede es que se devuelve la letra en dicha posición en caso de tratarse de una cadena de caracteres:

***Pug***

~~~pug
tag #{var_name[0][0]}
~~~

***HTML***

~~~html
<tag>
    v
</tag>
~~~
