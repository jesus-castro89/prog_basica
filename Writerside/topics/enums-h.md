# 8.1. La cabecera `enums.h`

Para efectos de nuestro proyecto crearemos en primer lugar tres archivos de cabecerá, uno por cada tipo de enumeración
dentro de nuestro proyecto:

## `suite.h`

```c++
// suite.h
#ifndef SUITE_H
#define SUITE_H

enum class Suite {
    HEARTS,
    DIAMONDS,
    CLUBS,
    SPADES
};

#endif
```

## `figure.h`

```c++
// figure.h
#ifndef FIGURE_H
#define FIGURE_H

enum class Figure {
    TWO = 2,
    THREE,
    FOUR,
    FIVE,
    SIX,
    SEVEN,
    EIGHT,
    NINE,
    TEN,
    JACK,
    QUEEN,
    KING,
    ACE
};

#endif
```

## `winner.h`

```c++
// winner.h
#ifndef WINNER_H
#define WINNER_H

enum class Winner {
    PLAYER,
    DEALER,
    DRAW
};

#endif
```

Estos archivos de cabecera contienen las definiciones de los enumeradores `Suite`, `Figure` y `Winner`,
respectivamente.

Ahora creamos un archivo que concentre todas las definiciones de enumeradores en un solo lugar:

## `enums.h`

```c++
// enums.h
#ifndef ENUMS_H
#define ENUMS_H

#include "suite.h"
#include "figure.h"
#include "winner.h"

#endif
```

El archivo `enums.h` incluye los archivos de cabecera `suite.h`, `figure.h` y `winner.h`, lo que nos permite
acceder a los enumeradores `Suite`, `Figure` y `Winner` desde un solo archivo.

Al utilizar archivos de cabecera, podemos separar la definición de los enumeradores de su implementación, lo que
facilita la organización y mantenimiento de nuestro código.