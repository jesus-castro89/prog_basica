# Constantes en C++

En C++, una constante es un valor que no puede ser modificado una vez que ha sido asignado. Las constantes se utilizan
para almacenar valores que no cambian durante la ejecución de un programa y se definen utilizando la palabra
clave `const`.

## Declaración de constantes

Para declarar una constante en C++, se utiliza la siguiente sintaxis:

```c++
const tipo nombre = valor;
```

Donde:

- `const` es la palabra clave que indica que la variable es una constante.
- `tipo` es el tipo de dato de la constante.
- `nombre` es el nombre de la constante.
- `valor` es el valor de la constante.

Por ejemplo, para declarar una constante de tipo entero con el valor `10`, se puede hacer lo siguiente:

```c++
const int numero = 10;
```

En este caso, `numero` es una constante de tipo entero con el valor `10`.

## Definición de constantes en preprocesador

Otra forma de definir constantes en C++ es utilizando directivas del preprocesador, como `#define`. Por ejemplo, para
definir una constante de tipo entero con el valor `20`, se puede hacer lo siguiente:

```c++
#define NUMERO 20
```

En este caso, `NUMERO` es una constante de tipo entero con el valor `20`.

Es importante tener en cuenta que las constantes definidas con `#define` no tienen un tipo de dato asociado y no
respetan el ámbito de las variables, por lo que pueden causar problemas si se utilizan de forma indiscriminada.

## Ventajas de utilizar constantes

El uso de constantes en un programa tiene varias ventajas, entre las que se encuentran:

- **Legibilidad**: Al utilizar constantes con nombres descriptivos en lugar de valores literales, se facilita la
  comprensión del código.
- **Mantenibilidad**: Si se necesita cambiar el valor de una constante, basta con modificar su definición en un solo
  lugar.
- **Seguridad**: Las constantes evitan que se modifiquen valores por error y ayudan a prevenir errores en el código.
- **Eficiencia**: Al utilizar constantes en lugar de valores literales, se evita la repetición de código y se mejora la
  eficiencia del programa.
- **Portabilidad**: Al utilizar constantes en lugar de valores literales, se facilita la portabilidad del código entre
  diferentes plataformas y sistemas.
- **Facilidad de depuración**: Al utilizar constantes en lugar de valores literales, se facilita la depuración del
  código al identificar rápidamente los valores que pueden estar causando problemas.
- **Documentación**: Al utilizar constantes con nombres descriptivos, se documenta de forma implícita el propósito y el
  significado de los valores utilizados en el código.