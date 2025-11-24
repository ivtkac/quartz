---
created: 2025-11-13
title: mysqldump
tags:
  - man
  - mysql
aliases:
description: Створити логічний повний бекап MySQL
---
> [!info] Створює [[Логічні бекапи|логічні]] [[Повна резервна копія|повні бекапи]] у вигляді [[SQL]]-запитів.

> [!warning] За замовчуванням виводить на [[стандартні потоки|STDOUT]], таблиці блокуються ([[Теплі бекапи|теплий бекап]]).

```bash
mysqldump -u [user] -p[password] [database] > backup.sql
```

> [!tip] **Для InnoDB:** опція `--single-transaction` для дампу в межах однієї транзакції.

> [!example] Опції
> - `-A, --all-databases` - всі БД
> - `-B, --databases` - конкретні БД
> - `--add-drop-table` - додає DROP TABLE
> - `--no-data` - тільки структура
> - `--single-transaction` - одна транзакція
> - `--master-data` - інформація про binlog