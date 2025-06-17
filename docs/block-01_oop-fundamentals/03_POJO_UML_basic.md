---
sidebar_position: 3
---

# POJO y UML Básico

## ¿Qué es un POJO?

**POJO (Plain Old Java Object)** es un objeto Java **sencillo y autónomo** que no depende de ninguna tecnología, framework o API externa (como Spring, Hibernate, etc.). Es la forma más limpia y pura de representar una **entidad del dominio**.

Características de un POJO:

- Tiene atributos privados.
- Posee constructores, setters y getters.
- Puede implementar `toString()`, `equals()` y `hashCode()`.
- No extiende de clases específicas ni implementa interfaces no necesarias.

**Ejemplo real:** Representar un libro (`Book`) solo con su título, autor, año y código ISBN.

## ¿Qué es UML?

**UML (Unified Modeling Language)** es un lenguaje gráfico que permite **modelar sistemas orientados a objetos**. El diagrama de clases UML representa:

- Clases
- Atributos
- Métodos
- Relaciones (asociación, herencia, composición, etc.)

**Símbolos básicos:**

- `+` público
- `-` privado
- `#` protegido
- `~` estático
- `*` multiplicidad (número de instancias)
