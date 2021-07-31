# Accesibilidad

El término accesibilidad se refiere a la forma en que los sitios se adaptan a personas con cierta discapacidad (ya sea visual o auditiva). Muchos utilizan lectores de pantalla para poder entender el contenido de un sitio web. Entre algunos de estos lectores de pantalla están:

- NVDA
- JAWS
- Voice Over (MAC OSX)

Dependiendo del sistema operativo se utiliza un lector u otro. Es responsabilidad de los desarrolladores utilizar una buena semántica HTML para ayudar a los lectores de pantalla a interpretar los elementos y secciones del sitio web.

## ANDI

ANDI es una herramienta que ayuda a desarrollar páginas y aplicaciones con mejor accesibilidad. Se puede obtener ANDI en el siguiente [enlace](https://www.ssa.gov/accessibility/andi/help/install.html). Para utilizar la herramienta se debe añadir a la barra de herramientas del navegador y hacer click en el texto 'ANDI'. La herrmienta muestra los errores de accesibilidad

## Mejorando la accesibilidad

### Tab index

Para hacer que el navegador lea un elemento que se considera importante a este se le coloca en HTML el atributo `tabindex` con el valor `"0"`:

~~~html
<tag tabindex="0"></tag>
~~~

Para ver más acerca de este atributo se puede consultar la documentación en el siguiente [enlace](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes/tabindex)

### Aria label

Cuando no se quiere dañar el diseño pero se quiere tener un respaldo en tema de accesibilidad al tratarse de inputs sin un `label` se puede utilizar un atributo llamado `aria-label`, el cuál permite colocar el texto corresponidente a un label en el elemento mismo:

~~~html
<input aria-label="text" ...>
~~~
