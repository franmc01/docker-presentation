---
level: 2
---

# Introducing Docker Commands

Explore commonly used Docker commands through a practical demonstration.

```bash {all|1-2|4-5|7-8|10-11|13-14}
# Pull an image from Docker Hub
docker pull hello-world

# Run a container from the hello-world image
docker run --name first-container hello-world

# List running containers
docker ps -a

# Stop the container named 'first-container'
docker stop first-container

# Remove the container named 'first-container'
docker rm first-container
```

<div class="absolute right-16 bottom-6 text-9xl animate-fade-in">
🚀
</div>