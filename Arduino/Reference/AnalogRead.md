# analogRead()

### Descripción

Lee el valor del pin analógico especificado. La placa Arduino contiene un conversor analógico-digital de 10 bit y 6 canales (8 canales en el Mini y Nano, 16 en el Mega). Esto significa que mapeará voltajes de entrada entre 0 y 5 voltios como valores enteros entre 0 y 1023. Por tanto se obtiene una resolución de 5V / 1024 o 0.0049V (4.9mV) por división. La resolución del rango de entrada se puede modificar con analogReference().

Se requiere unos 100 microsegundos (0.0001 s) para leer la entrada analógica, por lo que la velocidad máxima de lectura es de aproximadamente 10000 veces por segundo.

### Sintaxis

analogRead(pin)

### Parámetros

pin: el número del pin analógico que se quiere leer (de 0 a 5 en la mayoría de placas, de 0 a 7 en Mini y Nano, de 0 a 15 en Mega)

### Devuelve

int (0 a 1023)

**Nota**

Si el pin analógico no está conectado a nada, el valor de lectura que devuelve analogRead() fluctuará en base a diversos factores (valores de otras entradas, la proximidad de tu mano a la placa, etc.)

### Ejemplo

 
```Arduino
  
int analogPin = 3;     // el pin de enmedio del potenciometro conectado al pin 3
                       // los otros dos pines van conectados a GND y 5V respectivamente

int val = 0;           // variable para almacenar el valor leido



void setup()

{

  Serial.begin(9600);          //  configurar serial

}



void loop()

{

  val = analogRead(analogPin);    // leer el pin de entrada

  Serial.println(val);             // mostrar valor por consola

}

  ```



-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/AnalogRead)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
