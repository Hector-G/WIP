# goto

Transfiere el flujo del programa hasta un punto determinado por una etiqueta.

### Sintaxis

```Arduino
etiqueta:

goto etiqueta; // Envía el programa a la etiqueta
```

### Consejo

No se recomienda el uso de ```goto``` al programar en C, en algunos libros de programación los autores afirman que nunca existe la necesidad de utilizar ```goto``` en este lenguaje. Sin embargo, si se usa con criterio puede simplificar algunos programas. El motivo por el que muchos programadores se mosquean al ver el uso de ```goto``` en el código es porque su uso indiscriminado hace que se pierda el hilo del programa, haciendo que sea imposible de depurar.

Dicho esto, hay algunas situaciones en las que la expresión ```goto``` puede resultar útil simplificando el código. Un ejemplo es cuando queremos salir del interior de varios bucles ```for``` anidados, o bloques ```if```, dada una determinada condición.

### Ejemplo

```Arduino
for(byte r = 0; r < 255; r++){
    for(byte g = 255; g > -1; g--){
        for(byte b = 0; b < 255; b++){
            if (analogRead(0) > 250){ goto salida;}
            // más código ... 
        }
    }
}
salida:
```


-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Goto)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
