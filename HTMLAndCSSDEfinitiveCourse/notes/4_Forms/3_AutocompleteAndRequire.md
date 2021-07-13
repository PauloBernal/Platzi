# Autocomplete y require

Hay más funciones que se pueden añadir a los elementos de un formulario. Entre estas están `autocomplete` y `require`.

## Autocomplete

El atributo `autocomplete` permite que el navegador realice un autocompletado a algunos campos con información que el usuario ya haya ingresado en su cuenta. Esto es util al momento de hacer la experiencia menos pesada para el usuario que debe rellenar el formulario:

~~~html
<input type="type" autocomplete="value">
~~~

Se puede elegir la forma de autocompletado con distintos valores para el atributo:

- `name`.- Nombre
- `email`.- Correo electrónico
- `username`.- Nombre de usuario
- `country`.- País
- `bday`.- Día de nacimiento
- `postal-code`.- Código postal

## Required

Este atributo indica que el input debe tener algún valor de forma obligatoria para que el formulario sea enviado. Es un atributo que no requiere valor por lo que la sintaxis va de la forma:

~~~html
<input type="type" required>
~~~
