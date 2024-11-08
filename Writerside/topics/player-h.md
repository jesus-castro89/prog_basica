# 8.4. `player.h` y `player.cpp`

Una vez que hemos definido las estructuras `Card` y `Deck`, podemos proceder a implementar la estructura `Player` que
representará a un jugador en el juego de Blackjack.

## `player.h`

El archivo de cabecera `player.h` contendrá la definición de la clase `Player`.

```c++
#ifndef BLACK_JACK_PLAYER_H
#define BLACK_JACK_PLAYER_H

#include "card.h"
#include <string>
#include <vector>
#include <iostream>

struct Player {

    std::string name;
    std::vector<Card> hand;
    int score = 0;

    explicit Player(std::string name);

    void addCard(Card card);

    void showHand() const;
};

#endif
```

En el archivo `player.h`, se define la estructura `Player` que contiene los miembros `name`, `hand` y `score`.

- `name`: representa el nombre del jugador.
- `hand`: vector de cartas en la mano del jugador.
- `score`: puntaje del jugador en el juego.

Las funciones miembro de la clase `Player` son:

- `Player(std::string name)`: constructor de la clase `Player` que inicializa el nombre del jugador.
- `addCard(Card card)`: función miembro que agrega una carta a la mano del jugador.
- `showHand()`: función miembro que muestra las cartas en la mano del jugador.

## `player.cpp`

El archivo `player.cpp` contendrá la implementación de la clase `Player`.

```c++
#include "player.h"

Player::Player(std::string name) : name(std::move(name)) {

    hand.reserve(2);
}

void Player::addCard(Card card) {

    hand.push_back(card);
    score += card.value;
}

void Player::showHand() const {

    std::string handStr = "La mano de " + name + " es: ";
    for (auto &card: hand) {
        handStr += card.getCard() + " ";
    }
    std::cout << handStr << std::endl;
}
```

En el archivo `player.cpp`, se implementan las funciones miembro de la clase `Player`.

- `Player::Player(std::string name)`: constructor de la clase `Player` que inicializa el nombre del jugador y
  reserva espacio para las cartas en la mano.
- `addCard(Card card)`: función miembro que agrega una carta a la mano del jugador y actualiza el puntaje.
- `showHand()`: función miembro que muestra las cartas en la mano del jugador en la consola. La función `getCard()`
  de la clase `Card` se utiliza para obtener la representación de cada carta.

Con la implementación de la clase `Player`, hemos completado la definición de las estructuras básicas necesarias para
el juego de Blackjack. En los siguientes apartados, veremos cómo utilizar estas estructuras para crear el juego
completo.