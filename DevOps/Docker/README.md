Docker is a platform for developing, shipping, and running applications in **containers** -- lightweight, standalone packages that include everything an app needs to run (code, runtime, libraries, system tools). "It works on my machine" becomes "it works everywhere."

- Docker
  - Introduction 🔴
    - What Docker is (containerization platform)
    - Container vs Virtual Machine 🔴
      - Container: shares the host OS kernel, MB-sized, starts in seconds
      - VM: full guest OS, GB-sized, starts in minutes
    - Why Docker won (reproducible builds, isolation, portability)
  - Core concepts 🔴
    - **Image** -- read-only template (blueprint)
    - **Container** -- running instance of an image
    - **Dockerfile** -- recipe to build an image
    - **Registry** -- where images live (Docker Hub, GitLab, private)
    - **Volume** -- persistent data
    - **Network** -- communication between containers
  - Installation 🔴
    - Docker Desktop (macOS, Windows) -- uses WSL2 on Windows
    - Docker Engine (Linux)
  - The Dockerfile 🔴
    - ```dockerfile
      FROM node:20-alpine
      WORKDIR /app
      COPY package*.json ./
      RUN npm ci --production
      COPY . .
      EXPOSE 3000
      CMD ["node", "server.js"]
      ```
    - Instructions: `FROM`, `RUN`, `COPY`, `WORKDIR`, `EXPOSE`, `CMD`, `ENTRYPOINT`, `ENV`, `ARG`
  - Basic commands 🔴
    - `docker build -t myapp .`
    - `docker images`
    - `docker run -p 3000:3000 myapp`
    - `docker ps` (running containers)
    - `docker ps -a` (all containers)
    - `docker stop <id>` / `docker rm <id>`
    - `docker rmi <image>`
    - `docker logs <id>`
    - `docker exec -it <id> sh` (enter a running container)
  - Docker Hub and registries 🔴
    - `docker pull node:20`
    - `docker push yourname/myapp`
    - Tags and versioning
  - Volumes (persistent data) 🔴
    - `docker run -v /host/path:/container/path myapp`
    - Named volumes: `docker volume create`
    - Why containers are ephemeral (data is lost without volumes)
  - Networks 🔴
    - Bridge (default, isolated)
    - Host (uses host network)
    - Custom networks for multi-container apps
  - **Docker Compose** 🔴 (multi-container orchestration)
    - `docker-compose.yml`
    - ```yaml
      services:
        web:
          build: .
          ports: ["3000:3000"]
        db:
          image: mysql:8
          environment:
            MYSQL_ROOT_PASSWORD: secret
      ```
    - `docker compose up -d` / `docker compose down`
  - Multi-stage builds 🔴 (smaller images)
    - Build stage + runtime stage
  - Image optimization 🔴
    - Use Alpine or distroless base images
    - `.dockerignore`
    - Layer caching (copy `package.json` before source)
  - Docker in production 🔴
    - Health checks (`HEALTHCHECK`)
    - Restart policies (`--restart unless-stopped`)
    - Resource limits (`--memory`, `--cpus`)
    - Non-root user in container
  - Docker and orchestration 🔴
    - Docker Compose (single host)
    - Kubernetes / Swarm (multi-host, production)
  - Common use cases
    - Local development (Node + MySQL + Redis in one command)
    - CI/CD pipelines (reproducible builds)
    - Microservices deployment

---
🔴 Very Important
