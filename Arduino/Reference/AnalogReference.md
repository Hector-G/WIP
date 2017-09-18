# analogReference()

### Descripción

Configura el voltaje de referencia que se utiliza como entrada analógica (el valor máximo del rango de entrada). Las opciones son:

- DEFAULT: el valor por defecto es 5 voltios (en las placas Arduino de 5V) o 3.3 voltios (en las placas Arduino de 3.3V)
- INTERNAL: la referencia interna del chip, igual a 1.1 voltios en el ATmega168 o ATmega328 y 2.56 voltios en el ATmega8 (no disponible en el Arduino Mega)
- INTERNAL1V1: referencia predefinida de 1.1V (sólo Arduino Mega)
- INTERNAL2V56: referencia predefinida de 2.56V (sólo Arduino Mega)
- EXTERNAL: utiliza como referencia el voltaje aplicado en el pin AREF (sólo entre 0 y 5V)

### Sintaxis

analogReference(tipo)

### Parámetros

tipo: el tipo de referencia a usar (DEFAULT, INTERNAL, INTERNAL1V1, INTERNAL2V56, or EXTERNAL).

### Devuelve

Nada.

**Nota**

Al cambiar la referencia analógica, las primeras lecturas de analogRead() podrían no ser precisas.

**Precaución**

¡No utilizar ningún voltaje inferior a 0V o superior a 5V como referencia externa en el pin AREF! Para utilizar la referencia externa en el pin AREF, se debe configurar la referencia analógica como EXTERNAL antes de utilizar analogRead(). De lo contrario se cortocircuita el voltaje de referencia activo (generado internamente) y el del pin AREF, lo cual puede dañar el microcontrolador.

Como alternativa, se puede conectar el voltaje de referencia externo al pin AREF a través de una resistencia de 5K, lo cual permite alternar entre el voltaje de referencia interno y externo. Sin embargo hay que tener en cuenta que la resistencia afectará al voltaje de referencia ya que el pin AREF contiene una resistencia interna de 32K. Ambas forman un divisor de tensión, así, por ejemplo 2.5V en la resistencia dará un voltaje de 2.5 * 32 / (32 + 5) = ~2.2V en el pin AREF.


-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/AnalogReference)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
