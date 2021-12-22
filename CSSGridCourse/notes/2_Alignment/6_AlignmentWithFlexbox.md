# Técnicas de alineamiento con flexbox

## Alineamiento

Flexbox es otra de las características que mejoraron bastante la forma de trabajar con CSS. Esto debido a la facilidad de alineación junto a nuevas propiedades que trae. Para alinear elementos con flex se utilizan tres propiedades en el contenedor padre:

- `display: flex`
- `justify-content`
- `align-items`

### `justify-content`

Como posibles valores de esta propiedad de alineamiento horizontal están:

- `flex-start`.- Alinea los elementos al inicio del contenedor
- `flex-end`.- Alinea los elementos al final del contenedor
- `center`.- Centra los elementos horizontalmente
- `space-between`.- Distribuye el espacio del contenedor entre los elementos
- `space-around`.- Distribuye los elementos dejando un espacio entre los bordes laterales del contendor mayor al espacio entre elementos
- `space-evenly`.- Distribuye el espacio dejando un espacio igual entre los bordes laterales el contenedor y los elementos.

### `align-items`

Como posibles valores de esta propiedad de alineamiento vertical están:

- `flex-start`.- Alinea los elementos al inicio del contenedor
- `flex-end`.- Alinea los elementos al final del contenedor
- `center`.- Centra los elementos verticalmente
- `stretch`.- Hace que los elementos tengan la misma altura que el contenedor
- `baseline`.- Alinea los elementos de acuerdo a la línea base del texto dentro de estos
