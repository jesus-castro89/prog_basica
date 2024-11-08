# 8.2. `card.h` y `card.cpp`

En este apartado, se creará una clase `Card` que representará una carta de una baraja de póker. La clase `Card`
hará uso de las enumeraciones `Suite` y `Figure` para representar el palo y la figura de la carta, respectivamente.

## `card.h`

El archivo de cabecera `card.h` contendrá la definición de la clase `Card` y las enumeraciones `Suite` y `Figure`.

```c++
// card.h
#ifndef CARD_H
#define CARD_H

#include "enums.h"

struct Card {
    int value;
    Suite suite;
    Figure figure;
    bool isTaken = false;

    explicit Card(Suite suite, Figure figure);

    [[nodiscard]] std::string getCard() const;

    [[nodiscard]] std::string getSuiteDisplay() const;
};

#endif
```

En el archivo `card.h`, se define la estructura `Card` que contiene los miembros `value`, `suite`, `figure` e
`isTaken`.

- `value`: representa el valor numérico de la carta.
- `suite`: representa el palo de la carta.
- `figure`: representa la figura de la carta.
- `isTaken`: indica si la carta ha sido tomada por un jugador.
- `Card(Suite suite, Figure figure)`: constructor de la clase `Card` que inicializa los miembros `suite` y `figure`.
- `getCard()`: función miembro que devuelve una cadena de texto con la representación de la carta.
- `getSuiteDisplay()`: función miembro que devuelve una cadena de texto con el nombre del palo de la carta.

Para la implementación de la clase `Card`, se creará el archivo `card.cpp`, en el cual deberás de crear la
funcionalidad de los métodos de la clase `Card`.

## `card.cpp`

El archivo `card.cpp` contendrá la implementación de la clase `Card`.

```c++
// card.cpp
#include "card.h"

Card::Card(Suite suite, Figure figure) : suite(suite), figure(figure) {
    switch (figure) {
        case Figure::TWO:
            value = 2;
            break;
        // Casos omitidos para brevedad
        case Figure::NINE:
            value = 9;
            break;
        case Figure::TEN:
        case Figure::JACK:
        case Figure::QUEEN:
        case Figure::KING:
            value = 10;
            break;
        case Figure::ACE:
            value = 11;
            break;
    }
}

std::string Card::getCard() const {
    std::string cardDisplay;
    switch (figure) {
        case Figure::JACK:
            cardDisplay = "J";
            break;
        case Figure::QUEEN:
            cardDisplay = "Q";
            break;
        case Figure::KING:
            cardDisplay = "K";
            break;
        case Figure::ACE:
            cardDisplay = "A";
            break;
        default:
            cardDisplay = std::to_string(value);
            break;
    }
    return cardDisplay + getSuiteDisplay();
}

std::string Card::getSuiteDisplay() const {
    std::string suiteDisplay;
    switch (suite) {
        case Suite::HEARTS:
            suiteDisplay = "(C)";
            break;
        case Suite::DIAMONDS:
            suiteDisplay = "(D)";
            break;
        case Suite::CLUBS:
            suiteDisplay = "(T)";
            break;
        case Suite::SPADES:
            suiteDisplay = "(P)";
            break;
    }

    return suiteDisplay;
}
```

En el archivo `card.cpp`, se implementan los métodos de la clase `Card`:

- El constructor `Card::Card(Suite suite, Figure figure)` inicializa los miembros `suite`, `figure` y `value` de la
  carta.
- La función `Card::getCard()` devuelve una cadena de texto con la representación de la carta. Tomando en cuenta que
  las figuras `JACK`, `QUEEN`, `KING` y `ACE` se representan con las letras `J`, `Q`, `K` y `A`, respectivamente. Y
  qué sus valores numéricos son 10, 10, 10 y 11, respectivamente.
- La función `Card::getSuiteDisplay()` devuelve una cadena de texto con el nombre del palo de la carta.
- Se utiliza un `switch` para asignar el valor numérico de la carta y para obtener la representación de la carta y del
  palo.
- Se utiliza la función `std::to_string()` para convertir el valor numérico de la carta a una cadena de texto.

Con la implementación de la clase `Card`, se ha completado la definición de la estructura y su funcionalidad. En los
siguientes apartados, se continuará con la implementación de las clases `Deck` y `Player`.