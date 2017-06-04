# if (condicional) y los operadores de comparación ==, !=, <, >

```if```, que se utiliza conjuntamente con un operador de comparación, comprueba si se cumple una determinada condición, por ejemplo si una de las entradas ha superado cierto valor. El formato es el siguiente:

```Arduino
if (miVariable > 50)
{
  // hacer algo aquí
}
```

El programa comprobará si ```miVariable``` es mayor que 50. Si es así, el programa realizará una acción concreta. Dicho de otro modo, si la condición dentro del paréntesis se cumple, se ejecutarán las instrucciones dentro de las llaves. Si no se cumple, el programa salta el código y continúa con el resto.

Las llaves se pueden omitir después de un ```if```. Si no se utilizan llaves, la linea siguiente (delimitada por punto y coma) se convierte en la única instrucción condicionada.

```Arduino
if (x > 120) digitalWrite(LEDpin, HIGH); 

if (x > 120)
digitalWrite(LEDpin, HIGH); 

if (x > 120){ digitalWrite(LEDpin, HIGH); } 

if (x > 120){ 
  digitalWrite(LEDpin1, HIGH);
  digitalWrite(LEDpin2, HIGH); 
}                                 // todas son correctas
```


### Operadores de comparación:

```Arduino
 x == y (x es igual a y)
 x != y (x no es igual a y)
 x <  y (x es menor que y)  
 x >  y (x es mayor que y) 
 x <= y (x es menor o igual que y) 
 x >= y (x es mayor o igual que y)
 ```

#### Atención:

Cuidado con utilizar accidentalmente un único signo igual (por ejemplo ```if (x = 10)```). Un sólo signo igual ```=``` es un operador de asignación, por lo que asignaría a la variable x el valor 10 sin comprobar su valor actual. Utiliza el doble signo igual ```==``` que es un operador de comparación y comprueba si x es igual a 10 o no. En el segundo caso sólo se tiene que es cierto si x es igual a 10, el primero es cierto siempre.

Esto es porque C evalúa la expresión ```if (x = 10)``` del siguiente modo: se asigna a x el valor 10 (un sólo signo igual es operador de asignación), por lo que x ahora vale 10. Entonces el condicional ```if``` evalúa 10, que siempre será ```TRUE```, ya que es un valor distinto a cero. Por tanto, ```if (x = 10)```devolverá siempre ```TRUE```, que no es el resultado que esperamos al usar ```if``` y además x tomará el valor 10, que tampoco es algo que queríamos que sucediese.

```if``` se puede utilizar como parte de la estructura de control [if...else](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference/Else.md)

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/If)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
