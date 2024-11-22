
# Eureka Server

Este proyecto es un **Eureka Server** que actúa como un registro de servicios para la arquitectura basada en microservicios. Los clientes pueden registrarse y descubrir otros servicios dentro del ecosistema.

## 📋 Requisitos previos

Asegúrate de tener instalados los siguientes elementos:

- **Java 21** (o superior).
- **Gradle** (versión 7.6 o superior).
- Un IDE compatible con Spring Boot (por ejemplo, IntelliJ IDEA o STS).
- Conexión a Internet para descargar las dependencias.

## 🚀 Configuración y ejecución

### 1. Clonar el repositorio

```bash
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_PROYECTO>
```

### 2. Compilar el proyecto

Ejecuta el siguiente comando para compilar el proyecto y verificar las dependencias:

```bash
./gradlew clean build
```

### 3. Ejecutar el servidor

Puedes iniciar el Eureka Server con el siguiente comando:

```bash
./gradlew bootRun
```

Por defecto, el servidor estará disponible en [http://localhost:8761](http://localhost:8761).

### 4. Configuración del cliente Eureka

Para registrar un cliente en el Eureka Server, configura las propiedades de tu aplicación cliente en el archivo `application.yml`:

```yaml
eureka:
  client:
    service-url:
      defaultZone: http://localhost:8761/eureka/
```

## 📂 Estructura del proyecto

- **`src/main/java`**: Código fuente principal.
- **`src/main/resources/application.yml`**: Archivo de configuración para el Eureka Server.
- **`build.gradle`**: Archivo de configuración de Gradle.
- **`README.md`**: Documentación del proyecto.

## 🛠 Tecnologías utilizadas

- **Java 21**
- **Spring Boot 3.2**
- **Spring Cloud 2023.0**
- **Gradle**

## 🌐 Configuración de Eureka Server

El archivo `application.yml` incluye los parámetros básicos para configurar el servidor:

```yaml
server:
  port: 8761

eureka:
  client:
    register-with-eureka: false
    fetch-registry: false
  instance:
    hostname: localhost

spring:
  application:
    name: eureka-server
```

## 📖 Referencias

- [Documentación oficial de Spring Cloud Netflix](https://spring.io/projects/spring-cloud-netflix)
- [Documentación de Gradle](https://docs.gradle.org/)
- [Java 21 Features](https://openjdk.org/projects/jdk/21/)

## 👤 Autor

- **David**  
  Desarrollador Backend y Fullstack.  
  ¡Siempre dispuesto a aprender y mejorar proyectos en microservicios!
