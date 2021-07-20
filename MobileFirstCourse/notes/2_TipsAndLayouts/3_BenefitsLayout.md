# Sección de beneficios

## Posiciones absolutas respecto a un elemento padre

Para posicionar un elemento respecto a los bordes de su contenedor padre se pueden alterar las posiciones del contenedor padre y el contenedor hijo. en este caso el contenedor padre deberá tener una posición `relative` y el elemento hijo deberá tener una posición `absolute`:

~~~html
<parent>
    <child></child>
</parent>
~~~

~~~css
parent {
    position: relative;
}

child {
    position: absolute;
}
~~~

Haciendo esto se podrá utilizar las propiedades de `top`, `bottom`, `left` y `right` en el elemento hijo respecto a los bordes del elemento padre.
