# continue

Salta el resto de la iteración actual dentro de un bucle (```do```, ```for``` o ```while```). Continúa comprobando la condición del bucle, en la siguiente iteración.

### Ejemplo

```Arduino
for (x = 0; x < 255; x ++)
{
    if (x > 40 && x < 120){      // Esto hará que se salte los valores entre 40 y 120
        continue;
    }

    analogWrite(pinPWM, x);
    delay(50);
}
```

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Continue)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
