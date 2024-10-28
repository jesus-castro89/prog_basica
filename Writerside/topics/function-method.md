# Función y Método

## Introducción

En C++, una función es un bloque de código que realiza una tarea específica. Las funciones se definen con un tipo de
retorno, un nombre y una lista de parámetros. Por otro lado, un método es una función que está asociada a una estructura
en C++.

## Función

Una función es un bloque de código que realiza una tarea específica. En C++, las funciones se definen con un tipo de
retorno, un nombre y una lista de parámetros. Por ejemplo, la siguiente función suma dos números enteros y devuelve el
resultado:

```c++
int sum(int a, int b) {
    return a + b;
}
```

En este ejemplo, la función `sum` toma dos parámetros `a` y `b` de tipo entero y devuelve la suma de los dos números.

La estructura de una función en C++ es la siguiente:

```c++
tipo_de_retorno nombre_de_la_funcion(tipo_de_parametro1 parametro1, tipo_de_parametro2 parametro2, ...) {
    // Cuerpo de la función
    return valor_de_retorno;
}
```

Donde:

* `tipo_de_retorno`: Es el tipo de dato que devuelve la función.
* `nombre_de_la_funcion`: Es el nombre de la función.
* `tipo_de_parametro1`, `tipo_de_parametro2`, ...: Son los tipos de datos de los parámetros de la función.
* `parametro1`, `parametro2`, ...: Son los nombres de los parámetros de la función.
* `valor_de_retorno`: Es el valor que devuelve la función.

## Método

Un método es una función que está asociada a una estructura en C++. Los métodos se definen dentro de una estructura y
pueden acceder a los campos de la estructura. Por ejemplo, la siguiente estructura `Persona` tiene un método `saludar`
que muestra un saludo con el nombre de la persona:

```c++
struct Persona {
    std::string nombre;

    void saludar() {
        std::cout << "Hola, soy " << nombre << std::endl;
    }
};
```

En este ejemplo, el método `saludar` accede al campo `nombre` de la estructura `Persona` para mostrar un saludo con el
nombre de la persona.

La estructura de un método en C++ es la siguiente:

```c++
struct Nombre_de_la_estructura {
    tipo_de_dato campo1;
    tipo_de_dato campo2;
    ...

    tipo_de_retorno nombre_del_metodo(tipo_de_parametro1 parametro1, tipo_de_parametro2 parametro2, ...) {
        // Cuerpo del método
        return valor_de_retorno;
    }
};
```

Donde:

* `Nombre_de_la_estructura`: Es el nombre de la estructura.
* `tipo_de_dato campo1`, `tipo_de_dato campo2`, ...: Son los campos de la estructura.
* `tipo_de_retorno`: Es el tipo de dato que devuelve el método.
* `nombre_del_metodo`: Es el nombre del método.
* `tipo_de_parametro1`, `tipo_de_parametro2`, ...: Son los tipos de datos de los parámetros del método.
* `parametro1`, `parametro2`, ...: Son los nombres de los parámetros del método.
* `valor_de_retorno`: Es el valor que devuelve el método.

## Conclusión

En resumen, una función es un bloque de código que realiza una tarea específica en C++, mientras que un método es una
función asociada a una estructura en C++. Ambos son fundamentales para la programación en C++ y permiten organizar y
reutilizar el código de manera eficiente.