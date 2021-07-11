# Etiqueta form e input

Los formularios permiten interacción básica con el usuario. En muchos casos los formularios son un problema debido a que si no ofrecen una buena experiencia o se hacen tediosos para el usuario este dejará la página.

> "El mejor formulario es cuando no lo hay" — Usuario anónimo


## Etiquetas de formularios

### Etiqueta `<form>`

Es una etiqueta contenedora y la indica al navegador que lo que va dentro de ella es un formulario.
~~~
<form></form>
~~~
Esta suele ir acompañada del atributo `action` que indica la url de la base de datos a la cuál se enviarán los datos del formulario. 

### Etiqueta `<label>`

Es una etiqueta que hace referencia a otras etiquetas cuando se hace click sobre ella. Para colocarla se utiliza el atributo `for` y como valor la id de la etiqueta a la que hace referencia
~~~
<label for="id"></label>
~~~

### Etiqueta `<input>`

Esta etiqueta permite que el usuario ingrese datos, ya sea texto, contraseñas, email, etc. Se utiliza dentro de un `<form>`. En el atributo `type` se especifica el tipo de input:
~~~
<input type="type" />
~~~

La estructura general de un formulario vendrá dada por:

~~~
<form action="url">
    <label for="input_id">
        <input id="input_id" type="type" />
    </label>
</form>
~~~

El atributo `placeholder` se utiliza para colocar un texto de ejemplo dentro del input:
~~~
<input type="type" placeholder="example_text" />
~~~


## Tipos de input

- `text`.- Es un tipo de input que admite solamente texto
- `date`.- Permite introducir fechas como datos
- `password`.- Se usa para introducir contraseñas de forma segura
- `time`.- Se utiliza para introducir horas, minutos, segundos
- `email`.- Este input verifica por si mismo si el contenido se trata de un correo electrónico
