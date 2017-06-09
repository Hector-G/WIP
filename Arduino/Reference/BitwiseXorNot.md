# Negación bit a bit (~)

El operador bit a bit de negación _NOT_ en C++ utiliza el carácte tilde **~** . A diferencia de los operadores **&** y **|** , el operador bit a bit _NOT_ se aplica únicamente al operando de su derecha. Lo que hace es cambiar el bit por su opuesto: convierte 0 en 1 y 1 en 0. Por ejemplo:

```
    0  1    operando 1
   ----------
    1  0   ~ operando 1
    
    
    int a = 103;    // en binario:  0000000001100111
    int b = ~a;     // en binario:  1111111110011000        en decimal: -104 
    
```

Tal vez te sorprenda ver que el resultado es un número negativo. Esto es porque el bit más significativo (el que está más a la izquierda) en una variable tipo ```int``` representa el signo. Este bit se llama también bit de signo. Si el bit es 1, el número es negativo. Para saber más sobre codificación de signos, puedes echar un vistazo al [artículo en Wikipedia sobre complemento a dos](https://es.wikipedia.org/wiki/Complemento_a_dos).

Es interesante saber que para cualquier entero ```x```, ```~x``` es lo mismo que ```-x-1``` .

En multiplicaciones, el bit de signo puede causar alguna sorpresa inesperada.

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/If)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
