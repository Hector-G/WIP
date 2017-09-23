# Constantes enteras

Las constantes enteras son números que se utilizan directamente en un programa, como por ejemplo 123. Por defecto, estos números se tratan como ```int``` pero se puede cambiar con los modificadores **U** y **L**.

Normalmente las constantes enteras se consideran números enteros en base 10 (decimal), pero se puede añadir prefijo para indicar que el número está en otra base.

|Base |Ejemplo |Prefijo|Comentario |
|---|---:|---|---|
|10 (decimal) |123 |   ninguno|   |
|2 (binario)| B1111011| 'B' inicial | sólo funciona con valores de 8 bit (0 a 255). Válido 0 y 1.|
|8 (octal) |0173| "0" inicial| Válido de 0 a 7 |     
|16 (hexadecimal) |0x7B| "0x" inicial| Válido de 0 a 9 y de A a F (a - f) |   
<br />
<br />

**Decimal** es base 10. Este es el sistema al que estamos acostumbrados a trabajar en matemáticas. Cualquier constante sin prefijo se considera que está representada en formato decimal.

**Ejemplo:**

```101     // igual que 101 decimal   ((1 * 10^2) + (0 * 10^1) + 1) ```
<br />
<br />

**Binario** es base 2. Sólo hay dos caracteres válidos, que son 0 y 1. Esto es, cualquier número en binario se representa mediante ceros y unos.

**Ejemplo:**

```B101    // igual que 5 decimal   ((1 * 2^2) + (0 * 2^1) + 1) ```

El prefijo binario **B** sólo funciona con bytes (8 bits) entre 0 (B0) y 255 (B11111111). Si es necesario introducir un `int` (16 bit) en formato binario, se puede hacer en dos pasos del siguiente modo:

```miInt = (B11001100 * 256) + B10101010;    // B11001100 es el byte de mayor peso ```
<br />
<br />

**Octal** es base 8. Son válidos los caracteres de 0 a 7. Los números en octal se indican con el prefijo "0".

**Ejemplo:**

``` 0101    // igual que 65 decimal   ((1 * 8^2) + (0 * 8^1) + 1)  ```

**Atención**  

Es posible generar un error difícil de depurar al incluir (de manera no intencionada) un cero delante de una constante, lo que causará que el comilador lo interprete como una constante en octal.
<br />
<br />

**Hexadecimal (o hex)** es base 16. Los caracteres válidos son de 0 a 9 y las letras entre A y F. A tiene el valor 10, B es 11, y así hasta F que vale 15. Los valores `hex` se indican con el prefijo "0x". Las letras A - F se pueden escribir indistintamente en mayúsculas o minúsculas.

**Ejemplo:**

```0x101   // igual que 257 decimal   ((1 * 16^2) + (0 * 16^1) + 1)```

## Modificadores U y L

or defecto, se trata una constante entera como un ```int``` con la consiguiente limitación de valores. Para especificar un entero con otro tio de datos, se añade un sufijo:

+ una 'u' o 'U' para forzar una constante sin signo (_unsigned_). Ejemplo: `33u`
+ una 'l' o 'L' para formar una constante de formato largo (_long_). Ejemplo: `100000L`
+ una 'ul' o 'UL' para forzar una constante larga sin signo (_unsigned long_). Ejemplo: `32767ul`

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/IntegerConstants)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
