# docker-templates

Reusable Dockerfiles, Docker Compose templates, and multi-service stacks for backend development.

## Structure

- `dockerfiles/`
  - Single application container templates
  - Example: Spring Boot, Node.js, Python

- `compose/`
  - Single-service Docker Compose templates
  - Example: MySQL, Redis, Nginx

- `stacks/`
  - Multi-service Docker Compose templates
  - Example: Spring Boot + MySQL, Spring Boot + MySQL + Redis

## Included

### Dockerfiles
- Spring Boot
- Node.js
- Python

### Compose
- MySQL
- Redis
- Nginx

### Stacks
- Spring Boot + MySQL
- Spring Boot + MySQL + Redis

## Usage

### Run a single service
```bash
cd compose/redis
docker compose up -d

## Run a stack
cd stacks/spring-mysql
docker compose up -d

## Notes
	•	Copy .env.example to .env when needed.
	•	Update ports, passwords, and volume names for your own environment.
	•	These templates are intended as starting points, not production-ready defaults.

---

# 2. .gitignore

`.gitignore`

```gitignore
.env
.env.*
!.env.example

*.log
logs/
data/
tmp/

node_modules/
dist/
build/
target/

.idea/
.vscode/
.DS_Store
