# Bucles en C#

En programación utilizamos bucles para iterar la ejecución de uno o varios bloques de código dependiendo de una condición establecida según el tipo de bucle que se usa en el programa.

## Bucle while

El bucle más común es el bucle while, si la condición es verdadera el bloque de código se ejecutará en infinitas iteraciones mientras la condición sea verdadera, si es falsa se detendrá, por lo que el bucle while se utiliza cuando no se sabe exactamente la cantidad de veces que se va a iterar el bloque de código en cuestión.

EJEMPLO:

en el siguiente ejemplo el usuario va a una taquería para saciar su hambre comiendo tacos hasta que le indique que está satisfecho utilizando un "si" o "no" como respuesta, como extra se agregó un contador de tacos consumidos para contar la cantidad de iteraciones del bloque de código. 
```C#
using System;
namespace BucleWhile
{
    class Program
    {
        static void Main(string[] args)
        {
            //número de veces que se va a iterar el código dentro del while
            int TacosConsumidos = 0;

            Console.WriteLine("tienes hambre?");

            string respuesta = Console.ReadLine();

            //la condición es que siempre que el contenido del String "respuesta" sea "si" lo que está dentro de los corchetes del while seguirá iterando hasta que el usuario escriba otra cosa finalizando con el bucle

            while (respuesta == "si") 
            {
                Console.WriteLine("*come un taco*");

                TacosConsumidos++;

                Console.WriteLine("deseas comer más?");
                respuesta = Console.ReadLine();

                //aquí si el usuario escribió otra cosa que no haya sido si, el bucle terminará
            }
            Console.WriteLine($"consumiste {TacosConsumidos} tacos");
        }
    }
    
}
```



