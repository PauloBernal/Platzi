# Input type submit vs Button

Hay dos tipos de botones en HTML para enviar formularios. Estos tipos son input type submit y la etiqueta button:

~~~html
<input type="submit" />
~~~

~~~html
<button></button>
~~~

## Button

Esta es una etiqueta cerrada debido a que se puede cambiar el texto que está dentro del botón. También se puede cambiar el tipo de botón ya que puede enviar el formulario, resetear la información dentro de este, etc. Para usar `<button>` no es necesario estar dentro de un formulario debido a que es más flexible en cuanto a estilos, manejo, etc:

~~~html
<button type="type"> Text </button>
~~~

## Input type submit

Este tipo de botón se utiliza mayormente para enviar formularios. También es menos flexible que el botón de etiqueta por lo que no se suele modificar mucho (para cambiar el taxto del botón es necesario cambiar el valor del input):

~~~html
<input type="submit" value="Text" />
~~~
