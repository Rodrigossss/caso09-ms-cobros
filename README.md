# Microservicio Cobros - Caso 09 (EP1 DevOps)

Microservicio encargado de la gestión de cobros, implementado con **Java**, **Spring Boot**, **Docker** y un pipeline de automatización CI/CD con **GitHub Actions**.

##  Tecnologías Utilizadas

* **Lenguaje:** Java 17
* **Framework:** Spring Boot
* **Gestor de dependencias:** Maven
* **Contenedorización:** Docker
* **CI/CD:** GitHub Actions
* **Control de Versiones:** Git & GitHub (Metodología GitFlow)

##  Estrategia de Ramificación (GitFlow)

El repositorio sigue la estructura estándar de GitFlow:
* `main`: Contiene el código de producción listo para despliegue.
* `develop`: Rama principal de integración para desarrollo.
* `feature/*`: Ramas para el desarrollo de nuevas características.
* `hotfix/*`: Ramas para correcciones críticas en producción.

##  Pipeline de Integración Continua (CI/CD)

El workflow se activa automáticamente ante:
* `push` en la rama `develop`.
* `pull_request` con destino a la rama `main`.

**Pasos del Pipeline (`.github/workflows/ci-cd.yml`):**
1. Checkout del código fuente.
2. Configuración de Java JDK 17 (Temurin).
3. Compilación y ejecución de pruebas unitarias (`mvn clean test`).
4. Construcción de la imagen Docker de prueba.

##  Instalación y Ejecución Local

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/Rodrigossss/caso09-ms-cobros.git](https://github.com/Rodrigossss/caso09-ms-cobros.git)
   cd caso09-ms-cobros

