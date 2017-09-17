# digitalRead()

### Descripción

Lee el valor del pin digital especificado, que puede ser ```HIGH``` o ```LOW```.

### Sintaxis

digitalRead(pin)

### Parámetros

pin: el número del pin que se quiere leer (int)

### Devuelve

```HIGH``` o ```LOW```

### Ejemplo


```Arduino

int pinLED = 13; // LED conectado al pin digital 13
int pinBoton = 7;   // botón conectado al pin digital 7
int val = 0;     // variable para almacenar el valor leído

void setup()
{
  pinMode(pinLED, OUTPUT);      // pin digital 13 como salida
  pinMode(pinBoton, INPUT);      // pin digital 7 como entrada
}

void loop()
{
  val = digitalRead(pinBoton);   // leer el pin de entrada
  digitalWrite(pinLED, val);    // copiar el valor del botón en el LED
}
```

**NOTA**

Si el pin no está conectado a nada, digitalRead() puede devolver de forma impredecible cualquiera de los dos valores (```HIGH``` o ```LOW```), además el valor puede cambiar aleatoriamente.


Los pines analógicos se pueden utilizar como pines digitales, nombrándolos A0, A1, etc.


-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/DigitalRead)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
