# 4. Iniciando la codificación en C++ del proyecto

## 4.1. Introducción

Hasta ahora hemos visto los conceptos básicos de la programación y hemos aprendido a escribir programas en C++. En esta
sección, vamos a ver cómo podemos escribir programas más complejos y cómo podemos estructurar nuestro código de una
manera más eficiente.

## 4.2. Estructura de un programa en C++

Un programa en C++ se compone de una o más funciones. Cada función tiene un nombre y un cuerpo. El cuerpo de una función
es un bloque de código que se ejecuta cuando la función es llamada. El cuerpo de una función puede contener
declaraciones de variables, expresiones, sentencias de control y llamadas a otras funciones.

Un programa en C++ siempre tiene una función llamada `main`. La función `main` es la función principal del programa y
es la que se ejecuta cuando el programa es lanzado. El cuerpo de la función `main` es el punto de entrada del programa
y contiene el código que se ejecuta cuando el programa es lanzado.

```c++
#include <iostream>

int main() {
    std::cout << "Hello, world!" << std::endl;
    return 0;
}
```

En este ejemplo, el cuerpo de la función `main` imprime el mensaje "Hello, world!" en la consola y luego retorna 0. La
función `main` debe retornar un valor entero, que indica si el programa se ejecutó correctamente o no. Un valor de 0
indica que el programa se ejecutó correctamente, mientras que un valor distinto de 0 indica que hubo un error.

## 4.3. Creando los directorios del proyecto

Para organizar nuestro código de una manera más eficiente, es recomendable crear una estructura de directorios para el
proyecto. Por ejemplo, podemos crear un directorio llamado `src` para almacenar el código fuente del programa y un
directorio llamado `bin` para almacenar los archivos ejecutables.

```
project/
├── src/
│   └── main.cpp
└── bin/
```

En este ejemplo, el directorio `src` contiene un archivo llamado `main.cpp`, que es el archivo fuente del programa, y
el directorio `bin` está vacío. Cuando compilamos el programa, el archivo ejecutable se generará en el directorio
`bin`.

## 4.4. Configurando CLion para el proyecto

Antes que nada, debemos de crear dos directorios en la raíz del proyecto: `src` y `bin`. En el directorio `src` es
donde se colocarán los archivos fuente del proyecto y en el directorio `bin` es donde se colocarán los archivos
ejecutables.

Lo primero que debemos hacer crear un archivo de tipo CMakeLists.txt en la raíz del proyecto. Este archivo contiene las
instrucciones necesarias para compilar el proyecto. A continuación se muestra un ejemplo de un archivo CMakeLists.txt
para un proyecto en C++:

```cmake
# Definimos la versión mínima de CMake
cmake_minimum_required(VERSION 3.29)
# Definimos el nombre del proyecto
project(black-jack)
# Definimos la versión de C++ que vamos a utilizar
set(CMAKE_CXX_STANDARD 26)
# Definimos el nombre del ejecutable y los archivos que lo componen
add_executable(black-jack src/main.cpp)
```

En este ejemplo, el archivo CMakeLists.txt define un proyecto llamado `black-jack` que utiliza la versión 26 de C++ y
genera el archivo ejecutable en el directorio `bin`. El archivo ejecutable se llama `black-jack` y está compuesto por el
archivo `main.cpp`.

Creamos un archivo de tipo C++ en el directorio `src` con el nombre `main.cpp` y escribimos el siguiente código:

```c++
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```

Una vez que hemos creado los archivos necesarios, podemos abrir el proyecto en CLion y compilarlo. Para compilar el
proyecto, hacemos clic en el botón de "Build" en la barra de herramientas de CLion. Si todo está configurado
correctamente, el archivo ejecutable se generará en el directorio `bin` y se ejecutará.

## 4.5. Resumen

En esta sección, hemos visto cómo podemos estructurar un programa en C++ y cómo podemos organizar el código en
directorios. También hemos visto cómo configurar CLion para compilar un proyecto en C++ y cómo compilarlo. En la
siguiente sección, veremos cómo podemos escribir programas más complejos y cómo podemos utilizar bibliotecas externas
en nuestros programas.