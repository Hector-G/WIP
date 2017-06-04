# Bucles while

### Description

Los bucles ```while``` se ejecutan de forma continua, e infinita, hasta que la condición dentro del paréntesis deja de ser cierta. En algún momento algo debe cambiar la variable a comprobar, de lo contrario el programa nunca saldrá del bucle. Ese algo puede ser código, como una variable incrementada, o una condición externa, como la señal de un sensor. 

### Sintaxis

```Arduino
while(expresión){
  // instrucciones
}
```

### Parámetros

**expresión**: Una condición en C (booleana) cuyo resultado sea verdadero o falso

#### Ejemplo

```Arduino
var = 0;
while(var < 200){
  // Hacer algo repetitivo 200 veces
  var++;
}
```

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/While)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
