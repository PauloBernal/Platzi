# Más sobre selectores

Para dar prioridad a un estilo en específico se coloca `!important` después del valor de la propiedad. Se sigue la siguiente sintaxis:

~~~css
element {
  property: value !important;
}
~~~

Son malas prácticas en CSS:

- Utilizar id para estilos
- Utilizar `!important`
- Utilizar estilos embebidos en etiquetas HTML

Son buenas prácticas:

- Utilizar clases para estilos
- Utilizar otros selectores (por ejemplo selectores anidados)
- Hacer buen uso de la especificidad
