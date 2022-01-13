# `Hello World` con Kotlin

## Carpetas

Es importante saber las carpetas que componen nuestro proyecto en Kotlin:

- Las carpetas que comienzan con un punto (`.gradle` y `.idea`) guardan información del proyecto.
- El `gradle` es un programa que permite gestionar las dependencias del proyecto y compilar el mismo.
- La carpeta `build` es una carpeta en la que se encuentra el código previamente compilado por gradle.
- En la carpeta `src` es la carpeta más importante del proyecto debido a que aquí se ubica nuestro código.
- La carpeta `main` se ubica dentro de la carpeta `src`, y en esta se ubica el archivo principal del proyecto.
- La carpeta `test` también se ubica en `src`, y en esta están las pruebas necesarias para ejecutar y mejorar el rendimiento de la aplicación.

## Archivos

En el caso de archivos, también es necesario entender que papel desempeñan en el proyecto:

- El más importante de ellos es el archivo principal, también denominado `main.kt` o `Main.kt` por su traducción al inglés. Este archivo es el punto de partida del proyecto y en el que se escribe la rama principal del código del programa.
- Otro archivo importante es `build.gradle.kts`, debido a que almacena la configuración del proyecto, las dependencias, versión de Kotlin, etc.
- El archivo `gradle.properties` permite declarar propiedades para el proyecto.
- El archivo `gradlew.bat` sirve para diferentes plataformas o sistemas operativos.
- El archivo `settings.gradle.kts` almacena configuraciones del proyecto como ser el nombre, versión, etc.

## Archivo `Main.kt` y primeras líneas de código

La parte más importante del proyecto es la función `main`, debido a que sin ella el proyecto no se ejecuta. Esta tiene la siguiente estructura:

~~~kotlin
fun main(args: Array<String>) {
  println("Hello World!")
}
~~~

Más adelante en el curso se hablará más acerca de las funciones y su sintaxis. La función `println()` sirve para imprimir texto y no está como parte de la función `main()`, es simplemente un ejemplo.
