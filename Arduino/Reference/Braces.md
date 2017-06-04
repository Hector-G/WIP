# {} Llaves

Las llaves forman una parte importante dentro del lenguaje de programación C. Se utilizan en distintas estructuras, que se comentan a continuación. Puede resultar un poco ambiguo al principio.

Una llave de apertura ```{``` debe terminar siempre en una llave de cierre ```}```. A esto se le suele llamar equilibrar las llaves. El IDE de Arduino (*Integrated Development Environment* o Entorno de Desarrollo Integrado) es capaz de detectar llaves emparejadas. Simplemente selecciona una, o incluso clica el cursor inmediatamente detrás de la llave, y se resaltará su pareja.

Es muy aconsejable a la hora de programar escribir la llave de cierre inmediatamente después de poner una de apertura, para así asegurarse que siempre están equilibradas. Después se añade el bloque de código en el interior.

Las llaves desequilibradas producen complicados errores de compilador que en ocasiones son difíciles de encontrar en programas largos. 

Usos principales de las llaves:

### Funciones

```Arduino
  void mifuncion(tipodedato argumento){
    // instrucciones
  }
  ```
  
### Bucles

```Arduino
  while (boolean condición)
  {
     // instrucciones
  }
```

```Arduino
  do
  {
     // instrucciones
  } while (boolean condición);
```

```Arduino
  for (inicialización; condición de finalización; incremento)
  {
     // instrucciones
  } 
  
 ```
 
### Expresiones condicionales

```Arduino
  if (boolean condición)
  {
     // instrucciones
  }
```

```Arduino
  else if (boolean condición)
  {
     // instrucciones
  } 
  else
  {
     // instrucciones
  }
```


-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Braces)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
