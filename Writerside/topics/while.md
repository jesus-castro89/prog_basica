# Los ciclos while y do-while en C++

Los ciclos `while` y `do-while` son estructuras de control de flujo que permiten ejecutar un bloque de código mientras
se cumpla una condición. En este apartado, se explicará cómo funcionan estos ciclos y se mostrarán ejemplos de su uso.

## 1.- Ciclo `while`

El ciclo `while` permite ejecutar un bloque de código mientras se cumpla una condición. La sintaxis del ciclo `while`
es la siguiente:

```c++
while (condicion)
{
    // Bloque de código
}
```

Donde `condicion` es una expresión que se evalúa a verdadero o falso. Mientras la condición sea verdadera, el bloque de
código se ejecutará. Cuando la condición sea falsa, el ciclo `while` terminará y la ejecución del programa continuará
con la instrucción siguiente al bloque de código.

Por ejemplo, el siguiente código:

```c++
int i = 0;
while (i < 5)
{
    cout << i << endl;
    i++;
}
```

Imprimirá los números del 0 al 4 en la consola.

## 2.- Ciclo `do-while`

El ciclo `do-while` es similar al ciclo `while`, pero la condición se evalúa al final del ciclo, lo que garantiza que el
bloque de código se ejecute al menos una vez. La sintaxis del ciclo `do-while` es la siguiente:

```c++
do
{
    // Bloque de código
} while (condicion);
```

Donde `condicion` es una expresión que se evalúa a verdadero o falso. El bloque de código se ejecutará al menos una vez,
y luego se seguirá ejecutando mientras la condición sea verdadera.

Por ejemplo, el siguiente código:

```c++
int i = 0;
do
{
    cout << i << endl;
    i++;
} while (i < 5);
```

Imprimirá los números del 0 al 4 en la consola.

## 3.- Diferencias entre `while` y `do-while`

La principal diferencia entre el ciclo `while` y el ciclo `do-while` es que el ciclo `do-while` garantiza que el bloque
de código se ejecute al menos una vez, ya que la condición se evalúa al final del ciclo. En cambio, el ciclo `while`
puede no ejecutar el bloque de código si la condición es falsa desde el principio.

En general, se recomienda usar el ciclo `while` cuando se quiere ejecutar un bloque de código mientras se cumpla una
condición, y el ciclo `do-while` cuando se quiere ejecutar un bloque de código al menos una vez y luego repetirlo
mientras se cumpla una condición.

## Ejercicios

1. Escriba un programa que imprima los números del 1 al 10 utilizando un ciclo `while`.
2. Escriba un programa que lea un número entero positivo e imprima todos los números pares menores o iguales al número
   leído utilizando un ciclo `do-while`.
3. Escriba un programa que lea un número entero positivo e imprima la suma de los números del 1 al número leído utilizando
   un ciclo `while`.
4. Escriba un programa que lea un número entero positivo e imprima la suma de los números pares menores o iguales al
   número leído utilizando un ciclo `do-while`.
5. Escriba un programa que lea un número entero positivo e imprima la suma de los números impares menores o iguales al
   número leído utilizando un ciclo `while`.
6. Escriba un programa que lea un número entero positivo e imprima la suma de los números impares menores o iguales al
   número leído utilizando un ciclo `do-while`.
7. Escriba un programa que lea un número entero positivo e imprima la suma de los números múltiplos de 3 menores o iguales
   al número leído utilizando un ciclo `while`.
8. Escriba un programa que lea un número entero positivo e imprima la suma de los números múltiplos de 3 menores o iguales
   al número leído utilizando un ciclo `do-while`.
9. Escriba un programa que lea un número entero positivo e imprima la suma de los números múltiplos de 5 menores o iguales
   al número leído utilizando un ciclo `while`.
10. Escriba un programa que lea un número entero positivo e imprima la suma de los números múltiplos de 5 menores o iguales
    al número leído utilizando un ciclo `do-while`.