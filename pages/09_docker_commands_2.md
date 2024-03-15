---
level: 2
---

# Advanced Docker Usage: Env Variables and Ports

Now let's see how to set environment variables and expose ports when running containers.

```bash
# Run an Nginx container, exposing port 8080 on the host
docker run -d --name my-nginx -p 8080:80 nginx

# Run a PostgreSQL container, exposing port 5432, with custom user and password
docker run -d --name dev-postgres -e POSTGRES_USER=team -e POSTGRES_PASSWORD=time -p 5432:5432 postgres

# Run a PostgreSQL container with environment variables, in multiline for clarity
docker run -d --name dev-postgres \
  -e POSTGRES_USER=team \
  -e POSTGRES_PASSWORD=time \
  -p 5432:5432 \
  postgres

# Run a command in PowerShell, multiline syntax
docker run -d --name dev-postgres `
  -e POSTGRES_USER=team `
  -e POSTGRES_PASSWORD=time `
  -p 9090:5432 `
  postgres

```