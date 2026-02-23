# Torres de Hanoi

## 📘 Descripción General

Este proyecto corresponde a un trabajo académico de la asignatura **Fundamentos de Inteligencia Artificial**, cuyo objetivo es aplicar los conceptos de búsqueda de soluciones en espacios de estados utilizando el clásico problema de las **Torres de Hanoi**.

Se desarrolló un sistema capaz de modelar el problema, representar sus estados y aplicar algoritmos de búsqueda para que un agente artificial encuentre la secuencia óptima de movimientos que permite trasladar todos los discos desde la torre inicial hasta la torre objetivo cumpliendo las reglas del juego.

---

## 🎯 Objetivos del Proyecto

* Comprender el modelado de problemas como espacios de estados.
* Representar formalmente estados, acciones y transiciones.
* Implementar algoritmos de búsqueda para encontrar soluciones óptimas.
* Visualizar el estado del problema de forma clara en consola.
* Analizar la eficiencia de los algoritmos de búsqueda.

---

## 🧠 Fundamento Teórico

### Problemas sin Adversario

Las Torres de Hanoi corresponden a un **problema sin adversario**, donde:

* Existe un único agente.
* El objetivo es encontrar una secuencia de acciones que lleve del estado inicial al estado objetivo.
* No hay oponentes ni incertidumbre.

Estos problemas se modelan como un **espacio de estados**, donde:

* **Estados** → configuraciones posibles de los discos en las torres.
* **Acciones** → movimientos válidos de un disco entre torres.
* **Estado inicial** → todos los discos en la torre origen.
* **Estado objetivo** → todos los discos en la torre destino.

---

### Reglas del Problema

El problema consiste en:

* Tres torres: Origen, Auxiliar y Destino.
* Un conjunto de discos de diferentes tamaños.

Reglas:

1. Solo se puede mover un disco a la vez.
2. Solo se puede mover el disco superior de una torre.
3. No se puede colocar un disco grande sobre uno pequeño.

---

### Espacio de Estados

Cada estado puede representarse como una estructura que contiene tres listas:

```
Torre A: [3,2,1]
Torre B: []
Torre C: []
```

El objetivo es llegar a:

```
Torre A: []
Torre B: []
Torre C: [3,2,1]
```

---

### Solución Óptima

El número mínimo de movimientos necesarios está dado por la fórmula:

[
2^n - 1
]

donde **n** es el número de discos.

---

## ⚙️ Implementación Práctica

### Representación del Estado

El estado se representa mediante una estructura que contiene las tres torres y los discos en cada una.

Ejemplo:

```
estado = ([3,2,1], [], [])
```

---

### Generación de Acciones

La función:

```
acciones_disponibles(estado)
```

Retorna todos los movimientos válidos posibles desde el estado actual.

Ejemplo de acción:

```
Mover disco de Torre A a Torre C
```

---

### Transición de Estados

La función:

```
realizar_accion(estado, accion)
```

Genera un nuevo estado aplicando la acción seleccionada.

Esto permite explorar el espacio de estados.

---

### Algoritmo de Solución

Se implementa un algoritmo que permite encontrar la secuencia óptima de movimientos, basado en:

* Búsqueda recursiva
* Exploración sistemática del espacio de estados

El algoritmo garantiza:

* Encontrar la solución óptima
* Cumplir todas las reglas del problema

---

### Motor de Decisión

La función principal:

```
resolver_hanoi(n, origen, auxiliar, destino)
```

Permite generar la secuencia completa de movimientos necesarios para resolver el problema.

---

### Visualización en Consola

El sistema incluye una función que muestra gráficamente el estado de las torres utilizando caracteres ASCII.

Ejemplo:

```
Torre A: [3,2]
Torre B: [1]
Torre C: []
```

Esto permite seguir paso a paso la ejecución del algoritmo.

---

## ▶️ Ejecución

Para ejecutar el proyecto:

```
python main.py
```

Durante la ejecución se mostrará:

* Cada movimiento realizado
* El estado actualizado de las torres
* La solución completa

---

## 📊 Aprendizajes Obtenidos

Este proyecto permitió fortalecer conocimientos en:

* Modelado de problemas como espacios de estados
* Representación computacional de estados
* Implementación de algoritmos de búsqueda
* Resolución de problemas clásicos de inteligencia artificial
* Uso de estructuras de datos
* Visualización en consola

---

## 🔧 Mejoras Futuras

Posibles mejoras:

* Implementar búsqueda BFS y DFS
* Comparar eficiencia entre algoritmos
* Añadir interfaz gráfica
* Permitir seleccionar el número de discos dinámicamente
* Mostrar estadísticas del algoritmo (nodos explorados, tiempo, etc.)

---

## 👨‍💻 Autor

Trabajo realizado por estudiante de Ingeniería en Inteligencia Artificial de la Escuela Colombiana de Ingeniería Julio Garavito:

* David Santiago Pàez Palacio

---

## 📌 Conclusión

El problema de las Torres de Hanoi es un excelente ejemplo para comprender cómo la inteligencia artificial puede modelar y resolver problemas mediante la exploración de espacios de estados. La implementación demuestra cómo un agente puede encontrar una solución óptima utilizando principios fundamentales de búsqueda y representación del conocimiento.

