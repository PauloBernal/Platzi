# Especificidad en selectores

## Orden de declaración

Al declarar CSS el orden se controla de 3 formas:

1. Importancia
2. Especificidad
3. Orden de las fuentes

Si dos declaraciones tienen la misma importancia la especificidad será la que indique cuál aplicar, si dos tienen la misma especificidad se decidirá en el orden de las fuentes el resultado final.

### Importancia

EL orden de importancia carga de distinta forma los estilos dependiendo la jerarquía de estos (de menos importante a más importante):

1. Hoja de estilo de agente de usuario (estilos por defecto del navegador del usuario)
2. Declaraciones normales en hojas de estilo de autor (CSS del sitio)
3. Declaraciones importantes en hojas de estilos de autor (utilizar el `!important`)

### Especificidad

La especificidad de los selectores se refiere a la jerarquía de los mismos, es decir, para aplicar estilos a un elemento se toma en cuenta que tan específico es el selector que referencia al elemento:

| Selectores | Especificidad |
| --- | --- |
| `!important` | 1.0.0.0.0 |
| `inline styles` | 0.1.0.0.0 |
| `#id` | 0.0.1.0.0 |
| `.class` | 0.0.0.1.0 |
| `tag` | 0.0.0.0.1 |

Para verificar el orden de importancia de los estilos se puede acceder al siguiente [enlace](https://www.codecaptain.io/tools/css-specificity-calculator)

### Reglas de cascada

Las reglas de cascada es la forma en la que funciona el algoritmo de CSS. Estas se basan en un arbol de decisiones

1. Conflicto en la declaración
2. Diferente origen o `!important`
    - **SI**.- Utiliza la declaración con el origen de mayor prioridad
    - **NO**.- Siguiente paso
3. ¿Tiene algún inline style?
    - **SI**.- Utiliza las inline declarations
    - **NO**.- Siguiente paso
4. ¿Los selectores tienen una especificidad diferente?
    - **SI**.- Utiliza las declaraciones con mayor especificidad
    - **NO**.- Utiliza las declaraciones que vienen en su fuente original

### Orden de las fuentes

Esto quiere decir que los estilos que estén al final anularán los que están en la parte de arriba. Si después de modificar un elemento se cambian sus estilos más abajo estos anularán los anteriores.

***Ejemplo*** Que estilos se aplican al siguiente `span` en tema de tipo de fuente:

~~~css
span {
    font-family: Arial;
}

span {
    font-family: Verdana;
}
~~~

Como `Arial` está más arriba que `Verdana` se aplica esta última fuente al elemento.
