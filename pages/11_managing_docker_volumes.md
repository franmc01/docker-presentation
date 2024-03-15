---
transition: fade-out
hideInToc: true
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

---
transition: fade-out
hideInToc: true
---

# Real-World Example

Dive into a practical use case of Docker volumes by integrating one with a PostgreSQL container for data persistence.

### Steps:

- **Create a Docker Volume:**
  This volume will store PostgreSQL data persistently.
  ```bash
  docker volume create pg_data
  ```

- **Run PostgreSQL Container with the Volume:**
  Specify the volume to use for PostgreSQL data to ensure persistence.
  ```bash
  docker run -d \
    --name dev-postgres \
    -e POSTGRES_PASSWORD=mysecretpassword \
    -v pg_data:/var/lib/postgresql/data \
    -p 5432:5432 \
    postgres
  ```
<div class="absolute bottom-0 right-0 mb-4 mr-4 text-9xl">
  💾
</div>
