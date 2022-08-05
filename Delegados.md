Delegados
=========

## Definicion 

Se define como un tipo que permite declarar una variable/argumentos que apunta a otro método; siendo esto una referencia a otro método cualquiera que sea **compatible**, y encapsulandolo de forma segura.

> Un delegado es un objeto que contiene una referencia a un método. 

<br>

Hay que tener en cuenta algunas cosas acerca de los **delegados**
* **compatible**: El metodo que apunta el delegado debe compartir el mismo tipo de retorno y tipo de parametros declarados previamente. No tienen que coincidir los nombres.
* No es un metodo como tal, por lo tanto no tiene enunciados a ejecutar.
* Puede ser declarado tanto fuera como dentro de una clase.

<br>

## Declaracion

Para crear un delegado es necesario utilizar la palabra clave ***delegate***, asi como indicar cuáles son los parámetros y el tipo de retorno que se requiere, por ejemplo:

    <tipo de acceso> delegate <tipo de retorno> <nombre del metodo>(<parametros de entrada>) 

Traducido en un ejemplo de codigo se expresa:

    public delegate void mostrarDelegado(String valor);

Realicemos un ejemplo para que quede mas claro paso a paso.

### Ejemplo

Vamos a realizar la suma de dos numeros:

1. En una clase, declaremos un delegado de tipo entero con dos parametros del mismo. 

        class Programa
        {
            //metodo delegado 
            public delegate int Operar(int x1, int x2);

            static void Main(string[] args){
            }

        }

2. Creamos una funcion llamada "suma" que, como el metodo delegado, es de tipo entero y cuenta con dos atributos del mismo tipo, que nos devuelva la suma de las cantidades a recibir. 

        class Programa
        {
            //metodo delegado 
            public delegate int Operar(int x1, int x2);

            //funcion sumar 
            public int sumar(int x, int y){
                return x + y;
            }


            static void Main(string[] args){
            }

        }

    Como se menciono anteriormente, las funciones a las que el metodo delegado va a referenciar no requiere que tengan el mismo nombre en la funcion o en los parametros.

3.  Ahora veremos la forma convencional del llamado de una funcion y en como llamara a traves del delegado. Recordemos que, para el llamado de una funcion es necesario crear un objeto

    3.1 Forma convencional:
        
    + Con el objeto asigno, realizamos un llamado a la funcion "sumar" asignandole dos valores. 

        
            class Programa
            {
                //metodo delegado 
                public delegate int Operar(int x1, int x2);

                //funcion sumar 
                public int sumar(int x, int y){
                    return x + y;
                }


                static void Main(string[] args){
                    
                    //Creamos el objeto de clase
                    Programa objeto = new Programa();

                    //Mandamos a llamar a la funcion con sus respectivos valores
                    Console.WriteLine("La suma de los valores es: " + objeto.sumar(10, 5));
            }
    
    <br>
    
    3.2 Forma delegado
    + Asi como un objeto, tenemos que definir un nuevo objeto del tipo delegar en el cual le agregamos la referencia de la funcion a utilizar. 
        
        Declarando un objeto delegado:
        > `<nombre del delegado> <nombre del objeto> = <objeto de tipo clase>.<funcion>`

        Una vez declaro, prodecemos a realizar el llamado de la funcion con los valores asignado en el objeto del delegado.

            class Programa
            {
                //metodo delegado 
                public delegate int Operar(int x1, int x2);

                //funcion sumar 
                public int sumar(int x, int y){
                    return x + y;
                }

                static void Main(string[] args){
                    
                    //Creamos el objeto de clase
                    Programa objeto = new Programa();

                    //Creamos objeto del delegado
                    Operar objDelegado = objeto.sumar;

                    //Mandamos a llamar a la funcion con sus respectivos valores
                    Console.WriteLine(La suma de los valores utilizando delegado es: " + delegado(10, 5));
            }
            
4. Una vez ejecutado el programa, la salida de datos sera:

    Forma convencional
        
        La suma de los valores es: 15 

    Forma delegado

        La suma de los valores utilizando delegado es: 15 














