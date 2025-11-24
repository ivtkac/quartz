---
created: 2025-11-22
title: Docker tagging images
tags:
  - docker
aliases:
---
> [!note] Any tag except for temporary (for develop) should be treated as **immutable**

- Automated builds should use some combination of:
	- timestamp when image was built
	- Build ID (from [[continuous integraty|CI]] system)
	- Commit hash of code used to build image
	- SemVer release version