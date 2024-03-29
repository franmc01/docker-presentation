---
transition: slide-left
---

<div class="text-center big-title">
  Dockerfile: The Blueprint of Docker Images 🏗️
</div>

<style>
.big-title {
  font-size: 4rem;
  font-weight: bold;
  margin-top: 3rem;
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
transition: slide-left
---

# Comprehending Dockerfile

A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image. Using a Dockerfile is the most common method for creating a Docker container.

## Why Use a Dockerfile?

- **Automation**: Automate the image creation process, making it reproducible and consistent.
- **Version Control**: Track changes in your Docker environment in a way that’s transparent and maintainable.
- **Customization**: Customize and share images according to your application's specific needs.

## Key Commands

- Build: `docker build -t <tag> .`
- History: `docker history <image>`
- Image Building: `docker build [OPTIONS] PATH | URL | -`

<div class="absolute right-16 bottom-6 text-9xl animate-fade-in">
  📜
</div>

---
transition: slide-left
---

# Dockerfile Fundamentals

The Dockerfile defines the steps to create an image:

- **FROM**: Base image to start the build.
- **RUN**: Execute commands.
- **COPY/ADD**: Add files from local to the image.
- **EXPOSE**: Ports to expose.
- **CMD**: Default command at runtime.

Simple, yet powerful commands to package your application.

<div class="absolute right-16 bottom-6 text-9xl animate-fade-in">
  🏗️
</div>

---
transition: slide-left
---

# Advanced Dockerfile Instructions

To refine image creation:

- **ENV**: Set environment variables.
- **ARG**: Arguments for building images.
- **ENTRYPOINT**: Configure a container that will run as an executable.
- **USER**: Set the user name or UID.
- **WORKDIR**: Set the working directory.

More tools for a fine-tuned Docker experience.

<div class="absolute right-16 bottom-6 text-9xl animate-fade-in">
  🔧
</div>

---
transition: slide-left
---

# Simple Dockerfile Example for a Web Application

Let's look at a basic Dockerfile for a Node.js web app.

```bash {all|1-2|3-4}
# Start with the official Node image
FROM node:18

# Set the working directory in the container
WORKDIR /app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./
RUN npm install

# Bundle app source
COPY . .

# Bind to port 3000
EXPOSE 3000

# Define the command to run the app
CMD ["node", "app.js"]