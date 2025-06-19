---
sidebar_position: 7
---

# Proyecto práctico del bloque 1

## Objetivo general

Desarrollar un mini sistema en Java que aplique todos los conceptos del Bloque 1: clases, objetos, POJOs, constructores, encapsulamiento, uso de toString(), enum, String, StringBuffer, y pruebas con JUnit 5, siguiendo buenas prácticas de POO.

## Conceptos Integrados

|Concepto|Aplicación obligatoria en el proyecto|
|--|--|
|Clases y objetos|Modelado de entidades (Student, Course, etc.)|
|Encapsulamiento (`private`, `get/set`)|Gestión segura de atributos|
|Constructores vacíos y con parámetros|Inicialización flexible|
|`toString()`|Visualización de objetos en consola|
|`enum`|Representación de estados o roles|
|`String` y `StringBuffer`|Gestión de texto mutable/inmutable|
|Javadoc|Documentación profesional del código|
|Diagrama UML|Modelado estático de las clases|
|JUnit 5|Validación del comportamiento|

## Retos Propuestos

### 01: Sistemas de gestión de estudiantes

Diseñar un sistema que permita registrar estudiantes, cursos y su estado de inscripción.

Clases sugeridas:

- `Student`: nombre, código, estado (enum), comentarios (StringBuffer)
- `Course`: nombre, código, tipo (enum), cupo
- `Enrollment`: relación entre `Student` y `Course`
- `App`: clase main
- `Formatter`: para imprimir reportes legibles
- `StudentStatus` (enum): `ACTIVE`, `DROPPED`, `GRADUATED`
- `CourseType` (enum): `MANDATORY`, `ELECTIVE`

Objetivos técnicos:

- Modelar entidades (Student, Course, Enrollment) con clases POJO.
- Usar enum para estados y tipos (StudentStatus, CourseType).
- Aplicar StringBuffer para comentarios editables.
- Generar reportes legibles y probar con JUnit 5.

### 02: Sistemas de Gestión de Vehículos y Mantenimiento

Construir un sistema que permita registrar vehículos y sus reportes de mantenimiento. Cada vehículo tiene datos básicos y puede recibir observaciones técnicas escritas por el mecánico (usando StringBuffer).

Clases sugeridas:

- `Vehicle`: placa, marca, tipo (enum), año
- `MaintenanceRecord`: ID, fecha, mecánico, descripción (StringBuffer), estado (enum)
- `VehicleType` (enum): `CAR`, `MOTORCYCLE`, `TRUCK`, `BUS`
- `MaintenanceStatus` (enum): `PENDING`, `IN_PROGRESS`, `COMPLETED`
- `Formatter`: imprime reportes por vehículo
- `App`: clase principal para probar

Objetivos técnicos:

- Modelar relación 1 a muchos: un vehículo tiene varios mantenimientos
- Usar enum para clasificar tipos y estados
- Modificar descripciones usando StringBuffer
- Mostrar el historial del vehículo con toString()

### 03: Gestión de pedidos en una Cafetería Universitaria

Simular un sistema básico para registrar pedidos, clasificar productos y almacenar observaciones del cliente (por ejemplo, "sin azúcar", "para llevar", etc.).

Clases sugeridas:

- `Customer`: nombre, ID, categoría (enum) – ejemplo: `STUDENT`, `PROFESSOR`, `VISITOR`
- `Product`: código, nombre, tipo (enum), precio
- `Order`: ID, cliente, lista de productos, nota especial (StringBuffer)
- `Formatter`: imprime ticket de compra
- `App`: clase principal

Objetivos técnicos:

- Implementar listas y relaciones entre objetos (`ArrayList<Product>`)
- Construir y modificar notas con StringBuffer
- Categorizar productos con enum (`DRINK`, `FOOD`, `SNACK`)
- Usar toString() para presentar un recibo formateado

## Entregables por grupo

1. Proyecto en Java con:
   - Código limpio y comentado (JavaDoc)
   - Pruebas unitarias con JUnit 5
2. Diagrama de clases en formato UML (Mermaid o PlantUML)
3. Presentación oral breve (3–5 min)
   - ¿Qué clases crearon y por qué?
   - ¿Qué principios aplicaron?
   - ¿Qué retos encontraron?

## Criterios de evaluación

|Criterio|Ponderación|
|--|--|
|Aplicación de principios POO|30%|
|Buenas prácticas (nombres, JavaDoc, modularidad)|20%|
|Diagrama UML claro y coherente|20%|
|Pruebas unitarias funcionales|15%|
|Presentación y argumentación|15%|
