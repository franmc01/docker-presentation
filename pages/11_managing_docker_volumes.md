---
transition: fade-out
---

# Managing Docker Volumes

Docker volumes are essential for persisting and sharing data across containers and the host, facilitating data management.

## How to Work with Volumes:

- **Creating a Standalone Volume:**
  Create volumes independently for flexible usage across containers.
  ```bash
  docker volume create my_volume
  ```

- **Attaching a Volume to a Container:**
  Use volumes for persistent data when running containers.
  ```bash
  docker run -d --name my_container -v my_volume:/app/data my_image
  ```

- **Direct Volume Creation When Running a Container:**
  Docker can automatically create a volume if it doesn't exist.
  ```bash
  docker run -d --name my_new_container -v another_volume:/app/config my_image
  ```
