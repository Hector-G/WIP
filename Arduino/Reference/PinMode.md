# pinMode()

### Descripción

Configura el pin especificado para que se comporte bien como entrada o bien como salida. Ver la descripción de los pines digitales para obtener más detalles acerca de la funcionalidad de los pines.

A partir de Arduino 1.0.1, es posible activar las resistencias internas de _pullup_ con el modo ```INPUT_PULLUP```. El modo ```INPUT``` desactiva explícitamente las resistencias de _pullup_ .


### Sintaxis

pinMode(pin, modo)

### Parámetros

pin: el número del pin que se desea modificar.

modo: INPUT, OUTPUT, o INPUT_PULLUP.

### Devuelve

Nada

### Ejemplo


```Arduino
int pinLed = 13;                 // LED conectado al pin digital 13

void setup()
{
  pinMode(pinLed, OUTPUT);      // establece el pin como salida
}

void loop()
{
  digitalWrite(pinLed, HIGH);   // enciende el LED
  delay(1000);                  // espera un segundo
  digitalWrite(pinLed, LOW);    // apaga el LED
  delay(1000);                  // espera un segundo
}
```

**Nota**

Los pines analógicos se pueden utilizar como pines digitales, nombrándolos A0, A1, etc.

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Else)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
