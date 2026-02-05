---
title: Getting the Docker version and information
created: 2025-12-11
tags:
  - 🦮how-to
  - docker
aliases:
---
- `docker --version` - version of [[Docker]] client, server, container
- `docker version --format '{{ .Server.Version }}'` - server version
- `docker version --format '{{ json. }}'` - for get specific key
- `docker info` - get info