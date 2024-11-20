# Uso de `unique_ptr` y `make_unique` en C++

En C++, los punteros inteligentes (`smart pointers`) son una forma segura y conveniente de gestionar la memoria
dinámica. Uno de los punteros inteligentes más utilizados es `std::unique_ptr`, que garantiza que solo un puntero apunte
a un objeto en un momento dado. En este artículo, exploraremos cómo usar `std::unique_ptr` y `std::make_unique` para
gestionar la memoria de manera segura y eficiente.

## ¿Qué es `std::unique_ptr`?

`std::unique_ptr` es un puntero inteligente que garantiza que solo un puntero apunte a un objeto en un momento dado.
Esto significa que no se pueden copiar o asignar `std::unique_ptr`, lo que evita problemas comunes como la doble
liberación de memoria. Cuando un `std::unique_ptr` se destruye, libera automáticamente la memoria del objeto al que
apunta.

## Crear un `std::unique_ptr`

Para crear un `std::unique_ptr`, puedes utilizar la función `std::make_unique` de la siguiente manera:

```c++
#include <memory>

int main() {
    std::unique_ptr<int> ptr = std::make_unique<int>(42);
    return 0;
}
```

En este ejemplo, creamos un `std::unique_ptr` que apunta a un entero con el valor `42`. Cuando el puntero `ptr` sale
de alcance, el entero se libera automáticamente.

## Acceder al objeto apuntado por un `std::unique_ptr`

Para acceder al objeto apuntado por un `std::unique_ptr`, puedes utilizar el operador de indirección `*` o el operador
de acceso a miembros `->`. Por ejemplo:

```c++
std::unique_ptr<int> ptr = std::make_unique<int>(42);

int value = *ptr;

std::cout << "Value: " << value << std::endl;
```

En este caso, accedemos al valor del entero apuntado por `ptr` utilizando el operador de indirección `*`.

## Liberar explícitamente un `std::unique_ptr`

Si necesitas liberar explícitamente la memoria de un `std::unique_ptr`, puedes hacerlo llamando al método `reset`. Por
ejemplo:

```c++
std::unique_ptr<int> ptr = std::make_unique<int>(42);

ptr.reset();
```

Al llamar a `reset`, el `std::unique_ptr` libera la memoria del objeto al que apunta y se convierte en un puntero
nulo.

## Conclusión

En resumen, `std::unique_ptr` es una forma segura y eficiente de gestionar la memoria dinámica en C++. Al utilizar
`std::unique_ptr` y `std::make_unique`, puedes evitar problemas comunes asociados con la gestión manual de la memoria,
como fugas de memoria y corrupción de memoria. Siempre que sea posible, se recomienda utilizar punteros inteligentes
como `std::unique_ptr` para garantizar una gestión segura de la memoria en tus programas C++.