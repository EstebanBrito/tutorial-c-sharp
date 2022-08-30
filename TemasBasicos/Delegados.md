Delegados en C
=========

## Definición 
###
Los delegados son una referencia a un método con la finalidad de enviarlos como parámetros determinados a otros métodos. 

> Un delegado es un objeto que contiene una referencia a un método. 

<br>
Hay que tener en cuenta algunas cosas acerca de los **delegados**:

* El método referenciado debe compartir el mismo tipo de valor y tipo de parametros declarados del delegado. No tienen que coincidir los nombres.
* No es un método como tal, por lo tanto no tiene enunciados a ejecutar.
* Puede ser declarado tanto fuera como dentro de una clase.

<br>

## Declaración

Los delegados utilizan la palabra clave ***delegate***. Se debe indicar cuáles son los parámetros y el tipo de retorno que requiere, por ejemplo:

    <tipo de acceso> delegate <tipo de retorno> <nombre del método>(<parametros de entrada>) 

Ejemplo de código:

    public delegate void mostrarDelegado(String valor);

## Ejemplo
       
Declarando un objeto delegado:
> `<nombre del delegado> <nombre del objeto> = <objeto de tipo clase>.<función>`

Una vez declaro, prodecemos a realizar el llamado de la función con los valores asignados en el objeto del delegado.

```C
class Programa
{
    //Delegado 
    public delegate int Operar(int x1, int x2);

    //función sumar 
    public int sumar(int x, int y){
        return x + y;
    }

    static void Main(string[] args){
        
        //Creamos el objeto de clase
        Programa objeto = new Programa();

        //Creamos objeto del delegado
        Operar objDelegado = objeto.sumar;

        //Mandamos a llamar a la función con sus respectivos valores
        Console.WriteLine(La suma de los valores utilizando delegado es: " + objDelegado(10, 5));"
    }
}
```
            
4. Una vez ejecutado el programa, la salida de datos sera:

    > La suma de los valores utilizando delegado es: 15 

***

## Funciones Lamda

<br>

Algo a tomar en cuenta es que los delegados que vayamos a crear pueden recibir un nombre, pero también existe opción de ser una **función anónima**. Un tipo de delegado que permite pasar un bloque de código como parametro de un delegado creado. Pero ¿como llamar una función que no tiene nombre?

Las Expresiones *lambda* son funciónes anonimas que permiten enviar parametros a un método y ser efectuada en el mismo. De esta forma, puede realizar el llamado de una función de forma directa. 

Como se menciono en la definicion de los **delegados**, estos pueden apuntar a otros métodos, pero también a una lambda; permitiendo definir un delegado previamente declarado a un objeto que coincida con los parametros y el mismo tipo de dato a devolver de una expresión *lambda*.

## Declaración

Definamos como es la estructura de una expresión *lambda* común y como es aplicada con los delegados:

* Expresión *lambda* sin delegado
        
        (parametros de entrada) => expresión | {bloque de secuencia}

    Ejemplo de una expresión *lambda* declarada para calcular el % de descuento en un producto:

        (precio, descuento) => precio - (precio * descuento / 100);

<br>

* Expresión *lambda* aplicada con delegado

        <nombre del delegado> <nombre de la función> = (parametros de entrada) = expresión {bloque de secuencia}
    
    Ejemplo aplicado con delegado para multiplicar dos valores:

        //Definimos un delegado
        delegate int ejemploDelegado(int x, int y);

        //Delegado defido con expresión *lambda*
        ejemploDelegado objetoDelegado = (x, y) => x * y;


Podemos notar que al aplicar las funciónes *lambda* con los delegados nos permiten reducir la sobrecarga de código, ya que se evita estar solo declarando objetos de tipo delegado, así como métodos independientes y logrando un mejor rendimiento. 