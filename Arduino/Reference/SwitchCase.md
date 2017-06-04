# switch / case

Al igual que ```if```, la expresión switch ... case controla el flujo del programa permitiendo especificar distintos bloques de código que se ejecutarán si se cumplen unas condiciones determinadas. En particular ```switch``` compara el valor de una variable con los valores especificados en cada uno de los ```case```. Cuando se encuentra un ```case``` que concuerda con el valor de la variable, se ejecuta el bloque de código asociado a ese ```case```.

La instrucción ```break``` fuerza a salir de la estructura ```switch```. Normalmente se utiliza al final de cada bloque asociado a un ```case```. Si no se utiliza la instrucción ```break```, el programa continuará comprobando las siguientes expresiones hasta alcanzar un ```break``` o el final de toda la estructura ```switch```. 

### Ejemplo

```Arduino
switch (variable) {
    case 1:
      // Hacer algo cuando variable es igual a 1
      break;
    case 2:
      // Hacer algo cuando variable es igual a 2
      break;
    default: 
      // Si no coincide con ningún caso, ejecutar el bloque default (por defecto)
      // usar default es opcional
    break;
  }
```

#### Nota

Para poder declarar variables dentro de un ```case``` es necesario utilizar llaves como se muestra en el siguiente ejemplo:

```Arduino
switch (var) {
    case 1:
      {
      // Hacer algo cuando var es igual a 1
      int a = 0;
      .......
      .......
      }
      break;
    default: 
      // Si no coincide con ningún caso, ejecutar el bloque default (por defecto)
      // usar default es opcional
    break;
  }
``` 

#### Sintaxis

```Arduino
switch (var) {
  case etiqueta:
    // instrucciones
    break;
  case etiqueta:
    // instrucciones
    break;
  default: 
    // instrucciones
  break;
}
```

#### Parámetros

**var** : la variable cuyo valor se compara en los distintos ```case```

**etiqueta**: un valor a comparar con el de la variable


-------------------------

### Relacionado

[if](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference/If.md)

[if else](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference/Else.md)

 ------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/SwitchCase)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
