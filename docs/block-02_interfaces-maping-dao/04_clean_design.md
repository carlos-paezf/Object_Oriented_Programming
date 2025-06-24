---
sidebar_position: 4
---

# Diseño Limpio

## ¿Qué es el diseño limpio?

**Diseño limpio (Clean Design)** es una forma de estructurar el código para que sea:

1. Fácil de entender
2. Fácil de mantener
3. Fácil de extender sin romper lo existente

Se basa en principios de buena arquitectura, separación de responsabilidades y claridad del código. Fue popularizado por Robert C. Martin (Uncle Bob), quien propone que:

> *“Un buen diseño permite que el software cambie sin que duela.”*

## Objetivos del diseño limpio

1. Que cualquier desarrollador pueda leer y entender tu código rápidamente
2. Que el código sea modular y reutilizable
3. Que los cambios o nuevas funcionalidades no rompan otras partes del sistema
4. Que los errores sean fáciles de detectar y corregir
5. Que las pruebas unitarias sean más simples

> Escribir código limpio es un acto de empatía hacia tu yo del futuro y tu equipo.

## Fundamentos del diseño limpio

1. Separa responsabilidades
   - Cada clase debe tener **una única razón para cambiar** (principio SRP).
   - Ej: `StudentManager` gestiona lógica, `StudentRepository` accede a datos.
2. Evita acoplamientos fuertes
   - Usa interfaces para que una clase dependa de abstracciones, no de implementaciones (principio DIP).
3. Nombra con intención
   - Los nombres deben ser claros, descriptivos y sin abreviaciones vagas.
4. Aplica principios SOLID
   - Son la base del diseño limpio en programación orientada a objetos.
5. Organiza por capas o responsabilidad
   - Por ejemplo: dominio, aplicación, infraestructura, presentación.

## Ejemplo de estructura limpia

```txt
edu.usta.domain
├── model       → Clases puras del negocio (POJOs)
├── repository  → Interfaces como IPersonRepository

edu.usta.application
├── service     → Clases que orquestan el flujo (PersonService)

edu.usta.infrastructure
├── repository  → Implementaciones concretas (InMemory, JDBC)

edu.usta.ui
├── App.java    → Lógica de ejecución
```

Este enfoque **desacopla** la lógica de negocio de la tecnología que usamos para ejecutarla.s

> Imagina que haces un robot que debe saludar, moverse y cargar objetos. Si todo lo programas en una clase `RobotMega`, será difícil cambiarle el brazo sin dañar los pies. Pero si tienes: `Arm`, `Leg`, `Battery`, `SpeechModule`, cada parte es reemplazable, mantenible y testeable por separado.

## Diseño limpio no es solo para proyectos grandes

Aplicar diseño limpio desde proyectos pequeños:

- Te prepara para trabajar en sistemas reales.
- Evita la acumulación de código desordenado ("código espagueti").
- Mejora tu comprensión de cómo pensar en **modularidad** y **abstracción**.

## Buenas prácticas para empezar con diseño limpio

- Usa interfaces como contratos (`IStudentRepository`, `ICourseManager`)
- Mantén tus clases enfocadas: una tarea, una clase
- Usa nombres significativos y consistentes
- Separar los archivos sin miedo (¡mejor varios claros que uno confuso!)
- Comenta solo si es necesario, el código limpio se explica solo

El diseño limpio no se trata de seguir reglas estrictas, sino de **entender cómo organizar tu código para que otros puedan usarlo, cambiarlo y confiar en él**.

## Aplicaciones prácticas en proyectos

- En un sistema de gestión de estudiantes:
  - `StudentService` → lógica de negocio
  - `InMemoryStudentRepository` → datos simulados
  - `Student` → clase POJO
  - `IPersonRepository` → interfaz desacoplada
- En un videojuego:
  - `GameEngine`, `IControllable`, `Character`, `Enemy`, `WeaponService`

## Referencias

- Martin, R. C. (2017). Clean Architecture: A Craftsman's Guide to Software Structure and Design. Pearson.
- Martin, R. C. (2009). Clean Code: A Handbook of Agile Software Craftsmanship. Pearson.
- Jason Taylor. (2022). [Clean Architecture Template for ASP.NET](https://github.com/jasontaylordev/CleanArchitecture)
