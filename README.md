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

##  Requisitos del Sistema

- Python 3.x instalado

Verificar instalación:

```bash
python --version
```

##  Instrucciones para Pruebas

Al ejecutar el programa se mostrará un menú interactivo:

```
========= MENÚ =========
1. Insertar al principio
2. Insertar al final
3. Eliminar por carnet
4. Mostrar lista
5. Mostrar lista inversa (extra)
6. Salir
```

##  Posibles Mejoras Futuras

- Validación de entradas
- Interfaz gráfica
- Persistencia en archivo
- Implementación de búsqueda
- Ordenamiento de nodos
- Implementación con pruebas unitarias

---

