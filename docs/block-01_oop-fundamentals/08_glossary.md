---
sidebar_position: 8
---

# Glosario Bloque 01: Fundamentos de POO

## Sección 01 Parte 1: Conceptos Básicos

### Programación Orientada a Objetos (POO)

**Definición:** Paradigma de programación que modela el software como una colección de objetos que interactúan entre sí, cada uno con estado (atributos) y comportamiento (métodos).

**Ejemplo de uso:** En POO, un `Player` en un videojuego tiene atributos como `health` y métodos como `attack()`.

### Clase

**Definición:** Plantilla o molde que define un conjunto de atributos y métodos comunes a todos los objetos que se creen a partir de ella.

**Ejemplo de uso:** La clase `Car` define qué atributos y comportamientos tendrán todos los autos, como `startEngine()` o `model`.

### Objeto

**Definición:** Instancia concreta de una clase. Es una entidad con valores específicos para sus atributos y acceso a sus métodos.

**Ejemplo de uso:** `myCar = new Car("blue", "Toyota")` crea un objeto de la clase `Car`.

### Instancia

**Definición:** Representación específica de una clase cuando se crea un objeto a partir de ella.

**Ejemplo de uso:** Cada torta hecha con una receta es una instancia diferente de esa receta (clase).

### Atributo

**Definición:** Propiedad o característica de un objeto. Corresponde a una variable definida dentro de una clase.

**Ejemplo de uso:** En la clase `Person`, el atributo name almacena el nombre del individuo.

### Método

**Definición:** Comportamiento o función que puede realizar un objeto, definido dentro de su clase.

**Ejemplo de uso:** El método `greet()` en la clase `Person` permite al objeto decir su nombre y edad.

### Encapsulamiento

**Definición:** Principio que consiste en ocultar los detalles internos de los objetos y exponer solo lo necesario mediante métodos públicos.

**Ejemplo de uso:** La clase `Car` no permite acceso directo al atributo `engineOn`, sino que lo modifica mediante `start()` y `stop()`.

### Modularidad

**Definición:** Organización del código en módulos o componentes independientes y reutilizables que se comunican entre sí.

**Ejemplo de uso:** `CarService` gestiona la lógica de conducción sin modificar directamente la clase `Car`.

### Paradigma

**Definición:** Enfoque o estilo de programación. Puede ser estructurado, orientado a objetos, funcional, etc.

**Ejemplo de uso:** La POO es un paradigma que modela entidades reales como clases y objetos.

### Programación Estructurada

**Definición:** Paradigma de programación centrado en funciones y secuencia de instrucciones, sin clases ni objetos.

**Ejemplo de uso:** Un programa en C que calcula promedios mediante funciones sería estructurado, no orientado a objetos.

### Entidad (Entity)

**Definición:** En DDD (Domain-Driven Design), una clase que representa un concepto central del dominio, con identidad propia.

**Ejemplo de uso:** `Pet` es una entidad del sistema de registro de mascotas.

### Servicio (Service)

**Definición:** Clase que agrupa lógica de negocio que no pertenece directamente a una sola entidad.

**Ejemplo de uso:** `CarService` verifica si el motor está encendido antes de conducir el auto.

### Prueba Unitaria (Unit Test)

**Definición:** Código que verifica el comportamiento esperado de métodos o clases individuales.

**Ejemplo de uso:** En `CarTest`, se prueba que `start()` y `stop()` cambien correctamente el estado del motor.

### Abstracción

**Definición:** Representación simplificada de una entidad del mundo real, resaltando lo esencial y ocultando detalles innecesarios.

**Ejemplo de uso:** La clase `Student` modela un estudiante, sin entrar en detalles como su dirección física.

### Herencia

**Definición:** Mecanismo por el cual una clase puede adquirir atributos y métodos de otra clase.

**Ejemplo de uso (implícito):** Una clase `Dog` podría heredar de `Animal` en un sistema de mascotas.

### Composición

**Definición:** Relación entre clases donde una contiene una instancia de otra como parte de su definición.

**Ejemplo de uso (implícito):** La clase `Owner` puede tener una lista de objetos `Pet`.

### Polimorfismo

**Definición:** Capacidad de una misma operación de actuar de manera diferente según el objeto que la invoque.

**Ejemplo de uso (implícito):** Un método `printInfo()` puede comportarse distinto en `Book` y `Magazine`.

### Responsabilidad Única (SRP - Single Responsibility Principle)

**Definición:** Cada clase debe tener una única razón para cambiar, es decir, una responsabilidad única.

**Ejemplo de uso:** La clase `Person` solo gestiona datos de personas; `CarService` solo gestiona lógica de conducción.

