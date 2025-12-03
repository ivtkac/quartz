---
title: Контейнер
created: 2025-11-30
tags:
  - docker
aliases:
  - container
---
> [!tldr]
> **Container** is a runnable instance of [[docker image|image]].

> [!note] By default **container** is isolated from others containers and even host.

> [!example] Includes:
> - [[Файлова система|filesystem]] (some flavor of  Linux)
> - any software installed on top of this filesystem
> - additional runtime things like external volumes or ports

> [!example] Docker provides:
> - **[[namespaces]]**: a process in the container shouldn't see other processes running and should be the only process in system
> - **[[cgroups|control groups]]**: need for managing system resources
> - [[chroot]]: a process in the container should see/use only required parts of the filesystem
> - **process capabilities**: process should have enough [[Права доступу у Linux|permissions]] to manage/use kernel
> - 