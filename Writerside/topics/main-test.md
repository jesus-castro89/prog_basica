# 9. Probando el Juego

Ahora que hemos implementado todas las clases y funciones necesarias para nuestro juego de Blackjack, es hora de
probarlo. Para ello, podemos crear un archivo `main.cpp` que incluya las cabeceras de nuestras clases y funciones, y que
implemente la lógica del juego.

```c++
#include "blackjack.h"

int main() {

    BlackJack blackJack;
    blackJack.showTable();
    blackJack.showWinner();
    return 0;
}
```

En este archivo, creamos una instancia de la clase `BlackJack`, mostramos la mesa de juego y luego mostramos al ganador
del juego. Puedes modificar este archivo para agregar más interacciones con el usuario, como permitirle realizar jugadas
o apostar dinero.

Una vez que hayas probado el juego en su forma simple, nos queda hacer algunas mejoras y añadir más funcionalidades
para hacerlo más interesante y entretenido. Por ejemplo, puedes implementar la funcionalidad de apostar, generar una
pseudo-inteligencia para el dealer.