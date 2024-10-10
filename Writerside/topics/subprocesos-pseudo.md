# Subprocesos (Pseudocódigo)

Dentro de los algoritmos usando pseudocódigo y diagramas de flujo, los subprocesos son una parte importante para dividir
la lógica del programa en partes más pequeñas y manejables. Un subproceso es una secuencia de instrucciones que se
ejecutan de manera independiente al programa principal. En este tutorial, aprenderás cómo crear y utilizar subprocesos
en tus algoritmos.

## 1. Creando un subproceso

Para crear un subproceso en un algoritmo, debes seguir los siguientes pasos:

1. Definir la función del subproceso: La función del subproceso es un bloque de código que contiene las instrucciones
   que se ejecutarán en el subproceso. La función debe tener un nombre único y puede o no recibir parámetros.
2. Llamar al subproceso: Para llamar al subproceso desde el programa principal, debes usar el nombre de la función
   seguido de los parámetros necesarios.

A continuación, se muestra un ejemplo de cómo crear y utilizar un subproceso en un algoritmo:

```
Nombre del Algoritmo: Prueba de Subproceso

Definición de Subprocesos:
    Nombre del subproceso: `saludar()`
    Definir variables:
        Cadena: `nombre`
    1. Inicio // ó Inicio del subproceso `saludar`
    2. Escribir "Ingrese su nombre:"
    3. Leer `nombre`
    4. Escribir "¡Hola, " + `nombre` + "!"
    5. Fin // ó Fin del subproceso `saludar`

1. Inicio
2. Llamar al subproceso `saludar()`
3. Fin
```

En este ejemplo, se define un subproceso llamado `saludar` que solicita al usuario ingresar su nombre y luego imprime un
mensaje de saludo con el nombre ingresado. Luego, se llama al subproceso `saludar` desde el programa principal.

## 2. Subprocesos con retorno

Los subprocesos también pueden devolver un valor al programa principal. Para ello, debes definir el tipo de dato que
devolverá el subproceso y utilizar la instrucción `retornar` para enviar el valor al programa principal.

A continuación, se muestra un ejemplo de cómo crear un subproceso con retorno en un algoritmo:

```
Nombre del Algoritmo: Prueba de Subproceso con Retorno

Definición de Subprocesos:
    Nombre del subproceso: `sumar()`
    Definir variables:
        Entero: `a`, `b`
    1. Inicio // ó Inicio del subproceso `sumar`
    2. Leer `a`, `b`
    3. Retornar `a` + `b`
    4. Fin // ó Fin del subproceso `sumar`

1. Inicio
2. Escribir "La suma es: " + sumar()
3. Fin
```

En este ejemplo, se define un subproceso llamado `sumar` que solicita al usuario ingresar dos números enteros y luego
devuelve la suma de los números al programa principal. Luego, se imprime el resultado de la suma en el programa
principal.

## 3. Subprocesos con parámetros

Los subprocesos también pueden recibir parámetros para realizar operaciones específicas. Para ello, debes definir los
parámetros que recibirá el subproceso y utilizarlos en el bloque de código del subproceso.

A continuación, se muestra un ejemplo de cómo crear un subproceso con parámetros en un algoritmo:

```
Nombre del Algoritmo: Prueba de Subproceso con Parámetros

Definir variables:
    Entero: `d1`, `d2`

Definición de Subprocesos:
    Nombre del subproceso: `multiplicar(a, b)`
    Definir variables:
        Entero: `a`, `b`
    1. Inicio // ó Inicio del subproceso `multiplicar`
    2. Retornar `a` * `b`
    3. Fin // ó Fin del subproceso `multiplicar`

1. Inicio
2. Escribir "Ingrese dos números:"
3. Leer `d1`, `d2`
4. Escribir "La multiplicación es: " + multiplicar(`d1`, `d2`)
5. Fin
```