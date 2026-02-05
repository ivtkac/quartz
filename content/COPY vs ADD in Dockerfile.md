---
title: COPY vs ADD in Dockerfile
created: 2025-12-11
tags:
  - docker
  - question
aliases:
lang:
links:
  - "[[Docker]]"
  - "[[Dockerfile]]"
---
The difference between **COPY** and **ADD** is that **ADD** can work with archieve files, it can copy tarball files inside container and extract the content. The ADD directive also can copy directories or remote file URLs.