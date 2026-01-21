---
tags: [estructura-datos, java, memoria-contigua]
alias: [Arrays, Arreglos]
---

# Arreglo (Array)

Es la estructura más básica para almacenar una secuencia de valores del **mismo tipo** en bloques de memoria contiguos.

En [[Java]], se accede mediante la notación `a[i]`.

### Análisis de Rendimiento

| Operación | Complejidad | Notas |
| :--- | :---: | :--- |
| **Acceso (Indexación)** | $O(1)$ | Muy rápido si conoces el índice `i`. |
| **Inserción** | $O(n)$ | Lento. Requiere mover elementos o crear un nuevo array si está lleno. |
| **Búsqueda** | $O(n)$ | Lento si no está ordenado (hay que recorrerlo todo). |
| **Borrado** | $O(n)$ | Lento. Requiere desplazar los elementos huecos. |

### Limitaciones
- **Tamaño Fijo:** En Java, una vez declarado con `new type[size]`, no puede crecer.
- **Alternativa:** Si se requiere tamaño dinámico, es mejor usar una [[Lista Enlazada]].