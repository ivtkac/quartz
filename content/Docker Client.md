---
title: Docker Client (docker cli)
created: 2025-11-30
tags:
  - docker
aliases:
---
> [!tldr]
> **Docker client** is the primary way of interacting with [[Docker]].

## Options

> [!example] Options
> - `-d` —  run as background
> - `--entrypoint` — override entrypoint
> - `--env`, `-e`, `--env-file` —  pass [[змінні оточення|Environment variables]]
> - `--init` — spawn process as subprocess  (if app manage subprocesses itself)
> - `--interactive`, `-i`, `--tty`, `-t` — run tty session
> - `--mount`, `--volume`, `-v` — volume
> - `--name` — provide specific name for container
> - `--network`, `--net` — connect to specific network
> - `--platform` — which on architecture run
> - `--publish`, `-p` — ports
> - `--restart` — if exit container restart it
> - `--rm` — remove after exit

> [!tip] `docker scout` — check vulnerabilies

## Notes

> [!note]
> - client sends a command to [[daemon]] and carries them out
> - can communicate with one or more daemon
> - each commands use the [[Docker API]]