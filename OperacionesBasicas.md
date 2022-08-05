# **Operaciones Básicas**

C# proporciona operadores. Compatibles con tipos incorporados y operaciones básicas, incluyendo los siguientes grupos:

## Operadores aritméticos:

Operaciones aritmeticas con operandos númericos.

* Operando unarios: ++ (incremento), -- (decremento), + (más) y - (menos)
    * Más (+): devuelve el valor se su operando.

        **Código:**
        ```c#
        int a = 4;
        Console.WriteLine(+a);
        ```
        **Salida:**
        ```c#
        4
        ```
    * Menos (-): calcula la negación numérica del operando.

        **1. Código:**
        ```c#
        int a = 4;
        int b = -a;
        Console.WriteLine(-b);
        ```
        **Salida:**
        ```c#
        -4
        ```
        **2. Código:**
        ```c#
        int a = -4;
        int b = -a;
        Console.WriteLine(b);
        ```
        **Salida:**
        ```c#
        4
        ```
* Operadores binarios: * (multiplicación), / (división), % (resto), + (suma) y - (resta)
    * Multiplicación (*): calcula el producto de sus operandos.

        **1. Código:**
        ```c#
        int a = 5;
        int b = 2;
        Console.WriteLine(a * b);
        ```
        **Salida:**
        ```c#
        10
        ```
        **2. Código:**
        ```c#
        int a = 0.5;
        int b = 2.5;
        Console.WriteLine(a * b);
        ```
        **Salida:**
        ```c#
        1.25
        ```
    * División (/): divide el operando izquierdo entre el derecho.

        **Código:**
        ```c#
        int a = 13;
        int b = 5;
        Console.WriteLine(a / b);
        ```
        **Salida:**
        ```c#
        2
        ```

    Use **float**, **double** o **decimal** para obtener el cociente de los dos operandos como número de punto flotante.

    * Suma (+): calcula la suma de sus operandos.

        **Código:**
        ```c#
        int a = 5;
        int b = 4;
        Console.WriteLine(a + b);
        ```
        **Salida:**
        ```c#
        9
        ```

    Use el operador (+) para **concatenar cadenas** y **delegados**.

    * Resta (-): resta el operando derecho del izquierdo.

        **Código:**
        ```c#
        int a = 47;
        int b = 3;
        Console.WriteLine(a - b);
        ```
        **Salida:**
        ```c#
        44
        ```

## Operadores de asignación:

  * Asignación simple (=): almacena el valor del segundo operando en el objeto especificado por el primer operando.

  * Asignación compuesta: (*=): multiplica ambos valores de los operandos.

  * Asignación de resta (-=): resta ambos valores de los operandos.

## Operadores lógicos booleanos

Operaciones lógicas con los operandos bool:

  * Operador unario (negación lógica).

  * Operadores binarios (AND lógico), (OR lógico) y (OR exclusivo lógico).

    Esos operadores siempre evalúan ambos operandos.

  * Operadores binarios (AND lógico condicional) y (OR lógico condicional).

    * AND lógico condicional (&&): calcula el operador AND lógico de sus operandos.

    Genera true, si x y y se evalúa como true, y false, si x se evalúa como true y y como false.

    * OR lógico condicional (||): calculoa el operador OR lógico de sus operandos.
    
    Genera true, si x y y se evalúa como true, y false, si x se evalúa como true y y como false.

    Esos operadores evalúan el operando derecho sólo si es necesario.

    * Igualdad (==): devuelve true si sus operadores son iguales de lo contrario devuelve false.

    * Desigualdad (!=): devuelve true si sus operadores son iguales de lo contrario devuelve false.

    * Negación lógico (!): calcula la negación lógica de su operando.

    Genera true, si el operando se evalúa como false, y false, si el operando se evalúa como true.