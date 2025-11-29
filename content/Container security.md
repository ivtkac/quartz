---
created: 2025-11-23
title: Container security
tags:
  - docker
  - containerzation
aliases:
---
- vulnerabilities exist in your image that an attacker could exploit?
	- keep attack surface area as small as possible:
		- use minimal base images (multi-stages=key enabler)
		- don't install things you don't need (like dev deps)
	- scan images
	- use users with minimal permissions
	- keep sensitive info out of images
	- sign and verify images
	- use fixed image tags
		- either pin major.minor (allows patch fixes to be integrated)
		- pin specific image hash
- if compromise a container, what can they do? how difficulty will it be to move laterally?
	- docker daemon ([[dockerd]])
		- start with `--userns-remap` option (https://docs.docker.com/engine/security/userns-remap/)
	- individual containers:
		- use read only filesystem if writes are not needed
		- `--cap-drop=all`, then `--cap-add` anything you need
		- limit cpu, memory with `--cpus="0.5" --memory 1024m`
		- use `--security-opt`
			- seccomp profiles (https://docs.docker.com/engine/security/seccomp/)
			- apparmor profiles  (https://docs.docker.com/engine/security/apparmor/)