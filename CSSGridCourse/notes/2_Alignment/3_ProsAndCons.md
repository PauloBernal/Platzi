# Pros y contras de las técnicas de alineamiento previas a Grid

No existía ninguna propiedad para alinear elementos, por lo que todos los vistos anteriormente son trucos de alineación. Debido a esto por mucho tiempo las personas evitaron trabajar con CSS, creyendo que sigue siendo igual de complicado y rebuscado.

## Ventajas y desventajas

### Margin

- Ventaja.- El valor `auto` alinea horizontalmente cualquier elemento con cualquier ancho.
- Desventaja.- Alinear verticalmente debido a que deben calcularse estos valores.

### Line height

- Ventaja.- Se puede lograr una correcta alineación
- Desventaja.- Si el texto ocupa más de una línea, el elemento toma un alto más grande que lo necesario para los cálculos.

### Table Cell

- Ventaja.- La alineación vertical no está condicionada por fuentes, tamaños de fuentes o alturas de línea.
- Desventaja.- `vertical-align` solamente se aplica a elementos en línea.

## Limitantes

La mayor limitante de dichas propiedades es que son propiedades físicas (`margin-top`, `padding-bottom`, `border-left`, `right`). Se debe traducir esto a propiedades lógicas, algo que va muy ligado a los modos de escritura (por ejemplo en Japón leen de derecha a izquierda) y con lo que el sitio se puede romper si se trabaja con propiedades físicas.
