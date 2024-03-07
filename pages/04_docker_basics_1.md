---
transition: slide-up
---

# Docker Basics - Part 1

Let's familiarize ourselves with some foundational concepts of Docker.

<v-clicks>

<v-click>

### [Image](https://docs.docker.com/get-started/overview/#docker-objects)

A Docker **Image** is a lightweight, standalone, executable package that includes everything needed to run a piece of software, including the code, a runtime, libraries, environment variables, and config files.

</v-click>

<v-click>

### [Container](https://docs.docker.com/get-started/overview/#docker-objects)

A **Container** is a runtime instance of an image—what the image becomes in memory when executed, that is, an isolated environment in which the application runs.

</v-click>

<v-click>

### [Volumes](https://docs.docker.com/storage/volumes/)

**Volumes** are used in Docker to persist data generated by and used by Docker containers.

</v-click>

</v-clicks>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>