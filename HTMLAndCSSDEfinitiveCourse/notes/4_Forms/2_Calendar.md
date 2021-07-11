# Calendar

Cuando se busca que el usuario brinde información específica de fechas, meses o años se puede utilizar un calendario. Existen dos formas de realizar un calendario en HTML, una más sencilla que otra.

## Comentando en HTML

Un comentario es un bloque de texto que no se renderiza como parte de la estructura del documento, sino que se considera apartado de este. Para comentar en HTML se utiliza la siguiente sintaxis:
~~~
<!-- Comentario -->
~~~
En VSCode existe una combinaciónde teclas que comenta un bloque seleccionado. Para comentar se utiliza la combinación  '`Ctrl + }`'

## Primer método

Primero se debe tener la estructura básica de un formulario:
~~~
<form action="url">
    <label for="id1"></label>
    <label for="id2"></label>
    ...
    <label for="idN"></label>
</form>
~~~

Se puede especificar el tipo de dato que se pedirá al usuario con los siguientes tipos de input (en el atributo `type`):

- `time`.- Sirve para pedir un dato de tipo hora al usuario
~~~
<input type="time">
~~~
- `date`.- Sirve para que el usuario introduzca una fecha específica
~~~
<input type="date">
~~~
- `week`.- Sirve para que el usuario introduzca una semana específica del año
~~~
<input type="week">
~~~
- `month`.- Sirve para que el usuario intrduzca un mes en específico
~~~
<input type="month">
~~~


## Segundo método

Para hacer un calendario con un método más sencillo:

Primero se debe tener la estructura básica de un formulario:
~~~
<form action="url">
    <label for="id"></label>
</form>
~~~
Dentro del `label` se debe colocar un input con la siguiente estructura:
~~~
<input type="datetime-local">
~~~
Esto hace referencia a la hora y fecha locales. Con este input se puede seleccionar en una entrada la fecha y la hora. Para enviar información por medio de un formulario se utiliza el tipo de input `submit`:
~~~
<input type"submit" >
~~~
Para ver una lista de los tipos de input en HTML se puede acceder al siguiente [enlace](https://developer.mozilla.org/es/docs/Web/HTML/Element/input)