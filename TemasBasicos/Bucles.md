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

El ejemplo es el mismo que el de while pero esta vez usando *do-while*, la diferencia aquí es que el programa primero ejecutará el código dentro del bucle sin importar la repsuesta que se de, luego evaluará la condición para determinar si el do-while va a seguir iterando o no.

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

La sentencia de bucle *for* se suele utilizar cuando sabemos el número específico de iteraciones que necesitamos que se realicen dentro del bloque de código, declarando una **variable de inicialización** para dar un valor base a la variable que almacenará la cantidad de iteraciones, éste valor por lo general empieza con 0, un **límite de iteraciones** para indicar un valor que cuando sea alcanzado, el bloque de código se va a dejar de iterar y un **contador incrementador o decrementador** para llevar un control de cuantas unidades aumenta o decrementa el valor de la variable donde se almacena la cantidad de iteraciones realizadas como se muestra en la síntaxis más adelante.

### SÍNTAXIS:

```C#
for (int i = 0 ; i <= x; i++)
{    
    //bloque de código que se ejecutará
}
```
### EJEMPLO:
En el siguiente ejemplo se utiliza la sentencia de bucle *for* para imprimir un texto **6** veces, la variable *i* (**variable de inicialización**, i=0) empieza con valor cero y va aumentando su valor +1 (**contador incrementador o decrementador**, i++) por cada iteración del bloque de código, hasta llegar a la *sexta* iteración (**límite de iteraciones**, i<6). 

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

La sentencia de bucle *foreach* itera sobre los elementos de una variable, arreglo, colección o lista y ejecuta el bloque de código por cada elemento iterado, se suele utilizar en vez de otros bucles cuando se busca iterar el bloque de código según un número de elementos específicos encontrados dentro de la colección en cuestión.

SÍNTAXIS:
```C#
foreach(tipoDato nombre in array)
{
     //bloque de código que se ejecutará
}
```

### EJEMPLO:

En el siguiente ejemplo el *foreach* barrerá todo el vector y sumará los números por cada entero dentro, almacenando la sumatoria en la variable "Suma".

```C#
using System;

public class Program
{
	static void Main(string[] args)
	{
		int[] Numeros = { 1, 2, 3, 4, 5 };
		int Suma = 0;
		//el foreach barre todo el arreglo "Numeros" por medio de la variable "Numero" y hace válida la condición por cada elemento del arreglo
		foreach (int Numero in Numeros)
		{
			Suma = Suma + Numero;
		}
		Console.WriteLine($"la suma de todos los números es {Suma} unidades)");

	}

}
```
## Instrucción break
La instrucción *break* se utiliza dentro de una sentencia de bucle para (como su nombre lo indica) **romper** el bucle en cuestión, en otras palabras: finaliza el bucle de manera forzosa, ya sea con una condición previamente establecida o como un default para salir de un bucle.

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
El programa imprimiría esto:
0
1
2
3
4
5

El programa terminaría de imprimir números en el 5 porque como se menciona anteriormente, el 6 provoca la interrupción del bucle.

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
El programa imprimiría esto:
0
1
2
3
4
5
7
8
9
10
11

El programa imprime todos los números a excepción del 6, ya que como se menciona anteriormente, la iteración 6 es omitida por el continue.

## banderas
Una bandera es una variable lógica que se utiliza en el mundo de la programación para indicar que una condición es verdadera o falsa, permitiendo comunicar información de una parte del código a otra, para mantener un control dentro del código.

### EJEMPLO:

En el siguiente ejemplo se multiplica un número por 2 un número que debe ingresar el usuario, el bucle va a repetirse infinitamente hasta que el valor de la *bandera* sea verdadero, lo cual se logra si el usuario al final presiona la tecla z.
```C#
using System;

public class Program
{
	static void Main(string[] args)
	{
		int Num, Multi;
		string cadena = string.Empty;
		bool Bandera = false;

		do
		{
			Console.WriteLine("ingrese un número para multiplicar por 2:)");

			Console.WriteLine("Número:");
			cadena = Console.ReadLine();
			Console.WriteLine(cadena);
			Num = Convert.ToInt32(cadena);

			Multi = Num * 2;

			Console.WriteLine($"La multiplicación es igual a {Multi}");
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