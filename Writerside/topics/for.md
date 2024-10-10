# El ciclo `for`

El ciclo `for` es una estructura de control que permite ejecutar un bloque de código un número determinado de veces. La
sintaxis del ciclo `for` es la siguiente:

```c++
for (inicialización; condición; actualización)
{
    // Bloque de código
}
```

Donde:

- `inicialización` es una expresión que se ejecuta una sola vez al principio del ciclo y se utiliza para inicializar
  variables.
- `condición` es una expresión que se evalúa a verdadero o falso. Mientras la condición sea verdadera, el bloque de
  código se ejecutará.
- `actualización` es una expresión que se ejecuta al final de cada iteración del ciclo y se utiliza para actualizar
  variables.
- `Bloque de código` es el código que se ejecuta en cada iteración del ciclo.

Por ejemplo, el siguiente código:

```c++
for (int i = 0; i < 5; i++)
{
    cout << i << endl;
}
```

Imprimirá los números del 0 al 4 en la consola.

## Formas alternativas de usar el ciclo `for`

Además de la forma estándar de usar el ciclo `for`, existen algunas formas alternativas que pueden resultar útiles en
ciertas situaciones.

### Ciclo `for` sin condición

Si se omite la condición en el ciclo `for`, el ciclo se ejecutará indefinidamente. Esto puede ser útil cuando se desea
ejecutar un ciclo hasta que se cumpla una condición dentro del bloque de código.

Por ejemplo, el siguiente código:

```c++
for (int i = 0; ; i++)
{
    if (i == 5)
    {
        break;
    }
    cout << i << endl;
}
```

Imprimirá los números del 0 al 4 en la consola y luego terminará el ciclo.

### Ciclo `for` sin inicialización

Si se omite la inicialización en el ciclo `for`, se asume que las variables ya han sido inicializadas previamente. Esto
puede ser útil cuando se desea utilizar variables que ya han sido inicializadas fuera del ciclo.

Por ejemplo, el siguiente código:

```c++
int i = 0;
for (; i < 5; i++)
{
    cout << i << endl;
}
```

Imprimirá los números del 0 al 4 en la consola.

### Ciclo `for` sin actualización

Si se omite la actualización en el ciclo `for`, se asume que la actualización de variables se realizará dentro del
bloque de código. Esto puede ser útil cuando se desea actualizar variables de forma condicional.

Por ejemplo, el siguiente código:

```c++
for (int i = 0; i < 5; )
{
    cout << i << endl;
    i++;
}
```

Imprimirá los números del 0 al 4 en la consola.