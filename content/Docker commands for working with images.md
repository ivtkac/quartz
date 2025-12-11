---
title: Docker commands for working with images
created: 2025-12-11
tags:
  - docker
aliases:
lang:
---
The following [[Docker]] commands are used for working with Docker [[docker image|images]]:

- **docker images** shows all existing images
- **docker import** creates an image from a tarball
- **docker build** this command creates an image from a Dockerfile.
- **docker commit** creates an image from a container, pausing it temporarily if it is running.
- **docker rmi** removes one or more images from the host node.
- **docker load** loads an image from a tar archive as STDIN, including images and tags.
- **docker save** saves an image to a tar archive stream to STDOUT with all parent layers, tags and versions.
- **docker history** shows the history of an image.
- **docker tag** tags an image to a name (local or a registry one). The most common use of this command is to tag an image to send it to another repository since the repository name is always part of the name of the image in it.