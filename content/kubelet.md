---
title: kubelet
created: 2025-12-18
tags:
  - k8s
aliases:
---
- focused on running containers
- runs on all [[k8s node|Nodes]]
- [[k8s pod|Pod]]s are defined by a JSON or YAML file (called a **Pod Manifest**)
- has internal http server
	- read-only view on port 10255
	- kubelet URLs that you can curl
	- `/health` - health check
	- `/pods`
	- `/spec`
- handles (docker build, docker pull, docker run)