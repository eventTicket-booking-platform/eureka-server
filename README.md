# Eureka Server

Service discovery server for Event Hub. Backend services register here so the platform can track running service instances.

## Stack

- Java 17
- Spring Boot 3
- Netflix Eureka Server

## Responsibilities

- Maintain the service registry
- Accept service registrations from backend services
- Expose registry and dashboard views

## Non-Functional Requirements

- Fast local development startup
- Shared registry for all Spring services
- Low-friction discovery across services

## Common Endpoints

- `GET /`
- `GET /eureka`

## Local Setup

Run:

```powershell
.\mvnw.cmd spring-boot:run
```

Default port: `8761`

## Build

```powershell
.\mvnw.cmd clean package
```

## Notes

- The current local config sets `fetch-registry=false` and disables self-preservation for quicker local feedback.
