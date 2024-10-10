# 5. La función de cartas aleatorias

Es este apartado veremos cómo podemos generar cartas aleatorias en un juego de cartas. Para ello, utilizaremos la
función `rand()` de la librería `random` de C++.

## 5.1. Generando cartas aleatorias

Para efectos del punto actual del proyecto, vamos a generar una función que devuelva un valor aleatorio entre 2 y 11,
que representará el valor de una carta en un juego de cartas. Para ello, vamos a utilizar el siguiente código:

```c++
#include <iostream>
#include <random>
#include <string>

using namespace std;

int drawCard() {
    random_device rd;
    mt19937 gen(rd());
    uniform_int_distribution<int> dist(2, 11);
    return dist(gen);
}
```

Dónde:

- `random_device rd;`: Se crea un dispositivo de generación de números aleatorios.
- `mt19937 gen(rd());`: Se crea un generador de números aleatorios con una semilla aleatoria.
- `uniform_int_distribution<int> dist(2, 11);`: Se crea una distribución uniforme de números enteros entre 2 y 11.
- `return dist(gen);`: Se devuelve un número aleatorio entre 2 y 11.
- `drawCard()`: Es la función que genera un número aleatorio entre 2 y 11.
- `int`: Es el tipo de dato que devuelve la función.
- `using namespace std;`: Se utiliza para no tener que escribir `std::` antes de cada función de la librería estándar.

## 5.2. Probando la función

Para probar la función `drawCard()`, podemos escribir el siguiente código:

```c++
#include <iostream>
#include <random>
#include <string>

using namespace std;

int drawCard() {
    random_device rd;
    mt19937 gen(rd());
    uniform_int_distribution<int> dist(2, 11);
    return dist(gen);
}

int main() {
    cout << "Carta: " << drawCard() << endl;
    return 0;
}
```

## 5.3. Juego Rápido de Cartas

Para efectos de nuestro primer juego, vamos a hacer que tanto el jugador como la computadora reciban dos cartas
aleatorias y se muestre el valor de las cartas en pantalla. Para ello, vamos a utilizar el siguiente código:

```c++
#include <iostream>
#include <random>
#include <string>

using namespace std;

int drawCard() {
    random_device rd;
    mt19937 gen(rd());
    uniform_int_distribution<int> dist(2, 11);
    return dist(gen);
}

int main() {
    int playerCard1 = drawCard();
    int playerCard2 = drawCard();
    int computerCard1 = drawCard();
    int computerCard2 = drawCard();

    cout << "Jugador: " << playerCard1 << " " << playerCard2 << endl;
    cout << "Computadora: " << computerCard1 << " " << computerCard2 << endl;

    return 0;
}
```

En este código, se generan dos cartas aleatorias para el jugador y dos cartas aleatorias para la computadora. Luego, se
muestran en pantalla los valores de las cartas de ambos jugadores.

## 5.5. Conclusiones

En este apartado, aprendimos cómo generar cartas aleatorias en un juego de cartas utilizando la función `rand()` de la
librería `random` de C++. Además, aprendimos cómo utilizar la función `drawCard()` para generar un número aleatorio
entre 2 y 11 y cómo probar la función en un programa de prueba. Finalmente, aprendimos cómo hacer que tanto el jugador
como la computadora reciban dos cartas aleatorias y se muestre el valor de las cartas en pantalla.

En el siguiente apartado, veremos cómo podemos hacer que el jugador pueda pedir más cartas en un juego de cartas.