---
transition: slide-up
---

<div class="text-center">
  <span class="big-title">Now, Onto the Exciting Part...</span>
  <div class="mt-4">Get ready for orchestration with <strong>Docker Compose</strong> 🎼</div>
</div>

<style>
.big-title {
  font-size: 4rem;
  color: #0dbd8b; /* A Docker-inspired color */
  font-weight: bold;
}

.text-center {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  text-align: center;
}

.mt-4 {
  margin-top: 1rem;
  font-size: 1.5rem;
}
</style>

---
transition: slide-up
---

# What is Docker Compose?

Docker Compose simplifies managing multi-container Docker applications. With a single command, create and start all services from your `docker-compose.yml` file, making both development and deployment workflows more efficient.

## Key Features

- **Single-file service definition**: Organize your application's services, networks, and volumes in one file.
- **One-command setup**: Start your entire application stack with `docker-compose up`.
- **Easy cleanup**: Remove all components with `docker-compose down`.

<div class="absolute bottom-0 right-0 mb-4 mr-4 text-9xl">
  🌐
</div>


---
transition: slide-up
---

# Docker Compose: Basic Concepts

Master Docker Compose's building blocks to orchestrate applications with ease.

- **Services**: Components like web servers and databases.
- **Networks**: Communication channels between containers.
- **Volumes**: Persistent or shared data management.

These concepts enable the design and operation of complex applications.

<div class="absolute bottom-0 right-0 mb-4 mr-4 text-9xl">
  🏗️
</div>


---
transition: slide-up
---

# Docker Compose: Expanded Use Cases

Docker Compose facilitates:

- **Local development**: Simulate production environments seamlessly.
- **Automated testing**: Run tests in consistent, containerized environments.
- **CI/CD pipelines**: Automate the build and test phases of applications.
- **Multi-service apps**: Coordinate the launch and interaction of services like front-ends, back-ends, and databases.
- **Rapid prototyping**: Quickly stand up and tear down complex app stacks.

Harness Docker Compose for efficient multi-container orchestration.

<div class="absolute bottom-0 right-0 mb-4 mr-4 text-9xl">
  💼
</div>


---
transition: slide-up
---

# Docker Compose Real Example: Part 1

Setting up our Vue.js application within a Docker container.

```yaml
version: '3.9'

services:
  vue-app:
    build:
      context: ./vue-app
      dockerfile: Dockerfile
    ports:
      - "5000:80"
    container_name: vue-app-container
    networks:
      - tt-network-compose
```

This part of our `docker-compose.yml` focuses on building and running the Vue app, exposing it on port 5000.

<div class="absolute bottom-0 right-0 mb-4 mr-4 text-6xl">
  🌐
</div>


---
transition: slide-up
---

# Docker Compose Real Example: Part 2

Continuing with our NestJS app and custom network setup.

```yaml
services:
  nest-app:
    build:
      context: ./nest-app
      dockerfile: Dockerfile
    ports:
      - "5001:3000"
    container_name: nest-app-container
    networks:
      - tt-network-compose

networks:
  tt-network-compose:
    name: tt-network-compose
    driver: bridge
```

Here we add our NestJS app to the Docker Compose configuration, exposing it on port 5001, and define the `tt-network-compose` network.

<div class="absolute bottom-0 right-0 mb-4 mr-4 text-6xl">
  🛠️
</div>


---
transition: slide-up
---

# Key Takeaways

- **Docker simplifies the deployment process** by packaging applications and their dependencies into containers.
- **Docker Compose** allows for easy management of multi-container applications, defining services, networks, and volumes in a single file.
- **Multistage builds** optimize Docker images, keeping them lean and secure.
- Combining these tools **enhances development workflows** and **streamlines CI/CD pipelines**.

Embrace these Docker practices to boost efficiency and productivity in your projects.

<div class="absolute bottom-0 right-0 mb-4 mr-4 text-9xl">
  📚
</div>

---
layout: default
---

# Further Learning Resources

Dive deeper into the world of Docker, containers, and Kubernetes with these comprehensive resources:

- **[Docker Official Documentation](https://docs.docker.com/)**: The go-to place to start your Docker journey.
- **[Kubernetes.io](https://kubernetes.io/)**: The official Kubernetes documentation and learning resources.
- **[A Cloud Guru](https://acloudguru.com/)**: Offers courses on Docker, Kubernetes, and cloud technologies.
- **[Awesome Docker](https://github.com/veggiemonk/awesome-docker)**: A curated list of Docker resources and projects on GitHub.
- **[Play with Docker](https://labs.play-with-docker.com/)**: A free, interactive Docker playground.
- **[Play with Kubernetes](https://labs.play-with-k8s.com/)**: A similar interactive experience for Kubernetes.

These resources provide a wealth of information for both beginners and experienced users looking to enhance their skills.

<div class="absolute bottom-0 right-0 mb-4 mr-4 text-9xl">
  📚
</div>
