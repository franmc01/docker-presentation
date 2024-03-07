---
level: 2
---

# Advanced Docker Usage: Env Variables and Ports

Now let's see how to set environment variables and expose ports when running containers.

```bash
# Run a PostgreSQL container with an environment variable
docker run -d --name dev-postgres -e POSTGRES_PASSWORD=mysecretpassword postgres

# Alternate syntax, same effect
docker run -d --name dev-postgres \
  -e POSTGRES_PASSWORD=mysecretpassword postgres

# Expose an Nginx container's port to make it accessible on the host
docker run -d --name my-nginx -p 8080:80 nginx


# Start an app container with multiple environment variables
docker run -d --name my-widget -e VAR1=value1 -e VAR2=value2 myapp
```

Try these out:

- PostgreSQL Database: Create a container with a secure password.
- Nginx Web Server: Make a simple web server accessible through port 8080.
- Custom App Container: Demonstrate configuring an app with multiple environment settings.