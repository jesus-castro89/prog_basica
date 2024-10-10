# Estructuras Repetitivas

## Introducción

Las estructuras repetitivas son estructuras de control que permiten ejecutar un bloque de código múltiples veces. Estas
estructuras son útiles cuando se necesita realizar una tarea repetitiva, como sumar una lista de números o imprimir una
secuencia de caracteres.

Las estructuras repetitivas más comunes son el bucle `for`, el bucle `while` y el bucle `do while`. El bucle `for` se
utiliza cuando se conoce el número de iteraciones que se deben realizar, mientras que el bucle `while` se utiliza cuando
se desconoce el número de iteraciones.

## Mientras que (while)

La estructura repetitiva `while` es una estructura de control que permite ejecutar un bloque de código mientras se
cumpla una condición. La estructura `while` en pseudocódigo es la siguiente:

```text
n.- Mientras que [condición]
       Inicio
         [Acción]
       Fin
```

![while.png](while.png)

Como se puede observar, la estructura `while` consta de un bloque de código que se ejecuta mientras la condición sea
verdadera. Si la condición es falsa, el bloque de código no se ejecuta.

Es importante tener en cuenta que si la condición es siempre verdadera, el bucle `while` se ejecutará indefinidamente,

## Hacer hasta que (do while)

La estructura repetitiva `do while` es una estructura de control que permite ejecutar un bloque de código al menos una
vez y luego repetirlo mientras no se cumpla una condición. La estructura `do while` en pseudocódigo es la siguiente:

```text
n.- Hacer
       Inicio
         [Acción]
       Fin
    Hasta que [condición]
```

![dowhile.png](dowhile.png)

Como se puede observar, la estructura `do while` consta de un bloque de código que se ejecuta al menos una vez y luego
se repite mientras la condición sea falsa. Si la condición es verdadera, se continuará con el flujo del programa.

Al igual que con el bucle `while`, si la condición es siempre falsa, el bucle `do while` se ejecutará
indefinidamente.

## Para (for)

La estructura repetitiva `for` es una estructura de control que permite ejecutar un bloque de código un número fijo de
veces. La estructura `for` en pseudocódigo es la siguiente:

```text 
n.- Para [variable] = [inicio] Hasta [fin] Con Paso [paso] Hacer
       Inicio
         [Acción]
       Fin
```

Como se puede observar, la estructura `for` consta de una variable de control que se inicializa con un valor inicial y
luego se incrementa o decrementa en cada iteración. El bucle se ejecuta mientras la variable de control esté dentro del
rango especificado.

Sin embargo, la estructura `for` también puede no declarar la variable de control en la misma línea. En este caso, la
variable de control se declara e inicializa fuera del bucle y se incrementa o decrementa dentro del bucle. La estructura
`for` en pseudocódigo sin declarar la variable de control es la siguiente:

```text
n.- [variable] = [inicio]
m.- Para Hasta [condición] Con Paso [paso] Hacer
       Inicio
         [Acción]
       Fin
```

Como se puede observar, la estructura `for` sin declarar la variable de control consta de una condición que se evalúa en
cada iteración. El bucle se ejecuta mientras la condición sea verdadera.

Por último, el segmento `Con Paso [paso]` es opcional y se utiliza para especificar el incremento o decremento de la
variable de control en cada iteración. Si no se especifica, la variable de control se incrementa o decrementa en una
unidad por defecto. Además de esto, el segmento `Con Paso [paso]` también puede ser negativo, lo que permite decrementar
la variable de control en cada iteración. Aunque también se puede emplear para realizar algún tipo de operación en la
variable de control.

#### Diagrama de flujo

![for.png](for.png)