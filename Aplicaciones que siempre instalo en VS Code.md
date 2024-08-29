# Aplicaciones que siempre instalo en VS Code

Este documento sirve como recordatorio de las aplicaciones esenciales que instalo en Visual Studio Code y el propósito de cada una.

## 1. Insomnia

**Descripción:** Insomnia es una poderosa aplicación cliente para realizar pruebas de API REST.

**Uso:**

- Enviar solicitudes HTTP (GET, POST, PUT, DELETE, etc.) a APIs.
- Organizar y guardar solicitudes para su reutilización.
- Visualizar y manipular respuestas de API fácilmente.
- Crear y gestionar entornos para diferentes configuraciones de API.

**Por qué la instalo:** Insomnia simplifica enormemente el proceso de prueba y depuración de APIs, lo que es crucial en el desarrollo de aplicaciones modernas que dependen de servicios web.

## 2. Postman

**Descripción:** Postman es otra herramienta popular para el desarrollo y prueba de APIs.

**Uso:**

- Crear y enviar solicitudes HTTP a APIs.
- Automatizar pruebas de API.
- Generar documentación de API.
- Colaborar en equipo compartiendo colecciones de API.

**Por qué la instalo:** Aunque similar a Insomnia, Postman ofrece características adicionales como pruebas automatizadas y herramientas de colaboración que son útiles en proyectos más grandes o en equipos.

## 3. Yarn

**Descripción:** Yarn es un gestor de paquetes para JavaScript, alternativo a npm.

**Uso:**

- Instalar y gestionar dependencias de proyectos JavaScript.
- Ejecutar scripts definidos en el archivo `package.json`.
- Gestionar versiones de paquetes de manera más eficiente.

**Por qué la instalo:** Yarn ofrece una mayor velocidad y confiabilidad en la instalación de paquetes comparado con npm. También proporciona un bloqueo de versiones más preciso, lo que ayuda a mantener la consistencia entre diferentes entornos de desarrollo.

Claro, te ayudaré a instalar Yarn en tu Mac. Primero, vamos a crear un documento con las aplicaciones que sueles instalar, incluyendo Yarn, y luego te guiaré para instalar Yarn específicamente.

# Aplicaciones que siempre instalo

Este documento sirve como recordatorio de las aplicaciones que habitualmente instalo en mi entorno de desarrollo, junto con una breve descripción de su utilidad.

## 1. Insomnia

**Descripción:** Insomnia es una poderosa herramienta de cliente HTTP y GraphQL. Es útil para probar, depurar y diseñar APIs.

**Uso principal:**

- Realizar solicitudes HTTP (GET, POST, PUT, DELETE, etc.) a APIs
- Organizar y guardar solicitudes para su reutilización
- Probar y depurar APIs GraphQL
- Generar documentación de API

## 2. Postman

**Descripción:** Postman es otra popular herramienta de colaboración para el desarrollo de API. Ofrece funcionalidades similares a Insomnia, pero con algunas características adicionales.

**Uso principal:**

- Diseñar, probar y documentar APIs
- Colaborar en equipo en el desarrollo de APIs
- Automatizar pruebas de API
- Monitorear el rendimiento de las APIs

## 3. Yarn

**Descripción:** Yarn es un gestor de paquetes para JavaScript, alternativo a npm (Node Package Manager). Es conocido por su velocidad y seguridad.

**Uso principal:**

- Instalar y gestionar dependencias de proyectos JavaScript
- Garantizar que las instalaciones sean consistentes en diferentes sistemas
- Mejorar la velocidad de instalación de paquetes
- Proporcionar comandos adicionales útiles para el desarrollo

# Instalar Yarn en tu Mac. Aquí tienes los pasos a seguir:

1. Primero, asegúrate de tener Homebrew instalado. Si no lo tienes, puedes instalarlo ejecutando este comando en la Terminal:

   ```
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. Una vez que tengas Homebrew, puedes instalar Yarn fácilmente con el siguiente comando:

   ```
   brew install yarn
   ```

3. Espera a que la instalación se complete. Homebrew descargará e instalará Yarn y todas sus dependencias.

4. Para verificar que Yarn se ha instalado correctamente, puedes ejecutar:

   ```
   yarn --version
   ```

   Esto debería mostrar la versión de Yarn que has instalado.

5. Si quieres usar Yarn sin Node.js, puedes instalarlo sin dependencias usando:

   ```
   brew install yarn --ignore-dependencies
   ```

Y eso es todo. Ahora tienes Yarn instalado en tu Mac y puedes empezar a usarlo en tus proyectos JavaScript.
