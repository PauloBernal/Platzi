# Funciones de las etiquetas HTML más importantes

## Elementos principales

| Etiqueta | Descripción |
| --- | --- |
| `<!DOCTYPE html>` | Aquí definimos que el documento está bajo el estándar HTML 5 |
| `<html lang="en"></html>` | Representa la raíz del documento. Todos los demás elementos son descendientes de este. |
| `<head></head>` | Aquí se encuentran los metadatos (que se escriben en la etiqueta vacía `<meta>`) del documento, incluyendo también enlaces de scripts, estilos, tipografías, etc. |
| `<meta>` | Define los metadatos del documento como la codificación de caracteres (UTF-8) |
| `<title></title` | Aquí se define el título del documento que se muestra en la pestaña de la página |
| `<body></body>` | Representa todo el contenido principal y debe ser única en el documento |

## Elementos vacíos

| Etiqueta | Descripción |
| --- | --- |
| `<img>` | Se utiliza para añadir imágenes y normalmente va acompañada de los atributos `src` que indica la ruta de la imagen y `alt`, un texto alternativo que puede usarse como una descripción de la imagen (por ejemplo con personas que padecen alguna discapacidad visual) |
| `<input>` | Es un campo donde el usuario puede ingresar datos. Se utiliza como parte de formularios o algún área que requiera que el usuario introduzca información |
| `<br>` | Esta etiqueta simplemente permite realizar un salto de línea en un texto |
| `<hr>` | Es parecida a `<br>` pero en este caso coloca una línea de separación entre párrafos u otros elementos |

## Etiquetas semánticas

| Etiqueta | Descripción |
| --- | --- |
| `<header></header>` | Esta etiqueta se utiliza para definir la cabecera de la página donde usualmente va el logo, título, barra de navegación, etc. |
| `<nav></nav>` | En esta etiqueta se suele colocar enlaces de navegación. |
| `<article></article>` | Se utiliza para definir contenido que puede vivir independiente del resto del contenido. |
| `<section></section>` | En esta etiqueta se coloca el contenido de las secciones de la página. |
| `<aside></aside>` | Es contenido secundario (como un banner de publicidad), es decir, contenido que si se elimina no afecta al resto. |
| `<footer></footer>` | Es la parte final de la página donde se suele colocar información de contacto, políticas de privacidad, etc. |
| `<h1></h1>, <h2></h2>, <h3></h3>, <h4></h4>, <h5></h5>, <h6></h6>` | Se utilizan estas etiquetas para definir títulos en la página por orden de importancia, 1 el más importante y 6 el menos importante. |

## Etiquetas comunes

| Etiqueta | Descripción |
| --- | --- |
| `<div></div>` | Es un contenedor genérico de HTML. |
| `<button></button>` | Se utiliza para crear botones y generalmente se acompaña del evento 'onclick' y un script que define una acción a realizar cuando ocurra el evento. |
| `<p></p>` | Esta etiqueta se utiliza para escribir párrafos. |
| `<a></a>` | Esta etiqueta se utiliza para colocar enlaces con el atributo `href` especificando la ruta. |
| `<ol></ol>` | Se utiliza para definir listas ordenadas o ennumeradas. |
| `<ul></ul>` | Se utiliza para definir listas desordenadas. |
| `<li></li>` | Se utiliza para definir elementos de una lista. suele ir dentro de un `<ol>` o un `<ul>`. |
| `<form></form>` | Se utiliza para crear formularios y se puede ver más acerca de esta etiqueta en el siguiente [enlace](https://www.w3schools.com/tags/tag_form.asp) |
