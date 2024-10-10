# 2.- El Pseudocódigo del Proyecto

## 2.1.- Introducción

El pseudocódigo es una herramienta útil para planificar y diseñar un programa antes de comenzar a escribir el código
real. En este documento, se presentará el pseudocódigo para el proyecto integrador, que consiste en la creación de un
juego de Blackjack en C++. El juego permitirá a un jugador humano jugar contra la computadora y seguir las reglas
básicas del Blackjack.

## 2.2.- Pseudocódigo

A continuación, se presenta el pseudocódigo para el juego de Blackjack en C++:

```
Inicio del juego
    Crear una baraja de cartas
    Barajar las cartas
    Repartir dos cartas al jugador
    Repartir dos cartas a la computadora
    Mostrar las cartas del jugador
    Mostrar una carta de la computadora
    Mientras el jugador quiera pedir cartas adicionales
        Pedir una carta adicional al jugador
        Mostrar las cartas del jugador
        Calcular el puntaje del jugador
        Si el puntaje del jugador es mayor a 21
            Mostrar que el jugador ha perdido
            Terminar el juego
        Si el puntaje del jugador es igual a 21
            Mostrar que el jugador ha ganado
            Terminar el juego
    Fin del bucle
    Mientras la computadora quiera pedir cartas adicionales
        Pedir una carta adicional a la computadora
        Mostrar las cartas de la computadora
        Calcular el puntaje de la computadora
        Si el puntaje de la computadora es mayor a 21
            Mostrar que la computadora ha perdido
            Terminar el juego
        Si el puntaje de la computadora es igual a 21
            Mostrar que la computadora ha ganado
            Terminar el juego
    Fin del bucle
    Comparar los puntajes del jugador y la computadora
    Mostrar el resultado de la ronda
    Preguntar al jugador si quiere jugar otra ronda
Fin del juego
```

Este pseudocódigo describe el flujo general del juego de Blackjack, incluyendo la creación de la baraja de cartas, la
repartición de cartas, el cálculo de puntajes y la determinación del ganador. El juego continuará hasta que el jugador
decida no pedir más cartas o hasta que uno de los jugadores alcance un puntaje de 21 o más. Al final de cada ronda, se
mostrará el resultado y se preguntará al jugador si desea jugar otra ronda.

## 2.3.- Conclusiones

El pseudocódigo es una herramienta útil para planificar y diseñar un programa antes de comenzar a escribir el código
real. En este caso, el pseudocódigo proporciona una visión general del flujo del juego de Blackjack y ayuda a
identificar los pasos necesarios para implementar el juego en C++. Al seguir este pseudocódigo, los desarrolladores
podrán crear un juego de Blackjack funcional y entretenido para los jugadores.

## 2.4.- Entregables

Como entregable de las primeras dos unidades del curso, deberás de entregar el pseudocódigo usando las estructuras de
control que hemos visto en clase. Además, deberás de entregar un archivo README.md con los miembros del equipo y una
breve descripción del proyecto.

Deberás de crear la carpeta `pseudocode` y dentro de ella el archivo `proyecto.txt` con el pseudocódigo asumiendo que
existen las siguientes funciones(subprocesos) que deberán de ser implementadas posteriormente en C++:

- `draw_card()`: Función que devuelve una carta aleatoria de la baraja. Con un valor entre 2 y 11.

Con esta función en mente plantea el pseudocódigo del proyecto siguiendo las siguientes reglas:

1. Se deberá mostrar un mensaje al inicio del juego.
2. Se deberá de repartir dos cartas al jugador y dos a la computadora.
3. Se deberá de mostrar cuáles son las cartas del jugador y su puntaje.
4. Se deberá mantener un ciclo en el que el jugador pueda pedir cartas adicionales siempre que su puntaje sea
   menor a 21.
    - En cada iteración se deberá preguntar al jugador si desea pedir una carta adicional.
    - En caso de que el jugador pida una carta adicional, se deberá de mostrar cuáles son las cartas del jugador y su
      puntaje.
    - En caso de que el jugador no pida una carta adicional, se deberá de salir del ciclo.
    - En caso de que el jugador pida una carta adicional y su puntaje sea mayor a 21, se deberá de mostrar un mensaje
      indicando que el jugador ha perdido y salir del ciclo.
    - En caso de que el jugador pida una carta adicional y su puntaje sea igual a 21, se deberá de mostrar un mensaje
      indicando que el jugador ha ganado y salir del ciclo.
    - En caso de que el jugador pida una carta adicional y su puntaje sea menor a 21, se deberá de continuar con el
      ciclo.
5. Se deberá de mostrar cuáles son las cartas de la computadora y su puntaje únicamente si el jugador no ha perdido.
6. Se deberá comparar los puntajes del jugador y la computadora.
7. Se deberá mostrar el resultado de la ronda.
    - En caso de que el jugador haya ganado, se deberá mostrar un mensaje indicando que el jugador ha ganado.
    - En caso de que la computadora haya ganado, se deberá mostrar un mensaje indicando que la computadora ha ganado.
    - En caso de que haya un empate, se deberá mostrar un mensaje indicando que ha habido un empate.
8. Finalizar el juego.

El archivo README.md deberá de contener la siguiente información:

- Nombre del equipo.
- Integrantes del equipo.
- Descripción del proyecto.