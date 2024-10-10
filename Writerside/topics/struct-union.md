# Las estructuras y uniones en C++

## Estructuras

Las estructuras son un tipo de dato que permite agrupar diferentes tipos de datos en una sola entidad. En C++, las
estructuras se definen con la palabra clave `struct`.

```c++
struct Persona {
    std::string nombre;
    int edad;
    float altura;
};
```

En el ejemplo anterior, se ha definido una estructura llamada `Persona` que contiene tres miembros: `nombre`, `edad` y
`altura`. Para acceder a los miembros de una estructura, se utiliza el operador punto (`.`).

```c++
Persona p;
p.nombre = "Juan";
p.edad = 25;
p.altura = 1.75;
```

### Inicialización de estructuras

Las estructuras pueden ser inicializadas de la misma forma que los arreglos y los objetos. Se puede inicializar una
estructura proporcionando valores para sus miembros entre llaves `{}`.

```c++
Persona p = {"Juan", 25, 1.75};
```

### Funciones miembro

Las estructuras pueden tener funciones miembro. Para definir una función miembro, se utiliza la misma sintaxis que para
definir una función normal, pero dentro de la definición de la estructura.

```c++
struct Persona {
    std::string nombre;
    int edad;
    float altura;

    void imprimir() {
        std::cout << "Nombre: " << nombre << std::endl;
        std::cout << "Edad: " << edad << std::endl;
        std::cout << "Altura: " << altura << std::endl;
    }
};
```

Para llamar a una función miembro, se utiliza el operador punto (`.`).

```c++
Persona p = {"Juan", 25, 1.75};
p.imprimir();
```

## Uniones

Las uniones son un tipo de dato que permite almacenar diferentes tipos de datos en la misma dirección de memoria. En
C++, las uniones se definen con la palabra clave `union`.

```c++
union Dato {
    int entero;
    float flotante;
};
```

En el ejemplo anterior, se ha definido una unión llamada `Dato` que contiene dos miembros: `entero` y `flotante`. Al
igual que con las estructuras, se puede acceder a los miembros de una unión utilizando el operador punto (`.`).

```c++
Dato d;
d.entero = 10;
std::cout << d.entero << std::endl;
d.flotante = 3.14;
std::cout << d.flotante << std::endl;
```

Toma en cuenta que, al igual que con las estructuras, una unión solo puede tener un miembro activo en un momento dado. Y
que al modificar un miembro de la unión, se sobrescribirá el valor de los demás miembros. Esto se debe a que comparten
la misma dirección de memoria.

### Tamaño de las uniones

El tamaño de una unión es igual al tamaño de su miembro más grande. Esto se debe a que las uniones comparten la misma
dirección de memoria para todos sus miembros.

```c++
union Dato {
    int entero;
    float flotante;
};

std::cout << sizeof(Dato) << std::endl; // Imprime 4
```

En el ejemplo anterior, el tamaño de la unión `Dato` es 4 bytes, ya que el tipo de dato `int` ocupa 4 bytes en la
memoria.

### Uso de uniones

Las uniones son útiles cuando se necesita almacenar diferentes tipos de datos en la misma dirección de memoria. Por
ejemplo, para representar un valor que puede ser un entero o un flotante.

```c++
union Valor {
    int entero;
    float flotante;
};

Valor v;

v.entero = 10;
std::cout << v.entero << std::endl;

v.flotante = 3.14;
std::cout << v.flotante << std::endl;
```

En el ejemplo anterior, la unión `Valor` se utiliza para almacenar un valor que puede ser un entero o un flotante,
dependiendo de cuál miembro se haya modificado.

## Conclusión

Las estructuras y uniones son tipos de datos que permiten agrupar diferentes tipos de datos en una sola entidad. Las
estructuras se utilizan para agrupar datos relacionados, mientras que las uniones se utilizan para almacenar diferentes
tipos de datos en la misma dirección de memoria. Ambos tipos de datos son muy útiles en la programación en C++.