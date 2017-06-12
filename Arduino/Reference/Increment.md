# ++ (incremento) / -- (decremento)

### Descripción

Incrementa o decrementa una variable

### Sintaxis

```
  x++; //incrementa x en una unidad y devuelve el antiguo valor de x
  ++x; //incrementa x en una unidad y devuelve el nuevo valor de x
```

```
 x--; //decrementa x en una unidad y devuelve el antiguo valor de x
 --x; //decrementa x en una unidad y devuelve el nuevo valor de x
```

### Parámetros

**x** : un entero ( ```int``` ) o ```long``` . Puede ser ``` unsigned ```.

#### Devuelve

El valor original o el nuevo valor incrementado/decrementado de la variable.


### Ejemplos

```Arduino
x = 2;
y = ++x;      // x contiene ahora 3, y contiene 3
y = x--;      // x vuelve a contener 2, y sigue conteniendo 3
```

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Increment)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
