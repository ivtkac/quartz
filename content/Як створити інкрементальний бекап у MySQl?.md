---
created: 2025-11-13
title: Як створити інкрементальний бекап у MySQl?
tags:
  - 🦮how-to
  - backups
  - mysql
aliases:
---
```bash
xtrabackup --backup --target-dir=/data/backups/inc1 --incremental-basedir=/data/backups/full
```

Створити ланцюжок інкрементальних бекапів:

```bash
xtrabackup --backup --target-dir=/data/backups/inc2 --incremental-basedir=/data/backups/inc1
```

> [!warning] Чим довший ланцюжок, тим довше відновлення.