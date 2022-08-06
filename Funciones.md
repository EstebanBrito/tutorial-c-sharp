<!------Titulo------>
# **Funciones en C#**
Las funciones son un bloque de código que se reutilizan, esto con el propósito de no tener que volver a escribir el mismo segmento de código para realizar una operación. Las funciones que están asociadas a un objeto o clase se les denominan **Métodos**.

## Sintaxis de una Función
```csharp
void HelloWorld()
{
   Console.WriteLine("Hello World"); 
}
```
En esta función debemos de tener en cuenta los siguientes elementos:

* `void`
* `HelloWorld`
* `()`
*  `Console.WriteLine("Hello World");`

La palabra clave `void` le indica al compilador que la función no regresara ningún tipo de valor, en caso de que se desee regresará un valor se tiene que cambiar `void` al tipo de dato que se desea regresar.

 `HelloWorld` es el nombre de nuestra función.

 `()` es la parte en donde se colocan los paraámetros a emplear. 

 `Console.WriteLine(“Hello World”);` es el cuerpo de la función, todo lo que esté adentro de las `{}` se ejecutará cuando se llame la función.

 Dentro de las funciones de igual forma se pueden codificar funciones y variables para desarrollar labores, lo único a tomar en cuenta cuando se trabajar con estas funciones y variables, es que únicamente existen cuando se llama la función, por lo tanto si se desea hacer referencia a una variable que se creó en una función el compilador nos dirá que no esta permitido.

## ¿Qué es declarar una función?
Declarar una función es el proceso en el cual creamos una función siguiendo la sintaxis, para ello se necesita proporcionar el valor de retorno, el nombre y los argumentos junto con su tipo de datos.

## ¿Qué es y cómo se llama una función?
Llamar una función es la manera por la cual le comunicamos al compilador que ejecuté la función.

Para llamar una función se escribe el nombre de la función acompañada de un par de paréntesis donde generalmente suelen estar los parámetros. Usando la función anterior como ejemplo, se mostrara como llamar una función para que ejecute su bloque de instrucciones.

```csharp
void HelloWorld()
{
   Console.WriteLine("Hello World"); 
}

HelloWorld();
```
El output de la función sería el siguiente:
```bash
Hello World
```

## Declarar vs Llamar
La diferencia entre llamar y declarar es vasta, puesto que declarar es crear y encapsular el bloque de código, mientras que llamar es ejecutar ese bloque de código en alguna parte.

## Parámetros 
Cuando se desea trabajar con variables externas a la función se hace uso de los **Parámetros**, en el momento en que la función es llamada la función recibirá los parámetros. Para trabajar con parámetros es necesario declararlos dentro de los paréntesis de la función cuando se está declarando, de igual forma es necesario incluir los siguientes criterios cuando se desea declarar los parámetros de una función:

1. Tipo de dato.
2. Nombre del parametro.

## Argumentos
Los argumentos en cambio son aquellas variables o valores que se le proporcionan a la función cuando se le llama.

### Ejemplo
```csharp
void Suma(int a, int b)
{
    int sum = a + b;
    Console.WriteLine(sum);
}
```
En el ejemplo anterior se hace uso de los parámetros a y b, como bien se puede observar son de tipo entero, por lo cual la función no funcionará si hacemos uso de argumentos con valor decimal. De igual forma están separados por una coma entre cada parámetro, debido a que la sintaxis lo demanda.

## ¿Cómo retornar en una función?
Una función puede retornar una variedad de elementos, como lo son objetos, tipo de variables, etc. Para retornar un elemento en una variable se debe de cambiar la palabra clave `void` por el tipo de dato que deseamos retornar por ejemplo un `int` le indicaría al compilador que la función debe de retornar un entero. La palabra clave `return` es la que se encarga de regresar el valor que debe de retornar nuestra función, pero es de suma importancia denotar que al momento en que el compilador lee `return` termina la función dejando sin ejecutar los comando posteriores al `return`, de igual forma el `return` debe de retornar el tipo de variable u objeto que se declaró.

### Ejemplo
```csharp
int Suma(int a, int b)
{
    int sum = a + b;
    return sum;
}
Console.WriteLine("La suma es igual a: {0}", Suma(2,2));
```
El resultado que obtendríamos del ejemplo sería: 
```bash
La suma es igual a: 4
``` 

## ¿Qué es una firma y cuál es su finalidad?
Las firmas se emplean para diferencia los **Métodos** que creamos para diferentes labores a la hora de trabajar con objetos, puesto que en algunos casos se requerirá menos parámetros para realizar una labor especifico . 
### Ejemplo
```csharp
void InsertPacient(string name,string 2ndname, string lastname, int tel, string address, int zipcode)
{
	Insert(name,2ndname,lastname, tel, address, zipcode);
}
void InserPacient(string name, string lastname, int tel, string address, int zipcode)
{
	Insert(name,lastname,tel,address,zipcode);
}
```
En este ejemplo se hace referencia al 
objeto **Pacient** y se crea un caso hipotético donde se busca insertarlo en una base de datos, en la cual algunos campos son opcionales, como lo son el segundo nombre, puesto que no todos tenemos un segundo nombre.


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