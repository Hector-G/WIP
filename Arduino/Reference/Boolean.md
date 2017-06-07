# Operadores Booleanos

Se pueden utilizar en la condición de la expresión ```if``` .

### && (Y lógico)

Se cumple ( ```true``` ) si ambos operandos son ```true```

```Arduino
if (digitalRead(2) == HIGH  && digitalRead(3) == HIGH) { // leer dos interruptores 
  // ...
} 
```
Sólo se cumple si ambos son ```HIGH```


### || (O lógico)

Se cumple ( ```true``` ) si al menos uno de los operandos es ```true```

```Arduino
if (x > 0 || y > 0) {
  // ...
} 
```

es ```true``` si bien ```x``` o bien ```y``` es mayor que 0 (o también si ambos son mayor que 0).

### ! (negación)

Se cumple ( ```true``` ) el operando es ```false```

```Arduino
if (!x) { 
  // ...
} 
```

es ```true``` cuando ```x``` es ```false``` (es decir, cuando vale 0).

### Atención

Cuidado con no confundir el operador booleano **```&&```** (**Y**) con el operador bit a bit **```&```** . Son operaciones completamente distintas.

Del mismo modo, existe el operador booleano **```||```** (**O**) y el operador bit a bit **```|```** .

En el caso de la negación, el operador booleano es **```!```** y el operador bit a bit es **```~```** pero aún así hay que tener claro cuál se quiere usar en cada caso.

### Ejemplos

```Arduino
if (a >= 10 && a <= 20){}   // true si a está entre 10 y 20
```

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Boolean)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
