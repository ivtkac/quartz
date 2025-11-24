---
created: 2025-11-23
title: How to delete all docker images and container?
tags:
  - 🦮how-to
  - docker
aliases:
---
To delete all containers:

```bash
docker rm -vf $(docker ps -aq)
```

To delete all the images:

```bash
docker rmi -f $(docker images -aq)
```