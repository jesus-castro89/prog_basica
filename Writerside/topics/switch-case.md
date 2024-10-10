# El bloque `switch-case`

El bloque `switch-case` es una estructura de control que permite evaluar una expresión y ejecutar un bloque de código dependiendo del valor de la expresión. La sintaxis del bloque `switch-case` es la siguiente:

```c++
switch (expresion)
{
    case valor1:
        // Bloque de código
        break;
    case valor2:
        // Bloque de código
        break;
    // Otros casos
    default:
        // Bloque de código
        break;
}
```

Donde `expresion` es una expresión que se evalúa a un valor entero, `valor1`, `valor2`, etc., son los valores posibles de la expresión y `default` es un caso opcional que se ejecuta si la expresión no coincide con ninguno de los valores anteriores.

Por ejemplo, el siguiente código:

```c++
int x = 2;

switch (x)
{
    case 1:
        cout << "El valor es 1" << endl;
        break;
    case 2:
        cout << "El valor es 2" << endl;
        break;
    default:
        cout << "El valor no es ni 1 ni 2" << endl;
        break;
}
```

Imprimirá `El valor es 2` en la consola, ya que `x` tiene el valor 2.

El bloque `switch-case` es muy útil para simplificar la escritura de múltiples sentencias `if-else if-else`, especialmente cuando se tienen múltiples casos a evaluar. Sin embargo, se debe tener en cuenta que solo se pueden evaluar expresiones enteras y que cada caso debe terminar con una sentencia `break` para evitar que se ejecuten los casos siguientes.

## Reglas de uso

El bloque `switch-case` se puede utilizar en cualquier lugar donde se pueda utilizar una sentencia `if-else if-else`, pero es especialmente útil cuando se tienen múltiples casos a evaluar. Se recomienda usar el bloque `switch-case` en lugar de múltiples sentencias `if-else if-else` cuando se tienen más de tres casos a evaluar.

```c++
int x = 2;

switch (x)
{
    case 1:
        cout << "El valor es 1" << endl;
        break;
    case 2:
        cout << "El valor es 2" << endl;
        break;
    case 3:
        cout << "El valor es 3" << endl;
        break;
    default:
        cout << "El valor no es ni 1, ni 2, ni 3" << endl;
        break;
}
```

En general, se recomienda usar el bloque `switch-case` cuando se tienen múltiples casos a evaluar y se conoce de antemano los valores posibles de la expresión. Si los valores posibles de la expresión son desconocidos o no son enteros, se recomienda usar sentencias `if-else if-else` en su lugar.

Sin embargo, es prudente usarlo cuando en casa caso se realizarán o ejecutarán dos
o más instrucciones, de lo contrario, es mejor usar una sentencia `if-else`.