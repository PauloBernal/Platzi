# Medidas

En CSS los tipos de medidas se pueden dividir en 2:

- Relativas
- Absolutas

## Absolutas

Las medidas absolutas son aquellas que no varían con el tamaño del dispositivo o del elemento padre (son constantes). Como medidas absolutas se tiene:

- Pixeles (`px`)
- Centímetros (`cm`)
- Pulgadas (`in`)
- Milímetros (`mm`) = 1/10 `cm`
- Puntos (`pt`) = 1/72 `in`
- Picas (`pc`) = 12 `pt`

## Relativas

Son aquellas que cambian el tamaño del elemento de forma proporcional al cambio del tamaño de la ventana (o de un elemento padre). Algunas medidas relativas son:

- Porcentaje (`%`) respecto al elemento padre
- Altura de la ventana o 'viewport height' (`vh`)
- Ancho de la ventana o 'viewport width' (`vw`)
- Element `em` (unidad relativa al `font-size` del elemento padre)
- Root element `rem` (unidad relatva al `font-size` del elemento raíz)
- Min/Max width
- Min/Max height

Se denomina overflow cuando el contenido sobrepasa el tamaño de la pantalla, generando un scroll de forma horizontal.
