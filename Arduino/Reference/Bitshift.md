# Desplazamiento bit a bit izquierda (<<) y derecha (>>)

### Descripción

Hay dos operadores de desplazamiento en C++: el operador de desplazamiento a la izquierda **<<** y el operador de desplazamiento a la derecha **>>**. Estos operadores hacen que los bits del operando a la izquierda se desplacen en la dirección que indica el operador el número de posiciones que indica el operando de la derecha.


### Sintaxis

```variable << numero_de_bits```

```variable >> numero_de_bits```

### Parámetros

```variable - (byte, int, long) numero_de_bits integer <= 32```

### Ejemplo:

```
    int a = 5;        // en binario: 0000000000000101
    int b = a << 3;   // en binario: 0000000000101000, o 40 en decimal
    int c = b >> 3;   // en binario: 0000000000000101, o vuelta a 5 como al principio
```

Cuando se desplaza un valor x un número y de bits (x << y), los bits más a la izquierda se pierden, se desplazan fuera del número dejando de existir.

```
    int a = 5;        // en binario: 0000000000000101
    int b = a << 14;  // en binario: 0100000000000000 - el primer 1 de 101 se ha eliminado
    int c = b >> 14   // en binario: 0000000000000001
```

Si tienes la certeza que no se va a perder ningún uno desplazado al limbo de las matemáticas, una forma de entender el desplazamiento a la izquierda es multiplicar el operando de la izquierda por 2 elevado al operando de la derecha. Por ejemplo, para generar potencias de 2, se pueden usar las siguientes expresiones:

```
    1 <<  0  ==    1
    1 <<  1  ==    2
    1 <<  2  ==    4
    1 <<  3  ==    8
    ...
    1 <<  8  ==  256
    1 <<  9  ==  512
    1 << 10  == 1024
    ...
 ```
Cuando desplazas x a la derecha un número y de bits (x >> y), y el mayor bit en x es un 1, el comportamiento depende del tipo exacto de x. Si x es de tipo ```int``` , el bit más significativo es el bit de signo, que determina si x es negativo o no, como hemos visto antes. En ese caso, el signo se copia a otros bits.

```
    int x = -16;     // en binario: 1111111111110000
    int y = x >> 3;  // en binario: 1111111111111110
```

Este comportamiento, que se llama extensión de signo, suele no ser el comportamiento deseado. En su lugar, puedes querer ceros desplazados desde la izquierda. Resulta que las reglas para el desplazamiento a la derecha son diferentes para expresiones ```int``` sin signo, por lo que puedes usar un cambio de tipo de variable para evitar copiar unos a la izquierda:


```
    int x = -16;                   // en binario: 1111111111110000
    int y = (unsigned int)x >> 3;  // en binario: 0001111111111110
```

Si tienes cuidado para evitar la extensión de signo, puedes usar el operador de desplazamiento de signo a la derecha **>>** como forma de dividir entre potenccias de 2. Por ejemplo:

```
    int x = 1000;
    int y = x >> 3;   // división entera de 1000 entre 8, resultando y = 125.
```    
    
-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Bitshift)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.    
