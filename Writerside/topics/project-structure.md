# 7. Reestructurando el proyecto

Para nuestro proyecto manejaremos las siguientes estructuras:

* Enums:
    * Winner: Representa al ganador de una ronda.
    * Suit: Representa los palos de una baraja de cartas.
    * Figure: Representa las figuras de una baraja de cartas (J, Q, K, A).
* Structs
    * Card: Representa una carta de una baraja de cartas.
    * Player: Representa un jugador de la partida.
    * Deck: Representa una baraja de cartas.
    * BlackJack: Representa el juego de BlackJack.

## Enums

### Winner

El Enum `Winner` representa al ganador de una ronda. Puede tener los siguientes valores:

* `PLAYER`: El jugador ha ganado la ronda.
* `DEALER`: El dealer ha ganado la ronda.
* `DRAW`: La ronda ha terminado en empate.

```c++
enum class Winner {
    PLAYER,
    DEALER,
    DRAW
};
```

### Suit

El Enum `Suit` representa los palos de una baraja de cartas. Puede tener los siguientes valores:

* `HEARTS`: Corazones.
* `DIAMONDS`: Diamantes.
* `CLUBS`: Tréboles.
* `SPADES`: Picas.

```c++
enum class Suit {
    HEARTS,
    DIAMONDS,
    CLUBS,
    SPADES
};
```

### Figure

El Enum `Figure` representa las figuras de una baraja de cartas. Puede tener los siguientes valores:

* `N`: Dónde N es el número de carta en Inglés.
    * Por ejemplo: `TWO`, `THREE`, hasta llegar a `TEN`.
* `JACK`: Jota.
* `QUEEN`: Reina.
* `KING`: Rey.
* `ACE`: As.

```c++
enum class Figure {
    TWO=2,
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
```

## Structs

### Card

La estructura `Card` representa una carta de una baraja de cartas. Tiene los siguientes campos:

* `value`: Valor de la carta (2 al 11).
* `suit`: Palo de la carta.
* `figure`: Figura de la carta.
* `isTaken`: Indica si la carta ha sido tomada por un jugador.

Esta estructura deberá de contar con los siguientes métodos:

* `getCard()` Devuelve la carta en formato de texto.
* `getSuite()` Devuelve el palo de la carta en formato de texto.

Y los siguientes constructores:

* `Card()`: Constructor por defecto.
* `Card(Figure figure, Suit suit)`: Constructor que recibe la figura y el palo de la carta.

Por lo que la estructura `Card` se vería de la siguiente manera:

```c++
struct Card {
    int value;
    Suit suit;
    Figure figure;
    bool isTaken;

    std::string getCard();
    std::string getSuite();

    Card();
    explicit Card(Figure figure, Suit suit);
};
```

### Player

La estructura `Player` representa un jugador de la partida. Tiene los siguientes campos:

* `score`: Puntos del jugador.
* `cards`: Vector de cartas del jugador.
* `name`: Nombre del jugador.

Esta estructura deberá de contar con los siguientes métodos:

* `addCard(Card card)`: Añade una carta al jugador.
* `showHand()`: Muestra las cartas del jugador en pantalla.

Y los siguientes constructores:

* `Player()`: Constructor por defecto.
* `explicit Player(string name)`: Constructor que recibe el nombre del jugador.}

Por lo que la estructura `Player` se vería de la siguiente manera:

```c++
struct Player {
    int score;
    std::vector<Card> cards;
    std::string name;

    void addCard(Card card);
    void showHand();

    Player();
    explicit Player(std::string name);
};
```

### Deck

La estructura `Deck` representa una baraja de cartas. Tiene los siguientes campos:

* `cards`: Vector de cartas de la baraja.

Esta estructura deberá de contar con los siguientes métodos:

* `shuffleDeck()`: Baraja la baraja de cartas.
* `drawCard()`: Reparte una carta de la baraja.

Y los siguientes constructores:

* `Deck()`: Constructor por defecto que creará una nueva baraja de cartas.

Con estas estructuras y métodos, podremos manejar de manera más eficiente las cartas, jugadores y barajas de cartas en
nuestro proyecto.

Por lo que la estructura `Deck` se vería de la siguiente manera:

```c++
struct Deck {
    std::vector<Card> cards;

    void shuffleDeck();
    Card drawCard();

    Deck();
};
```

### BlackJack

La estructura `BlackJack` representa el juego de BlackJack. Tiene los siguientes campos:

* `deck`: Baraja de cartas.
* `player`: Jugador.
* `dealer`: Dealer.

Esta estructura deberá de contar con los siguientes métodos:

* `startGame()`: Inicia el juego.
* `showTable()`: Muestra la mesa de juego. (La manos de los jugadores)
* `showWinner()`: Muestra al ganador de la ronda.

Y los siguientes constructores:

* `BlackJack()`: Constructor por defecto que creará un nuevo juego de BlackJack.

Por lo que la estructura `BlackJack` se vería de la siguiente manera:

```c++
struct BlackJack {
    Deck deck;
    Player player;
    Player dealer;

    void startGame();
    void showTable();
    void showWinner();

    BlackJack();
};
```