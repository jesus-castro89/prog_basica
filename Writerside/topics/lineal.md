# La estructura de Decisión

La estructura de decisión es una estructura de control que permite tomar decisiones en un programa. La estructura de
decisión más simple es la estructura `if`, que evalúa una condición y ejecuta un bloque de código si la condición es
verdadera. Si la condición es falsa, el bloque de código no se ejecuta.

La estructura de decisión en pseudocódigo es la siguiente:

```text
n.- Si [condición]
       Entonces
          Inicio
            [Acción]
          Fin
       Si no
          Inicio
            [Acción]
          Fin
```

Como se puede observar, la estructura de decisión `if` consta de dos bloques de código: el bloque `Entonces` y el bloque
`Si no`. El bloque `Entonces` se ejecuta si la condición es verdadera, mientras que el bloque `Si no` se ejecuta si la
condición es falsa.

Así mismo, la estructura de decisión `if` puede tener múltiples condiciones anidadas. En este caso, se evalúan las
condiciones en orden y se ejecuta el bloque de código correspondiente a la primera condición verdadera. Si ninguna
condición es verdadera, no se ejecuta ningún bloque de código.

La estructura de decisión en pseudocódigo con múltiples condiciones es la siguiente:

```text
n.- Si [condición1]
       Entonces
          Inicio
            [Acción1]
          Fin
       Si no
          Si [condición2]
             Entonces
                Inicio
                  [Acción2]
                Fin
          Si no
            Si [condición3]
                Entonces
                   Inicio
                       [Acción3]
                   Fin
            Si no
                    Inicio
                        [Acción4]
                    Fin
```

## Diagrama de flujo

![desicion_flujo.png](desicion_flujo.png)

En el diagrama de flujo, la estructura de decisión `if` se representa con un rombo que contiene
la condición a evaluar. Si la condición es verdadera, se sigue la flecha que apunta hacia el bloque de código que se
ejecuta. Si la condición es falsa, se sigue la flecha que apunta hacia el bloque de código que no se ejecuta.

En el ejemplo se omite el texto "Si" y "No", debido a que queda a criterio del programador agregarlo en la dirección que
considere más adecuada.