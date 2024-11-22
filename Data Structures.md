---
tags: []
created: '2024-11-11'
title: 'Data Structures'
---

## Data Structures

### Vectors
In orden to declare a Vector, it's **primordial** to include the `vector` library at the top of our code.
**An interesting characteristic of vectors: they don't need a specified length because they're not tied to one**
> Syntax 
```
#include <vector>
vector<type> name; //During initialization
vector<type> name = {element1,element2,(and so on...)}; //Defining when initializing
```

### Arrays 
In orden to declare an array, it's **primordial** to define its **contained data `type`**, **`name`** and **element amount (integer `n`)**.
**Arrays' size it's limited to its previous specified length**
> Syntax 
```
type name[n] = {};
```
### Matrices
In order to declare a matrix it's **primordial** to include its **contained data `type`**, **`name`**, **row amount (integer `m`)**, **column amount (integer `n`)** 
> Syntax
```
 type name[m][n] = {
    {element11, element12, ..., element1n},
    {element21, element22, ..., element2n},
    ...
    {elementm1, elementm2, ..., elementmn}
};
```
### Strings
Before using strings we need to be sure to have their library included at the top of our file.
`#include <strings>`
Once included, we follow the next syntax:
```
std::string name; //When Defining
std::string name="This is a string; //When initializing during definition"; 
```

### Variables and constants
Both are **containers** (literally, spaces in memory) **for an specified data type**, and they share some **similarities**:

- Both need their data type specified before being named.
- Both locate within memory (location indistinct whether the container is constant or not).

They **differ** in some aspects:

- Once defined, constant values can't be changed.
- '`const`' must be specified before declaring a constant because it prevents us from changing fixed values (which may lead to confusing errors when testing our code).

```
const float PI = 3.14; //declaration of a constant
int i=3; //declaration of a variable
```
