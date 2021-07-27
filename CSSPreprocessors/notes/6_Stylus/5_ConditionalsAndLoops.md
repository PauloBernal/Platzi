# Condicionales y ciclos

## Ciclos

Los ciclos son estructuras que ejecutan un pedazo de código hasta que una función se cumpla o se deje de cumplir. Para ejecutar un ciclo en Stylus se utiliza a palabra reservada `for` seguida de una variable provisional de iteración de elementos, después la palabra reservada `in` y los elementos a iterar. En la parte de abajo se coloca el código a ejecutarse y si se quiere añadir la variable como texto se coloca entre llaves:

~~~stylus
for var in val2 val2 ... valN
  *code*
  ...{var}
  ...
~~~

## Condicionales

Los condicionales son estructuras que pemriten ejecutar o integrar un pedazo de código u otro dependiendo de una condición. Para realizar un condicional se coloca primero la palabra reservada `if` seguida de la condición y en la parte de abajo con identación el código a ejecutarse si se cumple la condición. En caso contrario se utiliza la palabra reservada `else` y abajo con identación el código que se ejecuta o integra si no se cumple la condición:

~~~stylus
if *condition*
  *code*
else
  *code*
~~~
