# Condicionales en C#

## Condicional if
Es una estructura condicional que permite la toma de decisiones evaluando una operación lógica. 

Si el resultado de esa operación es true entonces ejecutará el bloque de código siguiente, si es falso no ejecutará el código que esté dentro del bloque del if.

Se verá en el siguiente ejemplo como se usa el condicional if. 
```C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace EjemploIf
{
    public class Program
    {
        static void Main(string[] args)
        {
            int edadJuan=17;
            if (edadJuan<18)
            {
                Console.WriteLine("Juan NO puede ir a Bandidas");
            }
        }
    }
}
```
La variable edadJuan es un entero y tiene como valor 17. Al entrar al bloque del if este evalúa la variable con la condición que se ha puesto (en este caso compara si edadJuan es mayor o igual a 18). Al realizar la comparación da un resultado falso por lo tanto no se ejecuta el bloque de código dentro de las llaves del if y se salta a la siguiente instrucción. En este caso la consola imprimirá **"Juan NO puede ir a Bandidas"**.

También existe una forma de hacer el código del if más simple, este forma solo se usa cuando solo se va a ejecutar una sola línea de código. Lo que se hace es omitir las llaves del if y dar una identación o tambíen se puede escribir la línea de código inmediatamente despues del if.

```C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace EjemploIf
{
    public class Program
    {
        static void Main(string[] args)
        {
            int edadJuan=18;
            if (edadJuan<18) Console.WriteLine("Juan NO puede ir a Bandidas");
               
        }
    }
}
```
## Condicional if else
El else es una adición al if, este ejecuta un bloque de código si la condición dió como resultado false.

```C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace EjemploIfElse
{
    public class Program
    {
        static void Main(string[] args)
        {
            int edadJuan=17;
            if (edadJuan>=18) 
            {
                Console.WriteLine("Juan puede ir a Bandidas");
            } 
            else
            {
                Console.WriteLine("Juan NO puede ir a Bandidas");
            }  
        }
    }
}
```
En el ejemplo anterior la condición se evalua y da como resultado false, así que se ejecuta el bloque de código asociado al else.

Al igual que pasa como con el if si solamente se ejecuta una línea de código las llaves se pueden omitir. 

```C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace EjemploIfElse
{
    public class Program
    {
        static void Main(string[] args)
        {
            int edadJuan=17;

            if (edadJuan>=18) Console.WriteLine("Juan puede ir a Bandidas");

            else Console.WriteLine("Juan NO puede ir a Bandidas");  
        }
    }
}
```

## Condicional else if
El condicional else if se usa cuando la primera condición resulta ser false, pero se quiere evaluar otra condición de manera inmediata.

```C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace EjemploIfElse
{
    public class Program
    {
        static void Main(string[] args)
        {
            int valor1=10, valor2=10;

            if (valor1>valor2){
                Console.WriteLine(val1+" es mayor a "+val2);
            }else if(valor1<valor2){
                 Console.WriteLine(val2+" es mayor a "+val1);
            }else{
                 Console.WriteLine(val1+" es igual a "+val2);
            }
        }
    }
}
```
En el anterior ejemplo tanto valor 1 como valor 2 tienen el mismo valor (10). En el primer if la condición se evalua como false (por que valor1 no es mayor a valor2), por lo tanto pasa al siguiente else, este al tener otro if tiene que volver a evaluar la condición y da como resultado false (valor 1 no es menor que valor2), finalmente pasa al siguiente else y la consola imprime "10 es igual a 10".

# Referencias 
Información recuperada de [w3schools cs conditions](https://www.w3schools.com/cs/cs_conditions.php)