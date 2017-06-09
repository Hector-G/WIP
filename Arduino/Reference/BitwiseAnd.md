# Operaciones bit a bit AND (&), OR ( | ), XOR (^)

Los operadores bit a bit realizan sus cálculos sobre las variables a nivel de bit. Sirven para resolver muchos problemas comunes en programación.

### Descripción y sintaxis

A continuación están las descripciones y sintaxis de todos los operadores.

### AND (&) **_Y_** lógico

El operador bit a bit **Y** para el lenguaje C++ es **```&```** y se utiliza entre dos expresiones de enteros. Opera sobre cada bit de forma independiente siguiendo esta regla: si las dos entradas son 1, el resultado es 1, en cualquier otro caso el resultado es 0. Otra forma de escribirlo sería:
    
```    
    0  0  1  1    operando 1
    0  1  0  1    operando 2
    ----------
    0  0  0  1    (operando 1 & operando 2) - resultado
```

En arduino, el tipo ```int``` es un valor de 16 bit, por lo que al utilizar **```&```** se realizarán 16 operaciones _AND_ .

```
    int a =  92;    // en binario: 0000000001011100
    int b = 101;    // en binario: 0000000001100101
    int c = a & b;  // resultado:  0000000001000100, o 68 en decimal
    
```

Cada uno de los 16 bits en a y b se procesan usando el operador bit a bit, y los 16 resultados se almacenan en c, dando como resultado el valor 01000100 en binario, que es 68 en decimal.

Uno de los usos más comunes del operador bit a bit **```&```** es seleccionar un bit (o varios bit) en particular de un valor entero, en lo que se suele llamar máscara.

### OR ( | ) **_O_** lógico

El operador bit a bit _OR_ en C++ es la barra vertical **```|```** . Como el operador **```&```** , opera independientemente en cada uno de los bits, pero (obviamente) realiza otra operación. La operación _OR_ entre dos bits funciona así: si al menos uno de los dos bits de entrada es 1 el resultado es 1, si ambos son 0 el resultado es 0. Dicho de otro modo:

```
    0  0  1  1    operando 1
    0  1  0  1    operando 2
    ----------
    0  1  1  1    (operando 1 | operando 2) - resultado
```

Un ejemplo del operador bit a bit _OR_

```C++
    int a =  92;    // en binario: 0000000001011100
    int b = 101;    // en binario: 0000000001100101
    int c = a | b;  // resultado:  0000000001111101, o 125 en decimal.
```
### Programa de ejemplo para Arduino UNO

Una tarea común para los operadores bit a bit _AND_ y _OR_ es algo conocido como _Leer-Modificar-Escribir_ en un puerto. En los microcontroladores, un puerto es un número de 8 bits que representa algo sobre la condición de los pines. Escribir un puerto controla todos los pines de una.

```PORTD``` es una constante predefinida que hace referencia a las salidas de los pines digitales 0, 1, 2, 3, 4, 5, 6 y 7. Si hay un 1 en uno de los bits, significa que la salida de ese pin es ```HIGH``` . (Los pines tienen que estar definidos mediante el comando ```pinMode()``` ). De modo que si escribimos ```PORTD = B00110001;``` haremos que los pines 0, 4 y 5 estén en ```HIGH``` . Un pequeño detalle a tener en cuenta es que hemos puesto un 0 en los pines 0 y 1 de Arduino, que tiene reservados para la comunicación serie, por lo que podríamos interferir en los pines de comunicación.

El algoritmo para el programa sería:
  Leer ```PORTD``` y borrar sólo los bits correspondientes a los pines que queremos controlar (con **``` & ```** )

  Combinar el nuevo valor de ```PORTD``` modificado con el valor de los pines bajo control (con **``` | ```** )
  
```Arduino  
int i;     // contador
int j;

void setup(){
DDRD = DDRD | B11111100; // poner a 1 la dirección de los pines del 2 al 7, dejar el pin 0 y el 1 como estén (xx | 00 == xx)
// igual que pinMode(pin, OUTPUT) para los pines 2 a 7
Serial.begin(9600);
}

void loop(){
for (i=0; i<64; i++){

PORTD = PORTD & B00000011;  // limpiar los bits 2 - 7, dejar los pines 0 y 1 sin tocar (xx & 11 == xx)
j = (i << 2);               // desplazar la variables para los pines 2 - 7 - para evitar los pines 0 y 1
PORTD = PORTD | j;          // combinar la información del puerto co la nueva información de los pines LED
Serial.println(PORTD, BIN); // mostrar la máscara por consola
delay(100);
   }
}

```

###  XOR ( ^ ) **_O EXCLUYENTE_**

Existe un operador un tanto peculiar en C++ que se llama operador bit a bit _O EXCLUYENTE_, o _XOR_ . Se escribe con el símbolo acento circunflejo ( **^** ). Es muy similar al operador bit a bit _OR_ ( **|** ) sólo que devuelve un 0 en el caso en el que ambos operandos son 1.

```    
    0  0  1  1    operando 1
    0  1  0  1    operando 2
    ----------
    0  1  1  0    (operando 1 ^ operando 2) - resultado
``` 
Otra forma de entenderlo sería que el resultado es 1 cuando los bits de entrada son distintos y 0 si son iguales.

Un ejemplo de código:

```Arduino
    int x = 12;     // en binario: 1100
    int y = 10;     // en binario: 1010
    int z = x ^ y;  // en binario: 0110, o en decimal 6
```

El operador **^** se utiliza a menudo para alternar (cambiar de 0 a 1 o de 1 a 0) algunos bits en una expresión entera. En la operacion bit a bit _OR_ si hay un 1 en el bit de máscara, ese bit se invierte, y si hay un 0 el bit se queda igual. El siguiente ejemplo hace parpadear el pin digital 5.

```Arduino
// Blink_Pin_5

void setup(){
DDRD = DDRD | B00100000; // definir el PIN5 como OUTPUT 
Serial.begin(9600);
}

void loop(){
PORTD = PORTD ^ B00100000;  // invertir el bit 5 (DIGITAL PIN5), los demás no se tocan
delay(100);
}
```

-------------------------

[Índice Referencia](https://github.com/Hector-G/WIP/blob/master/Arduino/Reference.md)


[Documentación en la web oficial de Arduino](https://www.arduino.cc/en/Reference/BitwiseAnd)

Este documento es una traducción del texto de Arduino Reference, bajo una licencia [Creative Commons Reconocimiento-CompartirIgual 3.0](https://creativecommons.org/licenses/by-sa/3.0/es/). Los ejemplos de código son de dominio público.
