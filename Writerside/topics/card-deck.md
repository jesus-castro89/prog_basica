# 6. El Arreglo de Cartas y la Baraja

En el código anterior, hemos utilizado la función `drawCard()` para obtener cartas aleatorias. Sin embargo, para poder
realizar un juego de cartas más completo, necesitamos tener un conjunto de cartas que podamos barajar y repartir a los
jugadores. Para ello, vamos a utilizar un arreglo de cartas que represente una baraja de cartas.

## 6.1. Creando el Arreglo de Cartas

Para crear un arreglo de cartas, vamos a utilizar un arreglo de enteros que representen los valores de las cartas. En
este caso, vamos a utilizar un arreglo de 52 elementos, donde cada elemento representa una carta del 2 al 11. Para
crear el arreglo de cartas, tomando en cuenta que cada carta tiene un valor del 2 al 11, podemos utilizar el siguiente
código:

![Código para crear un arreglo de cartas](cards.png)

En este código, se crea un arreglo de 52 elementos, donde cada elemento representa una carta del 2 al 11. Para llenar
el arreglo, se utiliza un bucle `for` que recorrer cada uno de los palos o figuras de la baraja (corazones, diamantes,
tréboles y picas) y para cada palo, se llena el arreglo con las cartas del 2 al 11. Teniendo en cuenta que la J, Q, K,
valen 10 y el As vale 11, el arreglo de cartas se llena de la siguiente manera:

- Corazones: 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, As
- Diamantes: 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, As
- Tréboles: 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, As
- Picas: 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, As

## 6.2. Barajando el Arreglo de Cartas

Una vez que tenemos el arreglo de cartas, podemos barajarlo para obtener una baraja de cartas aleatoria. Para ello,
podemos utilizar la función `shuffle()` de la librería `algorithm` de C++. Para barajar el arreglo de cartas, podemos
utilizar el siguiente código:

```c++
void shuffleDeck() {

    random_device rd;
    mt19937 gen(rd());
    shuffle(begin(cards), end(cards), gen);
}
```

En este código, se utiliza la función `shuffle()` de la librería `algorithm` de C++ para barajar el arreglo de cartas.
La función `shuffle()` recibe tres parámetros:

- `begin(cards)`: Es un iterador que apunta al primer elemento del arreglo de cartas.
- `end(cards)`: Es un iterador que apunta al último elemento del arreglo de cartas.
- `gen`: Es el generador de números aleatorios que se utiliza para barajar el arreglo de cartas.

> **Nota**: Para utilizar la función `shuffle()`, es necesario incluir la librería `algorithm` en el código.

> **Nota**: Un Iterador es un objeto que permite recorrer una secuencia de elementos. En este caso, el iterador
> `begin(cards)` apunta al primer elemento del arreglo de cartas y el iterador `end(cards)` apunta al último
> elemento del arreglo de cartas.

## 6.3. Probando la Baraja de Cartas

Como evidencia de que la baraja de cartas se ha barajado correctamente, deberás de crear las funciones que permitan
asignar dos cartas tanto al jugador como al dealer y posteriormente mostrar las cartas en pantalla. Y determinar al
ganador de la ronda teniendo en cuenta lo siguiente:

* El jugador gana si tiene 21 puntos.
* Si el jugador tiene más de 21 puntos, pierde.
* Si el jugador tiene menos de 21 puntos, pero más que el dealer, gana.
* Si el jugador tiene menos de 21 puntos, pero menos que el dealer, pierde.
* Si el jugador y el dealer tienen la misma cantidad de puntos, es un empate.