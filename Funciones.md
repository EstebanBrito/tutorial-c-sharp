<!------Titulo------>
# Funciones en C#
Las funciones son un bloque de código que se reutilizan en una clase, esto con el propósito de no tener que volver a escribir el mismo segmento de código para realizar una operación. Las funciones que están asociadas a un objeto o clase se les denominan **Métodos**, debido a que cumplen una función integral en la clase, las funciones en cambio existen por si solas, puesto que no necesitan el uso de un objeto.

## Sintaxis de una Función
```csharp
void HelloWorld()
{
   Console.WriteLine("Hello World"); 
}
```
En esta función debemos de tener en cuenta los siguientes parámetros:

* `void`
* `HelloWorld()`
*  `Console.WriteLine("Hello World");`

La palabra clave `void` le indica al compilador que la función no regresara ningún tipo de valor. `HelloWorld` es el nombre de nuestra función. `Console.WriteLine(“Hello World”);` es el cuerpo de la función, todo lo que este adentro de las `{}` se ejecutara cuando se llame la función.


## ¿Cómo llamar una función?
Una función

## Parametros y argumentos
Los parametros son 
 


## ¿Por qué es integral el uso de las funciones?
Las funciones tienen un propósito más relevante que simplemente ser capaz de reutilizarse para hacer una labor, la funcionalidad de encapsular un bloque de código nos permite optimizar nuestro código, ya que si utilizamos la misma instrucción para realizar una suma, el tiempo de compilación seria notable, cuando uno trabaje con programas sencillo puede no notar este tiempo, pero cuando se trabaja con proyectos más grandes, una suma u operación mal optimizada puede significar un tiempo considerable para realizar una acción. En el siguiente *Ejemplo* se muestra el punto anterior.
## Ejemplo.
### Sin uso de funciones
```csharp
Console.WriteLine("Hola Mundo");
Console.WriteLine("Hola Mundo");
Console.WriteLine("Hola Mundo");
```
### Empleando funciones
```csharp
void PrintHelloWorld()
{
    Console.WriteLine("Hola Mundo");
}
PrintHelloWorld();
PrintHelloWorld();
PrintHelloWorld();
```
Si bien no se distingue una diferencia notable a simple vista, mediante el uso de la funciones le estamos comunicando al compilador que haga uso del bloque de código que previamente creamos para realizar la operación, por lo tanto le toma menos tiempo escribir “Hola Mundo", puesto que no tiene la necesidad de ejecutar tres comando en repetidas ocasiones, de igual forma es una forma sencilla de facilitar la lectura del código, debido a que las funciones son explicitas en su naturaleza.