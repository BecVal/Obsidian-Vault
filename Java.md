---
tags:
  - "#lenguajes/java"
  - "#cs/computacion"
  - "#backend"
  - "#oop"
fecha: 2026-01-22
estado: 🟢 Activo
tipo: 🧠 Concepto Fundamental
---

# Java: Arquitectura y Paradigma

## 1. Definición Formal
**Java** es un lenguaje de programación de propósito general, concurrente, fuertemente tipado y basado en clases. Su diseño sigue el paradigma **Orientado a Objetos (POO)**, priorizando la portabilidad del código fuente mediante una máquina virtual intermedia.

> [!QUOTE] Filosofía de Diseño
> *"Write Once, Run Anywhere" (WORA)*.
> Java desacopla el código fuente de la arquitectura de hardware subyacente mediante la abstracción de la JVM.

---

## 2. Arquitectura de Ejecución (El Modelo JVM)
A diferencia de lenguajes compilados a código máquina nativo (como C++ o Go), Java opera en un entorno híbrido de compilación e interpretación.

### Flujo de Compilación
1. **Código Fuente (.java):** Alto nivel, legible por humanos.
2. **Compilador (javac):** Transforma el código fuente en **Bytecode** (`.class`).
3. **Java Virtual Machine (JVM):** Interpreta o compila en tiempo de ejecución (JIT - Just In Time) el bytecode a código máquina específico del sistema operativo.



> [!INFO] ¿Por qué Bytecode?
> El bytecode actúa como un **Lenguaje Intermedio (IR)**. Esto permite que el mismo archivo `.class` se ejecute en Linux, Windows o macOS, siempre que exista una implementación de la JVM para esa plataforma.

---

## 3. Características Científicas Clave

### A. Gestión de Memoria (Garbage Collection)
Java abstrae la gestión manual de memoria (malloc/free de C).
* **Heap:** Donde residen los objetos instanciados.
* **Stack:** Donde residen las referencias y variables primitivas locales.
* **Garbage Collector (GC):** Un proceso demonio que identifica y libera memoria de objetos inalcanzables (sin referencias activas), previniendo *memory leaks* comunes, aunque introduciendo pausas no deterministas.

### B. Sistema de Tipos
Java es **estáticamente tipado** y **fuertemente tipado**.
* Cada variable debe declararse con un tipo de dato.
* La seguridad de tipos se verifica en tiempo de compilación (`compile-time`), reduciendo errores en tiempo de ejecución (`runtime`).

### C. Abstracción y Polimorfismo
Java implementa POO pura (casi en su totalidad, salvo primitivos) permitiendo modelar sistemas complejos mediante:
* **Encapsulamiento:** Ocultamiento de estado interno.
* **Herencia:** Reutilización de comportamiento.
* **Polimorfismo:** Capacidad de un objeto de comportarse de múltiples formas (Vía Interfaces o Herencia).

---

## 4. Estructura Canónica de una Clase

```java
/**
 * Representación abstracta de un proceso computacional.
 */
public class Proceso {
    
    // Estado (Variables de Instancia encapsuladas)
    private int pid;
    private String estado;

    // Constructor (Inicialización)
    public Proceso(int pid) {
        this.pid = pid;
        this.estado = "NUEVO";
    }

    // Comportamiento (Método)
    public void ejecutar() {
        this.estado = "EJECUTANDO";
        System.out.println("Proceso " + this.pid + " iniciado.");
    }
    
    // Entry Point (Punto de entrada estático)
    public static void main(String[] args) {
        Proceso p1 = new Proceso(101);
        p1.ejecutar();
    }
}