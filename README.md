# Object Oriented Programming (OOP)

[![wakatime](https://wakatime.com/badge/user/8ef73281-6d0a-4758-af11-fd880ca3009c/project/978c66b7-aedf-4b4c-a4ee-6197b6ef815e.svg?style=for-the-badge)](https://wakatime.com/badge/user/8ef73281-6d0a-4758-af11-fd880ca3009c/project/978c66b7-aedf-4b4c-a4ee-6197b6ef815e)

> 🌟 *El conocimiento no es útil si no se comparte.*

Este proyecto es una plataforma de documentación educativa desarrollada con [Docusaurus](https://docusaurus.io/).

## Objetivo

Brindar tanto a estudiantes cómo docentes, un recurso descentralizado, estructurado y multilingüe, que facilite el acceso a los siguientes temas:

- Bloque 01: Fundamentos de Programación Orientada a Objetos
  - Conceptos Básicos
  - Introducción a la Programación Orientada a Objetos
  - POJO y UML Básico
  - Unit Testing con JUnit para JDK 21+ (Bonus)
  - Constructores, Getters y Setters, toString
  - Enums, String, StringBuffer y StringBuilder
- Bloque 02: Interfaces, mapeo y patron DAO
  - Git y Github para estudiantes de Ingeniería (Bonus)
  - Mapeo y Creación de Objetos

## Internacionalización

El portal estará disponible en 2 idiomas:

- 🇪🇸 Español (predeterminado)
- 🇺🇸 Inglés

Puedes cambiar el idioma desde el menú superior del sitio.

## Instalación local

Para trabajar en el sitio de documentación de forma local:

```bash
# Clona el repositorio
git clone https://github.com/carlos-paezf/Object_Oriented_Programming_Intersemester.git
cd Object_Oriented_Programming_Intersemester

# Instala las dependencias
npm install

# Inicia el servidor de desarrollo
npm run start
```

Abre <http://localhost:3000> en tu navegador.

## Estructura del proyecto

- `/docs` Contenidos originales en español
- `/i18n/en` Traducciones al inglés
- `src` Componentes y páginas personalizadas
- `/static` Archivos estáticos (imágenes, descargas, etc.)

## Contribuciones

Este proyecto está abierto a docentes o estudiantes que deseen colaborar con:

- Traducciones
- Correcciones ortográficas o técnicas
- Mejora en la organización o visualización de los contenidos

Por favor, antes de hacer un Pull Request, revisa el archivo [`CONTRIBUTING.md`](./CONTRIBUTING.md)

## Comandos útiles

|Acción|Comando|
|--|--|
|Ejecutar en modo desarrollo|`npm run start`|
|Compilar para producción|`npm run build`|
|Generar estructura para traducciones|`npm run write-translations`|

## Autor

Proyecto desarrollado por Carlos David Páez Ferreira, Ingeniero de Sistemas y Docente Universitario, como recurso de apoyo para estudiantes y colegas.

## Licencia

Este proyecto está licenciado bajo la MIT License.
