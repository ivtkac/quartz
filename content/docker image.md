---
title: Образ docker
created: 2025-11-30
tags:
  - docker
aliases:
---
> [!tldr]
> An **image** is a read-only template with instructions for creating a [[docker container]].

> [!example] Creation
> Images are generated using the `build` command that runs script described in a [[Dockerfile]]. Images will create a container when run.

> [!example] Storing
> Images are stored in [[Docker Registry]] (https://hub.docker.com)

> [!example] Sending
> As images can become quite large, they are designed to be composed of layers of other images, allowing a minimal amount of data to be sent when transferring images over the [[Мережа|]] 