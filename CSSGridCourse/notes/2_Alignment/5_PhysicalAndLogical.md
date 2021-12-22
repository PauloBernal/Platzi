# Propiedades físicas y lógicas en CSS

Existen dos modelos de caja, uno físico y uno lógico. Durante muchos años se utilizó el modelo de caja físico, siendo que el nuevo modelo de caja tiene sus equivalentes:

| Modelo Físico | Modelo lógico |
| --- | --- |
| width | inline-size |
| height | block-size |
| top | inset-block-start |
| bottom | inset-block-end |
| left | inset-inline-start |
| right | inset-inline-end |
| *-top | *-block-start |
| *-bottom | *-block-end |
| *-left | *-inline-start |
| *-right | *-inline-end |

El tema de modos de escritura va muy ligado xon accesibilidad, por lo qeu una página utilizando estas propiedades resulta mucho más accesible en otras partes del mundo.
