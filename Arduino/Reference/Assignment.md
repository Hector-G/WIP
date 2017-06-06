# = operador de asignación (signo igual simple)

Almacena el valor de la derecha del signo igual en la variable del lado izquierdo.

El signo igual simple se llama operador de asignación en el lenguaje C. No significa lo mismo que en álgebra donde indica una ecuación o igualdad. El operador de asignación indica al microcontrolador que evalue el valor o expresión a la derecha del signo igual, y lo almacene en la variable a la izquierda del signo igual.

### Ejemplo

```Arduino
 int valorSensor;                  // crear una variable tipo int que se llama valorSensor
 valorSensor = analogRead(0);       // guardar el valor (numérico) del voltaje de entrada del pin Analog0 en valorSensor
 ```
 
### Consejos

La variable a la izquierda del operador de asignación debe ser capaz de almacenar el valor deseado. Debe ser del mismo tipo de dato y lo suficientemente grande. De lo contrario el valor almacenado será incorrecto.

No confundir el operador de asignación ```=``` (signo igual simple) con el operador de comparación ```==``` (signo igual doble), que evalúa si dos expresiones son iguales.

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Assignment)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
