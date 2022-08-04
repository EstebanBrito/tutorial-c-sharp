<!------Titulo------>
# **Funciones en C#**
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
* `HelloWorld`
* `()`
*  `Console.WriteLine("Hello World");`

La palabra clave `void` le indica al compilador que la función no regresara ningún tipo de valor, en caso de que se deseé regresar un valor se tiene que cambiar `void` al tipo de dato que se desea regresar.

 `HelloWorld` es el nombre de nuestra función.

 `()` es la parte en donde se colocan los parametros a emplear. 
 `Console.WriteLine(“Hello World”);` es el cuerpo de la función, todo lo que este adentro de las `{}` se ejecutara cuando se llame la función.


## ¿Cómo llamar una función?
Para llamar una función se escribe el nombre de la función acompañada de un par de paréntesis donde generalmente suelen estar los parámetros. Usando la función anterior como ejemplo, se mostrara como llamar una función para que ejecute su bloque de instrucciones.

```csharp
void HelloWorld()
{
   Console.WriteLine("Hello World"); 
}

HelloWorld();
```
El output de la función sería el siguiente:
`Hello World`
## Parametros y argumentos
Los parámetros son la parte de la estructura de la función que nos permite trabajar con variables afuera de nuestro bloque, para ello a la función se le tiene que añadir los siguientes criterios adentro del parentesis:

1. Tipo de dato.
2. Nombre del parametro.

Los argumentos en cambio son aquellas variables o valores que se le proporcionan a la función cuando se le llama.

### Ejemplo
```csharp
void Suma(int a, int b)
{
    int sum = a + b;
    Console.WriteLine(sum);
}
```
En el ejemplo anterior se hace uso de los parámetros a y b, como bien se puede observar son de tipo entero, por lo cual la función no funcionara si hacemos uso de argumentos con valor decimal. De igual forma están separados por una coma entre cada parámetro, debido a que la sintaxis lo demanda.

## ¿Cómo regresar un tipo de dato?

## ¿Qué es una firma y cuál es su finalidad?

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