# De pseudocódigo a C++

Para convertir un algoritmo en pseudocódigo a C++, se deben seguir los siguientes pasos:

1. Incluir la biblioteca `<iostream>` al inicio del programa.
2. Declarar las variables necesarias para el algoritmo.
3. Utilizar `std::cin` para leer datos del usuario.
4. Utilizar `std::cout` para mostrar datos en la consola.
5. Utilizar `std::endl` para imprimir saltos de línea en la consola.
6. Compilar y ejecutar el programa.
7. Verificar que el programa funcione correctamente.
8. Realizar pruebas adicionales si es necesario.
9. Corregir errores y optimizar el código si es necesario.
10. Documentar el código y agregar comentarios si es necesario.

Con estos pasos, se puede convertir un algoritmo en pseudocódigo a un programa funcional en C++ que pueda ser compilado
y ejecutado en un sistema informático.

## Ejemplo de conversión

A continuación se muestra un ejemplo de un algoritmo en pseudocódigo para calcular la suma de dos números enteros
convertido a un programa en C++:

<tabs>
<tab title="sumaValores.txt (Pseudocódigo)">

```text
Nombre del algoritmo: SumaValores
Definición de Variables:
    Entero: digito1, digito2, suma
Algoritmo:
    1.- Inicio
    2.- Leer digito1
    3.- Leer digito2
    4.- Hacer suma = digito1 + digito2
    5.- Escribir "La suma de los números es: ", suma
    6.- Fin
```

</tab>
<tab title="sumaValores.cpp (C++)">

```c++
#include <iostream>

int main() {
    // Declaración de variables
    int digito1, digito2, suma;
    // Impresión de mensajes y lectura de datos del primer número
    std::cout << "Ingrese el primer número: ";
    std::cin >> digito1;
    // Impresión de mensajes y lectura de datos del segundo número
    std::cout << "Ingrese el segundo número: ";
    std::cin >> digito2;
    // Cálculo de la suma de los números
    suma = digito1 + digito2;
    // Impresión del resultado
    std::cout << "La suma de los números es: " << suma << std::endl;
    // Fin del programa
    return 0;
}
```

</tab>
</tabs>