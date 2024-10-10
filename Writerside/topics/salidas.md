# Salida de Datos

En C++, la salida de datos se realiza principalmente utilizando el objeto `cout`, que pertenece a la librería estándar
de entrada/salida `iostream`. En este apartado veremos algunos ejemplos para que lo puedas aplicar en tus clases de
Fundamentos de Programación.

## Imprimir un mensaje

Para imprimir un mensaje en la consola, simplemente se utiliza el operador `<<` para concatenar el mensaje con el objeto
`cout`. Por ejemplo, para imprimir el mensaje "Hola, mundo!" se utiliza el siguiente código:

```c++
#include <iostream>

using namespace std;

int main() {
    cout << "Hola, mundo!" << endl;
    return 0;
}
```

En este caso, el mensaje "Hola, mundo!", se imprime en la consola y se agrega un salto de línea al final del mensaje.

## Imprimir una variable

Para imprimir una variable, simplemente se utiliza el operador `<<` para concatenar la variable con el objeto `cout`.

```c++
#include <iostream>

using namespace std;

int main() {
    int numero = 10;
    cout << "El número es: " << numero << endl;
    return 0;
}
```

En este caso, la variable `numero` se imprime en la consola y se agrega un salto de línea al final del mensaje.

## Imprimir una expresión

También es posible imprimir una expresión utilizando el objeto `cout`. Por ejemplo, para imprimir el resultado de una
suma se utiliza el siguiente código:

```c++
#include <iostream>

using namespace std;

int main() {
    int numero1 = 10;
    int numero2 = 20;
    cout << "La suma es: " << numero1 + numero2 << endl;
    return 0;
}
```

En este caso, la expresión `numero1 + numero2` se imprime en la consola y se agrega un salto de línea al final del
mensaje.

## Imprimir varios valores

También es posible imprimir varios valores utilizando el objeto `cout`. Por ejemplo, para imprimir el mensaje "El
número es: 10" se utiliza el siguiente código:

```c++
#include <iostream>

using namespace std;

int main() {
    int numero = 10;
    cout << "El número es: " << numero << endl;
    return 0;
}
```

En este caso, el mensaje "El número es: ", se imprime en la consola, seguido del valor de la variable `numero` y se
agrega un salto de línea al final del mensaje.

## Imprimir en formato

También es posible imprimir en un formato específico utilizando el objeto `cout`. Por ejemplo, para imprimir un número
en formato decimal se utiliza el siguiente código:

```c++
#include <iostream>

using namespace std;

int main() {
    double numero = 10.5;
    cout << "El número es: " << fixed << numero << endl;
    return 0;
}
```

### Manipuladores básicos sin argumentos

Estos manipuladores no requieren parámetros y afectan el formato de salida de forma inmediata.

- `std::endl`: Inserta un salto de línea (\n) y vacía el búfer del flujo (lo que puede ser útil para asegurarse de que
  la salida se muestre en pantalla inmediatamente).
- `std::flush`: Vacía el búfer del flujo, pero no inserta un salto de línea.
- `std::ends`: Inserta un carácter nulo al final de la cadena de salida.
- `std::unitbuf`: Habilita el búfer de salida unitario para el flujo asociado.
- `std::nounitbuf`: Deshabilita el búfer de salida unitario para el flujo asociado.
- `std::boolalpha`: Imprime valores booleanos como `true` o `false`.
- `std::noboolalpha`: Imprime valores booleanos como `1` o `0`.
- `std::showbase`: Imprime los prefijos de base (0x para hexadecimal, 0 para octal).
- `std::noshowbase`: No imprime los prefijos de base.
- `std::showpoint`: Siempre imprime el punto decimal en los números de punto flotante.
- `std::noshowpoint`: No imprime el punto decimal en los números de punto flotante.
- `std::showpos`: Imprime el signo `+` para valores positivos.
- `std::noshowpos`: No imprime el signo `+` para valores positivos.
- `std::skipws`: Omite los espacios en blanco iniciales en la entrada.
- `std::noskipws`: No omite los espacios en blanco iniciales en la entrada.
- `std::uppercase`: Imprime letras en mayúsculas.
- `std::nouppercase`: Imprime letras en minúsculas.
- `std::left`: Justifica a la izquierda.
- `std::right`: Justifica a la derecha.
- `std::internal`: Justifica a la izquierda, pero los rellenos se colocan después del signo o prefijo.
- `std::dec`: Establece la base de los números enteros en 10.
- `std::hex`: Establece la base de los números enteros en 16.
- `std::oct`: Establece la base de los números enteros en 8.
- `std::fixed`: Imprime números de punto flotante en notación decimal.
- `std::scientific`: Imprime números de punto flotante en notación científica.

## Cadenas con formato

Para imprimir cadenas con formato, se utiliza el objeto `cout` y la función `printf` de la librería `cstdio`. Por
ejemplo, para imprimir un número en formato decimal se utiliza el siguiente código:

```c++
#include <iostream>
#include <cstdio>

using namespace std;

int main() {
    double numero = 10.5;
    printf("El número es: %.2f\n", numero);
    return 0;
}
```

En este caso, el número `10.5` se imprime en la consola con dos decimales y se agrega un salto de línea al final del
mensaje.

### Comodines de formato

Los comodines de formato son secuencias de caracteres que se utilizan en las cadenas de formato para especificar cómo se
debe imprimir un valor. Algunos de los comodines de formato más comunes son:

- `%d`: Imprime un número entero en formato decimal.
- `%f`: Imprime un número de punto flotante en formato decimal.
- `%s`: Imprime una cadena de caracteres.
- `%c`: Imprime un carácter.
- `%x`: Imprime un número entero en formato hexadecimal.
- `%o`: Imprime un número entero en formato octal.
- `%p`: Imprime un puntero.
- `%e`: Imprime un número de punto flotante en formato científico.
- `%g`: Imprime un número de punto flotante en formato decimal o científico, dependiendo del valor.
- `%u`: Imprime un número entero sin signo en formato decimal.

## Conclusiones

En este apartado hemos visto cómo imprimir mensajes, variables, expresiones y cadenas con formato en C++. Estos
conceptos son fundamentales para poder visualizar la salida de un programa y depurar posibles errores. Esperamos que
esta información te sea de utilidad en tus clases de Fundamentos de Programación.