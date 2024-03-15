---
transition: fade-out
hideInToc: true
---

# Real-World Example: (Part 1)

Creating a custom Docker network and launching PostgreSQL and PgAdmin containers.

```bash
# Create a Custom Network
docker network create --driver bridge my_custom_network

# Run PostgreSQL Container
docker run -d \
  --name dev-postgres \
  --network my_custom_network \
  -e POSTGRES_PASSWORD=mysecretpassword \
  postgres

# Run PgAdmin Container
docker run -d \
  --name my-pgadmin \
  --network my_custom_network \
  -e PGADMIN_DEFAULT_EMAIL=user@example.com \
  -e PGADMIN_DEFAULT_PASSWORD=root \
  -p 80:80 \
  dpage/pgadmin4
```

---
transition: fade-out
hideInToc: true
---

# Real-World Example: (Part 2)

Connecting to PostgreSQL from PgAdmin within our custom Docker network.

## Steps to Connect:

1. Navigate to PgAdmin: `http://localhost`
2. Add a new server with these details:
   - **Name:** `dev-postgres`
   - **Host name/address:** `dev-postgres` (Use the container's name)
   - **Username:** `postgres`
   - **Password:** `mysecretpassword`

<div class="absolute bottom-0 right-0 mb-4 mr-4 text-9xl">
  🌐🔧
</div>

---
transition: fade-out
hideInToc: true
---

# Troubleshooting: "Name Does Not Resolve"

Encountering issues is part of the learning process. Here's how to tackle common network-related errors:

- **Error Message**: "Unable to connect: name does not resolve."
  - **Solution**: Verify both containers are indeed in `my_custom_network`.
  - **Tip**: Use the container name (`dev-postgres`) as the host name in your PgAdmin server settings.

Remember, encountering errors is an opportunity to deepen your understanding. Mistakes are our friends in the learning journey. Embrace them, and don't hesitate to experiment and explore solutions. 🧭👨‍🔧
