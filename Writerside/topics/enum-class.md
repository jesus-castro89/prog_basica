# La estructura de un Enum Class

Un Enum Class es una clase que contiene un conjunto de constantes. En C++ se puede definir un Enum Class de la siguiente
manera:

```c++
enum class Color {
    Red,
    Green,
    Blue
};
```

En este caso, `Color` es el nombre del Enum Class y `Red`, `Green` y `Blue` son las constantes que contiene. Para
acceder a las constantes de un Enum Class se utiliza el operador de resolución de ámbito `::`:

```c++
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

## Uso de Enum Classes

Los Enum Classes son útiles para representar un conjunto de valores que no cambian a lo largo de la ejecución de un
programa. Por ejemplo, se pueden utilizar para representar los días de la semana:

```c++
enum class Day {
    Monday,
    Tuesday,
    Wednesday,
    Thursday,
    Friday,
    Saturday,
    Sunday
};

Day day = Day::Monday;
```

En este caso, `day` es una variable de tipo `Day` que contiene la constante `Monday`.

Los Enum Classes también se pueden utilizar en instrucciones `switch`:

```c++
switch (day) {
    case Day::Monday:
        std::cout << "Today is Monday" << std::endl;
        break;
    case Day::Tuesday:
        std::cout << "Today is Tuesday" << std::endl;
        break;
    // ...
}
```

En este caso, se imprime un mensaje dependiendo del valor de la variable `day`.

## Conclusión

Los Enum Classes son una forma de definir un conjunto de constantes en C++. Son útiles para representar valores que no
cambian a lo largo de la ejecución de un programa y se pueden utilizar en instrucciones `switch` para tomar decisiones
basadas en el valor de una variable.