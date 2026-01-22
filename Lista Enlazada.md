---
tags: [estructuras-datos, nodos, memoria-dinámica]
alias: [Linked List, Lista Simple]
---

# Lista Enlazada

Una **Lista Enlazada** es una estructura de datos recursiva compuesta por un grupo de nodos que, juntos, representan una secuencia.

A diferencia del [[Arreglo (Array)]], los elementos **no** se almacenan en bloques contiguos de memoria. Cada elemento "apunta" al siguiente.



### Estructura del Nodo
La unidad básica es el **Nodo**, que contiene dos campos:
1.  **Item (Dato):** La información a guardar (ej. `int`, `String`).
2.  **Next (Puntero):** Una referencia al siguiente nodo de la lista.

```java
// Ejemplo básico de Nodo en Java (Inner Class)
private class Node {
    Item item;
    Node next;
}