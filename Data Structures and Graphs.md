# Capitulo 1
1. Definiciones Fundamentales

• **Algoritmo:** Es un método finito, determinista y efectivo para resolver un problema, adecuado para su implementación como programa de computadora. Es la descripción de los pasos para realizar una tarea.

• **Estructura de Datos:** Es un esquema para organizar datos en la memoria de una computadora (y a veces en disco) de manera que puedan ser procesados eficientemente por un algoritmo.

**La Relación:** Los algoritmos y las estructuras de datos son inseparables. Una estructura de datos existe como el producto final o subproducto de un algoritmo; debemos estudiarlas para entender cómo funcionan los algoritmos. De hecho, estructuras simples pueden dar lugar a algoritmos complejos y viceversa.

2. El Modelo de Programación Básico en Java

Antes de crear estructuras complejas, el primer capítulo establece las herramientas básicas del lenguaje (Java) que utilizaremos:

• **Tipos de Datos Primitivos:** Son la base del lenguaje. Incluyen enteros (int), números reales (double), booleanos (boolean para lógica verdadero/falso) y caracteres (char). Se combinan mediante operaciones (como +, -, /) para formar **expresiones**.

• **Sentencias:** Definen la computación. Incluyen:

    ◦ _Declaraciones:_ Crean variables de un tipo específico.

    ◦ _Asignaciones:_ Asocian un valor a una variable.

    ◦ _Condicionales (if, else):_ Controlan el flujo de ejecución.

    ◦ _Bucles (while, for):_ Permiten la repetición de instrucciones (iteración).

• **Arreglos (Arrays):** Es la estructura más básica para almacenar una secuencia de valores del mismo tipo. Usamos la notación a[i] para acceder al valor en la posición i. Crear un arreglo implica declararlo, asignarle espacio con new e inicializar sus valores.

• **Métodos Estáticos:** Son funciones que encapsulan y reutilizan código. Toman argumentos y pueden devolver un valor o causar un efecto secundario (como imprimir en pantalla).

3. Abstracción de Datos (ADT)

Este es quizás el concepto más importante del primer capítulo. Pasamos de escribir código simple a la **Programación Orientada a Objetos (POO)**.

• **Tipo de Dato Abstracto (ADT):** Es un tipo de dato cuya representación interna está oculta al cliente (quien usa el código). Nos enfocamos en _qué_ hace la estructura (sus operaciones) y no en _cómo_ lo hace internamente.

• **API (Interfaz de Programación de Aplicaciones):** Es la lista de constructores y métodos que ofrece un ADT. Sirve como un contrato entre el que implementa la estructura y el que la usa.

• **Objetos:** Son entidades que pueden tomar un valor de un tipo de dato. Se caracterizan por tres propiedades esenciales:

    1. **Estado:** El valor que contiene.

    2. **Identidad:** Lo que lo distingue de otros objetos (su ubicación en memoria).

    3. **Comportamiento:** El efecto de las operaciones (métodos) sobre él.

4. Ventajas y Desventajas Generales por ejemplo:

• **Arreglos:**

    ◦ _Ventaja:_ Inserción rápida y acceso muy rápido si se conoce el índice.

    ◦ _Desventaja:_ Tamaño fijo, búsqueda y borrado lentos (si no se conoce el índice).

• **Listas Enlazadas:**

    ◦ _Ventaja:_ Inserción y borrado rápidos; tamaño dinámico.

    ◦ _Desventaja:_ Búsqueda lenta (hay que recorrerla) y acceso lento a elementos individuales.
