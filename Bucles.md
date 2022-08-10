# Bucles en C#

En programación utilizamos bucles para iterar la ejecución de uno o varios bloques de código , el número de iteraciones es definido por una condición establecida dentro del programa, según el tipo de bucle que se está utilizando, como se mostrará más adelante en el blog.

## Bucle while

El bucle más común es el bucle while, si la condición es verdadera el bloque de código se ejecutará en infinitas iteraciones mientras la condición sea verdadera, si es falsa se detendrá, por lo que el bucle while se utiliza cuando no se sabe exactamente la cantidad de veces que se va a iterar el bloque de código en cuestión.

### SÍNTAXIS:
```C#
while (condición)
{
   // bloque de código que se ejecutará
}
```
### EJEMPLO:

En el siguiente ejemplo el usuario va a una taquería para saciar su hambre comiendo tacos hasta que le indique que está satisfecho utilizando un "si" o "no" como respuesta, como extra se agregó un contador de tacos consumidos para contar la cantidad de iteraciones del bloque de código. 
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

            Console.WriteLine("¿Tienes hambre?");

            string respuesta = Console.ReadLine();

            //la condición es que siempre que el contenido del String "respuesta" sea "si" lo que está dentro de los corchetes del while seguirá iterando hasta que el usuario escriba otra cosa finalizando con el bucle

            while (respuesta == "Si") 
            {
                Console.WriteLine("*Come un taco*");

                TacosConsumidos++;

                Console.WriteLine("¿Deseas comer más?");
                respuesta = Console.ReadLine();

                //aquí si el usuario escribió otra cosa que no haya sido si, el bucle terminará
            }
            Console.WriteLine($"Consumiste {TacosConsumidos} tacos");
        }
    }
    
}
```
## Bucle do-while

La sentencia do-while funciona prácticamente igual al while con la importante diferencia de que el *while* **primero** evalúa la condición y **después** ejecuta el bloque de código, el *do-while* lo hace alrevés, **primero** ejecuta el bloque de código y **después** evalúa la condición.

### SÍNTAXIS:
```C#
do
{
    // bloque de código que se ejecutará

}while (condición);
```
### EJEMPLO:

El ejemplo es el mismo que el de while pero esta vez usando *do-while*, la diferencia aquí es que el programa primero ejecutará el código dentro del bucle sin importar la repsuesta que se de, luego evaluará la condición para determinar si el do-while va a seguir iterando o no .

```C#
using System;

namespace BucleWhile
{
    class Program
    {
        static void Main(string[] args)
        {
            int TacosConsumidos = 0;

            Console.WriteLine("¿Tienes hambre?");

            string respuesta = Console.ReadLine();

            //primero ejecutará el codigo incluso si la condición es falsa
            do
            {
                Console.WriteLine("*Come un taco*");
                TacosConsumidos++;
                Console.WriteLine("¿Deseas comer más?");
                respuesta = Console.ReadLine();
            }
            //luego evalúa la condición para determinar si el do-while va a seguir iterando o no
            while (respuesta == "Si");

            Console.WriteLine($"Consumiste {TacosConsumidos} tacos");
        }
    }
    
}
```
## Bucle for

La sentencia de bucle *for* se suele utilizar cuando sabemos el número específico de iteraciones que necesitamos que se realicen dentro del bloque de código, declarando una **variable de inicialización**, un **límite de iteraciones** y un **contador incrementador o decrementador** como se muestra en la síntaxis más adelante.

### SÍNTAXIS:

```C#
for (int i = 0 ; i <= x; i++)
{    
    //bloque de código que se ejecutará
}
```
### EJEMPLO:
En el siguiente ejemplo se utiliza la sentencia de bucle *for* para imprimir un texto **6** veces, la variable *i* empieza con valor cero y va aumentando su valor +1 por cada iteración del bloque de código hasta llegar hasta el *6*. 

```C#
using System;

