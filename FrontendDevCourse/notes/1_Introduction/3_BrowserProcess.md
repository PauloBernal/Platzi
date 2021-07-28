# Proceso de renderizado de la web

## Estructuras

### DOM

El navegador por defecto no entiende directamente el código HTML. Para poder renderizar las páginas web existe algo llamado DOM (Document Object Model) que es la forma en que el navegador interpreta todos los elementos como un conjunto de objetos entendibles por el mismo.

### CSSOM

Es parecido al DOM, solamente que en este caso crea un mapa de objetos a los cuales se les asigna los estilos CSS.

### Render Tree

Es el proceso en el cual se juntan el DOM y el CSSOM para mostrar en pantalla los elementos con sus resepctivos estilos.

## Procesos

### Proceso de HTML para llegar al DOM

Lo primero que hace el navegador es transformar todo el código a bytes, después convierte los bytes a caracteres dependiendo de la codificación (la más popular es UTF-8 por el soporte que tiene para caracteres internacionales). Luego convierte los caracteres a tokens, una forma de estructurar y organizar los elementos separando el contenido en sus respectivas etiquetas. Posteriormente convierte los tokens en nodos (objetos) que se dividen en estructura y contenido. Finalmente viene el DOM, un árbol de los nodos vistos anteriormente.

- Bytes
- Caracteres
- Tokens
- Nodos
- DOM

### Proceso de CSS para llegar al CSSOM

Dependiendo del DOM enlaza los estilos después de realizar el mismo procedimiento. A cada elemento se le asignan los respectivos estilos dependiendo de los selectores.

### Resumen de pasos que realiza el navegador

1. Procesa HTML y construye el DOM
2. Procesa CSS y construye el CSSOM
3. DOM + CSSOM = Render Tree
4. Ejecuta el diseño en el Render Tree
5. Pinta el nodo en la pantalla
