# Ejemplo de uso de Punteros en C++

## Ejemplo 1

Veamos el siguiente ejemplo que encuentra el valor máximo, mínimo y suma de un arreglo de enteros utilizando punteros:

```c++
#include <iostream>

using namespace std;

// Declaramos el arreglo de enteros
int arr[] = {17, 3, 25, 2, 48};
// Declaramos un puntero a entero
int *ptr = nullptr;
// Declaramos las variables que almacenarán el valor mínimo, máximo y la suma
int min_n = 0;
int max_n = 0;
int sum = 0;

/**
 * Función que ordena el arreglo de enteros
 */
void sort() {
    // Asignamos el puntero al arreglo
    ptr = arr;
    // Recorremos el arreglo
    for (int i = 0; i < 5; i++) {
        for (int j = i + 1; j < 5; j++) {
            // Si el valor en la posición j es menor al valor en la posición i
            if (*(ptr + j) < *(ptr + i)) {
                // Intercambiamos los valores
                int temp = *(ptr + i);
                *(ptr + i) = *(ptr + j);
                *(ptr + j) = temp;
            }
        }
    }
    // Liberamos el puntero
    ptr = nullptr;
}

/**
 * Función que obtiene el valor mínimo y máximo del arreglo ordenado
 * @param size Tamaño del arreglo
 * @param min Valor mínimo
 * @param max Valor máximo
 */
void getMinMax(int size, int &min, int &max) {

    // Ordenamos el arreglo
    sort();
    // Asignamos el valor mínimo y máximo
    min = arr[0];
    max = arr[size - 1];
    // Mostramos el valor mínimo y máximo
    cout << "Min: " << min << endl;
    cout << "Max: " << max << endl;
}

/**
 * Función que obtiene la suma de los valores del arreglo
 * @param size Tamaño del arreglo
 * @param sum Suma de los valores
 */
void getSum(int size, int &sum) {

    // Asignamos el puntero al arreglo
    ptr = arr;
    // Recorremos el arreglo
    for (int i = 0; i < size; i++) {
        // Sumamos el valor en la posición i
        sum += *(ptr + i);
    }
    // Mostramos la suma
    cout << "Sum: " << sum << endl;
    // Liberamos el puntero
    ptr = nullptr;
}

/**
 * Función que imprime el arreglo
 * @param size Tamaño del arreglo
 */
void printArray(int size) {
    // Asignamos el puntero al arreglo
    ptr = arr;
    // Recorremos el arreglo
    cout << "Array: [";
    for (int i = 0; i < size; i++) {
        // Mostramos el valor en la posición i
        cout << *(ptr + i) << " ";
    }
    cout << "]";
    // Mostramos un salto de línea
    cout << endl;
    // Liberamos el puntero
    ptr = nullptr;
}

/**
 * Función principal
 */
int main() {

    // Mostramos el arreglo
    printArray(5);
    // Ordenamos el arreglo
    sort();
    // Mostramos el arreglo ordenado
    printArray(5);
    // Obtenemos el valor mínimo y máximo
    getMinMax(5, min_n, max_n);
    // Obtenemos la suma de los valores
    getSum(5, sum);
    return 0;
}
```

En este ejemplo, declaramos un arreglo de enteros `arr` y un puntero a entero `ptr`. Luego, implementamos una función
`sort` que ordena el arreglo utilizando punteros. Posteriormente, definimos funciones `getMinMax` y `getSum` que
obtienen el valor mínimo, máximo y la suma de los valores del arreglo, respectivamente. Finalmente, en la función
`main`, mostramos el arreglo, lo ordenamos, obtenemos el valor mínimo y máximo, y la suma de los valores.