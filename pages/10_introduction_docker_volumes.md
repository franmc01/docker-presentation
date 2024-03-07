---
transition: slide-up
---

# Understanding Docker Volumes

Docker volumes are essential for data persistence across container lifecycles, enabling data to survive beyond container rebuilds and deletions.

## Why Use Volumes?

- **Data Persistence**: Keep data across container updates.
- **Data sharing**: Easily share data between multiple containers.
- **Data security**: Keep sensitive information out of your container's image.


## Key Commands

- Create: `docker volume create <name>`
- List: `docker volume ls`
- Inspect: `docker volume inspect <name>`
- Remove: `docker volume rm <name>`


<div class="absolute right-16 bottom-6 text-9xl animate-fade-in">
  📦
</div>