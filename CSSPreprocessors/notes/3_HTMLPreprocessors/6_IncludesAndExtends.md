# Includes y Extends

Una de las mejores cosas de Pug es poder fragmentar el código en múltiples componentes y separarlos en diversos archivos para trabajar de mejor forma con un código modulado. Es importante determinar que partes son fijas en el documento para realizar esta modulación ya que en muchos casos se puede llegar a romper la estructura del documento si se trabaja con secciones variables.

## Includes

Para incluir componentes que están en archivos externos se utiliza la palabra reservada `include` seguida de la ruta relativa del archivo:

~~~pug
include /route/
~~~

## Extends

En caso de querer añadir contenido de un elemento hijo después de haber especificado el elemento padre se utiliza la palabra reservada `block` con un nombre cualquiera de contenido posterior. Al llamar la anterior plantilla se realiza con la palabra reservada `extend` en vez de `include` y el contenido que debe ir dentro se especifica con el mismo nombre de bloque que se utilizó en el componente externo:

***Componente***

~~~pug
*content*
    block more_content
~~~

***Documento principal***

~~~pug
extend /route/
block more_content
    *more content*
~~~

**Ejemplo** Se quiere tener como componente un `div` de clase `container` con un `h2` cuyo texto es "Component" y de clase `title` que dentro tenga elementos que se especifican en el documento principal (un párrafo con un texto "Lorem") y se definen con un bloque de nombre "content":

***Componente (Pug)***

~~~pug
.container
    h2.title Component
    block content
~~~

***Documento principal (Pug)***

~~~pug
extend ./component.pug
block content
    p Lorem ipsum dolor sit amet
~~~

***HTML***

~~~html
<div class="container">
    <h2 class="title">Component</h2>
    <p>Lorem ipsum dolor sit amet</p>
</div>
~~~
