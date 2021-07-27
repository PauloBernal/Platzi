# Tips

## Bootstrap Reboot

Es un archivo de CSS que ayuda a agilizar el reseteo de los estilos. Es útil debido a que la configuración general de reseteo ya viene en el archivo, no es necesario resetear de forma manual.

## Modularización de secciones en PUG

Hay partes de la estructura en HTML que pueden llegar a repetirse en otros archivos de HTML (tales como el header o el footer) que se pueden colocar en una plantilla y reutilizar cuando se necesite. Para generar estas plantillas se crea un archivo que contenga los elementos fijos y que con un `block` defina contenido variable que será integrado dependiendo del archivo.
