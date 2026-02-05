---
created: 2025-11-13
title: Як відновити дані у MySQL через xtrabackup?
tags:
  - mysql
  - backups
  - 🦮how-to
aliases:
links:
  - "[[xtrabackup]]"
---

> [!warning] Бекап потрібно підготувати перед відновленням, бо "гарячий" дамп не є цілісним.

> [!example]- Підготовка повного бекапу
> ```bash
> xtrabackup --prepare --target-dir=/data/backups/full
> ```

> [!example]- Підготовка інкрементального ланцюжка
> ```bash
> xtrabackup --prepare --apply-log-only --target-dir=/data/backups/full
> xtrabackup --prepare --apply-log-only --target-dir=/data/backups/full --incremental-dir=/data/backups/inc1
> xtrabackup --prepare --target-dir=/data/backups/full --incremental-dir=/data/backups/inc2
> ```

> [!warning] `--apply-log-only` на всіх кроках окрім останнього.