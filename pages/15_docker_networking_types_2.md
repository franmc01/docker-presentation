---
transition: fade-out
---

# Docker Networking Types - Part 2

Continuing with Docker's network types, let's explore more options for advanced networking and isolation.

### None Network

- Disables all networking for a container. Essentially, the container is isolated from accessing any network.
- Use cases: Tight security requirements or testing scenarios where network access should be entirely blocked.



## Custom Networks

- Allows for creating user-defined networks which can be configured with specific drivers and options.
- Facilitates network segmentation and more granular control over container communication.
- Use cases: Microservices architecture where containers need to communicate securely and efficiently.


<div class="absolute right-4 bottom-6 text-8xl animate-fade-in">
  📡
</div>
