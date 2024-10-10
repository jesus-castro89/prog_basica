# La documentación de código

La documentación de código es una parte importante del desarrollo de software, ya que permite a los desarrolladores y a
los usuarios comprender cómo funciona el código y cómo utilizarlo de manera efectiva. En este tutorial, aprenderás cómo
documentar tu código en C++ utilizando comentarios y herramientas de generación de documentación.

## 1. Comentarios en C++

Los comentarios son una forma de documentar el código en C++ y proporcionar información adicional sobre su
funcionamiento. Hay dos tipos de comentarios en C++: de una sola línea y de varias líneas.

### 1.1. Comentarios de una sola línea

Los comentarios de una sola línea comienzan con `//` y se extienden hasta el final de la línea. Por ejemplo:

```c++
// Este es un comentario de una sola línea
int x = 5; // Esto es un comentario en la misma línea que el código
```

### 1.2. Comentarios de varias líneas

Los comentarios de varias líneas comienzan con `/*` y terminan con `*/`. Pueden abarcar varias líneas de código. Por
ejemplo:

```c++
/*
Este es un comentario de varias líneas
que abarca varias líneas de código
*/
int y = 10; /* Esto es un comentario en la misma línea que el código */
```

## 2. Documentación de funciones

La documentación de funciones es una parte importante de la documentación de código, ya que permite a los desarrolladores
y a los usuarios comprender cómo funciona una función y cómo utilizarla de manera efectiva. Para documentar una función
en C++, puedes seguir el siguiente formato:

```c++
/**
 * Breve descripción de la función.
 * 
 * Descripción más detallada de la función, incluyendo los parámetros de entrada y salida.
 * 
 * @param param1 Descripción del primer parámetro.
 * @param param2 Descripción del segundo parámetro.
 * @return Descripción del valor de retorno.
 */
int myFunction(int param1, int param2) {
    // Código de la función
}
```