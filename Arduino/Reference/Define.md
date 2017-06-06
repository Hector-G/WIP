# #define

```#define``` es un componente de C muy útil que permite darle un nombre a un valor constante antes de compilar el programa. Las constantes definidas en arduino no ocupan ningún espacio en la memoria del chip. El compilador reemplaza las referencias a estas constantes por el correspondiente valor en el momento de compilar.

No obstante puede tener algunos efectos no deseados, si por ejemplo, si el nombre de una constante que se ha definido se guarda como alguna otra constante o variable. En ese caso el texto se reemplazaría por el número (o texto) definido. 

En general, es preferible utilizar ```const``` para definir constantes en vez de utilizar ```#define```.

La sintaxis de arduino es la misma que para C:

### Sintaxis

```Arduino
#define nombreConstante valor
```

Cuidado porque es necesario incluir la almohadilla (**#**)

### Ejemplo

```Arduino
#define pinLed 3
// El compilador reemplazará cualquier mención a pinLed por el valor 3 durante la compilación.
```

### Consejo

No se utiliza punto y coma al final de ```#define```. Si escribes punto y coma el compilador devolverá errores al final de la página.

```Arduino
#define pinLed 3;    // esto da error
```

De forma similar, incluir un signo igual con ```#define``` devolverá un error de compilador más adelante en la página.

```Arduino
#define pinLed  = 3  // esto también da error
```

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Define)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
