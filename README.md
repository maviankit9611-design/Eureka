# Eureka Service Discovery

Service Discovery component for the Order Management Microservices application.

This service uses Netflix Eureka Server to allow microservices to register
themselves and discover other services dynamically.

## Architecture

```text
                    ┌──────────────────────┐
                    │   Eureka Server      │
                    │   Service Registry   │
                    └──────────┬───────────┘
                               │
                ┌──────────────┼──────────────┐
                │              │              │
                ▼              ▼              ▼
        ┌──────────────┐ ┌──────────────┐ ┌──────────────┐
        │ Order Service│ │Product       │ │ Notification │
        │              │ │Service       │ │Service       │
        └──────────────┘ └──────────────┘ └──────────────┘
