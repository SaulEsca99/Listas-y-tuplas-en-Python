# 📊 Actividad 1: Listas y tuplas en Python
## Aprendizaje de máquina

**Integrantes:**
* González Pérez Monserrat
* Escamilla Lazcano Saúl
* Pérez Méndez Nancy Esmeralda
* Valencia Hernandez Kevin Guadalupe
* Zamudio López Leonardo

**Grupo:** 5BV1
**Profesora:** Dra. Camacho Vázquez Vanessa Alejandra
**Fecha:** 03/09/25

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange.svg)](https://jupyter.org/)

## 🚀 Descripción General del Proyecto

Este proyecto es un Jupyter Notebook que sirve como una introducción práctica y comparativa a dos de las estructuras de datos más fundamentales de Python: **Listas** y **Tuplas**.

El objetivo es explorar sus diferencias clave, con un enfoque en la **mutabilidad** (listas) frente a la **inmutabilidad** (tuplas), y cómo manipular cada una de ellas.

El proyecto demuestra las siguientes competencias:
1.  **Creación y Manipulación de Tuplas:** Se explora la creación, iteración, slicing e inmutabilidad.
2.  **Operaciones y Métodos de Listas:** Se demuestra la mutabilidad de las listas y se aplica un catálogo completo de métodos (`append`, `remove`, `sort`, `extend`, etc.).
3.  **Estructuras de Datos Complejas:** Se muestra cómo anidar listas y tuplas para crear estructuras de datos más complejas y cómo acceder a sus elementos.
4.  **Comprensión de Listas:** Se introduce y aplica la sintaxis de *list comprehension* como una alternativa eficiente a los bucles `for` tradicionales.

---

## 📊 1. Comparativa: Tuplas vs. Listas

El núcleo de la práctica es entender la diferencia fundamental entre estas dos estructuras ordenadas.

| Característica | Tupla | Lista |
| :--- | :--- | :--- |
| **Sintaxis** | Paréntesis `()` | Corchetes `[]` |
| **Mutabilidad** | **Inmutable** (No se puede cambiar) | **Mutable** (Se puede cambiar) |
| **Uso Común** | Para datos que no deben cambiar (ej. coordenadas, constantes). | Para colecciones flexibles de datos que crecerán o cambiarán (ej. una lista de usuarios). |

---

## 🧱 2. Tuplas (Inmutables)

Se exploran las operaciones básicas con tuplas, destacando su naturaleza inmutable.

* **Creación:** `tupla1 = (1, 3, 5, 7)`
* **Iteración:** Se pueden recorrer con bucles `for` directos o usando índices con `range(len(tupla))`.
* **Inmutabilidad:** Un intento de modificar un elemento (`tupla2[0] = 5`) genera un `TypeError`, lo cual se captura en un bloque `try-except` para demostrar que la operación falla.
* **Slicing:** Se pueden extraer sub-tuplas usando slicing (`tupla1[::2]`).
* **Tipos Mixtos:** Pueden contener cualquier tipo de dato, incluyendo otras listas o tuplas. `tup2 = (1, "John", tupla1, True, -23.1)`

---

## 🔄 3. Listas (Mutables)

Se demuestra la flexibilidad de las listas y su amplio conjunto de métodos para modificarlas *in-place*.

* **Creación:** `lista1 = ['Alvaro', 'Daniel', 'Pilar', 'Beatriz']`
* **Mutabilidad:** A diferencia de las tuplas, la asignación de un nuevo valor a un índice (`lista1[0] = 5`) es una operación válida y modifica la lista original.
* **Métodos Principales (Demostrados en Sec. 19):**
    * `append(6)`: Añade el 6 al final.
    * `extend([7, 8, 9])`: Añade los elementos 7, 8 y 9 al final.
    * `insert(2, 99)`: Inserta el 99 en el índice 2.
    * `remove(99)`: Elimina la primera aparición del valor 99.
    * `pop(4)`: Elimina y devuelve el elemento en el índice 4.
    * `sort()`: Ordena la lista numéricamente.
    * `reverse()`: Invierte el orden de los elementos.
    * `count(3)`: Devuelve cuántas veces aparece el valor 3.
    * `copy()`: Crea una copia superficial de la lista.
    * `clear()`: Elimina todos los elementos de la lista.

---

## 🪆 4. Estructuras Anidadas y Conversiones

El notebook explora cómo las listas y tuplas pueden interactuar y contenerse mutuamente.

* **Anidación:** Se crean estructuras complejas como una tupla que contiene una lista: `t2 = ([(1, 'Oleg', 24.5), ['Maria', 'Bonita']], 'manzana')`.
* **Acceso Anidado:** Se accede a elementos profundos usando múltiples corchetes. Por ejemplo, para acceder a `'Maria'`, se usa `t2[0][1][0]`.
* **Conversión de Tipos:**
    * `tuple(lista1)`: Convierte una lista en una tupla.
    * `list(vocalTupla)`: Convierte una tupla en una lista.
    * `list(alfabeto)`: Convierte un string en una lista de caracteres.
* **Concatenación vs. Anidación:** Se demuestra la diferencia entre unir dos listas en una sola (`alfanumL = alfaL + numL`) y crear una lista que contiene otras dos listas (`alfanumLL = [alfaL, numL]`).

---

## ⚡ 5. Comprensión de Listas (List Comprehension)

Finalmente, se introduce la *list comprehension* como una sintaxis más limpia y eficiente para crear listas basadas en iterables.

**Método Tradicional (Bucle For):**
```python
frutas = ['manzana', 'kiwi', 'guanabana', 'limon']
lista2 = []
for x in frutas:
    if "a" in x:
        lista2.append(x)
# Resultado: ['manzana', 'guanabana']
