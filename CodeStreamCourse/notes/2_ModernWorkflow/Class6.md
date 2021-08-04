# Tu herramienta de comunicación de código

## Principios de colaboración *Shift Left*

1. Mejor antes que después
2. Colaboración atomizada
3. **Más consulta que aprobación**
4. Reducir fricción adoministrativa
5. Compartir conocimientos

En este punto la evolución del flujo pasa a ser la Discusión informal también conocida como CodeChat utilizando Slack u otros.

## Sistema de CodeChat integrado

***Ejemplo 4*** *Pedir ayuda*

- Sin integración: 18 pasos
- con integración: 2 pasos

### Sin integración

1. Seleccionar bloque de código
2. Copiar
3. Alt-tab a Slack
4. Elegir el canal
5. Pegar texto y volver
6. Explicar el contexto
7. Dar detalles del repositorio y el proyecto
8. Teclear Path y archivo fuente
9. Copiar número de línea
10. Hacer referencia a la función
11. Encontrar a la persona correcta
12. Alt-tab a terminal
13. Cambiar al directorio correcto
14. git blame | grep
15. Alt-tab nuevamente a Slack
16. Copiar-pegar email del autor, email para mencionar
17. Escribir la pregunta (finalmente)
18. Alt-tab de vuelta al editor

### Con integración

1. Seleccionar el bloque de código
2. Hacer la pregunta

## Code Chat

- El Code Chat es mensajería de equipo diseñada para trabajar con líneas y bloques de código
- Detecta cambios y diferencias en distintas versiones del mismo bloque
- Contiene la meta-información para evolucionar con el código
- Se integra con Slack, Pull Requests, Jira
- Se transforma en documentación

### Propósito del Code Chat

- Colaboración informal atomizada
- Permite hacer preguntas y sugerencias sobre cualquier parte del código
- Conecta distintas partes del flujo
- Conecta distintos bloques de código
- Documenta el código
- Explica decisiones ya tomadas

### Code Marks

- Cada vez que se crea una unidad de comunicación en CodeStrean se crea un "CodeMark"
- Un codemark es un enlace entre la información dobre el código (metadata) y el bloque de código al que se refiere
- Un codemark puede ser un mensaje, un issue o un permalink (enlace permanente)
- Codemarks son exportables

### Sección Codemarks

- Añadir comentario
- Crear Issue
- Vista espacial
- Configuraciones
- Maximizar

#### Codemark abierto

- En el panel de CodeMark a la izquierda se puede ver la pregunta con el código al que hace referencia al igual que la respuesta. Se puede continuar la conversación cuanto se quiera para tratar un problema.

#### Spatial View

Es como ver un Google Docs, a la derecha se tiene el contenido y a la derecha el comentario que se realizó al contenido.

## CodeChat resumen

- El code chat facilita la colaboración informal
- Se integra con los sistemas de comunicación existentes
- Se adecúa a la evolución y las diferencias del código
- Se utiliza en cuqluier parte del repositorio

---

[Anterior](./FeedBackRequest.md)

[Siguiente](./PracticeII.md)

[Índice](../Intro.md)
