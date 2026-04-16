# Docker Lab

Docker Lab is the containerization track here. It starts with the mechanics of images and containers, then moves into Dockerfiles, Compose-driven multi-service environments, persistence, networking, and a small Podman branch for contrast.

## Project layout

The area is organized around a few practical projects rather than one single application:

- `project1/` focuses on image building, base images, and command execution behavior
- `project2/` is the most substantial exercise: a Dockerized Django application that grows from a single container into a Compose stack with PostgreSQL, custom networking, and persistent storage
- `project3/` shifts toward Podman-oriented deployment work
- `project-extra-jenkins-as-docker-container/` captures the separate thread of running Jenkins as a containerized service

The older command notes and screenshots still exist in the history of this area, but the real value here is the progression from isolated container commands into a small multi-service application environment.

## Technical focus

The Docker material covers the pieces that tend to matter first in real usage:

- image creation with `Dockerfile`
- container lifecycle and process model
- port publishing and runtime inspection
- multi-service orchestration with Compose
- service discovery and bridge networking
- persistent database volumes
- application plus database bootstrapping
- containerizing operational tooling such as Jenkins

`project2/` is especially useful because it turns container concepts into a real application shape: Django app, environment variables, PostgreSQL, Compose startup order, network isolation, and state persistence.

## Local workflow

Work from the specific project you want to run.

Typical commands in this area are:

```bash
docker build -t image-name .
docker compose up -d
docker compose down
docker exec -it <container> sh
```

The exact commands vary by project, but the structure of the area makes it easy to move from image-level basics into a more realistic application stack.

## Why it matters

Docker Lab is valuable because it turns container ideas into platform instincts. It is where packaging, process boundaries, ports, networks, and data persistence stop being abstract platform terms and start becoming concrete operational behavior.
