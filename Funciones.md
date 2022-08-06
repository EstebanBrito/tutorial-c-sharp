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
Una función puede retornar una variedad de elementos, como lo son objetos, tipo de variables, etc. Para retornar un elemento en una variable se debe de cambiar la palabra clave `void` por el tipo de dato que deseamos retornar por ejemplo un `int` le indicaría al compilador que la función debe de retornar un entero. La palabra clave `return` es la que se encarga de regresar el valor que debe de retornar nuestra función, pero es de suma importancia denotar los siguientes puntos:

* El momento en el que el compilador lee la línea donde se encuentra el `return` termina la ejecución de la función y regresa al código principal, esto significa que si tenemos comandos delante del `return` estos no se ejecutaran.
* El tipo de dato a retornar debe de ser el apropiado, por ejemplo, si se retorna un valor flotante en una función que retorna valores enteros, esto implicara un error de compilación a la hora de ejecutar el código.


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
Las firmas son un componente de la función que define sus entradas y salidas, con esto términos se hace referencia a los parámetros junto con su tipo y el valor de retorno junto con su tipo. En el siguiente ejemplo se puede notar una función con los siguientes elementos:
* `int`
* `multi`
* `(int a, int b)`

`int` es el componente de la firma que indica que se debe de retornar un valor y este debe de ser entero.

`multi` es el componente de la firma que indica el nombre de la función.

`(int a, int b)` es el componente de la firma que indica que la función tiene parámetros.


### Ejemplo
```csharp
int multi(int a, int b)
{
    int x = a * b;
    return x;
}
```

## ¿Por qué es integral el uso de las funciones?
Existen varias razones por la cual es esencial hacer uso de funciones, pero se resume en los siguientes puntos:
* **Organización**. Las funciones nos permiten tener un área de trabajo menos amontonada, puesto que las funciones se pueden separar del código principal, permitiéndonos crear pequeñas partes de nuestro programa.
* **Reusabilidad**. La reusabilidad que las funciones nos aportan es una de las ventajas más notables, debido a que podemos usar una función repetidamente para desarrollar una funcionalidad.
* **Testear**. Es más sencillo testear un bloque de código en una función, ya que como esta se encuentra separada del código principal, nos permite testearlo y expurgarlo de cualquier tipo de error sin tener que preocuparnos de algún cambio en el principal.