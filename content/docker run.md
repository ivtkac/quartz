---
title: Docker run
created: 2025-12-12
tags:
  - docker
aliases:
links:
  - "[[Docker]]"
---
docker run can be used with the following parameters:

- **-d runs** a container in the background and prints container ID
- **-P -** use it to publish all exposed ports to random ports
- **-p -** use it to publish a container's port(s) to the host
- **--restart** - use it to restart policy to apply when a container exits (default 'no')
- **-i -** use it to keep STDIN open even if not attached
- **-t -** use it to allocate a pseudo -TTY
- **--rm** - use it to automatically remove the container when it exits
- **-v -** use it to bind mount a volume
- **-e -** use it to set environment variables
- **--label** - use it to set metadata on a container
- **--log**-driver - use it to log driver for the container
- **-u -** use it to set a username or UID (<name|uid>[:<group|gid>])
- **-w -** use it to set the working directory inside the container
- **--entrypoint** - use it to overwrite the default ENTRYPOINT of the image