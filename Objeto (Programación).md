---
tags: [poo, conceptos, java, memoria]
alias: [Instancia, Objects]
---

# Objeto (Programación)

Un **Objeto** es una entidad concreta que existe en tiempo de ejecución y que instancia un [[Tipo de Dato Abstracto (ADT)]] (definido mediante una `clase` en Java).

### Las 3 Propiedades Esenciales
Para que una entidad sea considerada un objeto, debe poseer:

1.  **Estado:** Los datos que almacena en un momento dado.
    * *En código:* Sus variables de instancia o atributos.
2.  **Identidad:** Lo que lo distingue de otros objetos, incluso si tienen el mismo estado.
    * *En memoria:* Su dirección única en el [[Heap Memory]].
3.  **Comportamiento:** Las acciones que puede realizar o sufrir.
    * *En código:* Sus métodos (instrucciones).

[Image of Java object memory layout stack vs heap]

### Gestión en Memoria (Java)
Es crucial distinguir entre la **variable** y el **objeto**:
- La **Variable (Referencia):** Vive en el **Stack**. Contiene la dirección de memoria (puntero).
- El **Objeto Real:** Vive en el **Heap**. Contiene los datos.

> `PumaBank cuenta = new PumaBank();`
> * `cuenta` es la referencia (Stack).
> * `new PumaBank()` crea el objeto (Heap).

### 🧠 Conexiones
- Instancia de: [[Clase (Class)]]
- Se compara con: `==` (compara Identidad/Referencia) vs `.equals()` (compara Estado).