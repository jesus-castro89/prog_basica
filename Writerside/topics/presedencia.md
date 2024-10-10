# Precedencia de operadores en C++

La precedencia de operadores en C++ determina el orden en que se evalúan las expresiones en una instrucción. Es
importante comprender la precedencia de los operadores para evitar errores y garantizar que las expresiones se evalúen
correctamente.

## 1.- Precedencia de operadores

La precedencia de los operadores en C++ se basa en la jerarquía de los operadores y determina el orden en que se evalúan
las expresiones. A continuación, se presenta una lista de los operadores en orden de precedencia, de mayor a menor:

1. Paréntesis `()`
2. Operadores unarios `+`, `-`, `!`, `~`, `++`, `--`
3. Multiplicación `*`, División `/`, Módulo `%`
4. Suma `+`, Resta `-`
5. Relacionales `<`, `<=`, `>`, `>=`
6. Igualdad `==`, Desigualdad `!=`
7. AND lógico `&&`
8. OR lógico `||`
9. Operador condicional `? :`, también llamado operador ternario.
10. Asignación `=`, Asignación de suma `+=`, Asignación de resta `-=`, Asignación de multiplicación `*=`, Asignación
    de división `/=`, Asignación de módulo `%=`, Asignación de AND `&=`, Asignación de XOR `^=`, Asignación de OR `|=`.

Es importante tener en cuenta que los operadores con mayor precedencia se evalúan antes que los operadores con menor
precedencia. Por ejemplo, en la expresión `a + b * c`, la multiplicación se evaluará antes que la suma debido a la
precedencia de los operadores.

## 2.- Ejemplos de precedencia de operadores

A continuación, se presentan algunos ejemplos de expresiones con diferentes operadores y su respectiva evaluación:

### 2.1.- Ejemplo 1

```c++
#include <iostream>

using namespace std;

int main() {
    int a = 5, b = 10, c = 2, resultado;

    resultado = a + b * c;

    cout << "El resultado es: " << resultado << endl;

    return 0;
}
```

En este caso, la expresión `a + b * c` se evaluará primero la multiplicación `b * c` y luego la suma `a + (b * c)`. El
resultado se almacenará en la variable `resultado` y se imprimirá en la consola.

### 2.2.- Ejemplo 2

```c++
#include <iostream>

using namespace std;

int main() {
    int a = 5, b = 10, c = 2, resultado;

    resultado = (a + b) * c;

    cout << "El resultado es: " << resultado << endl;

    return 0;
}
```

En este caso, la expresión `(a + b) * c` se evaluará primero la suma `a + b` y luego la multiplicación `(a + b) * c`. El
resultado se almacenará en la variable `resultado` y se imprimirá en la consola.

## 3.- Conclusiones

La precedencia de operadores en C++ es fundamental para comprender cómo se evalúan las expresiones en un programa. Al
conocer la precedencia de los operadores, los programadores pueden escribir código más claro y evitar errores de
evaluación en las expresiones. Es importante recordar que los paréntesis pueden utilizarse para modificar el orden de
evaluación de los operadores y garantizar que las expresiones se evalúen correctamente.