---
transition: slide-up
---

# Managing Docker Networks

Docker provides powerful tools for networking, offering flexibility and control over how containers communicate.

## How to Work with Networks:

- **Creating Custom Networks:**
  Enhance communication control by creating isolated networks.
  ```bash
  docker network create --driver bridge my_network
  ```

- **Connecting Containers to Networks:**
  Attach containers to specific networks for controlled communication.
  ```bash
  docker run -d --name my_container --network my_network my_image
  ```

- **Isolating Containers:**
  Use the `none` network to completely isolate a container from external networks.
  ```bash
  docker run -d --name isolated_container --network none my_image
  ```

- **Leveraging the Host Network:**
  For performance-critical applications, use the host's network stack.
  ```bash
  docker run -d --name performance_container --network host my_image
  ```
```
