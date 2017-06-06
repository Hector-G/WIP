# #include

```#include``` se utiliza para incluir librerías externas en el programa. Esto da acceso a una gran cantidad de librerías estándar de C (conjuntos de funciones preestablecidas) así como librerías específicas para Arduino.

La referencia para las librerías AVR en C (AVR hace referencia a los chips de Atmel en los que se basa Arduino) la puedes consultar [aquí](http://www.nongnu.org/avr-libc/user-manual/modules.html) (en inglés).

Nota que ```#include```, de forma similar a ```#define```, no lleva punto y coma al final, y el compilador mostrará errores si se utiliza.

### Ejemplo

Este ejemplo incluye una librería que se usa para introducir datos en la memoria flash del programa en vez de la ram. De este modo se ahorra espacio ram para la memoria dinámica y hace que las tablas de datos sean más prácticas.

```Arduino
#include <avr/pgmspace.h> // incluir la librería

// creamos una tabla de datos
prog_uint16_t misConstantes[] PROGMEM = {0, 21140, 702  , 9128,  0, 25764, 8456,
0,0,0,0,0,0,0,0,29810,8968,29762,29762,4500};
```

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Include)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
