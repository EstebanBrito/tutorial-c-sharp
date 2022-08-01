# Introducción a C#

C# (pronunciado "se sharp") es un lenguaje de programación moderno, tipado y orientado a objetos. C# se origina de la misma familia que C, y por lo tanto, es sumamente similar a éste, así como a C++ y Java. A lo a largo de todo este tutorial se describirán diversos aspectos del lenguaje referentes a sintáxis, desarrollo de software, entre otros temas.   

## Características generales

C# es un lenguaje orientado a objetos, pero igual está orientado a componentes, proveyendo recursos sintácticos que soporten el desarrollo de componentes. De igual forma, C# posee otras características que ayudan a crear aplicaciones robustas. Entre ellas se encuentran:   

* Limpieza automática de memoria, reclamando almacenamiento ocupado por objetos no usados.
* Tipos nulos que protegen de variables que no apunten a objetos almacenados.
* Manejo de excepciones como una manera estructurada y extensible para la detección de errores.
* Exception handling provides a structured and extensible approach to error detection and recovery.
* Expresiones lambda que soportan técnicas propias del paradigma de programación funcional.
* La sintáxis LINQ (del inglés, *Language Integrated Query*) crea un patrón común para trabajar con datos de cualquier fuente.
* Soporte para operaciones asíncronas y desarrollo de sistemas distribuidos.
* Todos los tipos de C# (incluidos los tipos primitivos como *int* y *double*) heredan de un sólo objeto padre. Todos estos tipos comparten una serie de operaciones comunes y los valores de un tipo pueden almacenados, transportados y manipulados de una manera consistente.
* Soporte para tipos definidos por el usuario, sean tipos de referencia o tipos de valor.
* Alocación dinámica de objetos y otras estructuras ligeras.   

## ¿Por qué usar C#?

Hay muchas razones por las cuales C# es popular. Algunas de estas razones son:

* Fácil de usar: C# es un lenguaje de alto nivel similar a otros lenguaje populares como C, C++ o Java, por lo que aprender C# se vuelve una tarea sencilla para programadores con experiencia.
* C# es ampliamente usado par el desarrollo de aplicaciones web y aplicaciones de escritorio, especialemente para entornos Windows o para aplicaciones de Microsoft en general.
* La comunidad de C# es extensa, por lo que hay un soporte amplio para nuevas herramientas y artefactos de código. Además, esto asegura que C# seguirá vivo por bastante tiempo.
* C# es también uno de los lenguajes más usados para el desarrollo de videojuegos, principalmente por características como la recolacción automática de basura, interfaces, orientación a objetos, etc.

## Tu primer programa

### Código
```c#
// Programa para imprimir "Hola, Mundo"
using System;
  
namespace AppHolaMundo
{   
    class HolaMundo
    {   
        // Función main
        static void Main(string[] args)
        {
  
            // Imprimir "Hola, Mundo"
            Console.WriteLine("Hola, Mundo");
            // Pide a C# esperar a que se presione una tecla
            // Evita que la consola se cierre automáticamente
            Console.ReadKey();
        }
    }
}
```

### Salida

```bash
$ Hola, Mundo
```

### Explicación del código

#### Comentarios

Los comentarios son usados para explicar el código escrito y son ignorados por el compilador, así que no son ejecutados como tal. Siguen una sintáxis similar a lenguajes como Java.
Los comentarios de una línea se ven de la siguiente manera:

```c#
// Comentario de una línea
```

Los comentarios multilínea se declaran así:

```c#
/* 
Multi line comments
...
...
*/
```

#### System

"System" es una palabra reservada que incluye el espacio de nombres "System" en el programa. Un espacio de nombres hace referencia a una colección de clases y otros recursos programáticos existentes. En este caso, nuestro programa existe en el espacio "AppHolaMundo", la cual contiene la clase HolaMundo (y otros elementos que incluyan la línea "namespace AppHolaMundo).

#### Clases

Las clases son el elemento principal de los lenguajes orientados a objetos. Información adicional será agregada sobre ese tema en el futuro. Un programa de C# necesita una clase principal sobre la cual trabajar. En nuestro caso, es la clase HolaMundo.

#### static void Main()

Un programa en C# también necesita una función Main que funja como su punto inicial de ejecución. Esta función (la cual es un método de la clase HolaMundo), debe cumplir con dos características:

1. Debe ser estática, lo que significa que deberá ser posible ser usada sin instanciar objetos de la clase a la que pertenece. Esto se lleva a cabo anteponiendo la palabra reservada *static*.
2. No debe tener un tipo de retorno. Las funciones pueden devolver valores, pero la función principal no debería realizar esto, por lo que se le antepone la palabra reservada *void*.

#### Console

Console es un objeto perteneciente al espacio "System". Posee funciones que permiten interactuar con la consola del sistema (como cmd, en el caso de Windows). Específicamente, se usan dos funciones:

1. Console.WriteLine(), que imprime en la consola el mensaje especificado.
2. Console.ReadKey(), que hace al programa esperar a que una tecla se presione. Esto es puesto al final de ciertos programas basados en consola para evitar que ésta se cierre automáticamente una vez se hayan ejecutados todas las instrucciones que la componen.

Cabe resaltar el uso de puntos y comas (;) al final de las líneas de código.

