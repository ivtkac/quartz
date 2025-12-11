---
created: 2025-11-22
title: Dockerfile
tags:
  - docker
aliases:
doc: https://docs.docker.com/reference/dockerfile/
---
> [!tldr]
> **Dockerfile** — текстовий файл, який містить команди, які користувач може викликати у командному рядку для створення образу.

> [!example] Recipe
> 1. Start with OS
> 2. Install language runtime
> 3. Install application deps
> 4. Set up execution environment
> 5. Run application

## Commands

- **RUN** allows you to execute any commands in a new layer on top of the current image and commit the results.
- **CMD** provides defaults for a container that is being executed.
- **EXPOSE** informs Docker that the container connects to the specified network ports at runtime. Please note that the command does not make any ports accessible.
- **ENV** sets the environment variable.
- **ADD** copies new files, directories or a remote file to the container. It invalidates caches.
- **COPY** copies new files or directories to the container.
- **ENTRYPOINT** configures a container that will run as an executable.
- **VOLUME** creates a mount point for externally mounted volumes or other containers.
- **USER** sets the username for the following RUN / CMD / ENTRYPOINT commands.
- **WORKDIR** sets the working directory.
- **ARG** defines a build-time variable.
- **ONBUILD** adds a trigger instruction when the image is used as the base for another build.
- **STOPSIGNAL** sets the system call signal that will be sent to the container to exit
- **LABEL** applies key/value metadata to your images, containers or daemons


## Bad dockerfile

```dockerfile
FROM ubuntu

RUN apt update && apt install nodejs npm -y

COPY . .

RUN npm install

CMD ["npm", "run", "dev"]

```

## Good docker file

```dockerfile
FROM node:19.6-alpine

WORKDIR /usr/src/app

ENV NODE_ENV=production

COPY package*.json ./

RUN --mount=type=cache,target=/usr/src/app/.npm \
  npm set cache /usr/src/app/.npm && \
  npm ci --only=production

USER node

COPY --chown=node:node ./src .

EXPOSE 3000

CMD ["node", "index.js"]
```