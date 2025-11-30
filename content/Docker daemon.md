---
title: Docker daemon (docker server)
created: 2025-11-30
tags:
  - docker
aliases:
---
> [!example] Functions
> - listening to [[Docker API]] requests
> - managing Docker objects ([[Docker images|images]],[[Docker containers|containers]], [[Docker networks|networks]], and [[Docker volumes|volumes]])
> - communicating with other [[daemon]]s for managing services

```mermaid
graph
A[Docker Daemon] 
B[Container]
C[Image] --> B
D[Dockerfile] --> C
```