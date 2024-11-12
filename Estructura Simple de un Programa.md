---
tags: []
created: '2024-11-11'
title: 'Estructura Simple de un Programa'
---
## Estructura simple de un programa 
1. Inclusión de librerías (`#include <libreria>`)
2. Standard namespace
3. Global main function (an ESSENTIAL)

### Main Function
- **Must** return an integer
- Its parameters between parenthesis, statements between brackets, parameters between parenthesis.
- **Usually** set to **return 0 if statements suceed** (and usually return 1 if they didn't).

```
int main (parameters) {
};
```
### Librerías
Conjunto de clases y funciones orientadas a realizar tareas específicas. C++ tiene su propia [Librería Estándar de C++](https://en.cppreference.com/w/cpp/header), pero existen muchas más.

### Namespaces 
Organizadores de nombres. Evitan que variables, funciones o clases de distintas partes de un programa (o librerías) **pero homónimas entre sí**, entren en **conflicto**.

> Definiendo namespaces:

```
namespace Primera {
    void pedirEntrada() {
    }
};

namespace Segunda {
    void pedirEntrada() {
    }
};
```
En ambos namespaces se define la función `pedirEntrada`. Para llamar una función en específico, se añade su prefijo de namespace

> Usándolos:

```
Segunda::pedirEntrada();
```
