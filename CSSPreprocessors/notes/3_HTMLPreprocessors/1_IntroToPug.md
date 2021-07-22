# Introducción a Pug

Pug es un preprocesador de HTML que ayuda con distintas funcionalidades al momento de estructurar los archivos.

## Sintaxis

### Etiquetas

Para declarar una etiqueta en Pug solamente es necesario colocar el nombre de la etiqueta, si se requiere de algún atributo se especifica estos entre paréntesis y con un espacio se define el contenido de la etiqueta

***Pug***

~~~pug
tagname(property="value") content
~~~

***HTML***

~~~html
<tagname property="value">
    content
</tagname>
~~~

Para definir etiquetas anidadas se utiliza la identación:

***Pug***

~~~pug
parent 'Parent Content'
    child 'Child Content'
~~~

***HTML***

~~~html
<parent>
    'Parent Content'
    <child>
        'Child Content'
    </child>
</parent>
~~~

Con la identación hay que tener cuidado ya que solamente se puede utilizar una de las dos opciones (no dos a la vez), Tab o espacios.

### Inicializando el documento

La estructura básica en un documento HTML es:

~~~html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF_8" />
    </head>
    <body>
    </body>
</html>
~~~

Lo que en Pug se escribe:

~~~pug
doctype html
html
    head
        meta(charset="UTF-8")
    body
~~~

Y como se puede ver es más fácil y comprensible en Pug

## Clases

Para definir clases en Pug se coloca el nombre de la etiqueta, después un punto y finalmente el nombre de la clase:

***Pug***

~~~pug
tag.classname
~~~

***HTML***

~~~html
<tag class="classname"></tag>
~~~
