# Alcance de Variables en C++

En C++, el alcance de una variable se refiere a la región del código en la que la variable es visible y puede ser
utilizada. El alcance de una variable está determinado por su posición en el código y por las llaves `{}` que delimitan
bloques de código.

### Alcance de Archivo

Las variables globales tienen un alcance de archivo, lo que significa que pueden ser utilizadas en cualquier parte del
archivo en el que han sido declaradas.

Ejemplo de variable de alcance de archivo:

```c++
#include <iostream>

int global = 10; // Variable global

int main() {
    std::cout << global << std::endl; // Se puede acceder a la variable global
    return 0;
}
```

### Alcance de Bloque

Las variables locales tienen un alcance de bloque, lo que significa que solo pueden ser utilizadas dentro del bloque de
código en el que han sido declaradas. Un bloque de código está delimitado por llaves `{}` y puede contener variables
locales que solo son visibles dentro de ese bloque. En otras palabras, las variables locales solo existen mientras el
programa está dentro del bloque en el que han sido declaradas.

### Alcance de Parámetros

Los parámetros de una función tienen un alcance de bloque, lo que significa que solo pueden ser utilizados dentro del
cuerpo de la función en la que han sido declarados. Los parámetros de una función son variables locales que se utilizan
para pasar valores a la función desde el código que la llama.

Ejemplo de parámetros de función:

```c++
#include <iostream>

void imprimirNumero(int numero) {
    std::cout << numero << std::endl; // Se puede acceder al parámetro de la función
}

int main() {
    imprimirNumero(5); // Se pasa el valor 5 como argumento al parámetro de la función
    return 0;
}
```

En resumen, el alcance de una variable en C++ está determinado por su posición en el código y por las llaves `{}` que
delimitan bloques de código. Las variables globales tienen un alcance de archivo y pueden ser utilizadas en cualquier
parte del archivo en el que han sido declaradas, mientras que las variables locales tienen un alcance de bloque y solo
pueden ser utilizadas dentro del bloque de código en el que han sido declaradas.