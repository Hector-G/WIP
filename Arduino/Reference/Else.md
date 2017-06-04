# if / else

```if...else``` ofrece mayor control sobre el código que usar sólamente ```if```, ya que permite realizar varias comprobaciones de forma conjunta. Por ejemplo, se puede leer una entrada analógica, si su valor es menor que 500 se realiza una acción, y realizar otra acción diferente si el valor es mayor o igual que 500. El código tendría este aspecto:

```Arduino
if (pinEntrada < 500)
{
  // acción A
}
else
{
  // acción B
}

```

```else``` puede encadenar otro ```if``` de forma que se pueden comprobar diferentes condiciones mutuamente excluyentes de forma ordenada.

Cada condición saltará a la siguiente hasta que se encuentre una cuyo resultado sea cierto. Cuando se cumple la condición, su bloque de código asociado se ejecuta, y luego el programa salta hasta la linea después de toda la construcción if/else. Si no se cumple ninguna condición, se ejecuta el último bloque ```else``` por defecto siempre que se haya definido.

Nota que un bloque ```else if``` se puede usar con o sin otro bloque ```else``` al final y viceversa. El número de estructuras ```else if``` que se pueden encadenar es ilimitado.

```Arduino
if (pinEntrada < 500)
{
  // acción A
}
else if (pinEntrada >= 1000)
{
  // acción B
}
else
{
  // acción C
}
```

Otra forma de utilizar estructuras ramificadas mutuamente excluyentes es mediante la expresión [switch case](https://github.com/Hector-G/WIP/new/master/Arduino/Reference/SwitchCase.md)

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Else)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
