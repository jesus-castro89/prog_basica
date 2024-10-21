# La librería vector en C++

La librería `vector` en C++ es una de las estructuras de datos más utilizadas en la programación. Un `vector` es un
contenedor que almacena un conjunto de elementos de un mismo tipo en una secuencia contigua de memoria. A diferencia de
los arreglos tradicionales, los `vector` en C++ son dinámicos, es decir, su tamaño puede cambiar durante la ejecución
del programa.

## Creando un Vector

Para crear un `vector` en C++, se utiliza la plantilla `std::vector` de la siguiente manera:

```c++
#include <vector>

std::vector<int> numbers;
```

En este caso, se crea un `vector` de enteros llamado `numbers`. Para agregar elementos al `vector`, se utiliza el método
`push_back()` de la siguiente manera:

```c++
numbers.push_back(10);
numbers.push_back(20);
numbers.push_back(30);
```

En este caso, se agregan los números 10, 20 y 30 al `vector` `numbers`.

> Vector incluye la función `emplace_back` que permite agregar elementos al final del vector sin necesidad de copiar el
> elemento. Esto es útil cuando se trabaja con tipos de datos complejos.

```c++
numbers.emplace_back(10);
numbers.emplace_back(20);
numbers.emplace_back(30);
```

## Accediendo a los Elementos de un Vector

Para acceder a los elementos de un `vector`, se utiliza el operador de acceso `[]` de la siguiente manera:

```c++
std::cout << numbers[0] << std::endl; // Imprime 10
std::cout << numbers[1] << std::endl; // Imprime 20
std::cout << numbers[2] << std::endl; // Imprime 30
```

En este caso, se accede a los elementos del `vector` `numbers` utilizando el operador de acceso `[]`.

## Recorriendo un Vector

Para recorrer un `vector`, se puede utilizar un bucle `for` de la siguiente manera:

```c++
for (int i = 0; i < numbers.size(); i++) {
    std::cout << numbers[i] << std::endl;
}
```

En este caso, se recorre el `vector` `numbers` utilizando un bucle `for` y se imprime cada uno de los elementos del
`vector`.

## Eliminando Elementos de un Vector

Para eliminar elementos de un `vector`, se utiliza el método `erase()` de la siguiente manera:

```c++
numbers.erase(numbers.begin() + 1);
```

Dónde:

* `numbers.begin()`: Es un iterador que apunta al primer elemento del `vector`.
* `+ 1`: Se suma 1 al iterador para apuntar al segundo elemento del `vector`.

> Recuerda que los índices en C++ empiezan en 0. Por lo tanto, el primer elemento de un `vector` tiene el índice 0.
> Así mismo, no podrás eliminar un elemento que no exista en el `vector`.

En este caso, se elimina el segundo elemento del `vector` `numbers`. Aunque el método `erase()` es útil para eliminar
elementos de un `vector`, también se puede utilizar el método `pop_back()` para eliminar el último elemento del
`vector`.

```c++
numbers.pop_back();
```

## Tamaño de un Vector

Para obtener el tamaño de un `vector`, se utiliza el método `size()` de la siguiente manera:

```c++
std::cout << numbers.size() << std::endl; // Imprime 2
```

En este caso, se obtiene el tamaño del `vector` `numbers`, que en este caso es 2.
