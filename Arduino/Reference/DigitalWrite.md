# digitalWrite()

### Descripción

Escribe el valor ```HIGH``` o ```LOW``` en un pin digital.

Si el pin está configurado como ```OUTPUT``` (salida) mediante pinMode(), el voltaje en el pin tomará el valor correspondiente: ```HIGH``` a 5V ( o 3.3V en las placas que funcionan a 3.3V), y ```LOW``` a 0V (GND).

Si el pin está configurado como ```INPUT``` (entrada), digitalWrite() activará (```HIGH```) o desactivará (```LOW```) el _pullup_ interno en el pin de entrada. Se recomienda definir ```INPUT_PULLUP``` en pinMode() para activar la resistencia interna de _pullup_. 

**NOTA** : Si no se define el pinMode() como ```OUTPUT``` (salida), y se conecta un LED a un pin, cuando se utilice ```digitalWrite(HIGH)``` el LED parecerá atenuado. Si no se define explícitamente el pinMode(), digitalWrite() tendrá activada la resistencia interna de _pullup_, que actúa como un limitador de corriente. 

### Sintaxis

digitalWrite(pin, valor)

### Parámetros

pin: el número del pin

valor: HIGH o LOW

### Devuelve

Nada

### Ejemplo

 ```Arduino
int pinLED = 13;                 // LED conectado al pin digital 13

void setup()
{
  pinMode(pinLED, OUTPUT);      // pin digital como salida
}

void loop()
{
  digitalWrite(pinLED, HIGH);   // enciende el LED
  delay(1000);                  // espera un segundo
  digitalWrite(pinLED, LOW);    // apaga el LED
  delay(1000);                  // espera un segundo
}
```

**NOTA**

Los pines analógicos se pueden usar como pines digitales, nombrándolos como A0, A1, etc.

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Else)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
