---
title: Storing files in Docker
created: 2025-12-13
tags:
  - docker
aliases:
---
There are **three** options in [[Docker]] to store data:

- **bind mount** are stored on the host system (process outside docker can change it)
- **volume** are stored in specific area of host [[Файлова система|filesystem]] (`/var/lib/docker/volumes`) (process outside docker should not change it)
- **tmpfs mount** (only for Linux) are stored only in the memory on the host system and are not written to the host filesystem