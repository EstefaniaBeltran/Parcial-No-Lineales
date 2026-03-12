
```markdown
# Parcial: Estructuras de Datos No Lineales

**Ciencias de la Computación e Inteligencia Artificial**  
*Yeimy Estefania Beltran Sandoval*

---

Este repositorio contiene la solución al parcial la asignatura **Estructuras de Datos No Lineales**. Se implementan 15 ejercicios que cubren:

- Árboles N-arios (organización universitaria, sistema de archivos, árbol genealógico, menús, dependencias de software).
- Árboles Trie (autocompletado, corrector ortográfico, clasificador de intenciones, diccionario multilenguaje, motor de búsqueda).
- Tablas Hash (registro de estudiantes, comparación Hash vs Trie).
- Heaps y colas de prioridad (heap mínimo, planificador de tareas, simulación de red).

## Estructura del Proyecto

```
├── src/                      # Código fuente de los ejercicios
│   ├── ejercicio01.py        # Estructura Organizacional (Árbol N-ario)
│   ├── ejercicio02.py        # Sistema de Archivos
│   ├── ejercicio03.py        # Árbol Genealógico
│   ├── ejercicio04.py        # Menú de Aplicación
│   ├── ejercicio05.py        # Dependencias de Software
│   ├── ejercicio06.py        # Autocompletado (Trie)
│   ├── ejercicio07.py        # Corrector Ortográfico
│   ├── ejercicio08.py        # Clasificador de Intenciones
│   ├── ejercicio09.py        # Diccionario Multilenguaje (Trie)
│   ├── ejercicio10.py        # Motor de Búsqueda (Trie + Heap)
│   ├── ejercicio11.py        # Registro de Estudiantes (Hash Table)
│   ├── ejercicio12.py        # Comparación Hash vs Trie
│   ├── ejercicio13.py        # Heap Mínimo
│   ├── ejercicio14.py        # Planificador de Tareas
│   └── ejercicio15.py        # Simulación de Red
├── tests/                     # Pruebas unitarias (pytest / unittest)
│   └── (archivos de prueba opcionales)
├── README.md                  # Este archivo
    └── requirements.txt  

```

---

##  Requerimientos

- Python **3.10** o superior.
- No se requieren librerías externas (todo se implementa con la biblioteca estándar: `heapq`, `typing`, `datetime`, etc.).

Si se desea ejecutar las pruebas unitarias, instalar `pytest` (opcional):

```bash
pip install pytest
```

---

## Ejecución

Cada ejercicio es independiente y puede ejecutarse directamente como script principal:

```bash
python src/ejercicio01.py
python src/ejercicio02.py
...
python src/ejercicio15.py
```

Todos los archivos incluyen un bloque `if __name__ == "__main__":` que ejecuta un ejemplo demostrativo de la funcionalidad implementada.

### Pruebas unitarias (opcional)

Si se han implementado pruebas en la carpeta `tests/`, se pueden ejecutar con:

```bash
pytest tests/
```

---

##  Análisis de Complejidad Big O

### Ejercicios 1–5: Árboles N-arios

| Operación           | Complejidad |
|---------------------|-------------|
| Inserción de hijo   | O(1)*       |
| Recorrido completo  | O(n)        |
| Búsqueda por nombre | O(n)        |
| Eliminación         | O(n)        |

*O(1) usando diccionario para acceso directo por nombre.

### Ejercicios 6–10: Árboles Trie

| Operación               | Complejidad        |
|-------------------------|--------------------|
| Inserción               | O(L) (L = longitud)|
| Búsqueda exacta         | O(L)               |
| Búsqueda por prefijo    | O(L + M) (M = número de sugerencias) |
| Sugerencias (generador) | O(L + M)           |

### Ejercicios 11–12: Tablas Hash

| Operación               | Complejidad promedio | Peor caso    |
|-------------------------|----------------------|--------------|
| Inserción               | O(1)                 | O(n)         |
| Búsqueda                | O(1)                 | O(n)         |
| Eliminación             | O(1)                 | O(n)         |

*El peor caso ocurre cuando muchas colisiones degeneran en listas largas.*

### Ejercicios 13–15: Heaps y Colas de Prioridad

| Operación               | Complejidad |
|-------------------------|-------------|
| Inserción (heappush)    | O(log n)    |
| Extracción (heappop)    | O(log n)    |
| Consulta del mínimo     | O(1)        |

---

##  Características Implementadas

- **Type Hints** en todas las funciones y métodos.
- **Docstrings** estilo Google (descripción, Args, Returns, Raises cuando corresponde).
- **Generadores** (`yield`) para recorridos de árboles y sugerencias, optimizando memoria.
- **Métodos mágicos**:
  - `__iter__` en árboles y tablas hash.
  - `__setitem__` y `__getitem__` en la tabla hash (Ejercicio 11).
  - `__lt__` en las clases `Tarea` y `Paquete` para ordenamiento en heaps (Ejercicios 14 y 15).
- Manejo de colisiones en tabla hash mediante encadenamiento.
- Comparación experimental entre Hash y Trie (Ejercicio 12) con medición de tiempos.



*Entrega correspondiente al parcial de Estructuras de Datos No Lineales.*
```