### Open/Closed Principle (OCP)

**Definición:** Las clases deben estar abiertas a extensión pero cerradas a modificación.

**Ejemplo de uso:** Podemos extender `Car` con nuevos métodos sin cambiar su implementación original.

## Sección 01 Parte 2: Introducción a POO

### Clase Abstracta

**Definición:** Clase que no se puede instanciar directamente y que sirve como base para otras clases. Puede contener métodos abstractos (sin implementación) que deben ser sobreescritos por las subclases.

**Ejemplo de uso:** La clase `Animal` es abstracta y define el método `makeSound()` que será implementado por `Dog`, `Cat`, etc.

### Paquete (Package)

**Definición:** Mecanismo de organización del código fuente en Java que agrupa clases relacionadas dentro de un espacio de nombres común.

**Ejemplo de uso:** La clase `BankAccount` puede estar en el paquete `edu.usta.domain`, mientras que `BankAccountTest` en `edu.usta.test`.

### Jerarquía de Clases

**Definición:** Estructura en forma de árbol donde las clases se organizan por niveles de herencia, desde clases más generales (superclases) hasta más específicas (subclases).

**Ejemplo de uso:** `Vehicle` es la superclase de `Car`, `Bike` y `Truck` en un sistema de transporte.

### Principio de Sustitución de Liskov (Liskov Substitution Principle – LSP)

**Definición:** Principio SOLID que establece que los objetos de una subclase deben poder reemplazar a los de su superclase sin afectar el correcto funcionamiento del sistema.

**Ejemplo de uso:** Si `Dog` y `Cat` heredan de `Animal`, ambos deben comportarse correctamente al ser usados donde se espera un `Animal`.

### Principio de Segregación de Interfaces (Interface Segregation Principle – ISP)

**Definición:** Principio SOLID que sugiere que es mejor tener muchas interfaces específicas que una única interfaz general que obligue a implementar métodos innecesarios.

**Ejemplo de uso:** Es preferible tener una interfaz `Flyable` para animales que vuelan y `Swimmable` para los que nadan, en lugar de una interfaz `AnimalBehavior` con métodos que no todos usan.

### Patrón Template Method

**Definición:** Patrón de diseño en el que una clase abstracta define la estructura general de un algoritmo y permite que sus subclases implementen pasos específicos.

**Ejemplo de uso:** `Animal` define `makeSound()` como método abstracto, y cada subclase (`Dog`, `Cat`) proporciona su propio comportamiento.

### Patrón Strategy

**Definición:** Patrón de diseño que permite definir una familia de algoritmos, encapsularlos y hacerlos intercambiables sin modificar el código del cliente.

**Ejemplo de uso:** Si el comportamiento `makeSound()` se delega a clases como `BarkBehavior` o `MeowBehavior`, el sistema puede cambiar dinámicamente cómo suenan los animales.

## Sección 02: POJO y UML Básico

### POJO (Plain Old Java Object)

**Definición:** Objeto Java simple que no depende de frameworks ni librerías externas. Se usa para representar datos puros del dominio.

**Ejemplo de uso:** La clase `Book` es un POJO que contiene título, autor, año e ISBN sin lógica adicional.

### Setter y Getter

**Definición:** Métodos que permiten modificar (set) y acceder (get) a los atributos privados de una clase.

**Ejemplo de uso:** `getTitle()` devuelve el título del libro, y `setTitle("Nuevo título")` lo actualiza.

### toString()

**Definición:** Método de la clase Object en Java que retorna una representación en texto del objeto. Se puede sobreescribir para mostrar información personalizada.

**Ejemplo de uso:** `System.out.println(book)` imprimirá "Clean Code by Robert C. Martin (2008)" si `toString()` está sobreescrito.

### equals() y hashCode()

**Definición:** Métodos utilizados para comparar objetos y almacenarlos eficientemente en colecciones como HashMap o HashSet.

**Ejemplo de uso:** Se sobreescriben para que dos libros con el mismo ISBN sean considerados iguales.

### UML (Unified Modeling Language)

**Definición:** Lenguaje visual estandarizado para modelar sistemas orientados a objetos, incluyendo su estructura y comportamiento.

**Ejemplo de uso:** El diagrama de clases UML muestra las clases `Book`, `User` y `Loan` y sus relaciones.

### Diagrama de Clases

**Definición:** Tipo de diagrama UML que representa las clases de un sistema, sus atributos, métodos y relaciones (herencia, composición, agregación).

**Ejemplo de uso:** En el sistema de biblioteca, el diagrama de clases representa que `Loan` tiene relación de agregación con `Book` y `User`.

### Agregación (en UML)

