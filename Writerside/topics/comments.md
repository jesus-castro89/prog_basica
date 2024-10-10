# Documentación de Código

Los comentarios de documentación de código son una forma de documentar el código fuente de un programa. Estos
comentarios se utilizan para describir el propósito, el funcionamiento y la estructura del código, y su objetivo es
facilitar la comprensión y el mantenimiento del código.

En este apartado, vamos a ver cómo documentar el código fuente de un programa en C++ utilizando comentarios de
documentación de código.

## 1. Comentarios de Documentación de Código

Los comentarios de documentación de código se utilizan para describir el propósito, el funcionamiento y la estructura
del código fuente de un programa. Estos comentarios se colocan en el código fuente junto a las declaraciones de las
funciones, las variables y las constantes, y se utilizan para proporcionar información adicional sobre el código.

Los comentarios de documentación de código suelen seguir un formato estándar que incluye la descripción de la función o
variable, los parámetros que recibe, el valor que devuelve y ejemplos de uso. Este formato estándar facilita la lectura
y comprensión del código, y permite a otros programadores entender rápidamente cómo funciona el código.

A continuación, se muestra un ejemplo de un comentario de documentación de código en C++:

```c++
/**
 * @brief Esta función suma dos números enteros.
 * 
 * @param a El primer número entero.
 * @param b El segundo número entero.
 * @return La suma de los dos números enteros.
 * 
 * @code
 * int resultado = sumar(5, 3);
 * @endcode
 */
int sumar(int a, int b) {
    return a + b;
}
```

En este ejemplo, el comentario de documentación de código describe la función `sumar()`, indicando que suma dos números
enteros y devuelve el resultado. Además, se incluyen los parámetros que recibe la función (`a` y `b`), el valor que
devuelve (la suma de los dos números enteros) y un ejemplo de uso de la función.

Dónde:

* `@brief`: Es una etiqueta que se utiliza para indicar una breve descripción de la función.
* `@param`: Es una etiqueta que se utiliza para indicar los parámetros que recibe la función.
* `@return`: Es una etiqueta que se utiliza para indicar el valor que devuelve la función.
* `@code`: Es una etiqueta que se utiliza para indicar un ejemplo de uso de la función.
* `@endcode`: Es una etiqueta que se utiliza para indicar el final del ejemplo de uso de la función.

## 2. Ejemplo de Documentación de Código

A continuación, se muestra un ejemplo de documentación de código en C++ para una función que suma dos números enteros:

```c++
/**
 * @brief Esta función suma dos números enteros.
 * 
 * @param a El primer número entero.
 * @param b El segundo número entero.
 *
 * @code
 * int resultado = sumar(5, 3);
 * @endcode
 *
 * @return La suma de los dos números enteros.
 */
int sumar(int a, int b) {
    return a + b;
}   
```

## Para el Proyecto

Para documentar el código fuente de tu proyecto en C++, te recomiendo seguir las siguientes pautas:

1. Utiliza comentarios de documentación de código para describir las funciones, las variables y las constantes del
   programa.
2. Incluye una breve descripción de la función, indicando su propósito y su funcionamiento.
3. Indica los parámetros que recibe la función, el valor que devuelve y ejemplos de uso.
4. Utiliza etiquetas como `@brief`, `@param`, `@return`, `@code` y `@endcode` para estructurar el comentario de
   documentación de código.
5. Mantén los comentarios de documentación de código actualizados y coherentes con el código fuente del programa.

Al documentar el código fuente de tu proyecto en C++ con comentarios de documentación de código, facilitarás la
comprensión y el mantenimiento del código, y permitirás a otros programadores entender rápidamente cómo funciona tu
programa.