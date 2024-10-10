# Los operadores

Los operadores son símbolos que se utilizan para realizar operaciones en un programa. En C++, los operadores se dividen
en varias categorías:

- **Operadores aritméticos**: se utilizan para realizar operaciones matemáticas, como la suma(+), resta(-),
  multiplicación(*), división(/) y módulo(%).
- **Operadores de asignación**: se utilizan para asignar un valor a una variable, como el operador de asignación
  simple(=) o los operadores compuestos(+=, -=, *=, /=, %=).
- **Operadores de comparación**: se utilizan para comparar dos valores, como los operadores de igualdad(==),
  desigualdad(!=), mayor que(>), menor que(<), mayor o igual que(>=) y menor o igual que(<=).
- **Operadores lógicos**: se utilizan para combinar expresiones lógicas, como los operadores AND(&&), OR(||) y NOT(!).
- **Operadores de incremento y decremento**: se utilizan para incrementar(++) o decrementar(--) el valor de una
  variable.

Conocer y comprender los operadores en C++ es fundamental para poder escribir programas eficientes y funcionales. A
continuación, se presentan algunos ejemplos de cómo utilizar los operadores en C++.

## Operadores aritméticos

Los operadores aritméticos se utilizan para realizar operaciones matemáticas en C++. A continuación, se presentan
algunos ejemplos de operadores aritméticos:

```c++
#include <iostream>

using namespace std;

int main() {
    int numero1 = 10;
    int numero2 = 5;

    // Suma
    cout << "Suma: " << numero1 + numero2 << endl;

    // Resta
    cout << "Resta: " << numero1 - numero2 << endl;

    // Multiplicación
    cout << "Multiplicación: " << numero1 * numero2 << endl;

    // División
    cout << "División: " << numero1 / numero2 << endl;

    // Módulo
    cout << "Módulo: " << numero1 % numero2 << endl;

    return 0;
}
```

En este caso, se realizan operaciones de suma, resta, multiplicación, división y módulo entre dos variables `numero1`
y `numero2`. Los resultados de las operaciones se imprimen en la consola.

## Operadores de asignación

Los operadores de asignación se utilizan para asignar un valor a una variable en C++. A continuación, se presentan
algunos ejemplos de operadores de asignación:

```c++
#include <iostream>

using namespace std;

int main() {
    int numero = 10;

    // Asignación simple
    cout << "Número: " << numero << endl;

    // Operadores compuestos
    numero += 5;
    cout << "Número después de sumar 5: " << numero << endl;

    numero -= 2;
    cout << "Número después de restar 2: " << numero << endl;

    numero *= 3;
    cout << "Número después de multiplicar por 3: " << numero << endl;

    numero /= 2;
    cout << "Número después de dividir por 2: " << numero << endl;

    numero %= 4;
    cout << "Número después de aplicar módulo 4: " << numero << endl;

    return 0;
}
```

En este caso, se asigna un valor inicial a la variable `numero` y se utilizan operadores compuestos para realizar
operaciones de suma, resta, multiplicación, división y módulo con la variable `numero`. Los resultados de las
operaciones se imprimen en la consola.

## Operadores de comparación

Los operadores de comparación se utilizan para comparar dos valores en C++. A continuación, se presentan algunos
ejemplos de operadores de comparación:

```c++
#include <iostream>

using namespace std;

int main() {
    int numero1 = 10;
    int numero2 = 5;

    // Igualdad
    cout << "Igualdad: " << (numero1 == numero2) << endl;

    // Desigualdad
    cout << "Desigualdad: " << (numero1 != numero2) << endl;

    // Mayor que
    cout << "Mayor que: " << (numero1 > numero2) << endl;

    // Menor que
    cout << "Menor que: " << (numero1 < numero2) << endl;

    // Mayor o igual que
    cout << "Mayor o igual que: " << (numero1 >= numero 2) << endl;
}
```

En este caso, se comparan dos variables `numero1` y `numero2` utilizando operadores de igualdad, desigualdad, mayor que,
menor que y mayor o igual que. Los resultados de las comparaciones se imprimen en la consola.

## Operadores lógicos

Los operadores lógicos se utilizan para combinar expresiones lógicas en C++. A continuación, se presentan algunos
ejemplos de operadores lógicos:

```c++
#include <iostream>

using namespace std;

int main() {
    int numero1 = 10;
    int numero2 = 5;

    // AND
    cout << "AND: " << ((numero1 > 5) && (numero2 < 10)) << endl;

    // OR
    cout << "OR: " << ((numero1 > 5) || (numero2 > 10)) << endl;

    // NOT
    cout << "NOT: " << !(numero1 == 10) << endl;
}
```

En este caso, se combinan expresiones lógicas utilizando los operadores AND, OR y NOT. Los resultados de las
expresiones lógicas se imprimen en la consola.

## Operadores de incremento y decremento

Los operadores de incremento y decremento se utilizan para incrementar(++) o decrementar(--) el valor de una variable en
C++. A continuación, se presentan algunos ejemplos de operadores de incremento y decremento:

```c++
#include <iostream>

using namespace std;

int main() {
    int numero = 10;

    // Incremento
    cout << "Incremento: " << ++numero << endl;

    // Decremento
    cout << "Decremento: " << --numero << endl;
}
```

En este caso, se incrementa y decrementa el valor de la variable `numero` utilizando los operadores de incremento y
decremento. Los resultados de las operaciones se imprimen en la consola.

## Conclusiones

Comprender los operadores en C++ es fundamental para poder escribir programas eficientes y funcionales. Los operadores
aritméticos, de asignación, de comparación, lógicos e incremento y decremento son herramientas poderosas que permiten
realizar operaciones matemáticas, asignar valores a variables, comparar valores y combinar expresiones lógicas en un
programa. Al dominar los operadores en C++, los programadores pueden escribir código más claro, conciso y fácil de
mantener.