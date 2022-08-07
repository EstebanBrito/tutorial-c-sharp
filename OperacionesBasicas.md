# Operaciones básicas en C#.

Se le llama **operador** a un signo o símbolo, y sirven para identificar el tipo de cálculo a realizar sobre una expresión.

C# nos proporciona operadores, compatibles con tipos integrados y operaciones básicas, incluyendo los siguientes grupos:

* Operadores aritméticos
* Operadores de comparación.
* Operadores lógicos booleanos.
* Operadores bit a bit y de desplazamiento.
* Operadores de igualdad.

## Operadores aritméticos:

Los operadores aritméticos se utilizan para calcular el valor de dos o más números o para cambiar el signo de un número de tipo numéricos.

### Operandores unarios: incremento (++), decremento (--), más (+) y menos (-).

#### Más (+): devuelve el valor se su operando.

**Código:**
  ```c#
  int x = 4;
  Console.WriteLine(+x);
  ```

**Salida:**
  ```c#
  4
  ```

#### Menos (-): calcula la negación numérica del operando.

**Código:**
  ```c#
  int x = 4;
  Console.WriteLine(-x);
  ```

**Salida:**
  ```c#
  -4
  ```

### Operadores binarios: multiplicación (*), división (/), resto (%), suma (+) y resta (-).

#### Multiplicación (*): calcula el producto de sus operandos.

**1. Código:**
  ```c#
  int x = 5;
  int y = 2;
  Console.WriteLine(x * y);
  ```

**Salida:**
  ```c#
  10
  ```

**2. Código:**
  ```c#
  int x = 0.5;
  int y = 2.5;
  Console.WriteLine(x * y);
  ```

**Salida:**
  ```c#
  1.25
  ```

#### División (/): divide el operando izquierdo entre el derecho.

**1. Código:**
  ```c#
  int x = 13;
  int y = 5;
  Console.WriteLine(x / y);
  ```
  
**Salida:**
  ```c#
  2
  ```

**2. Código:**
  ```c#
  float x = 16.8;
  float y = 4.1;
  Console.WriteLine(x / y);
  ```
  
**Salida:**
  ```c#
  4.097561
  ```

Use **float**, **double** o **decimal** en ambos operadores para obtener el cociente de los dos operandos como número de punto flotante.

<!--Agrega también para qué sirve cuando los operandos son cadenas.-->

#### Suma (+): calcula la suma de sus operandos.

**1. Código:**
  ```c#
  int x = 5;
  int y = 4;
  Console.WriteLine(x + y);
  ```

**Salida:**
  ```c#
  9
  ```

**2. Código:**
  ```c#
  string word = "C#";
  Console.WriteLine("Bienvenido al curso de " + word);
  ```

**Salida:**
  ```c#
  Bienvenido al curso de C#
  ```

Use el operador (+) para **concatenar cadenas** y **delegados**.

#### Resta (-): resta el operando derecho del izquierdo.

**Código:**
  ```c#
  int x = 47;
  int y = 3;
  Console.WriteLine(x - y);
  ```

**Salida:**
  ```c#
  44
  ```

## Operadores de asignación:

Los operadores de asignación como su nombre lo indican asignan el valor de su operando derecho a una **variable**, **propiedad** o **elemento** de índice proporcionado por el operando izquierdo, como resultado se asigna el valor del operando izquierdo.

#### Asignación simple (=): almacena el valor del segundo operando en el objeto especificado por el primer operando.

**Código:**
  ```c#
  int number;
  number = 10;
  Console.WriteLine(number);
  ```

**Salida:**
  ```c#
  10
  ```

#### Asignación compuesta: (*=): multiplica ambos valores de los operandos y asigna el resultado al primer operando.

**Código:**
  ```c#
  int x = 10;
  x *= 2;
  Console.WriteLine(x);
  ```

**Salida:**
  ```c#
  20
  ```

#### Asignación de división (/=): divide ambos valores de los operandos y asigna el resultado al primer operando.

**Código:**
  ```c#
  int x = 20;
  x /= 4;
  Console.WriteLine(x);
  ```

**Salida:**
  ```c#
  5
  ```

#### Asignación de resta (-=): resta ambos valores de los operandos.

**Código:**
  ```c#
  int x = 14;
  x -= 4;
  Console.WriteLine(x);
  ```

**Salida:**
  ```c#
  10
  ```
Use el operador (-=) para especificar un **método de controlador de eventos**, cuando se trate de eliminar una baja de un evento.

#### Asignación de suma (+=): suma ambos valores de los operandos.

**Código:**
  ```c#
  int x = 5;
  x += 9;
  Console.WriteLine(x);
  ```

**Salida:**
  ```c#
  14
  ```

Use el operador (+=) para especificar un **método de controlador de eventos**, cuando se trate de una suscripción de eventos.

## Operadores lógicos booleanos

Los operadores lógicos booleanos son **palabras** o **símbolos** que se utilizan para realizar operaciones de forma lógica sobre sus operandos. 

### Operadores binarios (AND lógico condicional) y (OR lógico condicional).

#### AND lógico condicional (&&): calcula el operador AND lógico de sus operandos.

**Código:**
  ```c#
  bool x = true; 
  bool y = true;
  Console.WriteLine(x && y);
  ```

**Salida:**
  ```c#
  True
  ```

Genera true, si x y y se evalúa como true, y false, si x se evalúa como true y y como false.

#### OR lógico condicional (||): calcula el operador OR lógico de sus operandos.

**Código:**
  ```c#
  bool x = false; 
  bool y = false;
  Console.WriteLine(x || y);
  ```

**Salida:**
  ```c#
  False
  ```

Estos operadores evalúan el operando derecho sólo si es necesario.

### Operadores de igualdad: comprueban si los operadores son iguales.

#### Igualdad (==): devuelve true si sus operadores son iguales de lo contrario devuelve false.

**Código:**
  ```c#
  int x = 1 + 2 +3;
  int y = 6;
  Console.WriteLine(x == y);
  ```

**Salida:**
  ```c#
  True
  ```

#### Desigualdad (!=): devuelve true si sus operadores son iguales de lo contrario devuelve false.

**Código:**
  ```c#
  int x = 1 + 2 +3;
  int y = 6;
  Console.WriteLine(x != y);
  ```

**Salida:**
  ```c#
  True
  ```

#### Negación lógica (!): calcula la negación lógica de su operando.

**Código:**
  ```c#
  bool x = false;
  Console.WriteLine(!x);
  ```

**Salida:**
  ```c#
  True
  ```

Genera true, si el operando se evalúa como false, y false, si el operando se evalúa como true.

### Otros operaadores:

#### Operador condicional o ternario (?:): evalúa una expresión booleana y devuelve el resultado de las dos expresiones, dependiendo de si se evalua como true o false.

**Código:**
  ```c#
  int age = 17;
  string message = string.Empty;

  if (age > 18)
    message = "Eres legal";
  else
    message = "Eres ilegal";

  message = age>18 ? "Eres legal" : "Eres ilegal";
  Console.WriteLine(message);
  ```

**Salida:**
  ```c#
  Eres ilegal
  ```