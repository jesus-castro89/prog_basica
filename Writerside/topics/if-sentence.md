# Control de Flujo condicional en C++

## Sentencia `if`

La sentencia de control de flujo `if` en C++ permite ejecutar un bloque de código si se cumple una condición. La
estructura básica de la sentencia `if` es la siguiente:

```c++
if (condición) {
    // Bloque de código que se ejecuta si la condición es verdadera
}
```

Donde:

- `condición`: Es una expresión que se evalúa como verdadera o falsa. Si la condición es verdadera, se ejecuta el bloque
  de código dentro de las llaves `{}`.
- `Bloque de código`: Es el conjunto de instrucciones que se ejecutan si la condición es verdadera.
- `{}`: Representan el inicio y el final del bloque de código.
- `if`: Palabra clave que indica el inicio de la sentencia `if`.

### Ejemplo de la sentencia `if`

A continuación, se muestra un ejemplo de la sentencia `if` en C++:

```c++
#include <iostream>

int main() {
    int edad;
    std::cin>>edad;

    if (edad >= 18) {
        std::cout << "Eres mayor de edad." << std::endl;
    }

    return 0;
}
```

En este ejemplo, se solicita al usuario que ingrese su edad. Si la edad ingresada es mayor o igual a 18, se muestra el
mensaje "Eres mayor de edad". Si la edad es menor a 18, no se muestra ningún mensaje.

## Sentencia `if-else`

La sentencia de control de flujo `if-else` en C++ permite ejecutar un bloque de código si se cumple una condición y otro
bloque de código si la condición no se cumple. La estructura básica de la sentencia `if-else` es la siguiente:

```c++
if (condición) {
    // Bloque de código que se ejecuta si la condición es verdadera
} else {
    // Bloque de código que se ejecuta si la condición es falsa
}
```

Donde:

- `condición`: Es una expresión que se evalúa como verdadera o falsa. Si la condición es verdadera, se ejecuta el primer
  bloque de código. Si la condición es falsa, se ejecuta el segundo bloque de código.
- `Bloque de código`: Son los conjuntos de instrucciones que se ejecutan dependiendo de si la condición es verdadera o
  falsa.
- `{}`: Representan el inicio y el final de los bloques de código.
- `if`: Palabra clave que indica el inicio de la sentencia `if`.
- `else`: Palabra clave que indica el inicio del bloque de código que se ejecuta si la condición es falsa.

### Ejemplo de la sentencia `if-else`

A continuación, se muestra un ejemplo de la sentencia `if-else` en C++:

```c++
#include <iostream>

int main() {
    int edad;
    std::cin>>edad;

    if (edad >= 18) {
        std::cout << "Eres mayor de edad." << std::endl;
    } else {
        std::cout << "Eres menor de edad." << std::endl;
    }

    return 0;
}
```

En este ejemplo, se solicita al usuario que ingrese su edad. Si la edad ingresada es mayor o igual a 18, se muestra el
mensaje "Eres mayor de edad". Si la edad es menor a 18, se muestra el mensaje "Eres menor de edad".

## Sentencia `if-else if-else`

La sentencia de control de flujo `if-else if-else` en C++ permite evaluar múltiples condiciones y ejecutar un bloque de
código dependiendo de la primera condición que se cumpla. La estructura básica de la sentencia `if-else if-else` es la
siguiente:

```c++
if (condición1) {
    // Bloque de código que se ejecuta si la condición1 es verdadera
} else if (condición2) {
    // Bloque de código que se ejecuta si la condición2 es verdadera
} else {
    // Bloque de código que se ejecuta si ninguna de las condiciones anteriores es verdadera
}
```

Donde:

- `condición1`, `condición2`: Son expresiones que se evalúan como verdaderas o falsas. Se evalúan en orden, y se ejecuta
  el bloque de código correspondiente a la primera condición verdadera.
- `Bloque de código`: Son los conjuntos de instrucciones que se ejecutan dependiendo de si la condición es verdadera.
- `{}`: Representan el inicio y el final de los bloques de código.
- `if`: Palabra clave que indica el inicio de la sentencia `if`.
- `else if`: Palabra clave que indica la evaluación de una nueva condición si la condición anterior no se cumple.
- `else`: Palabra clave que indica el inicio del bloque de código que se ejecuta si ninguna de las condiciones
  anteriores es verdadera.

### Características de la sentencia `if-else if-else`

- Se evalúan las condiciones en orden, y se ejecuta el bloque de código correspondiente a la primera condición
  verdadera.
- Si ninguna de las condiciones es verdadera, se ejecuta el bloque de código dentro del `else`.
- Se pueden tener múltiples bloques `else if` para evaluar más de dos condiciones.
- La sentencia `if-else if-else` es útil cuando se necesita tomar decisiones basadas en múltiples condiciones.
- La sentencia `if-else if-else` es más eficiente que usar múltiples sentencias `if` anidadas.
- La sentencia `if-else if-else` es más legible y fácil de entender que múltiples sentencias `if` anidadas.

### Ejemplo de la sentencia `if-else if-else`

A continuación, se muestra un ejemplo de la sentencia `if-else if-else` en C++:

```c++
#include <iostream>

int main() {
    int edad;
    std::cin>>edad;

    if (edad < 0) {
        std::cout << "La edad no puede ser negativa." << std::endl;
    } else if (edad < 18) {
        std::cout << "Eres menor de edad." << std::endl;
    } else if (edad < 65) {
        std::cout << "Eres adulto." << std::endl;
    } else {
        std::cout << "Eres adulto mayor." << std::endl;
    }

    return 0;
}
```

Este mismo ejemplo puede ser representado anidadamente de la siguiente manera:

```c++
#include <iostream>

int main() {
    int edad;
    std::cin>>edad;

    if (edad < 0) {
        std::cout << "La edad no puede ser negativa." << std::endl;
    } else {
        if (edad < 18) {
            std::cout << "Eres menor de edad." << std::endl;
        } else {
            if (edad < 65) {
                std::cout << "Eres adulto." << std::endl;
            } else {
                std::cout << "Eres adulto mayor." << std::endl;
            }
        }
    }

    return 0;
}
```

Como se puede notar al usar la sentencia `if-else if-else`, el código es más legible y fácil de entender.

## Conclusión

Las sentencias de control de flujo condicional en C++ (`if`, `if-else`, `if-else if-else`) son fundamentales para tomar
decisiones en un programa en función de ciertas condiciones. Estas estructuras permiten modificar el flujo de ejecución
del programa y ejecutar diferentes bloques de código dependiendo de si se cumplen o no ciertas condiciones. Es
importante comprender cómo funcionan estas sentencias y cuándo es apropiado utilizar cada una de ellas para escribir
código claro, legible y eficiente.

## Referencias

- [C++ if, if...else and Nested if...else](https://www.programiz.com/cpp-programming/if-else)
- [C++ if, if...else and Nested if...else](https://www.tutorialspoint.com/cplusplus/cpp_decision_making.htm)
- [C++ if, if...else and Nested if...else](https://www.geeksforgeeks.org/decision-making-c-c-else-nested-else/)