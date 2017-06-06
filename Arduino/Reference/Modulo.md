# % Resto - [modulo]

### Descripción

Calcula el resto cuando se divide un entero entre otro. Es útil cuando se quiere mantener una variable dentro de un rango (por ejemplo el tamaño de un vector).


### Sintaxis

```
resultado = dividendo % divisor
```

### Parámetros

**dividendo**: el número a dividir

**divisor**: el número por el que se divide

### Devuelve

el resto de la división

### Ejemplos

```Arduino
x = 7 % 5;   // x ahora es 2
x = 9 % 5;   // x ahora es 4
x = 5 % 5;   // x ahora es 0
x = 4 % 5;   // x ahora es 4
```

#### Ahora con código

```Arduino
/* actualiza un valor del vector cada vez que pasa por el bucle */

int valores[10];
int i = 0;

void setup() {}

void loop()
{
  valores[i] = analogRead(0);
  i = (i + 1) % 10;   // el operador sobrescribe la variable 
}
```

### Consejo

El operador resto no funciona con datos del tipo ```float```.

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Modulo)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
