# do ... while

Este bucle funciona igual que el bucle ```while```, sólo que la condición se comprueba al final del bucle. Por tanto el bucle ```do``` se ejecutará al menos una vez, indistintamente si se cumple la condición o no.

```Arduino
do
{
    // bloque de código
} while (condición);
```

### Ejemplo

```Arduino
do
{
  delay(50);          // Esperar a que los sensores se estabilicen
  x = leerSensores();  // comprobar los sensores

} while (x < 100);
```
El programa leerá los sensores y continuará haciéndolo hasta que **x** deje de tener un valor menor a 100.  

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/DoWhile)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
