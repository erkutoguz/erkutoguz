# Erkut Oğuz

**Junior Backend Engineer**

I build backend systems with Java and Spring Boot, mostly event-driven services on PostgreSQL and Kafka. I also write systems code in C to understand what happens below the frameworks.

---

## Projects

### [Event-Driven E-Commerce Backend](https://github.com/erkutoguz/ecommerce)
`Java 21` `Spring Boot` `PostgreSQL` `Kafka` `Elasticsearch` `Docker Compose` `Testcontainers`

- Eight Spring Boot services behind an API gateway, each with its own PostgreSQL database (Flyway migrations).
- Order flow as an orchestrated Saga with compensation (payment expiry, out-of-stock).
- Transactional Outbox and consumer Inbox for at-least-once delivery, with idempotent consumers and dead-letter topics.
- Outbox rows claimed with `FOR UPDATE SKIP LOCKED` so several instances can publish safely; optimistic locking on carts, stock and Saga state.
- Stripe Checkout with idempotency keys and signed webhooks; JWT authentication and RBAC.
- Integration tests on real PostgreSQL and Kafka via Testcontainers.
- Prometheus metrics and OpenTelemetry tracing were implemented with AI assistance.

### [RouteMesh: Logistics & Payment Settlement Platform](https://github.com/erkutoguz/routemesh)
`Java 21` `Spring Boot` `gRPC` `Kafka` `Debezium` `Temporal` `PostgreSQL/PostGIS` `Redis`

> I designed the architecture and made all technical decisions; the code was implemented with AI coding agents under my review.

- Twelve services: gRPC inside, REST outside.
- Debezium-based outbox and Temporal workflows for the shipment lifecycle.
- Redis lock with fencing tokens so only one courier is assigned to a shipment.
- Append-only double-entry ledger with reconciliation against a simulated payment provider.

### [ErktDB](https://github.com/erkutoguz/erktdb)
`C` `Linux` `epoll` `TCP sockets`

Key-value store written from scratch in C: non-blocking TCP server with `epoll`, custom binary protocol, master–worker replication and disk persistence.

### [ErktVM](https://github.com/erkutoguz/erktvm)
`C`

LC-3 (16-bit) virtual machine: fetch–decode–execute loop, 16 opcodes, memory-mapped I/O.

[### [FindAway](https://github.com/erkutoguz/findaway)
`C` `Raylib`

Grid-based pathfinding visualiser: A* and Dijkstra with a hand-written binary min-heap.]

---

## Tech

- **Languages:** Java, C, SQL
- **Backend:** Spring Boot, Spring Security, Spring Data JPA/Hibernate, REST, gRPC, JWT, RBAC, Maven
- **Data & messaging:** PostgreSQL, Flyway, Kafka, Redis, Elasticsearch, Temporal, Debezium (CDC), PostGIS, Kafka Streams
- **Testing & DevOps:** JUnit, Testcontainers, Docker Compose, GitHub Actions, Git, Linux
- **Observability:** Prometheus, Grafana, OpenTelemetry

---

## Contact

- LinkedIn: https://www.linkedin.com/in/erkut-oguz/
- Email: erkutoguz.eo@gmail.com
