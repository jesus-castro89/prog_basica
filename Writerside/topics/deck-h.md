# 8.3. `deck.h` y `deck.cpp`

Una vez que hemos definido las estructura `Card` y las enumeraciones `Suite` y `Figure`, podemos proceder a implementar
la estructura `Deck` que representará una baraja de cartas.

## `deck.h`

El archivo de cabecera `deck.h` contendrá la definición de la clase `Deck` y las enumeraciones `Suite` y `Figure`.

```c++
#ifndef BLACK_JACK_DECK_H
#define BLACK_JACK_DECK_H

#include "card.h"
#include <vector>
#include <random>
#include <algorithm>

struct Deck {

    /**
     * @brief Vector de cartas
     */
    std::vector<Card> cards;

    Deck();

    void shuffle();

    Card draw();
};

#endif //BLACK_JACK_DECK_H
```

En el archivo `deck.h`, se define la estructura `Deck` que contiene el miembro `cards`.

Las funciones miembro de la clase `Deck` son:

- `Deck()`: constructor de la clase `Deck` que inicializa el vector de cartas.
- `shuffle()`: función miembro que mezcla las cartas del mazo.
- `draw()`: función miembro que extrae una carta del mazo y la devuelve.

## `deck.cpp`

El archivo `deck.cpp` contendrá la implementación de la clase `Deck`.

```c++
#include "deck.h"

using namespace std;

Deck::Deck() {

    cards.reserve(52);
    for (int i = 0; i < 4; i++) {

        for (int j = 0; j < 13; j++) {

            auto suite = static_cast<Suite>(i);
            auto figure = static_cast<Figure>(j + 2);
            cards.emplace_back(suite, figure);
        }
    }
}

void Deck::shuffle() {

    random_device rd;
    mt19937 g(rd());
    std::shuffle(cards.begin(), cards.end(), g);
}

Card Deck::draw() {

    random_device rd;
    mt19937 g(rd());
    uniform_int_distribution<int> distribution(0, (int) cards.size() - 1);
    int index;
    Card card = cards[0];
    do {
    
        index = distribution(g);
        card = cards[index];
    } while (card.isTaken);
    card.isTaken = true;
    return card;
}
```

En el archivo `deck.cpp`, se implementan las funciones miembro de la clase `Deck`.

- El constructor `Deck()` inicializa el vector de cartas con las 52 cartas de la baraja. Se utilizan dos bucles `for`
  para recorrer los palos y las figuras de las cartas y se añaden al vector.
- La función `shuffle()` mezcla las cartas del mazo. Para ello, se utiliza un generador de números aleatorios y la
  función `std::shuffle` de la biblioteca estándar.
- La función `draw()` extrae una carta aleatoria del mazo y la devuelve. Para ello, se utiliza un generador de números
  aleatorios y la función `std::uniform_int_distribution` para obtener un índice aleatorio en el rango de cartas
  disponibles. Se verifica que la carta no haya sido tomada previamente y se marca como tomada antes de devolverla.

Con la implementación de la clase `Deck`, ahora tenemos una forma de representar una baraja de cartas y realizar
operaciones como mezclar las cartas y extraer cartas aleatorias del mazo. Estas funcionalidades serán útiles para
implementar el juego de blackjack en nuestro proyecto.