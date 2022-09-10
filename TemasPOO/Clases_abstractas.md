# Clases abstractas en c#

En este pequeño blog se explicará el uso de la palabra reservada abstract, que es una clase y método abstracto. También se explicará como heredar una clase abstracta e implementar sus métodos.

## ¿Qué son las clases abstractas y para qué se usan en programación?

Una clase abstracta se define con la palabra reservada abstract, este tipo de clases tiene la funcionalidad de servir como una clase base que se heredará a otras clases NO ABSTRACTAS que requieran de su funcionalidad. Es necesario recalcar que NO SE PUEDE crear una instancia de una clase abstracta (es decir que no podemos crear objetos de dicha clase).

Las clases abstractas tienen métodos incompletos (no tienen cuerpo), estos métodos tienen que ser implementados en las clases que heredan la clase abstracta, ya que si no se hace se genera un error en la compilación.

## Uso y sintaxis de la palabra reservada abstract tanto en clases como en métodos.

Para crear una clase o método abstracto es necesario usar la palabra reservada abstract. Esta palabra reservada se escribe justo antes de la palabra reservada class (para las clases) o justo antes del tipo de dato del método. 

A continuación se presenta un ejemplo de su sintaxis, tanto para la clase abstracta como para el método abstracto.

```C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace EjemploAbstraccion
{
    //creamos la clase abstracta 
    public abstract class AbstractAnimales
    {   
        //creamos el método abstracto
        public abstract string Sonido();
    }
}
```

## ¿Cómo heredar de una clase abstracta e implementar sus métodos?

Para heredar una clase abstracta primero necesitamos otra (u otras) clase(s) que requieran de los métodos abstractos de la clase abstracta. 

Para heredar una clase abstracta se sigue la siguiente sintaxis: 

```C#
public class ClaseQueHereda:ClaseAbstracta{
    //para implementar el método abstracto se usa la palabra   
    //reservada override
    public override tipoDatoMetodoDelAbstracto nombreMetodoAbs()
    {
        //Implementación del método abstracto    
    }
}
```
Ahora veamos un ejemplo de como heredar la clase abstracta en un programa:

```C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace EjemploAbstraccion
{
    //creamos la clase abstracta
    public abstract class AbstractAnimales
    {
        //creamos el método abstracto
        public abstract string Sonido();
    }

    //creamos la clase que heredará la clase abstracta
    public class Perro:AbstractAnimales
    {
        public override string Sonido()
        {
            //Aquí implementamos el método abstracto
            Console.WriteLine("Waw waw");
        }
    }

    class Program{
        static void main(string[] args)
        {
            
            Perro Perrito=new Perro();//Instanciamos la clase Perro
            Perrito.Sonido();//Ejecutamos el método abstracto
        }
    }
}
```

## Referencias
Información recuperada de:

[w3schools C# Abstraction](https://www.w3schools.com/cs/cs_abstract.php)

[Microsoft C# abstract](https://docs.microsoft.com/es-es/dotnet/csharp/language-reference/keywords/abstract)

[csharp.net-tutorials clases abstractas](https://csharp.net-tutorials.com/es/123/clases/clases-abstractas/)
