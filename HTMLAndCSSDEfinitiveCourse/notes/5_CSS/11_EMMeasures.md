# Medidas EM/REM

## Medida EM

Un `em` es una medida relativa al tamaño de fuente del elemento padre. Por ejemplo si el elemento padre tiene un `font-size` de `16px` y el hijo tiene un tamaño de fuente de `2em` esto será proporcional al tamaño de fuente del elemento padre, es decir, el tamaño de fuente del elemento hijo será `32px` (1em = 16px).

***HTML***

~~~html
<parent>
  <child></child>
</parent>
~~~

***CSS***

~~~css
parent {
  font-size: 16px;
}

child {
  font-size: 2em;
}

/*child font-size = 2em = 2(16px) = 32px*/
~~~

Por defecto el `<body>` no tiene un tamaño de fuente predeterminado, este se ubica en la etiqueta `<html>`. Hay que tener cuidado al usar `em` en elementos anidados debido a que el `em` cambia dependiendo del tamaño de fuente del elemento padre (si un elemento que contiene a otro tiene el tamaño de fuente en `em`, esta pasará a ser la nueva medida relativa)

***HTML***

~~~html
<parent>
  <child1>
    <child2></child2>
  </child1>
</parent>
~~~

***CSS***

~~~css
parent {
  font-size: 16px;
}

child1 {
  font-size: 2em;
}

child2 {
  font-size: 1.5em
}

/*child1 font-size = 2em = 2(16px) = 32px*/
/*child2 font-size = 1.5em = 1.5(32px) = 48px*/
~~~

## Medida REM

Esta medida relativa es muy parecida al `em`, sin embargo en este caso el tamaño de fuente no cambia en función del `font-size` del elemento padre, sino que cambia en función del tamaño establecido en el elemento raíz (etiqueta `<html>`) que generalmente es de `16px`. Se puede modificar el tamaño de fuente de `<html>` para mejorar el manejo de `rem` y que esta medida equivalga a `10px`

~~~css
html {
  font-size: 62.5%;
}
~~~

Al obtener el 62.5% de 16px se tiene que ahora un `rem` equivale a `10px`, lo que permite un manejo más rápido de esta medida relativa. Como toma la medida del `rem` del elemento raíz, en este caso no hay el problema de anidar elementos como había con `em`.
