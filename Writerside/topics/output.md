# 10. Configurando la salida de datos

En muchas ocasiones, necesitamos configurar la salida de datos para que acepte o trabaje con cierto juego de caracteres
específico. Por ejemplo, si estamos trabajando con caracteres especiales o emojis, es posible que necesitemos configurar
la salida de datos para que los muestre correctamente.

En C++, podemos configurar la salida de datos utilizando la función `imbue` de la clase `std::locale`. Esta función
nos permite establecer una configuración específica para la salida de datos, como el juego de caracteres a utilizar o
el formato de los números.

A continuación, se muestra un ejemplo de cómo configurar la salida de datos para que acepte caracteres especiales:

```c++
#include <iostream>
#include <codecvt>
#include <string>

#ifdef _WIN32

#include <windows.h>

#endif

int main() {

    // Configurar la localización para UTF-8 si se está en Windows o Linux
#ifdef _WIN32
    SetConsoleOutputCP(CP_UTF8);
#endif
    // Configurar la localización para UTF-8
    std::locale::global(std::locale(std::locale(), new std::codecvt_utf8<wchar_t>));
    // Configurar la salida estándar para aceptar caracteres especiales
    std::wcout.imbue(std::locale());
}
```

En este ejemplo, configuramos la salida de datos para que acepte caracteres especiales utilizando la función `imbue` de
la clase `std::locale`. También utilizamos la función `codecvt_utf8` para convertir los caracteres a UTF-8 y mostrarlos
correctamente en la salida estándar.

Al configurar la salida de datos de esta manera, podemos trabajar con caracteres especiales y emojis en C++ de manera
sencilla y eficiente.

## Actualizando el proyecto para establecer la salida de datos

Para actualizar nuestro proyecto de Blackjack y establecer la salida de datos para aceptar caracteres especiales,
podemos agregar el código anterior al archivo `blackjack.cpp` o al archivo principal de nuestro proyecto. De esta 
manera, podremos mostrar mensajes y texto en la consola con caracteres especiales y emojis si es necesario.

```c++
#include "blackjack.h"
#include "deck.h"
#include <string>
#include <iostream>
#include <codecvt>

#ifdef _WIN32

#include <windows.h>

#endif

using namespace std;

int money = 100;

int *moneyPtr = &money;

BlackJack::BlackJack() {

    // Configurar la localización para UTF-8 si se está en Windows o Linux
#ifdef _WIN32
    SetConsoleOutputCP(CP_UTF8);
#endif
    // Configurar la localización para UTF-8
    std::locale::global(std::locale(std::locale(), new std::codecvt_utf8<wchar_t>));
    std::wcout.imbue(std::locale());
    //
    deck.shuffle();
    player.addCard(deck.draw());
    player.addCard(deck.draw());
    dealer.addCard(deck.draw());
    dealer.addCard(deck.draw());
    showTable();
    playerTurn();
    dealerTurn();
    showWinner();
    play();
}

void BlackJack::play() {

    string option;
    do {

        cout << "Dinero: " << money << endl;
        cout << "¿Quieres jugar otra vez? (s/n): ";
        cin >> option;
        if (option == "s") {

            deck = Deck();
            deck.shuffle();
            player.hand.clear();
            dealer.hand.clear();
            player.score = 0;
            dealer.score = 0;
            player.addCard(deck.draw());
            player.addCard(deck.draw());
            dealer.addCard(deck.draw());
            dealer.addCard(deck.draw());
            showTable();
            playerTurn();
            dealerTurn();
            showWinner();
        }
    } while (option == "s" && *moneyPtr > 0);
    cout << "Gracias por jugar" << endl;
}

void BlackJack::showTable() const {

    player.showHand();
    dealer.showHand();
}

void BlackJack::playerTurn() {

    string option;
    if (player.score < 21) {
        do {
            cout << "¿Quieres otra carta? (s/n): ";
            cin >> option;
            if (option == "s") {
                player.addCard(deck.draw());
                player.showHand();
            }
            if (player.score > 21) {
                break;
            }
        } while (option == "s");
    }
}

void BlackJack::dealerTurn() {

    while (dealer.score < 17) {
        dealer.addCard(deck.draw());
    }
    dealer.showHand();
}

[[nodiscard]] Winner BlackJack::getWinner() const {

    if (player.score > 21) {

        if (dealer.score > 21) {
            return Winner::DRAW;
        } else {
            *moneyPtr -= 10;
            return Winner::DEALER;
        }
    } else {
        if (player.score == 21 || dealer.score > 21) {
            *moneyPtr += 10;
            return Winner::PLAYER;
        } else {
            if (player.score > dealer.score) {
                *moneyPtr += 10;
                return Winner::PLAYER;
            } else if (player.score < dealer.score) {
                *moneyPtr -= 10;
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

En este ejemplo, hemos agregado el código para configurar la salida de datos en el constructor de la clase `BlackJack`.

Al hacerlo, podemos mostrar mensajes y texto con caracteres especiales y emojis en la consola de manera correcta.
Además, hemos actualizado el método `play` para que el juego continúe mientras el jugador tenga dinero disponible.

Al configurar la salida de datos de esta manera, podemos mejorar la presentación y la experiencia del usuario en nuestro
proyecto de Blackjack.

Con esto, hemos finalizado la implementación de nuestro proyecto de Blackjack en C++. Hemos explorado cómo diseñar e
implementar las clases y funciones necesarias para el juego, así como cómo configurar la salida de datos para aceptar
caracteres especiales y emojis.