**Definición:** Relación en la que una clase contiene referencias a otras como parte de su estructura, sin ser dueña exclusiva de ellas.

**Ejemplo de uso:** `Loan o-- Book` indica que un préstamo se asocia a un libro, pero el libro puede existir sin el préstamo.

### PlantUML

**Definición:** Herramienta que permite generar diagramas UML usando código textual.

**Ejemplo de uso:** Con PlantUML se puede escribir `class Book { +getTitle(): String }` para generar un diagrama de clase.

### Value Object (Patrón de Diseño)

**Definición:** Objeto que representa datos sin identidad propia, usado para transportar información.

**Ejemplo de uso:** `Book` es un value object si solo interesa su contenido (título, autor...) y no su identidad única.

### LocalDate (Java)

**Definición:** Clase de Java (`java.time`) que representa una fecha sin hora.

**Ejemplo de uso:** El atributo date en la clase `Loan` es de tipo `LocalDate`.

## Sección Bonus: Unit Testing con JUnit para JDK 21+

### JUnit 5

**Definición:** Framework moderno y modular para ejecutar pruebas unitarias en Java. Incluye API, plataforma de ejecución y soporte para versiones anteriores.

**Ejemplo de uso:** Usamos `@Test` de JUnit 5 para verificar que el método `add()` funcione correctamente.

### JUnit Jupiter

**Definición:** Módulo principal de JUnit 5 que proporciona la API de pruebas moderna, anotaciones como `@Test` y utilidades para aserciones.

**Ejemplo de uso:** `JUnit Jupiter` permite usar `assertEquals()` y `assertThrows()` para validar resultados esperados.

### JUnit Platform

**Definición:** Componente base de JUnit 5 encargado de lanzar y administrar las ejecuciones de pruebas en distintos entornos.

**Ejemplo de uso:** Herramientas como Maven o IntelliJ usan la JUnit Platform para correr pruebas desde la línea de comandos o el IDE.

### JUnit Vintage

**Definición:** Módulo de JUnit 5 que permite ejecutar pruebas escritas con JUnit 3 y 4.

**Ejemplo de uso:** Un proyecto antiguo puede seguir usando pruebas clásicas si se añade JUnit Vintage.

### Apache Maven

**Definición:** Herramienta de automatización y gestión de proyectos Java, que facilita la compilación, testing, empaquetado y dependencia de librerías.

**Ejemplo de uso:** Usamos Maven para compilar el proyecto con `mvn compile` y ejecutar pruebas con `mvn test`.

### pom.xml

**Definición:** Archivo de configuración central de un proyecto Maven. Define las dependencias, plugins y propiedades del proyecto.

**Ejemplo de uso:** Añadir la dependencia de junit-jupiter en el `pom.xml` permite usar JUnit 5 en el proyecto.

### exec-maven-plugin

**Definición:** Plugin de Maven que permite ejecutar clases Java directamente desde la línea de comandos.

**Ejemplo de uso:** Se configura este plugin en el `pom.xml` para ejecutar `App.java` con `mvn exec:java`.

### Aserción

**Definición:** Expresión lógica en un test que valida que una salida sea igual a lo esperado. Si falla, la prueba se considera incorrecta.

**Ejemplo de uso:** `assertEquals(5, calc.add(2, 3))` comprueba que la suma da el resultado esperado.

### @BeforeEach, @AfterEach, @BeforeAll, @AfterAll

**Definición:** Anotaciones de JUnit 5 que permiten ejecutar métodos auxiliares antes o después de una o todas las pruebas.

**Ejemplo de uso:** `@BeforeEach` prepara el entorno antes de cada test, como instanciar una clase.

### Maven Surefire Plugin

**Definición:** Plugin que permite ejecutar pruebas unitarias automáticamente al compilar el proyecto con Maven.

**Ejemplo de uso:** Las pruebas en `CalculatorTest.java` se ejecutan con mvn test gracias a `maven-surefire-plugin`.

### assertThrows()

**Definición:** Método de JUnit 5 que verifica que una excepción específica sea lanzada al ejecutar cierto código.

**Ejemplo de uso:** `assertThrows(IllegalArgumentException.class, () -> calc.divide(5, 0))` asegura que se lanza una excepción al dividir por cero.

## Sección 03: Constructores, Getters y Setters, toString

### Constructor

**Definición:** Método especial que se ejecuta automáticamente al crear un objeto con new. Se usa para inicializar atributos y definir el estado inicial de la instancia.

**Ejemplo de uso:** `Student s = new Student("Ana", "S001", 4.5);` crea un estudiante con datos iniciales.

### Constructor Implícito

