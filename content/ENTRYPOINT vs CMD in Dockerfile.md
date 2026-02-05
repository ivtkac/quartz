---
title: ENTRYPOINT vs CMD in Dockerfile
created: 2025-12-11
tags:
  - docker
  - question
aliases:
links:
  - "[[Docker]]"
---
**`CMD`** sets a default command or arguments that can be easily overridden by the `docker run` command line, while **`ENTRYPOINT`** defines the main command that _always_ runs, and any `docker run` arguments are appended to it as parameters