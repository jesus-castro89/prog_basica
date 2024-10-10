# Las librerías `random` y `string` de C++

En C++, las librerías `random` y `string` son muy útiles para trabajar con números aleatorios y cadenas de texto,
respectivamente. En este apartado, veremos cómo utilizar estas librerías en tus programas de C++.

## Librería `random`

La librería `random` proporciona funciones y clases para generar números aleatorios en C++. Algunas de las clases más
comunes de esta librería son:

- `std::random_device`: Clase que proporciona un generador de números aleatorios basado en hardware.
- `std::mt19937`: Clase que implementa un generador de números aleatorios basado en el algoritmo Mersenne Twister.
- `std::uniform_int_distribution`: Clase que distribuye números enteros de forma uniforme en un rango dado.
- `std::uniform_real_distribution`: Clase que distribuye números reales de forma uniforme en un rango dado.
- `std::bernoulli_distribution`: Clase que distribuye valores booleanos con una probabilidad dada.
- `std::normal_distribution`: Clase que distribuye números reales con una distribución normal.
- `std::poisson_distribution`: Clase que distribuye números enteros con una distribución de Poisson.
- `std::discrete_distribution`: Clase que distribuye valores discretos con una probabilidad dada.
- `std::piecewise_constant_distribution`: Clase que distribuye valores en intervalos con una probabilidad dada.

A continuación, se muestra un ejemplo de cómo generar números aleatorios utilizando la clase `std::mt19937` y
`std::uniform_int_distribution`:

```c++
#include <iostream>
#include random

int main() {
    std::random_device rd;
    std::mt19937 gen(rd());
    std::uniform_int_distribution<int> dist(1, 6);

    for (int i = 0; i < 10; ++i) {
        std::cout << dist(gen) << ' ';
    }

    std::cout << std::endl;
    return 0;
}
```

En este ejemplo, se crea un generador de números aleatorios `gen` basado en el algoritmo Mersenne Twister con una
semilla proporcionada por `std::random_device`. Luego, se crea una distribución uniforme de enteros en el rango
`[1, 6]` con la clase `std::uniform_int_distribution`. Finalmente, se generan 10 números aleatorios en ese rango y se
imprimen en la consola.

## Librería `string`

La librería `string` proporciona funciones y clases para trabajar con cadenas de texto en C++. Algunas de las clases
más comunes de esta librería son:

- `std::string`: Clase que representa una cadena de texto en C++.
- `std::wstring`: Clase que representa una cadena de texto amplia en C++.
- `std::basic_string`: Clase base para las clases `std::string` y `std::wstring`.
- `std::stringstream`: Clase que permite la conversión entre cadenas de texto y otros tipos de datos.
- `std::string_view`: Clase que proporciona una vista no propietaria de una cadena de texto.
- `std::to_string`: Función que convierte un valor numérico en una cadena de texto.
- `std::stoi`: Función que convierte una cadena de texto en un valor entero.
- `std::stof`: Función que convierte una cadena de texto en un valor de punto flotante.
- `std::stod`: Función que convierte una cadena de texto en un valor de doble precisión.
- `std::getline`: Función que lee una línea de texto de un flujo de entrada.
- `std::find`: Función que busca una subcadena en una cadena de texto.
- `std::replace`: Función que reemplaza todas las ocurrencias de una subcadena en una cadena de texto.
- `std::toupper`: Función que convierte una cadena de texto a mayúsculas.
- `std::tolower`: Función que convierte una cadena de texto a minúsculas.
- `std::strlen`: Función que devuelve la longitud de una cadena de texto.

A continuación, se muestra un ejemplo de cómo trabajar con cadenas de texto en C++ utilizando la clase `std::string`:

```c++
#include <iostream>
#include string

int main() {
    std::string nombre = "Juan";
    std::string apellido = "Perez";
    std::string nombre_completo = nombre + " " + apellido;

    std::cout << "Nombre completo: " << nombre_completo << std::endl;
    std::cout << "Longitud del nombre: " << nombre.length() << std::endl;

    return 0;
}
```

En este ejemplo, se crean dos cadenas de texto `nombre` y `apellido`, se concatenan para formar `nombre_completo` y
se imprime en la consola. Además, se muestra la longitud de la cadena `nombre`.

Estas son solo algunas de las funcionalidades que ofrecen las librerías `random` y `string` de C++. Puedes
explorar más sobre estas librerías en la documentación oficial de C++ para sacar el máximo provecho de ellas en tus
programas.

### Leer cadenas de texto con espacios

Para leer una cadena de texto con espacios en C++, puedes utilizar la función `std::getline` de la librería `string`.

```c++
#include <iostream>
#include string

int main() {
    std::string nombre;

    std::cout << "Ingrese su nombre completo: ";
    std::getline(std::cin, nombre);

    std::cout << "Su nombre es: " << nombre << std::endl;

    return 0;
}
```

## Referencias

- [Documentación de C++ para `random`](https://en.cppreference.com/w/cpp/header/random)
- [Documentación de C++ para `string`](https://en.cppreference.com/w/cpp/header/string)
- [C++ Random Number Generation](https://www.learncpp.com/cpp-tutorial/15-1-introduction-to-random-number-generation/)
- [C++ Strings](https://www.learncpp.com/cpp-tutorial/66-c-strings-an-introduction/)