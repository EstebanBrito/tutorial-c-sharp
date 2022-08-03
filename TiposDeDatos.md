# Tipos de datos en C#

### Variables y su forma de declarar: 

**int** i =0;
**decimal** x=0.0m;
**float** f=0.0f; 
**double** d=0.0D; 
**string** cadena= "Hola mundo"
**bool** o **boolean** bandera = false;
**DateTime** (se utiliza una clase y representa un valor que puede guardar tanto fechas como horas), fecha= DateTime.MinValue; 


### Imprimir variables: 

Console.WriteLine("El valor de i es: {0}",i);
Console.WriteLine("El valor de x es: {0:C}", x);
Console.WriteLine("El valor de f es: {0:F2}", f);
Console.WriteLine("El valor de d es: {0:F2}",d);
Console.WriteLine("El valor de cadena es: "+ cadena );
Console.WriteLine("El valor de bandera es: "+ bandera.ToString());
Console.WriteLine("El valor de fecha es: "+ fecha-ToShortDateString());
console.ReadKey(); 