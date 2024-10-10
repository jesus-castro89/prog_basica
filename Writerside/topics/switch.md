# En caso de (switch)

La estructura de decisión `switch` es una estructura de control que permite evaluar una expresión y ejecutar un bloque
de código dependiendo del valor de la expresión. La estructura `switch` en pseudocódigo es la siguiente:

```text
n.- En caso de [expresión]
       Caso [valor1]
          Inicio
            [Acción1]
          Fin
       Caso [valor2]
          Inicio
            [Acción2]
          Fin
       ...
       Caso [valorN]
          Inicio
            [AcciónN]
          Fin
       Otro Caso
          Inicio
            [Acción por defecto]
          Fin
```

Como se puede observar, la estructura `switch` consta de varios bloques de código, cada uno asociado a un valor
específico de la expresión. Si el valor de la expresión coincide con alguno de los valores especificados, se ejecuta el
bloque de código correspondiente. Si no se encuentra un valor coincidente, se ejecuta el bloque de código asociado
a `Otro Caso`.

Es importante tener en cuenta que la estructura `switch` no permite evaluar expresiones complejas, como rangos de
valores o expresiones booleanas. Solo se pueden evaluar valores concretos.

## Diagrama de flujo

![switch_flujo.png](switch_flujo.png)

En el diagrama de flujo, la estructura de decisión `switch` se representa con un rombo que contiene la variable o
expresión a evaluar. Cada flecha que sale del rombo representa un caso posible, con una etiqueta que indica el valor
asociado al caso. Si la expresión coincide con alguno de los valores especificados, se sigue la flecha correspondiente
al caso. Si no se encuentra un valor coincidente, se sigue la flecha correspondiente a `Otro Caso`.
