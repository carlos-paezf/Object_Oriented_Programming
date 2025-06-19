---
sidebar_position: 1
---

# Git y Github para estudiantes de Ingeniería

**Git** y **GitHub** son herramientas indispensables en el **mundo real del desarrollo de software**. Te permiten:

- Llevar el control de versiones de tu código
- Trabajar en equipo sin sobrescribir cambios
- Registrar tu progreso y retroceder cuando sea necesario
- Construir un portafolio profesional visible para empresas y comunidades

> Usar Git es como tener un historial inteligente de todo lo que haces en tu código. GitHub es como una nube social donde compartes ese historial.

## ¿Qué es Git?

Git es un sistema de control de versiones que se usa **desde tu computador**. Sirve para:

- Guardar cada cambio importante que haces
- Volver a versiones anteriores
- Comparar y fusionar cambios
- Trabajar en ramas sin afectar el código principal

## ¿Qué es GitHub?

GitHub es una plataforma en línea donde puedes **subir tus proyectos Git**. También permite:

- Mostrar tu código públicamente o de forma privada
- Colaborar con otras personas en un mismo proyecto
- Usar tableros, issues, wikis y GitHub Actions

## Configuración inicial (una sola vez)

1. Instala [Git](https://git-scm.com/)
2. Abre tu terminal o Git Bash y ejecuta:

   ```bash
   git config --global user.name "Tu nombre"
   git config --global user.email "tu.correo@ejemplo.com"
   ```

3. Abriendo una terminal en el directorio de tu proyecto puedes iniciar git (crear un repositorio local) con el siguiente comando:

   ```bash
   git init
   ```

## Comandos básicos

|Acción|Comando|
|--|--|
|Ver estado actual|`git status`|
|Agregar archivos al repositorio local|`git add .` o `git add nombreArchivo.java`|
|Confirmar cambios|`git commit -m "Mensaje claro del cambio"`|
|Ver historial|`git log`|

## Subir a GitHub (por primera vez en cada proyecto)

1. Crea un repositorio en [GitHib](https://github.com/)
2. En la terminal de tu proyecto ejecuta:

   ```bash
   git remote add origin https://github.com/usuario/repositorio.git
   git branch -M main
   git push -u origin main
   ```

## Ciclo de trabajo habitual

Cada que hagas cambios en tu proyecto debes seguir estos pasos básicos en la terminal de trabajo:

```bash
git add .
git commit -m "Mensaje claro del cambio"
git push
```

## Buenas prácticas

- Usa mensajes de commit claros (ej. `Agrega clase Course con enum`)
- Guarda tus cambios con frecuencia
- No subas archivos innecesarios (usa `.gitignore`)
- Haz `pull` antes de trabajar si estás en grupo
- Escribe tu nombre completo en tu perfil de GitHub y sube tus proyectos al portafolio

## ¿Por qué colaborar con Git y GitHub?

Git y GitHub permiten que **varios estudiantes trabajen en el mismo proyecto sin pisarse el trabajo**. Ayudan a:

- Dividir tareas por archivos o funcionalidades
- Controlar quién hizo qué y cuándo
- Resolver conflictos de forma controlada
- Aprender flujos de trabajo reales usados en la industria

> “Trabajar en grupo sin Git es como escribir un ensayo a varias manos... ¡usando el mismo cuaderno!”

## Flujo de trabajo recomendado para equipos

### Asignación de Roles en el equipo (mínimo 2)

1. **Líder de repositorio (owner):** crea y configura el repositorio
2. **Colaboradores:** contribuyen con funcionalidades específicas

### Paso a paso para trabajar en equipo

1. El líder crea el repositorio:
   1. Entra a [GitHib](https://github.com/)
   2. Crea un nuevo repositorio (ejemplo: "poo-intersemestral")
   3. Marca "Público" o "Privado", según la necesidad o preferencia
2. Agrega colaboradores:
   1. En el repositorio creado en Github, ve a las pestaña **Settings** y la sección **Collaborators**.
   2. Escribe el nombre de usuario GitHub de tu compañero y dale acceso.
3. Todos clonan el repositorio:
   1. Cada miembro del equipo debe clonar el proyecto a su equipo local:

   ```bash
   git clone https://github.com/usuario/repositorio.git
   cd repositorio
   ```

4. Crear una rama por persona o por funcionalidad:

   ```bash
   git checkout -b nombre-rama
   ```

   Ejemplos:

   - `git checkout -b dev`
   - `git checkout -b prod`
   - `git checkout -b new-features`

   :::danger
   ¡Nunca trabajes directamente sobre la rama `main`!
   :::

5. Trabaja en tu rama, guarda y sube a la nube:

   ```bash
   git add .
   git commit -m "Agrega clase Student con getters/setters"
   git push origin nombre-rama
   ```

6. Abre un Pull Request (PR):

   Desde tu proyecto en GitHub:

   1. Haz click en **Compare & Pull Request**
   2. Escribe un título y descripción claros
   3. Espera revisión o aprobación del líder de equipo

7. Revisa y fusiona ramas:

   El líder o cualquier colaborador puede revisar los cambios y hacer clic en **Merge Pull Request** cuando esté listo.

   > Git detectará automáticamente si hay conflictos. Si los hay, deben resolverse localmente antes de fusionar.

## Buenas prácticas colaborativas

- Usa **nombres de rama claros** (una tarea = una rama)
- Haz **commits frecuentes** y con mensajes descriptivos
- Siempre haz `pull` antes de comenzar a trabajar:
  
  ```bash
  git checkout main
  git pull origin main
  ```

- No subas archivos de compilación (`.class`, `.DS_Store`, etc.)
- Usa `.gitignore` correctamente
- Comunícate con tu equipo por WhatsApp, Discord o GitHub Issues

## Recursos recomendados

- [GitHub Student Pack](https://education.github.com/pack) — ¡Herramientas premium gratuitas para estudiantes!
- [Pro Git](https://git-scm.com/book/es/v2) (libro completo)
- [GitHub Docs](https://docs.github.com/es)
- [Git Visualizer](http://git-school.github.io/visualizing-git/) (para entender ramas)
- [Git Branching (interactivo)](https://learngitbranching.js.org/?locale=es_ES)
