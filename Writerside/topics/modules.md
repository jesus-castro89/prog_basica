# Los Módulos

Los módulos son una forma de organizar y reutilizar código en C++. Un módulo es un archivo que contiene un conjunto de
funciones y variables que pueden ser utilizadas en otros archivos. En este tutorial, aprenderás cómo crear y
utilizar módulos en C++.

## Crear un Módulo

Para crear un módulo en C++, simplemente debes escribir tus funciones y variables en un archivo `.cpp` o `.h`. Por
ejemplo, supongamos que tienes un archivo llamado `math.cpp` que contiene las siguientes funciones:

```c++
// math.cpp

int sum(int a, int b) {
    return a + b;
}

int multiply(int a, int b) {
    return a * b;
}
```

Para utilizar estas funciones en otro archivo, simplemente debes incluir el archivo `math.cpp` en tu archivo principal.
Por ejemplo, si tienes un archivo llamado `main.cpp` que utiliza las funciones del módulo `math.cpp`, puedes hacerlo de
la siguiente manera:

```c++
// main.cpp

#include "math.cpp"

int main() {
    int a = 5;
    int b = 10;

    int result = sum(a, b);
    std::cout << "Sum: " << result << std::endl;

    result = multiply(a, b);
    std::cout << "Multiplication: " << result << std::endl;

    return 0;
}
```

## Archivos de Cabecera

En lugar de incluir directamente el archivo `.cpp`, es una buena práctica utilizar un archivo de cabecera (`.h`) para
declarar las funciones y variables que se encuentran en el módulo. Por ejemplo, puedes crear un archivo `math.h` que
contenga las declaraciones de las funciones del módulo `math.cpp`:

```c++
// math.h

#ifndef MATH_H
#define MATH_H

int sum(int a, int b);

int multiply(int a, int b);

#endif
```

Luego, puedes incluir el archivo de cabecera en tu archivo principal en lugar del archivo `.cpp`:

```c++
// main.cpp

#include "math.h"

int main() {
    int a = 5;
    int b = 10;

    int result = sum(a, b);
    std::cout << "Sum: " << result << std::endl;

    result = multiply(a, b);
    std::cout << "Multiplication: " << result << std::endl;

    return 0;
}
```

En algunas ocasiones cuando debes usar otras librerías dentro de tu módulo, es posible que necesites incluir las
cabeceras de esas librerías en tu archivo de cabecera. Por ejemplo, si tu módulo utiliza la librería `iostream`, debes
incluir la cabecera correspondiente en tu archivo de cabecera:

```c++
// math.h

#ifndef MATH_H
#define MATH_H

#include <iostream>

int sum(int a, int b);

int multiply(int a, int b);

#endif
```

## Espacios de Nombres

Para evitar conflictos de nombres entre diferentes módulos, es una buena práctica utilizar espacios de nombres. Puedes
definir un espacio de nombres para tus funciones y variables en tu archivo de cabecera o en tu archivo `.cpp`. Por
ejemplo, puedes definir un espacio de nombres llamado `math` para tus funciones en el archivo `math.h`:

```c++
// math.h

#ifndef MATH_H
#define MATH_H

#include <iostream>

namespace math {
    int sum(int a, int b);

    int multiply(int a, int b);
}

#endif
```

## Compilar un Módulo

Para compilar un programa que utiliza módulos en C++, debes compilar todos los archivos `.cpp` que contienen las
funciones y variables que necesitas. Por ejemplo, para compilar el programa anterior, puedes hacerlo de la siguiente
manera:

```bash
g++ main.cpp math.cpp -o main
```

Esto compilará los archivos `main.cpp` y `math.cpp` y generará un archivo ejecutable llamado `main`.

> **Nota**: CLion y otros IDEs modernos pueden manejar la compilación de módulos automáticamente, por lo que no
> necesitas preocuparte por esto en la mayoría de los casos.

## Conclusión

Los módulos son una forma poderosa de organizar y reutilizar código en C++. Al dividir tu código en módulos, puedes
facilitar su mantenimiento y reutilización en diferentes partes de tu proyecto. ¡Esperamos que este tutorial te haya
sido útil!