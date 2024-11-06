# Las palabras reservadas `explicit`, `const` y `nodiscard`

En C++, existen algunas palabras reservadas que se utilizan para modificar el comportamiento de las funciones y
variables. En este artículo, nos enfocaremos en tres de ellas: `explicit`, `const` y `nodiscard`.

## `explicit`

La palabra reservada `explicit` se utiliza para evitar conversiones implícitas en la llamada a un constructor.

```c++
#include <iostream>

struct Product {
    int value;

    explicit Product(int v) : value(v) {}
};

int main() {
    Product p1 = 5; // Error: conversion implícita no permitida
    Product p2(10); // OK: llamada explícita al constructor
    return 0;
}
```

En el ejemplo anterior, la declaración `Product p1 = 5;` generará un error de compilación debido a que el constructor
de `Product` es explícito y no permite conversiones implícitas. En cambio, la declaración `Product p2(10);` es válida
porque se realiza una llamada explícita al constructor.

## `const`

La palabra reservada `const` se utiliza para indicar que una variable no puede ser modificada después de su
inicialización.

```c++
#include <iostream>

int main() {
    const int x = 5;
    x = 10; // Error: no se puede modificar una variable constante
    return 0;
}
```

En el ejemplo anterior, la variable `x` se declara como `const int`, lo que significa que no se puede modificar su
valor después de su inicialización. Por lo tanto, la línea `x = 10;` generará un error de compilación.

En funciones de una estructura o clase, la palabra reservada `const` se utiliza para indicar que la función no
modificará los miembros de la estructura o clase.

```c++
#include <iostream>

struct Point {
    int x;
    int y;

    void print() const {
        std::cout << "(" << x << ", " << y << ")" << std::endl;
    }
};

int main() {
    Point p = {3, 5};
    p.print();
    return 0;
}
```

En el ejemplo anterior, la función `print` de la estructura `Point` se declara como `const`, lo que indica que la
función no modificará los miembros de la estructura. Esto permite llamar a la función en objetos `const` de la
estructura.

## `nodiscard`

La palabra reservada `nodiscard` se utiliza para indicar que el valor de retorno de una función no debe ser ignorado.

```c++
#include <iostream>

[[nodiscard]] int square(int x) {
    return x * x;
}

int main() {
    square(5); // Advertencia: el valor de retorno no se está utilizando
    return 0;
}
```

En el ejemplo anterior, la función `square` se declara con el atributo `nodiscard`, lo que indica que el valor de
retorno de la función no debe ser ignorado. Si se llama a la función `square` sin utilizar su valor de retorno, se
generará una advertencia.

Estas son algunas de las palabras reservadas más comunes en C++ que se utilizan para modificar el comportamiento de
las funciones y variables. Al comprender su significado y uso, puedes escribir un código más claro y robusto.