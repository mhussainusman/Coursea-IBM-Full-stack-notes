# Course 10: Getting Started with Containers, Kubernetes and OpenShift
## Module 1: Introduction to Containers w/ Docker, Kubernetes & OpenShift

### Key Concepts
- Containers encapsulate everything needed to build, ship, and run applications.
- Containers reduce deployment time and costs, improve resource utilization, automate processes, and support microservices.
- Major container platforms include Docker, Podman, LXC, and Vagrant.
- Docker is an open platform for developing, shipping, and running containerized applications.
- Docker architecture includes Docker client, Docker host, and container registry.
- Docker host manages Dockerfiles, images, containers, networks, storage volumes, plugins, and add-ons.
- Docker networks isolate container communications.
- Docker volumes and bind mounts persist data beyond container lifecycle.
- Plugins extend Docker functionality, e.g., storage plugins.

### Notes
Containers are software units that package an application and its dependencies together, enabling consistent and efficient deployment across different environments. They are especially useful for modern application architectures like microservices. Docker is a widely used container platform that simplifies container management through its client, host, and registry components. The Docker host stores essential objects such as images and containers, while networks and volumes help manage communication and data persistence. Plugins enhance Docker's capabilities by connecting to external resources.

### Code Examples
```dockerfile
# Example Dockerfile to create a simple container image
FROM python:3.8-slim
WORKDIR /app
COPY . /app
RUN pip install -r requirements.txt
CMD ["python", "app.py"]
```

### Cheat Sheet
| Concept | Syntax / Example | Description |
|---|---|---|
| Container | — | Encapsulates an application and its dependencies |
| Docker client | — | Interface to communicate with Docker host |
| Docker host | — | Runs Docker daemon and manages containers/images |
| Docker registry | — | Stores and distributes container images |
| Dockerfile | `FROM`, `WORKDIR`, `COPY`, `RUN`, `CMD` | Script to build container images |
| Volume | — | Persistent storage for containers |
| Network | — | Isolates container communication |
| Plugin | — | Extends Docker functionality |

### Glossary
- **Container**: A lightweight, standalone package that includes everything needed to run a piece of software.
- **Docker client**: The command-line interface used to interact with the Docker daemon.
- **Docker host**: The machine running the Docker daemon and managing containers.
- **Docker registry**: A repository for storing and distributing Docker images.
- **Volume**: A storage mechanism to persist data used by containers.
- **Plugin**: An add-on that extends Docker's capabilities, such as storage or network plugins.

### Summary
This module introduced containers as a method to package and run applications efficiently across environments. Docker, a leading container platform, was explained including its architecture and key components like images, containers, networks, and volumes. Understanding these basics sets the foundation for working with containerized applications.