---
created: 2025-11-23
title: How to delete all docker images and container?
tags:
  - 🦮how-to
  - docker
aliases:
links:
  - "[[Docker]]"
---
To delete all containers:

```bash
docker rm $(docker ps -a -q -f status=exited)
```

