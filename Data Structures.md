---
tags: []
created: '2024-11-11'
title: 'Data Structures'
---

## Data Structures
### Arrays 
In orden to declare an array, it's **primordial** to define its **contained data `type`**, **`name`** and **element amount (integer `n`)**.
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
