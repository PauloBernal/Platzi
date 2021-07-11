# Index y su estructura básica: head

AL momento de crear el primer archivo html de un sitio web es importante que este reciba el nombre de `index.html` ya que es la página inicial que el servidor busca al momento de desplegar un sitio web. En caso de no existir un `index.html` se debe especificar al servidor el nombre de la página inicial del sitio web.

## Creando un archivo HTML

### Iniciando

Al momento de crear un archivo de HTML se debe especificar en la parte de arriba que se trata de un archivo de HTML 5 con la línea:
~~~
<!DOCTYPE html>
~~~
Es importante esto ya que el archivo le especifica al navegador que debe mostrar el sitio con HTML 5 y no sus versiones previas.

Después se debe crear el contenedor principal de la página, esto se crea haciendo uso de la etiqueta:
~~~
<html></html>
~~~
Dentro de esta van los otros contenedores necesarios para que el sitio funcione. Esta etiqueta lleva un atributo especial que se llama `lang`
, en el cuál se especifica el idioma del sitio web por medio de su código ISO 639. Esto ayuda al navegador a identificar en que idioma está el sitio web para poder traducirlo al idioma del usuario.
~~~
<html lang="language"></html>
~~~
Valores para lang:
- en.- Inglés
- es.- Español
- fr.- Francés

Para más valores se puede acceder al siguiente enlace de [códigos ISO 639](https://omegat.sourceforge.io/manual-standard/es/appendix.languages.html)


## Etiquetas principales

Las etiquetas principales en una página web son `<head></head>` y `<body></body>`, los cuales son contenedores hermanos. Al momento de colocarlas deben estar bien identadas (por buenas prácticas, para entender mejor la estructura del documento HTML), es decir, se debe dejar un espacio antes de la etiqueta para indicar que está dentro de otra etiqueta:
~~~
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
    </body>
</html>
~~~

## Head

Aquí va todo lo que es importante para cargar la página pero no es visible para el usuario. Entre el contenido que esta lleva en su interior puede haber estilos en CSS, scripts de JS, coniguración de caracteres, configuración de media queries, dependencias, fuentes, etc.
~~~
<head></head>
~~~
viendo una analogía se podría decir que el `head es el cerebro del documento`

### Etiqueta `<meta/>`

Son etiquetas que le dan cierta información al navegador para que sepa como manejar el proyecto. Las etiquetas meta se cierran a sí mismas por lo que toda la información se coloca en forma de parámetros de la etiqueta.
~~~
<meta atributo="valor" />
~~~
Entre los atributos que esta etiqueta puede llevar están:
- `charset`.- Este indica el estándar de caracteres que utilizará el sitio web. El más utilizado por su soporte para caracteres especiales es 'UTF-8', debido a que permite el uso de tíldes, el uso de la letra 'ñ' y otos caracteres más. Sin embargo tambiá hay otros como 'UTF-16' o 'ISO' que permiten o lomitan el manejo de algunos caracteres:
~~~
<meta charset="UTF-8" />
~~~

- `name`.- Ayuda a configurar la página en distintos aspectos como descripción del sitio y otros que ayudan a posicionar el sitio en los buscadores. Este atributo va acompañado del atributo `content`.
- `content`-. En este atributo va el contenido que se despliega en la propiedad cuyo nombre se estableció con `name`:
~~~
<meta name="property_name" content="property_content" />
~~~
Entre las más comunes están:
~~~
<meta name="description" content="This is the description of the webiste" />
~~~
La cuál ayuda a posicionar el sitio en los buscadores a base del contenido de la descripción del sitio.
~~~
<meta name="robots" content="index,follow" />
~~~
Esta permite que los robots de Google u otros buscadores ayuden a posicionar el sitio si se coloca `follow` o se les quita el permiso de acceso si se coloca `unfollow`.
~~~
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
~~~
Esta permite configurar la página para funcionar de forma responsive y adaptarse al ancho del dispositivo del usuario. Suele ir después de la etiqueta `title`.

### Etiqueta `<title></title>`

Al ingresar a una página en la parte superior de la pestaña aparece un título dependiendo del sitio, este título se establece haciendo uso de esta etiqueta:
~~~
<title>Title</title>
~~~

### Etiqueta `<link/>`

Esta etiqueta se utiliza para añadir estilos o un ícono del sitio. Por lo general tiene dos atributos:
- `rel`- Este indica de qué tipo es el contenido al que se está accediendo (como afecta al sitio web)
- `href`.- Este indica la ruta, ya sea de los estilos o de la imagen
~~~
<link rel="file_type" href="/route/" />
~~~

## Ejemplo

La estructura de head debe ir más o menos de la siguiente forma:
~~~
<head>
    <meta charset="UTF-8" />
    <meta name="description" content="This is a description" />
    <meta name="robots" content="index,follow" />
    <title>Title</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="/route/" />
</head>
~~~

Como un atajo para la mayoría de estas etiquetas VSCode permite iniciar un documento de HTML 5 escribiendo `html:5` al iniciar el documeto.