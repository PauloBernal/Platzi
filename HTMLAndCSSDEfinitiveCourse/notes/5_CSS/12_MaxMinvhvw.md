# Más medidas relativas

## View measures

Como medidas relativas también se pueden usar `vw` (view width) y `vh` (view height). Estos representan las dimensiones en relación a la ventana del navegador, es decir, cambian en función del cambio de tamaño en la ventana. Se suelen utilizar para asignar tamaños a contenedores padre aparte de ser muy usadas en 'Responsive Design' tomando en cuenta que se puede reescalar la ventana del navegador o puede haber un cambio de dispositivos. Para ocupar el 100% de la ventana se puede usar:

~~~css
element {
  width: 100vw;
  height: 100vh;
}
~~~

## Min/max

Cuando se utilizan medidas relativas de base es probable que se quiera limitar el crecimiento de un elemento. Para esto se pueden utilizar valores máximos y mínimos (en medidas absolutas) en el alto y el ancho del elemento. Existen cuatro propiedades en CSS que permiten añadir valores máximos y mínimos:

- `min-width` (anchura mínima)
- `max-width` (anchura máxima)
- `min-height` (altura mínima)
- `max-height` (altura máxima)

Estos valores máximos y mínimos generalmente se colocan en pixeles (`px`).
