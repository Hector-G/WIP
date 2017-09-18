# analogWrite()

### Descripción

Escribe un valor analógico (onda PWM) en un pin. Se puede utilizar para encender un LED con brillo variable o mover un motor a distintas velocidades. Tras llamar a analogWrite(), el pin generará una onda cuadrada continua con el ciclo de trabajo especificado hasta que se vuelva a llamar a analogWrite() (o digitalRead() o digitalWrite() en el mismo pin). La frecuencia de la señal PWM en la mayoría de pines es aroximadamente 490 Hz. En el Uno y similares, los pines 5 y 6 tienen una frecuencia aproximada de 980 Hz. Los pines 3 y 11 del Leonardo también funcionan a 980 Hz.

En la mayoría de las placas Arduino (con el ATmega168 o ATmega328), esta función es válida para los pines 3, 5, 6, 9, 10 y 11. En el Arduino Mega, funciona con los pines 2 -13 y 44 -46. Las placas más antiguas con el ATmega8 sólo admiten analogWrite() en los pines 9, 10 y 11.

El Arduino Due admite analogWrite() en los pines 2 a 13, además de los pines DAC0 y DAC1. A diferencia de los pines PWM, DAC0 y DAC1 son conversores digital a analógico, generando una salida analógica real.

No es necesario llamar a pinMode() para configurar el pin como salida antes de usar analogWrite().

La función analogWrite() no tiene nada que ver con los pines analógicos o con la función analogRead().


### Sintaxis

analogWrite(pin, valor)

### Parámetros

pin: el pin a escribir.

valor: el ciclo de trabajo : entre 0 (siempre apagado) y 255 (siempre encendido).

### Devuelve

Nada.

**Notas**

El PWM generado en los pines 5 y 6 puede tener mayor ciclo de trabajo del esperado. Esto es por la interacción entre las funciones millis() y delay(), que comparten el mismo temporizador interno para generar dichas salidas PWM. Este efecto se nota más en ciclos de trabajo bajos (entre 0 y 10) y puede resultar que no llegue a apagarse completamente con un valor 0 en los pines 5 y 6.

**Ejemplo**

Transfiere al LED un valor proporcional a la lectura del potenciómetro.
 
```Arduino
  
int pinLED = 9;      // LED conectado al pin digital 9

int analogPin = 3;   // potenciómetro conectado al pin analógico 3

int val = 0;         // variable para almacenar el valor leído


void setup()

{

  pinMode(pinLED, OUTPUT);   // pin como salida

}



void loop()

{

  val = analogRead(analogPin);   // leer el pin de entrada

  analogWrite(pinLED, val / 4);  // analogRead va de 0 a 1023, mientras que analogWrite va de 0 a 255 (es justo el cuádruple)

}

```   


-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/AnalogWrite)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
