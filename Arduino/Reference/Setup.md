# setup()

Se llama a la función ```setup()``` cuando arranca el sketch. Utilízala para inicializar variables, definir pines, utilizar librerías, etc. La función setup sólo se ejecuta una vez, al conectar la placa Arduino o al hacer un reset.

### Ejemplo

```Arduino 
int pinBoton = 3;

void setup()
{
  Serial.begin(9600);
  pinMode(pinBoton, INPUT);
}

void loop()
{
  // ...
}
```

\<link\>Reference Home


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Setup)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
