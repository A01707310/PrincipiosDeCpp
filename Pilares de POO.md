---
tags: []
created: '2024-11-07'
title: 'Pilares de POO'
---

 Programación Orientada a Objetos (POO): práctica común en programación que **a través de la creación de objetos** organiza el código en pedazos más comprensibles y reutilizables 

Los **objetos** se definen mediante [**clases**](Clases.md), _**Blueprints**_ de  **propiedades y comportamientos heredables** (**atributos** y **métodos**)

## PILARES DE POO:
### Abstracción: 
> Exponer solo lo esencial de un objeto o función y ocultar detalles internos.

Significa **simplificar** un sistema complejo, **enfocándose** en "**qué hace**" un objeto sin detallar "cómo lo hace". La idea es **definir las características y comportamientos esenciales, pero dejando fuera los detalles específicos de la implementación.**

Hacemos esto en los **header files**.

Los headers en C++ definen la "interfaz pública" de clases, funciones y estructuras, mostrando solo lo necesario para que el resto del programa las utilice. Este es precisamente el objetivo de la abstracción en POO.
### Encapsulación:
> Dando acceso sólo a propiedades/comportamientos a criterio

Limitando el acceso a través de **modificadores de acceso** (_private, public, protected_)

Obteniendo/Modificando valores private y protected:

- Haciendo métodos que **obtienen valores** de propiedades private **_(getters)_**

- Haciendo métodos que **modifican valores** de propiedades private **_(setters)_**

### Herencia:
La herencia se refiere a la capacidad de una clase (subclase) de heredar atributos y métodos de otra clase (superclase). 

<details markdown='1'><summary>Ejemplo</summary>

```
class Forma{
    private:
        cantidad_lados;
        perimetro;
        area;
    public:
        int calcular_perimetro(){};
        int calcular_area(){};
};
```
</details>

### Polimorfismo:
Permite que un método se comporte de manera diferente, dependiendo de la clase que se invoque.