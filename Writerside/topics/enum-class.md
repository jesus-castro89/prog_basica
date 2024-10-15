# La estructura de un Enum Class

Un Enum Class es una clase que contiene un conjunto de constantes. En C++ se puede definir un Enum Class de la siguiente
manera:

```cpp
enum class Color {
    Red,
    Green,
    Blue
};
```

En este caso, `Color` es el nombre del Enum Class y `Red`, `Green` y `Blue` son las constantes que contiene. Para
acceder a las constantes de un Enum Class se utiliza el operador de resolución de ámbito `::`:

```cpp
Color color = Color::Red;
```

En este caso, `color` es una variable de tipo `Color` que contiene la constante `Red`.

## Asignación de valores a las constantes

Por defecto, las constantes de un Enum Class se inicializan con valores enteros consecutivos empezando por 0. En el
ejemplo anterior, `Red` tiene el valor 0, `Green` tiene el valor 1 y `Blue` tiene el valor 2. Sin embargo, se pueden
asignar valores específicos a las constantes de un Enum Class:

```c++
enum class Color {
    Red = 1,
    Green = 2,
    Blue = 4
};
```

En este caso, `Red` tiene el valor 1, `Green` tiene el valor 2 y `Blue` tiene el valor 4.

## Atributos de un Enum Class

Un Enum Class puede tener atributos, como cualquier otra clase en C++. Por ejemplo, se pueden añadir métodos y
constructores a un Enum Class:

```c++
enum class Color {
    Red = 1,
    Green = 2,
    Blue = 4

    Color(int value) : value(value) {}
    int getValue() { return value; }

private:
    int value;
};
```