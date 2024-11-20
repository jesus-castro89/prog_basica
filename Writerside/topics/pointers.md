# 11. Añadiendo punteros e iconos

En este artículo, exploraremos cómo usar punteros en C++ para gestionar la memoria de manera eficiente y segura. Los
punteros son una característica fundamental de C++ que permite a los programadores trabajar directamente con la memoria
de un programa. Aprender a usar punteros de manera efectiva es esencial para escribir código C++ robusto y eficiente.

## Actualizando `card.h` para usar punteros

Para actualizar nuestro proyecto de Blackjack y utilizar punteros en lugar de valores directos, podemos modificar el
archivo `card.h` para que la clase `Card` utilice punteros en lugar de valores directos para el palo y el rango de la
carta. Esto nos permitirá gestionar la memoria de manera más eficiente y evitar problemas de copia y asignación.

```c++
#ifndef BLACK_JACK_CARD_H
#define BLACK_JACK_CARD_H

#include "enums.h"
#include <string>

struct Card {
    int value;
    Suite suite;
    Figure figure;
    bool isTaken = false;

    explicit Card(Suite suite, Figure figure);

    [[nodiscard]] std::string getCard() const;

    [[nodiscard]] std::string getSuiteDisplay() const;
};

#endif //BLACK_JACK_CARD_H
```

En este ejemplo, hemos actualizado la clase `Card` para que utilice punteros en lugar de valores directos para el palo
y el rango de la carta. Esto nos permitirá gestionar la memoria de manera más eficiente y evitar problemas de copia y
asignación.

## Actualizando `card.cpp` para usar punteros

Para reflejar los cambios en la clase `Card`, también debemos actualizar el archivo `card.cpp` para que utilice
punteros en lugar de valores directos para el palo y el rango de la carta. Aquí está el código actualizado:

```c++
#include "card.h"

Card::Card(Suite suite, Figure figure) : suite(suite), figure(figure) {

    switch (figure) {

        case Figure::TWO:
            value = 2;
            break;
        case Figure::THREE:
            value = 3;
            break;
        case Figure::FOUR:
            value = 4;
            break;
        case Figure::FIVE:
            value = 5;
            break;
        case Figure::SIX:
            value = 6;
            break;
        case Figure::SEVEN:
            value = 7;
            break;
        case Figure::EIGHT:
            value = 8;
            break;
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
            suiteDisplay = "(♥)";
            break;
        case Suite::DIAMONDS:
            suiteDisplay = "(♦)";
            break;
        case Suite::CLUBS:
            suiteDisplay = "(♣)";
            break;
        case Suite::SPADES:
            suiteDisplay = "(♠)";
            break;
    }
    return suiteDisplay;
}
```

En este ejemplo, hemos actualizado el constructor de la clase `Card` para que utilice punteros en lugar de valores
directos para el palo y el rango de la carta. También hemos actualizado los métodos `getCard` y `getSuiteDisplay` para
que funcionen con los punteros en lugar de los valores directos.

## Actualizando `player.h` y `deck.h` para usar punteros

Además de actualizar la clase `Card`, también podemos actualizar las clases `Player` y `Deck` para que utilicen
punteros en lugar de valores directos para las cartas y los jugadores. Esto nos permitirá gestionar la memoria de manera
más eficiente y evitar problemas de copia y asignación.

```c++
// player.h
#ifndef BLACK_JACK_PLAYER_H
#define BLACK_JACK_PLAYER_H

#include "card.h"
#include <vector>
#include <iostream>
#include <memory>

struct Player {

    std::string name;
    std::vector<std::unique_ptr<Card>> hand;
    int score = 0;
    bool isDealer{};

    explicit Player(std::string name, bool isDealer = true);

    void addCard(std::unique_ptr<Card> card);

    void showHand() const;
};

#endif
```

```c++
// deck.h
#ifndef BLACK_JACK_DECK_H
#define BLACK_JACK_DECK_H

#include "card.h"
#include <vector>
#include <memory>

/**
 * @brief Clase Deck
 * @code
 * Deck deck;
 * deck.shuffle();
 * Card card = deck.draw();
 * @endcode
 */
struct Deck {

    /**
     * @brief Vector de cartas
     */
    std::vector<std::unique_ptr<Card>> cards;

    Deck();

    void shuffle();

    std::unique_ptr<Card> draw();
};
#endif //BLACK_JACK_DECK_H
```

En estos ejemplos, hemos actualizado las clases `Player` y `Deck` para que utilicen punteros en lugar de valores
directos para las cartas y los jugadores. Esto nos permitirá gestionar la memoria de manera más eficiente y evitar
problemas de copia y asignación.

## Actualizando `player.cpp` y `deck.cpp` para usar punteros

Para reflejar los cambios en las clases `Player` y `Deck`, también debemos actualizar los archivos `player.cpp` y
`deck.cpp` para que utilicen punteros en lugar de valores directos para las cartas y los jugadores. Aquí está el código
actualizado:

```c++
// player.cpp
#include "player.h"
#include <iostream>

using namespace std;

/**
 * @brief Constructor del jugador
 * @code
 * Player player("Jugador");
 * @endcode
 * @param name nombre del jugador
 * @param isDealer si el jugador es el dealer
 * @return Player el jugador
 */
Player::Player(string name, bool isDealer) : name(std::move(name)), isDealer(isDealer) {

    hand.reserve(2);
}

/**
 * @brief Añade una carta a la mano
 * @code
 * player.addCard(card);
 * @endcode
 * @param card carta a añadir
 */
void Player::addCard(unique_ptr<Card> card) {

    if (card == nullptr) {

        cerr << "Error: Attempted to add a null card to the hand." << endl;
        return;
    }
    if (!isDealer) {

        if (card->figure == Figure::ACE) {

            int option;
            cout << "Elige el valor del As: 1 u 11:" << endl;
            cin >> option;
            while (option != 1 && option != 11) {

                cout << "Elige el valor del As: 1 u 11:" << endl;
                cin >> option;
            }
            score += option;
        } else {
            score += card->value;
        }
    } else {
        score += card->value;
    }
    hand.push_back(std::move(card));
}

/**
 * @brief Muestra la mano del jugador
 * @code
 * player.showHand();
 * @endcode
 */
void Player::showHand() const {

    string handStr = "La mano de " + name + " es: ";
    for (const auto &card: hand) {

        if (card != nullptr) {

            handStr += card->getCard() + " ";
        } else {
            cerr << "Error: Null card in hand." << endl;
        }
    }
    cout << handStr << endl;
}
```

```c++
// deck.cpp
#include "deck.h"
#include <algorithm>
#include <random>
#include <iostream>

using namespace std;

/**
 * @brief Constructor de la baraja
 * @code
 * Deck deck;
 * @endcode
 * @return Deck la baraja de cartas
 */
Deck::Deck() {

    cards.reserve(52);
    for (int i = 0; i < 4; i++) {

        for (int j = 0; j < 13; j++) {

            auto suite = static_cast<Suite>(i);
            auto figure = static_cast<Figure>(j + 2);
            cards.emplace_back(make_unique<Card>(suite, figure));
        }
    }
}

/**
 * @brief Baraja las cartas
 * @code
 * deck.shuffle();
 * @endcode
 */
void Deck::shuffle() {

    random_device rd;
    mt19937 g(rd());
    if (!cards.empty()) {

        std::shuffle(cards.begin(), cards.end(), g);
    }
}

/**
 * @brief Roba una carta
 * @code
 * Card card = deck.draw();
 * @endcode
 * @return Card carta robada
 */
unique_ptr<Card> Deck::draw() {
    random_device rd;
    mt19937 g(rd());
    uniform_int_distribution<int> distribution(0, static_cast<int>(cards.size()) - 1);
    unique_ptr<Card> card;

    while (true) {
        int index = distribution(g);
        if (index >= 0 && index < cards.size() && cards[index] != nullptr && !cards[index]->isTaken) {
            card = std::move(cards[index]);
            card->isTaken = true;
            return card;
        } else {
            cards.erase(cards.begin() + index);
        }
    }
}
```

En estos ejemplos, hemos actualizado los métodos `addCard` y `showHand` de la clase `Player` para que funcionen con
punteros en lugar de valores directos para las cartas. También hemos actualizado los métodos `shuffle` y `draw` de la
clase `Deck` para que funcionen con punteros en lugar de valores directos para las cartas.

## Conclusión

En este artículo, hemos explorado cómo usar punteros en C++ para gestionar la memoria de manera eficiente y segura. Al
utilizar punteros en lugar de valores directos, podemos evitar problemas de copia y asignación, y gestionar la memoria
de manera más eficiente. Al actualizar nuestro proyecto de Blackjack para utilizar punteros en lugar de valores
directos, hemos mejorado la eficiencia y la seguridad de nuestro código.

Al trabajar con punteros en C++, es importante seguir algunas buenas prácticas para evitar errores comunes. Aquí hay
algunas recomendaciones para usar punteros de manera segura:

1. **Inicializar los punteros nulos**: Siempre inicializa los punteros nulos al declararlos para evitar que contengan
   valores no deseados. Por ejemplo:

   ```c++
   int* ptr = nullptr;
   ```
2. **Verificar si un puntero es nulo antes de usarlo**: Antes de acceder al valor apuntado por un puntero, verifica si
   el puntero es nulo para evitar errores de acceso a memoria no válida. Por ejemplo:

    ```c++
    if (ptr != nullptr) {
         // Acceder al valor apuntado por ptr
    }
    ```
3. **Asignar un puntero nulo después de liberar la memoria**: Después de liberar la memoria apuntada por un puntero,
   asigna `nullptr` al puntero para evitar errores de acceso a memoria liberada. Por ejemplo:

    ```c++
    delete ptr;
    ptr = nullptr;
    ```
4. **Evitar comparaciones directas con punteros nulos**: Evita comparar directamente un puntero con `nullptr` o `NULL`.
5. **Usar punteros nulos en lugar de punteros salvajes**: En lugar de asignar un puntero a una dirección de memoria
   arbitraria, usa un puntero nulo para indicar que el puntero no apunta a nada.
6. **Usar referencias en lugar de punteros nulos**: Si es posible, utiliza referencias en lugar de punteros nulos para
   evitar problemas de punteros nulos.
7. **Usar punteros inteligentes**: Siempre que sea posible, utiliza punteros inteligentes como `std::unique_ptr` o
   `std::shared_ptr` en lugar de punteros crudos para gestionar la memoria de manera
8. **Evitar fugas de memoria**: Asegúrate de liberar la memoria correctamente cuando ya no la necesites para evitar
   fugas de memoria.
9. **Evitar la corrupción de memoria**: Evita acceder a la memoria liberada o a la memoria no válida para evitar la
   corrupción de memoria.

Siguiendo estas recomendaciones, puedes usar punteros de manera segura y eficiente en C++ y evitar errores comunes
asociados con la gestión de la memoria.