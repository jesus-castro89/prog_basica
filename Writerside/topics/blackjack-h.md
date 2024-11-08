# 8.5. `blackjack.h` y `blackjack.cpp`

Una vez que hemos definido las estructuras `Card`, `Deck` y `Player`, podemos proceder a implementar la estructura
`Blackjack` que representará el juego de Blackjack.

## `blackjack.h`

El archivo de cabecera `blackjack.h` contendrá la definición de la clase `Blackjack`.

```c++
#ifndef BLACK_JACK_BLACKJACK_H
#define BLACK_JACK_BLACKJACK_H

#include "deck.h"
#include "player.h"
#include <string>
#include <iostream>

struct BlackJack {

    Player player = Player("Jugador");
    Player dealer = Player("Dealer");
    Deck deck;

    BlackJack();

    void showTable() const;

    void playerTurn();

    void dealerTurn();

    [[nodiscard]] Winner getWinner() const;

    void showWinner() const;
};

#endif
```

En el archivo `blackjack.h`, se define la estructura `BlackJack` que contiene los miembros `player`, `dealer`
y `deck`.

Las funciones miembro de la clase `BlackJack` son:

- `BlackJack()`: constructor de la clase `BlackJack` que inicializa los jugadores y la baraja.
- `showTable()`: función miembro que muestra la mesa de juego.
- `playerTurn()`: función miembro que representa el turno del jugador.
- `dealerTurn()`: función miembro que representa el turno del dealer.
- `getWinner()`: función miembro que determina al ganador del juego.
- `showWinner()`: función miembro que muestra al ganador del juego.

## `blackjack.cpp`

El archivo `blackjack.cpp` contendrá la implementación de la clase `BlackJack`.

```c++
#include "blackjack.h"
#include "deck.h"
#include <string>
#include <iostream>

using namespace std;

BlackJack::BlackJack() {

    deck.shuffle();
    player.addCard(deck.draw());
    player.addCard(deck.draw());
    dealer.addCard(deck.draw());
    dealer.addCard(deck.draw());
}

void BlackJack::showTable() const {

    player.showHand();
    dealer.showHand();
}

void BlackJack::playerTurn() {

}

void BlackJack::dealerTurn() {

}

[[nodiscard]] Winner BlackJack::getWinner() const {

    if (player.score > 21) {
        return Winner::DEALER;
    } else {
        if (player.score == 21) {
            return Winner::PLAYER;
        } else {
            if (player.score > dealer.score) {
                return Winner::PLAYER;
            } else if (player.score < dealer.score) {
                return Winner::DEALER;
            } else {
                return Winner::DRAW;
            }
        }
    }
}

void BlackJack::showWinner() const {

    string winner = "El ganador es: ";
    switch (getWinner()) {
        case Winner::PLAYER:
            winner += player.name;
            break;
        case Winner::DEALER:
            winner += dealer.name;
            break;
        case Winner::DRAW:
            winner += "Empate";
            break;
    }
    cout << winner << endl;
}
```

En el archivo `blackjack.cpp`, se implementan las funciones miembro de la clase `BlackJack`.

- `BlackJack::BlackJack()`: constructor de la clase `BlackJack` que inicializa los jugadores y la baraja. Se reparten
  dos cartas a cada jugador.
- `showTable()`: función miembro que muestra la mesa de juego. Muestra las cartas de los jugadores.
- `playerTurn()`: función miembro que representa el turno del jugador. El jugador puede pedir una carta o plantarse.
- `dealerTurn()`: función miembro que representa el turno del dealer. El dealer pide cartas hasta alcanzar un puntaje
  mayor o igual a 17.
- `getWinner()`: función miembro que determina al ganador del juego. Compara los puntajes de los jugadores y decide el
  ganador.
- `showWinner()`: función miembro que muestra al ganador del juego. Imprime en consola el nombre del ganador o si hay
  empate.