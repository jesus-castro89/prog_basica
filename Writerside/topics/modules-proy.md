# 8. Modulación del Proyecto

Para trabajar con nuestro proyecto, crearemos módulos que nos permitan organizar y reutilizar el código de manera
eficiente. En este capítulo, aprenderás a modularizar tu proyecto en C++.

## Crear un Módulo

Un módulo en C++ es un archivo que contiene un conjunto de funciones y variables que pueden ser utilizadas en otros
archivos. Para crear un módulo, simplemente debes escribir tus funciones y variables en un archivo `.cpp` o `.h`.

Por ejemplo, supongamos que tienes un archivo llamado `math.cpp` que contiene las siguientes funciones:

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

Luego, puedes incluir el archivo de cabecera en tu archivo principal para utilizar las funciones del módulo:

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

Al utilizar archivos de cabecera, puedes separar la implementación de las funciones de su declaración, lo que facilita
la reutilización y mantenimiento del código.

## Para nuestro proyecto

Para nuestro proyecto crearemos un conjunto de módulos descritos a continuación:

### `enums.h`

Este módulo contendrá las enumeraciones utilizadas en el proyecto.

> **Nota:** Las enumeraciones son una forma de definir un conjunto de constantes enteras con nombres simbólicos.
> Por ejemplo, para representar los palos de una baraja de cartas, podríamos definir una enumeración `Suit` con los
> valores `Hearts`, `Diamonds`, `Clubs` y `Spades`.

> **Nota:** Las enumeraciones pueden ser trabajadas en archivos de cabecera separados para facilitar su uso en otros
> módulos.

### `card.h` y `card.cpp`

Estos módulos contendrán la definición y la implementación de la clase `Card`, que representa una carta de la baraja.

### `deck.h` y `deck.cpp`

Estos módulos contendrán la definición y la implementación de la clase `Deck`, que representa una baraja de cartas.

### `player.h` y `player.cpp`

Estos módulos contendrán la definición y la implementación de la clase `Player`, que representa un jugador del juego.

### `game.h` y `game.cpp`

Estos módulos contendrán la definición y la implementación de la clase `Game`, que representa el juego de cartas.

Al modularizar nuestro proyecto de esta manera, podremos organizar y reutilizar el código de manera eficiente, lo que
facilitará su mantenimiento y extensión en el futuro.