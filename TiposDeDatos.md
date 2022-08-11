# Tipos de datos en C#

C# es un lenguaje tipado, las variables que maneja(todo aquello declarado por el programador que quiera hacer referencia a asignar un valor) y constantes deben tener un tipo asi como cualquier expresión que se evalue como un valor. 

Entre la información almacenada en un tipo se pueden incluir los siguientes elementos:

-El espacio de almacenamiento que requiere una variable del tipo.
-Los valores máximo y mínimo que puede representar.
-Los miembros (métodos, campos, eventos, etc.) que contiene.
-El tipo base del que hereda.
-Interfaces que implementa.
-Los tipos de operaciones permitidas.

Este sistema de tipado de variables es muy necesario dentro de este tipo de lenguajes puesto que sin el para  que el compilador trabaje de manera correcta.  

## Espacio en memoria

-Int -> 32 bits
-Float -> 32 bits
-Double -> 64 bits 
-decimal -> 128 bits
-bool -> 8 bits 

para leer mas sobre los espacios en memoria que ocupa cada tipo de dato puedes checar [aqui] (https://www.incanatoit.com/2014/11/operadores-tipos-de-datos-variables-programacion-csharp-net.html)


## Variables y su forma de declarar: 

-**int** i =0;
-**decimal** x=0.0m; (En este caso se agrega un modificador m para indicar que es de tipo decimal) 
-**float** f=0.0f; (En este caso se agrega un modificador f para indicar que es de tipo float) 
-**double** d=0.0D; (En este caso se agrega un modificador d para indicar que es de tipo double) 
-**string** cadena= "Hola mundo"
-**bool** o **boolean** bandera = false;

#### En el caso del DateTime, existen distintas formas de declarar el formato a continuación, se muestran:

-**DateTime** (se utiliza una clase y representa un valor que puede guardar tanto fechas como horas), fecha= DateTime.MinValue; 
-DateTime= new DateTime(año, mes, dia); 
-DateTimeConHora= new DateTime (año, mes , dia, hora, minutos, segundos); 
[Aqui](https://www.youtube.com/watch?v=a3s3BxnDG44) te dejo un video con mas información del DateTime


## Imprimir variables: 

-Console.WriteLine("El valor de i es: {0}",i);
-Console.WriteLine("El valor de x es: {0:C}", x);
-Console.WriteLine("El valor de f es: {0:F2}", f);
-Console.WriteLine("El valor de d es: {0:F2}",d);
-Console.WriteLine("El valor de cadena es: "+ cadena );
-Console.WriteLine("El valor de bandera es: "+ bandera.ToString());  _El metodo ToString es para poder transformar ese valor booleano a cadena para la impresión_
-Console.WriteLine("El valor de fecha es: "+ fecha.ToShortDateString());
-Console.ReadKey(); 

En el caso de las impresiones con signos como _{0:C}_, esto hace referencia al formato que se le dara a la impresión en este caso es de moneda pero de igual manera existen otros , puedes obtener mas información [aqui](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings) 
