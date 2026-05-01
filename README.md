# Nova Gateway Service

API Gateway para la arquitectura de microservicios de Nova, encargado de centralizar y enrutar las peticiones a los diferentes servicios del ecosistema.

## Tecnologías y Versiones

- **Java:** 17
- **Spring Boot:** 3.4.3
- **Spring Cloud:** 2024.0.0
- **Dependencias Principales:**
    - `spring-cloud-starter-gateway`: Motor del Gateway.
    - `spring-boot-starter-webflux`: Entorno reactivo para el manejo de peticiones.
    - `spring-boot-starter-actuator`: Monitoreo y métricas.

## Requisitos de Conectividad

Para que el Gateway funcione correctamente, los siguientes servicios deben estar en ejecución:

- **Customer Service:** `http://localhost:8082`
- **Order Service:** `http://localhost:8083`
- **Order Management Service:** `http://localhost:8084`

El Gateway se ejecuta por defecto en el puerto **8085**.

## Ejecución en Local

Para ejecutar la aplicación localmente usando el Maven Wrapper incluido:

```bash
./mvnw spring-boot:run
```

O si tienes Maven instalado globalmente:

```bash
mvn spring-boot:run
```

## Ejecución con Docker

Si prefieres usar Docker para ejecutar todo el ecosistema de servicios, se recomienda utilizar el repositorio de infraestructura:

🔗 [infra-docker-services-nova](https://github.com/perez182/infra-docker-services-nova)

Este repositorio incluye un `docker-compose.yml` que levanta todos los servicios, incluido este Gateway, configurados para comunicarse entre sí dentro de la red de Docker.
