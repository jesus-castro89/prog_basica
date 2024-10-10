# Los tipos enumerados

En C++, un tipo enumerado (o enumeración) es un tipo de dato que permite definir un conjunto de constantes enteras con
nombres simbólicos. Los tipos enumerados son útiles para representar un conjunto finito de valores que tienen un
significado específico en un programa.

## 1. Definición de un Tipo Enumerado

Para definir un tipo enumerado en C++, se utiliza la palabra clave `enum` seguida de un nombre para el tipo enumerado y
una lista de constantes enteras separadas por comas. Por ejemplo, el siguiente código define un tipo enumerado llamado
`Color` con tres constantes enteras: `Rojo`, `Verde` y `Azul`:

```c++
enum Color {
    RED,
    GREEN,
    BLUE
};
```

En este código, se define un tipo enumerado `Color` con tres constantes enteras: `RED`, `GREEN` y `BLUE`. Cada constante
entera tiene un valor implícito que comienza en `0` y se incrementa en `1` para cada constante adicional. Por lo tanto,
las constantes `RED`, `GREEN` y `BLUE` tienen los valores `0`, `1` y `2`, respectivamente.

## 2. Uso de un Tipo Enumerado

Una vez que se ha definido un tipo enumerado, se puede utilizar para declarar variables, funciones y parámetros de
funciones. Por ejemplo, el siguiente código declara una variable `color` de tipo `Color` y la inicializa con la
constante
`RED`:

```c++
Color color = RED;
```

En este código, se declara una variable `color` de tipo `Color` y se inicializa con la constante `RED` del tipo
enumerado `Color`.

## 3. Asignación de Valores a las Constantes

En un tipo enumerado, se pueden asignar valores explícitos a las constantes enteras. Por ejemplo, el siguiente código
define un tipo enumerado `DiaSemana` con valores explícitos para las constantes enteras:

```c++
enum DiaSemana {
    LUNES = 1,
    MARTES = 2,
    MIERCOLES = 3,
    JUEVES = 4,
    VIERNES = 5,
    SABADO = 6,
    DOMINGO = 7
};
```

En este código, se define un tipo enumerado `DiaSemana` con valores explícitos para las constantes enteras. Por ejemplo,
`LUNES` tiene el valor `1`, `MARTES` tiene el valor `2`, y así sucesivamente.

Otra manera de asignar valores a las constantes es utilizando la asignación de valores a partir de una constante. Por
ejemplo, el siguiente código define un tipo enumerado `Meses` con valores asignados a partir de una constante:

```c++
enum Meses {
    ENERO = 1,
    FEBRERO,
    MARZO,
    ABRIL,
    MAYO,
    JUNIO,
    JULIO,
    AGOSTO,
    SEPTIEMBRE,
    OCTUBRE,
    NOVIEMBRE,
    DICIEMBRE
};
```

En este código, se define un tipo enumerado `Meses` con valores asignados a partir de la constante `ENERO`. Las
constantes `FEBRERO`, `MARZO`, `ABRIL`, etc., tienen valores consecutivos a partir de la constante `ENERO`.

## 4. Conversión de un Tipo Enumerado a Entero

En C++, un tipo enumerado se puede convertir implícitamente a un entero. Por ejemplo, el siguiente código muestra cómo
convertir un tipo enumerado `Color` a un entero:

```c++
Color color = RED;
int valor = color;
```

En este código, se declara una variable `color` de tipo `Color` y se inicializa con la constante `RED`. Luego, se
convierte la variable `color` a un entero y se almacena en la variable `valor`.
