# Listas de selección múltiple

## Select

A veces se quiere crear un formulario con un campo de selección múltiple y valores predefinidos. Para esto existe una etiqueta llamada `select`.

~~~html
<select></select>
~~~

Para colocar las opciones predeterminadas se utiliza la etiqueta `option` dentro de `select`. Con el atributo `value` se establece el valor que será enviado a la base de datos y el contenido de la etiqueta indica el texto que tendrá la opción al momento de desplegarse la lista múltiple:

~~~html
<select>
    <option value="option1"> Option1 </option>
    <option value="option2"> Option2 </option>
    ...
    <option value="optionN"> OptionN</option>
</select>
~~~

## Input list

Cuando hay demasiadas opciones puede llegar a ser molestoso para el usuario tener que buscar una por una para elegir. Como solución a esto hay otra forma de colocar estas listas pero con la diferencia de que estas permiten al usuario ingresar las primeras letras por teclado para facilitar la búsqueda. Para crear este tipo de listas se utiliza la etiqueta `<input/>` con el atributo `list` en el cuál como valor se coloca el id de la `datalist` que contiene las opciones. Esto se hace más o menos:

~~~html
<input list="datalist_id" />
<datalist id="datalist_id">
    <option value="option1"></option>
    <option value="option2"></option>
    ...
    <option value="optionN"></option>
</datalist>
~~~

En este caso no hay texto en la parte del contenido porque al momento de renderizar solamente se muestra el texto que se encuentra en el valor.
