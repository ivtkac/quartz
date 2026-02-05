---
created: 2025-11-14
title: how to configure static route?
tags:
  - 🦮how-to
  - OS/Linux
  - network
aliases:
links:
  - "[[ip command]]"
---
```bash
$ sudo ip route add 192.0.2.1/24 via 10.0.0.2 dev eth0
```