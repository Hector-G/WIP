# loop()

Después de crear la función ```setup()```, la cual inicializa y define los valores iniciales, la función ```loop()``` (bucle, en inglés) se repite consecutivamente, permitiendo al programa cambiar y responder. Utilízala para controlar la placa Arduino.

### Ejemplo

```Arduino
const int pinBoton = 3;

// en setup iniciamos la comunicación serie y el pin del botón
void setup()
{
  Serial.begin(9600);
  pinMode(pinBoton, INPUT);
}

// loop comprueba el pin del botón cada vez,
// y envía por serie si está pulsado
void loop()
{
  if (digitalRead(pinBoton) == HIGH)
    Serial.write('H');
  else
    Serial.write('L');

  delay(1000);
}
```

\<link\>Reference Home


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Loop)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
