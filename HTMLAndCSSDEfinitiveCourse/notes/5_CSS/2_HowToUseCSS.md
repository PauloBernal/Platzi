# ¿Como utilizamos CSS?: etiqueta, selector, clase, ID

## Incluyendo estilos en HTML

Para utiizar una hoja de estilos en un archivo HTML es necesario saber la ruta en la que se encuentran los estilos. Posteriormente se utiliza esta ruta como valor del atributo `href` de una etiqueta `<link/>`, la cual va en el head del documento y especifica el tipo de archivo al igual que la ruta:

~~~html
<link rel="stylesheet" href="/route/" />
~~~

También existe una etiqueta llamada `<style>` en la cual se pueden incluir los estilos en formato CSS, sin embargo esto es una mala práctica debido a que si se incluyen demasiados estilos en el documento de HTML tardará demasiado en cargar la página (esto debido a como funciona por dentro el navegador).

~~~html
<style></style>
~~~

Como tercera opción también se pueden especificar los estilos de un elemento en específico como parte de sus atributos:

~~~html
<tag style="styles"></tag>
<tag style="styles" />
~~~

A este tipo de estilos se los denomina estilos 'embebidos' debido a que vienen incluidos en el mismo elemento. La mejor práctica al momento de incluir estilos es trabajar en un archivo aparte de extensión `*.css`

## Sintaxis CSS

Para incluir estilos en formato CSS se utiliza una sintaxis sencilla. Primero se debe hacer referencia al elemento HTML en cuestión, después se especifica las propiedades a modificar y por último el valor de dichas propiedades, todo esto dentro de llaves `{}` después del elemento. Se incluyen cuantas propiedades se desee para un mismo elemento:

~~~css
html_element {
    property1: value1;
    property2: value2;
    ...
    propertyN: valueN;
}
~~~

## Comentarios en CSS

La forma de comentar en CSS es por medio de la siguiente sintaxis:

~~~css
/* Comment */
~~~

## Aplicando estilos a un elemento

Hay diversas formas de hacer referencia a un elemento de HTML en CSS. Entre estas se encuentran por etiqueta, por selector, por clase y por ID.

### **Etiqueta**

Para hacer referencia a un elemento por etiqueta se debe colocar el nombre de la etiqueta en CSS. Esto aplicará los estilos a todos los elementos que tengan esa etiqueta:

***HTML***

~~~html
<tag></tag>
~~~

***CSS***

~~~css
tag {
    property1: value1;
    property2: value2;
    ...
    propertyN: valueN;
}
~~~

### **Clase**

Para hacer referencia a un elemento por clase es necesario colocar el atributo `class` y especificarlo con un punto en CSS. Una misma clase puede hacer referencia a varios elementos a la vez.

***HTML***

~~~html
<tag class="class_name"></tag>
~~~

***CSS***

~~~css
.class_name {
    property1: value1;
    property2: value2;
    ...
    propertyN: valueN;
}
~~~

### **ID**

Es prácticamente igual que con las clases, con la diferencia de que el ID es único para cada elemento (solo se puede hacer referencia a un elemento a la vez). Para hacer referencia a un ID en CSS se utiliza el símbolo hash (#).

***HTML***

~~~html
<tag id="identifier"></tag>
~~~

***CSS***

~~~css
#identifier {
    property1: value1;
    property2: value2;
    ...
    propertyN: valueN;
}
~~~
