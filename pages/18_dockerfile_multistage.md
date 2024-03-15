---
transition: slide-left
---

<div class="text-center big-title">
  Docker Multistage Builds: Optimize Your Images 🚀
</div>

<style>
.big-title {
  font-size: 2rem;
  font-weight: bold;
  margin-top: 1.5rem;
  color: #FFFFFF;
}

.text-center {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  text-align: center;
}
</style>


---
layout: default
---

# Docker Multistage Build for a NestJS App

Using a multistage build process to create a lean and optimized Docker image for a NestJS application.

```bash {all}
# Stage 1: Build the application
FROM node:18-alpine AS builder
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Stage 2: Set up the production environment
FROM node:18-alpine
WORKDIR /usr/src/app
COPY --from=builder /usr/src/app/dist ./dist
COPY --from=builder /usr/src/app/node_modules ./node_modules
EXPOSE 3000
CMD ["node", "dist/main"]
```
---
layout: default
---

# Docker Multistage Build for a Node App

Using a multistage build process to create a lean and optimized Docker image for a Vue application.

```bash {all}
# Stage 1: Build the Vue.js application
FROM node:16-alpine as build-stage
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Stage 2: Serve the application using nginx
FROM nginx:stable-alpine as production-stage
COPY --from=build-stage /app/dist /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```