# Modificadores y tipos de datos

Los tipos de dato son el tipo del valor que se le asigna a una variable, ya sea booleano, cadena de texto, entero, etc. Estos tipos de dato se denominan primitivos debido a que son los tipos de datos que vienen con el lenguaje de programación. A partir de datos primitivos se puede crear otros tipos de datos, denominados objetos. Un objeto es una combinación de tipos de datos primitivos, funciones y otros objetos. Anteriormente se mencionó que en Kotlin todo es un objeto, esto debido a que los tipos de datos "primitivos" tienen sus métodos y propiedades, tal como un objeto.

## Ventajas de tratar los datos como objetos

Que todo en Kotlin se un objeto trae algunas ventajas consigo, como ser:

- La posibilidad de crear funciones específicas que se apliquen con ese objeto, las cuales se denominan "métodos".
- Poder sobreescribir operadores como la suma, para permitir que se operen dos objetos del mismo tipo.
- Extender el lenguaje para crear nuevas funciones qie permitan al equipo evitar repetir código y mantener una base de código saludable.

Hay algunas reglas que el código debe seguir para poderse compilar y tener la retrocompatibilidad con Java. Una de estas reglas es que un entero que puede ser nulo no se convierte a tipo primitivo, pero un entero no nulo sí lo hace.
