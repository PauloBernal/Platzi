# Autocomplete y require

Hay más funciones que se pueden añadir a los elementos de un formulario. Entre estas están `autocomplete` y `require`. 

## Autocomplete

El atributo `autocomplete` permite que el navegador realice un autocompletado a algunos campos con información que el usuario ya haya ingresado en su cuenta. Esto es util al momento de hacer la experiencia menos pesada para el usuario que debe rellenar el formulario:
~~~
<input type="type" autocomplete="value">
~~~

Se puede elegir la forma de autocompletado con distintos valores para el atributo:
- `name`.- Nombre
- `email`.- Correo electrónico
- `username`.- Nombre de usuario
- `country`.- País
- `bday`.- Día de nacimiento
- `postal-code`.- Código postal
