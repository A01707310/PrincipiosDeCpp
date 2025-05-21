---
tags: []
created: '2024-11-11'
title: 'Clases'
---
## Clases
> Blueprint: **modelo/plantilla** que **define** la **estructura** y el comportamiento de un objeto o clase.

Las clases son _**Blueprints**_  con los atributos **(propiedades)** y métodos (**comportamientos**) que poseeran los objetos **(instancias)** derivados.
### Identificando Clases
- <details markdown='1'><summary>Identificar posibles objetos</summary>

  - ¿Qué **entidades** del problema a resolver son **relevantes**? (_**Determinando clases**_)
  - Para cada entidad identificada, ¿Qué **propiedades** de esta entidad son **relevantes**? (_**Determinando atributos**_)
  - Para cada entidad identificada, ¿Qué **acciones** puede realizar? (**_Determinando métodos_**)
  
  > Ahora entiende los posibles tipos de relaciones entre clases: _Clase a Clase_, _Clase a Clases_ y _Clases  a Clases_  
</details>

- <details markdown='1'><summary>Generalización y especialización</summary>

  **Generalización**: el uso de clases **(superclases)** que contengan las propiedades y comportamientos que **heredaran** sus **subclases**, evitando así reescribir código (y complicarlo) de manera innecesaria.

  **Especialización**: aprovechamiento de subclases para crear **objetos específicos** que además de contener las propiedades y comportamientos comunes (provistos en la superclase), considerarán **otras propiedades/comportamientos** que les permitirán una **singularidad** como objeto.
</details>


- <details markdown='1'><summary>Revisar y Refinar</summary>

  Nunca esta demás revisar que el diseño de tus objetos y clases sea el óptimo. **Evita la redundancia entre clases** (Principio de Responsabilidad Única). Queremos el mejor código para mantenerlo de manera fácil en el futuro.
</details>

### Atributos/Variables de instancia
> Propiedad, heredable.
Representan las propiedades del objeto a modelar y son accesibles por cualquier método de la misma clase. Cualquier subclase los heredará.
```int num = 1; // tipo nombre = dato;```


Podemos simplemente definirlos al inicio de la clase (aunque pueden inicializarse ahí mismo, pero esto suele hacerse mas adelante en la clase y mediante un constructor).
### Methods
> Comportamiento, heredable.

They can recibe values, use them in operations, and/or return them. Just like functions.
 
The difference remains on their implementation context: **methods are related to objects, functions aren't.** 
### Constructor
> Preconfigurando los objetos productos de tu clase 

Un tipo especial de método, incluido en la clase para inicializar los atributos de futuros objetos. Comparte nombre con la clase y no genera un retorno (ni siquiera `void`). 
### Objetos
Entidad concreta que se crea a partir de estructura y comportamientos de la clase. Si hay un constructor dentro de su clase, los atributos del objeto podrán ser inicializados con mediante este, proporcionándole argumentos.

<details markdown='1'><summary>Inicializar atributos para un objeto</summary>

En clases como esta:

```
class Perro{
    private:
        string nombre;
        int edad;
        double peso;
    public:
        void alimentar(int cantidad_alimento){};
        Perro(string n, int e, double p) : nombre(n), edad(e), peso(p) {};
        //Un constructor puede tener valores por defecto
        Perro(string n=,"Unknown" int e=0, double p=0.0 : nombre(n), edad(e), peso(p) {};
};
```
Maneras de inicializar atributos de nuestros objetos:
- Usando su constructor:
  
  `Perro miPerro("Terry", 4, 36.9)`
- Directamente desde su declaración en la clase:
  ```
  class Perro{
      nombre="Unknown";
      edad=0;
      peso=0.0;
  }
  ```
- Asignar los valores manualmente:
  ```
    Perro miPerro;
    miPerro.nombre="Terry";
    miPerro.edad=4;
    miPerro.peso=36.9
  ```
</details>

### Dibujando diagramas de clase (UML)
A una clase se le representa con una tabla cuyo header será el nombre de la clase misma.

Orden de agrupamiento: 
- Atributos en la parte superior
- Métodos (incluye constructores) en la parte inferior

Criterios de agrupamiento:
- Previo a cada propiedad/comportamiento, un signo que representa su tipo de acceso [revisar modificadores de acceso](https://github.com/A01707310/PrincipiosDeCpp/blob/main/Pilares%20de%20POO.md#encapsulaci%C3%B3n): 

  - '-' para _private_
  - '+' para _public_
  - '#' para _protected_

- Añadir luego de ':' el tipo de dato contenido/retornado para el atributo/propiedad, respectivamente.

<details markdown='1'><summary>Ejemplo de clase en forma de código y de diagrama</summary>

```
class Perro{
    private:
        string nombre;
        int edad;
        double peso;
    public:
        void alimentar(int cantidad_alimento){};
};
```
|Perro|
|:--
|-----------------Atributos------------------|
|- nombre : string|
|- edad : int|
|- peso : double|
|- cantidad_alimento : int|
|-----------------Métodos------------------|
|+ alimentar(cantidad_alimento : int) : void|

</details>


<details markdown='1'><summary>Representando interrelaciones dentro del diagrama</summary>
  
  - Asociación: línea sólida. Indica que hay relación entre los objetos de dos clases.
  - Agregación: línea sólida con rombo abierto (pegado a la clase receptora). Representa dentro de una clase, el recibir un objeto previamente construido (y por tanto independiente) a esta.
  - Composición: línea sólida con rombo cerrado (pegado a la clase contenedora). Representa objetos contenidos dentro de objetos contenedores (lo contenido no puede existir sin su contenedor).
  - Herencia: línea sólida con triángulo hueco (el triángulo pegado a la superclase). Representa clases que heredan propiedades y métodos de otra (una superclase).
  - Realización: línea discontinua con triángulo hueco.
  - Línea discontinua con flecha: Dependencia (una clase depende de otra clase, indicando que un cambio en una puede afectar a la otra)
</details

LINK A UN VIDEO SOBRE DIAGRAMAS UML: https://www.youtube.com/watch?v=6XrL5jXmTwM
