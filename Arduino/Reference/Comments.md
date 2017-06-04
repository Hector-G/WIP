# Comentarios

Los comentarios son lineas en el programa que se utilizan para anotar información sobre cómo funciona el programa. El compilador las ignorará y no las exportará al procesador por lo que no ocupan ningún espacio en la memoria del chip Atmega.

El único objetivo de los comentarios es ayudar a entender (o recordar) cómo funciona el programa, o simplemente dar cierta información adicional. Hay dos maneras de marcar una linea como comentario:

### Ejemplo

```Arduino
 x = 5;  // Esto es un comentario de una linea. Todo lo que está detrás de la doble barra es comentario 
         // hasta el final de la linea

/* esto es un comentario multilinea. Puedes comentar bloques de código enteros

if (gwb == 0){   // se admiten comentarios de una linea dentro de comentarios multilinea
x = 3;           /* pero no comentarios multilinea dentro de comentarios multilinea. Esto no funciona. */
}
// No olvides cerrar los comentarios multilinea.
*/
```

### Consejo
Cuando haces pruebas con código, "comentar" partes del programa es una forma práctica de eliminar lineas con posibles fallos. Así puedes dejar las lineas en el código, pero al convertirlas en comentarios, el compilador las ignora y no se ejecutan. Este truco es especialmente útil cuando tratas de encontrar un problema, o cuando el programa no quiere compilar porque hay algún error sin especificar en una linea determinada.

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/Comments)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
