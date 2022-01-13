# Java Virtual Machine

Una máquina virtual es una simulación, ya sea de un sistema operativo o de los procesos que ocurren dentro de uno. La Java Virtual Machine pertenece al segundo tipo, y por lo tanto se denomina "Process Virtual Machine". Las ventajas de estas es que permiten manejar punteros y referencias de memoria que en lenguajes como C o C++ se realiza manualmente. Para esto se utiliza el proceso Garbage Collection, el cual se encarga de revisar aquellos espacios en memoria que no se están utilizando para eliminarlos y reducir la memoria que consume el programa.

La JVM funciona como un traductor entre código y lenguaje máquina. El código es convertido a un lenguaje denominado Java Bytecode. Es debido a esto que se puede ingresar código de Kotlin y tener un programa funcional, debido a la compatibilidad del Java Bytecode.
