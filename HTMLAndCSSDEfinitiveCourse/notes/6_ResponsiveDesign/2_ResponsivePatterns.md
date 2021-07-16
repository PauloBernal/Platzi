# Patrones responsive

Existen distintos patrones de responsive design que ayudan a realizar de mejor forma el diseño. Entre estos están:

- Mostly Fluid
- Layout Shifter
- Columnn Drop

Para estos patrones se utiliza bastante las funcionalidades de `flex`. Al colocar una hoja de estilos por cada breakpoint se descargan en el orden que necesita de forma prioritaria el usuario en el momento.

## Mostly Fluid

Este patrón se basa en reacomodar los elementos y contenedores a medida que vaya creciendo el dispositivo.

- Small.- Usualmente el contenido está en columnas dependiendo de los contenedores
- Intermediate.- El contenido se distribuye teniendo más elementos por fila
- Large.- Llegado cierto punto el contenedor padre deja de crecer para posicionarse en medio con los demás elementos dentro.

## Layout Shifter

Este patrón se basa en modificar la disposición de distintos contenedores padre y distintos contenedores hijo. 

- Small.- Usualmente el contenido está en columnas dependiendo de los contenedores
- Intermediate.- Los elementos se posicionan dependiendo de los contenedores. El contenido no se distribuye de forma uniforme, sino que se posicionan por orden de importancia.
- Large.- Llegado cierto punto el contenedor padre deja de crecer para posicionarse en medio con los demás elementos dentro.

## Column Drop

Este patrón consiste en mover los contenedores hacia la parte de arriba del layput a medida que la ventana aumenta de tamaño.

- Small.- El contenido está dispuesto en columnas y uniformemente distribuido.
- Intermediate.- Los elementos superiores se posicionan en una sola fila a medida que el dispositivo es más grande.
- Large.- El contenido secundario se va agrupando en filas mientras que el contenido principal crece.
