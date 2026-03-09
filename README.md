# Docker Templates

![Docker](https://img.shields.io/badge/docker-ready-blue)
![License](https://img.shields.io/badge/license-MIT-green)

Reusable Dockerfiles, Docker Compose templates, and multi-service stacks for backend development.

This repository provides ready-to-use container templates for common backend infrastructure and application environments.

---

# Repository Structure

```
docker-templates
├─ dockerfiles
│  ├─ springboot
│  ├─ node
│  ├─ python
│  └─ fastapi
│
├─ compose
│  ├─ mysql
│  ├─ postgres
│  ├─ redis
│  ├─ nginx
│  ├─ kafka
│  ├─ elasticsearch
│  ├─ prometheus
│  └─ grafana
│
└─ stacks
   ├─ spring-mysql
   ├─ spring-mysql-redis
   ├─ monitoring
   └─ spring-monitoring
```

---

# Dockerfiles

Application container templates.

| Stack | Description |
|------|-------------|
| Spring Boot | Java Spring Boot container |
| Node.js | Node backend container |
| Python | Generic Python container |
| FastAPI | FastAPI application container |

Example:

```bash
docker build -t my-app ./dockerfiles/springboot
```

---

# Compose Templates

Single-service infrastructure templates.

| Service | Description |
|-------|-------------|
| MySQL | Relational database |
| PostgreSQL | Alternative relational database |
| Redis | In-memory cache |
| Nginx | Reverse proxy / static server |
| Kafka | Event streaming platform |
| Elasticsearch | Search engine |
| Prometheus | Metrics collection |
| Grafana | Monitoring dashboards |

Example:

```bash
cd compose/redis
docker compose up -d
```

---

# Stacks

Multi-service development environments.

| Stack | Description |
|------|-------------|
| spring-mysql | Spring Boot + MySQL |
| spring-mysql-redis | Spring Boot + MySQL + Redis |
| monitoring | Prometheus + Grafana |
| spring-monitoring | Spring Boot + Prometheus + Grafana |

Example:

```bash
cd stacks/spring-mysql
docker compose up -d
```

---

# Monitoring Example

The `spring-monitoring` stack includes:

- Spring Boot application
- Prometheus metrics scraping
- Grafana dashboards

Run:

```bash
cd stacks/spring-monitoring
docker compose up -d --build
```

Access:

```
Spring App   http://localhost:8080
Prometheus   http://localhost:9090
Grafana      http://localhost:3000
```

Default Grafana login:

```
admin / admin
```

---

# Requirements

- Docker
- Docker Compose

Install Docker:

https://docs.docker.com/get-docker/

---

# Improving This Repository

To improve the quality of this repository, consider adding the following:

## 1. Add a Full Development Stack

Provide a full backend development environment.

Example stack:

```
Spring Boot
MySQL
Redis
Kafka
```

Suggested folder:

```
stacks/full-backend
```

This helps developers start a full backend environment with a single command.

---

## 2. Add More Infrastructure Templates

Consider including commonly used infrastructure services.

Recommended additions:

```
compose/mongodb
compose/rabbitmq
compose/minio
compose/kafka-ui
compose/kibana
compose/node-exporter
compose/cadvisor
```

These services are frequently used in modern backend systems.

---

## 3. Add Documentation for Each Template

Add a small README inside each service folder.

Example:

```
compose/mysql/README.md
compose/redis/README.md
compose/kafka/README.md
```

Each README should include:

- What the service does
- Default ports
- How to run it
- Example usage

Example:

```bash
cd compose/mysql
docker compose up -d
```

This makes the repository easier to navigate and use.

---

# License

MIT License