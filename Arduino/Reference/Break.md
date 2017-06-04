# break

Se utiliza ```break``` para salir de un bucle ```do```,```while``` o ```for```, ignorando las condiciones del propio bucle. También se utiliza para salir de la expresión ```switch```.

### Example
```Arduino
for (x = 0; x < 255; x ++)
{
    analogWrite(pinPWM, x);
    sens = analogRead(pinSensor);  
    if (sens > limite){      // salir a la señal del sensor
       x = 0;
       break;
    }  
    delay(50);
}
```

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Break)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
