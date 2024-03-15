---
transition: fade-out
hideInToc: true
---

# Docker Networking Types - Part 1

Docker provides various network types, each tailored for different needs, enhancing container communication and isolation.

### Bridge Network

- **Default network** when you run a container without specifying a network.
- Containers can communicate with each other while isolated from the host network.
- Use cases: Most applications needing communication between containers.


## Host Network

- Removes network isolation between the container and the Docker host, sharing the host’s networking namespace.
- Use cases: High-performance requirements where containers need to avoid network overhead.


<div class="absolute right-6 bottom-6 text-8xl animate-fade-in">
  🌉
</div>
