# Microservicio Cobros - Caso 09 (EP1 DevOps)

Microservicio encargado de la gestion de cobros, implementado con Java, Spring Boot, Docker y un pipeline de automatizacion CI/CD con GitHub Actions.

## Tecnologias Utilizadas

* Lenguaje: Java 17
* Framework: Spring Boot
* Gestor de dependencias: Maven
* Contenedorizacion: Docker
* CI/CD: GitHub Actions
* Control de Versiones: Git & GitHub (Metodologia GitFlow)

## Estrategia de Ramificacion (GitFlow)

El repositorio sigue la estructura estandar de GitFlow:
* main: Contiene el codigo de produccion listo para despliegue.
* develop: Rama principal de integracion para desarrollo.
* feature/*: Ramas para el desarrollo de nuevas caracteristicas.
* hotfix/*: Ramas para correcciones criticas en produccion.

## Pipeline de Integracion Continua (CI/CD)

El workflow se activa automaticamente ante:
* push en la rama develop.
* pull_request con destino a la rama main.

Pasos del Pipeline (.github/workflows/ci-cd.yml):
1. Checkout del codigo fuente.
2. Configuracion de Java JDK 17 (Temurin).
3. Compilacion y ejecucion de pruebas unitarias (mvn clean test).
4. Construccion de la imagen Docker de prueba.

## Instalacion y Ejecucion Local

1. Clonar el repositorio:
   git clone https://github.com/Rodrigossss/caso09-ms-cobros.git
   cd caso09-ms-cobros

2. Construir la imagen Docker:
   docker build -t ms-cobros:latest .