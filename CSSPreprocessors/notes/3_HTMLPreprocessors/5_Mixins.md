# Mixins

Los mixins son similares a las variables pero mucho más potentes debido a que permiten generar porciones de código enteras y no solo valores.

## Declarando mixins

Al igual que con las variables se recomienda crear estos mixins al inicio del documento para no generar conflictos. Para crear un mixin se utiliza la palabra reservada `mixin` seguida del nombre del mixin. Se utiliza un salto de línea e identación para colocar el bloque de elementos que formarán parte del mixin:

~~~pug
mixin mixin_name
    *elements*
~~~

**Ejemplo** Se quiere crear una página para visualizar fotos y se desea almacenar en un mixin el formato con un `figure` de clase `picture-container`, un título con `h3` de clase `picture-title` y una imagen adentro (sin ruta por el momento) de clase `picture`. Dicho mixin debe llamarse `picture`

~~~pug
mixin picture
    figure.picture-container
        h3.picture-title Título
        img.picture(src="#" alt="")
~~~

## Llamando mixins

Para llamar un mixin en una parte específica del documento se utiliza el símbolo más (`+`) seguido del nombre del mixin.

~~~pug
+mixin_name
~~~

**Ejemplo** Utilizando el ejemplo anterior se quiere colocar tres fotografías dentro de un contenedor `section` de clase `pictures`

***Pug***

~~~pug
section.pictures
    +picture
    +picture
    +picture
~~~

***HTML***

~~~html
<section class="pictures">
    <figure class="picture-container">
        <img src="#" alt="" />
    </figure>
    <figure class="picture-container">
        <img src="#" alt="" />
    </figure>
    <figure class="picture-container">
        <img src="#" alt="" />
    </figure>
</section>
~~~

## Argumentos en mixins

Cuando existe contenido que cambia dentro del mixin se pueden colocar argumentos o partes variables dentro del mixin que se definen con paréntesis y nombres de variables provisionales. al mandar a llamar estos mixins también se debe definir con paréntesis los valores de las variables provisionales:

~~~pug
mixin mixin_name(var1, var2, ... , varN)

-mixin_name(value1, value2, ... , value3)
~~~

**Ejemplo** Utilizando el ejemplo de la galería se tiene una carpeta llamada `img` en la que se encuentran las imágenes. Como título tendrán la palabra `Imagen` y el número de imagen, al igual que el texto alternativo. Los respectivos nombres de las imágenes son `img1.png`, `img2.png` e `img3.png`:

***Pug***

~~~pug
mixin picture(route, title)
    figure.picture-container
        h3.picture-title Imagen #{title}
        img.picture(src=route alt="Imagen "+title)

section.pictures
    +picture("./img/img1.png", "1")
    +picture("./img/img2.png", "2")
    +picture("./img/img3.png", "3")
~~~

***HTML***

~~~html
<section class="pictures">
    <figure class="picture-container">
        <h3>Imagen 1</h3>
        <img src="./img/img1.png" alt="Imagen 1" />
    </figure>
    <figure class="picture-container">
        <h3>Imagen 2</h3>
        <img src="./img/img2.png" alt="Imagen 2" />
    </figure>
    <figure class="picture-container">
        <h3>Imagen 3</h3>
        <img src="./img/img3.png" alt="Imagen 3" />
    </figure>
</section>
~~~
