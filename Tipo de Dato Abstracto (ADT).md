---
tags: [poo, diseño, ingeniería-software]
alias: [ADT, API, Abstracción de Datos]
---

# Tipo de Dato Abstracto (ADT)

Un ADT es un tipo de dato cuya representación interna está **oculta** al cliente. Nos enfocamos en el *qué* hace (sus operaciones) y no en el *cómo* lo hace.

### Componentes Clave
1. **[[API]] (Interfaz):** Es la lista de constructores y métodos públicos. Funciona como un "contrato" entre el desarrollador de la estructura y el usuario.
2. **Implementación:** El código Java oculto (privado) que realiza las tareas.

### El Objeto
Un ADT se instancia como un **Objeto**, el cual posee tres propiedades esenciales:
1. **Estado:** El valor que contiene (sus variables).
2. **Identidad:** Su ubicación única en memoria (lo distingue de otros con el mismo valor).
3. **Comportamiento:** Cómo reacciona a los métodos del API.