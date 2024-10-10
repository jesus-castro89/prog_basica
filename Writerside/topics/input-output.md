# La librería `<iostream>`

La biblioteca `<iostream>` es una biblioteca estándar de C++ que proporciona las funciones de entrada y salida estándar.
Esta biblioteca incluye las clases `std::cin` y `std::cout` para la entrada y salida de datos, respectivamente.

## Inclusión de la biblioteca

Para utilizar la biblioteca `<iostream>`, se debe incluir la siguiente directiva de preprocesador al inicio del
programa:

```c++
#include <iostream>
```

## Funciones de entrada y salida

Las funciones de entrada y salida de la biblioteca `<iostream>` se utilizan para leer datos del usuario y mostrar datos
en la consola.

### std::cin

La clase `std::cin` se utiliza para leer datos del usuario. Por ejemplo, para leer un número entero del usuario, se
puede utilizar la siguiente instrucción:

```c++
int numero;
std::cin >> numero;
```

### std::cout

La clase `std::cout` se utiliza para mostrar datos en la consola. Por ejemplo, para imprimir un mensaje en la consola,
se puede utilizar la siguiente instrucción:

```c++
std::cout << "Hola, mundo!";
```

### std::endl

La clase `std::endl` se utiliza para imprimir un salto de línea en la consola. Por ejemplo, para imprimir un mensaje en
una nueva línea, se puede utilizar la siguiente instrucción:

```c++
std::cout << "Hola, mundo!" << std::endl;
```

## Ejemplo

A continuación se muestra un ejemplo de un programa simple en C++ que lee un número entero del usuario y lo muestra en
la consola:

```c++
#include <iostream>

int main() {
    int numero;

    std::cout << "Ingrese un número: ";
    std::cin >> numero;

    std::cout << "El número ingresado es: " << numero << std::endl;

    return 0;
}
```

En este ejemplo, el programa solicita al usuario que ingrese un número entero, lee el número ingresado y lo muestra en
la consola.

La biblioteca `<iostream>` es una biblioteca estándar de C++ que proporciona las funciones de entrada y salida estándar,
lo que permite interactuar con el usuario a través de la consola. Al incluir la biblioteca `<iostream>` al inicio del
programa, se pueden utilizar las clases `std::cin` y `std::cout` para leer y mostrar datos en la consola,
respectivamente.