# Manejo de archivos de texto

## Introducción

En C++ se pueden manejar archivos de texto de dos maneras: secuencial y aleatoria. En este documento se explicará cómo
hacerlo de manera secuencial.

## Apertura de un archivo

Para abrir un archivo se utiliza la clase `fstream` que se encuentra en la librería `fstream`. Para abrir un archivo se
utiliza el método `open` de la clase `fstream`. El método `open` recibe como parámetro el nombre del archivo y el modo
en el que se desea abrir el archivo. Los modos de apertura son:

* `ios::in`: Abre el archivo en modo lectura.
* `ios::out`: Abre el archivo en modo escritura.
* `ios::app`: Abre el archivo en modo escritura, pero no borra el contenido del archivo.

```c++
#include <fstream>

int main() {
    std::fstream archivo;
    archivo.open("archivo.txt", std::ios::out);
    archivo.close();
    return 0;
}
```

## Escritura en un archivo

Para escribir en un archivo se utiliza el operador `<<` de la misma manera que se hace con `std::cout`.

```c++
#include <fstream>

int main() {
    std::fstream archivo;
    archivo.open("archivo.txt", std::ios::out);
    archivo << "Hola, mundo!" << std::endl;
    archivo.close();
    return 0;
}
```

> **Nota**: Si se desea escribir en un archivo que ya tiene contenido, se debe abrir el archivo en modo `ios::app`.
> De lo contrario, el contenido del archivo se sobreescribirá.

## Lectura de un archivo

Para leer un archivo se utiliza el operador `>>` de la misma manera que se hace con `std::cin`.

```c++
#include <fstream>

int main() {
    std::fstream archivo;
    archivo.open("archivo.txt", std::ios::in);
    std::string linea;
    archivo >> linea;
    std::cout << linea << std::endl;
    archivo.close();
    return 0;
}
```

> **Nota**: Si se desea leer un archivo línea por línea, se puede utilizar el método `getline` de la clase `fstream`.
> Este método recibe como parámetro un `std::string` donde se almacenará la línea leída.

Podemos usar un ciclo `while` para leer todas las líneas del archivo.

```c++
#include <fstream>

int main() {
    std::fstream archivo;
    archivo.open("archivo.txt", std::ios::in);
    std::string linea;
    while (std::getline(archivo, linea)) {
        std::cout << linea << std::endl;
    }
    archivo.close();
    return 0;
}
```

## Ejemplo completo

```c++

#include <fstream>
#include <iostream>

using namespace std;

int main() {
    fstream archivo;
    archivo.open("archivo.txt", ios::out);
    archivo << "Hola, mundo!" << endl;
    archivo.close();

    archivo.open("archivo.txt", ios::in);
    string linea;
    while (getline(archivo, linea)) {
        cout << linea << endl;
    }
    archivo.close();
    return 0;
}
```
