# Constantes

Las constantes son expresiones predefinidas en el lenguaje Arduino. Se emplean para hacer que los programas sean más fáciles de leer. Podemos clasificar las constantes en grupos:

## Niveles lógicos: true y false (booleanas)

Hay dos constantes que representan verdadero y falso: ```true``` y ```false```

### false

```false``` (falso) es la más fácil de definir de las dos. Simplemente se define como 0 (cero).

### true

```true``` (verdadero) se define a menudo como 1, lo cual es correcto, pero tiene una definición más amplia. Cualquier entero con valor distinto a cero es ```true```, en el sentido booleano. Así -1, 2 y -200 también serían ```true```.

**Nota**. Las constantes ```true``` y ```false``` se escriben en minúsculas a diferencia de ```HIGH```,  ```LOW```, ```INPUT``` y ```OUTPUT```.

## Definición de los estados de los pines: HIGH y LOW

Cuando escribimos en un pin digital sólo hay dos valores posibles: ```HIGH``` y ```LOW```.

### HIGH

El significado de ```HIGH``` (refiriéndose a un pin) es un poco distinto dependiendo si el pin está en modo ```INPUT``` o ```OUTPUT```. Cuando un pin está configurado como ```INPUT``` (entrada) utilizando pinMode(), y se lee con digitalRead(), Arduino devolverá ```HIGH``` si:

  - se detecta en el pin un voltaje mayor a 3.0V (placas de 5V)
  - se detecta en el pin un voltaje mayor a 2.0V (placas de 3.3V)

Un pin se puede configurar también como ```OUTPUT``` (salida) con pinMode() y escribirle ```HIGH``` con digitalWrite(), el pin estará a:

  - 5 voltios (placas de 5V)
  - 3.3 voltios (placas de 3.3V)
  
En este estado puede emitir corriente, por ejemplo para encender un LED que lleva conectada una resistencia en serie hasta GND.

### LOW

El significado de ```LOW``` también cambia dependiendo si el pin está configurado como ```OUTPUT``` o como ```INPUT```. Cuando un pin se configura como ```INPUT``` (entrada) mediante pinMode() y se lee con digitalRead(), Arduino devolverá ```LOW``` si:

  - se detecta en el pin un voltaje inferior a 1.5V (placas de 5V)
  - se detecta en el pin un voltaje inferior a 1.0V (placas de 3.3V)
  
Cuando se configura un pin como ```OUTPUT``` (salida) mediante pinMode() y se escribe ```LOW``` con digitalWrite(), el pin se pone a 0 voltios (tanto en placas de 5V como de 3.3V). En este estado puede drenar corriente, por ejemplo encender un LED conectado a una resistencia en serie a +5V (o +3.3V).


## Definición de los modos de los pines: INPUT, INPUT_PULLUP y OUTPUT

Los pines digitales se pueden usar como salidas (```OUTPUT```), entradas (```INPUT```) o entradas con resistencia _pullup_ (```INPUT_PULLUP```). Al cambiar un pin con pinMode() cambia el comportamiento eléctrico del pin.

### Pines configurados como ```INPUT```

Se dice que los pines configurados como entradas (```INPUT```) tienen estado de alta impedancia. Los pines configurados en ```INPUT``` requieren muy poca corriente del circuito que están leyendo, equivaliendo a una resistencia de 100 Megaohm conectada en serie con el pin. Esto hace que sea práctico para leer un sensor.

Si configuras un pin como ```INPUT``` y estás leyendo un interruptor, cuando el interruptor se encuentre en estado abierto la entrada quedará "flotando", lo cual genera resultados impredecibles. Para asegurar una lectura correcta del interruptor abierto, se debe usar una resistencia de _pullup_ o _pulldown_. La finalidad de estas resistencias es forzar el pin a un estado conocido cuando el interruptor esté abierto. Normalmente se usa una resistencia de 10K, que es lo suficientemente baja para evitar una entrada flotante, pero al mismo tiempo es lo suficientemente alta como para no drenar demasiada corriente cuando se cierra el circuito.

Si se utiliza una resistencia de _pulldown_, el pin de entrada estará en ```LOW``` cuando el interruptor esté abierto y ```HIGH```cuando el interruptor esté cerrado.

Si se utiliza una resistencia de _pullup_, el pin de entrada estará en ```HIGH``` cuando el interruptor esté abierto y ```LOW```cuando el interruptor esté cerrado.

### Pines configurados como ```INPUT_PULLUP```

El microcontrolador Atmega de Arduino tiene resistencias de _pullup_ internas (resistencias conectadas a la alimentación de manera interna) a las cuales se puede acceder. Si prefieres utilizarlas en vez de conectar resistencias externas, puedes activarlas con ```INPUT_PULLUP``` en pinMode().

Los pines configurados como entradas mediante ```INPUT``` o ```INPUT_PULLUP``` se pueden dañar o destruir si se conectan a voltajes negativos (por debajo del valor de GND) o por encima del voltaje de alimentación (5V o 3V).

### Pines configurados como ```OUTPUT```

Se dice que los pines configurados como salidas (```OUTPUT```) tienen estado de baja impedancia. Esto significa que pueden dar una cantidad considerable de corriente a otros circuitos. Los pines del Atmega pueden dar - o drenar - hasta 40 mA (miliamperios) de corriente a otros aparatos/circuitos. Esto los hace especialmente útiles para alimentar LED porque los LED normalmente consumen menos de 40 mA. Cargas superiores a 40 mA (como por ejemplo un motor) requieren un transistor u otro circuito adicional.

Los pines configurados como salidas se pueden dañar o destruir si se conectan tanto a la vía de GND como a la de alimentación positiva.

## Definición de componentes de fábrica: LED_BUILTIN

La mayoría de las placas Arduino llevan un LED y una resistencia en serie incorporados, conectados a uno de los pines. La constante ```LED_BUILTIN``` es el número del pin al cual está conectado el LED en susodicha placa. En la mayoría de casos es el pin digital 13.

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Constants)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.


