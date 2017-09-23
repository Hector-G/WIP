# return

Terminar una función y devolver un valor de una función, si así se desea.

### Sintaxis:

```Arduino
return;

return valor; // Ambas posibilidades son válidas
```
### Parámetros

**valor** : cualquier tipo de variable o constante

### Ejemplos:

Una función que compara el valor de un sensor con un valor umbral

```Arduino
 int compruebaSensor(){       
    if (analogRead(0) > 400) {
        return 1;
    else{
        return 0;
    }
}
``` 
Usar ```return``` es útil para probar una sección de código sin tener que "comentar" muchas lineas en un programa con posibles fallos.

```Arduino
void loop(){

// Una maravillosa idea que quieres probar

return;

// El resto del código aquí
// después de return no se ejecutará nunca
}
```
-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Return)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