namespace BucleFor
{
    class Program
    {
        static void Main(string[] args)
        {
            for (int i = 0; i < 6; i++)
            {
                Console.WriteLine("TEXTO DE EJEMPLO");
            }
        }
    }
    
}
```
## Bucle foreach

La sentencia de bucle *foreach* enumera los elementos (int,Char,String,float double) de una variable, arreglo, colecciones o listas y ejecuta el bloque de código por cada elemento contado.

SÍNTAXIS:
```C#
foreach(tipoDato nombre in array)
{
     //bloque de código que se ejecutará
}
```

### EJEMPLO:

En el siguiente ejemplo se contará la cantidad de números dentro del arreglo de enteros "Numeros" por medio de un *foreach* y posteriormente se imprimirá.

```C#
using System;

public class Program
{
	static void Main(string[] args)
	{
		int[] Numeros = { 1, 2, 3, 4, 5 };
		int ContadorNumeros=0;
        //el foreach barre todo el arreglo "Numeros" por medio de la variable "Numero" y hace válida la condición por cada elemento del arreglo
		foreach (int Numero in Numeros)
		{
			ContadorNumeros++;	
		}
		Console.WriteLine($"se contaron {ContadorNumeros} numeros");

	}
	
}
```
## Instrucción break
La instrucción *break* se utiliza dentro de una sentencia de bucle para (como su nombre lo indica) **romper** su ejecución, en otras palabras: finaliza el proceso de manera forzosa, dependiendo de una condición previamente establecida.

Como se muestra en el siguiente ejemplo que aumenta el valor de *i* en 1+ por cada iteración y dentro tiene una condicional que indica que si *i* es igual a 6 entonces el bucle se romperá:
```C#
for (int i = 0; i < 12; i++) 
{
  //
  if (i == 6) 
  {
    break;
  }
  Console.WriteLine(i);
}
```

## Instrucción continue
La instrucción *continue* es similar a la instrucción *break*, solo que *continue* no finaliza con las iteraciones del bucle, solo "omite" la iteración en cuestión si la condicional es verdadera.

Como se muestra en el siguiente ejemplo que aumenta el valor de *i* en 1+ por cada iteración y dentro tiene una condicional que indica que si *i* es igual a 6 entonces el bucle omitirá la iteración donde *i* es igual a 6 y seguirá con el bucle:
```C#
for (int i = 0; i < 12; i++) 
{
  if (i == 6) 
  {
    continue;
  }
  Console.WriteLine(i);
}
```
## banderas
En programación utilizamos variables llamadas *banderas* para marcar cuando una posible situación prevista por el programador es verdadera o falsa, por lo que usualmente se usan variables de tipo booleano para declararlas.

Funciona entre algunos ejemplos para marcar que se ha encontrado cierto elemento al barrer un arreglo o para marcar un error dentro del programa y poder programar una línea de acción para hacer que el código se realinie o como se muestra en el siguiente ejemplo: para que el usuario pueda salir de un bucle aparentemente infinito utilizando un símbolo clave.

### EJEMPLO:

En el siguiente ejemplo se hace una sumatoria con 2 números que se preguntan al usuario como strings que posteriormente se convierten en enteros y se suman, el bucle va a repetirse infinitamente hasta que el valor de la *bandera* sea verdadero, lo cual se logra si el usuario al final presiona la tecla z.
```C#
using System;

public class Program
{
	static void Main(string[] args)
	{
		int Num1, Num2, Suma;
		string cadena = string.Empty;
		bool Bandera = false;

		do
		{
			Console.WriteLine("Sumatoria, ingrese 2 números:)");

			Console.WriteLine("Número 1:");
			cadena = Console.ReadLine();
			Console.WriteLine(cadena);
			
			Num1 = Convert.ToInt32(cadena);

			Console.WriteLine("Número 2:");
			cadena = Console.ReadLine();
			Num2 = Convert.ToInt32(cadena);


			Suma = Num1 + Num2;
			Console.WriteLine($"La suma es igual a {Suma}");
			Console.WriteLine("presione cualquier tecla para continuar | presione z para terminar");
			cadena = Console.ReadLine();
			if (cadena == "z")
			{
				Bandera = true;
			}
		}
		while (Bandera == false);


	}

	
}
```