---
title: How to create RAID in linux?
created: 2025-12-13
tags:
  - 🦮how-to
  - OS/Linux
  - filesystem
aliases:
lang:
---
```bash
sudo mdadm --create --verbose /dev/md1 --level=1 --raid-devices=2
```