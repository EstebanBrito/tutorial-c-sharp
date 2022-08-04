<!------Titulo------>
# Funciones en C#
Las funciones son un bloque de código que se reutilizan en una clase, esto con el propósito de no tener que volver a escribir el mismo segmento de código para realizar una operación. Las funciones que están asociadas a un objeto o clase se les denominan *Métodos*, debido a que cumplen una función integral en la clase, las funciones en cambio existen por si solas, puesto que no necesitan el uso de un objeto.
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
void Print Hello World()
{
    Console.WriteLine("H"ola Mundo");
}
PrintHelloWorld();
PrintHelloWorld();
PrintHelloWorld();
```
Si bien no se distingue una diferencia notable a simple vista
## Sintaxis de una Función


## Función vs Método

```csharp
void Suma(int a, int b)
{

}
```

