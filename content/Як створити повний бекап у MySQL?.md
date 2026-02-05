---
created: 2025-11-13
title: Як створити повний бекап у MySQL?
tags:
  - mysql
  - backups
  - 🦮how-to
aliases:
links:
  - "[[xtrabackup]]"
  - "[[MySQL]]"
---
```bash
xtrabackup -u[user] -p[password] --backup --target-dir=/data/backups/full
```