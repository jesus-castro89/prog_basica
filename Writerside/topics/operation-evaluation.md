# Evaluación de Operaciones

La evaluación de operaciones es una parte fundamental de la programación en C++, ya que permite realizar cálculos y
manipulaciones de datos de manera eficiente. En este apartado, se explicarán como se evalúan las operaciones en C++ y se
mostrarán ejemplos de su uso, así como ejercicios para practicar.

## Conceptos básicos

En C++, las operaciones se evalúan siguiendo una serie de reglas y prioridades. A continuación, se presentan los
conceptos básicos que debes conocer sobre la evaluación de operaciones en C++:

- **Operadores aritméticos:** Los operadores aritméticos como la suma `+`, la resta `-`, la multiplicación `*`, la
  división `/` y el módulo `%` se evalúan en el orden en que aparecen en la expresión.
- **Operadores de asignación:** Los operadores de asignación como `=`, `+=`, `-=`, `*=`, `/=`, entre otros, se evalúan
  de derecha a izquierda.
- **Operadores de comparación:** Los operadores de comparación como `==`, `!=`, `<`, `>`, `<=`, `>=` se evalúan en el
  orden en que aparecen en la expresión.
- **Operadores lógicos:** Los operadores lógicos como `&&`, `||`, `!` se evalúan en el orden en que aparecen en la
  expresión.
- **Operadores de incremento y decremento:** Los operadores de incremento `++` y decremento `--` se evalúan de acuerdo
  a su posición en la expresión. Ya que pueden ser prefijos o sufijos, su evaluación puede variar.
    - **Prefijo:** Si el operador de incremento o decremento es prefijo, se evalúa antes de la operación.
    - **Sufijo:** Si el operador de incremento o decremento es sufijo, se evalúa después de la operación.
- **Operadores de bits:** Los operadores de bits como `&`, `|`, `^`, `~`, `<<`, `>>` se evalúan en el orden en que
  aparecen en la expresión.
- **Operadores condicionales:** El operador condicional `? :` se evalúa de acuerdo a la condición que se cumpla.
- **Operadores de puntero y referencia:** Los operadores de puntero `*` y referencia `&` se evalúan de acuerdo a su
  posición en la expresión.
- **Operadores de miembro:** Los operadores de miembro `.` y `->` se evalúan de acuerdo a su posición en la expresión.
- **Operadores de alcance:** Los operadores de alcance `::` se evalúan de acuerdo a su posición en la expresión.
- **Operadores de coma:** El operador de coma `,` se evalúa de izquierda a derecha.

## Ejemplos

A continuación, se presentan algunos ejemplos de evaluación de operaciones en C++:

```c++
#include <iostream>

int main() {
    int a = 5, b = 3, c = 2, d = 4;
    int result = a + b * c / d;
    std::cout << "Resultado: " << result << std::endl; // Resultado: 5
    return 0;
}
```

En este ejemplo, se evalúa la expresión `a + b * c / d` siguiendo las reglas de prioridad de los operadores aritméticos.
Primero se realiza la multiplicación `b * c`, luego la división `b * c / d` y finalmente la suma `a + b * c / d`.

```c++
#include <iostream>

int main() {
    int a = 5, b = 3, c = 2, d = 4;
    int result = (a + b) * c / d;
    std::cout << "Resultado: " << result << std::endl; // Resultado: 3
    return 0;
}
```

En este ejemplo, se evalúa la expresión `(a + b) * c / d` siguiendo las reglas de prioridad de los operadores
aritméticos. Primero se realiza la suma `a + b`, luego la multiplicación `(a + b) * c` y finalmente la división
`(a + b) * c / d`.

## Ejercicios

Sean `a = 5`, `b = 3`, `c = 2`, `d = 4`, `e = 6` y `f = 8`. Evalúa las siguientes expresiones y determina su
resultado:

1. `a + b * c / d`
2. `(a + b) * c / d`
3. `a + b * (c / d)`
4. `a + b * c % d`
5. `a + b * c / d + e % f`
6. `a + b * c / d + e % f - a`
7. `a + b * c / d + e % f - a * b`
8. `a + b * c / d + e % f - a * b / c`
9. `a + b * c / d + e % f - a * b / c + d`
10. `a + b * c / d + e % f - a * b / c + d - e`

