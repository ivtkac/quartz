---
title: How to add new hard disk to an existing RAID?
created: 2025-12-13
tags:
  - 🦮how-to
  - OS/Linux
  - filesystem
aliases:
lang:
links:
  - "[[mdam]]"
  - "[[RAID]]"
---
```bash
mdadm <device> --add /dev/new-disk
mdadm <device> --grow --raid-devices=3
```