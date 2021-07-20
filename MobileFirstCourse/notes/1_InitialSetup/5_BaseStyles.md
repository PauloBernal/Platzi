# Estilos base

Los estilos base son estilos que resetean los estilos que el navegador coloca por defecto, configuraciones para hacer más fácil el proyecto y algunas variables a utilizar.

## Reseteando y configurando

Para resetear los estilos que vienen por defecto en el navegador, configurar el `box-sizing` para facilitar el manejo de tamaños con el modelo de caja y configurar el `font-size` por defecto para optimizar el uso de `rem` como medida se puede utilizar:

~~~css
* {
    box-sizing: 0;
    margin: 0;
    padding: 0;
}

html {
    font-size: 62.5%;
}
~~~

Como convención al momento de generar estilos se puede seguir el siguiente orden:

1. Posicionamiento
2. Modelo de caja
3. Tipografía
4. Visuales
5. Otros

## Variables

Al momento de trabajar con proyectos grandes las variables ayudan a ser más organizado y no confundirse con los estilos, teniendo fuentes, colores, tamaños, y otros valores almacenados en estas variables. Todas estas se almacenan en el elemento `root`:

~~~css
:root {
    --var_name1: value1;
    --var_name2: value2;
    ...
    --var_nameN: valueN;
}
~~~