**Definición:** Constructor sin parámetros que Java crea automáticamente si la clase no define uno explícitamente.

**Ejemplo de uso:** Si `Book` no define constructores, Java añade `public Book() {}` por defecto.

### Constructor Vacío

**Definición:** Constructor definido manualmente sin parámetros, que permite crear objetos sin inicializar atributos de inmediato.

**Ejemplo de uso:** `new Product()` usa el constructor vacío para luego usar setters.

### Constructor con Parámetros

**Definición:** Constructor que recibe argumentos para inicializar directamente los atributos del objeto.

**Ejemplo de uso:** `new Product("Mouse", "P001", 29.99, 10);` crea un objeto con datos definidos desde el inicio.

### Sobrecarga de Constructores (Constructor Overloading)

**Definición:** Definir múltiples constructores en la misma clase con diferentes listas de parámetros, permitiendo formas flexibles de instanciación.

**Ejemplo de uso:** `Book` puede tener constructores con 0, 1 o 2 parámetros para mayor versatilidad.

### Acceso Controlado

**Definición:** Principio del encapsulamiento en el que se accede a los atributos de una clase solo mediante métodos públicos (getters y setters).

**Ejemplo de uso:** `student.setGpa(4.5)` aplica validación antes de modificar el atributo.

### Formato uniforme en toString()

**Definición:** Técnica recomendada para mostrar el estado del objeto en texto con una estructura clara y consistente.

**Ejemplo de uso:** `"Student{name='Ana', id='S001', gpa=4.2}"` es un formato legible para depuración y registros.

## Sección 04: Enums, String, StringBuffer y StringBuilder

### enum (Enumeración)

**Definición:** Tipo especial de clase que define un conjunto fijo de constantes con nombre. Ideal para representar estados, categorías o roles inmutables.

**Ejemplo de uso:** `UserStatus status = UserStatus.ACTIVE`; define el estado de un usuario con un valor seguro y validado.

### ordinal()

**Definición:** Método de enum que devuelve la posición (índice) de una constante dentro de la enumeración, comenzando desde 0.

**Ejemplo de uso:** `Priority.HIGH.ordinal()` devuelve 0.

### valueOf(String)

**Definición:** Método de enum que convierte una cadena de texto al valor correspondiente de la enumeración.

**Ejemplo de uso:** `UserStatus.valueOf("SUSPENDED")` devuelve `UserStatus.SUSPENDED`.

### StringBuffer

**Definición:** Clase mutable y sincronizada para manipulación eficiente de texto en entornos multihilo. Pertenece a `java.lang`.

**Ejemplo de uso:** `sb.append(" nuevo texto");` modifica el contenido sin crear un nuevo objeto.

### StringBuilder

**Definición:** Versión no sincronizada de StringBuffer, más rápida para uso en un solo hilo. También mutable.

**Ejemplo de uso:** `new StringBuilder("Hola").append(" mundo")` concatena cadenas de forma eficiente.

### reverse()

**Definición:** Método que invierte el contenido de un StringBuffer o StringBuilder.

**Ejemplo de uso:** `"Java"` se convierte en `"avaJ"` con `reverse()`.

### capacity()

**Definición:** Método que retorna la capacidad interna (en caracteres) del buffer de un StringBuilder o StringBuffer, no confundir con `length()`.

**Ejemplo de uso:** `new StringBuilder().capacity()` devuelve 16 por defecto.

### CharSequence

**Definición:** Interfaz que representa una secuencia legible de caracteres. String, StringBuffer y StringBuilder la implementan.

**Ejemplo de uso:** Métodos que aceptan `CharSequence` pueden recibir cualquiera de esas tres clases.

### Thread-safe

**Definición:** Propiedad que indica que una clase o método puede ser usado de forma segura en contextos de múltiples hilos simultáneamente.

**Ejemplo de uso:** StringBuffer es thread-safe, mientras que StringBuilder no lo es.

### String Pool

**Definición:** Área especial de memoria donde Java almacena internamente literales de cadenas para optimizar uso de memoria y evitar duplicados.

**Ejemplo de uso:** `String a = "hola"; String b = "hola";` → ambas referencias apuntan al mismo objeto del pool.

### Comparación por contenido (equals())

**Definición:** Método que compara el contenido de dos objetos String.

**Ejemplo de uso:** `"Java".equals("Java")` → true, mientras que `"Java" == "Java"` compara referencias, no contenido.

### Benchmark

**Definición:** Prueba de rendimiento que mide el tiempo de ejecución de fragmentos de código para comparar eficiencia.

**Ejemplo de uso:** Se comparan String, StringBuffer y StringBuilder para concatenar 100,000 caracteres.
