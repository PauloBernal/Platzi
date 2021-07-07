# Feedback Request

## Introducción

### Feedback Requests (CodeStream)

- Es un concepto relacionado con el de un Pull Request
- Se realiza antes en el flujo para atomizar la colaboración
- Permite pedir feedback (comentarios y sugerencias acerca del código)
- Es mucho más fácil de revisar


### Principios de colaboración *Shift Left*

1. Antes mejor que después
2. Colaboración atomizada
3. Más consulta que aprobación
4. Reduce la fricción administrativa
5. Compartir conocimientos

### Evolución del flujo

Para trabajar con un Feedback Request se requiere de al menos una persona más que forme parte del flujo (entorno equipo).

## Feedback Request (FR)

### Definición

Un Feedback Request es una revisión de código ligera antes del Pull Request. Para recibir comentarios sobre cualquier cambio, incluso antes de un commit.

### Secciones

- Título.- Acerca de qué se está pidiendo un Feedback Request
- Descripción.- Especificación más detallada del Feedback Request
- Reviewers.- Se tiene la opción de elegir quienes van a ser los revisores de los cambios
- Cambios.- Se registran los cambios en los archivos para que sean revisados

Es una versión más ágil de un Pull Request mucho más eficiente

## Integración de proyectos/tareas en VSCode

### Beneficios
- Incluye funcionalidad completa
- Tres propósitos: automatización, uniformidad, comunicación
- Permite integrar más de una aplicación en la misma lista de tareas (Trello, Jira, Github Issues)

***Ejemplo 3*** *Asignar un ticket*
- Sin integración: 7 pasos
- Con integración: 2 pasos

#### Sin integración
1. Navegar hasta Atlassian y elegir Jira
2. Aplicar filtro a los tickets para encontrar el deseado
3. Mover el ticket a "In Progress"
4. Escribir código
5. Commit, push, etc.
6. Al terminar el código mover el ticket a "En revisión"
7. Cuando se termina la revisión mover el ticket a "Terminado"

#### Con integración
1. Seleccionar un ticket del editor
2. Un solo click para crear un branch, mover el ticket a "In Progress" y actualizar el estado en Slack

### Jira

- Filtros de Jira integrados en el editor
- La selección de un ticket está integrada en el editor de código y se compone de 6 secciones:

    1. Título
    2. Descripción
    3. Código y cambios
    4. Cambiar la tarjeta a la próxima etapa (Kanban)
    5. Crear un branch en el repositorio
    6. Actualización del estado en Slack

#### Ventajas de tener un Issue TRacker integrado

- Agregar ticket mientras se escribe o revisa código
- Conectar el ticket directamente al código
- Notificar a la persona indicada que hay un ticket y dirigirlo al lugar correcto
- No tener que cambiar la aplicación o contexto
- Crear un registro de los tickets asociados al código mismo
