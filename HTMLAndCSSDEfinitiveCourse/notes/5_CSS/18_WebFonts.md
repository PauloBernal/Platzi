# Fonts

## Fuentes genéricas

Son fuentes que vienen instaladas por defecto en el ordenador o en el navegador. Estas fuentes son:

- serif (Times New Roman, Georgia)
- sans-serif (Helvética, Verdana)
- cursive (Dancing Script, Good Vibes)
- monospace (Courier New, Roboto Mono)

La forma de ver las fuentes que vienen por defecto es entrar a Configuración del navegador, sección de diseño, Personalizar Fuentes. Ahí se puede modificar las fuentes por defecto en el navegador.

## Fuentes Web

Existen fuentes en particular que se puede encontrar en internet en sitios como 'Google Fonts', un sitio web de fuentes abierto. En estos sitios hay dos formas de obtener las fuentes, descargadas o embebidas. Se puede incluir la fuente directamente con un link directo con un `@import` de CSS:

~~~css
@import url(*url*)
~~~

Sin embargo los `@import` no son muy buenas prácticas en tema de fuentes. Para ello existe una alternativa que es incluir la fuente en el `<head>` del documento HTML. Para esto se utiliza la etiqueta `<link>`:

~~~html
<link href="*url*" rel="stylesheet" />
~~~

Estos url vienen con un `display=swap` al final, lo cual quiere decir que el proyecto cargue con la fuente por defecto del navegador y una vez que esté listo incluya la fuente externa.

En el sitio web hay una opción que indica como llamar la fuente en CSS con `font-family`

~~~css
element {
    font-family: *font_name*;
}
~~~

Como buenas prácticas al trabajar con fuentes están:

- Solamente cargar una fuente por proyecto (máximo 2)
- Importarlas siempre en la etiqueta `<head>`
