# 12. Agregando el manejo de archivos

## Manejo de archivos

Para nuestro proyecto de BlackJack en C++, necesitaremos manejar archivos para guardar y cargar partidas. Para ello,
utilizaremos la librería `fstream` de C++. Esta librería nos permite manejar archivos de texto, tanto para lectura como
para escritura.

### Archivos de texto

Un archivo de texto es un archivo que contiene texto plano, es decir, caracteres que representan letras, números y
símbolos. En C++, podemos leer y escribir archivos de texto utilizando los objetos `ifstream` y `ofstream` de la
librería `fstream`.

### Los archivos en nuestro proyecto

Para nuestro proyecto de BlackJack, necesitaremos guardar y cargar partidas. Para ello, crearemos dos archivos de texto:
uno para guardar las partidas guardadas y otro para guardar las partidas cargadas.

### Guardar una partida

Para guardar una partida, necesitaremos escribir la información de la partida en un archivo de texto. Para ello,
utilizaremos un objeto `ofstream` para escribir en el archivo.

```c++
#include <fstream>

void guardarPartida(const Partida& partida) {
    std::ofstream archivo("partidas_guardadas.txt", std::ios::app);

    if (archivo.is_open()) {
        archivo << partida << std::endl;
        archivo.close();
    } else {
        std::cerr << "Error al abrir el archivo" << std::endl;
    }
}
```

En este ejemplo, la función `guardarPartida` recibe una referencia a un objeto `Partida` y lo escribe en el archivo
`partidas_guardadas.txt`. Para ello, se utiliza un objeto `ofstream` llamado `archivo` que se abre en modo `app` (
append), lo que permite agregar información al final del archivo.

### Cargar una partida

Para cargar una partida, necesitaremos leer la información de una partida desde un archivo de texto. Para ello,
utilizaremos un objeto `ifstream` para leer del archivo.

```c++
#include <fstream>

Partida cargarPartida() {
    std::ifstream archivo("partidas_guardadas.txt");

    if (archivo.is_open()) {
        Partida partida;
        archivo >> partida;
        archivo.close();
        return partida;
    } else {
        std::cerr << "Error al abrir el archivo" << std::endl;
        return Partida();
    }
}
```

En este ejemplo, la función `cargarPartida` lee una partida del archivo `partidas_guardadas.txt` y la devuelve como
un objeto `Partida`. Para ello, se utiliza un objeto `ifstream` llamado `archivo` que se abre en modo `in` (input),

### La estructura `Partida`

Para poder guardar y cargar partidas, necesitaremos definir una estructura `Partida` que contenga la información
necesaria para representar una partida de BlackJack. Esta estructura puede contener los siguientes campos:

```c++
struct Partida {
    std::string jugador;
    int puntaje;
    std::string mano;
    bool gano;
};
```

En este ejemplo, la estructura `Partida` contiene tres campos: `jugador`, `puntaje` y `gano`. Estos campos representan
el nombre del jugador, el puntaje obtenido en la partida y si el jugador ganó o perdió la partida.

### Guardar y cargar partidas

Con estas funciones y estructuras, podemos guardar y cargar partidas en nuestro proyecto de BlackJack. Para ello,
necesitaremos definir las funciones `guardarPartida` y `cargarPartida` en nuestro proyecto y utilizarlas para guardar
y cargar partidas.

```c++
int main() {
    Partida partida = { "Juan", 21, true };
    guardarPartida(partida);

    Partida partida_cargada = cargarPartida();
    std::cout << "Jugador: " << partida_cargada.jugador << std::endl;
    std::cout << "Puntaje: " << partida_cargada.puntaje << std::endl;
    std::cout << "Gano: " << (partida_cargada.gano ? "Si" : "No") << std::endl;

    return 0;
}
```

En este caso al crear un nuevo juego, se deberá solicitar al usuario su nombre.
Al finalizar cada ronda de juego, se deberá preguntar al usuario si desea guardar la partida.
Al iniciar el juego, se deberá preguntar al usuario si desea cargar una partida guardada.

Con esto, ya tenemos una forma de guardar y cargar partidas en nuestro proyecto de BlackJack en C++.