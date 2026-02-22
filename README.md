#  Implementación de Lista Doblemente Enlazada en Python

##  Descripción General

Este proyecto consiste en la implementación completa de una **estructura de datos dinámica tipo Lista Doblemente Enlazada**

Este programa permite gestionar registros de estudiantes mediante los siguientes atributos:

- Nombre
- Apellido
- Carnet

El sistema funciona mediante un menú interactivo en consola que permite al usuario manipular la estructura de datos dinámicamente.

---

##  Objetivos del Proyecto

- Implementar una estructura de datos enlazada sin utilizar listas nativas de Python.
- Aplicar conceptos de nodos, referencias y punteros.
- Practicar inserción y eliminación en estructuras dinámicas.
- Permitir recorrido bidireccional de la lista.
- Simular el funcionamiento interno de estructuras utilizadas en sistemas reales.

---

##  Estructura del Programa

El programa está compuesto por tres partes principales:

### 1️ Clase `Nodo`

Representa cada elemento de la lista y contiene:

- `nombre`
- `apellido`
- `carnet`
- `siguiente`
- `anterior`

Cada nodo mantiene referencia tanto al nodo siguiente como al anterior, permitiendo navegación bidireccional.

---

###  Clase `ListaDoblementeEnlazada`

Administra la estructura completa mediante:

- `cabeza`: primer nodo de la lista
- `cola`: último nodo de la lista

Contiene los siguientes métodos:

- `insertar_al_principio()`
- `insertar_al_final()`
- `eliminar_por_valor()`
- `mostrar_lista()`
- `mostrar_lista_inversa()`

Cada operación actualiza correctamente las referencias para mantener la integridad de la estructura.

---

###  Función `menu()`

Permite interacción con el usuario mediante consola, ofreciendo un sistema de opciones para ejecutar las operaciones disponibles.

---

##  Instrucciones Detalladas para Pruebas del Programa

Esta sección describe paso a paso cómo verificar el correcto funcionamiento de la lista doblemente enlazada mediante diferentes escenarios de prueba.

Al ejecutar el programa, se mostrará el siguiente menú interactivo:

```
========= MENÚ =========
1. Insertar al principio
2. Insertar al final
3. Eliminar por carnet
4. Mostrar lista
5. Mostrar lista inversa (extra)
6. Salir
```

A continuación se detallan los casos de prueba recomendados:

---

###  1. Prueba de Inserción al Principio

**Objetivo:** Verificar que el nuevo nodo se convierta en la cabeza de la lista y que las referencias se actualicen correctamente.

Pasos:

1. Seleccionar opción `1`
2. Ingresar los datos solicitados:
   - Nombre
   - Apellido
   - Carnet
3. Repetir el proceso con al menos 2 o 3 registros adicionales.
4. Seleccionar opción `4` para mostrar la lista.

Resultado esperado:

- El último nodo insertado debe aparecer primero.
- Las referencias deben mostrarse correctamente en orden.

Ejemplo esperado:

```
None <- [Ana López (2023003)] <-> [Carlos Pérez (2023002)] <-> [Juan García (2023001)] <-> None
```

---

###  2. Prueba de Inserción al Final

**Objetivo:** Confirmar que el nodo se agregue al final y que la cola se actualice correctamente.

Pasos:

1. Seleccionar opción `2`
2. Ingresar los datos
3. Insertar al menos 2 registros
4. Mostrar la lista con opción `4`

Resultado esperado:

- El orden debe mantenerse según el orden de inserción.
- El último nodo insertado debe aparecer antes de `None`.

---

###  3. Prueba de Eliminación de Nodo Intermedio

**Objetivo:** Verificar que las referencias anterior y siguiente se reconecten correctamente.

Pasos:

1. Insertar al menos 3 nodos.
2. Seleccionar opción `3`.
3. Ingresar el carnet de un nodo que esté en medio.
4. Mostrar la lista.

Resultado esperado:

- El nodo eliminado ya no debe aparecer.
- Los nodos anterior y siguiente deben estar correctamente enlazados.

---

###  4. Prueba de Eliminación del Primer Nodo

**Objetivo:** Validar que la cabeza cambie correctamente.

Pasos:

1. Insertar varios nodos.
2. Eliminar el carnet del primer nodo.
3. Mostrar la lista.

Resultado esperado:

- La nueva cabeza debe ser el segundo nodo.
- Su referencia `anterior` debe ser `None`.

---

###  5. Prueba de Eliminación del Último Nodo

**Objetivo:** Validar que la cola se actualice correctamente.

Pasos:

1. Insertar varios nodos.
2. Eliminar el último carnet.
3. Mostrar la lista.

Resultado esperado:

- La cola debe actualizarse al nodo anterior.
- Su referencia `siguiente` debe ser `None`.

---

###  6. Prueba de Eliminación de Carnet Inexistente

**Objetivo:** Confirmar que el programa maneje correctamente un valor no encontrado.

Pasos:

1. Seleccionar opción `3`
2. Ingresar un carnet que no exista

Resultado esperado:

```
No se encontró un nodo con ese carnet.
```

El programa no debe cerrarse ni generar errores.

---

###  7. Prueba de Lista Vacía

**Objetivo:** Verificar el comportamiento cuando no hay nodos.

Pasos:

1. Ejecutar el programa.
2. Seleccionar opción `4` sin haber insertado datos.

Resultado esperado:

```
None <- None
```

---

###  8. Prueba de Recorrido Inverso

**Objetivo:** Confirmar el funcionamiento bidireccional de la estructura.

Pasos:

1. Insertar varios nodos.
2. Seleccionar opción `5`.

Resultado esperado:

- Los nodos deben mostrarse desde la cola hacia la cabeza.
- El orden debe ser inverso al mostrado en la opción 4.

---

##  Validación General

El programa funciona correctamente si:

- No se generan errores durante inserciones o eliminaciones.
- Las referencias anterior y siguiente se mantienen coherentes.
- La lista puede recorrerse en ambos sentidos.
- Se manejan adecuadamente casos especiales como lista vacía o eliminación del único nodo.

---
##  Posibles Mejoras Futuras

- Validación de entradas
- Interfaz gráfica
- Persistencia en archivo
- Implementación de búsqueda
- Ordenamiento de nodos
- Implementación con pruebas unitarias

---

