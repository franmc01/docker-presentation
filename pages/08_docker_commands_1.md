---
level: 2
---

# Introducing Docker Commands

Having seen the variety of commands available, let's try out some of the most frequently used Docker commands.

```bash {all|1-2|4-5|7-8|10-11|13-14}
# Pull an image from Docker Hub
docker pull nginx

# Run a container from the nginx image
docker run -d --name my-nginx -p 8080:80 nginx

# List running containers
docker ps

# Stop the container named 'my-nginx'
docker stop my-nginx

# Remove the container named 'my-nginx'
docker rm my-nginx
```

<div class="absolute right-16 bottom-6 text-9xl animate-fade-in">
🚀
</div>