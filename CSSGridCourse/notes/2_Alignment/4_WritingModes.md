# Modos de escritura y ejes de alineamiento

## Modos de escritura en CSS

Como se mencionó anteriormente, existen diversos modos de escritura dependiendo de la cultura. Por ejemplo:

- De izquierda a derecha.- Latín
- De derecha a izquierda.- Árabe
- Bidireccional.- Latín + Árabe
- Vertical.- Carácteres asiáticos

Debido a esto surgió una propiedad en CSS denominada `writing-mode`, la cuál puede tener uno de los siguientes valores:

- `horizontal-tb`.- Horizontal con flujo de arriba a abajo.
- `vertical-lr`.- Vertical con flujo de izquierda a derecha.
- `vertical-rl`.- Vertical con flujo de derecha a izquierda.
- `sideways-rl`.- Vertical de arriba a abajo con los glifos de lado hacia la derecha.
- `sideways-rl`.- Vertical de arriba a abajo con los glifos de lado hacia la izquierda.

Esta propiedad no se debe utilizar con tablas.

## Alineación y flujo del texto

Se debe tomar en cuenta tres aspectos:

1. Modo de escritura (`writing-mode`)
2. Dirección dle flujo de los elementos (`display`, `flex-direction`)
3. Orientación del texto ()

## Flex

Es otra propiedad útil para controlar el modo de escritura modificando en este caso la disposición de los elementos. En flex la propiedad es `flex-direction` y tiene los siguientes valores:

- `row`.- elementos en línea que van de izquierda a derecha
- `column`.- Elementos en columna que van de arriba a abajo
- `row-reverse`.- Elementos en línea que van de derecha a izquierda
- `column-reverse`.- elementos en columna que van de abajo a arriba

Para controlar la posición de dichos elementos también se hace uso de la propiedad `justify-content` con sus valores `flex-end` y `flex-start`

## Grid

En grid la cosa es distinta debido a que los elementos se posicionan en filas y columnas especificadas. Estas se modifican con las propiedades:

- `grid-column-start`
- `grid-column-end`
- `grid-row-start`
- `grid-row-end`
