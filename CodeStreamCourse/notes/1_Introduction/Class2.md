# El editor de texto moderno

## El editor de texto como Eje (Hub)

- Se usa en todo el desarrollo el editor de texto
- Se utilizan otras herramientas que no forman parte del editor (GitHub, JIRA, Slack, Email, etc)
- Cambios de contexto o entorno de trabajo reducen la productividad

Se pueden implementar en el editor de texto moderno tres herramientas importantes en el flujo de trabajo para aumentar la productividad:

- GitHub
- JIRA
- Slack

Así se evita el problema de el cambio de contexto al momento de trabajar. La idea esencial aquí es mejorar la productividad al momento de trabajar eliminando pasos innecesarios y manteniendo un mismo entorno de trabajo.

## Integración de herramientas

Sin integración una sola tarea puede requerir de más pasos para ser llevada a cabo, mientras que con integración esto se puede disminuir bastante

***Ejemplo 1*** *Flujo integrado*

- Sin integración: 20 pasos
- Con integración: 6 pasos

### Sin integración

1. Escribir código
2. Alt-tab a terminal
3. `git status`
4. Verificar los cambios por archivo en el editor
5. `git diff`
6. `git branch -b feature/new-branch`
7. Alt-tab a Chrome
8. Encontrar la lengüeta en JIRA
9. Ir a la lista de Issues
10. Encontrar el issue en cuestión
11. Copiar
12. `git commit -am "Commit message #JIRA Ticket"`
13. `git pull`
14. `git push`
15. Copiar el url de la terminal
16. Alt-tab a Chrome, pegar
17. Crear un título para le PR y una descripción, RETURN
18. Agregar un revisor al PR
19. Alt-tab a Slack
20. @mention al revisor para avisar que se está esperando

### Con integración

1. Hacer click en el ticket para generar una rama y empezar a trabajar
2. Escribir el código
3. Realizar revisión, agregar commmit a cada archivo en el panel SCM del editor
4. Sincronizar cambios con GitHub
5. Hacer click en New Pull Request (el título y descripción se crean automáticamente con referencia al ticket de JIRA)
6. Agregar revisor al PR

***Ejemplo 2*** *GitHub (Revisor)*

- Sin integración: 14 pasos
- Con integración: 4 pasos

### Sin integrar

1. Recibir notificación
2. Click para cargar PR e github.com
3. Examinar el review, darse cuenta que se tiene que mirar el código en contexto para entender los cambios
4. Copiar el nombre de la rama
5. Alt-tab a terminal, encontrar el directorio donde está el repositorio
6. `git fetch`
7. `git checkout branch-name`
8. `git pull`
9. Alt-tab al editor, donde se puede ver el código
10. Alt-tab de vuelta a github.com, navegar hasta el archivo que se quiere comentar
11. Alternar de ida y vuelta entre el editor y github.com
12. Terminar la revisión
13. Alt-tab a Slack
14. @mention al autor para avisarle que se finalizó con la revisión

### Integrando

1. Recibir notificación en el editor
2. Click para hacer un pull y checkout a la rama
3. Realizar la revisión de código en contexto y comentar en cualquier parte sin restricciones
4. Terminar la revisión

## Beneficios de la integración de las herramientas en el editor

- Se ahorra tiempo
- Se reducen distracciones
- Se tiene acceso al código en todo momento
- Se mejora la calidad
- Se mejora la comunicación
- No se debe cambiar de herramientas ni de contexto

## Evolución del flujo

### El camino hacia Shift Left

- Pull Request (personal)
- Feedback Request (equipo)
- Discusión informal (equipo)
- Documentación (organización)

---

[Anterior](Class1.md)

[Siguiente](./PracticeI.md)

[Índice](../Intro.md)
