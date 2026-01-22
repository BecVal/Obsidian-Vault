---
tags:
  - "#lenguajes/java"
  - "#cs/compiladores"
  - "#sintaxis"
  - "#fundamentos"
fecha: 2026-01-22
padre: [[Java - Arquitectura y Paradigma]]
---

# Java: Sintaxis y Estructura Léxica

## 1. Fundamentos Gramaticales

Desde la perspectiva de la teoría de compiladores, la sintaxis de Java se define mediante una **Gramática Libre de Contexto (CFG)**. Su diseño léxico es descendiente directo de C/C++, adoptando una estructura de bloques jerárquicos.

El compilador `javac` analiza el flujo de caracteres convirtiéndolos en _tokens_ léxicos antes de construir el Árbol de Sintaxis Abstracta (AST).

**Axiomas Sintácticos:**

1. **Sensibilidad Léxica (Case-Sensitivity):** Los identificadores `System` y `system` apuntan a referencias de memoria distintas.
    
2. **Delimitación de Sentencias:** El punto y coma `;` actúa como el símbolo terminal de una instrucción imperativa.
    
3. **Ámbito (Scope):** Las llaves `{ ... }` definen el ciclo de vida y visibilidad de las variables locales (Stack Frames).
    

## 2. Sistema de Tipos (Type System)

Java impone un **tipado estático fuerte**. Cada variable debe declararse explícitamente, lo que permite al compilador realizar una verificación de tipos (_type checking_) rigurosa antes de la ejecución.

### A. Primitivos (Value Types)

Datos atómicos almacenados directamente en la pila de ejecución (_Stack_). Son inmutables en tamaño y no poseen métodos.

|Tipo|Bits|Representación Interna|Rango Aproximado|
|---|---|---|---|
|`byte`|8|Complemento a 2|$-128$ a $127$|
|`int`|32|Complemento a 2|$\approx \pm 2 \times 10^9$|
|`long`|64|Complemento a 2|$\approx \pm 9 \times 10^{18}$ (Sufijo `L`)|
|`double`|64|IEEE 754 (Flotante)|$\approx \pm 1.7 \times 10^{308}$|
|`boolean`|1*|Lógica Binaria|`true` / `false`|
|`char`|16|Unicode (UTF-16)|`\u0000` a `\uffff`|

> [!NOTE] Nota sobre Booleanos (*) Aunque teóricamente requiere 1 bit, el tamaño real en memoria de un `boolean` depende de la implementación específica de la JVM (a menudo se alinea a 1 byte o a una palabra de máquina).

### B. Referencias (Reference Types)

Variables que almacenan direcciones de memoria (punteros gestionados) que apuntan a objetos en el _Heap_.

```java
String cadena = "Inmutable"; // Instancia de la clase String
int[] vector = new int[5];   // Los arrays son objetos en Java
```

## 3. Control de Flujo (Algoritmia)

Estructuras que alteran el contador de programa (PC) para romper la ejecución secuencial.

### Bifurcación Condicional

```java
if (condicion_booleana) {
    // Rama True
} else {
    // Rama False
}

// Operador Ternario (Expresión Condicional)
int x = (a > b) ? a : b; 
```

### Iteración (Bucles)

- **Bucle Determinado (`for`):** Optimizado para recorrer estructuras indexadas.
    
- **Bucle Indeterminado (`while`):** Basado en pre-condiciones de estado.
    
- **Iterador (`for-each`):** Abstracción sintáctica para recorrer colecciones (`Iterable`).
    

```java
// Sintaxis "Enhanced For-Loop"
for (String elemento : listaDeStrings) {
    procesar(elemento);
}
```

## 4. Anatomía de Métodos (Subrutinas)

En Java, las funciones son ciudadanos de segunda clase; deben pertenecer a una clase.

```java
// [Modificadores] [Tipo Retorno] [Identificador] ([Parámetros Formales])
public static double calcularEntropia(double[] probabilidades) {
    if (probabilidades == null) return 0.0; // Cláusula de guarda
    
    // Lógica computacional
    double entropia = 0.0;
    // ... cálculo ...
    return entropia;
}
```

> [!WARNING] Paso de Parámetros Java **siempre** pasa argumentos **por valor** (_pass-by-value_).
> 
> - Para primitivos: Se copia el valor real.
>     
> - Para objetos: Se copia el valor de la referencia (la dirección de memoria), no el objeto en sí.
>     

## 5. Excepciones (Control de Errores)

Mecanismo para manejar anomalías en tiempo de ejecución interrumpiendo el flujo normal.

```java
try {
    // Código propenso a fallos (I/O, Red, Aritmética)
} catch (IOException e) {
    // Manejo específico del error
} finally {
    // Bloque determinista: Se ejecuta SIEMPRE (limpieza de recursos)
}
```

## 6. Referencias Cruzadas

- **Siguiente Nivel:** [[Java - Programación Orientada a Objetos]]
    
- **Conceptos Teóricos:** [[Teoría de Tipos]], [[Gestión de Memoria (Stack vs Heap)]]
    
- **Comparativa:** [[C++ Syntax]] (Punteros explícitos vs Referencias).